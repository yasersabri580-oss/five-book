# GROUND OBJECT — CONCRETE FLOOR

---

## Asset Name
**ConcreteFloor**

## Category
Floor Tiles

## Gameplay Purpose
Primary indoor ground surface for factory interiors, military installations, bunkers, and SENTINEL facility interiors. The most common urban floor type in Chapter 1. Characters, tanks, and props are placed on top of it.

## Visual Description
Smooth industrial concrete slab with subtle pour lines and minor surface aging. Color is cold mid-grey — desaturated, not white. Surface has low-contrast micro-texture: faint aggregate speckle, slight surface grain, hairline stress marks in a few variants. No cracks (see CrackedConcrete for damaged variant). No dirt accumulation on the base tile (see SurfaceDecals for layered grime). The tile reads as a maintained but aged industrial floor.

Tile variants (4):
- **Variant A (clean):** Smooth grey, faint pour line toward one edge, very minimal grain
- **Variant B (worn):** Same base, slightly more aggregate visible, faint scuff marks from machinery
- **Variant C (water stained):** Darker grey center, lighter dried-ring water stain halo — low contrast
- **Variant D (utility line):** Faint painted utility line segment (faded yellow #5A4A10) cutting across the tile diagonal — used near factory walkway zones

## Material / Style
- Base color: Cold mid-grey (#707878)
- Aggregate: Lighter grey speckle (#888E8E), very low contrast — barely visible at game zoom
- Pour lines: Slightly darker grey (#606868), 1px width
- Utility line (Variant D): Faded dirty yellow (#5A4A10), thin, clearly faded
- Lighting: Soft top-left directional bake. Left face of isometric tile slightly brighter (#808A8A); right face slightly darker (#606868)
- Surface sheen: NONE — completely matte. Industrial concrete has no specular

## Reference Image Prompt

```
Isometric 2.5D floor tile — concrete industrial floor, dieselpunk game style.

Tile shape: isometric diamond (parallelogram top-view), 128×64 px. Flat top-down isometric perspective — the tile is a flat ground surface seen at 30-degree pitch.

Surface: Smooth industrial concrete. Cold mid-grey (#707878). Subtle aggregate speckle in slightly lighter grey (#888E8E) — barely visible, very low contrast. Faint surface grain texture. One pour line (darker grey, 1px) running diagonally across the tile. Minor surface aging — not cracked, not broken. Clean but old.

Lighting: Soft top-left directional bake. Left face of isometric tile (the tile is a parallelogram — left-slanted face) slightly brighter. Right-slanted face slightly darker. No specular. Flat matte material.

Edges: NO black outline on this tile. Ground tiles have no outlines. Tile edges are defined by the lighting differential between left and right faces only.

Seamless: This tile must tile seamlessly with itself in all 4 isometric directions (left, right, top, bottom connections). No edge artifacts. No repeating pattern visible at 3×3 tile grid.

Background: None — this IS the background. No framing.

Style: Semi-realistic texture, painterly but readable at 64×32 px display size. NOT pixel art. NOT photorealistic. Consistent with IRON BREACH's semi-realistic painterly art style.

Do NOT include: characters, props, weapons, bright colors, harsh outlines, or any element that competes with gameplay objects placed on top.
```

## Tile Variants Prompts

**Variant B (worn):** Add "More aggregate speckle visible. Faint scuff marks from heavy machinery — 2–3 short parallel scrape lines across the tile, very low contrast."

**Variant C (water stained):** Add "Center of tile slightly darker grey. Faint dried ring watermark — a faint lighter oval outline from an evaporated puddle, very subtle."

**Variant D (utility line):** Add "A faded painted utility line (dirty yellow #5A4A10, approximately 3px wide at 128×64 resolution) crossing the tile at an angle. Clearly faded — not a fresh painted line."

## Tiling Note
**Tileable — seamless.** Use Unity Random Tile with Variants A, B, C weighted 40/40/15/5 (D is rare — placed intentionally near factory walkways).

## Animation Requirement
**None.** Static tile.

## Unity Usage Note
- Component: Unity Tilemap, `Ground` tilemap layer
- Z position: 0 (base ground layer)
- Rule Tile: 4-variant Random Tile
- Collider: None — characters pass over freely
- Sorting layer: `Ground`
- Use in: Factory interiors, bunker corridors, SENTINEL facility floors, military base interiors

## Folder Name Suggestion
`/GroundObjects/FloorTiles/ConcreteFloor/`
