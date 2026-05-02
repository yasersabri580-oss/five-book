# CHARACTER PROFILE — SENTINEL CORPORATE SOLDIER

---

## Character Name
**SENTINEL Corporate Soldier** *(no individual name — faction operative unit)*
*In-game faction: SENTINEL Corporate Security*

---

## Role in the Game
**Human enemy — SENTINEL faction infantry (most disciplined and dangerous human enemies).**
SENTINEL Soldiers are professional private military contractors deployed by the SENTINEL corporation. They appear in Missions 4, 6 (recon team), 9, and 10. They operate in fireteams of 3, are tactically disciplined, and never behave erratically. They are the most dangerous human opponents Kael faces.

---

## Visual Identity
SENTINEL Soldiers look like the enemy of a different kind: corporate, funded, professional. They are as threatening as Reclaimers but visually opposite — clean, uniform, and deliberate. They look like private military, not soldiers, and not militia.

- **Helmet:** Full-face ballistic helmet — matte black (#1A1A1A), smooth modern composite shell. Integrated visor — tinted dark grey (#2A2A30). Unlike Kael's cracked visor, this is pristine. Small camera module clipped to right side of helmet (surveillance — SENTINEL documents everything). SENTINEL corporate logo on left side of helmet — a stylized "S" in a clean white line.
- **Upper body:** Close-fitting black tactical jacket, clean lines, subtle texture (water-resistant ripstop fabric). No chest rig — internal magazine pockets built into the jacket (visible as subtle panel seams). SENTINEL logo patch on right chest (black-on-black with a reflective sheen — barely visible). Corporate aesthetic: this is uniform, not kit.
- **Body armor:** Slim plate carrier over the jacket — matte white (#DCDCDC) front plate, black straps. Clean, not scratched. The white plate is the dominant visual feature of the torso and makes SENTINEL soldiers immediately identifiable in the field.
- **Arms:** Both arms in fitted black tactical sleeves. Gloves — full-finger black tactical gloves. No skin visible.
- **Legs:** Black tactical trousers, clean. Knee pads — matte white (#DCDCDC), matching the plate carrier. Thigh holster on right leg — black, with sidearm.
- **Boots:** Black boots, ankle-high, modern tactical design, clean (maintained).

---

## Personality
SENTINEL Soldiers are not people in the story — they are a corporation's tools. They communicate with short coded efficiency and follow orders without question. In combat, they function as a unit, not as individuals. They do not taunt, do not panic, do not break formation until forced.

The SENTINEL faction is the most threatening because it has resources, structure, and motivation (profit from war) — the Reclaimers are chaos; FORGE is a machine; SENTINEL is a plan.

---

## Story Relevance
SENTINEL forces are the hidden hand behind FORGE's rogue state (the Conquest Protocol). Encountering them in combat is a mid-game escalation — they are not the enemy Kael came to fight, and their presence confirms something is deeper and more sinister than a machine uprising. The captured SENTINEL field commander in Mission 4 provides the first explicit hint.

---

## Gameplay Purpose
- Enemy infantry in Missions 4, 6, 9, and 10
- AI behaviors: operates in fireteams of 3 (1 shield bearer, 1 suppressor, 1 flanker)
- Tactical withdrawal when ≤50% of fireteam lost — falls back and calls reinforcements
- Destroys radio tower to prevent calling reinforcements
- Most accurate human enemy — controlled semi-auto fire
- The **shield bearer sub-type** carries a rectangular ballistic shield on the left arm (requires separate sprite variant)

---

## Size / Silhouette / Body Type
- **Height:** Same as Kael (~1.85m), matching human scale
- **Build:** Athletic and contained — less bulky than Reclaimer. Lean but armored.
- **Silhouette key features:** Full-face matte black helmet, WHITE plate carrier chest (critical ID feature), white knee pads, clean uniform lines
- **Sprite height:** 3 tiles
- **Isometric footprint:** 1×1 tile

---

## Color Palette
| Element | Color |
|---|---|
| Helmet | Matte black (#1A1A1A) |
| Helmet visor | Dark grey tint (#2A2A30) |
| SENTINEL logo (helmet) | White line mark (#E0E0E0), small |
| Tactical jacket | Near-black (#1E1E22) |
| Plate carrier (front) | Matte white (#DCDCDC) |
| Plate carrier straps | Black (#1A1A1A) |
| Knee pads | Matte white (#DCDCDC), matching plate |
| Trousers | Black (#1A1A22) |
| Boots | Clean black (#141414) |
| Gloves | Matte black (#1A1A1A) |
| SENTINEL chest logo | Black-on-black, reflective sheen (barely visible) |

---

## Weapon / Tool
| Slot | Item | Description |
|---|---|---|
| Primary | Compact assault carbine | Short barrel, folding stock, suppressor on muzzle. Clean finish — maintained, professional. Black, with white SENTINEL serial number strip on the receiver (tiny, barely visible). |
| Secondary | Sidearm in thigh holster | Black compact pistol — holstered on right thigh. |
| Shield variant | Ballistic shield (shield bearer sub-type) | Rectangular, matte white on front face with SENTINEL logo, black handle on rear. Covers full body height when raised. |
| Radio | Earpiece + wrist terminal | Earpiece in right ear. Small terminal on left wrist (used for calling reinforcements — press/activate animation needed). |

---

## Movement Style
- Precise, minimal. No wasted movement.
- Walk: upright, controlled. Military march efficiency.
- Run: controlled sprint in fireteam formation.
- Tactical withdrawal: turn, sprint to pre-scripted cover point, re-engage. Smooth, rehearsed.

---

## Combat Style
- **Suppressor sub-type:** stays at long range, fires controlled 2-round burst.
- **Flanker sub-type:** moves perpendicular to player using sprint, attacks from 45° angle.
- **Shield bearer sub-type:** walks toward player with shield raised, providing mobile cover for team.
- All sub-types call for reinforcements by pressing wrist terminal before retreating.
- Never charge headfirst (contrast with Reclaimers).

---

## Animation Requirements
| State | Loop | Notes |
|---|---|---|
| Idle | Yes | Alert at rest — head scans, controlled breathing |
| Walk (all 8 directions) | Yes | Upright, precise gait |
| Run (all 8 directions) | Yes | Controlled sprint, rifle raised |
| Attack — carbine fire (all 8 directions) | Yes (while firing) | Raised rifle, aimed fire (not hip-fire) |
| Hurt (all 8 directions) | No | Controlled stagger — less dramatic than Reclaimer |
| Death (4 directions) | No | Clean collapse |
| Tactical withdrawal sprint (4 directions) | Yes | Same as run set, reuse |
| Call reinforcements (1-2 frames, 2 directions) | No | Press left wrist terminal, look down at it 1 frame |
| Shield raised walk (shield bearer sub-type, all 8 directions) | Yes | Left arm raised with shield in front |

---

## Direction Requirements
All combat states: **8 directions.** Special actions: **4 directions.**

---

## Technical Constraints for Consistency
- The **white plate carrier** is the primary faction identification feature. It must be clearly visible in south, southwest, and southeast views. In north-facing views the rear of the plate carrier is visible (black back plate — slightly different shade from jacket).
- The matte black helmet must always contrast with Kael's olive/amber helmet — no color bleed.
- The **shield bearer sub-type** is a sprite variant — separate from the standard soldier. Only the left arm and frontal coverage change. All other costume elements are identical to the standard variant.
- SENTINEL soldiers must look cleaner than Reclaimers and more uniform than Kael — their kit condition (scratches, worn areas) is minimal.
