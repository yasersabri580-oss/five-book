# REFERENCE IMAGE PROMPT — FUEL TANK

---

## Purpose
This prompt generates the **canonical reference image** for the FuelTank.
The horizontal cylinder silhouette and orange hazard diamond must be the primary visual identifiers.

---

## Reference Image Generation Prompt

```
2.5D isometric game asset — Fuel Tank (two states + orientation variant) for the game IRON BREACH.

CAMERA: Isometric 2.5D, 30-degree pitch, south-east facing. Objects shown as standalone sprites on flat near-black background (#121212). No environment.

ART STYLE: Stylized game asset. Crisp 2px black outline. Baked isometric lighting on the cylindrical form — the top curved surface is the lightest, the south-facing curved surface is mid-tone, the shadow areas at the cylinder bottom and east side are darkest. The cylinder is not perfectly round in isometric — it reads as a slightly flattened oval in profile. NOT pixel art. NOT photorealistic.

REFERENCE SHEET: Three panels.

PANEL 1 — INTACT FUEL TANK (south-facing, tank length east-west):
- SHAPE: Horizontal cylindrical steel tank, 1.0 isometric tile wide (east-west) × 0.6 tile deep (north-south) × 0.5 tile tall (the cylinder diameter). Total height with support legs: 0.7 tile (supports add 0.2 tile below).
- TWO SADDLE SUPPORTS: A-frame steel brackets, one at each end (approximately 0.2 tile from each end of the tank). Each support: a simple A-frame shape in dark grey steel (#2E2E2C). The legs of the A-frame rest on the ground. The curved saddle cradles the bottom of the cylinder.
- TANK BODY: Military olive-green (#3A4828). The top curved face is lighter (#4A5A34). The bottom and east/shadow face is darker (#283218).
- CYLINDER SEAMS: 2 circumferential rivet seam rings around the cylinder, visible on the front curved face — one at 1/3 length from left end, one at 2/3 length. Each seam ring is a thin dark line (#242E1A) with small rivet dots.
- END CAPS: The left and right cylinder end faces (visible at isometric angle on the left end — the cap is circular). The end cap has: a subtle concave center (suggesting the domed end cap shape). WARNING STRIPES across the end cap face: 4–5 diagonal yellow (#C8A020) and black (#1A1A18) stripes at 45°.
- SOUTH FACE (front curved face, most visible):
  - HAZARD DIAMOND: Centered on the south face, a standard hazard diamond shape. The diamond border: orange-red (#C84010). Background inside the diamond: slightly lighter than the tank body (#485A34). A flame icon inside the diamond — a simple cartoon flame silhouette (orange #C84010, readable as a flame symbol at small size). This is the primary warning indicator.
  - FUEL GAUGE SIGHT GLASS: To the right of center on the south face, a small vertical rectangle (sight glass window). Frame: dark grey metal (#2A2A28). Inside the glass: a vertical liquid column, dark greenish (#1A2A10 dark liquid) filling approximately 70% of the glass height (tank 70% full). A small horizontal line marks the fill level.
  - VALVE PIPE + WHEEL: At the lower-right area of the south face, near the support leg: a short stubby pipe nub (#2A2A28) protruding from the tank, with a small valve wheel at its end (a flat wheel-spoke shape, dark metal). Very small but recognizable.
  - FILLER PORT: On the TOP face of the cylinder, centered: a small recessed circular port (#1A1A18 dark metal rim, darker inside). A small closed cap on top.

PANEL 2 — LEAKING STATE (damaged):
- Same tank, same orientiation. The south face: a horizontal crack near the bottom of the cylinder body (a thin irregular crack line #1A1008). Below the crack, a dark fuel drip: a small vertical dark streak (#1A1008 oily dark liquid) running down the tank face to the support, and a small dark pooling area at the base of the south face on the ground. The hazard diamond is more prominent now — the danger is real.

PANEL 3 — EAST-FACING ORIENTATION (tank length north-south):
- The same intact tank rotated 90°. Now the tank length runs north-south (the cylinder is shown in its width from the isometric camera angle). This is the alternate placement orientation. The south-facing end cap is now the primary visible face — showing the warning stripes prominently. The saddle support is seen from the side. The south face of the cylinder body shows the hazard diamond from a more foreshortened angle.

COLOR PALETTE:
- Tank body: #3A4828 (olive-green)
- Tank top: #4A5A34 (lighter)
- Tank shadow: #283218 (dark)
- Seam rings: #242E1A
- Saddle supports: #2E2E2C
- Warning stripes: #C8A020 (yellow) + #1A1A18 (black)
- Hazard diamond: #C84010 (orange-red) outline + flame icon
- Fuel gauge liquid: #1A2A10 (dark fuel)
- Valve pipe + wheel: #2A2A28
- Filler port: #1A1A18
- Fuel drip (leaking): #1A1008 (dark oily)
- Outline: #0A0A0A (2px)

SCALE REFERENCE: Include a faint isometric tile grid ghost.

OUTPUT: One reference sheet, three panels: Intact, Leaking, East-Facing. All labeled. Dark background.
```

---

## Checklist — What This Prompt Establishes

- [x] Camera angle (isometric 30-degree, SE facing)
- [x] Art style (stylized, cylindrical form, baked lighting, 2px outline)
- [x] Intact, leaking, and east-facing orientation variants
- [x] Critical: orange hazard diamond with flame icon is primary danger indicator
- [x] Detail elements (seam rings, saddle supports, sight glass, valve wheel, filler port, warning stripes)
- [x] Color palette (all elements with hex codes)
- [x] Scale reference (tile grid ghost)
- [x] Dark background
