# GROUND OBJECT — DIRT GROUND

---

## Asset Name
**DirtGround**

## Category
Floor Tiles

## Gameplay Purpose
Primary outdoor natural ground surface. Used in open-field missions, rural approaches, off-road paths, and areas outside urban infrastructure. Commonly found in Missions 1, 3, and 5. Communicates "outside the city / untouched territory."

## Visual Description
Dry compacted earth — not soft mud, not sand, but hard-packed outdoor dirt. Color is a desaturated warm tan-brown. Surface has irregular micro-texture from soil granules. Small stones and pebbles are visible as faint slightly-lighter specks. Some variants include tire track impressions, shallow dips, or dried soil crack patterns. Very different from concrete in both color and texture — should be immediately readable as outdoor/natural.

Tile variants (4):
- **Variant A (clean dirt):** Compacted earth, uniform. Small stone specks, faint soil grain texture
- **Variant B (pebble-scattered):** Several small visible pebbles (2–4 per tile), slightly raised appearance with tiny shadow beneath each
- **Variant C (tire-tracked):** Two parallel compressed grooves across the tile — vehicle tire impressions, slightly darker in the groove base
- **Variant D (dry cracked):** Dry compacted earth with a low-contrast craquelure crack pattern — fine web of hairline cracks across the surface, not structural (very different from CrackedConcrete — these are desiccation cracks, organic in pattern)

## Material / Style
- Base color: Desaturated warm tan-brown (#8A7050)
- Stone specks: Slightly lighter grey-tan (#9A8870), very small
- Tire groove (Variant C): Darker tan (#6A5840) in groove, slightly lighter rim on edges
- Desiccation cracks (Variant D): Dark brown (#4A3828), hairline — very organic, irregular
- Lighting: Top-left directional bake. Slightly warmer shadow side than concrete
- Surface sheen: None — fully matte, dry earth

## Reference Image Prompt

```
Isometric 2.5D floor tile — dry compacted dirt ground, outdoor dieselpunk war-zone game style.

Tile shape: Isometric diamond (parallelogram), 128×64 px. Flat top-down isometric view, 30-degree pitch.

Surface: Dry compacted outdoor earth. Base color: desaturated warm tan-brown (#8A7050). Surface is NOT soft or muddy — this is hard-packed ground. Irregular micro-texture from soil granules and dust. Very small stone specks scattered across the surface — lighter grey-tan (#9A8870), irregular shapes, tiny, some barely visible. Surface is slightly irregular — not perfectly flat, subtle micro-undulation suggestion.

No grass, no vegetation, no puddles on this base tile. No debris. Purely natural compacted earth.

Lighting: Soft top-left directional bake. Left face of isometric tile brighter (warm tan). Right face darker (slightly deeper brown). No specular — dry earth is completely matte.

Edges: NO black outline. Ground tiles do not have outlines.

Seamless: Must tile seamlessly in all 4 isometric directions. Texture variation must not create visible repeating grid at 4×4 tile view.

Style: Semi-realistic painterly, readable at 64×32 px. IRON BREACH art direction. NOT pixel art. NOT photorealistic.

Do NOT include: vegetation, puddles, bright colors, or any element that reads as an interactive object.
```

## Tile Variants Prompts

**Variant B (pebble-scattered):** "2–4 small pebbles visible on the surface. Each pebble: a slightly lighter grey-tan irregular shape with a tiny dark shadow cast on one side (isometric top-left light). Pebbles range from 3–8px at 128×64 resolution."

**Variant C (tire-tracked):** "Two parallel compressed grooves running diagonally across the tile — vehicle tire track impressions. Each groove: a darker tan (#6A5840) recessed line, approximately 8–10px wide at 128×64, with a very thin slightly lighter rim on the upper edge (light catching the groove edge). Surrounding dirt is slightly denser/darker near the groove edges."

**Variant D (dry cracked):** "Desiccation crack pattern across the surface — irregular organic web of hairline cracks, NOT geometric. Crack lines: dark brown (#4A3828), 1px. Pattern is irregular and natural-looking (like dried mud or drought-cracked earth). Very different from CrackedConcrete — these are soil cracks, not structural breaks."

## Tiling Note
**Tileable — seamless.** Use Unity Random Tile. Variants A and B weighted 45/30/15/10 (A/B/C/D). Variant C should be used in road-adjacent zones or vehicle path areas.

## Animation Requirement
**None.** Static tile.

## Unity Usage Note
- Component: Unity Tilemap, `Ground` tilemap layer
- Z position: 0
- Sorting layer: `Ground`
- Use in: Open-field areas, rural approaches, dirt paths, off-road mission sections
- Note: Pair with GrassPatch tiles at field edges and transition via TransitionTiles at road/concrete boundaries

## Folder Name Suggestion
`/GroundObjects/FloorTiles/DirtGround/`
