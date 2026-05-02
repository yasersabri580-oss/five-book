# ANIMATION PROMPTS — SECURITY DOOR

---

## Animation Status

**Animation required: Open sequence (6 frames). Indicator light state change (2 frames).**

---

## ANIMATION 1 — DOOR OPEN SEQUENCE (6 frames)

```
6-frame opening animation for the SecurityDoor (south-facing orientation). This animation plays once when the door is unlocked and the player approaches. Based on the canonical SecurityDoor reference image. Preserve all visual identity.

CAMERA: Isometric 2.5D, 30-degree pitch, south-east facing. Same as reference.
ART STYLE: Same as reference sprite — crisp 2px outline, baked isometric lighting, dark steel palette.

Context: Door opens by sliding RIGHT (into the right wall pocket). The indicator light simultaneously transitions from RED to GREEN (can be handled as a separate light sprite swap concurrent with this animation).

FRAME 1 — CLOSED:
Door in fully closed/locked position (identical to the Closed/Locked state in the reference image). Door fills the opening completely.

FRAME 2 — SLIGHT VIBRATION:
The door very slightly judders — 2px shift to the left, as if the electromagnetic lock is releasing. Almost imperceptible. The door still fills the opening.

FRAME 3 — BEGINS SLIDING (25% open):
The door has moved right — 25% of the opening is now clear (dark interior visible on the left side). The right 75% of the opening is still covered by the door slab. The door's left edge has moved right by 0.25 tile.

FRAME 4 — MID-SLIDE (50% open):
50% of the opening is clear. Door slab is centered — equal amounts of opening on the left and dark interior. The slab is beginning to slide into the right wall pocket.

FRAME 5 — NEARLY OPEN (80% open):
Only 20% of the opening on the right is still covered. The slab is mostly inside the right wall pocket. The door frame posts are clearly visible.

FRAME 6 — FULLY OPEN:
Door slab is fully hidden inside the right wall pocket. Only the door frame remains (two posts + header). Opening is completely clear — dark interior beyond. This frame is held indefinitely until the door closes.

Total frames: 6
Frame timing: 0.07s per frame (total 0.42s — snappy)
Loop: No. Plays once on open. If a close sequence is needed, reverse the frame order (close is same frames in reverse).
Direction: Door slides right for south-facing variant. Door slides north for east-facing variant (separate animation).
```

---

## ANIMATION 2 — INDICATOR LIGHT STATE CHANGE (2 frames)

```
2-frame indicator light transition for the SecurityDoor. Plays concurrently with the open animation (Frame 1 → Frame 2 timing).

FRAME 1 — LOCKED (RED):
Indicator light box shows solid red (#C42020) with a very faint 2px glow halo.

FRAME 2 — UNLOCKED (GREEN):
Indicator light box shows solid green (#20C440) with a very faint 2px glow halo.

Transition: Instant swap (no transition frames needed — the lock-release moment is Frame 2 of the door animation).
```

---

## Animation State Machine (Unity Animator Reference)

| State | Clip | Transition |
|---|---|---|
| `door_closed` | Static — `door_closed.png` | → `door_opening` when `DoorUnlock` trigger fires |
| `door_opening` | 6-frame clip, plays once | → `door_open` when clip ends |
| `door_open` | Static — `door_open.png` | Held indefinitely (door does not auto-close in Chapter 1) |
