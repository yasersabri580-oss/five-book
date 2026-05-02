# OBJECT PROFILE — WOODEN CRATE

---

## Object Name
**WoodenCrate**

---

## Category
Destructible Objects

---

## Gameplay Purpose
Common destructible obstacle. Blocks infantry movement and provides soft cover until destroyed. Can be stacked or grouped. Players and enemies can destroy it with gunfire or explosives. When destroyed, it disappears (leaving a small rubble decal). Level designers use crates to create soft cover zones that change during combat — cover that was there at the start of a fight may not be there at the end. Also used as supply containers: some crates contain ammo pickups that spawn on destruction.

---

## Where It Is Used
- Supply depots, warehouse areas, loading docks
- Enemy staging areas — crates near enemy spawn points
- Interiors: storage rooms, factory floors
- NOT used in field/outdoor areas — use ConcreteBlock or SandbagBarrier for outdoor cover

---

## Interaction Type
**Destructible** — Can be destroyed by gunfire, explosives, or melee. May contain loot pickup on destruction.

---

## Visual Description

| Property | Detail |
|---|---|
| Shape | Cube with lid. 0.8 tiles wide × 0.8 tiles deep × 0.8 tiles tall. Slightly smaller than a full tile to allow stacking and visual breathing room. |
| Material | Rough planked wood — visible wood planks on all faces, horizontal grain on the sides, with steel corner brackets |
| Color | Warm tan wood (#8A6A3A). Aged/dirty: darker streaks (#5A3A18). Steel brackets: dark grey (#3A3A38). Metal nails: small dark dots. |
| Size | 0.8×0.8 tile footprint |
| Silhouette | Boxy cube. Clearly a container. Lid visible on top face from isometric angle. |
| Details | Wood grain lines on planks. 4 corner steel L-brackets (one at each vertical corner). 3–4 nails per plank visible as small dark dots. Optional stenciled military text ("FORGE ARMS CO." in worn stencil) on one face — adds lore flavor. |

---

## Damage Behavior

**Three visual states (not animated — sprite swap on damage threshold):**

| State | HP Threshold | Visual |
|---|---|---|
| Intact | 100–51% HP | Normal crate sprite |
| Damaged | 50–1% HP | Cracked planks, one corner bracket bent, lid slightly ajar |
| Destroyed | 0% HP | Sprite removed; rubble decal spawns at position (loose planks, metal bracket fragments on ground) |

The destroyed rubble decal is a separate flat sprite placed on the ground layer.

---

## Collision Type
**Full block** (intact and damaged states) — 0.8 tile footprint box collider. Collider removed on destruction.

---

## Animation Needs
**None** — state changes are sprite swaps, not animations. A simple impact shake (0.1s position oscillation) on damage is handled by engine script, not art.

---

## Technical Constraints
- Three sprites required: `crate_intact.png`, `crate_damaged.png`, `crate_destroyed_decal.png`
- Stacking: Two crates stacked vertically (a double-stack variant) is a separate sprite — 2× height, same footprint. Provide `crate_stack2.png` for double-stack.
- The "FORGE ARMS CO." stencil must be readable if present but not overly prominent — use worn stencil style (#6A4A20 faded darker on the wood)
- Damaged state must be readable at a glance — cracked planks must be distinct from intact
- Must be visually distinct from the SupplyBox (metal, green) — crate is wood/warm tones
