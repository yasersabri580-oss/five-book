# ANIMATION PROMPTS — WOODEN CRATE

---

## Animation Status

**No animation required.**

The WoodenCrate uses sprite swaps for its damage states (intact → damaged → destroyed). The transitions are handled by the engine script `DestructibleController` calling `SpriteRenderer.sprite = ...` when HP thresholds are crossed.

A brief impact shake (position oscillation over 0.1s) on damage is a code-driven effect — no art deliverable needed for this.

---

## State Summary

| State | Trigger | Sprite Used | Art Deliverable |
|---|---|---|---|
| Intact | Default / HP 100–51% | `crate_intact.png` | ✅ Required |
| Damaged | HP drops to 50% | `crate_damaged.png` | ✅ Required |
| Destroyed | HP reaches 0 | Main sprite removed + `crate_destroyed_decal.png` placed on ground | ✅ Required |
| Double-stack | Level designer placed | `crate_stack2.png` | ✅ Required |

---

## Notes for Art Team

- All four sprites above are in the `DestructibleObjects/WoodenCrate/` folder in Unity
- The destroyed decal sprite must be on the `Ground` sorting layer, not the `Environment` layer
- Do not create a transition animation — sprite swap is instant and handled by code
- If loot is inside the crate, the loot pickup spawns at the crate's position the moment the destroyed state triggers — this is a gameplay/code concern, no additional art needed from the object sprite side
