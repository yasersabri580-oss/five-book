# NOTES — RECLAIMER MILITIA SOLDIER

---

## Pipeline Notes

- The Reclaimer Militia Soldier is the **second most common human enemy** in the game.
- There should be **3 visual variants** of the Reclaimer to suggest a faction rather than clones. Variant differentiation should be light — only change: helmet color, jacket condition, bandolier/no bandolier swap. All variants share the same animation set.
- Variants:
  - **Variant A (reference):** spray-painted brown helmet, olive jacket, bandoliers
  - **Variant B:** no helmet / black balaclava, darker jacket, single bandolier
  - **Variant C:** rust-red spray helmet, same jacket with more visible patches/tears, double bandolier
- The animation set is shared across all variants — variants are palette/texture swaps at the sprite atlas level.

---

## Animation Priority Order

1. Walk — all 8 directions
2. Run/sprint — all 8 directions (Aggressor behavior)
3. Idle — 4 cardinal directions
4. Attack — rifle hip-fire — all 8 directions
5. Hurt — 4 cardinal directions
6. Death — 4 directions
7. Attack — molotov throw — 4 directions
8. Scavenge sprint (same as run sprites — reuse)

---

## Faction-Specific Mechanic: Scavenge Rush

When the Scavenge Rush triggers, the Reclaimer runs directly toward a destroyed tank. This uses the **Run animation set** — no unique animation needed. The direction is determined at runtime by pathfinding. Only the AI state changes; the art is reused.

---

## Developer Notes

- Reclaimers vocalize (shout taunts, war cries) — sound team note: each variant should have distinct voice lines to avoid repetition.
- Reclaimers interact with destroyed tanks (the game's Scavenge Rush mechanic). The "tank interaction" animation for a Reclaimer is the same as Kael's tank entry animation (repurposed — same hatch-grab pull-up). Confirm with animation team.
- Molotov throw: the lighter flicker (lighting the rag) is a 1-frame bright orange flash on the left hand holding the bottle, just before the throw. This can be a sprite frame or a 1-frame engine particle at the hand position. Recommend engine particle for efficiency.
- Reclaimer death should be more visually dramatic than FORGE drone death — these are human deaths with physical impact reads. Plan for at least 2 death variants (forward collapse and backward collapse) to avoid repetition.

---

## Known Open Questions

- Confirm mission count: Reclaimers appear in Missions 2, 5, 9. Verify if they appear in Mission 10 (game doc references "chaos" in the city ruins — Reclaimers may appear briefly).
- Are the 3 visual variants needed for Chapter 1 release, or is Variant A sufficient as a placeholder?
- Confirm if the Reclaimer leader (unnamed in current GDD) needs a distinct visual. Currently treating all Reclaimers as unnamed grunts.
