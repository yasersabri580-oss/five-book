# ANIMATION PROMPTS — KAEL DROS — JUMP

---

## Instructions for Jump Prompts
- Use the canonical reference image (see `reference_prompt.md`) as the visual source of truth.
- **Only the airborne pose and direction change. Costume, proportions, and visor are locked.**
- Jump used for: vault over obstacles, and tank entry (pull-up climb). These are separate sub-animations.
- Sprite size: 192×192 px per frame. Isometric 2.5D. 30-degree pitch.

---

# VAULT OVER OBSTACLE

## Instructions
4 cardinal directions. 3-frame sequence: approach push → airborne mid-vault → land.
One-handed push with the human right arm over a low wall or crate (≤1 tile high).

---

## VAULT — FACING DOWN (South)

```
Isometric 2.5D vault animation frame (airborne peak — mid-vault) of Sergeant Kael Dros, vaulting over a low obstacle while moving south.

Preserve exactly from reference: cracked amber visor helmet, gunmetal mechanical left arm, canvas chest rig, cargo trousers, boots. Do NOT change any costume element.

Pose: Right hand placed on top edge of a 0.5-tile high surface (crate or wall edge — shown as a minimal flat surface edge). Body horizontal in a brief flying side-pass over the obstacle. Right arm locked straight supporting partial body weight. Left mechanical arm tucked to body (not used — this is a right-handed vault). Legs together and bent upward to clear obstacle — knees at ~90°. Head tilted downward tracking landing zone. Rifle slung diagonally across back with barrel up (stored during vault — brief stow animation before vault starts).

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
Lighting: Baked isometric top-left directional.
```

---

## VAULT — FACING LEFT (West)

```
Isometric 2.5D vault mid-frame of Sergeant Kael Dros, vaulting over obstacle while moving west.

Preserve exactly from reference: left visor profile, mechanical arm near side (tucked), right arm extended on obstacle edge.

Pose: Right arm planted on obstacle edge at left of sprite. Body horizontal moving left. Legs bent and airborne. Rifle across back. Mechanical arm tucked to chest.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

## VAULT — FACING RIGHT (East)

```
Isometric 2.5D vault mid-frame of Sergeant Kael Dros, vaulting right.

Preserve exactly from reference: right visor profile (crack visible), human arm near side.

Pose: Right arm extended on obstacle edge at right side. Body horizontal moving right. Legs airborne bent. Rifle across back.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

## VAULT — FACING UP (North)

```
Isometric 2.5D vault mid-frame of Sergeant Kael Dros, vaulting north (away from viewer).

Preserve exactly from reference: rear helmet, radio pack, mechanical arm recessed.

Pose: From rear view — body extended northward over obstacle. Right arm on obstacle surface. Legs airborne. Rifle across back. Mechanical arm recessed near side.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

# TANK ENTRY (JUMP / PULL-UP)

## Instructions
This is a specialized 4-frame non-looping animation: approach → reach up → pull up over hatch rim → disappear inside.
Direction: 4 cardinal directions based on which side of the tank the player approaches.
Mechanical arm is used to grab/pull — this is a key character moment.

---

## TANK ENTRY — FACING UP (North — reaching up to tank hatch above)

```
Isometric 2.5D tank entry animation frame (mid-pull-up) of Sergeant Kael Dros climbing into an enemy tank hatch. Facing north, pulling himself up into a hatch opening above him.

Preserve exactly from reference: cracked helmet, mechanical arm, chest rig. Do NOT change costume.

Pose: Both arms raised overhead gripping the hatch rim (shown as the bottom edge of a tank hull rectangle above). Mechanical left arm grips the near edge of hatch rim — blue glow of wrist screen lit actively (using it to grip/hack hatch). Human right arm grips far edge. Body lifted — feet off the ground by ~0.75 tile, dangling and kicking slightly. Head level with hatch rim. Rifle is holstered/slung (not in hand). Torso angled up, slight twist.

Background: Transparent PNG. Tank hull should be minimal — just the bottom edge of the hatch opening as a dark rectangle framing the top of the character.
Art style: Semi-realistic painterly sprite, 2px black outline.
Lighting: Baked isometric top-left directional.
```

---

## TANK ENTRY — FACING DOWN / LEFT / RIGHT
*(Follow the same format as the North-facing entry above, adjusting the approach direction and hatch edge position. The mechanical arm always leads the grip. Blue glow always active on mechanical wrist. Body always in mid-pull-up with feet slightly off ground. Rifle always slung/stowed for this animation.)*
