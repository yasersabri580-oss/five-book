# ANIMATION PROMPTS — REPAIR STATION

---

## Animation Status

**Animation required: healing-in-progress pulse (3 frames, loops during 2s heal).**
All other states are static sprites.

---

## ANIMATION 1 — HEALING IN PROGRESS (3 frames, looping)

```
3-frame looping animation for the RepairStation while the player is actively healing (holding E and the 2s progress is filling). Based on the canonical reference image (Available state, Panel 1). Preserve all visual identity — only the indicator light and cross brightness change.

CAMERA: Isometric 2.5D, same as reference.
ART STYLE: Same as reference sprite.

Context: The player is holding E. The UI progress bar is filling. This animation loops during the 2s hold duration and stops when healing completes (station transitions to Used/1-remaining or Depleted sprite).

FRAME 1 — HEALING PULSE START:
Base state: Available (Panel 1 reference). The red cross is at normal brightness (#C42020). The indicator light is bright green as normal. No change from base state — this is the "between pulses" frame.

FRAME 2 — HEALING PULSE PEAK:
The red cross brightens significantly: #E83030 (noticeably brighter red). The cross acquires a subtle warm glow halo — 2px soft warm red-orange edge glow (#FF6020 very faint) bleeding slightly beyond the cross shape. The indicator light also brightens: #40F060 (brighter, more saturated green). The whole access panel very subtly brightens (panel color from #6A6A68 to #787874 — barely perceptible). This peak frame communicates "active healing pulse."

FRAME 3 — HEALING PULSE FALLING:
The cross returns to base brightness (#C42020). The glow halo is almost gone — just the faintest trace. The indicator light is back to normal (#20C440). This is the transition frame back to Frame 1.

Total frames: 3
Frame timing: 0.15s each (one pulse cycle = 0.45s — about 4–5 pulses during the 2s hold)
Loop: Yes — continuous while player holds E.
Stop condition: When healing completes OR player releases E. On completion: transition to the appropriate depleted sprite (1-use remaining or fully depleted).
```

---

## Static Sprites Summary

| State | Sprite | Animation |
|---|---|---|
| Available (full charge) | `repairstation_available.png` | None (base state) |
| Healing in progress | `repairstation_available.png` base | 3-frame healing pulse loop |
| One use remaining | `repairstation_oneuse.png` | None |
| Fully depleted | `repairstation_depleted.png` | None |
| Wall-mounted (all states) | Separate sprite set (same logic) | Same as freestanding |
