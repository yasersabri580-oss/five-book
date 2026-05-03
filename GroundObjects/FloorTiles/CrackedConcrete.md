# GROUND OBJECT — CRACKED CONCRETE

---

## Asset Name
**CrackedConcrete**

## Category
Floor Tiles

## Gameplay Purpose
Damaged outdoor and partially collapsed indoor ground surface. Used in war-damaged zones, rubble-adjacent areas, contested outdoor plazas, and anywhere FORGE or tank combat has damaged the ground. Signals a dangerous or contested area visually without explicit UI markers.

## Visual Description
Concrete slab floor with visible structural cracks — irregular fracture lines radiating from stress points. Some cracks are hairline; some are wider, showing dark interior depth. Small chip fragments remain near wide cracks. Surface color is slightly more weathered than clean ConcreteFloor — exposed aggregate in crack zones, dust accumulation in crevices. No grass or vegetation growth (this is active warzone — recent damage). The tile reads as damaged but still traversable.

Tile variants (4):
- **Variant A (light crack):** Single radiating crack, hairline, across one diagonal
- **Variant B (heavy crack):** Multiple intersecting cracks, 1–2 showing dark depth, small chips
- **Variant C (slab shift):** Crack running edge-to-edge with a slight 2–3px elevation offset between the two halves — one side of the crack sits very slightly higher (isometric read: slight shadow on the lower half)
- **Variant D (blast damage):** Circular crack pattern radiating from a central blast point — small dark crater dimple at center, cracks fanning outward

## Material / Style
- Base color: Weathered concrete grey (#686F70), slightly darker/dirtier than clean ConcreteFloor
- Crack lines: Near-black (#1A1A1A), 1–2px, with a thin lighter highlight edge (#888A88) on one side to suggest depth
- Crack interior shadow: Very dark grey (#2A2A2A) in wider cracks only
- Chip fragments: Slightly lighter than base (#8A9090), small irregular polygons near wide cracks
- Dust accumulation: Very subtle — barely lighter smudge in crack crevices
- Lighting: Same top-left directional bake as ConcreteFloor

## Reference Image Prompt

```
Isometric 2.5D floor tile — cracked concrete ground, dieselpunk war-damage game style.

Tile shape: Isometric diamond (parallelogram), 128×64 px. Flat top-down isometric view at 30-degree pitch. This is a damaged concrete ground tile.

Surface: Weathered and cracked industrial concrete slab. Base color: weathered grey (#686F70), slightly darker and dirtier than clean concrete. Multiple irregular fracture cracks across the surface — irregular jagged paths, not geometric. Primary crack: prominent, running diagonally from one corner area toward opposite. Secondary smaller cracks branching from it. Crack lines: near-black (#1A1A1A), thin (1–2px at 128×64 res). One edge of each wider crack has a thin lighter highlight (#888A88) suggesting depth. Small concrete chip fragments scattered near the widest cracks — slightly lighter irregular shapes. Surface has faint dust accumulation in crevices.

Lighting: Soft top-left directional bake. Left face slightly lighter, right face slightly darker. No specular — completely matte.

Edges: NO black outline. Ground tiles have no outlines.

Seamless: Must tile seamlessly in all 4 isometric directions. Cracks must not align perfectly with tile edges in a way that creates an obvious grid pattern.

Style: Semi-realistic painterly, readable at 64×32 px display. Same art direction as IRON BREACH. NOT pixel art. NOT photorealistic.

Do NOT include: vegetation, puddles, blood, weapon remnants, or any element that could be confused for an interactive pickup or hazard.
```

## Tile Variants Prompts

**Variant A (light crack):** "Single hairline crack, very thin, running diagonally across tile. Minimal chips. Barely visible at small zoom — subtle damage."

**Variant C (slab shift):** "Crack runs full edge-to-edge. One half of tile is very slightly elevated — a 2–3px shadow line along the lower side of the crack simulates the height differential in isometric view."

**Variant D (blast damage):** "Cracks radiate from a central point in a starburst/circular pattern. Small dark circular dimple at the center — a blast impact point. This variant is used to mark former explosion sites."

## Tiling Note
**Tileable — seamless.** Use Unity Random Tile with Variants A, B, C, D weighted 30/35/20/15. Variant D (blast) should be placed sparingly — preferably manually at scripted explosion sites, not random.

## Animation Requirement
**None.** Static tile.

## Unity Usage Note
- Component: Unity Tilemap, `Ground` tilemap layer
- Z position: 0
- Rule Tile: 4-variant Random/Rule Tile. Variant D: place manually or via scripted post-explosion swap
- Collider: None
- Sorting layer: `Ground`
- Use in: Outdoor war zones, bombed plazas, rubble-adjacent corridors, anywhere post-combat damage is implied

## Folder Name Suggestion
`/GroundObjects/FloorTiles/CrackedConcrete/`
