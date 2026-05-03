# ANIMATION PROMPTS — FORGE INFANTRY DRONE — IDLE (PATROL SCAN)

---

## Instructions for All Idle Prompts
- Use the canonical reference image (see `reference_prompt.md`) as the visual source of truth.
- **Only the direction changes. Body design, sensor eye color, cannon/claw arm positions, and all mechanical details are strictly locked.**
- Right arm is ALWAYS the cannon arm. Left arm is ALWAYS the claw arm. Never swap.
- Sensor eyes (#20D4E0 cyan glow) are ON in all idle frames.
- Idle is a slow patrol-scan loop: the sensor module rotates 15° left, then back to center, then 15° right, then back — one full sweep = one loop. Body is completely still during this scan. Only the sensor module rotates.
- Note: The sensor module rotation is handled by the engine as a separate sprite layer. The body layer (what these prompts describe) is STATIC during idle — completely still.
- Sprite size: 192×192 px per frame. Isometric 2.5D. 30-degree pitch.

---

## IDLE — FACING DOWN (South, toward viewer)

```
Isometric 2.5D idle patrol scan frame of a FORGE Infantry Drone, facing south (toward the viewer). Front-diagonal view. BODY LAYER ONLY — sensor module is a separate rotating sprite handled by engine.

Preserve exactly from reference: matte gunmetal grey body chassis (#4A4A4A), flat black panel seams (#1A1A1A), FORGE gear-circuit logo on right torso panel (dark charcoal, slightly raised), reverse-knee digitigrade legs in stable wide stance — thick upper joint, thinner lower strut, wide flat foot pad with grip teeth, chrome-grey joint pivots (#8A8A8A). RIGHT arm: integrated autocannon barrel (fixed to limb, barrel at rest angle pointing slightly down-forward). LEFT arm: three-fingered manipulator claw (open, loosely at side). Sensor module mount point on top of torso (no sensor cluster visible in body layer — engine overlays separately). Do NOT change any visual element or swap arm roles.

Pose: Completely still. Weight evenly distributed on both reverse-knee legs. Right cannon arm pointing down-forward at rest angle (natural hang). Left claw arm open at side. Body upright. No motion — this frame is the static body reference for the idle state. Front of body facing south — FORGE logo on right torso panel visible from this front-left angle.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline, readable at 64×64 px display size.
Lighting: Baked isometric top-left directional. No self-illumination on the body layer (sensor eye glow is on the sensor module sprite — separate layer).
```

---

## IDLE — FACING UP (North, away from viewer)

```
Isometric 2.5D idle patrol scan frame of a FORGE Infantry Drone, facing north (away from viewer). Rear-diagonal view. Body layer only.

Preserve exactly from reference: rear of chassis body (matte gunmetal grey, panel seams on rear panels visible), FORGE logo partially visible on far torso panel from rear angle, reverse-knee legs in stable stance — leg joints distinctive from rear (reverse-knee visible from both sides). Right cannon arm visible on right side of sprite (character's right = weapon arm), barrel pointing down and away from viewer. Left claw arm on left side of sprite, open fingers loosely at side. Sensor module mount on top of chassis rear (no sensor cluster — engine overlay).

Pose: Completely still, body facing north. Rear of chassis to viewer. Cannon arm (right side of sprite in rear-facing view — character's right arm) at rest. Claw arm (left side of sprite) at rest.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
Lighting: Baked isometric top-right directional (rear-facing bake).
```

---

## IDLE — FACING LEFT (West)

```
Isometric 2.5D idle patrol scan frame of a FORGE Infantry Drone, facing left (west). Left-profile isometric view. Body layer only.

Preserve exactly from reference: left side of chassis in profile. IMPORTANT: In left-facing view, the LEFT arm (claw arm) is the near-side arm (facing viewer). Right cannon arm is the far side. Reverse-knee legs clearly visible in profile — the distinctive digitigrade leg geometry is most readable in profile. Sensor module mount on top, slightly front-left (facing direction). Leg joints (chrome-grey pivot) prominent in profile.

Pose: Still. Claw arm near-side (left arm = claw), open fingers loosely at side in profile. Cannon arm far side — barrel partially visible as a shape at far edge of chassis. Reverse-knee legs in stable stance, profile view showing leg geometry clearly.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

## IDLE — FACING RIGHT (East)

```
Isometric 2.5D idle patrol scan frame of a FORGE Infantry Drone, facing right (east). Right-profile isometric view. Body layer only.

Preserve exactly from reference: right side of chassis in profile. IMPORTANT: In right-facing view, the RIGHT arm (cannon arm) is the near-side arm (facing viewer). Cannon barrel is the dominant near-side feature. Left claw arm is far side — minimally visible. Reverse-knee legs in profile — same distinctive geometry. FORGE logo on right torso panel visible in this right-facing profile (the logo is on the right torso panel, which is now the near side).

Pose: Still. Cannon arm near-side — barrel at rest angle, pointing slightly forward and down. Claw arm far side — barely visible. Legs in stable stance profile.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

## IDLE — FACING DIAGONAL DOWN-LEFT (Southwest)

```
Isometric 2.5D idle patrol scan frame of a FORGE Infantry Drone, facing southwest. Front-left three-quarter view. Body layer only.

Preserve exactly from reference: front-left view of chassis. Left arm (claw) somewhat near-left (claw arm visible on the near-left side). Right arm (cannon) somewhat far-right. FORGE logo on right torso panel — partially visible at front-right edge of chassis in this view. Sensor module mount top front. Both legs visible in a three-quarter stance.

Pose: Still. Claw arm near-left at rest, open fingers. Cannon arm far-right at rest. Legs stable. Chassis body showing its front-left face.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

## IDLE — FACING DIAGONAL DOWN-RIGHT (Southeast)

```
Isometric 2.5D idle patrol scan frame of a FORGE Infantry Drone, facing southeast. Front-right three-quarter view. Body layer only.

Preserve exactly from reference: front-right view of chassis. Right arm (cannon) near-right — cannon barrel the dominant near-side arm feature. Left arm (claw) far-left. FORGE logo on right torso panel near-right (most visible in this angle). Sensor module mount top front-right. Both legs in three-quarter stance.

Pose: Still. Cannon arm near-right at rest, barrel down-forward. Claw arm far-left at rest. Legs stable. FORGE logo prominent near-right.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

## IDLE — FACING DIAGONAL UP-LEFT (Northwest)

```
Isometric 2.5D idle patrol scan frame of a FORGE Infantry Drone, facing northwest. Back-left three-quarter view. Body layer only.

Preserve exactly from reference: rear-left chassis view. Right arm (cannon) — in rear-left view, the character's right arm appears on the RIGHT SIDE of the sprite (since we're looking at the back-left). Cannon arm near-left from rear? CLARIFICATION: Character faces northwest. Character's right arm (cannon) is on character's right side. From a rear-left view (viewer behind-left of character), character's right arm (cannon) is on the far-right side of the sprite. Character's left arm (claw) is the near-left arm. Reverse-knee legs visible from rear-left. Sensor module mount rear.

Pose: Still. Rear-left of chassis. Claw arm near-left at rest. Cannon arm far-right. Legs in stable rear stance.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

## IDLE — FACING DIAGONAL UP-RIGHT (Northeast)

```
Isometric 2.5D idle patrol scan frame of a FORGE Infantry Drone, facing northeast. Back-right three-quarter view. Body layer only.

Preserve exactly from reference: rear-right chassis view. Character faces northeast — viewer sees from behind-right. Character's right arm (cannon) is near-right side in this view. Character's left arm (claw) is far-left. Reverse-knee legs from rear-right. FORGE logo on right torso near-right partially visible from rear-right angle.

Pose: Still. Cannon arm near-right at rest, barrel slightly visible in rear-right profile. Claw arm far-left. Legs stable. FORGE logo partial visibility near-right.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```
