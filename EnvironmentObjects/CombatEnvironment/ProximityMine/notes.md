# NOTES — PROXIMITY MINE

---

## Unity Integration

### Component Setup
- **Prefab:** `ProximityMine.prefab`
- **Structure:**
  - Root: `ProximityMine` (no collider — mine is walked over)
    - Child: `Minebody` — `SpriteRenderer` + `Animator` (mine body + LED, or LED as separate child)
    - Child: `ProximityTrigger` — `CircleCollider2D` (IsTrigger: true, radius 0.5 tile). This is the detection zone.
- **Components:**
  - `ProximityMineController` — handles trigger enter, armed/triggered/explode state machine
  - `HealthComponent` — 1 HP (one bullet destroys it safely — detonates without proximity trigger if shot)
  - `ExplosionComponent` — radius: 1.5 tile, damage: 60, team: neutral (damages everyone)

### State Machine
| State | Condition | Behavior |
|---|---|---|
| Armed | Default | LED slow pulse animation loop |
| Triggered | Player/enemy enters ProximityTrigger | LED rapid flash, play warning audio, 0.8s countdown |
| Exploded | Countdown ends OR HP = 0 | Remove sprite, fire ExplosionComponent, place scorch decal |
| Disarmed | EMP pulse within range | LED off (mine_disarmed.png), disable ProximityTrigger and HealthComponent |

### Sorting Layer
- **Sorting Layer:** `Ground`
- **Order in Layer:** 10 (above floor tile, below all environment objects and characters)
- Mine MUST be on the Ground layer — it is a floor-level object. Infantry sprites render above it.

---

## Pivot
- **Pivot:** Center of the mine disc (center-center)
- Position in scene by placing the center of the mine at the intended ground point

---

## Scale Consistency
- The mine (0.3 tile) is the smallest interactive object in the pipeline
- At 0.3 tile, the mine is approximately 20–25 px wide at standard game resolution — this is intentionally small
- The LED glow halo (when at peak brightness) should be the most visually prominent element at game scale
- Test at actual game resolution to verify the LED is visible at normal camera zoom levels

---

## LED as Separate Sprite Layer
- The LED animation is only 2 frames — but driving the entire mine sprite animation for just a few pixels of LED change is wasteful
- Recommended: Place the LED as a child `SpriteRenderer` overlaid exactly on the LED position
- The `Animator` on the LED child handles only the LED flash/pulse animation (2-frame loop)
- Additive blend mode on the LED child SpriteRenderer creates a natural glow effect

---

## Placement Guidelines (for Level Designers)
- Never place a mine on the player's only possible path without a visual warning cue (a warning sign, a visible body of a soldier who stepped on one, audio cue in Rina's radio dialogue)
- Place in groups of 2–3 for a "minefield" feeling — single mines are used as traps
- Half-hidden variant (`mine_halfhidden.png`) used in outdoor minefields — standard variant used indoors
- A safe detonation corridor (path between mine trigger zones) must always exist for a skilled player to navigate without triggering

---

## Reuse Possibilities
- **Anti-vehicle mine:** Larger disc (0.5 tile), only triggered by vehicle weight (separate trigger layer). Same art approach, larger and slightly more prominent.
- **Deployable mine (player-placed):** If future design adds player mine deployment, the same art is reused with a green LED (#20C440) indicating a friendly mine. No new base art needed.
