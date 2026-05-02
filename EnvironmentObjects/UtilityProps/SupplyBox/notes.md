# NOTES — SUPPLY BOX

---

## Unity Integration

### Component Setup
- **Prefabs:** `SupplyBox_FORGE.prefab` and `SupplyBox_Rift.prefab`
- **Components:**
  - `SpriteRenderer` — current state sprite
  - `Animator` — manages lid-open animation and state transitions
  - `BoxCollider2D` — 0.9×0.7 tile partial blocker
  - `InteractableComponent` — prompt: "Press [E] for Ammo", instant interaction (no hold), fires `OnSupplyUsed`
  - `SupplyBoxController` — on `OnSupplyUsed`: triggers lid-open animation, fires `PlayerAmmo.Resupply()`, transitions to depleted state (no further interaction possible)

### Ammo Resupply Logic
- `PlayerAmmo.Resupply()` fills all current weapon ammo to maximum
- If the player is fully stocked (all ammo already full): the box still opens (animation) but no ammo is given. The `InteractableComponent` should hide the E prompt when the player is fully stocked (to avoid wasting the box).
- This is handled by `SupplyBoxController` checking `PlayerAmmo.NeedsResupply()` on approach

### Animator State Machine
| State | Clip | Transition |
|---|---|---|
| `box_closed` | Static — closed sprite | → `box_opening` when `OnSupplyUsed` fires |
| `box_opening` | 3-frame clip, plays once | → `box_open` when clip ends |
| `box_open` | Static — open sprite | Held indefinitely |

### Sorting Layer
- **Sorting Layer:** `Environment`
- **Order in Layer:** Y-sorted

---

## Pivot
- **Pivot:** Bottom-center of the 0.9×0.7 tile footprint
- The supply box is lower and wider than the WoodenCrate — do not confuse their pivots when placing both in the same scene

---

## Scale Consistency
- Supply box (0.9×0.7×0.6 tile) vs WoodenCrate (0.8×0.8×0.8 tile): supply box is wider, deeper, but shorter
- The different silhouette (wide/low vs square/tall) is crucial for player distinction at a glance — never place them immediately adjacent to each other

---

## Faction Variant Selection
| Level Context | Prefab to Use |
|---|---|
| FORGE-controlled facility | `SupplyBox_FORGE.prefab` (green) |
| Rift safehouse / friendly zone | `SupplyBox_Rift.prefab` (grey) |
| Neutral / abandoned area | Either variant, but consistently one or the other per zone |
| Do NOT mix FORGE and Rift boxes in the same room | Narrative inconsistency |

---

## Interaction Flow (Player Experience)
1. Player enters 1.5 tile proximity → "Press [E] for Ammo" prompt appears above the box
2. Player presses E → lid-open animation plays (0.2s) + ammo resupply fires
3. Ammo resupply feedback shown in UI (weapon ammo counter flashes full)
4. Box holds in open state → prompt disappears → box is permanently depleted

---

## Reuse Possibilities
- **Empty box (pre-looted):** The open/depleted sprite with no `InteractableComponent` or `SupplyBoxController` — placed as static scenery in areas the player is supposed to understand were already looted before they arrived. Narrative use.
- **Medical supply variant:** Same box, white/red cross markings (#C42020 cross on light grey box face) — functions identically but restores HP instead of ammo. Reuses the entire prefab and animation. Change stencil art and swap `SupplyBoxController` resupply type.
- **Weapon cache:** A third variant with orange markings and a grenade stencil — grants a grenade or special weapon pickup. Same prefab structure. Orange palette (#C86010 body, grenade silhouette stencil).
- **Large supply crate:** The same box art at 2× scale (1.8×1.4 tile) for major supply cache scenes — provides 2 resupply uses before depleting.
