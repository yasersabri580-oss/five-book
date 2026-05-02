# NOTES — EXPLOSIVE BARREL

---

## Unity Integration

### Component Setup
- **Prefab:** `ExplosiveBarrel.prefab`
- **Components:**
  - `SpriteRenderer` — current state sprite
  - `CircleCollider2D` — radius 0.25 tile (matches 0.5 tile footprint), disabled on explosion
  - `DestructibleController` — HP: 30. Triggers `OnExplode` event at 0 HP
  - `ExplosionComponent` — radius: 3 tiles, damage: 80, team: neutral (damages everyone). Fires on `OnExplode`.
  - `HealthComponent` — 30 HP
- **Double-barrel prefab:** `ExplosiveBarrel_Double.prefab` — two `ExplosiveBarrel` prefabs parented to an empty root, positioned side by side. Each barrel explodes independently.

### Chain Explosions
- Two barrels within 3 tiles of each other will chain-explode: one explosion damages the adjacent barrel, triggering a second explosion
- Ensure level designers are aware: never place 3+ barrels within chain range unless that chain explosion is intentional

### Sorting Layer
- **Sorting Layer:** `Environment`
- **Order in Layer:** Y-sorted

---

## Pivot
- **Pivot:** Bottom-center of the barrel footprint (0.5 tile footprint, center bottom)
- Because the barrel is narrower than a standard tile, always manually adjust position when placing — do not auto-snap to tile center unless intentional

---

## Scale Consistency
- A single barrel (0.5 tile footprint) is visibly slimmer than a wooden crate (0.8 tile) — this is intentional for visual hierarchy: barrel is the most dangerous-looking small object
- The barrel height (0.9 tiles) should be slightly shorter than the ConcreteWallSegment (1.5 tiles) but taller than the wooden crate (0.8 tiles)

---

## Readability Rule
- The explosive barrel's red color MUST stand out in any level. Do NOT place other red objects near a barrel (e.g., no red lights, red wall markings) that could reduce the visual signal clarity of the barrel's danger.
- The barrel must be the reddest object in any scene it appears in.

---

## Reuse Possibilities
- **Water / Oil drum non-explosive:** Same barrel shape but painted industrial blue-grey (#3A4A6A) with no hazard stripes. Used as decorative utility prop (see FuelTank for a related variant). No explosion behavior.
- **Stacked barrels (horizontal):** The same barrel sprite rotated 90° and placed on its side — a separate static sprite showing a barrel lying on its side (not a physics simulation). Useful for loading dock dressing.
- **Empty barrel:** A dull grey (#4A4A48) single barrel with open top (no bung holes) — used as scenery near destroyed areas with no explosive behavior.
