# OBJECT PROFILE — CONCRETE WALL SEGMENT

---

## Object Name
**ConcreteWallSegment**

---

## Category
Terrain Props

---

## Gameplay Purpose
Primary hard cover and level geometry. Blocks movement and projectiles entirely. Used to define combat lanes, create choke points, and separate areas. Players and enemies cannot pass through or shoot through this wall. A fundamental building block of every level layout.

---

## Where It Is Used
- All level types: military bases, industrial zones, ruined city sectors, perimeter fortifications
- Used as straight wall runs, corner joints, and T-intersections to build enclosed areas
- Placed along level edges to define playable space

---

## Interaction Type
**Static** — No interaction. Full collision blocker.

---

## Visual Description

| Property | Detail |
|---|---|
| Shape | Rectangular slab, 1 tile wide × 1 tile deep × 1.5 tiles tall. Flat top. |
| Material | Poured concrete — rough surface with faint formwork seam lines |
| Color | Desaturated mid-grey (#4A4A48). Top face slightly lighter (#5A5A58). Shadow face darker (#2E2E2C). |
| Size | 1×1 isometric tile footprint. Tiles horizontally for runs. |
| Silhouette | Clean rectangular block. Clearly a wall. No organic variation. |
| Details | 1–2 faint cracks on the front face. Optional rebar stub at top edge. Dirt/grime streak near base. All detail minimal — readable at small size. |

---

## Damage Behavior
**Not destructible.** ConcreteWallSegment is hardened geometry. Tank shells can crack it visually (cosmetic decal applied by engine) but the object does not change state or collapse. Only the WeakWallSection variant is destructible.

---

## Collision Type
**Full block** — 100% movement and projectile collision on all sides. No passable edges.

---

## Animation Needs
**None.** Static sprite only.

---

## Technical Constraints
- Must tile seamlessly: left-edge and right-edge of the sprite must connect cleanly with adjacent wall segments
- Must align to isometric grid without gaps or overlaps
- Pivot: isometric base-center (bottom center of tile footprint)
- Top face must read clearly from the 30-degree camera angle — do not make it too thin
- Must remain readable at 64×64 px minimum display size
- Provide variant sprites: straight segment, corner (45°), and T-intersection cap
