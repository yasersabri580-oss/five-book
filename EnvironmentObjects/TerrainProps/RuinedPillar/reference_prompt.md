# REFERENCE IMAGE PROMPT — RUINED PILLAR

---

## Purpose
This prompt generates the **canonical reference image** for the RuinedPillar.
Both height variants must be visually consistent in material, color, and style.

---

## Reference Image Generation Prompt

```
2.5D isometric game asset — Ruined Pillar (two height variants) for the game IRON BREACH.

CAMERA: Isometric 2.5D, 30-degree pitch, south-east facing. Objects shown as standalone sprites on flat near-black background (#121212) or transparent. No scene, no environment.

ART STYLE: Stylized game asset. Crisp 2px black outline. Baked isometric lighting: top/fracture face is lightest, south face is mid-tone, east face is darkest. NOT pixel art. NOT photorealistic. Clean, readable, stylized. Consistent with the concrete material language of ConcreteWallSegment in this project.

REFERENCE SHEET LAYOUT: Two panels side by side.

PANEL 1 — TALL PILLAR VARIANT (1.5 tile height, 0.5 tile footprint):
- A reinforced concrete rectangular column, fractured at the top with a rough diagonal break. The break is at approximately 1.5 isometric tiles from the ground. The break exposes: 2–3 bent rebar strands in dark rust-orange (#7A4A28), angling outward in different directions from the top edge. The fracture face (the raw broken top) is lighter than the intact sides — showing fresh concrete interior (#6A6460). Diagonal crack lines run from the break downward along the south face, tapering out before they reach halfway down. Small rubble chips at the very base of the pillar on the ground, same color as the main concrete. Dark staining (water/oil/grime) near the base, #2A1A0A dark streak.

PANEL 2 — STUB PILLAR VARIANT (0.75 tile height, 0.5 tile footprint):
- Same column material and style. The break is much lower — only 0.75 isometric tiles tall. Wider rubble scatter at the base (more rubble = more was knocked off). Rebar still exposed at top — same treatment as tall variant. One additional diagonal crack on the south face of this shorter stub.

COLOR PALETTE (both panels):
- Main concrete body: #484644 (desaturated grey-brown)
- Top break fracture face: #6A6460 (lighter — fresh interior)
- East/shadow face: #2A2220 (darkest)
- Rebar: #7A4A28 (rust-orange, dark)
- Rubble chips: same as main concrete, #484644 fragments
- Grime staining at base: #2A1A0A dark streak
- Outline: #0A0A0A (2px black)

IMPORTANT NOTES:
- The column is NOT smooth — it has subtle surface texture suggesting formwork and age
- The rebar strands must look structural, not decorative. They are bent outward by the force of the break, not artistically arranged.
- Rubble at the base is just 3–5 small irregular chips, not a full rubble pile — for that see the WeakWallSection destroyed state
- No text, no logos, no symbols on the column

SCALE REFERENCE: Include a faint isometric tile grid ghost under each panel.

OUTPUT: One horizontal reference sheet with two panels. Left panel: Tall Pillar. Right panel: Stub Pillar. Both labeled. Dark background.
```

---

## Checklist — What This Prompt Establishes

- [x] Camera angle (isometric 30-degree, SE facing)
- [x] Art style (stylized, baked lighting, 2px outline)
- [x] Two height variants (tall 1.5 tile, stub 0.75 tile)
- [x] Material (reinforced concrete, rebar exposure, fracture face)
- [x] Color palette (body, fracture face, shadow, rebar, grime)
- [x] Break and crack detail (diagonal cracks, 2–3 rebar strands)
- [x] Rubble at base (minimal chips, not full pile)
- [x] Scale reference (tile grid ghost)
- [x] Dark background (clean sprite output)
