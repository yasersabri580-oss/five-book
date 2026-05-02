# ANIMATION PROMPTS — CONTROL TERMINAL

---

## Animation Status

**Animation required: screen idle loop (4 frames), interacting state pulse (4 frames).**
Static sprites handle: used state, disabled state.

---

## ANIMATION 1 — IDLE SCREEN LOOP (4 frames)

```
4-frame looping idle screen animation for the ControlTerminal. Based on the canonical reference image (Panel 1 — Idle state). Preserve all visual identity. Only the screen changes between frames — housing, LEDs, and cable are identical in all frames.

CAMERA: Isometric 2.5D, same as reference.
ART STYLE: Same as reference — crisp 2px outline, baked lighting on housing, emissive screen.

Screen base: abstract data grid — horizontal and vertical lines forming a loose grid (#20C480 cyan-green). A single vertical scan line moves upward across the screen.

FRAME 1 — SCAN LINE AT BOTTOM:
Scan line (a 2px-wide bright vertical band, #30F0A0 bright cyan-green, slightly brighter than the base grid) is positioned at the bottom 20% of the screen. The data grid is at full idle brightness (#20C480). Some grid cells show filled bars (random pattern, fixed between frames — only the scan line moves).

FRAME 2 — SCAN LINE AT MID-LOW:
Same as Frame 1. Scan line has moved to the 40% vertical position on the screen.

FRAME 3 — SCAN LINE AT MID-HIGH:
Same as Frame 1. Scan line at 65% vertical position.

FRAME 4 — SCAN LINE AT TOP:
Scan line at the 85% position, just below the top edge. On this frame, the scan line is slightly fainter (as it approaches the top and will loop back to the bottom).

Total frames: 4
Frame timing: 0.2s per frame (scan line completes one pass in 0.8s — a slow, meditative idle rhythm)
Loop: Yes — continuous loop while terminal is in idle/active state.
```

---

## ANIMATION 2 — INTERACTING STATE PULSE (4 frames)

```
4-frame looping animation for the ControlTerminal while the player is actively hacking (holding E). Based on the canonical reference image (Panel 2 — Interacting state).

Screen is brighter overall during this state (see reference Panel 2). The pulse is a rectangular ring expanding outward from the screen center.

FRAME 1 — PULSE RING SMALL:
A bright green rectangle ring (#30F0A0) centered on the screen. Ring is at 30% of screen size. Ring border width: 2px. Background data grid is still visible behind the ring (ring is overlaid, not replacing the grid).

FRAME 2 — PULSE RING MEDIUM:
Ring expands to 60% of screen size. Ring becomes slightly more transparent at the edges (inner brightness #30F0A0, outer edge fades toward #20C480).

FRAME 3 — PULSE RING LARGE:
Ring expands to 90% of screen size. Ring is now quite faint — nearly at the screen edge. Approaching transparency.

FRAME 4 — PULSE RING GONE / RESET:
Ring is invisible (fully faded). This frame matches the interacting base state (bright grid, no ring visible). Brief reset before the ring starts again.

Total frames: 4
Frame timing: 0.12s per frame (faster than idle — pulse feels urgent while hacking)
Loop: Yes — continuous while player is holding E / interacting.
Stop condition: When interaction completes (success or player releases E), animation stops and static sprite is applied (Used state or back to Idle).
```

---

## Static Sprites Summary

| State | Sprite | Animation |
|---|---|---|
| Idle / Active | Base frame only | 4-frame idle loop |
| Interacting (hacking) | Bright base frame | 4-frame pulse loop |
| Used / Access Granted | `terminal_used.png` | None |
| Disabled / Screen Off | `terminal_off.png` | None |
| Wall-mounted idle | Separate sprite | Optional idle loop (same logic, smaller) |
