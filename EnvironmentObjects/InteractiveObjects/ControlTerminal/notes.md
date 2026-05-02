# NOTES — CONTROL TERMINAL

---

## Unity Integration

### Component Setup
- **Prefab:** `ControlTerminal.prefab`
- **Components:**
  - `SpriteRenderer` — housing (static)
  - `SpriteRenderer` (child) — screen layer (animated via Animator)
  - `Animator` — manages screen state machine
  - `BoxCollider2D` — 0.8×0.6 tile partial blocker (player cannot walk through terminal)
  - `InteractableComponent` — holds prompt text ("Hold E to Hack"), hold duration (1.5s), fires `OnInteracted` event
  - `TerminalController` — receives `OnInteracted` event, fires linked events (door open, turret disable, etc.), transitions screen to Used state

### Screen as Separate Child Sprite
- The screen is a separate child `SpriteRenderer` on the prefab
- This allows the animated screen to be handled by the Animator independently of the housing sprite
- The screen child object is positioned at the terminal's face/screen location in isometric space
- **Blend mode for screen glow:** Use Unity's `Additive` blend mode on the screen SpriteRenderer for a natural glow bleed effect — no additional glow shader needed

### Animator State Machine
| State | Clip | Transition |
|---|---|---|
| `screen_idle` | 4-frame loop | → `screen_interacting` when `StartInteract` trigger fires |
| `screen_interacting` | 4-frame loop | → `screen_used` when `InteractComplete` trigger fires; → `screen_idle` when `InteractCancel` fires |
| `screen_used` | Static sprite | No exit (terminal is permanently used in Chapter 1) |
| `screen_off` | Static sprite | → `screen_idle` when `TerminalRestore` fires (after 5s EMP disable) |

---

## Pivot
- **Pivot:** Bottom-center of the terminal footprint (0.8×0.6 tile base)
- Wall-mounted variant: pivot at the back-center base (the wall face connection point)

---

## Scale Consistency
- Terminal (1.0 tile tall) is shorter than a security door (1.8 tiles) and concrete wall (1.5 tiles)
- Players can see over the terminal — it does not block line-of-sight
- Terminal footprint (0.8×0.6) allows the player to approach from multiple angles — do not create a single-approach bottleneck with wall placements around the terminal

---

## Interaction Prompt UI
- When player enters 1.5 tile radius: a floating UI element appears above the terminal reading "Hold [E] to Hack"
- This is a UI/HUD element, NOT part of the terminal sprite — art team does not deliver this
- The prompt disappears when the player moves beyond 1.5 tile range or when the terminal enters Used state

---

## Reuse Possibilities
- **Kael's Mechanical Arm animation:** When interacting with the terminal, Kael's arm should show the "hacking" animation — this is a character animation concern, not a terminal art concern
- **Neutral terminal (non-FORGE):** Remove the FORGE brand bar and change the screen color to amber (#C8A020) for Rift-faction or neutral systems
- **Broken terminal decor:** A static version of the Off state with additional physical damage (cracked screen, housing dent) used as level dressing in already-cleared areas — no behavior
- **Data-only terminal:** A smaller terminal (0.5×0.4 tile) used only for intel pickups — no door linking, simpler interaction
