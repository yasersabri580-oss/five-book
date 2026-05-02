# ANIMATION PROMPTS — CONCRETE WALL SEGMENT

---

## Animation Status

**No animation required.**

The ConcreteWallSegment is a fully static terrain object. It does not move, react, or change state under any gameplay condition.

The only visual change that can occur is a damage decal (cracks, scorch marks) applied dynamically by the engine via a separate decal sprite layer — this is not animated and is not part of this object's sprite sheet.

---

## Static Sprite Variants Required

While the ConcreteWallSegment itself is not animated, the following static sprite variants are needed for the tile system:

| Variant | Description |
|---|---|
| `wall_straight.png` | Standard 1×1 segment — tileable left/right |
| `wall_corner.png` | 90-degree corner piece |
| `wall_t_cap.png` | T-intersection — wall connects on three sides |

These are three separate sprites, not animation frames. They are placed in the object's sprite folder in Unity.
