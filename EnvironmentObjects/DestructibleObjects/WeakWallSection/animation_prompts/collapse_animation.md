# ANIMATION PROMPTS — WEAK WALL SECTION

---

## Animation Status

**One animation required: the collapse sequence.**

The intact → heavily damaged transition is a sprite swap (no animation). But the final collapse (heavily damaged → destroyed) is a significant gameplay moment — a 4-frame collapse animation is recommended and included here.

---

## COLLAPSE ANIMATION — 4 Frames

```
4-frame collapse animation for the WeakWallSection. Based on the canonical reference image for this object. Preserve all visual identity from the reference sprite.

CAMERA: Isometric 2.5D, 30-degree pitch, south-east facing. Same as reference.
ART STYLE: Same style as reference sprites — crisp 2px outline, baked lighting, brick material, dusty red-brown color palette.

Sequence: plays ONCE when the wall's HP reaches 0. After the sequence ends, the static Rubble Pile sprite is placed at the base.

FRAME 1 — FINAL CRACK:
The heavily damaged wall (use Panel 2 from reference as base). New: a bright burst-crack at the center of the south face — a white-grey (#D8D0C0) radiating star-crack, as if a tank shell just hit. The crack is sharp and bright (impact flash). Brick fragments just beginning to move — 2–3 small bricks at the top center starting to separate from the wall body (shown slightly displaced from their normal position, angled outward).

FRAME 2 — TOP COLLAPSE:
The top third of the wall (upper 0.5 tiles) has broken away. The remaining 1.0 tile lower section still stands. The broken top section is shown as mid-fall — fragments of the upper section at a 45° angle, halfway between standing and ground. Brick fragments and mortar dust trail in the air (simple static dust cloud silhouette in light grey #D8D0C0, no animation — just the frame shape at mid-fall). The lower section shows raw jagged breaks at its new top edge.

FRAME 3 — FULL FALL:
The entire wall section is now falling — shown as a mass of bricks at a steep angle (70° from vertical), lower section breaking away from the ground. Dust cloud widens — a broader grey dust silhouette obscuring the lower half. The bricks are no longer a coherent wall shape — they are a chaotic mass.

FRAME 4 — IMPACT / RUBBLE:
The bricks have landed. A dense dust cloud (wide, low, grey-white #D8D0C0 to transparent edges) covers the impact zone, obscuring what will become the rubble pile. This frame transitions to the static Rubble Pile sprite as the dust dissipates (dust dissipation is a VFX particle — separate from this animation).

Total frames: 4
Frame timing: 0.1s per frame (fast collapse — 0.4s total)
Loop: No. Plays once. Ends by being replaced with the Rubble Pile static sprite.
Dust elements in frames 2–4: flat silhouette shapes, not animated particles. The cloud shape changes between frames only.
```

---

## Static Sprite Summary

| State | Sprite | Animation |
|---|---|---|
| Intact | `weakwall_intact.png` | None |
| Heavily Damaged | `weakwall_damaged.png` | None |
| Collapse | `weakwall_collapse_sheet.png` | 4 frames, plays once |
| Rubble Pile | `weakwall_rubble.png` | None (permanent ground decal) |
