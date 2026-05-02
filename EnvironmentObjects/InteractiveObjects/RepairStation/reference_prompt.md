# REFERENCE IMAGE PROMPT — REPAIR STATION

---

## Purpose
This prompt generates the **canonical reference image** for the RepairStation.
The red cross and indicator light are the critical visual communication elements.

---

## Reference Image Generation Prompt

```
2.5D isometric game asset — Repair Station (three availability states) for the game IRON BREACH.

CAMERA: Isometric 2.5D, 30-degree pitch, south-east facing. Objects shown as standalone sprites on flat near-black background (#121212). No environment.

ART STYLE: Stylized game asset. Crisp 2px black outline. Baked isometric lighting: top face lightest, south face mid-tone, east face darkest. The red cross on the front panel is the dominant visual element — do NOT understate it. NOT pixel art. NOT photorealistic. This object must read as "healing available" the moment it appears on screen.

REFERENCE SHEET: Three panels side by side.

PANEL 1 — AVAILABLE STATE (full charge):
- Freestanding cabinet: 0.9 isometric tile wide × 0.5 tile deep × 1.2 tiles tall.
- Cabinet body: matte olive-green (#3A4830) on all faces. Top face: lighter (#4A5838). East/shadow face: darker (#28321E).
- SOUTH FACE (camera-facing front): A lighter grey access panel occupies the center 60% of the south face height (#6A6A68 grey panel, recessed slightly — 1px inset from the cabinet body edges). On this access panel: a BOLD RED CROSS (#C42020). The cross is simple — two rectangles at 90°, each arm of equal width, centered on the access panel. The cross must be visible and readable at 32×32 px minimum. The cross is raised (slightly proud of the panel surface — a subtle bevel outline on the cross shape, slightly lighter #E03030 on the top-left edge of each arm, darker #A01010 on the bottom-right edge).
- INDICATOR LIGHT: At the very top-center of the south face, above the access panel: a small square light indicator (5×5 px in game). BRIGHT GREEN (#20C440) — the light glows, add a 1–2 px soft glow halo in lighter green (#40D460).
- Access panel handle: a small horizontal bar on the right side of the access panel (#4A4A48 dark grey, slightly raised).
- BASE PIPE: at the bottom-right corner, a small pipe or conduit nub connects to the floor (dark #28281E, barely prominent).
- Cabinet wear: subtle dents (a slight concave shadow depression) on the top-left corner and lower-right of the cabinet body. Scuff marks along the lower front edge.
- MANUFACTURER PLATE: Very bottom of the south face, below the access panel: a small flat dark rectangle (#1A2018) with no readable text.

PANEL 2 — ONE USE REMAINING STATE:
- Identical cabinet body. One use has been consumed.
- The access panel: the red cross is now dimmer/darker — #8A1010 (darker red, the cross is still visible but less vibrant). A slight crack or scratch line across one arm of the cross (suggesting it has been used/stressed).
- INDICATOR LIGHT: AMBER (#C8A020) with amber glow halo — the station is at half capacity.
- The access panel handle has a very slight smudge/hand-mark dirt (#2A2820 faint print) — suggesting it has been touched once.

PANEL 3 — FULLY DEPLETED STATE:
- Same cabinet body. Both uses consumed.
- The access panel: the red cross is gone — the access panel is now flat grey (#6A6A68) with a scratched/smudged surface where the cross was. An EMPTY outline of where the cross was is barely visible as a slightly lighter #727272 ghost-shape. The station is visually spent.
- INDICATOR LIGHT: OFF — same color as cabinet body (#283220). Just a dark square, no glow.
- The access panel handle is further smudged/marked.

COLOR PALETTE:
- Cabinet body: #3A4830 (matte olive-green)
- Cabinet top face: #4A5838 (lighter green-grey)
- Cabinet east/shadow face: #28321E (dark green)
- Access panel: #6A6A68 (grey panel)
- Red cross (available): #C42020 (bright danger red)
- Red cross highlight: #E03030 (top-left bevel edge)
- Red cross shadow: #A01010 (bottom-right bevel edge)
- Red cross (1-use remaining): #8A1010 (dimmed red)
- Indicator light (available): #20C440 (green) + glow halo
- Indicator light (1-use): #C8A020 (amber) + glow halo
- Indicator light (depleted): #283220 (dark, no glow)
- Handle: #4A4A48
- Outline: #0A0A0A (2px)

SCALE REFERENCE: Include a faint isometric tile grid ghost under each panel.

OUTPUT: One horizontal reference sheet, three panels: Available, One-Use Remaining, Depleted. All labeled. Dark background.
```

---

## Checklist — What This Prompt Establishes

- [x] Camera angle (isometric 30-degree, SE facing)
- [x] Art style (stylized, baked lighting, 2px outline, bold red cross)
- [x] Three availability states (full, 1-use, depleted)
- [x] Critical: red cross is primary visual element, readable at 32×32 px
- [x] Indicator light (green/amber/off clearly communicates state)
- [x] Cabinet detail (wear, dents, handle, pipe nub, manufacturer plate)
- [x] Color palette (all elements with hex codes)
- [x] Scale reference (tile grid ghost)
- [x] Dark background
