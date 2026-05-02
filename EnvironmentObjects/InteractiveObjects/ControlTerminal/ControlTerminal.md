# OBJECT PROFILE — CONTROL TERMINAL

---

## Object Name
**ControlTerminal**

---

## Category
Interactive Objects

---

## Gameplay Purpose
Primary interactive object for player hacking and mission-critical actions. Players approach and hold E (1.5s) to interact, triggering effects such as: opening security doors, disabling turrets, downloading data, or activating/deactivating systems. The control terminal is the player's primary tool for engaging with FORGE-controlled infrastructure. It must look obviously interactive (screen glow, prompt appears on approach) and clearly show whether it is active, disabled, or already used.

---

## Where It Is Used
- FORGE-controlled facilities: server rooms, command centers, power stations
- Alongside SecurityDoors (as the unlock mechanism)
- In objective areas (mission-critical terminals that must be hacked to complete objectives)
- Standalone in patrol areas (optional terminals that give intel pickups)

---

## Interaction Type
**Usable** — Player presses and holds E for 1.5s on approach. Progress bar shown in UI. On success: linked event fires. Terminal changes to "used" state.

---

## Visual Description

| Property | Detail |
|---|---|
| Shape | Wall-mounted or freestanding terminal unit. Freestanding: angular console desk with angled screen. 0.8 tiles wide × 0.6 tiles deep × 1.0 tile tall. Screen angled at 30° face-up from vertical. |
| Material | Matte black hard plastic housing (#1A1E22). Screen: flat panel with lit display. Metal frame around screen: dark gun-metal (#2A2E32). |
| Color | Housing: #1A1E22 (near-black). Active screen: cyan-green glow (#20C480) with grid/data display. Inactive screen: dark grey (#2A2E30). FORGE branding bar across the top panel: dark red (#6A1010). |
| Size | 0.8×0.6 tile footprint. 1.0 tile tall. |
| Silhouette | Angled console desk with screen. Clearly a computer terminal. |
| Details | Screen displays a simplified data grid / map pattern — abstract lines suggesting code or map data. FORGE brand bar at top with small logo. 2–3 indicator LEDs on the housing (small dots: green active, red inactive). Keyboard panel below screen (implied via a horizontal flat panel, no individual keys visible at game scale). Cable running down the back. |

---

## Damage Behavior
**Not destructible.** Terminals are hardened FORGE hardware. If a grenade lands within 1 tile, the terminal screen goes dark (temporarily disabled for 5s) — handled by game code via a `screen_off.png` sprite state, not a damage system. The terminal housing is not physically damaged.

---

## Collision Type
**Partial block** — 0.8×0.6 tile footprint box collider. Player cannot walk through the terminal.

---

## Animation Needs
**Required:** Screen idle animation (ambient data scroll), active/interacting state (screen brightens, progress indication), used state (screen dims to a solid checkmark or "ACCESS GRANTED" display), and disabled state (screen off).

---

## Technical Constraints
- Screen glow must be readable in both bright and dark level lighting — the cyan glow is the primary readability cue
- The player interaction prompt ("Hold E to Hack") appears as UI above the terminal when player is within 1.5 tiles — this is a UI element, not part of the terminal sprite
- Two variants: freestanding (standard) and wall-mounted (flat against a wall, smaller footprint) — wall-mounted is a separate sprite with 0.3 tile depth
- Screen data pattern must look like FORGE system data but be abstract — no readable text, no real-world UI elements
