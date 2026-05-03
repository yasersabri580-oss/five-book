# GROUND OBJECT — GRASS PATCH

---

## Asset Name
**GrassPatch**

## Category
Floor Tiles

## Gameplay Purpose
Natural outdoor ground surface with vegetation. Used in open-field mission sections, outskirts of Verak city, and areas far from industrial infrastructure. Contrasts strongly with concrete and metal floors to signal "civilian/natural territory." Missions 1, 2 (outskirts), and 5.

## Visual Description
Low, desaturated grass — NOT lush bright green. This is war-zone grass: dried, patchy, slightly yellowed in places. A desaturated olive-green as the dominant tone, not vivid or colorful. Individual grass blade clusters are implied by texture, not individually drawn. Some variants show partial bare earth exposure through the grass. The tile communicates "overgrown open ground" not a manicured lawn.

Tile variants (4):
- **Variant A (dense grass):** Solid grass coverage, desaturated olive-green, dense texture
- **Variant B (patchy grass):** ~60% grass coverage with exposed dirt patches (#8A7050) visible between clusters
- **Variant C (yellowed):** Same density as Variant A but color shifted toward dried yellow-green (#7A7030) — drought or war-damaged grass
- **Variant D (trampled):** Flattened grass areas — compressed patches with lower grass, some bare earth. Used near paths or frequently trafficked areas

## Material / Style
- Base grass color: Desaturated olive-green (#5A6030)
- Blade texture: Slightly lighter (#6A7040) individual cluster tips implied
- Shadow recesses: Darker olive (#3A4020) between grass clusters
- Yellowed variant: Dried yellow-green (#7A7030) dominant
- Bare earth patches: DirtGround tan-brown (#8A7050)
- Lighting: Top-left directional bake. Grass tips slightly lighter on left face, shadow in grass depth on right

## Reference Image Prompt

```
Isometric 2.5D floor tile — dry war-zone grass ground, outdoor dieselpunk game style.

Tile shape: Isometric diamond (parallelogram), 128×64 px. Flat top-down isometric view, 30-degree pitch.

Surface: Low, slightly dried grass ground. Base color: desaturated olive-green (#5A6030). This is NOT bright or lush grass — this is war-zone grass: slightly dried, desaturated, dull. Grass texture is suggested through color variation — lighter blade tips (#6A7040) and darker recessed shadow between clusters (#3A4020). Individual blades are NOT individually drawn — the texture reads as grass through pattern and color but is abstracted.

No bright colors, no flowers, no vivid green. Grass reads as alive but worn.

Lighting: Soft top-left directional bake. Slightly brighter on the left-facing isometric face. Shadow areas slightly deeper on right-facing face. No specular — matte natural surface.

Edges: NO black outline. Ground tiles do not have outlines.

Seamless: Must tile seamlessly in all 4 isometric directions.

Style: Semi-realistic painterly, readable at 64×32 px. IRON BREACH art direction. NOT pixel art. NOT photorealistic.

Do NOT include: flowers, bright colors, puddles, or any element that reads as an interactive object or hazard.
```

## Tile Variants Prompts

**Variant B (patchy):** "Grass coverage is approximately 60%. Between the grass clusters, exposed dirt earth (#8A7050) is visible — irregular bare patches, natural-looking. The dirt and grass areas transition organically within the tile."

**Variant C (yellowed):** "Color palette shifts toward dried yellow-green (#7A7030) — same grass texture as Variant A but the grass is drier, more straw-colored. Some blades lean toward tan (#8A7840). The tile reads as drought-affected or fire-scorched grass."

**Variant D (trampled):** "Flattened grass — portions of the tile have grass compressed flat (a darker, less textured area), suggesting a path or high-traffic route. Partial bare earth (#8A7050) visible in the most flattened areas."

## Tiling Note
**Tileable — seamless.** Use Unity Random Tile. Variants A and B weighted 40/30/20/10 (A/B/C/D). Use Variant D manually near pathways or building entrances.

## Animation Requirement
**None.** Static tile. (Grass sway is a VFX particle layer, not baked into the floor tile.)

## Unity Usage Note
- Component: Unity Tilemap, `Ground` tilemap layer
- Z position: 0
- Sorting layer: `Ground`
- Use in: Open fields, rural outskirts, natural outdoor areas away from city center
- Note: Use TransitionTiles at grass-to-dirt and grass-to-concrete boundaries

## Folder Name Suggestion
`/GroundObjects/FloorTiles/GrassPatch/`
