# OBJECT PROFILE — SANDBAG BARRIER

---

## Object Name
**SandbagBarrier**

---

## Category
Cover Objects

---

## Gameplay Purpose
Low-profile cover that stops bullets but does not fully block line of sight or movement. Infantry can crouch behind a sandbag barrier to become protected from gunfire while still being able to shoot over it. Tanks can drive through and crush sandbag barriers (destroying them permanently). The sandbag is the archetypal infantry cover object — readable, functional, and present in nearly every combat encounter. Stacked variants (single row, double row) provide different degrees of cover.

---

## Where It Is Used
- All combat encounter zones — the most common cover object in the game
- Defensive positions set up by enemy infantry
- Player rest points before combat engagements
- Used extensively in outdoor battle zones, corridors, and fortified positions

---

## Interaction Type
**Static** (default) — Player crouches behind it. No button interaction needed. Cover behavior is handled by the player's crouch mechanic and the obstacle's collision box.
**Destructible by vehicle only** — A tank driving through it crushes the barrier (replaced with flat debris sprite).

---

## Visual Description

| Property | Detail |
|---|---|
| Shape | Row of 3 tightly-packed sandbags. Each bag is an ovoid mound. Single-row barrier: 1 tile wide × 0.5 tile deep × 0.4 tile tall. Double-row (stacked): same footprint, 0.7 tile tall. |
| Material | Burlap sandbags — rough woven texture. Slightly bulging mounds with visible stitching on the top of each bag. |
| Color | Base: warm sandy tan (#8A7A58). Darker streaks where wet/compressed (#5A4A30). Stitch lines: darker (#4A3A22). Sandbag interior bulge highlight: lighter tan (#A08A68). |
| Size | 1 tile wide × 0.5 tile deep. Heights: single row 0.4 tile, double row 0.7 tile. |
| Silhouette | Three connected mound shapes in a row. Clearly a sandbag barrier. Unmistakable. |
| Details | Each sandbag has visible burlap weave lines (simplified — light cross-hatch). The bags are tied at the top — a slight pinch/tie at the top of each bag with a dark rope (#3A2A18). The barrier sits on the ground with slight compression at the base. Dirt/sand trickle at the corners suggesting the bags are slightly leaking. |

---

## Damage Behavior
**Crushed by vehicle only:**

| State | Trigger | Visual |
|---|---|---|
| Intact | Default | Normal sandbag barrier |
| Crushed | Tank drives through | Flattened bags on the ground — a low flat sand spill decal |

Infantry gunfire and explosions do NOT destroy sandbag barriers (they absorb bullet impact as intended). Grenades displace them (cosmetic — one bag appears to shift visually, engine applies decal overlay, but the barrier remains functional).

---

## Collision Type
- **Infantry:** Partial block — movement blocked (cannot walk through), but crouch state allows being "behind" the barrier (hitbox is reduced below the barrier top)
- **Vehicles:** Crushable — tank collider overrides the sandbag collider, triggering the crush event

---

## Animation Needs
**None.** Static sprite only. Three variants: single row, double row (stacked), and crushed ground decal.

---

## Technical Constraints
- Must be clearly distinguishable from ConcreteBlock (hard/angular vs soft/rounded)
- The single-row barrier (0.4 tile tall) must be short enough that a crouching character sprite clearly reads as "behind cover" (character sprite clips to just above the barrier top when crouching)
- Must tile horizontally: multiple sandbag barriers placed side by side must connect seamlessly for long defensive lines
- Provide end cap variant (half-barrier, 0.5 tile wide) for natural-looking barrier ends that don't look cut off
