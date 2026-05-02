# ANIMATION PROMPTS — CONCRETE BLOCK

---

## Animation Status

**No animation required.**

The ConcreteBlock is fully static. It does not react to infantry weapons. Tank shell impact results in a cosmetic decal (applied by the engine as a separate decal sprite overlaid on the block) — this is not an animation of the block itself.

---

## Static Sprite Variants Required

| Variant | Filename | Description |
|---|---|---|
| Standard block | `concrete_block.png` | Single block, full detail |
| Impact decal overlay | `concrete_block_impact.png` | A small impact crater/chip decal sprite placed over the block by engine on tank shell hit. Rendered at +1 sort order above the block. |

---

## Notes for Art Team

- The impact decal (`concrete_block_impact.png`) is a small sprite (approximately 0.2 tile wide) showing a radiating chip/crater on the concrete face. It is placed by the engine at the hit position on the block's south face — not a full-block sprite replacement.
- Multiple impact decals can be stacked (if the block is hit multiple times) — the engine manages decal stacking up to a max of 3.
- The impact decal uses the same concrete palette: raw concrete chip (#5E5E5A lighter inside the crater, #2A2A28 dark shadow at the chip edge).
