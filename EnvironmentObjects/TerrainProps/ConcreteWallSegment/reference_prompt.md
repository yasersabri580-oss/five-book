# REFERENCE IMAGE PROMPT — CONCRETE WALL SEGMENT

---

## Purpose
This prompt generates the **canonical reference image** for the ConcreteWallSegment.
All wall tile art must be consistent with this reference for visual identity and tiling accuracy.

---

## Reference Image Generation Prompt

```
2.5D isometric game asset — Concrete Wall Segment for the game IRON BREACH.

CAMERA: Isometric 2.5D, 30-degree pitch, south-east facing. The wall is shown as a standalone tileable segment on a transparent or flat near-black background (#121212). No environment, no scene.

ART STYLE: Stylized but gameplay-readable. Crisp 2px black outline. Flat-ish shading with subtle baked lighting — top face is lightest, front face is mid-tone, right side face is darkest. NOT pixel art. NOT full 3D render. NOT photorealistic. Clean game asset sprite style. Same style as all IRON BREACH environment objects.

SHAPE: Rectangular concrete slab. 1 isometric tile wide × 1 tile deep × 1.5 tiles tall. Flat top surface. Vertical front face. The segment is meant to tile horizontally — left and right edges are clean and straight for seamless connection.

MATERIAL: Poured concrete. Rough but not chaotic. Faint horizontal formwork seam lines across the front face (subtle, 1–2 lines, grey-on-grey). Optional rebar stub visible at the top-left corner — just a short dark metal stub, not elaborate. A grime/dirt darkening streak near the base on the front face.

COLOR PALETTE:
- Top face: #5A5A58 (lighter — receives top light)
- Front face (south): #4A4A48 (base grey)
- Right face (east): #2E2E2C (shadow face — darkest)
- Outlines: black (#0A0A0A)
- Grime/dirt: #2A2420 streak near base
- Rebar stub: #3A3A38 dark metal

DETAILS: Minimal. 1–2 faint surface cracks on the front face — thin, irregular, but short. No holes, no heavy damage (this is the intact variant). Slight ambient occlusion darkening at the base where wall meets ground.

SCALE: Provide the segment next to a simple isometric tile grid marker so scale is clear. Wall is 1×1 tile footprint, 1.5 tiles tall.

OUTPUT: Three panels on the same image:
1. Left: Straight wall segment (standard 1×1 tile, as described above)
2. Center: Corner wall piece (90° corner, same style — two faces visible, square footprint)
3. Right: T-intersection cap (wall that connects on three sides — for wall crossings)

All three on flat dark background. Transparent alpha where there is no object.
```

---

## Checklist — What This Prompt Establishes

- [x] Camera angle (isometric 30-degree, SE facing)
- [x] Art style (stylized, 2px outline, baked lighting, not pixel art)
- [x] Shape and proportions (1×1 tile, 1.5 tiles tall)
- [x] Material (concrete, seam lines, rebar stub, grime)
- [x] Color palette (three faces + outline + grime)
- [x] Detail level (minimal — gameplay readable)
- [x] Three tile variants (straight, corner, T-intersection)
- [x] Scale reference included
- [x] Transparent / dark background (clean sprite output)
