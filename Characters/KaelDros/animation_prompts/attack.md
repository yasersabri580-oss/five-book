# ANIMATION PROMPTS — KAEL DROS — ATTACK

---

## Instructions for All Attack Prompts
- Use the canonical reference image (see `reference_prompt.md`) as the visual source of truth.
- **Only the attack pose and direction change. Costume, proportions, and visor design are strictly locked.**
- Attack animations are short, punchy, and non-looping (except rifle fire which loops while trigger held).
- Sprite size: 192×192 px per frame. Isometric 2.5D. 30-degree pitch.

---

# ATTACK — RIFLE FIRE

## Instructions
Rifle fire is a looping animation while the trigger is held. Shows raised rifle, aim pose, and a per-frame recoil jolt.
Muzzle flash renders as a separate engine effect — do NOT bake a muzzle flash into the sprite.

---

## RIFLE FIRE — FACING DOWN (South)

```
Isometric 2.5D rifle-fire animation frame of Sergeant Kael Dros shooting south (toward viewer). Raised-rifle aim pose.

Preserve exactly from reference: cracked amber visor helmet, gunmetal mechanical left arm, canvas chest rig, dark cargo trousers. Do NOT change costume.

Pose: Both hands on rifle, raised to shoulder height. Right hand on grip (trigger finger extended over guard in aim). Mechanical left hand supports barrel from underneath — fingers wrapped around forend. Rifle barrel points directly at viewer (foreshortened barrel tip visible). Slight recoil tilt — rifle muzzle 5° above eye line. Feet planted, slight crouch in stance. Shoulders squared toward viewer.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
Lighting: Baked isometric top-left directional.
Note: Muzzle flash is NOT included in this sprite — engine applies particle effect at barrel tip.
```

---

## RIFLE FIRE — FACING UP (North)

```
Isometric 2.5D rifle-fire frame of Sergeant Kael Dros shooting north (away from viewer). Rear view of aim pose.

Preserve exactly from reference: rear of helmet, radio pack, mechanical arm on right of sprite (character's left), human arm on left of sprite.

Pose: Rifle raised to shoulder, arms extended forward (away from viewer). Barrel points north. Mechanical arm (right side of sprite) supporting barrel from left (under-forend). Right arm (trigger hand) at right side of sprite but partially obscured behind body. Recoil suggestion — slight rearward lean of upper body.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

## RIFLE FIRE — FACING LEFT (West)

```
Isometric 2.5D rifle-fire frame of Sergeant Kael Dros shooting left. Left-profile aim view.

Preserve exactly from reference: Left visor profile, mechanical arm near side (under-forend grip), rifle barrel extending left and slightly elevated.

Pose: Side-on rifle raise. Both arms extended left, rifle at shoulder. Mechanical left arm supporting forend. Right (human) trigger arm slightly behind. Barrel points left, slight upward angle at recoil peak. Head slightly tilted into rifle stock.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

## RIFLE FIRE — FACING RIGHT (East)

```
Isometric 2.5D rifle-fire frame of Sergeant Kael Dros shooting right. Right-profile aim view.

Preserve exactly from reference: Right visor (crack prominent in profile), human right arm near side on trigger, mechanical arm far side supporting forend, wrist glow faint.

Pose: Side-on rifle raise pointing right. Right (human) arm near-side on trigger. Mechanical arm far-side under forend, glow faint. Barrel extending right.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

## RIFLE FIRE — DIAGONAL DOWN-LEFT (Southwest)

```
Isometric 2.5D rifle-fire frame of Sergeant Kael Dros shooting southwest. Front-left three-quarter aim.

Preserve exactly from reference: Front visor visible, mechanical arm near-left supporting forend, chest rig front-left face.

Pose: Raised rifle aimed southwest. Both hands on rifle. Barrel pointed down-left at target. Slight crouch, squared stance.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

## RIFLE FIRE — DIAGONAL DOWN-RIGHT (Southeast)

```
Isometric 2.5D rifle-fire frame of Sergeant Kael Dros shooting southeast. Front-right three-quarter aim.

Preserve exactly from reference: Front-right visor, human arm near-right on trigger, mechanical arm far side.

Pose: Raised rifle aimed southeast. Human arm near-right dominant. Mechanical arm under forend on far side. Slight stance crouch.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

## RIFLE FIRE — DIAGONAL UP-LEFT (Northwest)

```
Isometric 2.5D rifle-fire frame of Sergeant Kael Dros shooting northwest. Back-left three-quarter aim.

Preserve exactly from reference: Rear-left helmet, mechanical arm on near-right side of sprite under forend, rifle barrel pointing up-left.

Pose: Rifle raised toward northwest. Arms extended away from viewer-left. Mechanical arm near-right side visible supporting forend.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

## RIFLE FIRE — DIAGONAL UP-RIGHT (Northeast)

```
Isometric 2.5D rifle-fire frame of Sergeant Kael Dros shooting northeast. Back-right three-quarter aim.

Preserve exactly from reference: Rear-right helmet, human arm near-right side on trigger, mechanical arm far side glow faint.

Pose: Rifle raised northeast. Human arm near-side on trigger. Mechanical arm far side supporting forend.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

# ATTACK — MELEE (Mechanical Arm Strike)

## Instructions
4 cardinal directions only. Non-looping. 3-frame punch: wind-up → strike → recovery.
The mechanical arm is the striking limb — left arm forward hook. Stun/impact focus, not a killing blow.

---

## MELEE — FACING DOWN (South)

```
Isometric 2.5D melee attack frame (strike frame — peak of punch) of Sergeant Kael Dros. Mechanical left arm hook strike, facing south.

Preserve exactly from reference: helmet, chest rig, mechanical arm design. Do NOT change costume.

Pose: Mechanical left arm fully extended forward toward viewer in a short hook punch. Fist closed (metal fingers curled). Wrist interface screen faces up — blue glow visible on knuckles from the screen below. Right human arm holds rifle tucked against body (not used in strike). Torso rotated 30° left to drive the punch. Feet planted, slight forward step with left foot to sell impact.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

## MELEE — FACING LEFT (West)

```
Isometric 2.5D melee strike frame of Sergeant Kael Dros punching left.

Preserve exactly from reference: left profile, mechanical arm near side, helmet left profile.

Pose: Mechanical arm fully extended left in hook. Fist closed. Torso rotation drives the punch. Right arm holds rifle tucked to body. Left foot slightly forward.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

## MELEE — FACING RIGHT (East)

```
Isometric 2.5D melee strike frame of Sergeant Kael Dros punching right.

Preserve exactly from reference: right profile, visor crack visible, mechanical arm extended across body to reach right side.

Pose: Mechanical arm extended right — cross-body reach. This is a wide hooking motion. Torso twists right to drive reach. Right (human) arm tucked with rifle.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

## MELEE — FACING UP (North)

```
Isometric 2.5D melee strike frame of Sergeant Kael Dros punching north (away from viewer).

Preserve exactly from reference: rear helmet view, mechanical arm extending forward away from viewer.

Pose: Mechanical arm extended northward, fist forward (away from viewer). Body lean forward. Right arm + rifle tucked.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

# ATTACK — GRENADE THROW

## Instructions
4 cardinal directions. Non-looping. 4-frame sequence: grip grenade → cook (hold) → overhead throw arc → follow-through.
Show the grenade in hand during cook pose and release frame. Grenade is a separate particle/physics object in engine.

---

## GRENADE THROW — FACING DOWN (South)

```
Isometric 2.5D grenade throw animation frame (release frame — peak of throw) of Sergeant Kael Dros, facing south.

Preserve exactly from reference: helmet, chest rig, mechanical arm, dark trousers. Do NOT change costume.

Pose: Right human arm fully extended overhead at 11 o'clock position, hand open — grenade just released (small cylindrical frag grenade visible at fingertip, launching upward-forward). Mechanical left arm extends forward slightly for balance. Torso slight backward lean (counterbalance to throw). Right foot slightly back (planted for throw power). Slight upward tilt of head/visor tracking the grenade arc.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

## GRENADE THROW — FACING LEFT (West)

```
Isometric 2.5D grenade throw release frame of Sergeant Kael Dros throwing west (left).

Preserve exactly from reference: helmet left-profile, mechanical arm on near side (balance extension), human right arm extended overhead-left.

Pose: Right arm arcing overhead, throwing toward left. Mechanical arm slightly extended right for counterbalance. Left foot forward (step into throw).

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

## GRENADE THROW — FACING RIGHT (East)

```
Isometric 2.5D grenade throw release frame of Sergeant Kael Dros throwing east (right).

Preserve exactly from reference: right-profile visor (crack visible), human arm overhead throwing right.

Pose: Right arm arcing right-overhead. Mechanical arm (far side) extended slightly for balance. Right foot planted forward.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

## GRENADE THROW — FACING UP (North)

```
Isometric 2.5D grenade throw release frame of Sergeant Kael Dros throwing north (away from viewer).

Preserve exactly from reference: rear helmet, radio pack, right arm overhead seen from behind.

Pose: Right arm overhead, throw toward north (away from viewer). Mechanical arm barely visible at side. Body lean forward into throw.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

# ATTACK — EMP TOSS

## Instructions
4 cardinal directions. Non-looping. 2-frame quick underhand toss with mechanical left arm.
Blue glow emanates from hand during toss.

---

## EMP TOSS — FACING DOWN (South)

```
Isometric 2.5D EMP toss frame of Sergeant Kael Dros, facing south. Mechanical arm underhand toss of cylindrical EMP device.

Preserve exactly from reference: helmet, chest rig, mechanical arm design.

Pose: Mechanical left arm swung forward in underhand arc, hand open releasing EMP cylinder. Blue glow (#4AB0D0) emanates from wrist interface and palm — brighter than normal idle glow. Rifle held in right hand tucked to body. Body slightly forward-leaned into toss.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
Note: EMP cylinder is a separate particle effect in engine — show hand open at release but cylinder may be minimally rendered as a small blur leaving the hand.
```

---

## EMP TOSS — FACING LEFT / RIGHT / UP
*(Follow the same format as the Down-facing prompt above, adjusting body orientation and arm direction to face west, east, and north respectively. Mechanical arm remains dominant. Blue glow from wrist interface is always visible. Rifle tucked in right hand. Underhand arc motion.)*
