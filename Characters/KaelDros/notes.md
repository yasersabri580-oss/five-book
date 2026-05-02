# NOTES — SERGEANT KAEL DROS

---

## Pipeline Notes

- Kael is the highest-priority character in the pipeline. All other character designs should maintain visual contrast against him.
- The **mechanical arm** is the most critically distinctive feature. In every animation frame, the mechanical arm must be visually distinguishable from the human arm — never render them at the same shade.
- The **cracked visor** is the second most distinctive feature. Even in small sprite size, the crack line + tape repair should be readable.
- The **chest rig silhouette** adds bulk to the torso that differentiates Kael from unarmored characters. Do not lose this in directional views.

---

## Animation Priority Order

Generate in this order for the fastest playable build:
1. Idle (down-facing / south) — first sprite needed for UI and menus
2. Walk (all 8 directions)
3. Run (all 8 directions)
4. Attack — rifle fire (all 8 directions)
5. Hurt (all 8 directions)
6. Death (all 4 cardinal directions minimum)
7. Roll (4 directions)
8. Attack — melee, grenade, EMP (4 directions each)
9. Hack (2 directions: facing terminal left or right)
10. Vault (2 directions: left/right)
11. Jump / enter tank, Exit tank

---

## Consistency Anchors

These visual elements must appear in **every single animation frame** without exception:
- Cracked visor helmet (color #4A5240, amber tint #C89020)
- Mechanical grey left arm (#5A5A5A)
- Chest rig over jacket
- Dark boots

These elements may change subtly per animation:
- Rifle position (raised, lowered, slung)
- Mechanical arm position (extended, at side, pressed to surface)
- Body lean angle (upright vs. forward lean)

---

## Developer Notes

- Kael's on-foot sprite footprint is 1×1 isometric tile.
- Crouched state reduces effective hitbox to 1×0.5 tile (handled in engine, not art — art simply shows lower silhouette).
- The **Survivor Instinct** passive (at <15% HP) should be a shader/overlay effect applied by the engine, not baked into the sprite. Art team does not need to create separate low-HP sprites.
- **Hack animation** uses the mechanical arm's wrist screen — the blue glow should pulse in a 3-frame loop (dim → bright → dim) during the 1.5-second hack.
- Tank entry/exit animations are **one-directional only** (player always approaches from the hatch side) — these do not need 8-direction variants.

---

## Known Open Questions (for art director review)

- Should the visor glow/light react to EMP usage? (Currently: no — propose adding a brief flicker overlay handled by engine.)
- Grenade throw direction: currently planned as 4-direction only. Confirm with gameplay team if 8-direction is needed.
- Death animation: currently planned as 2 variants (forward fall, backward fall). Confirm if left/right falls are also needed for all enemy-direction hits.
