# OBJECT PROFILE — CONCRETE BLOCK

---

## Object Name
**ConcreteBlock**

---

## Category
Cover Objects

---

## Gameplay Purpose
Solid mid-height infantry cover that blocks bullets and projectiles at standing and crouching height. The concrete block is the hardest cover option short of a full wall — it does not get destroyed by small arms, withstands grenades (takes no damage), and requires a direct tank shell to damage. It is a reliable safe haven in a fight. Players learn to identify concrete blocks as "safe cover" — contrasted with sandbag barriers (softer, crouchable) and wooden crates (destructible). The concrete block's visual weight and mass communicate permanence and safety.

---

## Where It Is Used
- Military bases: defensive fortification barriers, vehicle checkpoint dividers
- Industrial zones: large concrete supports, cable reel bases, construction blocks
- Urban areas: highway dividers, road barriers
- Used as standalone or in rows for defensive lines

---

## Interaction Type
**Static** — No interaction. Hard cover blocker.

---

## Visual Description

| Property | Detail |
|---|---|
| Shape | Jersey-barrier style concrete block — wider at the base, slightly tapered inward toward the top. 1 tile wide × 0.6 tile deep × 1.0 tile tall. Trapezoidal cross-section (wider base, narrower top). |
| Material | Heavy poured concrete. Smooth-finished surface (not rough rock — machine-formed mold). |
| Color | Base grey (#4A4A48). Top face: lighter (#5E5E5A). Shadow face: darker (#2A2A28). Wear marks: darker streaks (#3A3A35) and tire/scrape marks. |
| Size | 1×0.6 tile footprint. 1.0 tile tall. |
| Silhouette | Trapezoidal mass — the wider base and narrower top give it a distinctive silhouette distinct from the straight-sided ConcreteWallSegment. |
| Details | A single horizontal seam line around the mid-height (suggesting two-piece mold). Small rebar loop embedded in the top face (a U-shaped metal bar, dark grey, used for lifting — sits flush). Tire scuff marks on the south face (dark rubber smear #2A2020 at lower half). Cracked corner at one edge (minor, subtle). Optional: faded yellow safety stripe at the base (#A88000 faded — barely visible, from its original road-divider use). |

---

## Damage Behavior
**Not destructible by infantry weapons or grenades.** Only a direct tank shell can damage it:
- 1 tank shell: cosmetic impact crater (decal applied by engine) + slight forward displacement (script-handled nudge, 0.2 tile push). Does not destroy the block.
- No destroyed state for the concrete block — it is a permanent fixture.

---

## Collision Type
**Full block** — 1×0.6 tile box collider. Full movement and projectile blocker at all heights (the block is 1 tile tall — no over-cover shooting possible).

---

## Animation Needs
**None.** Static sprite only.

---

## Technical Constraints
- Trapezoidal profile must be visible from the isometric angle — the base visibly extends beyond the top
- The rebar lifting loop on the top face must be recognizable as metal (not a decorative ring) — keep it simple and readable
- Must not be confused with RockFormation (concrete = straight machine edges; rock = irregular organic edges)
- Multiple blocks can be placed in a row to create a road barrier line — left and right edges do not need to tile but should not create visual gaps that look wrong when adjacent
