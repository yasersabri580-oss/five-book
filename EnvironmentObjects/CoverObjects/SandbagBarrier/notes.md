# NOTES — SANDBAG BARRIER

---

## Unity Integration

### Component Setup
- **Prefab:** `SandbagBarrier_Single.prefab` and `SandbagBarrier_Double.prefab`
- **Components:**
  - `SpriteRenderer` — current state sprite
  - `BoxCollider2D` — 1 tile wide × 0.5 tile deep, height based on variant:
    - Single row: full-height box (0.4 tile) — blocks infantry movement, not infantry bullets above crouch height
    - Double row: full-height box (0.7 tile) — taller cover
  - `SandbagController` — listens for `OnVehicleCollision` from tank triggers, switches to crushed decal and disables collider

### Cover Interaction (Crouch Mechanic)
- When the player crouches behind a sandbag barrier, the player's hitbox reduces to the lower half of the character
- The barrier's box collider height (0.4 tile / 0.7 tile) is the threshold — the player's crouch hitbox must fit below this
- This is a character/physics mechanic, not an object art concern — but the barrier heights must be set correctly in the BoxCollider2D

### Vehicle Crush Logic
- The tank prefab has an `OnTriggerEnter2D` component that checks if the collider is tagged `CrushableCover`
- Tag `SandbagBarrier` as `CrushableCover`
- On trigger: the `SandbagController` receives the message, swaps to `sandbag_crushed.png` on the Ground layer, disables the BoxCollider2D

### Sorting Layer
- **Sorting Layer:** `Environment`
- **Order in Layer:** Y-sorted
- Crushed decal: `Ground` layer, Order 5

---

## Pivot
- **Pivot:** Bottom-center of the 1 tile wide × 0.5 tile deep footprint
- End cap (single bag): pivot at bottom-center of the single bag footprint (0.3 tile wide)

---

## Tiling / Level Design Setup
A complete defensive line setup:
1. Place `EndCap` at the left end (facing right)
2. Place as many `SandbagBarrier_Single` (or Double) as needed side by side
3. Place a mirrored `EndCap` (scale X = -1) at the right end

This creates a natural-looking sandbag wall with tapered ends.

---

## Scale Consistency
- Single row (0.4 tile tall): just above the knee of the character sprite — player clearly reads as "behind low cover" when crouching
- Double row (0.7 tile tall): reaches approximately the waist/chest of the character sprite — better cover, less movement flexibility
- Sandbag barrier must be clearly lower than the ConcreteBlock (1.0 tile tall) and ConcreteWallSegment (1.5 tile) — height hierarchy communicates cover quality at a glance

---

## Reuse Possibilities
- **Snow-dusted variant:** Add a thin white cap to the top row of bags (#F0F0F0, thin horizontal band on the top face) for winter environment levels
- **Dirt-stained variant:** Darker, muddier color version (#6A5A3A base) for wet/muddy outdoor areas — recolor only
- **Double row L-corner:** Two double row segments placed at 90° with a corner piece (a single bag in the corner gap) — create corner defensive positions without custom art
- **Destroyed (non-tank):** For scripted scenes where the area has clearly been bombed, use the crushed decal as permanent scenery with no behavior
