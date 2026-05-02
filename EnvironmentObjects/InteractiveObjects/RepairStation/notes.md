# NOTES — REPAIR STATION

---

## Unity Integration

### Component Setup
- **Prefab:** `RepairStation.prefab`
- **Components:**
  - `SpriteRenderer` — housing and state sprite
  - `Animator` — manages the healing pulse animation and state transitions
  - `BoxCollider2D` — 0.9×0.5 tile partial blocker
  - `InteractableComponent` — prompt: "Hold [E] to Repair", hold duration: 2.0s, fires `OnHealUsed`
  - `RepairStationController` — tracks remaining uses (1 or 2, set per prefab variant), handles heal dispatch, transitions state sprites

### Heal Event
- `RepairStationController.OnHealUsed` fires:
  1. `PlayerHealth.Heal(40)` (or `TankHealth.Repair(40)` if player is mounted)
  2. Decrements remaining use counter
  3. Triggers appropriate sprite/animator state transition

### Variants
- `RepairStation_1Use.prefab` — single use (starts at Full, goes to Depleted after 1 heal)
- `RepairStation_2Use.prefab` — two uses (Full → OneUse → Depleted)

### Sorting Layer
- **Sorting Layer:** `Environment`
- **Order in Layer:** Y-sorted

---

## Pivot
- **Pivot:** Bottom-center of the 0.9×0.5 tile footprint
- The access panel (south face) always faces south — do not rotate this prefab; use the wall-mounted variant for wall placement

---

## Scale Consistency
- Station (1.2 tiles tall) is taller than wooden crate (0.8) and shorter than security door (1.8)
- The olive-green cabinet with red cross must stand out from the grey/brown environment color palette — do not place the station against a green wall or in an area with similar hues

---

## Placement Guidelines (for Level Designers)
- Always give the player a visible line of sight to the station before they need it — do not hide it behind a wall where it can only be found by chance during a fight
- Place after a difficult combat encounter (before or after), never in the middle of an active enemy patrol zone
- A depleted repair station is a valid environmental narrative element — it tells the player this area has been fought through before

---

## Reuse Possibilities
- **Tank repair station:** Same cabinet art with different branding. A large vehicle-sized repair platform (2×2 tile) that uses the same repair station design language — a red cross on a larger industrial frame — can be built from the same visual components
- **Ammo resupply variant:** Same cabinet body and indicator light system, but with yellow/orange branding and a bullet icon instead of the red cross. Functions as an ammo restock point — reuses the entire cabinet art pipeline
- **Hostile sabotage:** A repair station that has been sabotaged by FORGE (screen cracked, red cross crossed out with a FORGE stencil) — appears in certain missions as a trap. No heal provided. Same base sprite + overlay.
