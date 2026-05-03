# ANIMATION PROMPTS — FORGE INFANTRY DRONE — WALK

---

## Instructions for All Walk Prompts
- Use the canonical reference image (see `reference_prompt.md`) as the visual source of truth.
- **Only direction and leg positions change. Body, arm assignments, sensor eye glow, and all mechanical details are strictly locked.**
- Walk cycle: 6-frame looping. The reverse-knee (digitigrade) leg geometry creates a distinctive mechanical forward-bobbing gait — this is the drone's signature movement.
- Right arm = cannon arm (ALWAYS). Left arm = claw arm (ALWAYS). Arm positions change slightly with gait rhythm but arm roles never swap.
- Sensor module is STABLE during walk — gyroscopically stabilized, it does NOT bob with the body (engine handles module rotation separately; body layer shows the mount point only).
- Sensor eyes glow (#20D4E0) is part of the sensor module layer — not in body layer prompts.
- Body has a slight forward lean during walk (~5°) — less than human characters.
- Sprite size: 192×192 px per frame. Isometric 2.5D. 30-degree pitch.

---

## WALK — FACING DOWN (South)

```
Isometric 2.5D walk animation frame (mid-stride) of a FORGE Infantry Drone, walking south (toward the viewer). Front-diagonal view.

Preserve exactly from reference: matte gunmetal grey chassis, flat black panel seams, FORGE gear-circuit logo on right torso panel, reverse-knee digitigrade legs, chrome-grey joint pivots, right arm = cannon barrel (fixed), left arm = three-fingered claw. Sensor module mount top (no sensor — engine layer). Do NOT change any visual element or swap arm roles.

Pose: Mid-stride south. Right leg extended forward — the reverse-knee geometry shows: upper joint extends forward-down, lower strut angles back down to a planted foot pad (heel-pad landing on right foot). Left leg at push-off — upper joint angling back, lower strut pushing against ground at toe-pad. Body slight forward lean (~5°). Right cannon arm swings slightly forward in opposition to the right leg (mechanical gait rhythm). Left claw arm swings slightly back. Sensor module mount STABLE — does not tilt with body (key feature). Ground pad contact visible on forward foot.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline, readable at small display size.
Lighting: Baked isometric top-left directional.
```

---

## WALK — FACING UP (North)

```
Isometric 2.5D walk animation frame (mid-stride) of a FORGE Infantry Drone, walking north (away from viewer). Rear-diagonal view.

Preserve exactly from reference: rear of chassis, rear leg geometry visible (reverse-knee joints distinctive from rear), cannon arm on right side of sprite (character's right arm), claw arm on left side of sprite.

Pose: Mid-stride north. Left leg forward (away from viewer). Right leg at push-off. Reverse-knee geometry visible from rear — distinctive lower strut angle as it pushes off. Cannon arm (right of sprite) swings slightly forward. Claw arm (left of sprite) swings slightly back. Body slight forward lean. Sensor module mount stable.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

## WALK — FACING LEFT (West)

```
Isometric 2.5D walk animation frame (mid-stride) of a FORGE Infantry Drone, walking left (west). Left-profile isometric view.

Preserve exactly from reference: left profile of chassis. In left-facing view: LEFT arm (claw) is near-side. RIGHT arm (cannon) is far-side. Reverse-knee legs most readable in profile — this is the clearest view of the leg geometry. Sensor module mount top-front in this profile.

Pose: Mid-stride west. Right leg (far side in left profile) extended forward in stride. Claw arm (near-side) swings slightly forward. Cannon arm (far-side) swings slightly back — barrel partially visible at far edge. Reverse-knee joint geometry prominent in left profile. Sensor module mount stable.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

## WALK — FACING RIGHT (East)

```
Isometric 2.5D walk animation frame (mid-stride) of a FORGE Infantry Drone, walking right (east). Right-profile isometric view.

Preserve exactly from reference: right profile of chassis. In right-facing view: RIGHT arm (cannon) is near-side — barrel is the dominant near-side arm feature. LEFT arm (claw) is far-side. Reverse-knee leg geometry visible in profile. FORGE logo on right torso panel visible near-side.

Pose: Mid-stride east. Left leg extended forward. Cannon arm (near-side) swings slightly forward — barrel most visible in this angle. Claw arm (far-side) swings back. Reverse-knee geometry in profile. Sensor module stable.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

## WALK — FACING DIAGONAL DOWN-LEFT (Southwest)

```
Isometric 2.5D walk animation frame (mid-stride) of a FORGE Infantry Drone, walking southwest. Front-left three-quarter view.

Preserve exactly from reference: front-left chassis view. Claw arm near-left. Cannon arm far-right. Both legs visible. Sensor mount stable.

Pose: Mid-stride southwest. Right leg forward at stride. Claw arm (near-left) swings slightly forward. Cannon arm (far-right) swings back. Both legs showing reverse-knee geometry. Slight forward lean. FORGE logo partially visible on far-right torso.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

## WALK — FACING DIAGONAL DOWN-RIGHT (Southeast)

```
Isometric 2.5D walk animation frame (mid-stride) of a FORGE Infantry Drone, walking southeast. Front-right three-quarter view.

Preserve exactly from reference: front-right chassis view. Cannon arm near-right — barrel most visible. Claw arm far-left. FORGE logo near-right torso. Sensor mount stable.

Pose: Mid-stride southeast. Left leg forward. Cannon arm (near-right) swings forward — barrel the dominant arm feature. Claw arm (far-left) back. FORGE logo near-right. Sensor mount stable.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

## WALK — FACING DIAGONAL UP-LEFT (Northwest)

```
Isometric 2.5D walk animation frame (mid-stride) of a FORGE Infantry Drone, walking northwest. Back-left three-quarter view.

Preserve exactly from reference: rear-left chassis. Claw arm near-left (character's left, near in rear-left view). Cannon arm far-right. Reverse-knee legs from rear-left. Sensor mount stable rear.

Pose: Mid-stride northwest. Left leg forward (away from viewer-left). Claw arm near-left swings forward. Cannon arm far-right back. Reverse-knee geometry visible from rear-left. Sensor mount stable.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

## WALK — FACING DIAGONAL UP-RIGHT (Northeast)

```
Isometric 2.5D walk animation frame (mid-stride) of a FORGE Infantry Drone, walking northeast. Back-right three-quarter view.

Preserve exactly from reference: rear-right chassis. Cannon arm near-right (character's right is near side in rear-right view). Claw arm far-left. FORGE logo on right torso near-right partially visible. Sensor mount stable.

Pose: Mid-stride northeast. Right leg forward (away from viewer-right). Cannon arm near-right swings forward. Claw arm far-left back. FORGE logo partial visibility. Sensor mount stable.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```
