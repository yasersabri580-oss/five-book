# NOTES — POWER NODE

---

## Unity Integration

### Component Setup
- **Prefab:** `PowerNode_South.prefab` and `PowerNode_East.prefab`
- **Components:**
  - `SpriteRenderer` — current state sprite (or LED child SpriteRenderer setup)
  - `Animator` — manages LED pulse loop and state transitions
  - `InteractableComponent` — prompt: "Hold [E] to Hack", hold duration: 1.0s, fires `OnNodeHacked`
  - `HealthComponent` — 30 HP
  - `DestructibleController` — swaps to destroyed sprite at 0 HP, fires `OnNodeDestroyed`
  - `LinkedSystemsController` — fires `OnSubsystemDisabled` to linked turret/door/light on `OnNodeDestroyed` or `OnNodeHacked`
- **No collider** — the node is flush against the wall, player walks close to the wall without colliding with the node itself. The wall behind it provides the collision.

### Hack vs Destroy
| Action | Effect | Duration |
|---|---|---|
| Hacked (E key) | Linked system disabled temporarily (10s) | Temporary — system reactivates |
| Destroyed (0 HP) | Linked system disabled permanently | Permanent — unless engineer restores (story event) |

### Wall Placement
- The power node is always placed as a child of the wall GameObject in the scene, or placed manually at the wall face
- In the editor: snap the power node to the wall face surface. The 0.1 tile depth protrusion must not overlap the wall collision box.
- The cable sprites (hugging the wall surface) are separate flat sprites placed on the wall face at a slightly higher sort order — art team delivers cables as a separate static sprite that runs along the wall.

### Sorting Layer
- **Sorting Layer:** `Environment`
- **Order in Layer:** Y-sorted. The power node renders above the wall (it is in front of the wall surface).

---

## Pivot
- **Pivot:** Back-center of the housing (where the housing touches the wall surface) — center horizontally, at the wall contact point
- This allows the node to be placed by positioning the pivot on the wall face

---

## Scale Consistency
- The power node (0.4×0.5 tile) is deliberately small — it is infrastructure, not a prominent gameplay object
- Players who explore and pay attention notice power nodes and can interact with them
- The LED glow (amber) must be visible at game camera zoom — test at standard game zoom level

---

## Reuse Possibilities
- **Rift faction node:** Same housing shape with a cyan LED (#20C480) instead of amber and a Rift faction mark instead of FORGE triangle — used in player-controlled or friendly infrastructure areas
- **Power node cluster:** 3–4 power nodes grouped on a wall panel together with cable connections between them — creates a "server/distribution panel" look using multiple node sprites + connecting cable sprites. No new art needed.
- **Destroyed node as dressing:** A pre-destroyed power node (using `powernode_destroyed.png`) placed as static non-interactive scenery in already-cleared areas — communicates that others fought here before the player.
