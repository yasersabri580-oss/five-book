# GROUND OBJECT — EDGE AND TRANSITION TILES

---

## Asset Name
**EdgeAndTransitionTiles**

## Category
Transition Tiles

## Gameplay Purpose
Tiles that bridge adjacent surface types — preventing visual jarring at terrain boundaries. Without transition tiles, a concrete-to-dirt edge would be a hard, unnatural cut. Transition tiles blend the two surfaces across a single tile width, creating a natural-looking seam. Edge tiles define the outer boundary of an elevated surface type (e.g., concrete slab edge where it drops to dirt below).

This set serves two functions:
1. **Transition tiles:** Blend surface A into surface B across one tile
2. **Edge tiles:** Represent the physical edge/lip of a raised surface (e.g., the concrete curb at road edge, or the end of a metal floor slab)

---

## TRANSITION TILES

### Visual Description
Each transition tile shows surface A fading into surface B across the tile. The boundary is irregular and organic (for natural materials like dirt/grass) or sharp and geometric (for constructed surfaces like concrete/asphalt). The transition must be seamless — no hard pixel edge.

### Transition Type Matrix

The following surface-pair transitions are required for Chapter 1:

| Pair | Priority | Notes |
|---|---|---|
| Concrete → Dirt | High | Urban/outdoor boundary (most common) |
| Concrete → Rubble | High | Damage zone boundaries |
| Asphalt Road → Concrete | High | Road edge/sidewalk |
| Asphalt Road → Dirt | High | Road edge into outdoor area |
| Dirt → Grass | Medium | Natural terrain boundary |
| Dirt → Mud | Medium | Wetland boundary (Mission 5) |
| Metal Floor → Concrete | Medium | Factory interior transitions |
| Grass → Mud | Low | Wetland edge |
| Rubble → Dirt | Low | Debris edge boundary |

Each transition requires 4 directional tile variants:
- North edge (surface A top, surface B bottom)
- South edge (surface B top, surface A bottom)
- East edge (surface A right, surface B left)
- West edge (surface A left, surface B right)
- Plus: 4 corner variants (convex and concave inner/outer corners)

### Reference Image Prompt — Concrete to Dirt Transition

```
Isometric 2.5D floor transition tile — concrete surface transitioning into dirt ground, dieselpunk game style.

Tile shape: Isometric diamond (parallelogram), 128×64 px. Flat top-down isometric view, 30-degree pitch.

Tile content: The left half of the tile (isometric left-slant face) shows solid concrete floor surface (#707878, smooth industrial concrete). The right half shows compacted dirt ground (#8A7050). The boundary between them runs diagonally across the tile from upper-left to lower-right (in isometric grid terms, this is the north edge of the concrete meeting the south dirt). The transition line is slightly irregular — not a perfectly straight edge, but a slightly ragged boundary as if the concrete slab ends and the earth begins.

Neither surface continues past its own area. No blending into each other (these are distinct materials with a defined edge).

Lighting: Each surface area retains its own baked lighting — concrete slightly cooler, dirt slightly warmer. The boundary edge has a very subtle 2–3px shadow on the dirt side, suggesting the concrete slab sits very slightly higher than the earth (a 2–3 cm elevation differential at scale).

Edges: NO black outline on tile. The material boundary provides the visual edge.

Seamless: This tile must connect seamlessly to: a pure concrete tile on the left, a pure dirt tile on the right, and to the corner transition tiles at the diagonal joins.

Style: Semi-realistic painterly, readable at 64×32 px. IRON BREACH art direction.
```

*(For other transition pairs: use the same prompt structure, substituting the surface descriptions, colors, and boundary behavior.)*

---

## EDGE TILES

### Visual Description
Edge tiles represent the physical edge of an elevated surface — typically the concrete curb, slab edge, or metal floor lip where a higher surface meets a lower one. These are not flat tiles — they show a slight elevation in the elevated surface and a very small shadow or depth on the lower side.

### Edge Types Required

| Edge | Description |
|---|---|
| Concrete slab edge | The end of a concrete slab where it meets dirt or asphalt — a 5–10cm raised edge, slightly beveled |
| Asphalt road curb | The curb between asphalt road and sidewalk/ground — a small raised grey curb lip |
| Metal floor lip | The edge of a factory metal floor — a folded metal lip where the floor ends |

### Reference Image Prompt — Concrete Slab Edge (North Edge)

```
Isometric 2.5D floor edge tile — concrete slab north edge (concrete on top half of tile, edge drop to lower ground on bottom half), dieselpunk game style.

Tile shape: Isometric diamond (parallelogram), 128×64 px. Flat top-down isometric view, 30-degree pitch.

Tile content: Top portion of tile (approximately top 2/3): standard concrete floor surface (#707878). The concrete surface ends at a slightly raised slab edge — a 5–8px wide beveled edge running horizontally across the isometric tile at the 2/3 height mark. The bevel face is slightly darker than the top surface (#606868) — it is the vertical face of the slab edge. Below the bevel: a shadow — very dark (near-black, #2A2A2A), approximately 3px, cast downward from the slab edge. Below the shadow: the adjacent lower surface begins (dirt or other material).

The slab edge must read clearly as a physical elevation change — the concrete is higher than the ground beyond the edge.

Lighting: Top-left directional. The bevel face is in shadow (it faces away from the light). The shadow cast below is slightly longer on the right side of the tile.

Seamless: Must connect to flat concrete tiles on the top connection and flat ground tiles on the bottom connection. Left and right connections match to corner edge tiles.

Style: Semi-realistic painterly, 64×32 px readable. IRON BREACH art direction.
```

---

## Tiling Note
**Rule-based placement.** Edge and transition tiles are placed automatically by a Unity Rule Tile that detects adjacent tile types and selects the correct edge/transition variant. Level designers do not manually place these — the Rule Tile system handles it.

## Animation Requirement
**None.** Static tiles.

## Unity Usage Note
- Component: Unity Tilemap, `Ground` tilemap layer
- Implementation: Unity Advanced Rule Tile or custom C# ITilemap rule implementation detecting adjacent TileBase types
- Transition logic: Each tile checks its 4 neighbors; if neighbor type differs, a transition tile is placed automatically between them
- Priority: When three or more different surfaces meet at a corner, concrete/metal > asphalt > rubble > dirt > grass > mud in layering priority
- Sorting layer: `Ground`

## Folder Name Suggestion
`/GroundObjects/TransitionTiles/`
