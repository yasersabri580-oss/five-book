# GROUND OBJECT — ASPHALT ROAD

---

## Asset Name
**AsphaltRoad**

## Category
Road Surfaces

## Gameplay Purpose
Primary vehicle road surface for urban streets, military supply roads, and facility access routes. Tank movement is optimized on road tiles (no movement penalty). Used in Missions 1 (city streets), 4, 6, 9, and 10. Serves as the main vehicle traversal lane in urban areas.

## Visual Description
Dark asphalt road — worn, cracked at edges, with faded road markings. Color is very dark grey-black, notably darker than ConcreteFloor. Surface has a low aggregate texture from the asphalt mix. Road markings (center lines, edge lines) are present in some variants as faded yellowed or white painted lines. The tile communicates "vehicle road" immediately at game view. Road tiles are directional — there are horizontal (east-west) and vertical (north-south) variants, plus intersection variants.

Tile variants / types:
- **Straight (E-W):** Road running east-west across the isometric tile
- **Straight (N-S):** Road running north-south
- **Corner (4 variants):** NE, NW, SE, SW corner tiles
- **T-intersection (4 variants):** T-junction in each orientation
- **Full intersection:** 4-way cross intersection
- **Edge tile:** Transition between asphalt and adjacent ground surface — road edge/curb

Road marking variants:
- **No markings:** Pure asphalt, worn surface
- **Center line:** Faded dashed yellow center line
- **Edge line:** Faded white solid edge stripe

## Material / Style
- Base asphalt: Very dark grey (#282828), slightly warm-tinted — not pure black, aged asphalt
- Aggregate: Very subtle lighter speck texture (#303030), barely visible
- Center line: Faded dirty yellow (#6A5A18), dashed, clearly old
- Edge line: Faded white (#9A9898), solid stripe near road edge
- Curb (edge tile): Medium grey (#686868) — a raised edge between road and sidewalk/ground
- Lighting: Same top-left directional. Dark base makes directional difference less obvious — slight surface micro-sheen on left face

## Reference Image Prompt

```
Isometric 2.5D floor tile set — dark asphalt road surface, urban dieselpunk war-zone game style.

Tile shape: Isometric diamond (parallelogram), 128×64 px. Flat top-down isometric view, 30-degree pitch. This tile is a ROAD SURFACE — the road runs across the tile in a specific direction.

Primary variant: Road running east-west (the road strip fills the full width of the isometric tile from left edge to right edge, approximately 60–70% of the tile height centered). Shoulder areas above and below the road strip show a hint of transition to adjacent ground.

Road surface: Very dark grey (#282828) asphalt — notably darker than concrete floor. Subtle aggregate texture: very faint slightly lighter micro-speckle (#303030), almost invisible. Road surface has minor age cracking near edges — hairline cracks, not dramatic. A faded dashed yellow center line (#6A5A18) runs along the center of the road strip, dashed segments. The center line is clearly old and partially worn away. A faded white solid edge stripe (#9A9898) near each road edge.

Lighting: Soft top-left directional bake. Very dark surface makes lighting differential subtle — slight lightness on left-facing surface only.

Edges: NO hard black outline on the tile itself. Road edge at the tile boundary is defined by a subtle color shift toward adjacent ground tone.

Seamless: Road tiles must connect seamlessly to adjacent road tiles. Markings must align across tile edges.

Style: Semi-realistic painterly, readable at 64×32 px. IRON BREACH art direction. NOT pixel art. NOT photorealistic.

Do NOT include: vehicles, barriers, bright colors, or any gameplay props. This is ground only.
```

## Tile Variant Set Requirements

The following tile types are required for the complete road system:

| Tile | Direction | Notes |
|---|---|---|
| Straight | E-W | Road runs left-right in isometric view |
| Straight | N-S | Road runs top-bottom in isometric view |
| Corner | NE | Road turns from east to north |
| Corner | NW | Road turns from west to north |
| Corner | SE | Road turns from east to south |
| Corner | SW | Road turns from west to south |
| T-junction | E facing W | 3-way junction |
| T-junction | W facing E | 3-way junction |
| T-junction | N facing S | 3-way junction |
| T-junction | S facing N | 3-way junction |
| Intersection | Full 4-way | Cross intersection |
| Dead end | All 4 directions | Road ends |

Each tile type requires separate image prompt — see reference prompt above as base and adjust the road direction and connection edges for each type.

## Tiling Note
**Directional — not random.** Road tiles are placed by level designers to form coherent road networks. Unity Rule Tile system handles automatic direction selection based on adjacent road tile connections.

## Animation Requirement
**None.** Static tile.

## Unity Usage Note
- Component: Unity Tilemap, `Ground` tilemap layer (same Z as other ground tiles)
- Rule Tile: Unity Terrain/Road Rule Tile — auto-selects correct tile variant based on neighbor connections
- Tag: `TerrainType.Road` — used by tank movement system to apply road movement bonus
- Sorting layer: `Ground`
- Use in: Urban streets, supply roads, facility access routes, vehicle highways

## Folder Name Suggestion
`/GroundObjects/RoadSurfaces/AsphaltRoad/`
