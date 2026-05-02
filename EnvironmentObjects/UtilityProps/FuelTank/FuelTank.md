# OBJECT PROFILE — FUEL TANK

---

## Object Name
**FuelTank**

---

## Category
Utility Props

---

## Gameplay Purpose
Environmental hazard and visual storytelling prop. The fuel tank communicates "this is an industrial or military fuel depot" and implicitly warns players that the area is flammable. If shot, the fuel tank leaks and eventually ignites in a sustained fire (unlike the explosive barrel, which explodes instantly — the fuel tank burns, creating a persistent fire hazard zone for 8 seconds). Players can use this tactically: shoot a fuel tank near enemy infantry and then attack while they are caught in the fire.

---

## Where It Is Used
- Vehicle fueling stations, motor pools
- Industrial fuel storage areas
- Near generators and power equipment
- NOT in clean command centers or server rooms — fuel tanks belong in mechanical/industrial zones

---

## Interaction Type
**Static / Hazard** — Cannot be interacted with. Damaged by gunfire (ignites when HP reaches 0). Not instantly explosive — it is a fire hazard that creates a burn zone.

---

## Visual Description

| Property | Detail |
|---|---|
| Shape | Large horizontal cylindrical tank on two saddle supports. Tank cylinder: 1.0 tile wide × 0.5 tile tall. Total with support legs: 0.7 tile tall. 0.6 tile deep. |
| Material | Steel tank — riveted/welded construction. Painted. |
| Color | Tank body: dark olive-military green (#3A4828). Warning stripes: yellow (#C8A020) and black (#1A1A18) diagonal stripes at both ends. Saddle supports: dark grey steel (#2E2E2C). Flammable hazard stencil: orange-red (#C84010) diamond on the cylinder side face. Fuel cap/filler: dark metal top of the tank. |
| Size | 1.0 tile wide × 0.6 tile deep × 0.7 tile tall. |
| Silhouette | Horizontal cylinder on legs. Very distinct from the vertical explosive barrel. |
| Details | Two saddle support frames holding the tank (simple A-frame steel stands). 2–3 riveted seam rings around the cylinder. Fuel filler port on the top of the tank (a small recessed circular cap). Warning hazard diamond (orange) on the south face. Yellow/black diagonal warning stripes on the end cap faces. A fuel gauge sight glass on the cylinder side (a small rectangular vertical window with a liquid level indicator line — fuel level 60–80% full). Pipe fitting at the base of the south face (fuel outlet pipe) with a valve wheel. |

---

## Damage Behavior

**Two states + fire event:**

| State | HP | Visual |
|---|---|---|
| Intact | 80 HP | Normal tank sprite |
| Leaking | 40–1 HP | Crack on the south face, dark fuel drip (#1A1008 dark oily liquid) running down from the crack |
| Burning | 0 HP | Sprite replaced with burning-tank sprite (flame flickering on top — VFX via engine). Fire zone: 2 tile radius, 5 damage/second for 8 seconds. |

---

## Collision Type
**Full block** — 1.0 tile wide × 0.6 tile deep box collider. Remains during burning state (the tank wreck is still physically present).

---

## Animation Needs
**None for intact or leaking states** — sprite swaps only. Burning state handled by VFX system (engine-spawned fire particle on top of the burnt tank sprite).

---

## Technical Constraints
- Must be visually distinct from the ExplosiveBarrel (horizontal vs vertical, green vs red)
- The flammable hazard diamond (orange) is the primary danger indicator — must be readable at game scale
- The fuel gauge sight glass must be a recognizable detail at a glance — even if small
- Two placement orientations: south-facing (tank length runs east-west) and east-facing (tank length runs north-south)
