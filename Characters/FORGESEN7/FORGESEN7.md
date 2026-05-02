# CHARACTER PROFILE — FORGE SENTINEL-7

---

## Character Name
**FORGE SENTINEL-7** *(known as "Seven" by factory workers)*

---

## Role in the Game
**Boss 1 — Mission 8, The Crucible production hall.**
FORGE SENTINEL-7 is the guardian unit of The Crucible. It is a unique, one-of-a-kind machine built by FORGE to protect its most critical production facility. It is not a standard FORGE unit — it is purpose-built for indoor factory defense, designed to navigate industrial spaces that standard tanks cannot access.

---

## Visual Identity
SENTINEL-7 is massive, alien, and deeply unsettling. It does not look like a tank or a drone — it looks like a spider built from a tank chassis. Its size, movement, and sound are designed to make the factory floor feel dangerous in a completely new way.

- **Body core:** A large rounded-hexagonal chassis body — twice the width of a standard FORGE tank hull. Matte black (#141414) with subtle hexagonal surface panel lines (not grid — FORGE design language, all geometric). Cyan panel accent lights in thin strips along the panel edges (same cyan as FORGE eyes: #20D4E0, but thinner and more angular — trim lines, not eyes).
- **Legs (4 legs — quadrupedal):** Heavy, thick, jointed mechanical legs in an insect-style configuration — two legs on each side. Reverse-joint (like the Infantry Drone). Each leg is roughly 1.5m long. The legs anchor SENTINEL-7 firmly to the floor and allow it to traverse the factory interior, step over obstacles, and (in Phase 3) latch onto conveyor belts. Leg material: same matte black as body, chrome-grey joint pivots.
- **Sensor cluster (front):** No traditional tank barrel on the front. Instead, a rotating sensor cluster — a horizontal oval module that rotates independently of the body. On this module: a row of 5 sensor "eyes" instead of 2 — the central eye is larger (#20D4E0, full brightness), and four flanking eyes are smaller (slightly dimmer cyan). The cluster rotates left-right to track the player. This sensor cluster is the closest thing to a "face" on SENTINEL-7.
- **Weapons:**
  - Left side: autocannon mount — a protruding turret arm on the left body flank, rotates to aim. Fires 4-shot bursts.
  - Right side: heavy plated shoulder section — no weapon here, just heavy armor. This asymmetry is deliberate — it creates a distinctive silhouette and an exploitable side (left is the weapon arm; right is the more armored flank).
  - Underside: heat coils (Phase 3 heat missiles launch from underside — not visible until Phase 3, when underside hatch opens).
- **Vent covers (Phase 1 weakness):** Two vent covers on each side of the chassis (total 4). They are flush panels in the standard Phase 1 state. Shooting them open (2 shots each) exposes glowing orange interior vents — the weakpoints. When a vent is exposed and grenaded, it emits a bright orange burst.
- **Scale:** SENTINEL-7 is approximately 2 tiles wide and 1.5 tiles tall — it occupies a 2×2 tile footprint. It is significantly larger than any infantry unit.
- **FORGE logo:** On top of the body chassis — same gear-circuit logo as Infantry Drones, but much larger and more prominent. Visible from above/isometric.

---

## Personality
None — but a presence. FORGE SENTINEL-7 is entirely silent in terms of speech. But it communicates through its actions: methodical, relentless, and adaptive. The Phase transitions feel like watching a machine solve a problem. It does not rage, it does not hesitate. It identifies what is working against it and changes. That mechanical adaptability is more frightening than anger.

---

## Story Relevance
SENTINEL-7 is the culminating mechanical threat of The Crucible. Defeating it opens the path to the production core that Kael must plant the detonation device in. SENTINEL-7's presence confirms the scale of FORGE's capability — this was built not from external supply but from the factory's own production. FORGE has been building its own boss-class defenders from scratch.

---

## Gameplay Purpose
- Boss 1 of Chapter 1 (Mission 8)
- No tank available for this fight — pure infantry encounter
- Three distinct phases with specific mechanical weaknesses:
  - **Phase 1:** Expose and grenade side vents
  - **Phase 2:** Use crane hook terminal (2 uses); manage Crawler reinforcements
  - **Phase 3:** Shoot leg joints (4 total) to immobilize, then finish with grenades + fire
- HP: 2200 (no visible HP bar — damage read only through visual/audio cues)
- Arena: factory production floor, level 3 — conveyor belts, steam vents, hanging cranes, smelting vats

---

## Size / Silhouette / Body Type
- **Width:** 2 tiles (isometric footprint 2×2)
- **Height:** 1.5 tiles at body; legs extend to 2 tiles total with legs deployed
- **Silhouette key features:** Quadrupedal stance (all 4 legs visible), large hexagonal body, rotating sensor cluster (5 eyes), asymmetric weapon arm (left) vs. heavy armor (right), vent covers on sides
- **Scale rule:** SENTINEL-7 must dominate the arena visually. It should fill approximately 40% of the screen width in the combat view.

---

## Color Palette
| Element | Color |
|---|---|
| Body chassis | Matte black (#141414) |
| Panel edge trim | Thin cyan lines (#20D4E0) — angular/geometric |
| Sensor eyes (5) | Central: full cyan (#20D4E0); flanking 4: slightly dimmer (#10A0A8) |
| Legs | Matte black (#141414), chrome joint pivots (#8A8A8A) |
| Cannon arm | Dark grey-black (#2A2A2A), polished barrel tip |
| Vent covers (closed) | Flush matte black — barely distinguishable from body panels |
| Vent covers (open/exposed) | Glowing orange interior (#D04010), heat shimmer |
| Leg joints — Phase 3 weakness | Glowing red (#D02020) at joint pivot points when phase 3 activates |
| FORGE logo (top chassis) | Dark charcoal (#2A2A2A), large gear-circuit emboss |

---

## Weapon / Tool
| Component | Description |
|---|---|
| Left-side autocannon mount | Rotatable turret arm, fires 4-shot burst. Range: full arena. |
| Charge attack | Phase 1: full-body charge forward — telegraphed by red sensor eye glow + stomp audio |
| Ground slam (Phase 2) | All 4 legs slam simultaneously — 4-tile radius shockwave |
| Crawler deployment (Phase 2) | Relay module in body activates — 6 FORGE Crawlers emerge from underside hatches |
| Heat missiles (Phase 3) | Underside hatches open — launches guided heat missiles with floor reticle targeting |

---

## Animation Requirements
All animations are directional only for the boss's orientation relative to the player. Boss always occupies center of arena and faces the player (tracks).

| State | Notes |
|---|---|
| Idle patrol (Phase 1) | Slow 4-leg walk around arena perimeter |
| Combat walk (all phases) | Medium-speed movement tracking player |
| Attack — autocannon burst | Cannon arm swings to player direction, fires |
| Attack — charge (Phase 1) | Wind-up (sensor glow red) → full sprint across arena |
| Attack — ground slam (Phase 2) | All legs rise and slam simultaneously |
| Crawler deployment (Phase 2) | Two underside hatches open, Crawlers emerge |
| Attach to conveyor (Phase 3 transition) | Body latches onto conveyor belt, legs retract partially |
| Move along conveyor (Phase 3) | Sliding motion, partial leg contact with belt |
| Attack — heat missile (Phase 3) | Underside hatches open, missile launched upward-arc |
| Phase transition (1→2, 2→3) | Stagger + brief power flicker (cyan lights dim, then flare) |
| Hurt (per phase) | Body rock, cyan lights flicker, sparks from hit location |
| Vent exposed (Phase 1) | Vent cover panel blows off (separate FX), orange interior glow visible |
| Death | All legs buckle, body collapses, sensor eyes go dark, smoke and sparks |

---

## Direction Requirements
SENTINEL-7 always faces the player. The animation system rotates the boss facing based on player position.
Provide: **4 cardinal direction sets** for each state. Engine interpolates between them.

---

## Technical Constraints for Consistency
- SENTINEL-7's sprite must be drawn at **3× scale** relative to standard character sprites. Standard: 192×192 px → SENTINEL-7: 576×576 px per frame.
- The 4-leg stance must always be stable and clearly quadrupedal in all directional views.
- Sensor cluster rotation is handled by the engine (separate rotating sprite layer on top of body) — art team provides: body sprite sheet + sensor cluster sprite sheet (separate).
- Vent covers are a separate sprite layer — closed covers, then open/glowing interiors are a sprite swap managed by the engine. Art team provides: closed vent frames baked into body sprite, plus: separate glowing vent overlay sprites (2 per side, 4 total).
- Phase 3 leg joint glow (#D02020 red at joints) is a separate overlay layer applied by engine at phase 3 — similar to the Survivor Instinct overlay for Kael. Art team does not need to rebake all Phase 3 frames with red joints.
