# ANIMATION PROMPTS — PROXIMITY MINE

---

## Animation Status

**Minimal animation required: LED slow pulse (armed) and LED rapid flash (triggered warning).**
Both are 2-frame loops on only the LED element.

---

## ANIMATION 1 — LED SLOW PULSE (Armed State, 2 frames)

```
2-frame looping LED pulse animation for the ProximityMine in armed state. Only the LED element changes — the mine body is completely static.

FRAME 1 — LED DIM (between beats):
LED at minimum brightness: #6A0808 (very dark red). No glow halo. This frame represents the "resting" phase of the heartbeat rhythm.

FRAME 2 — LED PEAK (pulse beat):
LED at maximum slow-pulse brightness: #C42020 (bright red). 2px soft glow halo (#8A1010 fading outward). The glow halo radius is 2px beyond the LED circle edge.

Frame timing: Frame 1 holds 1.6s, Frame 2 holds 0.25s. (Total cycle: 1.85s — one slow heartbeat approximately every 2 seconds.)
Loop: Yes — continuous in armed state.
Purpose: A slow, subtle pulse that attentive players will notice but rushing players may miss.
```

---

## ANIMATION 2 — LED RAPID FLASH (Triggered Warning, 2 frames)

```
2-frame rapid looping flash animation for the ProximityMine in triggered state (player within 0.5 tile, 0.8s countdown to explosion).

FRAME 1 — LED OFF (flash off):
LED at off state: #1A0808 (near-black — the LED is in its dark cycle). No glow.

FRAME 2 — LED BRIGHT FLASH (flash on):
LED at maximum alert brightness: #FF2020 (full bright red). 3–4 px glow halo (#C01010 fading). This is significantly brighter than the slow pulse peak.

Frame timing: Frame 1 holds 0.08s, Frame 2 holds 0.08s. (One flash per 0.16s — approximately 6 flashes per second over the 0.8s warning window ≈ 5 flashes before detonation.)
Loop: Yes — plays for 0.8s, then mine detonates (engine handles detonation, not animation).
Audio: A rapid beep sound plays synchronized to Frame 2 (each LED-on frame triggers a beep — engine audio system concern, not art).
```

---

## Static Sprites Summary

| State | Sprite | Animation |
|---|---|---|
| Armed | `mine_armed.png` (body) | 2-frame LED slow pulse |
| Triggered (warning) | `mine_armed.png` (body, unchanged) | 2-frame LED rapid flash |
| Disarmed (EMP) | `mine_disarmed.png` (LED off) | None |
| Half-hidden | `mine_halfhidden.png` | 2-frame LED slow pulse (LED still visible) |

Note: The LED animation can be a separate child `SpriteRenderer` overlaid on the mine body, allowing the LED to animate independently without redrawing the whole mine sprite each frame.
