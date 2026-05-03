# GROUND OBJECT — METAL FLOOR

---

## Asset Name
**MetalFloor**

## Category
Floor Tiles

## Gameplay Purpose
Industrial interior ground surface for factory production floors, vehicle maintenance bays, platform walkways, and FORGE facility interiors. Signals a high-tech or heavy-industry environment. Used in Missions 7, 8 (The Crucible), and 10.

## Visual Description
Riveted metal floor panels — overlapping rectangular steel plates, each panel slightly different in tone due to age and surface oxidation. Rivet heads are visible at panel corners and mid-edges. Subtle surface grating or non-slip diamond-plate texture on some variants. Panel seams are visible as thin dark lines. Overall color is a warm-tinted gunmetal grey — slightly warmer than the cold ConcreteFloor. Some panels show minor rust bloom at edges (not aggressive rust — just age-coloration). In wet variants, a very faint specular sheen (floor reflects overhead industrial lights).

Tile variants (4):
- **Variant A (clean panels):** Rectangular metal panels, rivets at corners, mild patina, panel seams
- **Variant B (grated):** Diamond-plate non-slip texture across the tile — raised grid pattern visible in isometric
- **Variant C (rust-edged):** Panel edges have rust-brown (#6A3A18) bloom along seam lines — orange-brown stain, low saturation
- **Variant D (wet/oil-stained):** Dark oil stain (#1A1A14) pooled in panel seam recesses. Very faint surface sheen in panel centers

## Material / Style
- Base color: Warm gunmetal grey (#5A5850), slightly warm-tinted
- Panel seam lines: Near-black (#1A1A1A), 1px
- Rivet heads: Slightly lighter grey hemisphere (#7A7870) — tiny raised dome suggestion
- Rust bloom (Variant C): Desaturated orange-brown (#6A3A18)
- Oil stain (Variant D): Very dark near-black (#1A1A14), pooled at seams
- Specular (Variant D): Faint grey highlight in center of panels only — 1 shade lighter than base
- Lighting: Top-left directional bake. Metal reads slightly more contrast than concrete due to subtle specular

## Reference Image Prompt

```
Isometric 2.5D floor tile — industrial riveted metal floor, dieselpunk factory game style.

Tile shape: Isometric diamond (parallelogram), 128×64 px. Flat top-down isometric view, 30-degree pitch.

Surface: Industrial metal floor panels. Base color: warm gunmetal grey (#5A5850). The floor is divided into rectangular metal plates — each plate is approximately 1/3 to 1/2 of the tile in size. Panel seam lines: thin near-black lines (1px) between each plate. Rivet heads at panel corners and mid-edges: small slightly lighter grey raised dots (#7A7870), subtle. Mild surface patina — slightly uneven tone between adjacent panels (some panels one shade lighter, some one shade darker, all within narrow range). Non-aggressive surface texture — not rough, not completely smooth. Slight worn factory feel.

Lighting: Soft top-left directional bake. Left face of isometric tile brighter. Right face darker. Very slight metallic micro-sheen — one shade lighter catch-light in panel centers only, not a mirror reflection.

Edges: NO black outline on this tile. Ground tiles do not have outlines.

Seamless: Must tile seamlessly in all 4 isometric directions. Panel seam lines should continue naturally across tile edges.

Style: Semi-realistic painterly, readable at 64×32 px. Same IRON BREACH art direction. NOT pixel art. NOT photorealistic.

Do NOT include: characters, machinery, glow effects (except very subtle specular), or anything that reads as interactive or hazardous.
```

## Tile Variants Prompts

**Variant B (grated):** "Replace smooth panel surface with diamond-plate non-slip texture — a regular raised diamond/lozenge grid embossed into the metal surface. Individual diamonds are small — approximately 4–5 per tile width at 128px. The raised diamond tops catch slightly more light."

**Variant C (rust-edged):** "Panel seam lines have rust bloom: orange-brown staining (#6A3A18) spreading 3–4px from each seam line onto the panel face. Low saturation — not bright rust, aged and desaturated. Rivets also show rust halos."

**Variant D (wet/oil-stained):** "Dark oil stain (#1A1A14) pooled in the recessed seam gutters between panels. Panel centers have a very faint specular highlight — one shade lighter than base, suggesting a thin liquid film or reflective surface from overhead lighting."

## Tiling Note
**Tileable — seamless.** Use Unity Random Tile. Variants A and B weighted equally (40/40). C and D at 10% each. D (wet) should be concentrated in specific zone dressing via manual placement.

## Animation Requirement
**Variant D only — optional:** 2-frame subtle light shift on the specular highlight (frame 1: highlight at default intensity; frame 2: slightly dimmer). Loop at 2 fps. Can be disabled per-project performance budget.

## Unity Usage Note
- Component: Unity Tilemap, `Ground` tilemap layer
- Z position: 0
- Sorting layer: `Ground`
- Use in: Factory production floors (Missions 7, 8, 10), vehicle bays, FORGE facility interiors
- Note: Variant D can be manually placed at specific locations to imply oil spill or recent machinery activity

## Folder Name Suggestion
`/GroundObjects/FloorTiles/MetalFloor/`
