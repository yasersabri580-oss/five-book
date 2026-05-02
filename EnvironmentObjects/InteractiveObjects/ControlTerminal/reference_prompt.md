# REFERENCE IMAGE PROMPT — CONTROL TERMINAL

---

## Purpose
This prompt generates the **canonical reference image** for the ControlTerminal.
The screen glow and idle animation frames are established from this reference.

---

## Reference Image Generation Prompt

```
2.5D isometric game asset — Control Terminal (freestanding and wall-mounted variants, all states) for the game IRON BREACH.

CAMERA: Isometric 2.5D, 30-degree pitch, south-east facing. Objects shown as standalone sprites on flat near-black background (#121212). No environment.

ART STYLE: Stylized game asset. Crisp 2px black outline. Baked isometric lighting on the housing (top face lightest, south face mid-tone, east face darkest). The SCREEN is the exception — it is self-illuminated (emissive) — brighter than the ambient lighting, with a cyan-green glow that bleeds very slightly beyond the screen boundary (1–2 px soft glow edge). NOT pixel art. NOT photorealistic. The terminal must look like a piece of cold corporate FORGE technology — precise, angular, dark, with the screen as the only warm (well, cold-cyan) light source.

REFERENCE SHEET: Two rows.

ROW 1 — FREESTANDING TERMINAL (0.8×0.6 tile footprint, 1.0 tile tall):

Five panels left to right:

PANEL 1 — IDLE / ACTIVE STATE:
- Freestanding console desk. Front panel (south face): slightly angled screen (30° from vertical, faces up and toward camera). The console housing is matte black-charcoal (#1A1E22). Angular beveled edges. A FORGE brand bar runs along the very top face of the console: a flat matte-dark-red panel (#6A1010) with a small FORGE triangle logo (same angular triangle from the SecurityDoor, reversed — slightly lighter red #7A1818, barely visible on the dark red bar).
- SCREEN: Flat panel display, bright cyan-green (#20C480) base. On the screen, a simplified data visualization: abstract horizontal and vertical lines forming a loose grid, some cells filled with lighter green (#30D890) dots or bars, others empty. The pattern suggests system data or a tactical map but is entirely abstract. NO readable text. One slow-moving vertical scan line (slightly brighter than the base green, moving upward) — this is the animation cue (frame variation).
- Three small LEDs on the front left panel corner: one green (#20C440), one green, one amber (#C8A020). All lit.
- Below the screen: a flat horizontal keyboard panel, slightly recessed — no individual keys, just a flat dark panel (#121618) with a faint horizontal line suggesting the keyboard area.
- Side faces: matte black, only subtle outline detail.
- Cable: at the back-right base corner, a thin dark cable runs down to the ground and off frame.

PANEL 2 — INTERACTING STATE (player is hacking):
- Same as Panel 1. Screen changes: the data visualization brightens significantly — all lines are now brighter (#30F0A0 bright cyan-green), the scan line is now prominent and fast. A subtle rectangular pulse ring appears on the screen (a bright green rectangle, 80% of screen size, pulsing outward — shown at one size for the static reference, animation handles the pulse).
- The three LEDs: all amber now (#C8A020, #C8A020, #C8A020) — system under access.
- Screen overall is 20% brighter than idle state.

PANEL 3 — USED / ACCESS GRANTED STATE:
- Same housing. Screen now shows: a large simple checkmark symbol centered on the screen (#20C440 bright green on a slightly darker #0A3020 background). The data grid is gone — only the checkmark. The screen glow is slightly softer than idle (it has settled). The scan line is gone.
- LEDs: all green (#20C440, #20C440, #20C440).

PANEL 4 — DISABLED / SCREEN OFF STATE:
- Same housing. Screen is dark — #0A0E10 (near black, no glow). Just a dark flat panel. The housing looks identical but powerless. LEDs: all off (same color as housing, no illumination — just dark dots).

PANEL 5 — WALL-MOUNTED VARIANT (IDLE):
- A smaller, flatter version of the terminal. 0.5 tile wide × 0.3 tile deep × 0.7 tile tall. Mounted flush against a wall face. Same matte black housing. Screen angled slightly outward toward the player (25° from the wall face). Same screen data visualization as Panel 1 but smaller. No keyboard panel — just a small flat panel below the screen with 2 LEDs. FORGE brand bar across the top edge. No cable visible (cable is hidden in the wall).

COLOR PALETTE:
- Housing: #1A1E22 (matte black-charcoal)
- Housing top face: #252A2E (lighter face)
- Housing east/shadow face: #10141A (darkest)
- FORGE brand bar: #6A1010 (dark red)
- Screen (idle): #20C480 (cyan-green, emissive)
- Screen (interacting): #30F0A0 (bright cyan-green)
- Screen (used/checkmark): #20C440 on #0A3020
- Screen (off): #0A0E10 (dark)
- LEDs green: #20C440
- LEDs amber: #C8A020
- LEDs off: same as housing
- Screen glow bleed: 1–2px soft halo of #1A8050 beyond screen edge
- Keyboard panel: #121618
- Cable: #0A0A08
- Outline: #0A0A0A (2px)

SCALE REFERENCE: Include a faint isometric tile grid ghost under each panel.

OUTPUT: Two rows — Row 1: five panels (Freestanding: Idle, Interacting, Used, Off, Wall-Mounted Idle). All labeled. Dark background.
```

---

## Checklist — What This Prompt Establishes

- [x] Camera angle (isometric 30-degree, SE facing)
- [x] Art style (stylized, self-illuminated screen, baked housing lighting, 2px outline)
- [x] Freestanding and wall-mounted variants
- [x] Four states (idle, interacting, used/granted, disabled)
- [x] Screen data visualization (abstract grid, scan line, checkmark)
- [x] Color palette (all elements with hex codes, screen glow)
- [x] LED indicators (green active, amber interacting, off disabled)
- [x] FORGE branding (brand bar, triangle logo)
- [x] Scale reference (tile grid ghost)
- [x] Dark background
