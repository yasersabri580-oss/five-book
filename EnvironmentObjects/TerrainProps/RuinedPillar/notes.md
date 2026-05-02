# NOTES — RUINED PILLAR

---

## Unity Integration

### Component Setup
- **Component:** `SpriteRenderer` on a static `GameObject` tagged `Environment_Static`
- **Physics:** `PolygonCollider2D` — narrow rectangle matching the column base (0.5 tile wide). Do NOT extend the collider to cover the rebar strands — they are decorative.
- Optional: passable-edge variant with a 0.3-tile-wide collider for tight areas where level designers need vehicles to clip past

### Sorting Layer
- **Sorting Layer:** `Environment`
- **Order in Layer:** Y-sorted. Because the pillar is tall, the Y-sort pivot is at the base — the sprite renders above objects at a lower Y position.

---

## Pivot
- **Pivot:** Bottom-center of the pillar base (not the full sprite bounding box — the base footprint center)
- The rebar at the top extends slightly beyond the bounding box — ensure the sprite canvas has adequate headroom above the actual column top
- Set in Unity Sprite Editor: custom pivot at horizontal center, vertical bottom of the column body

---

## Scale Consistency
- The 0.5 tile footprint width must be visually consistent with ConcreteWallSegment (which is 1 tile wide) — a pillar is roughly half a wall segment's width
- Tall variant height (1.5 tiles) must visually match 1.5 wall segment heights

---

## Reuse Possibilities
- **Clean pillar:** A non-ruined version of the same shape (full-height rectangular column, no break, no rebar) can serve as active-area architectural dressing in FORGE-controlled zones
- **Overgrown variant:** A green-tinted lichen/moss overlay on the pillar for outdoor abandoned environments — reuses base sprite
- **Corner decoration:** Paired pillars on either side of a doorway arch create architectural gateway framing without extra custom assets
- **Rubble base sprite** (`pillar_rubble_base.png`) reusable under any destroyed concrete object for visual language consistency
