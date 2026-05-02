# NOTES — CONCRETE BLOCK

---

## Unity Integration

### Component Setup
- **Prefab:** `ConcreteBlock.prefab`
- **Components:**
  - `SpriteRenderer` — static block sprite
  - `BoxCollider2D` — 1 tile wide × 0.6 tile deep × 1.0 tile tall. This is a full block (no partial or passable).
  - `ConcreteBlockController` — listens for tank shell hit events, spawns impact decal at hit position
- **Tag:** `IndestructibleCover` (so turret AI knows this is permanent cover and pathfinds around it)

### Sorting Layer
- **Sorting Layer:** `Environment`
- **Order in Layer:** Y-sorted

---

## Pivot
- **Pivot:** Bottom-center of the 1 tile × 0.6 tile footprint (the widest part of the trapezoid at the base)
- The top of the block is narrower than the base — the pivot must be at the BASE, not at the visual center of the sprite

---

## Scale Consistency
- Concrete block (1.0 tile tall) is the same height as the ConcreteWallSegment height baseline but with a different footprint (0.6 tile vs 1 tile deep)
- The concrete block is taller than the sandbag barrier (0.4 / 0.7 tile) — players understand it provides better standing-height cover
- The trapezoidal silhouette must be distinctly different from the rectangular ConcreteWallSegment silhouette — test by placing both in the same scene view and confirming visual distinction at a glance

---

## Placement in Rows
- For a barrier row: place multiple blocks directly adjacent (touching side-to-side)
- A slight manual positional offset (0.05 tile depth difference) on alternating blocks makes the row feel naturally placed rather than perfectly aligned
- Level designers should avoid perfectly uniform spacing — slightly irregular placement reads as more realistic

---

## Cover Height Design Note
- A player CHARACTER (2.8 tiles tall) standing behind a 1.0 tile block is at approximately waist/chest height cover from the front
- The player's head/shoulders are above the block when standing — this is INTENTIONAL. The concrete block provides partial standing cover only (torso-down protected, head exposed)
- Players wanting full standing cover must use the ConcreteWallSegment
- This height differentiation creates gameplay decision-making in cover choice

---

## Reuse Possibilities
- **Large concrete block (2-tile wide):** Scale the same sprite to 2× width for a wider barrier. Works visually because of the smooth machine-formed concrete face.
- **Elevated block (platform):** Used as a height platform with one block stacked on another (stacked using scene objects, no custom art) — 2.0 tile tall elevated position for sniping or advantaged positioning
- **Ruined block:** The same block with heavy damage: large chunks chipped off the corners, deeper cracks, more severe impact decals pre-baked into the sprite. Used as static level dressing in ruined areas. Same pipeline, no new geometry.
