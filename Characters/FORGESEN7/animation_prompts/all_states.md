# ANIMATION PROMPTS — FORGE SENTINEL-7 — ALL STATES

---

## Instructions for All SENTINEL-7 Prompts
- Use the canonical reference image (see `reference_prompt.md`) as the visual source of truth.
- **This is a boss unit. Only the action state and directional facing change. All design elements (legs, sensor cluster, cannon arm, armor plate, vent covers, FORGE logo) are locked.**
- Sprite scale: 576×576 px per frame (3× standard sprite scale).
- Engine layering system: Body layer + Sensor Cluster layer (separate) + Vent Overlay layer (separate).
- All prompts describe the **body layer** unless otherwise specified.
- Isometric 2.5D. 30-degree pitch.

---

# COMBAT WALK (All Phases)

## Instructions
4 cardinal directions. Looping, 6-frame cycle. The 4-leg mechanical gait is deliberate and heavy — each step is a visual impact. The sensor cluster tracks independently (handled by engine rotation — body prompt does not specify cluster facing).

---

## COMBAT WALK — FACING DOWN (South, toward viewer)

```
Isometric 2.5D combat walk animation frame (mid-stride) of FORGE SENTINEL-7, moving south.

Preserve exactly from reference: matte black hexagonal chassis body, 4 reverse-knee legs, left-side autocannon arm, right-side heavy armor plate, closed vent cover panels (cyan-outlined), FORGE gear-circuit logo on top surface, 5-eye sensor cluster mount point (no sensor cluster in this layer — engine overlays it separately). Do NOT redesign any element.

Pose (body layer only): Mid-stride movement. Front-left and back-right legs are at the forward/planted phase. Front-right and back-left legs are at the lifted/swing phase. Quadrupedal diagonal-pair movement (front-left + back-right move together; front-right + back-left move together). Each leg lift: the foot lifts 0.3m above the ground surface, short stride. Heavy body is stable — minimal body vertical oscillation (this machine is heavy, not bouncy). Cannon arm stable at default rest angle (slightly down-forward). Body facing south — front sensor mount visible at front.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline, boss-class detail level.
Lighting: Baked isometric top-left directional. Cyan trim strips provide self-illumination glow on adjacent panels.
```

---

## COMBAT WALK — FACING UP / LEFT / RIGHT
*(Follow the Down-facing format above, adjusting body orientation. In north-facing view: FORGE logo on top surface visible, sensor mount on far side. In left profile: all 4 legs visible in profile, cannon arm on near side (left). In right profile: armor plate on near side (right), cannon arm on far side.)*

---

# ATTACK — AUTOCANNON BURST

## Instructions
4 cardinal directions. Looping while firing. The cannon arm rotates to face the attack direction and fires a 4-round burst.

---

## ATTACK — AUTOCANNON — FACING DOWN (South)

```
Isometric 2.5D autocannon attack frame of FORGE SENTINEL-7, firing south (toward viewer).

Preserve exactly from reference: all body design elements locked.

Pose: All 4 legs planted in stable wide attack stance (not walking — stationary while firing). Left-side cannon arm rotated to face south — twin barrels pointing directly at viewer (foreshortened barrels visible at tips). Cannon arm elevation: horizontal level. Body remains still. Sensor mount is positioned frontally (but sensor cluster sprite handled separately by engine). Slight recoil suggestion: cannon arm pushed back ~3° from barrel thrust. Vents still closed (Phase 1 default).

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
Note: Muzzle flash is engine particle at barrel tips. Do not bake into sprite.
```

---

# ATTACK — CHARGE (Phase 1)

## Instructions
4 cardinal directions. Non-looping. 3-frame sequence: wind-up → full sprint → sudden stop.
The wind-up frame is critical — it telegraphs the charge and gives the player 0.5s to dodge.

---

## CHARGE — WIND-UP FRAME (Facing Down — South)

```
Isometric 2.5D charge wind-up animation frame of FORGE SENTINEL-7, facing south. This is the TELEGRAPH frame — 0.5s before the charge begins.

Preserve exactly from reference: all design elements locked.

Pose: All 4 legs bend into a deep pre-charge crouch — body lowers ~0.3m. Front legs splayed outward, rear legs bent for thrust. Cannon arm pulled back (rotated inward toward body — not aimed). Sensor cluster eyes: ALL FIVE eyes shift to FULL RED (#D02020) — this overrides the normal cyan for this one frame only. This is the critical visual signal. Body slightly coiled, tensed. This frame reads as: something terrible is about to happen.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
IMPORTANT: Sensor eyes in this frame ONLY are RED (#D02020), not cyan. This is the danger signal.
```

---

## CHARGE — SPRINT FRAME (Facing Down — South)

```
Isometric 2.5D charge sprint animation frame of FORGE SENTINEL-7, charging south at full speed.

Preserve exactly from reference: all design elements locked. (Sensor eyes return to cyan during sprint — the warning was the wind-up frame.)

Pose: Full gallop — both front legs extended far forward, both rear legs extended far back. Body horizontal, aggressive forward lean (~25°). All legs close to the ground in sprint posture. Cannon arm flung slightly back from sprint momentum. Body compressed forward, speed lines/motion blur suggested at rear legs and body edges (subtle trailing softness on trailing edges — not full blur).

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

# ATTACK — GROUND SLAM (Phase 2)

## Instructions
4 cardinal directions. Non-looping. 3-frame: raise all legs → peak position → slam down.
Shockwave is an engine particle (floor pulse ring). Do not bake shockwave into sprite.

---

## GROUND SLAM — IMPACT FRAME (Facing Down — South)

```
Isometric 2.5D ground slam impact animation frame of FORGE SENTINEL-7 in Phase 2, slamming all legs simultaneously.

Preserve exactly from reference: all design elements locked.

Pose: Impact moment — all 4 legs have just slammed into the ground. Front legs fully straightened downward (not bent — maximum downward extension). Rear legs same. Body drops to lowest point — chassis nearly touching the floor (only 0.1m clearance). All 4 leg foot pads pressed hard into the ground. Cannon arm swings downward from the impact (mechanical recoil). Dust/debris cloud at each foot pad contact point — engine particle handles this; sprite shows only the leg positions. Sensor eyes: FULL BRIGHTNESS (#20D4E0) — Phase 2 activation state.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

# CRAWLER DEPLOYMENT (Phase 2 Transition)

## Instructions
Facing south only (this is a scripted event, not all-direction). Non-looping. 2-frame: underside hatches slide open → Crawlers emerge.
The Crawler emergence is handled by spawning Crawler units in the engine. The SENTINEL-7 body sprite shows only the hatch-open state.

---

## CRAWLER DEPLOYMENT — HATCH OPEN FRAME

```
Isometric 2.5D crawler deployment frame of FORGE SENTINEL-7, showing two underside hatch covers open. Viewed from below-isometric angle (standard isometric camera sees the underside slightly due to the pitch).

Preserve exactly from reference: all body design elements locked.

Pose: Body stationary. Two underside hatch panels are shown in the OPEN position — they slide outward to the sides (like bay doors opening). The hatches are rectangular panels on the underside of the chassis. When open, the interior shows a dim orange glow (#D04010) inside the hatch cavity — the warm light of FORGE's internal mechanisms. The hatches are on the LEFT and RIGHT underside, symmetrically placed. All 4 legs stable and planted. Cannon arm stationary.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
Note: The actual Crawler units emerge as separate spawned sprites via engine — this frame shows only the open hatches on SENTINEL-7's body.
```

---

# PHASE TRANSITION (1→2 and 2→3)

## Instructions
Non-looping. 3-frame: stagger → lights flicker (dim) → lights flare (bright) → recovery posture.
Used at both phase transitions (65% HP and 30% HP).

---

## PHASE TRANSITION — LIGHTS FLICKER FRAME (Dim)

```
Isometric 2.5D phase transition frame (dim/flicker state) of FORGE SENTINEL-7.

Preserve exactly from reference: all design elements locked.

Pose: Body in a stagger — slight lateral lean (~10°). One front leg slightly lifted from impact/shock. All sensor eyes DIMMED to near-off (#052020) — this is the dim frame of the flicker. Cyan trim lines also dimmed (very faint, barely visible #0A3030). Cannon arm rotated slightly inward from shock. Overall: the machine looks briefly broken.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
Note: Engine alternates this dim frame with a full-bright frame to create the flicker effect before the phase recovery.
```

---

# DEATH

## Instructions
4 cardinal directions. Non-looping. 5-frame collapse sequence: leg buckle → body tilt → impact fall → dust → final rest (held).

---

## DEATH — FINAL REST FRAME (South-facing collapse)

```
Isometric 2.5D death animation final rest frame of FORGE SENTINEL-7, destroyed and collapsed.

Preserve exactly from reference: all design elements locked.

Final pose: All 4 legs completely buckled and folded under/around the chassis body — the machine has fallen. Body lies at a slight diagonal (not perfectly flat — one side of the chassis slightly elevated, leaning on the front-right leg joint). Cannon arm has fallen outward to the left, fully extended along the ground. All sensor eyes: COMPLETELY DARK (#050505 — fully off). All cyan trim lines: COMPLETELY DARK. FORGE logo on top surface visible — still intact but inert. Surface shows impact scorch marks and dents (baked in as damage texture on this specific frame). The machine is dead. No glow, no motion, no sparks — all of those are engine particles that fade before the final rest frame is reached.

Background: Transparent PNG.
Art style: Semi-realistic painterly sprite, 2px black outline.
Note: Held final frame. Sensor eyes and all lights must be completely dark — critical for the death read. This is a machine whose power has been completely cut.
```
