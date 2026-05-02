# OBJECT PROFILE — WEAK WALL SECTION

---

## Object Name
**WeakWallSection**

---

## Category
Destructible Objects

---

## Gameplay Purpose
A wall section that can be destroyed by concentrated firepower or a single tank shell, creating a new passage through previously blocked terrain. Level designers use weak walls to gate progression (player must destroy the wall to advance) or create optional breach routes (player can choose to punch through instead of using the main path). Weak walls must be visually distinct from the indestructible ConcreteWallSegment — players must recognize without being told that this wall can be broken.

---

## Where It Is Used
- Military base interiors: thin partitions that can be breached
- Industrial structures: deteriorated brick sections in old factory walls
- Ruined environments: partially collapsed walls that are near the breaking point
- Always used as a contextual "secret or alternate path" or "scripted breach point"

---

## Interaction Type
**Destructible** — Destroyed by heavy gunfire (30+ bullets), grenades (2 grenades), or one tank shell (instant). Creates a passable gap on destruction.

---

## Visual Description

| Property | Detail |
|---|---|
| Shape | Same footprint as ConcreteWallSegment (1 tile wide × 1 tile deep × 1.5 tiles tall). Must look similar to the concrete wall from a distance but visually communicate fragility up close. |
| Material | Old brick or deteriorated concrete — visually older and weaker than the solid ConcreteWallSegment. Brick coursing visible on the face. |
| Color | Dusty brick red-brown (#7A5A44). Mortar lines: lighter grey-tan (#8A7A68). Significant cracking and spalling across the face. Darker at the base (moisture staining). |
| Size | Same as ConcreteWallSegment: 1×1 tile footprint, 1.5 tiles tall. |
| Silhouette | Same silhouette as a wall segment — but the surface reads as deteriorated. |
| Details | Visible brick coursing pattern (brick rows across all faces). Large diagonal cracks running across the south face. Sections of missing brick near corners exposing dark gaps. Slight forward lean (top is 3–5° toward the camera) suggesting structural instability. |

---

## Damage Behavior

**Three states (sprite swap):**

| State | HP | Visual |
|---|---|---|
| Intact (structurally weak) | 150–76 HP | Cracked brick wall, large cracks, some missing brick at corners |
| Heavily Damaged | 75–1 HP | Major cracks extend to center, top portion visibly crumbling, mortar falling |
| Destroyed | 0 HP | Wall removed; rubble pile sprite placed at base (pile of bricks on the ground, passable terrain) |

The destroyed rubble pile is passable by infantry (no collision) but blocks vehicles (low pile, vehicle collision remains).

---

## Collision Type
- **Intact/Damaged:** Full block — same collision as ConcreteWallSegment
- **Destroyed:** Rubble pile is passable by infantry, low collision box for vehicles

---

## Animation Needs
**None for standard states** — sprite swaps only. A 4-frame collapse animation is recommended for the final destruction event (brick wall crumbling from top to bottom) as it is a significant gameplay moment.

---

## Technical Constraints
- Must be visually distinguishable from ConcreteWallSegment: the brick material, obvious cracking, and slight lean must communicate "this is not the same wall" at a glance
- Same 1×1 tile footprint as ConcreteWallSegment — they can be used in the same wall run
- Rubble pile on destruction must not block player progress — ensure rubble pile collision height allows infantry to walk over
- The slight forward lean is a visual trick only — collider is still the full block rectangle
