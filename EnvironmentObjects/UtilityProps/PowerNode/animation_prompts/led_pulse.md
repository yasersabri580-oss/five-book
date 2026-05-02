# ANIMATION PROMPTS — POWER NODE

---

## Animation Status

**Minimal animation: LED idle pulse (2 frames, looping) in active state.**
Destroyed state is a static sprite.

---

## ANIMATION 1 — LED IDLE PULSE (Active State, 2 frames)

```
2-frame looping LED pulse for the PowerNode active state. Only the LED panel and indicator light change — the housing is completely static.

CAMERA: Isometric 2.5D, same as reference.
ART STYLE: Same as reference.

Implementation note: This can be implemented as a 2-frame animation on the entire active sprite, OR as a child LED sprite layer on the node. Child layer approach is preferred (saves redrawing the housing each frame).

FRAME 1 — PULSE LOW:
- LED panel: amber (#C8A020) at 70% brightness. Glow halo is minimal (1px, barely perceptible).
- Indicator LED: green (#20C440) at normal brightness. Standard glow.

FRAME 2 — PULSE PEAK:
- LED panel: amber (#D8B030) at 100% brightness. 2px amber glow halo (#A08010 fading).
- Indicator LED: green (#30D450) slightly brighter. Glow slightly larger.
- The data bars on the LED panel: very slightly more visible on this frame (same amber, just at full brightness).

Frame timing: Frame 1 holds 0.8s, Frame 2 holds 0.3s (a slow, calm pulse — this is infrastructure, not an alarm).
Loop: Yes — continuous in active state.
```

---

## Static Sprites Summary

| State | Sprite | Animation |
|---|---|---|
| Active (south-facing) | `powernode_active_s.png` | 2-frame LED pulse |
| Active (east-facing) | `powernode_active_e.png` | 2-frame LED pulse |
| Destroyed (south) | `powernode_destroyed_s.png` | None |
| Destroyed (east) | `powernode_destroyed_e.png` | None |
