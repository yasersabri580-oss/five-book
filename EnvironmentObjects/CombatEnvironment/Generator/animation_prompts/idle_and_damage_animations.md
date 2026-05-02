# ANIMATION PROMPTS — GENERATOR

---

## Animation Status

**Animation required: exhaust heat shimmer (operational, 4 frames looping) and amber light flicker (damaged state, 2 frames looping).**
All other states are static sprites.

---

## ANIMATION 1 — EXHAUST HEAT SHIMMER (Operational, 4 frames)

```
4-frame looping idle animation for the Generator exhaust vents. Only the area directly above the exhaust vents changes — the rest of the generator body is a static background sprite.

Implementation note: The generator body is a static SpriteRenderer. The heat shimmer animation is a SECOND child SpriteRenderer positioned directly above the exhaust vent slots. Only this small child sprite animates — the body sprite does not change.

CAMERA: Isometric 2.5D, same as reference.
ART STYLE: Same as reference. Subtle effect — the shimmer should suggest heat rising from the vents, not be a dramatic VFX element.

The shimmer sprite: a small (roughly 0.4 tile wide × 0.3 tile tall) near-transparent overlay positioned directly above the three exhaust vent slots on the generator top face. The shimmer is a very faint wavy distortion effect — represented as a series of semi-transparent lighter bands in slightly irregular wavy shapes.

FRAME 1 — SHIMMER LOW:
Three very faint near-transparent wavy bands (#5A6050 at 20% opacity, approximately) rising from the vent positions. The waves are at their lowest point — barely above the vents.

FRAME 2 — SHIMMER RISING:
The three bands have risen 2–3 px from the vents. Slightly more visible than Frame 1. The wave shapes are different — slightly different irregular curves.

FRAME 3 — SHIMMER MID:
Bands at mid-height above the vents. Slightly more spread horizontally. The lowest edge of each band is fading (lower opacity at bottom of the shimmer band, higher at the top). New bands are beginning at vent level.

FRAME 4 — SHIMMER HIGH / FADE:
Previous bands are near the top of the shimmer zone, very faint. New bands are visible at low height from the vents. The cycle resets to Frame 1.

Total frames: 4
Frame timing: 0.18s per frame (smooth rolling shimmer)
Loop: Yes — continuous while generator is operational.
```

---

## ANIMATION 2 — AMBER LIGHT FLICKER (Damaged State, 2 frames)

```
2-frame looping flicker for the amber running light strip on the generator control section. Only the amber light strip child sprite changes.

FRAME 1 — LIGHT ON:
Amber strip at normal damaged brightness: #C8A020 with soft glow halo. The strip is at 80% normal brightness (slightly dimmer than operational state — the light is failing).

FRAME 2 — LIGHT OFF:
Amber strip is dark: #1A1410 (near-black, barely perceptible). No glow.

Frame timing: Frame 1 holds 0.2s, Frame 2 holds 0.1s. Irregular: every 3rd cycle, Frame 2 extends to 0.4s (a longer outage — power surging).
Loop: Yes — continuous in damaged state.
Purpose: The flickering light communicates that the generator is damaged and failing. Combined with engine-spawned spark VFX at the cable junction, this makes the damaged generator feel kinetically alive.
```

---

## Static Sprites Summary

| State | Sprite | Animation |
|---|---|---|
| Operational | `generator_body.png` | None (body static) |
| Exhaust shimmer overlay | `generator_exhaust_shimmer.png` | 4-frame shimmer loop (child layer) |
| Amber light strip | `generator_amber_light.png` | None — or 2-frame flicker in damaged state |
| Damaged body | `generator_damaged.png` | None (body; amber light child does flicker) |
| Destroyed / Wreck | `generator_destroyed.png` | None |
