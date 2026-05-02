# NOTES — CONCRETE WALL SEGMENT

---

## Unity Integration

### Component Setup
- **Component:** `SpriteRenderer` on a static `GameObject` tagged `Environment_Static`
- **Tilemap:** Use Unity's isometric Tilemap for wall placement. Create an `EnvironmentWall` Tilemap layer.
- **Tile Asset:** Create a `Tile` asset for each variant (straight, corner, T-cap) in the Unity Tilemap system
- **Physics:** Attach a `CompositeCollider2D` on the Tilemap with `TilemapCollider2D` — set to full block

### Sorting Layer
- **Sorting Layer:** `Environment`
- **Order in Layer:** Calculated dynamically by Y position (isometric Y-sort). Walls always render above floor tiles.

---

## Pivot
- **Pivot:** Base-center of the isometric tile footprint (horizontal center, bottom of sprite bounding box)
- In Unity Sprite Editor: set pivot to **Bottom Center** then adjust Y slightly up to the base of the 3D slab (not the very bottom of the drop shadow)

---

## Scale Consistency
- All wall segments must share the exact same pixel height and tile alignment
- Do not resize wall sprites in the Unity scene — scale is 1:1 from the sprite
- Pixel-per-unit setting: match the project-wide setting (defined in master art spec)
- A wall segment's top must visually align with the top of adjacent wall segments when placed side-by-side

---

## Tiling Rules
- Left edge and right edge of `wall_straight.png` must match exactly — test by duplicating and placing side-by-side in Unity
- Corners and T-caps must visually close the gap between perpendicular wall runs without overlap artifacts

---

## Reuse Possibilities
- **Damage decal overlay:** Apply a separate cracked-concrete decal sprite on top of the wall (on a higher sorting order sub-layer) when a tank shell impacts. The decal is a separate asset, not a wall variant.
- **Recolor variants:**
  - Rust-stained version (#5A3A28 grime) for older industrial zones
  - Mossy version (#3A4A30 green tint on grime) for exterior/abandoned levels
  - These require only a texture overlay pass — same geometry sprite
- **Sandbag topper:** A separate SandbagTopper prop sprite can be placed on top of a wall run to create a fortified-wall look without creating a new wall type

---

## Known Gotchas
- Isometric walls at the player's Y level may clip character sprites — ensure wall collider stops at the tile edge, and use the Z-sort system to handle visual layering correctly
- Do not use the concrete wall for destructible geometry — use `WeakWallSection` for that purpose
