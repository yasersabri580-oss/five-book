# GROUND OBJECT — MUD GROUND

---

## Asset Name
**MudGround**

## Category
Floor Tiles

## Gameplay Purpose
Wet, waterlogged ground surface. Used at river edges, swamp zones, drainage areas, and low-lying terrain that collects water. Signals movement hazard terrain — tanks forced to exit if they enter deep mud zones (game mechanic). Used in Mission 5 (wetlands sector) and at water-adjacent map edges.

## Visual Description
Wet compacted earth with standing surface moisture. Darker than DirtGround — waterlogged dark brown. Surface has a faint sheen from the water layer. Footprint impressions are visible in some variants. Small standing water pockets (very shallow, irregular) are partially visible in low-lying areas within the tile. Mud is thick and heavy-looking — the color and texture communicate resistance and weight.

Tile variants (4):
- **Variant A (wet mud):** Dark wet earth, slightly reflective surface sheen, no standing water
- **Variant B (muddy pools):** Small irregular standing water pockets within the tile — very thin water layer, reflective
- **Variant C (boot-tracked):** Boot-print impressions pressed into the mud, 2–3 prints
- **Variant D (vehicle-tracked):** Deep tire ruts pressed into mud, heavy vehicle track impressions

## Material / Style
- Base mud: Dark desaturated brown (#4A3828) — very dark, nearly earthy black when wet
- Surface sheen (Variant A): Very faint single-shade highlight in tile center area — suggests surface moisture
- Standing water (Variant B): Very dark near-black (#1A1A18) for the water pocket, with a thin bright reflection line (#9AA0A8) — the simplest water read
- Boot prints (Variant C): Slightly darker depression (#3A2A1A) with a subtle raised rim
- Tire ruts (Variant D): Deep dark parallel grooves — darker than Variant C, more compressed

## Reference Image Prompt

```
Isometric 2.5D floor tile — wet muddy ground, waterlogged war-zone terrain, dieselpunk game style.

Tile shape: Isometric diamond (parallelogram), 128×64 px. Flat top-down isometric view, 30-degree pitch.

Surface: Waterlogged dark mud. Base color: very dark desaturated brown (#4A3828) — much darker than DirtGround, suggesting saturated wet earth. Surface texture: slightly irregular, slightly soft-looking — not hard-packed. Very faint surface moisture sheen in the center of the tile — one shade lighter highlight (#5A4838) suggesting a thin water film on the surface. The overall read is heavy, wet, muddy terrain.

No bright colors, no standing water pools on this base variant. Purely wet earth tone.

Lighting: Soft top-left directional bake. Left face slightly lighter, right face darker. The faint sheen adds a subtle catch-light in the tile center only — not a full specular highlight.

Edges: NO black outline. Ground tiles do not have outlines.

Seamless: Must tile seamlessly in all 4 isometric directions.

Style: Semi-realistic painterly, readable at 64×32 px. IRON BREACH art direction. NOT pixel art. NOT photorealistic.

Do NOT include: vegetation, ripple effects, characters, or anything that reads as an interactive zone boundary.
```

## Tile Variants Prompts

**Variant B (muddy pools):** "Small shallow standing water pockets visible on the tile — 2–3 irregular oval areas. Water color: very dark near-black (#1A1A18) for the flat water surface. A thin single-pixel bright grey-blue reflection line (#9AA0A8) at one edge of each water pocket (isometric top-left light catch). Surrounding mud is pushed slightly aside at water pocket edges."

**Variant C (boot-tracked):** "2–3 boot-print impressions pressed into the mud. Each print: a slightly darker depression (#3A2A1A) showing a simplified boot outline — heel and toe shape, no fine tread detail. Each print has a very subtle slightly lighter raised rim around it (displaced mud)."

**Variant D (vehicle-tracked):** "Two deep parallel ruts from a heavy vehicle tire — running diagonally across the tile. Each rut: a wide dark depression (~12px at 128×64), darker than the base (#3A2818). Mud is pushed up into ridges on each rut edge — slightly lighter raised mud rim. Ruts are heavy and authoritative-looking."

## Tiling Note
**Tileable — seamless.** Use Unity Random Tile. Variants A and B weighted 40/30/20/10 (A/B/C/D). Variant D used deliberately at vehicle crossing zones.

## Animation Requirement
**Variant B only — optional:** Very subtle 2-frame water surface shift (frame 1: reflection line at default; frame 2: reflection line shifted 1px). Loop at 1 fps. Very slow, barely perceptible. Can be disabled for performance.

## Unity Usage Note
- Component: Unity Tilemap, `Ground` tilemap layer
- Z position: 0
- Sorting layer: `Ground`
- Gameplay note: Deep mud zones (3+ connected mud tiles) trigger the tank deep-water exit rule. This is handled by the game's tile-type tagging system, not by the tile sprite. Tag mud tiles as `TerrainType.Mud` in the tilemap metadata.
- Use in: Wetlands (Mission 5), river edges, drainage areas, low-lying terrain between urban zones

## Folder Name Suggestion
`/GroundObjects/FloorTiles/MudGround/`
