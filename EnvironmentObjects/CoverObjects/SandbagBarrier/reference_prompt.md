# REFERENCE IMAGE PROMPT — SANDBAG BARRIER

---

## Purpose
This prompt generates the **canonical reference image** for the SandbagBarrier.
The soft rounded organic shape must be immediately distinguishable from hard angular concrete objects.

---

## Reference Image Generation Prompt

```
2.5D isometric game asset — Sandbag Barrier (four variants) for the game IRON BREACH.

CAMERA: Isometric 2.5D, 30-degree pitch, south-east facing. Objects shown as standalone sprites on flat near-black background (#121212). No environment.

ART STYLE: Stylized game asset. Crisp 2px black outline. Baked isometric lighting: top face lightest, south face mid-tone, east shadow face darkest. The sandbags are SOFT and ROUNDED — in direct visual contrast to the hard angular concrete and steel objects in this project. Burlap texture: simplified cross-hatch or weave lines on each bag face. NOT pixel art. NOT photorealistic. The bags must read as heavy, dense, filled-to-bursting — combat cover.

REFERENCE SHEET: Four panels side by side.

PANEL 1 — SINGLE ROW BARRIER (1 tile wide × 0.5 tile deep × 0.4 tile tall):
- A row of 3 sandbags, tightly packed side by side. Each bag is an ovoid mound shape — wider in the middle, tapering toward each end. The bags press against each other, slightly deforming where they contact.
- SOUTH FACE of each bag: the most visible face. Each bag: a rounded mound front with soft shading (lighter center #A08A68, darker at the edges and base #5A4A30 where the bag compresses against the ground and adjacent bags). A subtle burlap pattern across the face — simplified diagonal cross-hatch lines (#6A5A40 on #8A7A58), not a photorealistic weave, just enough to suggest burlap texture.
- TOP FACE of each bag (angled, partially visible from isometric camera): A pinch/tie point at the top center of each bag — the burlap is gathered and tied with a dark rope. The rope tie is a small dark knot (#3A2A18) at the bag's top-center, with slight puckering of the fabric around it (slightly irregular top shape due to the tie).
- DIRT TRICKLE: At the left and right ends of the barrier, a very subtle sand/dirt trickle on the ground at the base of the end bags — 2–3 small sand-color dots (#8A7A58) suggesting the bags leak slightly.
- The three bags rest on the ground with a slight flattening at the base contact point (base shadow #4A3A28).
- SEAMLESS EDGE: The left and right edges of the sprite are designed to connect seamlessly when placed adjacent to another barrier segment.

PANEL 2 — DOUBLE ROW (STACKED) BARRIER (1 tile wide × 0.5 tile deep × 0.7 tile tall):
- Two rows of sandbags stacked: 3 bags on the bottom (same as Panel 1), 3 bags on top but offset by half a bag width (like a brick-lay pattern — the seams of the top row do not align with the seams of the bottom row).
- The top row bags are visually similar to the bottom row bags but slightly smaller (they look slightly compressed by gravity from the bags below).
- The top row also has tie-points. The top row bags sit in the grooves between the bottom row bags (stable stacking).
- Overall the double stack reads as a more significant cover barrier — taller and more substantial.
- Same dirt trickle at the base ends.

PANEL 3 — END CAP VARIANT (0.5 tile wide — half-barrier for barrier line ends):
- A single sandbag (one bag only). The same bag shape as in Panel 1 but isolated. Left or right end cap: the bag's far end tapers to show the end of the barrier run naturally. Used at the left end or right end of a long sandbag barrier run to avoid cut-off edges.
- Same art treatment as individual bags in Panel 1.

PANEL 4 — CRUSHED GROUND DECAL:
- The barrier has been crushed by a tank. A flat, low ground-level sprite.
- The bags have been flattened — they are no longer ovoid, they are flat irregular spread-out shapes, still showing burlap texture but compressed. Sand has spilled out: a spread of sandy tan (#A08A68, irregular irregular patch) around the flattened bag shapes.
- No height — this is a flat ground decal (placed on the Ground sorting layer, no collision).

COLOR PALETTE:
- Sandbag base: #8A7A58 (warm sandy tan)
- Sandbag highlight: #A08A68 (lighter center/top face)
- Sandbag shadow/edges: #5A4A30 (darker — compressed areas)
- Sandbag deep shadow: #4A3A28 (base contact area)
- Burlap weave lines: #6A5A40 (subtle cross-hatch on mid-tones)
- Rope tie: #3A2A18 (dark rope/twine)
- Dirt trickle/sand spill: #8A7A58 (same as base, small dots)
- Crushed sand spill: #A08A68 (lighter spread patch)
- Outline: #0A0A0A (2px)

SCALE REFERENCE: Include a faint isometric tile grid ghost. The single row barrier (0.4 tile tall) and double row (0.7 tile tall) should be clearly visible in proportion to the grid.

OUTPUT: One horizontal reference sheet, four panels: Single Row, Double Row Stacked, End Cap, Crushed Decal. All labeled. Dark background.
```

---

## Checklist — What This Prompt Establishes

- [x] Camera angle (isometric 30-degree, SE facing)
- [x] Art style (stylized, soft and rounded — visually contrasts angular concrete)
- [x] Four variants (single row, double row stacked, end cap, crushed decal)
- [x] Material detail (burlap weave, rope tie, sand trickle, compression)
- [x] Seamless left/right edge for tiling
- [x] Color palette (all elements with hex codes)
- [x] Scale reference (tile grid ghost, height comparison)
- [x] Dark background
