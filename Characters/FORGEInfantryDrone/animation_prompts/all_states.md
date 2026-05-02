# ANIMATION PROMPTS — FORGE INFANTRY DRONE — ALL STATES

---

## Instructions for All Drone Prompts
- Use the canonical reference image (see `reference_prompt.md`) as the visual source of truth.
- **Only direction and action state change. Body design, sensor eye color, cannon/claw arm positions, and color palette are locked.**
- Right arm is ALWAYS the cannon arm. Left arm is ALWAYS the claw arm. Never swap these.
- Sensor eyes (#20D4E0 cyan glow) are ON in all frames EXCEPT EMP-stunned and death.
- Sprite size: 192×192 px per frame. Isometric 2.5D. 30-degree pitch.

---

# IDLE — PATROL SCAN

## Instructions
4 cardinal directions. Looping. The drone stands in place while its sensor module slowly rotates (15° scan sweep left and right). One full scan sweep = one loop cycle.

---

## IDLE — FACING DOWN (South)

```
Isometric 2.5D idle patrol scan frame of a FORGE Infantry Drone, facing south (toward viewer). Front-diagonal view.

Preserve exactly from reference: matte gunmetal grey body (#4A4A4A), sensor module with two glowing cyan eyes (#20D4E0), FORGE gear-circuit logo on right torso panel, reverse-knee legs in wide stable stance, right arm = cannon arm (barrel at rest/down angle), left arm = claw arm (open, at side). Do NOT change any visual element.

Pose: Standing still in patrol rest. Weight evenly distributed on both legs. Right cannon arm pointing down-forward at rest angle. Left claw arm loosely open at side. Sensor module: at center position of scan arc (facing viewer). Eyes fully lit (#20D4E0) with faint ambient halo (#10A0A8).

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
Lighting: Baked isometric top-left directional. Cyan eye self-illumination on top of torso surface (subtle).
```

---

## IDLE — FACING UP / LEFT / RIGHT
*(Use the same prompt format as the Down-facing Idle above, adjusting the sensor module facing direction and body rotation to north, west, and east respectively. Cannon arm always on right side of drone body. Claw arm on left. Sensor eyes always glowing.)*

---

# WALK

## Instructions
8 directions. Looping, 6-frame cycle. The reverse-knee legs give a distinctive mechanical forward-bobbing gait. The sensor module remains stable (does not bob with body — it is gyroscopically stabilized).

---

## WALK — FACING DOWN (South)

```
Isometric 2.5D walk animation frame (mid-stride) of a FORGE Infantry Drone moving south (toward viewer).

Preserve exactly from reference: all visual elements locked. Cannon arm right, claw arm left, sensor eyes glowing cyan.

Pose: Mid-stride, right leg extended forward (heel-pad landing), left leg at push-off. Body leans slightly forward (aggressive walking posture). Reverse-knee legs show distinctive forward-lean lower joint extension. Sensor module STABLE — does not tilt with body movement (gyroscopic stabilization). Right cannon arm swings slightly forward in opposition to right leg (mechanical gait rhythm). Left claw arm swings slightly back. Slight ground-level compression visible at foot pad contact.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

## WALK — FACING UP / LEFT / RIGHT / ALL DIAGONALS
*(Follow the Walk — Down format above for all 8 directions. Adjust body orientation, leg extension direction, arm swing opposition. Sensor module remains stable in all directions. Eyes always glowing.)*

---

# RUN (ALERT SPRINT)

## Instructions
8 directions. Looping. Used for Aggressor behavior — faster than walk, more aggressive lean. Same mechanical gait but faster cycle and greater limb extension.

---

## RUN — FACING DOWN (South)

```
Isometric 2.5D sprint animation frame of a FORGE Infantry Drone sprinting south (toward viewer). Aggressive, fast movement.

Preserve exactly from reference: all visual elements locked.

Pose: Greater forward lean than walk (~20°). Right leg fully extended forward (longer stride). Left leg kicked back higher. Both cannon arm and claw arm in more aggressive position — cannon arm raised slightly (ready to fire on arrival at target), claw arm back for momentum. Sensor module still stable. Eyes at FULL brightness (#20D4E0) — alert combat state.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

# ATTACK — BURST FIRE

## Instructions
8 directions. Looping while actively firing. Cannon arm raised to firing angle. The muzzle flash and projectile tracer are engine particle effects — do NOT bake into sprite.

---

## ATTACK — BURST FIRE — FACING DOWN (South)

```
Isometric 2.5D attack animation frame of a FORGE Infantry Drone firing its autocannon south (toward viewer).

Preserve exactly from reference: all visual elements locked. Cannon arm is RIGHT arm only.

Pose: Right cannon arm raised to firing position — barrel pointing directly toward viewer (foreshortened barrel visible at tip). The arm/barrel is elevated to horizontal level (90° from rest angle). Left claw arm tucked back slightly for stability. Both legs planted wide, slight body rock backward from recoil (small recoil lean). Sensor eyes at FULL brightness (#20D4E0) — targeting state.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
Note: No muzzle flash in sprite — engine adds particle effect at barrel tip position.
```

---

## ATTACK — BURST FIRE — ALL 8 DIRECTIONS
*(Follow the same format as Down-facing, adjusting body and cannon arm direction for each of the 8 directions. Sensor eyes always full brightness during attack. Claw arm always tucked back. Legs always planted wide.)*

---

# HURT (HIT REACTION)

## Instructions
4 cardinal directions minimum. Non-looping. Short stagger — 2 frames: impact → partial recovery. One sensor eye flickers on hit (eye goes to dim state for this frame).

---

## HURT — FACING DOWN (South, hit from front)

```
Isometric 2.5D hurt-reaction frame of a FORGE Infantry Drone, hit from the south (front). Front-diagonal view.

Preserve exactly from reference: all body design elements locked.

Pose: Hit from front — body rocks backward. Torso tilts back 15–20°. Reverse-knee legs absorb the shock — slight knee-bend. Cannon arm flung slightly up from impact. Claw arm raised defensively in reflex (automated damage-response protocol). LEFT sensor eye: DIMMED to near-off (#082830) — flickering damage state. Right sensor eye: still bright (#20D4E0). One small spark particle at right torso panel (impact point) — engine FX.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

# DEATH (DESTROYED)

## Instructions
4 cardinal directions. Non-looping. 4-frame sequence: hit → buckle → topple → final rest (held). Sensor eyes go dark on the first frame of the buckle (power loss). Final rest pose is held on screen.

---

## DEATH — FACING DOWN (Topple forward)

```
Isometric 2.5D death animation final rest frame of a FORGE Infantry Drone, destroyed and toppled forward.

Preserve exactly from reference: body design locked.

Final pose: Drone has collapsed forward, face-down (sensor module pressed to ground — sensor eyes now DARK, #1A1A1A — completely off). Both legs buckled and folded under/behind the torso. Cannon arm extended forward past the torso (weapon pointed down into ground). Claw arm folded under body. Body slightly twisted — right side elevated more than left. Small scorch mark on right torso panel (impact damage that destroyed it). No sparks in this final rest frame — machine is fully powered down.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
Note: Held final frame. Completely still. Eyes MUST be dark (##1A1A1A) — this is critical for the death read.
```

---

# EMP STUNNED (Frozen State)

## Instructions
4 cardinal directions. Non-looping — this is a **single held frame** for the duration of EMP stun (2–4s). All joints locked. Eyes dark.

---

## EMP STUNNED — FACING DOWN (South)

```
Isometric 2.5D EMP-stunned frozen frame of a FORGE Infantry Drone, facing south (toward viewer).

Preserve exactly from reference: all body design locked.

Pose: COMPLETELY STILL — all joints locked in whatever motion position the drone was in when the EMP hit. For this reference frame, use the mid-walk pose (right leg forward, left back, slight forward lean). ALL motion is stopped — mid-stride, frozen in place. Sensor eyes: COMPLETELY DARK (#1A1A1A — fully off). Cannon arm in whatever position it was (use mid-swing from walk). Claw arm mid-swing. The frozen quality must be unmistakable — this is a machine that has had its power cut.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
Note: This is a held frame — no animation at all. Eyes must be dark. Engine plays a brief EMP static particle effect on this frame separately.
```
