# NOTES — FUEL TANK

---

## Unity Integration

### Component Setup
- **Prefab:** `FuelTank.prefab`
- **Components:**
  - `SpriteRenderer` — current state sprite
  - `BoxCollider2D` — 1.0×0.6 tile, full block
  - `HealthComponent` — 80 HP
  - `DestructibleController` — swaps to leaking sprite at 40 HP, triggers fire event at 0 HP
  - `FireHazardComponent` — on `OnDestroyed`: spawns fire VFX, creates 2-tile burn zone (8s duration, 5 damage/sec), swaps to burnt sprite

### Orientation Handling
- South-facing (default): `FuelTank.prefab` — cylinder east-west
- East-facing: `FuelTank_East.prefab` — cylinder north-south
- These are separate prefabs with separate sprites — do NOT rotate the south-facing prefab to get the east-facing orientation (the isometric perspective would be wrong)

### Sorting Layer
- **Sorting Layer:** `Environment`
- **Order in Layer:** Y-sorted

---

## Pivot
- **Pivot:** Bottom-center of the 1.0×0.6 tile footprint (at the base of the saddle support legs)
- For east-facing variant: pivot at the bottom-center of the 0.6×1.0 tile footprint (swapped dimensions)

---

## Scale Consistency
- Fuel tank (0.7 tile tall) is shorter than the explosive barrel (0.9 tile) — the horizontal profile makes it feel lower and heavier
- The 1.0 tile width makes it the widest single-unit prop in the UtilityProps category
- The fuel tank must not be confused with the explosive barrel: fuel tank = horizontal, green, fire hazard; explosive barrel = vertical, red, explosion hazard

---

## Readability vs Explosive Barrel
- These two objects must be visually distinct at a glance and should never be placed near each other:
  - ExplosiveBarrel: VERTICAL, RED, EXPLODES
  - FuelTank: HORIZONTAL, GREEN, BURNS
- The color difference (red vs green) and shape difference (vertical vs horizontal cylinder) provide the visual distinction

---

## Reuse Possibilities
- **Water tank:** Same cylinder shape and saddle supports, painted light grey (#8A9090) with a blue water stencil. No hazard. Purely decorative or for environmental storytelling. No damage behavior.
- **Large fuel storage tank:** A 2×1 tile version (double-length cylinder) for major fuel depot areas — same art family, larger sprite.
- **Fuel tank trailer (vehicle prop):** The fuel tank cylinder attached to a trailer base — a separate combined prop for motor pool scenes, using the same cylinder art.
