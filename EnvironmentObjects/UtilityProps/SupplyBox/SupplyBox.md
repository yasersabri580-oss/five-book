# OBJECT PROFILE — SUPPLY BOX

---

## Object Name
**SupplyBox**

---

## Category
Utility Props

---

## Gameplay Purpose
Ammo and supply container — the player's primary field resupply source. When the player interacts with a supply box (E key, instant — no hold required), they receive a full ammo resupply for their current weapons. Supply boxes are single-use: they are emptied on first interaction and cannot be used again. Their placement signals to the player "a fight is coming" or "you are in friendly/neutral territory." Supply boxes are also used in lore-building: FORGE supply boxes contain military-grade ammo, while Rift supply boxes contain improvised or scavenged gear (different visual variant). Clearly distinguishable from the WoodenCrate (which is ambiguously interactive) and the SandbagBarrier (which is cover only).

---

## Where It Is Used
- Before major combat encounters — placed in secure positions before the player commits to a fight
- Rift safehouse areas — friendly supply caches
- Neutral areas: captured supply depots
- Always placed where the player can access them safely (or semi-safely) — not in the middle of active enemy fire

---

## Interaction Type
**Usable (instant)** — Player presses E once on approach. Immediate ammo resupply. Box opens (lid flips up), then switches to depleted state. No hold duration — this is a quick pick-up, not a hack or repair.

---

## Visual Description

| Property | Detail |
|---|---|
| Shape | Rectangular military supply crate with a hinged lid. 0.9 tiles wide × 0.7 tiles deep × 0.6 tiles tall. Wider and lower than the WoodenCrate. Clearly a different silhouette. |
| Material | Stamped steel with rubber corner guards. Military-issue equipment case aesthetic. |
| Color | FORGE variant: dark military green (#2A3820) with FORGE red decal stencil. Rift variant: darker matte grey (#282828) with Rift white lightning-bolt stencil. Ammo indicator: a small yellow triangle stencil ("AMMO") on the front face. |
| Size | 0.9×0.7 tile footprint. 0.6 tile tall. Wider and lower than the WoodenCrate (0.8×0.8 tile). |
| Silhouette | Wide low rectangle with a defined lid line. Clearly a military equipment case. Flat lid, not bulging. |
| Details | Rubber corner guards at all 8 corners (slightly rounded dark rubber bumpers). Two spring-latch clasps on the front face (the camera-facing face). Handle on the lid (a flat bar handle). A stenciled "AMMO" triangle on the front face in yellow (#C8A020). Rift faction lightning bolt on the side face (Rift variant). Carry handles at both ends (visible on the short-end faces). |

---

## Damage Behavior
**Not destructible.** The supply box is a hardened military case. It cannot be damaged or destroyed.

---

## Collision Type
**Partial block** — 0.9×0.7 tile box collider. Player cannot walk through it but it is a low obstacle.

---

## Animation Needs
**Minimal:** 3-frame lid-open animation when the player interacts (lid flips up, revealing interior). After animation, holds on the open/depleted state.

---

## Technical Constraints
- Must be visually distinct from the WoodenCrate (wood/tan vs steel/green; tall vs wide)
- The "AMMO" stencil and the clasp detail must communicate "this is a military supply container" at a glance
- Two faction variants: FORGE (green + red stencil) and Rift (grey + white stencil) — same geometry, different color/markings
- Two states: closed (available) and open/depleted (used) — lid-open state shows empty interior or a few spent shells for flavor
- The lid-open animation is the key interaction feedback — make it feel satisfying and quick (0.2s)
