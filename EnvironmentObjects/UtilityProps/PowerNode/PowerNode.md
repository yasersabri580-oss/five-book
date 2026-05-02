# OBJECT PROFILE — POWER NODE

---

## Object Name
**PowerNode**

---

## Category
Utility Props

---

## Gameplay Purpose
Secondary power distribution point for FORGE systems. Unlike the main Generator (which powers an entire area), a power node powers a single subsystem — one turret, one security door, or one set of lights. Destroying a power node disables its linked subsystem without triggering a large explosion. This gives players a quieter, more surgical option than destroying the main generator. Power nodes are also mission intel targets (hacking a power node via its small control interface can give the player a map overlay of linked system locations). Visually, power nodes help tell the story of FORGE's infrastructure.

---

## Where It Is Used
- Throughout FORGE-controlled facilities: on walls, in corridors, near turret emplacements
- Typically wall-mounted (not freestanding) — they are infrastructure, not equipment
- Often placed in secondary/hidden locations that reward exploring players

---

## Interaction Type
**Destructible / Usable** — Can be destroyed by gunfire (low HP), disabling linked system. Can also be interacted with by Kael's mechanical arm (E key, 1.0s hack) to temporarily disable or repurpose the linked system.

---

## Visual Description

| Property | Detail |
|---|---|
| Shape | Wall-mounted rectangular unit. 0.4 tile wide × 0.1 tile deep (flat against wall) × 0.5 tile tall. A distribution box with cables entering and exiting. |
| Material | Dark metal housing, painted FORGE dark grey. Small screen/LED panel on the front face. Cable conduits entering from top and exiting from bottom. |
| Color | Housing: dark #1E2228. LED panel: small screen with amber (#C8A020) or cyan (#20C480) readout. Power indicator light: small bright dot (green when active, red when disabled). Cable conduits: dark grey (#2A2A28). |
| Size | 0.4 tile wide × 0.1 tile deep × 0.5 tile tall. Flat wall-mounted box. |
| Silhouette | Flat rectangular box on a wall. Small, functional, clearly technological. |
| Details | 2 cable conduits entering from the top. 2 cables exiting from the bottom (one runs left along the wall, one runs right — suggesting the distribution network). A small LED panel in the center of the front face (5×3 px in game): amber glow with minimal data lines. One power indicator LED (bright green circle). FORGE triangle mark on the housing. Small number plate (node ID) — a dark plaque with no readable text. |

---

## Damage Behavior

**Two states:**

| State | HP | Visual |
|---|---|---|
| Active | 30 HP | Normal — LED amber glow, indicator green |
| Destroyed | 0 HP | Housing cracked/scorched, LED dark, indicator off. Static destroyed sprite. Linked system disabled. |

No intermediate damage state needed (low HP unit — either active or destroyed).

---

## Collision Type
**None** — Power nodes are wall-mounted and do not extend far enough into the play area to create meaningful collision. Players can walk close to the wall without collision from the node.

---

## Animation Needs
**Minimal:** LED idle pulse (2-frame loop, amber glow slightly brightens and dims). Static on all other states.

---

## Technical Constraints
- Wall-mounted: the node is always placed against a wall face. It does not exist as a freestanding object.
- Two wall orientations: south-wall-mounted (visible from south camera) and east-wall-mounted (visible from east camera — darker face)
- The LED readout and indicator light must be visible at small size (the node is small — 0.4×0.5 tile)
- Cable conduits entering/exiting the node must visually connect to the wall surface they are mounted on — no floating cables
