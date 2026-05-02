# OBJECT PROFILE — AUTO TURRET

---

## Object Name
**AutoTurret**

---

## Category
Combat Environment Objects

---

## Gameplay Purpose
Automated enemy threat that challenges the player to identify, approach cautiously, and neutralize before engaging the surrounding area freely. Turrets control zones — areas the turret covers are dangerous to cross without a plan. Players must destroy the turret (via concentrated fire, EMP + focus fire, or flanking from outside its arc) or hack the linked ControlTerminal to disable it. Destroyed or disabled turrets change the tactical map significantly. Turrets must be immediately readable as active threats — a scanning turret must look menacing.

---

## Where It Is Used
- FORGE facility perimeters and guard posts
- Chokepoint coverage (corridors, bridges, doorways)
- Protecting high-value targets (generators, terminals, commanders)
- Never placed in areas the player is supposed to move through freely

---

## Interaction Type
**Hazard** — Cannot be interacted with directly by the player. Destroyed by concentrated gunfire or EMP + follow-up. Disabled by linked ControlTerminal hack.

---

## Visual Description

| Property | Detail |
|---|---|
| Shape | Fixed-mount turret on a rotating pedestal. Pedestal: cylindrical base, 0.5 tile diameter, 0.4 tile tall. Turret body: boxy housing unit, 0.5 tile wide × 0.4 tile deep × 0.3 tile tall, mounted on the pedestal. Barrel: two parallel gun barrels extending from the front of the housing, 0.4 tile length. |
| Material | Matte black and dark steel. Angular panels on the turret housing. Gun barrels: matte dark grey steel. |
| Color | Pedestal: #2A2E32. Turret housing: #1A2028 (very dark blue-black). Barrel: #2A2A2A. FORGE red stripe around the housing: #8A1010 (subtle — one stripe per face). Active sensor/eye: a glowing red-orange lens (#E04010) on the front face. |
| Size | Total footprint: 0.5 tile diameter on the pedestal. Total height: 0.7 tiles (pedestal + turret body + barrel). |
| Silhouette | Compact, low-profile, militaristic. The twin barrels are the primary silhouette cue. The sensor lens glows red — unmistakably hostile. |
| Details | The front face of the turret housing has a single sensor/camera lens (the "eye") — a convex red-orange lens with a bright center point. FORGE red stripe (thin, 3–4 px wide) runs around the top edge of the turret housing. Angular armor panels on the housing sides. The pedestal has attachment bolts visible at the base. |

---

## Damage Behavior

**Three states:**

| State | HP | Visual |
|---|---|---|
| Active | 120 HP | Scanning turret, red sensor glowing |
| Damaged | 60–1 HP | One barrel bent/broken, housing cracked, sparks (VFX via engine) |
| Destroyed | 0 HP | Blackened housing, barrels drooping, sensor dark. Static ruined sprite. |

Disabled state (via EMP or terminal hack): turret stops scanning, sensor dims to amber (#604000), barrels point neutral (forward). This is a temporary state that reverts after 3s (EMP) or is permanent (terminal hack).

---

## Collision Type
**Full block** — 0.5 tile diameter circular collider on the pedestal base. Players and enemies cannot walk through the turret.

---

## Animation Needs
**Required:** Scan animation (turret barrel rotates left/right in a threat arc), active fire animation, damaged state (static with engine-spawned spark VFX), destroyed state (static). See animation_prompts/.

---

## Technical Constraints
- The sensor lens is the readability anchor — it must be clearly visible and bright at all gameplay distances
- Turret scan arc: 120° default coverage arc, configurable per instance
- The barrel rotation is achieved by rotating the turret body sprite (or a separate barrel sprite) — the pedestal stays static
- Provide barrel/turret-body as a separate sprite layer above the static pedestal for rotation purposes
- Two variants: ground mount (standard, described above), and wall mount (turret housing attached to a wall at elevation 0.8 tile height — different footprint but same turret body art)
