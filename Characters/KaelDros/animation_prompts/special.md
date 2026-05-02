# ANIMATION PROMPTS — KAEL DROS — SPECIAL ABILITIES

---

## Instructions for All Special Prompts
- Use the canonical reference image (see `reference_prompt.md`) as the visual source of truth.
- **Costume, proportions, and visor design are locked across all special ability frames.**
- Each ability has a distinct visual moment. Keep it readable and sprite-friendly.
- Sprite size: 192×192 px per frame. Isometric 2.5D. 30-degree pitch.

---

# HACK (Terminal Interaction)

## Instructions
Non-looping, 3-frame: approach press → active hack (held 1.5s loop) → release.
The **hack loop** (middle state) should loop for the duration of the 1.5s hack.
2 directional variants: player pressing terminal to their left, and player pressing terminal to their right.
Mechanical arm is pressed against the terminal surface — this is the hacking limb.

---

## HACK — PRESSING LEFT (Terminal to West side)

```
Isometric 2.5D hack animation frame (active hack — mechanical arm pressed to terminal) of Sergeant Kael Dros, standing at a terminal to his left.

Preserve exactly from reference: cracked amber visor helmet, gunmetal mechanical left arm with blue wrist interface, canvas chest rig, cargo trousers, boots. Do NOT change costume.

Pose: Character standing left-profile, facing west, left arm fully extended into a terminal surface (terminal represented as a small glowing panel at left edge of sprite — can be minimal). Mechanical arm palm pressed flat against terminal panel. Blue glow (#4AB0D0) emanates from wrist interface screen and from the palm/finger contact points — this is the peak-glow frame of the pulse (bright). Head slightly bowed — concentrating. Right arm holds rifle loosely at side, muzzle down (non-combat ready). Feet planted, weight slightly forward-left.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
Lighting: Baked isometric top-left directional plus the blue glow self-illumination from mechanical arm.
Note: This frame is the brightest-glow frame. Create a dim-glow frame for the loop by reducing the blue emission intensity — engine alternates the two to create the pulsing effect.
```

---

## HACK — PRESSING RIGHT (Terminal to East side)

```
Isometric 2.5D hack animation frame (active hack) of Sergeant Kael Dros, pressing mechanical arm against terminal to his right.

Preserve exactly from reference: right profile visor (crack visible), mechanical arm extended right across body.

Pose: Character facing right (east), but mechanical left arm extends across the body to press the terminal on the right side. This cross-body reach creates a distinctive, slightly awkward but purposeful pose. Torso rotated slightly right. Mechanical arm reaches diagonally right — fully extended. Wrist interface glowing bright blue (#4AB0D0) at contact point. Right human arm holds rifle loosely, muzzle down.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
Note: Cross-body reach variant — the mechanical arm being the only hacking limb creates this unique cross-body gesture for right-side terminals.
```

---

# ROLL (DODGE)

## Instructions
4 cardinal directions. Non-looping. 3-frame rapid dive: launch → full roll → land-crouch.
Fast, low-profile. The roll covers approximately 2 tiles of distance.

---

## ROLL — FACING DOWN (South)

```
Isometric 2.5D roll dodge animation frame (mid-roll — fully airborne) of Sergeant Kael Dros, rolling south.

Preserve exactly from reference: helmet, mechanical arm, chest rig, cargo trousers, boots. Do NOT change costume.

Pose: Character fully horizontal, tucked in roll — body parallel to ground, approximately 0.5 tile off the surface. Spine rounded. Head tucked, chin to chest (helmet brim forward). Both arms tucked to body — rifle pressed against chest in right arm grip, mechanical arm tucked tight to torso. Knees pulled to chest. The character is a compact rolling ball moving south. No limbs extended. This is the briefest possible airborne silhouette.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
Lighting: Baked isometric top-left directional.
```

---

## ROLL — FACING LEFT (West)

```
Isometric 2.5D roll dodge mid-frame of Sergeant Kael Dros, rolling west (left).

Preserve exactly from reference: all costume elements preserved.

Pose: Same fully tucked roll, body moving left. Left profile — mechanical arm tucked to chest (visible as a grey mass against olive jacket). Rifle against right side. Compact, airborne.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

## ROLL — FACING RIGHT (East)

```
Isometric 2.5D roll dodge mid-frame of Sergeant Kael Dros, rolling east (right).

Preserve exactly from reference: all costume elements preserved.

Pose: Tucked roll right. Right profile. Mechanical arm on far side (left of sprite) tucked to chest — grey mass visible. Compact roll silhouette.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

## ROLL — FACING UP (North)

```
Isometric 2.5D roll dodge mid-frame of Sergeant Kael Dros, rolling north (away from viewer).

Preserve exactly from reference: rear helmet visible in tucked roll, mechanical arm rear-side grey.

Pose: Tucked roll away from viewer. Rear of helmet at top. Body compact. Arms and legs tucked. Moving northward.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

# SURVIVOR INSTINCT PASSIVE (Low HP Visual)

## Instructions
This is an **overlay layer only** — it is applied over any existing animation state via engine shader.
Art team provides: a semi-transparent red pulse aura around the character silhouette.
This is NOT a separate character animation — it is a sprite border glow.

---

## SURVIVOR INSTINCT AURA — OVERLAY PROMPT

```
Semi-transparent red glow aura overlay for a 192×192 px sprite frame. The aura hugs the exact silhouette of the character (matches alpha channel of character sprite). The glow is:
- Color: desaturated blood red (#8C2020) with soft feathered edge (8px feather)
- Opacity: 40% at the inner edge, 0% at the outer edge (radial falloff)
- Pulse: this is the bright-state frame (for pulse animation). Dim-state frame: reduce opacity to 15%. Engine alternates bright (this frame) and dim at 0.5s interval.
- NO solid outline — purely a soft glow following the sprite silhouette.

This overlay is applied as a second render layer on top of the character sprite in Unity URP's sprite renderer, using a custom material with an outline/glow shader. Do NOT bake this into the character animation frames.
```
