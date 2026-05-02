# REFERENCE IMAGE PROMPT — POWER NODE

---

## Purpose
This prompt generates the **canonical reference image** for the PowerNode.
This is a small, wall-mounted object — the LED panel and indicator light are the critical readable elements.

---

## Reference Image Generation Prompt

```
2.5D isometric game asset — Power Node (two orientations, active and destroyed states) for the game IRON BREACH.

CAMERA: Isometric 2.5D, 30-degree pitch, south-east facing. Objects shown mounted against a thin wall section stub (show just 0.2 tile of ConcreteWallSegment as context for the mounting surface). Flat near-black background (#121212). No full environment.

ART STYLE: Stylized game asset. Crisp 2px black outline. Baked isometric lighting: front face (south or east) is mid-tone, any top edge surface slightly lighter, side faces darker. The LED panel and indicator light are self-illuminated — they are brighter than the ambient lighting. NOT pixel art. NOT photorealistic. Small object — detail must be minimal but legible.

NOTE: Each panel in the reference sheet should be shown at 3× game resolution for detail clarity, with a label noting the actual game display size.

REFERENCE SHEET: Four panels.

PANEL 1 — SOUTH-WALL-MOUNTED, ACTIVE (facing south, mounted on south wall face):
- The power node: 0.4 tile wide × 0.1 tile deep (protrudes 0.1 tile from wall surface) × 0.5 tile tall. It is shown mounted flush against the grey wall section stub.
- HOUSING: Dark metal box, #1E2228 (very dark blue-charcoal). The housing front face (south-facing) is the main visible face. A very faint FORGE triangle embossed on the housing surface (barely visible — same dark family, slightly lighter #282E34).
- LED PANEL: Centered on the front face. A small rectangular panel (approximately 0.15 tile wide × 0.1 tile tall, at game scale this is about 8×5 px). Inside the panel:
  - A bright amber glow (#C8A020, self-illuminated). A very faint 1px amber glow halo bleeds beyond the panel border.
  - 2–3 thin amber horizontal lines on the panel face (abstract data bars, very short — just 2–3 px per bar at game resolution). These suggest live data feed.
  - The panel has a thin dark grey frame/bezel (#1A1A18) around the lit area.
- INDICATOR LED: In the upper-right corner of the front face, a very small circle (2×2 px at game resolution). BRIGHT GREEN (#20C440) with a tiny 1px glow halo. This is the "active/online" indicator.
- NODE ID PLATE: Below the LED panel, a small dark rectangular plaque (#141618). No readable text — just the plaque shape.
- CABLE CONDUITS: Two conduits enter the housing from the TOP: two dark grey tubes (#2A2A28), each approximately 0.06 tile wide, entering the top of the housing from above. The conduit ends at the top of the housing — the cables above are against the wall and not drawn (they run along the wall surface above frame). Two cables EXIT from the BOTTOM of the housing: one exits left (along the wall, disappearing off the left edge), one exits right (along the wall, disappearing off the right edge). The cables hugging the wall are a flat dark grey stripe against the wall texture.

PANEL 2 — SOUTH-WALL-MOUNTED, DESTROYED:
- Same housing, damaged. Housing is cracked: a diagonal crack on the front face, 1px thin. A scorch mark radiating from the crack (#0A0806 dark radial soot). The housing front face is blackened around the crack area.
- LED PANEL: DARK — #0A0E10, no glow.
- INDICATOR LED: OFF — same color as housing, no glow.
- Cables: still connected (the cables are in the wall — they don't drop away on node destruction).

PANEL 3 — EAST-WALL-MOUNTED, ACTIVE (facing east, mounted on east wall face):
- Same node, but mounted on the east-facing wall surface. The east face is the camera-shadow face — darker overall. The node front face is also darker (#161C22 very dark). But the LED panel and indicator light must still be clearly visible — these are self-illuminated and should read clearly even on the dark face.
- Cable conduits same setup as Panel 1 but oriented for the east-wall mounting.

PANEL 4 — INTERACTIVE CLOSE-UP (3× zoom reference for the LED panel detail):
- Just the front face of an active node, very large, showing the LED panel and indicator in detail. This is a reference only for art team — not a game sprite. Shows the exact amber data lines, indicator glow, panel bezel, and FORGE emboss at clear resolution.

COLOR PALETTE:
- Housing: #1E2228 (dark blue-charcoal)
- Housing front (east-mounted, darker): #161C22
- FORGE emboss: #282E34 (barely visible)
- LED panel glow: #C8A020 (amber) + 1px halo
- LED data bars: same amber, thinner
- LED panel bezel: #1A1A18
- Indicator LED: #20C440 (green) + 1px halo
- ID plate: #141618
- Cable conduits: #2A2A28
- Destroyed scorch: #0A0806
- LED off: #0A0E10
- Outline: #0A0A0A (2px)

OUTPUT: One reference sheet, four panels: Active South, Destroyed South, Active East, Close-up Detail. All labeled. Dark background.
```

---

## Checklist — What This Prompt Establishes

- [x] Camera angle (isometric 30-degree, SE facing)
- [x] Art style (stylized, self-illuminated LED, 2px outline, minimal detail)
- [x] Both wall-mount orientations (south and east)
- [x] Active and destroyed states
- [x] Critical: LED panel + indicator light visible even at small game size
- [x] Cable conduits entering/exiting the housing
- [x] FORGE emboss (subtle)
- [x] Color palette (all elements)
- [x] Scale note (3× zoom for reference)
- [x] Dark background
