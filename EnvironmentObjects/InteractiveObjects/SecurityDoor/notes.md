# NOTES — SECURITY DOOR

---

## Unity Integration

### Component Setup
- **Prefab:** `SecurityDoor.prefab`
- **Components:**
  - `SpriteRenderer` — current door state sprite
  - `Animator` — controls the open animation and light state transitions
  - `BoxCollider2D` — full block when closed, disabled when open
  - `SecurityDoorController` script — listens for `DoorUnlock` event (fired by ControlTerminal or mission script), triggers Animator
  - `ProximityDetector` — if door is unlocked, opens when player enters 1.5 tile proximity radius

### Orientation Variants
- **South-facing prefab:** `SecurityDoor_South.prefab` — door face visible on south side (main camera-facing)
- **East-facing prefab:** `SecurityDoor_East.prefab` — door face visible on east side (darker face toward camera)
- Level designers place the correct orientation variant based on which wall the door sits in

### Sorting Layer
- **Sorting Layer:** `Environment`
- **Order in Layer:** Y-sorted. While the door is closed, it sorts as a wall-level object. When open, the frame-only sprite sorts below character sprites that walk through the opening.

---

## Pivot
- **Pivot:** Bottom-center of the door opening (at the floor level, centered horizontally in the 1-tile opening)
- The pivot is the same regardless of open/closed state — the animation slides the sprite, not the pivot

---

## Scale Consistency
- Door opening (1 tile wide) must match the ConcreteWallSegment opening perfectly — no pixel gap or overlap
- Door height (1.8 tiles) is taller than a concrete wall segment (1.5 tiles) — the door extends slightly above the standard wall height, communicating that it is a reinforced, heavy installation
- The door frame header is the extra 0.3 tiles above the standard wall height

---

## Indicator Light as Separate Sprite
- The indicator light can be implemented as a **second SpriteRenderer** child object on the door prefab
- This child SpriteRenderer holds the light state sprite (red or green), positioned at the left frame post
- Allows the light to be toggled independently of the door animation
- Add a subtle `SpriteGlow` effect (additive blend mode, low intensity) to the light sprite in engine for the glow effect

---

## Reuse Possibilities
- **Airlock variant:** Same door model but with a different emblem (no FORGE triangle) and a yellow/amber indicator light (#E8A800) for player-controlled airlocks or safe zones
- **Broken door:** A destroyed variant (door bent inward, frame crumpled) used as level dressing in already-cleared or bombed areas — no collision, no behavior, purely decorative
- **Vehicle bay door:** A 2-tile-wide version of the SecurityDoor using the same art language — scale the door horizontally in the sprite, adjust collision to 2 tiles wide
