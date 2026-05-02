# NOTES — RINA

---

## Pipeline Notes

- Rina is a **portrait and cutscene character** for Chapter 1. No gameplay sprites are needed now.
- Her design must be production-ready and extendable for Chapter 2 (potential playable character or on-screen NPC).
- Visual contrast with Kael is critical: Kael = military, asymmetric, mechanical, olive/grey. Rina = civilian, symmetrical, human, charcoal/navy.
- The Rift patch on her left arm is the only faction visual marker on her person — keep it subtle but consistent.

---

## Portrait Variants Required (Chapter 1)

| Variant | Emotion | When Used |
|---|---|---|
| Neutral | Alert, scanning | Default mission HUD |
| Speaking | Slight mouth open | Active radio dialogue line |
| Alarmed | Eyes wider, forward lean | Urgent warning moments |
| Grim | Eyes slightly lowered | Deaths, mission failures, bad news delivery |
| Captured (final) | Wrists bound, slight defiance in expression | Chapter 1 ending cutscene only |

Each portrait is: 256×256 px generated, displayed at 128×128 px in-game.
All portraits use the same framing: chest-up, three-quarter left-facing, on dark background.
Only expression and pose differ — costume, features, lighting must be IDENTICAL across all variants.

---

## HUD Portrait Frame

In-game the portrait appears in the bottom-left corner of the HUD during radio communication, framed in a hexagonal border (black with a thin Rift white line border). The border is applied by the UI system — art team delivers portrait only, no border baked in.

---

## Animation Priority (Chapter 1)

1. Neutral portrait (first needed — used in all mission HUDs)
2. Speaking portrait (2-3 frame mouth flap for voiced lines)
3. Alarmed portrait
4. Grim portrait
5. Cutscene: seated at console (Mission 1 safehouse)
6. Cutscene: standing with map (Mission 6 sewer contact)
7. Captured portrait (Chapter 1 ending — lowest priority, last scene)

---

## Developer Notes

- Voice actress for Rina: to be confirmed. Radio effect (slight compression + bandwidth limit) applied in engine to all Rina audio — not processed in audio delivery.
- Rina's portrait mouth animation (Speaking variant) is a 2-frame alternation: closed mouth → slightly open. Applied by engine based on voiceover amplitude. Art delivers only: closed mouth frame and open mouth frame.
- In the **Captured** final portrait: Rina's wrists should show visible restraints (SENTINEL-style — thin black polymer cuffs). Her expression should read as defiance, not defeat. She is not broken.

---

## Known Open Questions (for art director review)

- Will Rina appear in any in-engine real-time scene in Chapter 1, or all pre-rendered? (Currently planning: all portraits are 2D sprites; cutscenes are in-engine using character sprites on scene objects.)
- Rift patch design: needs finalization with narrative team (the "fracture line" motif is a placeholder — confirm before art lock).
- If Rina becomes playable in Chapter 2, plan for 8-direction movement sprites, attack sprites for SMG/sidearm, and a more worn/field-ready version of the jacket (possible shoulder rig addition).
