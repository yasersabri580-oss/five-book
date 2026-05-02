# ANIMATION PROMPTS — SANDBAG BARRIER

---

## Animation Status

**No animation required.**

The SandbagBarrier is fully static. The transition to crushed state (when a tank drives through) is an instant sprite swap handled by the engine — no collapse animation is needed or planned for this object.

---

## Static Sprite Variants Required

| Variant | Filename | Description |
|---|---|---|
| Single row | `sandbag_single.png` | 3-bag row, 0.4 tile tall, tileable edges |
| Double row (stacked) | `sandbag_double.png` | 6-bag stack, 0.7 tile tall, tileable edges |
| End cap | `sandbag_endcap.png` | Single bag, for use at barrier line ends |
| Crushed decal | `sandbag_crushed.png` | Flat ground decal (Ground sorting layer) |

---

## Notes for Art Team

- All tileable variants (single and double row) must have matching left and right edge pixels — test by placing two segments side by side in Unity and checking for seam lines
- The end cap can be mirrored horizontally in-engine to serve as both a left-end cap and a right-end cap — provide only one orientation, apply mirroring in Unity Sprite Settings or via scale X = -1
- The crushed decal must be placed on the `Ground` sorting layer, not the `Environment` layer
