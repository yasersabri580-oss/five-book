# NOTES — WEAK WALL SECTION

---

## Unity Integration

### Component Setup
- **Prefab:** `WeakWallSection.prefab`
- **Components:**
  - `SpriteRenderer` — current damage state sprite
  - `BoxCollider2D` — same dimensions as ConcreteWallSegment (full block, 1×1 tile)
  - `DestructibleController` — HP: 150. Swap to `weakwall_damaged.png` at 75 HP. Trigger collapse animation at 0 HP.
  - `Animator` — plays `collapse` animation clip once on `OnDestroyed` event
  - `HealthComponent` — 150 HP
- **Rubble prefab:** `WeakWallRubble.prefab` — static GameObject with `weakwall_rubble.png`, placed at position of destroyed wall. Has a low `BoxCollider2D` (height 0.1 tile) that blocks vehicles but NOT infantry.

### Damage Thresholds
| HP | Action |
|---|---|
| 150 → 76 | Sprite: `weakwall_intact.png` |
| 75 → 1 | Sprite: `weakwall_damaged.png` |
| 0 | Trigger collapse Animator → spawn `WeakWallRubble` → destroy WeakWallSection GameObject |

### Sorting Layer
- **Sorting Layer:** `Environment`
- **Order in Layer:** Y-sorted (same as all wall objects)
- Rubble pile: `Ground` layer, `Order in Layer: 5`

---

## Pivot
- **Pivot:** Bottom-center of the 1×1 tile footprint (identical to ConcreteWallSegment for grid compatibility)
- The WeakWallSection can be placed in the same wall run as ConcreteWallSegments — pivots must be identical for alignment

---

## Scale Consistency
- The WeakWallSection is the SAME size as ConcreteWallSegment
- The visual difference is entirely material and damage-based — not size-based
- In a mixed wall run (ConcreteWallSegment + WeakWallSection), the different texture is the only visual cue — this is intentional design

---

## Level Design Notes
- Mark WeakWallSection instances in the editor with a custom gizmo so level designers can see at a glance which walls are destructible
- Typically placed at intentional breach points: one per corridor or room, never multiple adjacent weak walls (that would allow too wide a gap)
- Never block a required progression path with an indestructible wall when a weak wall should be there

---

## Reuse Possibilities
- **Ruined wall decor:** The intact sprite (heavily cracked, lean) placed as a static non-destructible prop (`Environment_Static` tag, no HP) for pre-ruined decorative sections
- **Wood plank variant:** Swap the brick texture for horizontal dark wood planks (#5A3A18) — creates a `WeakWoodWall` variant at low art cost, used for interior wooden partitions in older structures
