# NOTES — FORGE SENTINEL-7

---

## Pipeline Notes

- SENTINEL-7 is the most technically complex character in the pipeline. Plan for it last, after all infantry and standard enemy assets are complete.
- It requires a **modular sprite layering system** (see Technical Constraints in FORGESEN7.md). Do not attempt to bake all states into a single sprite sheet — it will be unmanageable.
- Confirmed sprite layers for SENTINEL-7:
  1. **Body layer** — the chassis, legs, cannon arm, armor plate
  2. **Sensor cluster layer** — separate rotating sprite on top of the body
  3. **Vent overlay layer** — vent-open sprites, swapped by engine at phase trigger
  4. **Phase 3 leg glow layer** — engine shader overlay, not art-generated

---

## Sensor Cluster Rotation

The sensor cluster rotates independently to track the player. The art team delivers:
- **Sensor cluster as a separate sprite sheet**: 8 rotation positions (every 45°) × idle + alert states = 16 frames total
- The body sprite itself shows the cluster mount point (a circular socket) — the rotating cluster is overlaid at that position by the engine
- In Phase 2 and 3, the sensor eyes should be at FULL BRIGHTNESS — the eye dims should be reserved for idle Phase 1

---

## Phase Visual Changes

| Phase | Visual Changes |
|---|---|
| Phase 1 (100–65% HP) | Normal — all vent covers closed, sensor eyes at 70% brightness, cannon arm at standard position |
| Phase 2 (65–30% HP) | Body spark effects on right chassis from crane hit damage (engine particle), two Crawler hatch covers open on underside |
| Phase 3 (30–0% HP) | Legs latched to conveyor belt (leg animation changes), underside hatch covers open (heat missiles), leg joints glow red (#D02020) — engine overlay |

---

## Damage State Progression

SENTINEL-7 has no visible HP bar. Visual damage cues communicate phase and health:
- **70% HP:** First physical impact marks on chassis (scorch mark on right armor plate from player fire) — engine decal
- **65% HP:** Phase 2 transition: body shudders, cyan lights flicker (dim-then-bright burst) — 1-second transition animation
- **30% HP:** Phase 3 transition: same shudder + flicker, then underside hatch opens, legs move to conveyor attachment
- **15% HP:** Steam/smoke venting from top of chassis (engine particle, not art)
- **Death:** All lights out, legs buckle sequence, body collapses, full sparks/smoke

---

## Animation Priority Order

1. Body — walk (4 directions)
2. Sensor cluster rotation (8 positions × 2 states)
3. Attack — autocannon burst (4 directions)
4. Attack — charge Phase 1 (4 directions: wind-up → sprint → stop)
5. Phase transition animation (1→2, 2→3)
6. Attack — ground slam Phase 2
7. Crawler deployment Phase 2 (underside hatch open — 2 hatches)
8. Conveyor latch Phase 3 (transition to sliding movement)
9. Attack — heat missile Phase 3
10. Vent overlay sprites (open + glowing, 4 positions)
11. Death sequence

---

## Arena Integration Notes

- SENTINEL-7 must never exit the production floor arena (level 3). Its movement is constrained by the arena boundaries (engine handles this with a navmesh box around the arena).
- When SENTINEL-7 destroys a conveyor belt (by walking over it), the engine removes those tiles from Kael's navigation mesh. Art: no unique animation for this — the conveyor belt destruction is environmental FX, not character animation.
- Crane hook attack (Phase 2): the crane is a separate environmental object. SENTINEL-7 does not animate the crane — it only reacts to being hit by it (stagger + top hatch open). Art team provides: the stagger reaction frame and the top hatch open sprite (a new body layer frame where the top center hatch is open, revealing the interior reactor glow — orange #D04010).

---

## Known Open Questions

- Confirm whether SENTINEL-7 should have a unique audio signature for its sensor cluster (a rotating gyro hum) — flag for audio team.
- Confirm whether the "body falls" death animation requires a screen-shake companion effect — flag for VFX team.
- Is there a visual intro cutscene for SENTINEL-7 (drops from ceiling per game doc)? If yes, need a unique "dropping from ceiling" animation: folded legs → impact → legs unfold + stand. This may be an in-engine cutscene, not a sprite animation. Confirm with animation lead.
