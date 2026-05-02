# OBJECT PROFILE — REPAIR STATION

---

## Object Name
**RepairStation**

---

## Category
Interactive Objects

---

## Gameplay Purpose
Health restoration point for the player (on foot) or tank (while mounted). The player holds E for 2s at a repair station to restore 40 HP. Stations are limited-use (1 or 2 uses per station, depending on level design intent). This is one of the few reliable healing sources in a level — its placement is a deliberate design choice that affects combat pacing. Players learn to locate repair stations before committing to hard fights. The station must visually communicate: "I can heal here" immediately.

---

## Where It Is Used
- Safe zones before major combat encounters
- Mid-level checkpoints after difficult fights
- Hidden in optional exploration paths as a reward
- Never in areas that are trivially easy — always placed where healing is a meaningful resource

---

## Interaction Type
**Usable** — Player holds E for 2s. Progress bar fills in UI. Station heals 40 HP (or repairs 40 tank HP if player is mounted). After use, station enters a "depleted" state (changes appearance, no further healing). Optional: 2-use variant (resets visual to depleted-1 after first use, fully depleted after second).

---

## Visual Description

| Property | Detail |
|---|---|
| Shape | Industrial medical/repair cabinet. Freestanding unit: 0.9 tiles wide × 0.5 tiles deep × 1.2 tiles tall. Heavy-duty grey-green cabinet with a red cross symbol and a dispenser/access panel on the front face. |
| Material | Powder-coated steel cabinet — matte green-grey (#3A4830). Red cross panel on the front (#C42020 on a lighter grey panel). Indicator light at top of front face. |
| Color | Cabinet body: matte olive-green (#3A4830). Red cross: #C42020. Access panel: light grey (#6A6A68). Indicator light: green (#20C440) when available, amber (#C8A020) when depleted-1-use, off (#1A1A18) when fully depleted. |
| Size | 0.9×0.5 tile footprint. 1.2 tiles tall. |
| Silhouette | Upright cabinet, wider than it is deep. Clearly a supply/medical unit. The red cross is the primary visual signal. |
| Details | Red cross centered on the access panel (front face). Indicator light at top-front center. A small pipe or hose connection at the base-right corner. Cabinet handle on the right side of the access panel. Manufacturer plate at the bottom of the front face (small dark panel, no readable text). Slight dents and wear marks on the cabinet body — this is field equipment, not pristine. |

---

## Damage Behavior
**Not destructible.** The repair station is hardened field equipment. It cannot be damaged or removed by gameplay actions.

---

## Collision Type
**Partial block** — 0.9×0.5 tile box collider. Allows approach from multiple sides.

---

## Animation Needs
**Required:** Active/healing animation (indicator pulses, access panel light brightens during the 2s heal) — 3-frame loop while healing is in progress. Depleted state is a static sprite (no animation).

---

## Technical Constraints
- The red cross must be the first thing the player sees — it must contrast sharply against the olive-green cabinet and the surrounding environment
- The indicator light at the top must clearly distinguish three states: available (green), 1-use-remaining (amber), depleted (off)
- The access panel (where the red cross is) must face south (camera-facing) in all placement scenarios
- Must be clearly different from the WoodenCrate and SupplyBox in silhouette and color — the green/red combination is unique to this object
- Two variants: freestanding (standard) and wall-mounted (attached to a wall, same front face, reduced depth)
