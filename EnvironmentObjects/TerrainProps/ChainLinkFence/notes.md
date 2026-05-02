# NOTES — CHAIN-LINK FENCE

---

## Unity Integration

### Component Setup
- **Component:** `SpriteRenderer` on a static `GameObject` tagged `Environment_Fence`
- **Physics (intact):** `BoxCollider2D` — narrow box matching the fence panel width (1 tile wide, 0.1 tile deep). Infantry cannot pass through. Set Layer to `FenceLayer` which is NOT hit by projectile raycasts.
- **Physics (crushed):** Collider is disabled. Crushed sprite is a flat ground sprite with no collision.
- **Tank interaction:** When a tank's collider overlaps the fence collider, the fence GameObject switches to crushed state (sprite swap + collider disable). Implement via `OnTriggerEnter2D` on the tank, calling `FenceController.Crush()`.

### Sorting Layer
- **Sorting Layer:** `Environment`
- **Order in Layer:** Y-sorted. Intact fence renders above ground and at infantry mid-level. Crushed state renders below infantry (ground level).

---

## Pivot
- **Fence segment pivot:** Bottom-center of the panel (base-center)
- **Post pivots:** Bottom-center of the post footing
- Posts are placed as separate GameObjects positioned at the ends of each segment

---

## Tiling Rules
- Fence is assembled modularly: one post + one segment + one post = one section
- Mid-post is used when two segments share a post — place mid-post at the segment junction
- End-post used at the start and end of a fence run
- Never place a segment without posts at its ends

---

## Scale Consistency
- Fence height (1.2 tiles) should be visually shorter than the ConcreteWallSegment (1.5 tiles) — players can visually read that a fence is lower than a wall
- Posts extend slightly above the fence segment top — consistent across all fence tile setups

---

## Reuse Possibilities
- **Barbed wire only variant:** Just the top barbed wire strand as a standalone sprite (no mesh, no posts) for quick perimeter dressing on top of walls
- **Damaged intact variant:** A slightly bent/damaged-but-standing fence sprite that implies previous near-miss impacts — for pre-damaged levels
- **Electrified fence:** Reuse the base fence sprite; add a separate glow overlay (animated yellow-white pulse) to create electrified fence hazard — no new base art needed
