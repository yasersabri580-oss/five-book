# ANIMATION PROMPTS — AUTO TURRET

---

## Animation Status

**Animation required: scan (idle), active-tracking, and fire animations for the turret body.**
The pedestal is always static. The turret body sprite rotates separately.

---

## TURRET ROTATION SYSTEM NOTE

The turret body is a SEPARATE SPRITE LAYER above the static pedestal. In Unity, the turret body `SpriteRenderer` is rotated by the `TurretAIController` script to track the player. No frame-by-frame rotation animation is needed — the rotation is handled in code.

Art only needs to provide the turret body facing SOUTH (the canonical orientation). The engine rotates the sprite in 2D, which will look slightly incorrect at extreme angles in isometric — this is acceptable and matches the 2.5D visual style of this project.

---

## ANIMATION 1 — SENSOR LENS IDLE PULSE (2 frames, looping)

```
2-frame looping idle pulse for the AutoTurret sensor lens. Only the sensor lens changes — the rest of the turret body sprite is static.

CAMERA: Isometric 2.5D, same as reference.
ART STYLE: Same as reference.

FRAME 1 — LENS NORMAL:
Sensor lens at normal active brightness: center #FF6020, edge #C02010, 1–2 px glow halo #C02010.

FRAME 2 — LENS PEAK PULSE:
Sensor lens slightly brighter: center #FF8040 (slightly warmer/brighter), edge #E03020 (brighter edge). The glow halo is slightly wider — 3 px. The overall lens circle is 1 px larger in diameter (simulating a slight expansion).

Frame timing: Frame 1 holds 0.6s, Frame 2 holds 0.25s (the pulse is a quick bright moment in a slow beat).
Loop: Yes — continuous while turret is in active/scanning state.
Purpose: This subtle pulse makes the turret feel alive and powered, even when not firing. The rhythmic glow warns the player this is an active threat.
```

---

## ANIMATION 2 — TURRET FIRE (4 frames, plays once per burst)

```
4-frame fire animation for the AutoTurret. Plays when the turret fires a burst at the player.

CAMERA: Isometric 2.5D, same as reference.
ART STYLE: Same as reference.

FRAME 1 — PRE-FIRE:
The turret body in its current facing direction. Sensor lens at peak brightness — a brief "lock-on" flash. Both barrels fully extended.

FRAME 2 — MUZZLE FLASH:
The barrel tips show a bright flash: a small starburst shape (#FFE060 bright yellow-white) at the end of each barrel tip. The sensor lens at peak glow (#FF8040). This is a single frame — extremely brief.

FRAME 3 — RECOIL:
The turret body is displaced 2–3 px backward (toward the back of the facing direction) — a very slight recoil nudge. No barrel distortion (the barrels are rigid). Muzzle flash is gone.

FRAME 4 — RETURN:
The turret body returns to its normal position (no displacement). Sensor lens returns to normal idle brightness. Back to the cycling idle pulse.

Total frames: 4
Frame timing: Frame 1 (0.06s), Frame 2 (0.05s — flash is fast), Frame 3 (0.06s), Frame 4 (0.08s)
Plays once per burst. The turret fires in 2-shot bursts with a 0.3s gap between bursts.
```

---

## Static Sprites Summary

| State | Sprite / Component | Animation |
|---|---|---|
| Pedestal (all states) | `turret_pedestal.png` | None (static) |
| Active turret body | `turret_body.png` | 2-frame lens pulse loop |
| Damaged turret body | `turret_body_damaged.png` | None (lens still pulses — same 2 frame applied) |
| Disabled turret body | `turret_body_disabled.png` | None (lens is off) |
| Destroyed turret body | `turret_body_destroyed.png` | None |
| Fire flash | Frame 2 of fire animation | 4-frame, plays per burst |
