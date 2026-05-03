# ANIMATION PROMPTS — FORGE INFANTRY DRONE — HURT

---

## Instructions for All Hurt Prompts
- Use the canonical reference image (see `reference_prompt.md`) as the visual source of truth.
- **Only the hit-reaction pose changes. Body design, arm roles, and all mechanical details are strictly locked.**
- Hurt: 2 frames (impact → stabilization). Non-looping.
- FORGE Drones do NOT express pain — they have no nervous system. Their hurt is a mechanical stagger from projectile force.
- Visual hurt cues: Body rocks from impact force. One sensor eye FLICKERS (dims briefly — engine handles sensor module flicker, not the body layer). Cannon arm may jolt from the force. Sparks may emit from the impact point (engine particle — do not bake).
- The stagger is shorter and less dramatic than human characters — approximately 8–10° body rock (less than SENTINEL's 12°, much less than Reclaimer's 25°).
- If at 50% HP or below, the drone uses its "damaged variant" frame set — art team provides a separate damaged body sprite set with impact dents and scorch marks on the right torso panel.
- Sprite size: 192×192 px per frame. Isometric 2.5D. 30-degree pitch.

---

## HURT — FACING DOWN (South, hit from front)

```
Isometric 2.5D hurt-reaction frame of a FORGE Infantry Drone, hit from the south (front impact). Front-diagonal view.

Preserve exactly from reference: matte gunmetal grey chassis, flat black panel seams, FORGE logo on right torso panel, reverse-knee legs, right arm = cannon arm, left arm = claw arm. Do NOT change any visual element or swap arm roles.

Pose: Impact from front — mechanical body rock backward. Body tilts back ~8–10° from projectile force impact. Legs absorb — knees bend slightly more, feet stay planted (the drone's wide foot pad grip prevents stumbling). Cannon arm jolts back and slightly up from the impact wave. Claw arm jerks outward slightly (mechanical force dispersion). Head module (sensor mount point) tilts very slightly back — but remains more stable than a human head (gyroscopic). This is a machine absorbing a physics impact, not a creature feeling pain.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
Lighting: Baked isometric top-left directional.
Note: Engine adds spark particle at impact location and sensor module flicker (separate sensor sprite layer dims one eye briefly).
```

---

## HURT — FACING UP (North, hit from rear)

```
Isometric 2.5D hurt-reaction frame of a FORGE Infantry Drone, hit from behind (north hit). Rear view.

Preserve exactly from reference: rear chassis, cannon arm right of sprite, claw arm left of sprite.

Pose: Hit from rear — mechanical body pitch forward ~8°. Legs stay planted. Cannon arm (right of sprite) jolts forward from impact. Claw arm (left of sprite) jerks forward. Body pitches forward but remains upright — mechanical stability.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

## HURT — FACING LEFT (West, hit from left)

```
Isometric 2.5D hurt-reaction frame of a FORGE Infantry Drone, hit from the left. Left-profile view.

Preserve exactly from reference: left profile, claw arm near-side, cannon arm far-side.

Pose: Hit from left — body rocks right ~8°. Claw arm (near-side) jolts right. Cannon arm (far-side) jolts right. Legs planted. Body rock to the right from left-side impact.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

## HURT — FACING RIGHT (East, hit from right)

```
Isometric 2.5D hurt-reaction frame of a FORGE Infantry Drone, hit from the right. Right-profile view.

Preserve exactly from reference: right profile, cannon arm near-side, claw arm far-side. FORGE logo near-right.

Pose: Hit from right — body rocks left ~8°. Cannon arm (near-side) jolts left. Claw arm (far-side) jolts left. Legs planted. If at 50% HP: impact dent visible on near-right torso panel (right panel = FORGE logo panel = the near panel in right profile).

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

## HURT — FACING DIAGONAL DOWN-LEFT (Southwest)

```
Isometric 2.5D hurt-reaction frame of a FORGE Infantry Drone, hit from southwest. Front-left three-quarter view.

Preserve exactly from reference: front-left chassis, claw arm near-left, cannon arm far-right.

Pose: Impact from front-left — mechanical rock northeast-backward ~8°. Both arms jolt from impact. Legs planted.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

## HURT — FACING DIAGONAL DOWN-RIGHT (Southeast)

```
Isometric 2.5D hurt-reaction frame of a FORGE Infantry Drone, hit from southeast. Front-right three-quarter view.

Preserve exactly from reference: front-right chassis, cannon arm near-right, FORGE logo near-right, claw arm far-left.

Pose: Impact from front-right — mechanical rock northwest-backward ~8°. Cannon arm jolts. Legs planted. If at 50% HP: scorch mark on right torso panel near impact zone (right torso panel near-right).

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

## HURT — FACING DIAGONAL UP-LEFT (Northwest)

```
Isometric 2.5D hurt-reaction frame of a FORGE Infantry Drone, hit from northwest rear. Back-left three-quarter view.

Preserve exactly from reference: rear-left chassis, claw arm near-left, cannon arm far-right.

Pose: Hit from rear-left — body pitches forward-right ~8°. Mechanical forward-pitch response. Arms jolt forward. Legs planted.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

## HURT — FACING DIAGONAL UP-RIGHT (Northeast)

```
Isometric 2.5D hurt-reaction frame of a FORGE Infantry Drone, hit from northeast rear. Back-right three-quarter view.

Preserve exactly from reference: rear-right chassis, cannon arm near-right, claw arm far-left.

Pose: Hit from rear-right — body pitches forward-left ~8°. Cannon arm (near-right) jolts. Claw arm (far-left) jolts. Legs planted.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```
