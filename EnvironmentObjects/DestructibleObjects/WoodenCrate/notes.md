# NOTES — WOODEN CRATE

---

## Unity Integration

### Component Setup
- **Prefab:** `WoodenCrate.prefab`
- **Components:**
  - `SpriteRenderer` — displays current damage state sprite
  - `BoxCollider2D` — 0.8 tile footprint, disabled on destruction
  - `DestructibleController` script — tracks HP, triggers sprite swap and destruction event
  - `HealthComponent` — 60 HP (light — destroyed by rifle fire in ~10 hits or one grenade)
- **Loot variant:** A secondary prefab `WoodenCrate_Loot.prefab` has a `LootSpawner` component that spawns an `AmmoPickup` at the crate's position on the `OnDestroyed` event

### Sorting Layer
- **Sorting Layer:** `Environment`
- **Order in Layer:** Y-sorted dynamically
- Destroyed decal: `Ground` layer, `Order in Layer: 5` (renders above floor tile, below all objects)

---

## Pivot
- **Pivot:** Bottom-center of the 0.8×0.8 tile footprint
- The crate is slightly smaller than a full tile — do not center it in the tile automatically; place it manually in the scene

---

## Scale Consistency
- Crate (0.8 tile) should be noticeably shorter and smaller than the ConcreteBlock (1 tile footprint, 1.2 tile tall)
- Double-stack crate (1.6 tiles tall) is taller than the ConcreteBlock — visual landmark for "big destructible pile"
- Crates should feel lighter/flimsier than metal objects — the warm wood color palette helps communicate material fragility

---

## Reuse Possibilities
- **FORGE-branded crate:** Same sprite with a different stencil — replace "FORGE ARMS CO." with "RIFT SUPPLY" for friendly supply areas, or leave stencil off for neutral warehouse filler
- **Burnt crate:** A dark-tinted (desaturated, charred wood black) version of the damaged or destroyed decal — placed in already-destroyed areas as permanent scenery, not a gameplay object
- **Crate palette variants:** A green metal version of the same box shape → becomes the SupplyBox prop (see UtilityProps). Same geometry, different material — design efficiency.
- **Stack of three:** A triple-stack (2.4 tiles tall) can serve as a tall visual landmark or impassable stack — no new art, just three crate prefabs stacked in the scene
