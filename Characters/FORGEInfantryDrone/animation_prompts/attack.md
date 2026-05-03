# ANIMATION PROMPTS — FORGE INFANTRY DRONE — ATTACK (BURST FIRE)

---

## Instructions for All Attack Prompts
- Use the canonical reference image (see `reference_prompt.md`) as the visual source of truth.
- **Only the attack pose and direction change. Body design, arm assignments, sensor eye glow, and all mechanical details are strictly locked.**
- Attack is a 3-round burst fire from the cannon arm. The cannon arm ROTATES to aim — it is the right arm, and it pivots at the shoulder joint to point toward the target direction.
- All 4 legs are planted in a stable attack stance during firing. The drone does not walk and shoot simultaneously.
- Sensor eyes are at FULL brightness (#20D4E0) during attack — maximum alert state.
- Muzzle flash is engine particle at barrel tip — do NOT bake into sprite.
- Recoil: slight backward press of the cannon arm — 3–5° recoil push at peak burst.
- Sprite size: 192×192 px per frame. Isometric 2.5D. 30-degree pitch.

---

## ATTACK — BURST FIRE — FACING DOWN (South, firing toward viewer)

```
Isometric 2.5D burst-fire animation frame of a FORGE Infantry Drone, firing south (toward viewer). Cannon arm aimed at viewer.

Preserve exactly from reference: matte gunmetal grey chassis, flat black panel seams, FORGE logo on right torso panel, reverse-knee legs in stable stance, right arm = cannon arm, left arm = claw arm. Sensor module mount top (engine adds sensor eyes). Do NOT change any visual element or swap arm roles.

Pose: All 4 legs planted in wide stable firing stance — slightly wider than walk stance for recoil stability. Legs: each knee slightly bent, foot pads firmly on ground. RIGHT cannon arm ROTATED to aim south — the shoulder joint has rotated so the barrel points directly at the viewer (south). Barrel tip pointed south (foreshortened barrel visible at tip, circular barrel opening). Cannon arm slightly elevated to horizontal level. LEFT claw arm loosely at side (not engaged). Body facing south, stable. Recoil suggestion: cannon arm 3° backward-press from burst. Body does not flinch — this is a machine absorbing its own recoil mechanically.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
Lighting: Baked isometric top-left directional.
Note: Muzzle flash is engine particle at barrel tip. Do not bake into sprite.
```

---

## ATTACK — BURST FIRE — FACING UP (North, firing north away from viewer)

```
Isometric 2.5D burst-fire frame of a FORGE Infantry Drone, firing north (away from viewer). Cannon arm aimed north.

Preserve exactly from reference: rear chassis view, cannon arm right of sprite (character's right arm), claw arm left of sprite.

Pose: 4 legs planted stable. Cannon arm (right of sprite in rear view) rotated to aim north — arm extending forward away from viewer, barrel pointing north. Claw arm loosely at side. Body stable, no motion.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

## ATTACK — BURST FIRE — FACING LEFT (West)

```
Isometric 2.5D burst-fire frame of a FORGE Infantry Drone, firing left (west). Cannon arm aimed west.

Preserve exactly from reference: left profile chassis. In left-facing view: claw arm is near-side (left arm = near in left profile). Cannon arm is far-side, rotated to aim west. Barrel extends west past the left edge of the body.

Pose: 4 legs planted. Cannon arm (far-side in left profile) rotated to aim west — the arm reaches across or around the body toward the west direction. Barrel pointing left. Claw arm near-side loose. In this left-profile, the cannon arm rotation is particularly dramatic — the arm extends past the near-side of the body to point at the target on the far left.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

## ATTACK — BURST FIRE — FACING RIGHT (East)

```
Isometric 2.5D burst-fire frame of a FORGE Infantry Drone, firing right (east). Cannon arm aimed east.

Preserve exactly from reference: right profile chassis. Cannon arm near-side (right arm = near in right profile). Barrel extends east — pointing right in right profile. Claw arm far-side loose. FORGE logo on right torso panel near-side.

Pose: 4 legs planted. Cannon arm near-right aims east — most natural position for east-facing fire (the cannon arm is already on the right side, so east aim is a natural forward extension). Barrel pointing right, level. FORGE logo visible near-right.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

## ATTACK — BURST FIRE — FACING DIAGONAL DOWN-LEFT (Southwest)

```
Isometric 2.5D burst-fire frame of a FORGE Infantry Drone, firing southwest. Front-left three-quarter view, cannon aimed southwest.

Preserve exactly from reference: front-left chassis, cannon arm (right arm) rotated to aim southwest. Claw arm (left) loose near-left side.

Pose: 4 legs planted. Cannon arm rotated from its right-side position to aim southwest — arm crosses body to aim toward the southwest direction. Barrel pointing down-left at target. Claw arm near-left at rest.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

## ATTACK — BURST FIRE — FACING DIAGONAL DOWN-RIGHT (Southeast)

```
Isometric 2.5D burst-fire frame of a FORGE Infantry Drone, firing southeast. Front-right three-quarter view, cannon aimed southeast.

Preserve exactly from reference: front-right chassis, cannon arm near-right aiming southeast. FORGE logo near-right.

Pose: 4 legs planted. Cannon arm near-right naturally extends southeast — the arm's natural position in front-right view aligns well with southeast fire. Barrel pointing southeast. Claw arm far-left loose.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

## ATTACK — BURST FIRE — FACING DIAGONAL UP-LEFT (Northwest)

```
Isometric 2.5D burst-fire frame of a FORGE Infantry Drone, firing northwest. Back-left three-quarter view, cannon aimed northwest away from viewer.

Preserve exactly from reference: rear-left chassis, cannon arm on character's right (appears on right side of sprite in rear view), aimed northwest.

Pose: 4 legs planted. Cannon arm rotated to aim northwest (away from viewer-left). Barrel pointing northwest. Claw arm near-left loose. Body stable.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

## ATTACK — BURST FIRE — FACING DIAGONAL UP-RIGHT (Northeast)

```
Isometric 2.5D burst-fire frame of a FORGE Infantry Drone, firing northeast. Back-right three-quarter view, cannon aimed northeast away from viewer.

Preserve exactly from reference: rear-right chassis, cannon arm near-right (character's right arm, near side in rear-right view), aimed northeast. FORGE logo partial near-right.

Pose: 4 legs planted. Cannon arm near-right aims northeast — extends away from viewer-right. Barrel northeast. Claw arm far-left. Body stable.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

# ATTACK — EMP-STUNNED (Special State)

## Instructions
4 cardinal directions. Looping held pose (1-frame static). Completely frozen — all joints locked, sensor eyes DARK (#1A1A1A — no glow at all). Body may have a slight lean if caught mid-stride. This is a one-frame held state.

---

## EMP-STUNNED — FACING DOWN (South)

```
Isometric 2.5D EMP-stun held frame of a FORGE Infantry Drone, frozen facing south (toward viewer).

Preserve exactly from reference: all body elements. CRITICAL CHANGE: Sensor module eyes are DARK (#1A1A1A — completely off, no cyan glow). All joints are completely rigid — no natural hang or motion. The drone looks "dead but standing."

Pose: Body frozen in whatever position it was in. Legs may be mid-stride or in a standing position. All joints locked at their current angle — no relaxation or slumping. Cannon arm wherever it was when stunned. Claw arm frozen. Eyes dark. The ONLY difference from the walk/idle is: ALL sensor eyes off, all joints locked/rigid.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
Note: 1-frame static — engine holds this frame for 2–4 seconds.
```

*(Follow the same format for north, west, east EMP-stun variants. Eyes always dark. All joints locked.)*
