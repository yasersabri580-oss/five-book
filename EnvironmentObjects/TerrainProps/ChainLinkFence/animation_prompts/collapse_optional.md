# ANIMATION PROMPTS — CHAIN-LINK FENCE

---

## Animation Status

**No animation required for the standard intact and crushed states.**

The transition from intact to crushed is handled as an instant sprite swap by the game engine (no animation needed). An optional collapse animation is noted below as a low-priority enhancement.

---

## Optional Enhancement — Collapse Animation (Low Priority)

If animation budget allows, a short collapse sequence adds polish. This is **not required for Chapter 1 launch.**

### COLLAPSE SEQUENCE — 3 Frames

```
Animation of a chain-link fence segment collapsing under vehicle impact. Based on the canonical reference image for ChainLinkFence. Preserve all visual identity from the reference.

CAMERA: Isometric 2.5D, 30-degree pitch, south-east facing. Same as reference.
ART STYLE: Same style as reference sprite — crisp 2px outline, baked lighting, stylized game asset.

FRAME 1 — IMPACT:
The fence segment is struck. The left-side post buckles outward (tilts 20° toward the south face, leaning toward the camera). The mesh distorts at the impact point — subtle warping at center-left. The fence is still standing but visibly stressed.

FRAME 2 — MID-FALL:
The fence is at 45° angle — falling toward south (toward camera/viewer). Posts are bent severely. Mesh is heavily distorted — buckled diamonds, irregular shape. Barbed wire tangles. The concrete footing on one side lifts slightly off the ground.

FRAME 3 — CRUSHED (Final State):
Matches the CRUSHED variant sprite from the reference sheet. Fence is fully flat on the ground. Posts bent sideways. Mesh is a distorted tangled mass. This frame transitions to the static crushed sprite.

Total frames: 3
Frame timing: 0.08s per frame (fast collapse — about 0.25s total)
Loop: No. Plays once then holds on Frame 3 (or transitions to static crushed sprite).
Direction: South-facing collapse (toward camera) consistent with isometric camera.
```

---

## Static Sprite Variants Required

| Sprite | Filename | Description |
|---|---|---|
| Intact Segment | `fence_segment.png` | Standard upright mesh panel, no posts |
| End Post | `fence_post_end.png` | Terminal post with footing |
| Mid Post | `fence_post_mid.png` | Shared post between two segments |
| Crushed | `fence_crushed.png` | Flattened destroyed state |
