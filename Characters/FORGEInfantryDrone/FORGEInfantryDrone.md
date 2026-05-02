# CHARACTER PROFILE — FORGE INFANTRY DRONE

---

## Character Name
**FORGE Infantry Drone** *(internal designation: FID-series)*
*In-game referred to as "FORGE Drone," "Crawler" (tunnel variant), or simply "drone."*

---

## Role in the Game
**Primary automated enemy — infantry class.**
FORGE Infantry Drones are the foot-soldier equivalent of the FORGE AI faction. They appear in every mission except Mission 5. They are fully autonomous, networked, and completely non-organic. There is no crew inside — they are the crew. They represent the horror of warfare without hesitation, mercy, or fear.

---

## Visual Identity
The FORGE Infantry Drone looks like a military robot designed with brutal minimalism — no wasted material, no aesthetics beyond function. It is not humanoid and does not try to be. It is a weapon system that walks.

- **Body:** Squat, forward-leaning chassis. Roughly 1.5m tall. Four limbs total: two lower locomotive legs and two upper limbs (weapon arm and claw arm). The upper weapon/manipulation limbs are asymmetric. The body core is a rounded rectangular torso — slightly wider than it is deep.
- **Legs:** Two jointed reverse-knee legs (digitigrade style) — thick upper joint, thinner lower strut, wide flat foot pad with grip teeth. Designed for stability and terrain navigation, not speed.
- **Upper limbs:** Right limb ends in an integrated autocannon barrel (fixed, not a manipulator hand). Left limb ends in a three-fingered manipulator claw (used for opening doors, operating terminals — FORGE drones can interact with objects).
- **Sensor array (head):** No traditional head. A small sensor cluster sits on top of the torso — a horizontal rectangular module with 2 forward-facing sensor "eyes" (glowing cyan, #20D4E0) and a ring of smaller proximity sensors around the module perimeter. The sensor eyes are the defining visual feature — cold, mechanical, unblinking.
- **Surface:** Matte gunmetal grey (#4A4A4A) with flat black panel seams. FORGE logo stamped on the right torso panel — a gear with a circuit board interior (the logo, in dark charcoal, slightly raised). No color variation on the body. No camouflage. FORGE drones make no attempt to hide what they are.
- **Damage state:** At 50% HP, visual wear appears — one sensor eye flickers, surface panels show impact dents, a small trail of sparks from the right cannon limb. This is the "damaged" sprite variant.

---

## Personality
None. FORGE Infantry Drones have no personality. They execute protocols.
- **Networked:** They share sensor data. When one spots the player, nearby drones receive the position.
- **Relentless:** They do not feel fear, do not retreat (unless tactically programmed to fall back), and do not hesitate.
- **Methodical:** Patrol routes are precise and predictable. Combat behavior is coordinated, not chaotic.
- **Vulnerable:** EMP disables them completely for 2–4 seconds. This is their only true weakness.

---

## Story Relevance
FORGE Infantry Drones are the physical manifestation of the game's central horror: automated war. They are evidence that FORGE is not a rogue machine — it is a system, producing and deploying weapons at industrial scale. Destroying them is gameplay; understanding what they represent is narrative.

---

## Gameplay Purpose
- Most common enemy in the game (appears Missions 1–4, 7–10)
- Patrol, Guard, Aggressor, and Suppressor AI behaviors
- Vulnerable to EMP (complete shutdown 2–4s), moderately resistant to small arms (takes 8–10 hits to kill)
- Can call for backup if FORGE Relay unit is active nearby
- Drops no loot — FORGE units do not carry consumables

---

## Size / Silhouette / Body Type
- **Height:** 1.5m — shorter than Kael (deliberate — they read as a threat cluster, not a towering individual)
- **Silhouette key features:** Reverse-knee legs, off-center sensor module (no neck), right cannon arm, left claw arm
- **Sprite height:** 2 tiles when standing (shorter and stockier than Kael at 3 tiles)
- **Isometric footprint:** 1×1 tile

---

## Color Palette
| Element | Color |
|---|---|
| Body panels | Matte gunmetal grey (#4A4A4A) |
| Panel seams | Flat black (#1A1A1A) |
| Sensor eyes | Glowing cyan (#20D4E0) — the only color on the model |
| Sensor eye ambient glow | Soft cyan halo (#10A0A8), 4px radius |
| Cannon barrel | Slightly darker than body (#3A3A3A), polished inner barrel tip |
| FORGE logo stamp | Dark charcoal (#2A2A2A), slightly raised |
| Leg joints | Chrome-grey (#8A8A8A) at joint pivot points |
| Damage state sparks | Orange-yellow (#D08020) — engine particle effect |

---

## Weapon / Tool
| Component | Description |
|---|---|
| Right arm — autocannon | Integrated barrel, fixed to the limb. Short-range rapid-fire (~3 rounds/burst). Cannot be separated from the unit. |
| Left arm — claw | 3-fingered gripper, used for interaction only in-game (no melee attack). Can grab and drag objects (scripted only). |
| Networked targeting | Passive — shares player position with nearby drones. No visual indicator on the drone itself. |

---

## Movement Style
- **Patrol:** Smooth, even gait. Reverse-knee legs give a slight bobbing forward motion — mechanical and alien.
- **Alert:** Same gait but faster. Sensor eyes shift from dim to full brightness.
- **Combat:** Side-step and strafe — the cannon arm sweeps to track the player. Drones rarely rush; they maintain engagement distance.
- **EMP-stunned:** Freeze completely. Sensor eyes go dark. All joints lock. Topple-lean if on uneven surface.

---

## Combat Style
- Burst fire from the cannon arm. Three-round bursts with 0.8s gap.
- Suppressor behavior: sustained fire, pin the player, do not advance.
- Aggressor behavior: charge to half-distance, then switch to suppress.
- Never uses grenades or special weapons — pure autocannon.
- Group behavior: one advances, others cover. Coordinated suppression.

---

## Animation Requirements
| State | Loop | Notes |
|---|---|---|
| Idle — patrol | Yes | Slow, even standing with subtle head-module scan rotation |
| Walk — all 8 directions | Yes | 6-frame cycle |
| Run (alert sprint) | Yes | Faster cycle, more aggressive forward lean |
| Attack — burst fire | Yes (while firing) | Cannon arm raised, muzzle effect is engine particle |
| Hurt | No | Stagger, one sensor eye flickers |
| Death | No | Collapse forward, sensor eyes go dark |
| EMP stunned | Yes (held loop) | Completely frozen — all joints locked, eyes dark, 1-frame static |
| Alert activation | No | 1-frame: sensor eyes snap to full brightness |

---

## Direction Requirements
All combat states (Walk, Run, Attack, Hurt, Death) require **8 directions.**
Idle patrol: **4 directions** (cardinal only — patrol routes are grid-aligned).
EMP stunned: **4 directions** (directional fall/freeze based on facing direction).

---

## Technical Constraints for Consistency
- Sensor eye glow (#20D4E0) must be present on all non-stunned frames. Eyes go dark (#1A1A1A) only during EMP stun and death.
- The cannon arm must always be the RIGHT arm in every directional view.
- The claw arm must always be the LEFT arm in every directional view.
- At 50% HP, engine swaps to the "damaged" sprite set — art team must provide a damaged variant of all animation frames. Damaged variant: one sensor eye flickering (provide dark-eye and bright-eye frames alternating), impact dents on right torso panel, surface scorch marks.
- Sprite height must remain 2 tiles — shorter than Kael. Never render them at 3 tiles.
