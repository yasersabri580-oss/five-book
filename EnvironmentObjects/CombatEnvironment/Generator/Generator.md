# OBJECT PROFILE — GENERATOR

---

## Object Name
**Generator**

---

## Category
Combat Environment Objects

---

## Gameplay Purpose
High-value destructible target that powers FORGE systems. Destroying the generator disables linked systems: turrets go offline, security doors lose power, floodlights go dark. Generators are mission-critical targets in several missions ("destroy the generator before FORGE reinforcements arrive"). They also function as environmental cover (large and solid) but are placed in dangerous areas to create risk/reward decisions: the generator is tempting cover BUT destroying it has a large area-of-effect explosion. Players must approach generators with a plan — they are both opportunity and threat.

---

## Where It Is Used
- FORGE command centers and fortified positions
- Power supply rooms in industrial facilities
- Open-area power nodes for external perimeter systems
- Always visible from a distance — a landmark object in its area

---

## Interaction Type
**Destructible / Hazard** — Cannot be interacted with by the player directly. Destroyed by sustained gunfire (high HP) or a single tank shell. Explodes on destruction (large radius, 120 damage), disabling all linked systems.

---

## Visual Description

| Property | Detail |
|---|---|
| Shape | Large industrial generator unit. 1.5 tiles wide × 1.0 tile deep × 1.2 tiles tall. Boxy with a large turbine/engine section on the left and a control panel section on the right. Exhaust vents on the top. |
| Material | Heavy industrial steel — riveted panels, matte painted surface. Diesel-electric generator aesthetic (dieselpunk). |
| Color | Body: dark industrial grey-green (#2E3828). Accent panels: slightly lighter (#3A4830). Exhaust vents: near-black (#1A1A18). Running lights: amber (#C8A020, small indicator strip). FORGE decal: dark red (#6A1010) panel on the control section. Power output cables: dark grey thick conduits running from the right side to the ground. |
| Size | 1.5×1.0 tile footprint. 1.2 tiles tall. Largest stationary prop in the game. |
| Silhouette | Wide, heavy, industrial block. Clearly the largest object on any given screen. The exhaust vents on top and the power cables on the side make it unmistakably a generator. |
| Details | Riveted panel seams on all faces. Exhaust vents: 3 horizontal slot vents on the top face, very dark. Cooling fins on the left (engine section) side face. A FORGE data-plate on the control panel section. Amber running light strip along the top edge of the control panel face. Power output cables (2 thick cables): leave from the right side base, run to the ground and off-frame. Bolted anchor points at the base corners. |

---

## Damage Behavior

**Three states:**

| State | HP | Visual |
|---|---|---|
| Operational | 300–151 HP | Running — amber light strip on, exhaust animation |
| Damaged | 150–1 HP | One cable spark (VFX), housing panels dented/blackened, amber light flickering |
| Destroyed | 0 HP | Explodes (large VFX, 120 damage, 4 tile radius), replaced with burnt-out wreck static sprite |

---

## Collision Type
**Full block** — 1.5×1.0 tile footprint box collider. Removed on destruction (burnt-out wreck is also a full block but does not explode again).

---

## Animation Needs
**Required:** Exhaust vent heat shimmer / idle spin animation (4 frames, looping while operational). Amber light flicker for damaged state (2 frames). Destruction explosion handled by VFX system.

---

## Technical Constraints
- Generator is the largest object in the environment object library — must be visually dominant and readable at long range
- Amber running light must be visible from at least 5 tiles away
- The FORGE marking must be on the most camera-visible face
- Burnt-out wreck (destroyed state) must still function as cover (full block collision) — players can use the wreck for cover after destroying the generator
- Two power cable directions available (cables leaving to the right or to the left) as separate sprites — for flexible placement
