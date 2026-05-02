# NOTES — SENTINEL CORPORATE SOLDIER

---

## Pipeline Notes

- SENTINEL Soldiers are the highest-priority **enemy** character in visual fidelity terms. They must look sharp and clean — they are the funded, professional threat.
- **Two sub-type variants** required:
  - **Standard Soldier** (Suppressor / Flanker behaviors) — the reference is this type
  - **Shield Bearer** — left arm replaced with ballistic shield, same rest of costume. Shield bears SENTINEL white-on-black logo on its front face.
- Standard soldier and Shield Bearer share the same animation set, except Shield Bearer has unique **walk-with-shield** and **crouch-behind-shield** animations.

---

## Shield Bearer Sub-Type

The Shield Bearer is an animation extension of the Standard Soldier:
- Left arm raises a rectangular ballistic shield (matte white, ~1m tall, ~0.5m wide, SENTINEL logo front face).
- Shield raised: standard walk/run animations but left arm is locked in a forward-raised position holding the shield. The shield partially obscures the character's left side.
- Shield lowered (non-combat): shield hangs at the left side, arm at rest.
- The shield is part of the sprite, not a separate game object — it must be included in the character's sprite frames.

---

## Animation Priority Order

1. Walk — all 8 directions (needed for patrol and fireteam movement)
2. Run — all 8 directions (flanker and tactical withdrawal)
3. Idle — 4 cardinal directions
4. Attack — carbine fire — all 8 directions
5. Hurt — 4 cardinal directions
6. Death — 4 directions
7. Call reinforcements — 2 directions (wrist terminal press)
8. Shield Bearer: walk-with-shield-raised — all 8 directions
9. Shield Bearer: crouch-behind-shield — 4 directions

---

## Fireteam Visual Logic

In gameplay, SENTINEL soldiers appear in fireteams of 3. The three role types (suppressor, flanker, shield bearer) should be visually distinguishable at a glance at sprite scale:
- **Suppressor:** Standard Soldier — long-range, crouched stance in attack
- **Flanker:** Standard Soldier — sprinting animation set
- **Shield Bearer:** Shield Bearer variant — distinct left arm + shield silhouette

All three use the same base costume. Role is communicated through pose/animation state, not costume changes.

---

## Developer Notes

- SENTINEL soldiers are EMP-resistant (from game doc: S-class Interceptor tanks have EMP-resistant chassis — confirm whether infantry also has this resistance or if it's tank-only). If confirmed infantry EMP-resistant: no EMP-stun animation needed for SENTINEL soldiers.
- The wrist terminal "call for reinforcements" animation is a critical gameplay signal — it tells the player they must destroy the radio tower NOW or reinforcements arrive. Consider a brief white screen flash (from the wrist terminal) as the visual cue. Art team: provide the terminal-press frame; engine adds the white glow particle.
- SENTINEL Soldiers speak in short coded phrases and do not taunt — voice lines are minimal and professional.
- Death animation: clean collapse forward. No dramatic falling — SENTINEL falls like a professional even in death. This is a subtle but important character tone moment.

---

## Known Open Questions

- Confirm whether SENTINEL Soldiers have an EMP resistance in infantry form (only mentioned for tanks in GDD).
- Confirm if the SENTINEL recon team (Mission 6 sewer encounter) uses the same visual as the standard SENTINEL Soldier, or if they have a lighter/stealthier variant (currently assuming: same costume, different behavior).
- Does the white knee pad + white plate carrier visual need to be adjusted for readability in dark environments (Mission 6 sewers are dark)? Consider if a shader edge-glow is needed for dark scenes — flag for lighting design team.
