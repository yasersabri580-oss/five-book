# GROUND OBJECT — RUBBLE GROUND

---

## Asset Name
**RubbleGround**

## Category
Floor Tiles

## Gameplay Purpose
Post-destruction ground surface — bombed-out areas, collapsed building interiors, FORGE-devastated zones, and tank-fire impact areas. Signals extreme environmental damage. Used in Missions 3 (post-bombardment district), 7, and as scattered patches throughout urban missions.

## Visual Description
Ground covered in broken concrete chunks, brick fragments, twisted metal scraps, and dust. The rubble layer sits on a base of pulverized concrete dust. Individual debris pieces vary in size: large flat concrete slabs (2–4 per tile), small brick fragments, and fine dust. The tile reads as visually chaotic but the silhouette is flat — rubble is low profile, not tall. No props stick up more than a few pixels (props use EnvironmentObjects for that). Pure ground-level debris scatter.

IMPORTANT: Rubble tiles must NOT be confused with cover objects. All debris is ground-level — flat or nearly flat. This is a traversal surface, not an obstacle.

Tile variants (4):
- **Variant A (light rubble):** Mostly concrete dust with a few medium fragments scattered. Traversable look.
- **Variant B (heavy rubble):** Dense fragment coverage — several concrete chunks, brick pieces, metal fragments. Still flat/low-profile.
- **Variant C (brick-dominant):** More reddish-orange brick fragments (#8A4830) visible — from collapsed masonry building
- **Variant D (metal-dominant):** Twisted metal scrap fragments dominant (#5A5A5A) — from vehicle wreckage or machinery destruction

## Material / Style
- Base dust: Pulverized concrete — cool pale grey (#9A9898), lighter than base concrete
- Concrete fragments: Mid-grey (#787878), slight edge highlight on upper faces
- Brick fragments (C): Desaturated orange-red (#8A4830)
- Metal scraps (D): Gunmetal grey (#5A5A5A) with very slight edge highlight
- Debris shadow: Very dark shadow beneath each fragment piece on its lower-right side
- Lighting: Top-left directional bake. Each fragment catches light individually — upper-left faces lighter, lower-right faces darker

## Reference Image Prompt

```
Isometric 2.5D floor tile — war rubble ground, post-destruction dieselpunk game style.

Tile shape: Isometric diamond (parallelogram), 128×64 px. Flat top-down isometric view, 30-degree pitch.

Surface: Ground covered in low-profile post-destruction rubble. Base: fine pulverized concrete dust (#9A9898) — lighter grey than solid concrete, powdery appearance. On top of the dust base: scattered concrete fragment pieces — irregular angular flat slabs, 2–4 medium pieces per tile, each casting a tiny shadow on its lower-right side (isometric light source top-left). Fragment colors: mid-grey (#787878). Smaller brick and stone chips scattered between larger pieces. No piece rises more than 4–6px above the base (this is flat ground rubble, not obstacle rubble).

Important: All rubble elements are FLAT or nearly flat — this is a traversal surface, not a blocking obstacle.

Lighting: Each fragment catches isometric top-left light — fragment upper-left face slightly lighter, lower-right face darker. Dust base is evenly lit, slightly lighter than solid concrete.

Edges: NO black outline on the tile. Fragment pieces have a very subtle thin darker edge to suggest their irregular form.

Seamless: Must tile seamlessly in all 4 isometric directions.

Style: Semi-realistic painterly, readable at 64×32 px. IRON BREACH art direction. NOT pixel art. NOT photorealistic.

Do NOT include: standing walls, tall props, weapons, bodies, or anything that reads as an interactive gameplay object.
```

## Tile Variants Prompts

**Variant A (light rubble):** "Sparse fragments — mostly dust base with 2 medium concrete pieces and a few small chips. Open and traversable-looking. 60% dust, 40% fragments."

**Variant C (brick-dominant):** "Add brick fragments: desaturated orange-red (#8A4830) irregular brick pieces mixed with concrete fragments. More warm tones visible — suggests a collapsed masonry building."

**Variant D (metal-dominant):** "Replace some concrete fragments with twisted metal scrap pieces: gunmetal grey (#5A5A5A), slightly irregular and jagged edge shapes. A small visible bent metal strip or corner piece. Suggests destroyed machinery or vehicle wreckage debris."

## Tiling Note
**Tileable — seamless.** Use Unity Random Tile. All 4 variants weighted 30/30/20/20. Manual placement preferred in specific destruction zones to control visual narrative.

## Animation Requirement
**None.** Static tile.

## Unity Usage Note
- Component: Unity Tilemap, `Ground` tilemap layer
- Z position: 0
- Sorting layer: `Ground`
- Collider: None — characters move through rubble ground freely (the gameplay friction/slowdown is a game mechanic, not a tile collision)
- Use in: Bombed districts, post-battle zones, collapsed building areas, anywhere destruction is the narrative context

## Folder Name Suggestion
`/GroundObjects/FloorTiles/RubbleGround/`
