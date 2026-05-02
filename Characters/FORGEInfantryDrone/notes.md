# NOTES — FORGE INFANTRY DRONE

---

## Pipeline Notes

- The FORGE Infantry Drone is the **highest-volume enemy** in the game. Its animations will be used in almost every mission.
- Optimize sprite count — this character should have efficient animation cycles to reduce asset volume.
- The **damaged variant** (used at ≤50% HP) must be planned as a second sprite sheet, not a shader overlay — the visual changes (dent on torso, flickering eye) are structural, not just color.
- The **EMP stun state** is a single held frame (all joints locked). This is the simplest animation state.

---

## Animation Priority Order

1. Walk — all 8 directions (needed first for patrol behavior)
2. Idle patrol — 4 cardinal directions
3. Attack burst fire — all 8 directions
4. Alert activation — 4 directions (1-frame)
5. EMP stun — 4 directions (1-frame held)
6. Hurt — 4 cardinal directions minimum
7. Death — 4 cardinal directions minimum
8. Run/sprint — 8 directions (for Aggressor behavior)
9. Damaged variants of all the above

---

## Damaged Variant Notes

At ≤50% HP, the engine switches to the **damaged sprite sheet**. The damaged variants must differ from normal variants only in:
- One sensor eye flickers: provide 2 frames per animation — eye-bright and eye-dark. Engine alternates at 2Hz.
- Right torso panel: visible impact dent + scorch marks. This is baked into all damaged-set frames.
- Right cannon arm: small spark trail at the barrel joint. This is a **particle effect**, NOT baked into the sprite. Particle attachment point: right cannon arm barrel base.

---

## FORGE Crawler (Tunnel Variant)

For Mission 6 (sewers), the **FORGE Crawler** is a smaller variant of the Infantry Drone. It shares the same core visual design but with:
- Much smaller profile: 0.5 tile height (fits in low tunnels)
- No cannon arm — replaced by a second claw arm (pure melee threat)
- Faster movement cycle
- Both sensor eyes always glowing (no damaged variant — they die in 2 hits)

Crawler uses the same color palette and design language as the Infantry Drone. Create separately in the pipeline — it is a sub-variant, not a replacement.

---

## Developer Notes

- FORGE drones cannot be commandeered. No hatch, no cockpit. No entry animation needed.
- FORGE logo on right torso should be visible in north and south-facing sprites but may be obscured in left-profile sprites (acceptable — do not force visibility in all angles).
- Sensor eye glow creates a subtle ambient pool on the ground below the drone — this is a runtime light effect applied by the engine, NOT baked into the sprite.
- The reverse-knee legs are distinctive and must be preserved in all directional views. They are the primary visual differentiator from human enemy types.

---

## Known Open Questions

- Confirm whether FORGE Crawler needs its own full animation set or can share the Infantry Drone rig with a size scale.
- Confirm number of distinct animation variants needed (patrol-only vs. combat-capable drones have different AI — do they need different art, or does engine select behavior from the same sprite set?).
