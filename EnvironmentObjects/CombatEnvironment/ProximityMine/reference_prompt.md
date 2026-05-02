# REFERENCE IMAGE PROMPT — PROXIMITY MINE

---

## Purpose
This prompt generates the **canonical reference image** for the ProximityMine.
The tiny LED is the most critical element — it must be visible and bright against the dark casing.

---

## Reference Image Generation Prompt

```
2.5D isometric game asset — Proximity Mine (all states + half-hidden variant) for the game IRON BREACH.

CAMERA: Isometric 2.5D, 30-degree pitch, south-east facing. Objects shown on flat near-black background (#121212). No environment. Because the mine is very small (0.3 tile), enlarge the view for the reference sheet (each panel is shown at 3× game resolution for detail clarity — annotate this on the sheet).

ART STYLE: Stylized game asset. Crisp 2px black outline (the entire mine is only about 20–25 px wide at game resolution — the outline and the LED are the dominant visual elements). Baked isometric lighting: the angled top face of the mine hub is slightly lighter. NOT pixel art style, but the small size means minimal detail is possible. The LED must be clearly readable — it is the only bright element on an otherwise dark object.

REFERENCE SHEET: Four panels side by side. Each panel shows the mine at 3× resolution with a note "3× reference zoom, game display ≈ 0.3 isometric tile".

PANEL 1 — ARMED STATE (default):
- Flat circular disc, 0.3 tile diameter, nearly flat on the ground.
- TOP FACE (visible from isometric angle, angled): Dark olive-green (#2A3020). Slightly lighter where the isometric light hits (#323828). The top face shows a subtle circular etched groove running around the perimeter of the disc (a thin dark line #1A2018 just inside the outer edge). This groove is the detonation ring.
- CENTER HUB: A slightly raised circular post in the center of the disc. Dark metal (#1A1A18). A small raised nub at the very center (the pressure trigger point — very small, subtle).
- LED on the hub: A small circle (approximately 3×3 px at game resolution). Currently at slow-pulse dim state — DARK RED (#6A0808, dim — this is the "between pulses" dim state). The LED circle has a barely-perceptible 1px dark red glow halo.
- FORGE TRIANGLE: On the outer ring of the disc, between the etched groove and the outer edge: a small angular triangle mark (#3A4028 — slightly lighter than the disc, barely visible). Very subtle — a detail for close inspection, not a primary visual.
- ONE ATTACHMENT SPIKE: On the south-facing edge of the disc, a small pointed nub extends downward toward the ground (barely 1–2 px, suggesting the mine is staked into the surface).

PANEL 2 — LED PULSE PEAK (armed state, Frame 2):
- Identical to Panel 1 except the LED is at peak brightness: BRIGHT RED (#C42020) with a 2–3 px soft glow halo (#8A1010 fading outward). This is the "beat" moment of the slow pulse.

PANEL 3 — TRIGGERED / WARNING STATE (LED rapid flash):
- Same mine body. LED is at maximum brightness, rapid flash state: #FF2020 (full bright red), 3–4 px glow halo (#C01010 fading), the halo is larger than in Panel 2. The mine body may show a very faint vibration (1 px positional difference from Panel 1 — barely perceptible, suggesting the mine is "live").

PANEL 4 — HALF-HIDDEN VARIANT:
- The mine is 60% covered by a dirt/dust overlay. The disc and hub are partially obscured — only the outer curved edge of the disc and the center hub with LED are clearly visible. The dirt overlay is a rough irregular shape (#4A3A28 dusty brown) covering the left and front portions of the mine. The LED is still fully visible (the hub is not covered). The FORGE triangle is not visible. This variant is used for camouflaged mine placement.

COLOR PALETTE:
- Mine casing: #2A3020 (dark olive-green)
- Mine casing light face: #323828
- Hub: #1A1A18 (dark metal)
- LED (dim/off-beat): #6A0808 (very dark red)
- LED (pulse peak): #C42020 (bright red) + glow halo
- LED (triggered): #FF2020 (maximum red) + larger glow halo
- Etched groove: #1A2018 (thin dark line on disc)
- FORGE triangle: #3A4028 (barely visible)
- Dirt overlay (hidden variant): #4A3A28
- Outline: #0A0A0A (2px)

SCALE NOTE: At actual game resolution, this mine is approximately 20–25 px wide. The reference sheet should note this. The 3× zoom is for reference clarity only.

OUTPUT: One horizontal reference sheet, four panels: Armed (dim), Armed (peak pulse), Triggered, Half-Hidden. All labeled. Dark background.
```

---

## Checklist — What This Prompt Establishes

- [x] Camera angle (isometric 30-degree, SE facing)
- [x] Art style (stylized, 2px outline, minimal detail at tiny size)
- [x] All states: armed-dim, armed-pulse, triggered, half-hidden
- [x] Critical: LED brightness and glow is the readability anchor
- [x] Material detail (disc, etched groove, hub nub, FORGE triangle, attachment spike)
- [x] Color palette (all elements)
- [x] Scale note (3× reference zoom)
- [x] Half-hidden dirt variant
- [x] Dark background
