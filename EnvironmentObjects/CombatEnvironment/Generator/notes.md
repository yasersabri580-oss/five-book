# NOTES — GENERATOR

---

## Unity Integration

### Component Setup
- **Prefab:** `Generator.prefab`
- **Structure:**
  - Root: `Generator` (BoxCollider2D, DestructibleController, HealthComponent)
    - Child: `GeneratorBody` — `SpriteRenderer` (static body)
    - Child: `ExhaustShimmer` — `SpriteRenderer` + `Animator` (4-frame shimmer loop)
    - Child: `AmberLight` — `SpriteRenderer` + `Animator` (amber strip; flicker in damaged state)
- **Components:**
  - `BoxCollider2D` (on root) — 1.5×1.0 tile full block, remains after destruction (wreck still blocks movement)
  - `HealthComponent` — 300 HP
  - `DestructibleController` — triggers sprite swaps at HP thresholds, fires `OnDestroyed`
  - `ExplosionComponent` — radius: 4 tiles, damage: 120, team: neutral. Fires on `OnDestroyed`.
  - `LinkedSystemsController` — fires `OnSystemDisabled` event to all linked turrets, doors, and lights when `OnDestroyed` is called

### Linked Systems
- The generator is linked to other objects in the level via the `LinkedSystemsController`
- Turrets and security doors reference the generator's `LinkedSystemsController`
- When the generator is destroyed, all linked objects receive the `OnSystemDisabled` event and switch to their disabled states
- Level designers link objects in the Unity Inspector — no hardcoded references

### Sorting Layer
- **Sorting Layer:** `Environment`
- **Order in Layer:** Y-sorted (the generator is a large high-value object)
- `ExhaustShimmer` child: `Order in Layer: +2` above body (renders above the generator body)
- `AmberLight` child: same order as body or +1 (light renders on the body face)

---

## Pivot
- **Pivot:** Bottom-center of the 1.5×1.0 tile footprint (center of the base)
- Because the generator is asymmetric (engine left, control right), the pivot is at the geometric center of the total footprint, not the visual center — verify grid alignment when placing

---

## Scale Consistency
- The generator (1.5×1.0 tile, 1.2 tile tall) is the largest object in the environment pipeline
- It should visually dominate any room or area it occupies — it is a landmark, not background dressing
- The character (Kael Dros at 2.8 tiles) is taller than the generator — but the generator is much wider
- Power cables trailing from the generator must visually connect to something (a wall panel, another prop, or off-screen) — do not leave cables floating in open space

---

## Placement Guidelines (for Level Designers)
- Always place the generator where it is visible from the area entrance — players must be able to see the target before planning their approach
- Ensure there is at least one valid approach path that avoids direct line-of-sight from turrets linked to the generator (the tactical puzzle: attack the generator while the turrets it powers are still active)
- The generator explosion (4 tile radius, 120 damage) is lethal to the player at close range — ensure players have room to retreat before detonation

---

## Reuse Possibilities
- **Smaller power relay:** A 1×0.5 tile version of the generator (the right "control section" only, no engine section) used as a secondary power relay node — same art family, weaker object (100 HP), smaller explosion (2 tile radius)
- **Tank fuel generator:** Same generator art with yellow/amber livery markings instead of FORGE red — for player-friendly or neutral fuel storage areas. No explosion on destruction (just fire VFX).
- **Background industrial dressing:** Non-destructible generator variant (no HP, no explosion, no linked systems) placed as scenery in distant level background sections
