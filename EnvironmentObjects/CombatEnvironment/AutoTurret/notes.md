# NOTES — AUTO TURRET

---

## Unity Integration

### Component Setup
- **Prefab:** `AutoTurret.prefab`
- **Structure:**
  - Root GameObject: `AutoTurret` (holds BoxCollider2D, TurretAIController)
    - Child: `TurretPedestal` — `SpriteRenderer` with `turret_pedestal.png`, static
    - Child: `TurretBody` — `SpriteRenderer` + `Animator`, rotated by TurretAIController
- **Components:**
  - `BoxCollider2D` (on root) — 0.5 tile footprint circle (use CircleCollider2D), blocks movement
  - `TurretAIController` — manages scan behavior, player detection, rotation, fire logic
  - `HealthComponent` — 120 HP
  - `DestructibleController` — swaps `TurretBody` sprite on damage thresholds, fires `OnDestroyed`

### Turret AI Behavior
| State | Condition | Behavior |
|---|---|---|
| Scanning | No target in range | Rotates body left–right over scan arc (120°), 0.8 complete sweeps/second |
| Tracking | Player detected in arc | Rotates body toward player at 180°/sec, plays idle lens pulse |
| Firing | Player locked (0.3s lock delay) | Fires 2-shot burst, then 0.4s cooldown |
| Disabled | EMP hit or terminal hack | Stops all behavior, body points neutral, lens dims. Duration: 3s (EMP), permanent (terminal). |
| Destroyed | HP = 0 | All behavior stops. Spawns hit VFX. Swaps to destroyed sprite. |

### TurretBody Sprite Rotation
- The `TurretBody` Transform is rotated in 2D (Z-axis) by the AI controller
- The sprite is drawn in the south-facing orientation — Unity rotation handles all directions
- Note: Isometric depth distortion at extreme angles is acceptable (this is a 2.5D tradeoff)

### Sorting Layer
- **Sorting Layer:** `Environment`
- **Pedestal order:** Y-sorted (base)
- **TurretBody order:** +1 above pedestal (always renders on top of pedestal regardless of Y)

---

## Pivot
- **Pedestal pivot:** Bottom-center of the 0.5 tile circular base
- **TurretBody pivot:** Center of the turret housing (the rotation center — where the body pivots on the pedestal mounting ring)

---

## Scale Consistency
- The auto turret is deliberately low-profile (0.7 tiles tall total) — it should not tower over infantry
- The twin barrels are the widest element (extend 0.4 tile forward of the housing) — they should visually "point at" the player during tracking, reinforcing the threat

---

## Detection Arc Visualization (Editor Only)
- Add a `TurretArcGizmo` editor component that draws the 120° detection arc in the Scene view
- This is a development tool only — not visible in-game

---

## Reuse Possibilities
- **Heavy turret:** Same pedestal, larger turret body (0.8 tile wide) with a single large barrel instead of twin. Higher HP (200), slower rotation, wider fire damage. Uses the same turret body art at 1.5× scale.
- **Mounted turret (vehicle):** The `TurretBody` sprite is the same art used on enemy tank turrets — design consistency means the FORGE visual language is coherent across turrets and tanks.
- **Disabled turret (level dressing):** An already-destroyed or already-disabled turret placed as static scenery using `turret_body_destroyed.png` + pedestal, no components — just SpriteRenderers.
