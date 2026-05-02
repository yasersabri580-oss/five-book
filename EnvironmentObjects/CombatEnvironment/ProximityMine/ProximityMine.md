# OBJECT PROFILE — PROXIMITY MINE

---

## Object Name
**ProximityMine**

---

## Category
Combat Environment Objects

---

## Gameplay Purpose
Area denial hazard. The proximity mine sits on the ground — invisible or nearly invisible to a rushing player, but clearly readable to an attentive one. When the player or an enemy infantry unit moves within 0.5 tiles, the mine triggers after a 0.8s warning beep (visual LED flash and audio cue), then explodes for heavy damage (60 damage, 1.5 tile radius). Forces careful movement through mined areas. Can be destroyed safely from range (1 shot detonates it without triggering the proximity fuse). Key gameplay skill: noticing mines before stepping on them.

---

## Where It Is Used
- FORGE-laid minefields (outdoor level sections, corridor approaches)
- Defensive perimeters around FORGE installations
- Occasionally in abandoned battlefield areas (implying earlier combat)
- Never placed in the player's only path without warning — always an alternate safe route available

---

## Interaction Type
**Hazard** — Cannot be interacted with. Player cannot disarm by hand. Can be detonated remotely (shoot it) or avoided. Kael's EMP pulse disarms it permanently (design note — not art concern).

---

## Visual Description

| Property | Detail |
|---|---|
| Shape | Flat disc mine, 0.3 tile diameter, 0.05 tile tall. Sits flush on the ground. Designed to be subtle — the player must be paying attention to spot it. |
| Material | Dark military-green matte plastic casing with a slight raised center hub. |
| Color | Casing: dark olive (#2A3020). Center hub: dark metal (#1A1A18). Warning LED on the hub: small bright red dot (#C42020). Subtle FORGE triangle etched on the casing face. |
| Size | Very small: 0.3 tile diameter. Ground-level only — no height. |
| Silhouette | Very flat disc. Minimal profile. The red LED is the only bright element. |
| Details | The mine casing has a subtle circular etched line around the perimeter (detonation ring shape). The center hub has a small raised post (the trigger/pressure plate). The LED is a tiny circle on the hub — the single most important readability element. 3 small attachment spikes at the mine's underside hold it to the ground (only 1 visible from the isometric angle). |

---

## Damage Behavior

**Two states:**

| State | Condition | Visual |
|---|---|---|
| Armed | Default | LED pulses slowly (dim red pulse, 1 beat per 2 seconds) |
| Triggered (warning) | Player within 0.5 tile | LED flashes rapidly (3 fast red flashes over 0.8s) |
| Destroyed (detonated) | HP = 0 or triggered explode | Sprite removed, explosion VFX by engine, small scorch decal placed |
| Disarmed | EMP hit | LED off, dark static sprite — mine is inert |

---

## Collision Type
**None** — Players and enemies walk over the mine without physics collision. The proximity trigger is a separate trigger zone (handled by script, not by the collider system).

---

## Animation Needs
**Minimal animation required:** LED slow pulse (armed state, 2-frame loop), LED rapid flash (triggered warning state, 2-frame fast loop).

---

## Technical Constraints
- The mine's small size (0.3 tile) is intentional — it should be spotted by attentive players but missed by rushed players
- The LED is the ONLY visual cue at distance — it must be bright enough to be noticed
- The mine MUST be placed on the `Ground` sorting layer — it is a floor-level object, not a mid-height object
- It must be beneath any infantry sprite that walks over it (infantry renders on top of the mine)
- Provide also a partially-visible variant (`mine_halfhidden.png`) where the mine is 60% covered by dirt/dust — for minefields where the mines are meant to be harder to spot
