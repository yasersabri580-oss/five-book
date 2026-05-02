# ANIMATION PROMPTS — FUEL TANK

---

## Animation Status

**No animation required for the tank sprite itself.**

The intact → leaking state is a sprite swap. The burning state (after destruction) is handled by engine-spawned fire VFX on top of the burnt tank sprite — no animation is part of the tank object itself.

---

## Static Sprite Summary

| State | Sprite | Animation |
|---|---|---|
| Intact (south-facing) | `fueltank_intact.png` | None |
| Leaking (south-facing) | `fueltank_leaking.png` | None |
| Intact (east-facing) | `fueltank_intact_east.png` | None |
| Leaking (east-facing) | `fueltank_leaking_east.png` | None |
| Burning wreck | `fueltank_burnt.png` | Fire VFX spawned by engine over this sprite |

---

## Notes for Art Team

- `fueltank_burnt.png`: The tank in its post-destruction state. The tank body is charred/blackened (#1A1A18). The hazard diamond is burnt off. The cylinder has a large rupture hole (irregular dark gap) on the south face. Saddle supports remain (they are steel and don't burn away). No flame baked into the sprite — fire VFX handles the visual fire.
- The fire zone on destruction is 2 tile radius — the engine spawns a separate ground fire decal (`fire_zone_decal.png`) — this is a VFX/environment decal, not part of this object's art pipeline.
