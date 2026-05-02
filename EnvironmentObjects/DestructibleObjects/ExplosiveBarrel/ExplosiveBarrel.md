# OBJECT PROFILE — EXPLOSIVE BARREL

---

## Object Name
**ExplosiveBarrel**

---

## Category
Destructible Objects

---

## Gameplay Purpose
Environmental hazard and combat tool. Shooting an explosive barrel causes a large explosion that damages all units (player and enemy) within a radius of 3 tiles. Provides both threat and opportunity: enemies placed near barrels are vulnerable to one well-placed shot; the player standing near a barrel is equally at risk. Explosive barrels must be immediately recognizable as hazardous — a player new to the game must understand the danger within the first second of seeing one.

---

## Where It Is Used
- Enemy staging areas and depots
- Industrial zones and fuel storage areas
- Near generators or power equipment for environmental destruction setups
- Never placed in a location that is unavoidable — always has a safe path around

---

## Interaction Type
**Destructible / Hazard** — Destroyed by gunfire, explosions, or fire. Explodes on destruction. Cannot be interacted with (no E key prompt).

---

## Visual Description

| Property | Detail |
|---|---|
| Shape | Standard cylindrical steel drum, 0.5 tile footprint, 0.9 tiles tall. Vertical drum with two rolled ridges around the circumference. Flat top with two bung holes. |
| Material | Steel drum — painted metal, chipped in places. |
| Color | **CRITICAL:** Bright danger red (#C42020) as the primary body color. Hazard yellow (#E8B800) warning stripes diagonal across the front face. White skull-and-crossbones or simple hazard diamond stencil. This must immediately read as "danger, explosive." |
| Size | 0.5 tile footprint (narrow drum). Standard single-barrel variant. Double-barrel (two drums side by side) is a separate sprite. |
| Silhouette | Tall narrow cylinder. Very distinct from all other objects. |
| Details | Two circumferential ridges (rolled rings around the barrel). Two bung holes on the flat top. Yellow hazard stripe diagonal across the south face. Hazard stencil (simple skull or diamond). Slight corrosion at the base ring. An optional rust-red drip stain near one bung hole suggesting the contents have leaked slightly. |

---

## Damage Behavior

**Two states (sprite swap) + explosion event:**

| State | HP | Visual |
|---|---|---|
| Intact | 30 HP | Normal red barrel sprite |
| Leaking / Damaged | 1–15 HP | Barrel dented, bung hole dripping, slightly darkened |
| Destroyed | 0 HP | Sprite removed, explosion VFX triggered by engine, small metal fragment decal on ground |

When HP reaches 0: the `DestructibleController` fires `OnExplode` event. Engine handles explosion radius damage (3 tile radius, 80 damage), VFX, and audio — no additional art from this object.

A barrel exposed to fire (flame hazard) auto-damages over 2 seconds before exploding — engine handles this with no additional sprite states.

---

## Collision Type
**Full block** (0.5 tile footprint box collider). Collider removed on explosion.

---

## Animation Needs
**None for standard states.** The damaged state is a sprite swap. The explosion is a VFX system, not an object animation.

Optional low-priority enhancement: 2-frame "heat shimmer flicker" on the damaged barrel (blink between intact and slightly brighter) to signal imminent explosion — a nice-to-have, not required.

---

## Technical Constraints
- RED color is mandatory — no desaturated version. The barrel must be the most color-saturated object in any level it appears in (contrast against the grey/green/tan environment palette)
- Hazard stripes must be visible from the isometric angle — place them on the south face (camera-facing face), not just on the top
- The skull/hazard stencil must be readable at 32×32 px — keep it as simple silhouette shapes, not detailed
- Double-barrel variant: two barrels side by side on a shared 1×0.5 tile footprint
- Barrel leaning against a wall is NOT a standard variant — barrels must always stand upright
