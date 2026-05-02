# CHARACTER PROFILE — RINA

---

## Character Name
**Rina** *(surname withheld — Rift protocol)*

---

## Role in the Game
**Allied NPC — Rift Strategist and Radio Contact.**
Rina does not appear on the battlefield in Chapter 1. She is Kael's primary contact throughout all 10 missions, providing mission briefings, tactical updates, and narrative commentary via radio. She appears in **cutscenes and static portrait UI panels** (mission briefing screens, radio call HUD).

She may become a playable or on-screen character in Chapter 2 — her visual design must be production-ready and extendable.

---

## Visual Identity
Rina is a survivor-turned-tactician. She does not look like a soldier — she looks like someone who became a strategist because she had to, not because she trained for it. Her appearance is intelligent, alert, and deliberately non-militaristic — a visual contrast to Kael's worn soldier aesthetic.

- **Face:** Sharp features, high cheekbones, dark eyes that are always scanning. A small scar along the left jawline (knife wound, old). Dark complexion — warm olive-brown skin tone. Short, practical hair: close-cropped on the sides, slightly longer on top, unstyled.
- **Clothing:** Civilian-base layers modified for field use. Dark charcoal grey fitted jacket with worn collar, zipped 3/4 up. No military insignia. A small Rift patch on the upper left arm — a stylized jagged line (lightning bolt meets fracture line) in white on black fabric.
- **Accessories:** Over-ear tactical headset on right ear — matte black, simple civilian model with a small black mic arm. A small earpiece visible in the left ear. Map case slung over left shoulder (for cutscenes — not always visible). Fingerless gloves, dark grey.
- **Eyes:** Alert, calculating. Slight dark circles — she does not sleep enough.
- **Build:** Lean and contained. Not fragile — she has clearly lived rough. Posture is upright and controlled, never relaxed.

---

## Personality
Rina is the operational brain of every mission. She gives concise intelligence with no wasted words, acknowledges danger without dramatizing it, and delivers bad news directly. She trusts Kael and he trusts her, though both keep their emotional vulnerability guarded. Under pressure she is calmer than circumstances warrant — a coping mechanism she never acknowledges.

She carries survivor's guilt from the early days of FORGE's rogue period — she got out of Verak before the lockdown; others in her network did not.

---

## Story Relevance
- Rina is Kael's primary connection to the wider world throughout Chapter 1.
- She receives the SENTINEL schematics Kael transmits at Mission 9 and broadcasts them publicly.
- In the final moments of Chapter 1, she is captured by SENTINEL — her last radio line to Kael is the emotional endpoint of the chapter.
- Her capture is the hook into Chapter 2's narrative.

---

## Gameplay Purpose
- Voiced radio lines during all 10 missions — mission start briefings, mid-mission updates, plot twists, encouragement, warnings.
- **Static portrait UI panel** during radio calls (shown in HUD corner — 128×128 px portrait, isometric-adjacent angle or slight three-quarter front view).
- **Full-body cutscene appearance** (Missions 1, 6, and 10 endings at minimum — shown in Rift safehouse or in a vehicle cockpit via transmission screen).
- **No combat animations needed for Chapter 1.** Design must support future combat/movement animations for potential Chapter 2 gameplay.

---

## Size / Silhouette / Body Type
- **Height:** Medium (approximately 1.70m)
- **Build:** Lean, angular. Not bulky. Silhouette reads as sharp and precise.
- **Sprite height (if playable):** 2.8 tiles standing.
- **Portrait framing:** Head + shoulders visible in HUD portrait. 128×128 px portrait at game display.

---

## Clothing / Armor / Accessories
| Item | Description |
|---|---|
| Charcoal jacket | Dark grey (#2E2E2E), fitted, worn collar, 3/4 zip |
| Rift patch | Left upper arm — white jagged fracture line on black oval |
| Tactical headset | Right ear, matte black, civilian model, mic arm |
| Left earpiece | Small black in-ear unit |
| Fingerless gloves | Dark grey (#303030), worn at knuckle edges |
| Map case | Left shoulder strap, worn leather tan (#7A6040) — cutscene prop |
| Undershirt | Dark navy (#1A2030), crew neck, visible at collar |

---

## Color Palette
| Element | Color |
|---|---|
| Jacket | Dark charcoal (#2E2E2E) |
| Undershirt | Dark navy (#1A2030) |
| Gloves | Dark grey (#303030) |
| Skin | Warm olive-brown (#7A5A3A) |
| Eyes | Near-black brown (#2A1A10) |
| Hair | Dark near-black brown (#1A1008) |
| Rift patch | Black background, white fracture line (#FFFFFF) |
| Headset | Matte black (#1A1A1A), matte silver details |
| Map case strap | Worn tan leather (#7A6040) |
| Scar (left jaw) | Slightly lighter than skin (#8A6A4A), faint |

---

## Weapon / Tool
- **Chapter 1:** No weapon visible. Rina operates as rear-command only.
- **UI context:** She holds a tablet or map in some cutscene frames (civilian tablet, cracked screen, tactical overlay displayed).
- **Future-proofing:** If Chapter 2 requires combat, her weapon would be a compact submachine gun (to be defined at that stage).

---

## Movement Style
*(Chapter 1 cutscene only — no gameplay movement)*
- Deliberate, economical movement. Does not fidget or waste motion.
- Seated at a field console or standing over a map — her body is still but mentally engaged.
- When the situation gets bad: she leans forward. When she has to deliver bad news: she leans back slightly, recalibrates.

---

## Combat Style
*(Not applicable — Chapter 1)*

---

## Animation Requirements
For Chapter 1, Rina requires:

| State | Type | Notes |
|---|---|---|
| Portrait — Neutral | Static frame | Default HUD portrait — alert, neutral expression |
| Portrait — Speaking | Animated (2-3 frame mouth movement) | For voiced lines — minimal mouth movement |
| Portrait — Alarmed | Static frame | Used for urgent/dangerous moments |
| Portrait — Grim | Static frame | Used for bad news / deaths |
| Cutscene — Seated at console | Full body, 4-5 frames idle | Rift safehouse scene |
| Cutscene — Standing with map | Full body, 3-4 frames idle | Mission briefing cutscene |
| Cutscene — Captured (final) | 1 frame static | Chapter 1 ending — in SENTINEL custody, hands bound |

---

## Direction Requirements
**Portrait panels:** Frontal three-quarter only (facing slightly left — standard portrait convention).
**Cutscene full body:** Isometric 2.5D, same camera as Kael. South-facing (toward viewer) primary.

---

## Reference Image Requirements
See `reference_prompt.md` for the full reference image generation prompt.

The reference image must establish:
- Exact facial features (sharp, scar on left jaw, dark eyes)
- Hair style (close-cropped sides, slightly longer top)
- Jacket + headset + gloves
- Rift patch design
- Color palette
- Three-quarter portrait framing (for HUD use)
- Art style matching Kael's semi-realistic painterly style

---

## Technical Constraints for Consistency
- Portrait sprite: **128×128 px** display size, generated at **256×256 px** for editor preview.
- Portrait must be readable at 128×128 — no fine detail that disappears at that size.
- Rift patch must be recognizable on the portrait at 128×128 — keep it as a simple silhouette.
- Facial scar on left jaw must be subtle — not a defining disfigurement, a history marker.
- The headset right-ear placement must be consistent across all portraits.
- In all cutscene animations, lighting matches the environment (safehouse = warm amber; field = cold grey).
- Kael and Rina must be visually contrasted: Kael = military/worn/asymmetric/mechanical; Rina = civilian/controlled/symmetrical/human.
