# ANIMATION PROMPTS — SUPPLY BOX

---

## Animation Status

**Animation required: lid-open sequence (3 frames, plays once on interaction).**
Closed state and open/depleted state are static sprites.

---

## LID OPEN ANIMATION — 3 Frames (FORGE variant; Rift variant uses same frame structure)

```
3-frame one-shot animation for the SupplyBox when the player interacts (presses E). Based on the canonical reference image. Preserve all visual identity — only the lid changes between frames.

CAMERA: Isometric 2.5D, same as reference.
ART STYLE: Same as reference sprite — crisp 2px outline, baked lighting, military green body.

Context: Player presses E. This animation plays once (0.2s total). After completion, the open/depleted static sprite is held indefinitely.

FRAME 1 — LID BEGINNING TO OPEN:
The clasps on the south face are unlatched — the clasp bars swing down (now hanging at 45° below horizontal). The lid has just begun to lift: it is at approximately 15° open from horizontal (barely open). The lid front edge (the clasp edge) has just started to rise, and a thin dark gap is visible between the lid and the south face. The interior is not yet visible.

FRAME 2 — LID FULLY SWINGING:
The lid is at approximately 70° open (past vertical midpoint, swinging backward). The interior is now partially visible — a dark interior recess. The lid clasps are now fully swung and trailing. The lid handle is arcing through its travel path. This is the peak motion frame.

FRAME 3 — LID FULLY OPEN / SETTLED:
The lid is in its final open position (approximately 110° from closed — angled slightly past vertical, leaning back toward the north). This matches the OPEN state sprite from the reference image. The clasps hang loosely. The interior is fully visible with 2–3 spent shell casings.

Total frames: 3
Frame timing: Frame 1 (0.06s), Frame 2 (0.07s), Frame 3 (0.07s) — total 0.2s
Plays once. Ends by holding Frame 3 (transitions to the static open/depleted sprite, which is visually identical to Frame 3).
Loop: No.
```

---

## Static Sprites Summary

| Sprite | Filename | State |
|---|---|---|
| FORGE closed | `supplybox_forge_closed.png` | Available — ready to interact |
| FORGE open | `supplybox_forge_open.png` | Depleted — lid open, interior empty/spent casings |
| Rift closed | `supplybox_rift_closed.png` | Available |
| Rift open | `supplybox_rift_open.png` | Depleted |
| Lid open animation (FORGE) | `supplybox_forge_lidopen_sheet.png` | 3 frames, spritesheet |
| Lid open animation (Rift) | `supplybox_rift_lidopen_sheet.png` | 3 frames, spritesheet (same frames, Rift colors) |
