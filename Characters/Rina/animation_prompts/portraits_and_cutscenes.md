# ANIMATION PROMPTS — RINA — PORTRAITS AND CUTSCENE FRAMES

---

## Instructions for All Rina Prompts
- Use the canonical reference image (see `reference_prompt.md`) as the visual source of truth.
- **Only expression and minor pose change between portrait variants. Costume, facial features, scar placement, and headset are strictly locked.**
- All portraits: 256×256 px delivered, displayed at 128×128 px in-game. Face must fill at least 50% of portrait frame.
- Camera for portraits: three-quarter front-left view (standard portrait convention, character faces slightly right of frame).
- Background: flat dark near-black (#121212) for all portraits.
- Art style: same semi-realistic painterly style as Kael. Crisp 2px black outline.

---

# PORTRAITS (HUD Use)

---

## PORTRAIT — NEUTRAL (Default)

```
Portrait frame of Rina from the game IRON BREACH. Chest-to-crown framing, three-quarter left-facing view.

Preserve exactly from reference: sharp angular face with warm olive-brown skin, subtle scar on left jawline, close-cropped dark hair, dark charcoal jacket, right-ear headset with mic arm, Rift patch on upper left arm visible at frame edge. Do NOT change any visual element.

Expression: Neutral intelligence. Eyes (#2A1A10) alert and slightly narrowed — scanning, not relaxed. Mouth closed, neutral. No smile. No grimace. Chin level. This is the face of someone processing information at all times.

Background: Flat dark near-black (#121212). No environment.
Art style: Semi-realistic painterly, 2px black outline. Readable at 128×128 px.
Lighting: Soft top-left directional baked in. Slight right-edge rim light.
```

---

## PORTRAIT — SPEAKING

```
Portrait frame of Rina — Speaking variant. Same framing and base as NEUTRAL portrait.

Preserve exactly from reference: all costume and facial features locked. Do NOT redesign.

Expression: Mouth open — mid-speech position. Lower jaw dropped naturally (not exaggerated). Upper teeth just visible. Eyes remain alert and slightly narrowed — she never breaks focus while talking. This is a natural speaking face, not a yell or gasp.

Note: Art team delivers TWO frames — Neutral (mouth closed) and Speaking (mouth open). Engine alternates between them based on voiceover amplitude to simulate speech.

Background: Flat dark near-black (#121212).
Art style: Semi-realistic painterly, 2px black outline. Readable at 128×128 px.
```

---

## PORTRAIT — ALARMED

```
Portrait frame of Rina — Alarmed variant. Same framing and base as NEUTRAL portrait.

Preserve exactly from reference: all costume and facial features locked.

Expression: Alert escalated to alarm. Eyes wider — whites slightly more visible above the iris (not wide-eyed cartoon alarm — believable human alarm). Brow slightly furrowed in the center (concern/urgency furrow). Mouth slightly open — inhale before speaking urgently, or holding breath. Head canted 3–5° forward (leaning toward her console, toward the situation). Still controlled — Rina does not panic visually, but the urgency is clear.

Background: Flat dark near-black (#121212).
Art style: Semi-realistic painterly, 2px black outline. Readable at 128×128 px.
```

---

## PORTRAIT — GRIM

```
Portrait frame of Rina — Grim variant. Same framing and base as NEUTRAL portrait.

Preserve exactly from reference: all costume and facial features locked.

Expression: Eyes slightly lowered at the outer corners — a subtle weight to the gaze. Mouth pressed closed, slight tension at the corners (not a frown — a controlled tightening). This is the face of someone delivering news they did not want to have to deliver. No tears. No dramatic drooping. Controlled grief, delivered in Rina's characteristically precise manner.

Background: Flat dark near-black (#121212).
Art style: Semi-realistic painterly, 2px black outline. Readable at 128×128 px.
```

---

## PORTRAIT — CAPTURED (Chapter 1 Ending)

```
Portrait frame of Rina — Captured variant. SENTINEL custody. End of Chapter 1 only.

Preserve exactly from reference: facial features locked. Costume changed for this variant only — see below.

Expression: Defiance. Chin slightly raised. Eyes direct, unwavering — looking at the viewer / at Kael through the radio. A faint tension in the jaw. She has been taken, but she has not surrendered.

Costume changes (captured variant only):
- Jacket is present but slightly disheveled — collar knocked askew, one side of the zip partially open
- The headset is GONE — SENTINEL removed it. No headset in this variant.
- Wrists: thin black polymer cuffs at the bottom of frame, barely visible at the very lower edge of the portrait (just wrist tops at frame bottom, hands below frame). The restraints are SENTINEL-style — clean, corporate, black.
- Slight mark on right cheekbone — a faint bruise suggestion (desaturated purple-blue undertone on the right cheek, #3A2040 tint, very subtle).

Background: Slightly different from other portraits — dark grey with a faint cold blue tint (#121520) to suggest SENTINEL lighting environment.
Art style: Semi-realistic painterly, 2px black outline.
```

---

# CUTSCENE FULL-BODY FRAMES

---

## CUTSCENE — SEATED AT CONSOLE (Mission 1 Safehouse)

```
Isometric 2.5D full-body cutscene frame of Rina, seated at a field console in a Rift safehouse. South-facing (toward viewer), 30-degree pitch.

Preserve exactly from reference: charcoal jacket, Rift patch, headset, fingerless gloves, dark boots, map case strap.

Pose: Seated at a makeshift console (a folding table with a cracked monitor/tablet, cables, papers). Leaning slightly forward — elbows near the table edge. Left hand on the table, fingers spread, reading data. Right hand near the headset mic arm — adjusting it or holding it steady while speaking. Head tilted slightly down toward the console, eyes up to camera (meeting Kael's eyes through radio). Expression: focused, slightly concerned (Mission 1 narrative context — first Kael contact).

Environment (minimal): Safehouse interior suggestion — warm amber lighting from a single overhead lamp at top of frame. Concrete wall texture behind her. A few papers on table. Keep environment minimal — this is a character animation, not a full scene render.

Background: Dark grey concrete, single amber overhead light glow baked in.
Art style: Semi-realistic painterly sprite, 2px black outline.
```

---

## CUTSCENE — STANDING WITH MAP (Mission 6 Field Contact)

```
Isometric 2.5D full-body cutscene frame of Rina, standing and looking at a tactical map. South-facing (toward viewer), 30-degree pitch.

Preserve exactly from reference: all costume elements. Map case strap visible.

Pose: Standing, weight on left foot. Right hand holding an unfolded tactical map at chest height (map is a flat paper sheet with grid lines and marked positions — minimal detail). Left hand pointing to a position on the map. Head slightly down toward map, eyes flicking up toward camera. Expression: Neutral — delivering intelligence.

Background: Field exterior — cold grey ambient light. Suggestion of concrete or industrial structure behind her (dark wall surface). No environment clutter.
Art style: Semi-realistic painterly sprite, 2px black outline.
```
