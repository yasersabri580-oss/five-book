# NOTES — ROCK FORMATION

---

## Unity Integration

### Component Setup
- **Component:** `SpriteRenderer` on a static `GameObject` tagged `Environment_Static`
- **Physics:** `PolygonCollider2D` — manually traced to match the irregular rock silhouette base. Do NOT use a box or circle collider.
- For the large (1×2) variant, use a single `PolygonCollider2D` spanning the full base

### Sorting Layer
- **Sorting Layer:** `Environment`
- **Order in Layer:** Y-sorted (dynamic, calculated by Y base position)
- Rocks render above ground tiles and below characters that stand behind them

---

## Pivot
- **Pivot:** Base-center of the total rock cluster bounding box
- Set in Unity Sprite Editor: bottom-center of the sprite, at the point where the rock sits on the ground tile
- For the large variant: pivot at horizontal center of the full 1×2 footprint, vertical bottom

---

## Scale Consistency
- Small, medium, and large variants must be proportionally consistent — medium is visually about 1.5× small, large is about 2.5× small
- Do not resize in the Unity scene — sizes are established at the sprite level
- The small rock should roughly match the height of a sandbag barrier (visual readability of scale hierarchy)

---

## Placement Rules (for Level Designers)
- Always place rocks in clusters — 2–3 objects overlapping slightly creates natural groupings
- Small rocks can be placed in front of medium or large rocks to add depth
- Never place a single isolated medium or large rock in the center of open space — it looks placed, not natural
- Leave at least 0.5 tile gap between rocks and walls to avoid tight stuck-zones for player movement

---

## Reuse Possibilities
- **Rubble pile variant:** Same sprites, slightly darker and more dusty tones, used in ruined/collapsed environments
- **Snow variant:** Add a thin white (#E8E8F0) cap overlay sprite on top of rock — reuses base rock sprite for winter-themed levels
- **Crater edge:** Large rock variant placed at the rim of a crater decal creates bomb-crater geography without custom art
- Used as natural level-edge borders to prevent the playfield from feeling artificially walled
