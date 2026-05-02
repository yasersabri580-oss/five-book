# ANIMATION PROMPTS — EXPLOSIVE BARREL

---

## Animation Status

**Minimal animation — 1 optional enhancement only.**

The intact-to-damaged transition is a sprite swap, not an animation. The explosion on destruction is handled by the VFX system.

---

## Optional Enhancement — Danger Flicker (Low Priority)

When the barrel's HP drops below 15 (leaking/damaged state), a subtle flicker signals imminent explosion. This is a 2-frame animation loop.

```
2-frame looping flicker animation for a damaged ExplosiveBarrel. Based on the canonical reference image for the Damaged Barrel state.

CAMERA: Isometric 2.5D, same as reference.
ART STYLE: Same as reference sprite — crisp 2px outline, baked lighting, same red/yellow color palette.

FRAME 1 — NORMAL DAMAGED STATE:
The barrel as it appears in the Damaged sprite. No change from reference.

FRAME 2 — HEAT GLOW:
The barrel is very slightly brightened overall. The bung hole drip glows faintly — the dark oily drip acquires a subtle orange-amber edge glow (#C87020 very faint). The yellow hazard stripes are 10% brighter (#F0C800). The overall saturation of the barrel red is very slightly increased (#D02020). This is a subtle shimmer — NOT a dramatic flash. The effect should feel like heat building up inside the barrel.

Frame timing: Frame 1 holds for 0.4s, Frame 2 holds for 0.15s. Loop continuously.
Total frames: 2
Loop: Yes — continuous loop while barrel is in damaged/leaking state.
Stop condition: Loop stops when barrel HP reaches 0 (explosion triggered).
```

---

## Static Sprite Summary

| State | Sprite | Animation |
|---|---|---|
| Intact | `barrel_intact.png` | None |
| Damaged / Leaking | `barrel_damaged.png` + optional 2-frame flicker | Optional 2-frame loop |
| Ground debris (post-explosion) | `barrel_fragments_decal.png` | None (placed by VFX system) |
| Double variant | `barrel_double.png` | None |
