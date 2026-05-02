# REFERENCE IMAGE PROMPT — CONCRETE BLOCK

---

## Purpose
This prompt generates the **canonical reference image** for the ConcreteBlock.
The trapezoidal silhouette (jersey-barrier profile) is the critical visual differentiator from the ConcreteWallSegment.

---

## Reference Image Generation Prompt

```
2.5D isometric game asset — Concrete Block (standalone and row-of-three variant) for the game IRON BREACH.

CAMERA: Isometric 2.5D, 30-degree pitch, south-east facing. Objects shown as standalone sprites on flat near-black background (#121212). No environment.

ART STYLE: Stylized game asset. Crisp 2px black outline. Baked isometric lighting: top face lightest, south face mid-tone, east shadow face darkest. Machine-formed smooth concrete — NOT rough stone, NOT brick. Smooth flat faces with only subtle surface marks. The trapezoidal profile is the key shape. NOT pixel art. NOT photorealistic.

REFERENCE SHEET: Two panels.

PANEL 1 — SINGLE CONCRETE BLOCK:
- 1 isometric tile wide × 0.6 tile deep × 1.0 tile tall.
- SHAPE: Jersey-barrier style. In isometric view, the south face shows a TRAPEZOIDAL profile — the base is wider than the top. The base-to-top taper is approximately 15° on each side (total: the top face is about 70% of the base width). This taper must be clearly visible in the isometric view.
- TOP FACE: Flat, slightly lighter (#5E5E5A). One REBAR LIFTING LOOP embedded flush in the top face: a simple U-shaped dark metal bar (#3A3A38), both ends embedded in the concrete, arch above the surface by 3–5 px. The loop is centered on the top face. It is clearly metal, clearly a functional lifting handle.
- SOUTH FACE: Base grey concrete (#4A4A48). The tapered shape means the south face is a trapezoid — wider at the bottom. Surface marks:
  - MIDLINE SEAM: A single faint horizontal line at mid-height (#3A3A38, 1px, running the full width) — the mold parting line where the two-piece form was separated. Very subtle.
  - TIRE SCUFF: On the lower third of the south face, a dark rubber smear (#2A2020) — irregular, horizontal, suggesting a vehicle has scraped against the block. Approximately 30% of the south face width. Not a uniform stripe — a natural looking smear.
  - FADED SAFETY STRIPE: Along the very bottom edge of the south face, a barely-visible yellow stripe (#8A6800, very faded and worn — originally a warning stripe from the block's road-divider past). Only 5–8% of the face height. Partially obscured by dirt.
  - CRACKED CORNER: At the lower-left corner of the south face, a small diagonal crack radiating from the corner into the face — thin, 1px, approximately 10% of the face height in length.
- EAST FACE: Dark (#2A2A28). Fewer details — just the overall block shape and the tapered profile visible. Midline seam also continues on this face.
- BASE: A very subtle ambient occlusion shadow at the very base where the block meets the ground (#1E1E1C dark strip, very thin at base edge).

PANEL 2 — ROW OF THREE BLOCKS:
- Three blocks placed side by side. The blocks share the same ground line. No gaps between them — they touch side-to-side.
- The middle block is slightly offset in depth by 0.05 tile to the south (toward the camera), giving a very slight stagger and preventing a perfectly flat front face — this looks more natural, as if the blocks were placed by a vehicle and aren't perfectly aligned.
- Only the outer-facing south and east surfaces of the end blocks are visible (the touching faces are hidden). The overall row reads as a barrier line.
- The row is 3 tiles wide total, 0.6 tile deep, 1.0 tile tall.

COLOR PALETTE:
- Main body: #4A4A48 (base grey)
- Top face: #5E5E5A (lighter)
- East/shadow face: #2A2A28 (darkest)
- Midline seam: #3A3A38 (subtle)
- Tire scuff: #2A2020 (dark rubber)
- Safety stripe: #8A6800 (very faded yellow)
- Crack: #2A2A28 (thin dark crack line)
- Rebar loop: #3A3A38 (dark metal U-shape)
- Base shadow: #1E1E1C
- Outline: #0A0A0A (2px)

SCALE REFERENCE: Include a faint isometric tile grid ghost. Show that the block is 1 tile wide × 0.6 tile deep × 1.0 tile tall.

OUTPUT: One reference sheet, two panels: Single Block and Row of Three. Both labeled. Dark background.
```

---

## Checklist — What This Prompt Establishes

- [x] Camera angle (isometric 30-degree, SE facing)
- [x] Art style (stylized, smooth machine-formed concrete, baked lighting, 2px outline)
- [x] Single block and row-of-three variant
- [x] Critical: trapezoidal profile clearly visible (jersey-barrier silhouette)
- [x] Detail elements (mold seam, tire scuff, faded stripe, corner crack, rebar loop)
- [x] Color palette (all elements with hex codes)
- [x] Scale reference (tile grid ghost)
- [x] Dark background
