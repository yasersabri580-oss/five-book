# IRON BREACH — GROUND OBJECT & FLOOR TILE ASSET PIPELINE

### Production-Ready Ground Object Design Document

---

## SCOPE

This pipeline covers all **ground objects, floor tiles, and terrain surfaces** for IRON BREACH Chapter 1.

**INCLUDED:**
- Floor tiles (concrete, cracked, metal, dirt, grass, rubble, mud)
- Road surfaces (asphalt, dirt track)
- Transition tiles (edge tiles, surface-to-surface transitions)
- Surface decals (shadow decals, small surface details)

**NOT INCLUDED:**
- Props, walls, or 3D environment objects (see `EnvironmentObjects/PIPELINE.md`)
- Characters, vehicles, or VFX
- Skyboxes or full scene backgrounds

---

## STYLE REFERENCE

- **Visual style:** 2.5D isometric, dieselpunk / near-future militarism
- **Color palette:** Desaturated greens, greys, oranges, dirty earth tones. Sharp red/yellow danger highlights reserved for interactive props, not ground
- **Camera:** Fixed isometric, 30-degree pitch, Southeast-facing (viewer looks from above-southeast toward northwest)
- **Art style:** Stylized but readable. Crisp 2px black border on elevated objects only. Ground tiles use subtle soft edges — no hard outlines on flat surfaces. NOT pixel art. NOT full 3D
- **Readability rule:** Ground must NOT compete visually with characters, props, or HUD. Ground is always the lowest visual layer

---

## DESIGN RULES

1. **Ground supports gameplay readability first.** Characters and cover objects must pop against the ground.
2. **Ground tiles must be clearly distinct from each other.** Concrete ≠ dirt ≠ metal. Silhouette and color contrast at game resolution.
3. **Tiles are modular.** All floor tiles tile seamlessly in all 4 isometric directions.
4. **Tonal range is narrow.** Ground palettes are deliberately desaturated. Avoid vibrant greens or yellows on ground — save those for enemy faction highlights and UI.
5. **Lighting is baked.** Top-left directional soft light baked into the tile texture. No runtime ground lighting needed.
6. **Variation without noise.** Each tile set includes 2–4 variants to prevent repetitive tiling. Variants must not break the tile seam.
7. **Ground height is zero.** All floor tiles are flat — no elevation or raised edges. Props provide height; ground provides context.
8. **Transition tiles** must blend naturally between adjacent surface types without visual jarring at seams.
9. **Performance:** Ground tiles rendered as a Tilemap layer behind all sprites. No transparency needed on base tiles. Decal overlays use transparency.

---

## TILE SPECIFICATION

| Property | Value |
|---|---|
| Base tile size | 64×32 px (isometric rhombus — standard isometric tile unit) |
| Generated at | 128×64 px (2× for editor preview and high-DPI) |
| Tile shape | Isometric diamond (flat top, flat bottom, two slanted sides) |
| Tiling | All base tiles: seamless in all 4 isometric directions |
| Transparency | Base tiles: no transparency (opaque). Decals: transparent PNG |
| Outline | NO outline on base ground tiles. Outline reserved for props/characters |
| Shadow | Prop shadows are cast onto ground as decal sprites — not baked into tile |

---

## SURFACE CATEGORY LIST

### 1. FLOOR TILES
Base surface materials — the primary gameplay ground type.

| Surface | File |
|---|---|
| ConcreteFloor | `FloorTiles/ConcreteFloor.md` |
| CrackedConcrete | `FloorTiles/CrackedConcrete.md` |
| MetalFloor | `FloorTiles/MetalFloor.md` |
| DirtGround | `FloorTiles/DirtGround.md` |
| GrassPatch | `FloorTiles/GrassPatch.md` |
| RubbleGround | `FloorTiles/RubbleGround.md` |
| MudGround | `FloorTiles/MudGround.md` |

### 2. ROAD SURFACES
Traversal-specific surfaces for mission roadways and vehicle tracks.

| Surface | File |
|---|---|
| AsphaltRoad | `RoadSurfaces/AsphaltRoad.md` |
| DirtTrack | `RoadSurfaces/DirtTrack.md` |

### 3. TRANSITION TILES
Tiles that blend adjacent surface types into each other without visual jarring.

| Surface | File |
|---|---|
| EdgeAndTransitionTiles | `TransitionTiles/EdgeAndTransitionTiles.md` |

### 4. SURFACE DECALS
Sprite-based overlays placed on top of floor tiles to add context, detail, or shadow.

| Surface | File |
|---|---|
| ShadowAndSurfaceDecals | `SurfaceDecals/ShadowAndSurfaceDecals.md` |

---

## FOLDER STRUCTURE

```
/GroundObjects/
  PIPELINE.md               ← This file
  FloorTiles/
    ConcreteFloor.md
    CrackedConcrete.md
    MetalFloor.md
    DirtGround.md
    GrassPatch.md
    RubbleGround.md
    MudGround.md
  RoadSurfaces/
    AsphaltRoad.md
    DirtTrack.md
  TransitionTiles/
    EdgeAndTransitionTiles.md
  SurfaceDecals/
    ShadowAndSurfaceDecals.md
```

---

## UNITY INTEGRATION OVERVIEW

| Component | Usage |
|---|---|
| Base floor tiles | Unity Tilemap component, `Ground` layer, Z = 0 |
| Road surfaces | Unity Tilemap, `Ground` layer, same Z as base tiles |
| Transition tiles | Unity Tilemap, same layer — placed at biome/surface boundaries |
| Surface decals | SpriteRenderer on GameObject, sorted above Tilemap, Y-sort disabled (flat decal) |
| Sorting layers | `Ground` (bottom) → `Decals` → `Props` → `Characters` → `VFX` → `HUD` |
| Grid alignment | All tiles aligned to Unity isometric grid (default 64×32 isometric cell) |
| Tile variants | Unity Rule Tile or Random Tile for automatic variant selection |
| Collider | Ground tiles: NO collider (characters walk on them freely). Prop objects above handle their own colliders |

---

## ANIMATION STATE GUIDE

Ground tiles do not animate by default. Exceptions:

| Surface | Animation |
|---|---|
| MudGround | Optional: very subtle slow bubble/shimmer (1 fps, 2-frame, can be disabled for performance) |
| MetalFloor (wet variant) | Optional: very faint specular flicker — 2-frame light shift |
| All others | Static — no animation |

---

## ANTI-DETAIL RULES

Ground tiles must NOT include:
- Character silhouettes or shadows baked in
- Weapon props or debris that could be mistaken for interactive objects
- Bright accent colors that compete with gameplay elements
- High-frequency noise that degrades at 64×32 display size
- Anything that could be confused for a hazard, pickup, or interactive zone

Ground tiles SHOULD include:
- Low-contrast surface micro-texture (visible at close zoom, dissolves at game zoom)
- Directional light bake that matches all scene props (top-left)
- 2–4 tile variants per surface to prevent patterning artifacts
- Subtle surface wear, age, and environmental history
