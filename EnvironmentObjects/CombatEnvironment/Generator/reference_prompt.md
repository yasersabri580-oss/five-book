# REFERENCE IMAGE PROMPT — GENERATOR

---

## Purpose
This prompt generates the **canonical reference image** for the Generator.
This is the largest environment object — it must be immediately readable as a power source and a target.

---

## Reference Image Generation Prompt

```
2.5D isometric game asset — Industrial Generator (operational and destroyed states) for the game IRON BREACH.

CAMERA: Isometric 2.5D, 30-degree pitch, south-east facing. Object shown as standalone sprite on flat near-black background (#121212). No environment.

ART STYLE: Stylized game asset. Crisp 2px black outline. Baked isometric lighting: top face lightest, south face mid-tone, east face darkest. Riveted industrial steel aesthetic — dieselpunk. The generator is large (1.5 tiles wide) and must be the most imposing stationary object in the game environment. It should feel heavy, important, and dangerous. NOT pixel art. NOT photorealistic. Bold, readable, industrial.

REFERENCE SHEET: Two rows.

ROW 1 — OPERATIONAL STATE (healthy, running):

MAIN VIEW:
- Total size: 1.5 isometric tiles wide × 1.0 tile deep × 1.2 tiles tall.
- The generator is divided into two visual sections:
  
  LEFT SECTION — ENGINE/TURBINE SECTION (0.8 tile width):
  - Heavier, more closed-off appearance. Dark industrial grey-green (#2E3828) body.
  - Cooling fins on the left face (east face in isometric): a set of 5–6 horizontal parallel fins (#242E1E dark), each fin is a thin horizontal bar projecting 2–3 px from the side face. These fins identify this section as the engine.
  - On the south face of the engine section: a large hinged access panel (suggested by a rectangular frame recess and 4 corner bolts). The panel face is the same dark grey-green but shows rivets around its perimeter and one large locking latch handle in the center.
  - RIVETED SEAMS: Horizontal rivet rows running across the engine section panels. Each rivet is a small circle (#1A2018 dark, with a 1px lighter highlight on the top-left to suggest 3D rivet head). Rivets spaced approximately 0.1 tile apart.

  RIGHT SECTION — CONTROL PANEL SECTION (0.7 tile width):
  - Slightly lighter body (#3A4830) to differentiate from the engine section.
  - SOUTH FACE (control panel): This is the most detailed face (camera-facing).
    - FORGE DATA PLATE: Upper portion of the control panel south face — a dark red panel (#6A1010) with the FORGE triangle logo (same angular downward-pointing triangle as the SecurityDoor emblem, small, #7A1818 slightly lighter on #6A1010 background). A small data plate format — it fills about 25% of the control panel face height.
    - AMBER RUNNING LIGHT STRIP: A horizontal strip of amber light (#C8A020) running along the top edge of the south face of the control section — just below the top edge. Approximately 8px wide (at reference resolution), a glowing amber bar. Add a very faint 1–2px amber glow halo above and below the strip.
    - GAUGES / INDICATORS: Two small circular gauge faces on the south face below the FORGE plate (one above the other). Each gauge: a dark circle (#1A1A18) with a slightly lighter dial face (#2A2A28) and a small indicator needle (orange/amber #C88020). These are purely decorative at game scale — just 2 small circles with a dot.
    - POWER OUTPUT CABLES: Two thick dark grey conduits (#2A2A28) exit from the base-right corner of the control section, curving downward and running off-frame to the right. Each conduit is approximately 4px wide at reference resolution. Metal cable clamp rings visible along the conduit at intervals.

  TOP FACE:
  - EXHAUST VENTS: 3 rectangular slot vents on the top face of the engine section. Each vent: a thin dark slot (#0A0A08 near black) with a very faint upward heat shimmer suggestion (a very faint lighter area just above each vent opening — this is where the animated shimmer will go). Vent grilles: 2px dark bars across each slot.
  - The top face color: slightly lighter than the south face (#3A4828 warm tint), baked top-face lighting.

  BASE:
  - Anchor bolts at each of the four base corners: raised hex-head bolt shapes (#1A1A18), slightly prominent from the base edge.
  - A slight shadow/ambient occlusion at the very base (darkening where the generator meets the ground, #1A1E16 at the base edge).

ROW 2 — DESTROYED STATE (burnt-out wreck):

MAIN VIEW:
- Same 1.5×1.0 tile footprint. Object is still present as a wreck (used as cover by players).
- Color: Heavily scorched — the entire body is now near-black or dark charcoal (#1A1A18 to #2A2A22), with soot marks (radial scorch pattern #0A0808) spreading from the engine section left side.
- FORGE data plate: barely visible — scorched dark, letter plate warped.
- Amber light strip: GONE — dark, no glow.
- Cooling fins: two fins are bent and broken — pointing downward at irregular angles.
- Access panel: blown open — the panel is ajar at a 30° angle, the interior is dark (#0A0A08). One corner bolt is missing (just a hole).
- Exhaust vents: warped, distorted slots. Dark smoke stain spreading upward from the vents (dark upward smear on the top face, #0A0808 radial stain).
- Power cables: the cable conduits are severed — their cut ends dangle at the right side, torn ends.
- OVERALL: The wreck is clearly the same object but completely dead and scorched. It still reads as the generator shape but is visually inert.

COLOR PALETTE:
- Body operational: #2E3828 (dark grey-green)
- Control section: #3A4830 (slightly lighter)
- Top face: #3A4828
- Cooling fins: #242E1E
- Rivets: #1A2018 with 1px lighter highlight
- FORGE data plate: #6A1010 (dark red)
- Amber light strip: #C8A020 + soft glow halo
- Gauges: #1A1A18 circle, #C88020 needle
- Cables: #2A2A28
- Exhaust vents: #0A0A08
- Anchor bolts: #1A1A18
- Outline: #0A0A0A (2px)
- Destroyed: #1A1A18 base, #0A0808 scorch, all color elements dark

SCALE REFERENCE: Include a faint isometric tile grid ghost showing the 1.5×1.0 tile footprint. A small character silhouette (stick figure, same height as Kael Dros — 2.8 tiles) next to the generator for scale reference (generator should reach 1.2 tile height versus the 2.8 tile character).

OUTPUT: Two rows. Row 1: full operational generator, large single panel. Row 2: destroyed generator wreck. Both labeled. Dark background.
```

---

## Checklist — What This Prompt Establishes

- [x] Camera angle (isometric 30-degree, SE facing)
- [x] Art style (stylized, industrial riveted, baked lighting, 2px outline)
- [x] Operational state (full detail — engine section, control panel, lights, cables)
- [x] Destroyed state (scorched wreck, cover-capable)
- [x] Critical elements: amber light strip, FORGE plate, cooling fins, power cables, exhaust vents
- [x] Color palette (all elements with hex codes)
- [x] Scale reference (tile grid ghost + character silhouette)
- [x] Dark background
