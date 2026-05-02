# OBJECT PROFILE — RUINED PILLAR

---

## Object Name
**RuinedPillar**

---

## Category
Terrain Props

---

## Gameplay Purpose
Vertical cover and level geometry for destroyed or abandoned architecture. Provides tall narrow cover points that allow infantry to stand behind while still being flanked. Creates verticality cues in the environment — players can read the space as "this was once a building." Used in ruined city sectors, abandoned factories, and battle-scarred fortifications.

---

## Where It Is Used
- Ruined urban levels: collapsed buildings, bombed-out city blocks
- Abandoned industrial zones: factory floors with broken support columns
- Pre-battle zones: showing the aftermath of earlier FORGE strikes
- Does NOT appear in clean/active military bases — only in degraded environments

---

## Interaction Type
**Static** — No interaction. Solid cover object.

---

## Visual Description

| Property | Detail |
|---|---|
| Shape | Broken rectangular column. Bottom section intact (0–1.5 tiles tall). Top is fractured — jagged diagonal break. Optional rubble pile at base. |
| Material | Reinforced concrete — same material language as ConcreteWallSegment but showing older, more severe damage |
| Color | Base concrete (#484644). Exposed rebar: dark rust-orange (#7A4A28). Fracture face: lighter raw concrete (#6A6460). Rubble chips at base: match wall color. |
| Size | 0.5 tile footprint (square column). 1.5 tile tall (from ground to jagged break). Two variants: tall break (1.5 tile) and stub (0.75 tile). |
| Silhouette | Vertical narrow rectangle with an irregular jagged top — unmistakably a broken pillar. Thin and distinctive, does not confuse with wall. |
| Details | Rebar strands exposed at the break — 2–3 bent rods angling outward. Diagonal crack lines running up the lower section. Rubble chips scattered at the base (small separate sprite or baked into base sprite). Dark staining near the base. |

---

## Damage Behavior
**Not destructible.** Already ruined — this is a final destroyed state used as static geometry. No further damage states needed. A tank can drive through it only if the level designer uses the passable collision layer variant (see Technical Constraints).

---

## Collision Type
**Full block** (default). Optional: **partial block** variant with narrower collision (0.3 tile wide) that allows vehicles to clip the edge.

---

## Animation Needs
**None.** Static sprite only.

---

## Technical Constraints
- Two height variants needed: tall (1.5 tile height, 0.5 tile footprint) and stub (0.75 tile height, 0.5 tile footprint)
- Rebar exposure at top break must not look like a weapon — keep it structural and clearly architectural
- Must read as "ruined" not "functional" — no clean edges at the break point
- Footprint is narrow (0.5 tile) so PolygonCollider2D must be correctly sized to not over-block player movement
- Rubble at base can be a separate sprite layered at a lower Y sort order to appear on the ground
