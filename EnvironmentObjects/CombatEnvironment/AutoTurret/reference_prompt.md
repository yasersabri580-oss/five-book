# REFERENCE IMAGE PROMPT — AUTO TURRET

---

## Purpose
This prompt generates the **canonical reference image** for the AutoTurret.
The separate pedestal and turret-body sprites are critical — the turret body rotates independently in-game.

---

## Reference Image Generation Prompt

```
2.5D isometric game asset — Auto Turret (pedestal + rotating body, all states) for the game IRON BREACH.

CAMERA: Isometric 2.5D, 30-degree pitch, south-east facing. Objects shown as standalone sprites on flat near-black background (#121212). No environment.

ART STYLE: Stylized game asset. Crisp 2px black outline. Baked isometric lighting on the pedestal (top lighter, sides darker). The turret body has its own baked lighting assuming it is facing south (standard facing). The sensor lens is self-illuminated — brighter than ambient, with a glow halo. NOT pixel art. NOT photorealistic. This object must look like a cold, automated killing machine — angular, dark, industrial. The red lens is the most important visual element.

REFERENCE SHEET: Three rows.

ROW 1 — COMPONENT BREAKDOWN (for separation into game sprites):

LEFT PANEL — STATIC PEDESTAL:
- Cylindrical base, 0.5 isometric tile diameter, 0.4 tiles tall.
- Dark steel (#2A2E32). Top face: flat circle, slightly lighter (#3A4040). Side: faint seam lines running vertically (suggesting the base is a welded assembly). Attachment bolts at the base: 4 small dark circles (#1A1A18) at N/S/E/W positions on the base ring.
- Armored mounting ring at the top of the pedestal (where the turret body sits): a raised ring ridge, slightly darker than the pedestal body.

CENTER PANEL — TURRET BODY (south-facing / camera default):
- Boxy armored housing: 0.5 tile wide × 0.4 tile deep × 0.3 tile tall. Very dark blue-black (#1A2028).
- FRONT FACE (south-facing): the camera-facing face of the turret. In the center: a convex red-orange sensor lens. The lens is circular, 15% of the front face width. Bright center point (#FF6020 bright orange-red), graduating to darker red at the edge (#C02010). A 1–2 px soft glow halo of the same orange-red extends beyond the lens circle. This lens is the IDENTITY of the turret — make it prominent.
- A thin FORGE red stripe (#8A1010) runs along the top edge of the housing on the front and both side faces.
- Two parallel gun barrels extend from the front face: matte dark grey (#2A2A2A), each barrel is a simple elongated rectangle in isometric perspective. Each barrel has a slightly lighter highlight on the top edge. The barrels are the clearest "this shoots things" silhouette cue.
- Angular armor side panels on the left and right faces — slightly beveled edges, same dark color family.

RIGHT PANEL — ASSEMBLED VIEW (pedestal + turret body together):
- The turret body seated on the pedestal. Shows how they align. The assembled turret total height is 0.7 tiles.

ROW 2 — DAMAGE AND DISABLED STATES:

LEFT PANEL — DAMAGED STATE (60 HP):
- Same assembled view. The turret body is damaged: the LEFT barrel is bent 30° downward (drooping slightly). A crack on the front face housing near the sensor lens. The lens is still glowing but slightly dimmer (#D03010 duller red-orange). The FORGE stripe on the left side is scraped off.

CENTER PANEL — DISABLED STATE (EMP / terminal hack):
- Assembled view. Turret barrels are angled to a neutral forward position (not scanning). The sensor lens is OFF — replaced with a dull amber glow (#604000), very dim, no halo. The whole housing looks slightly less active.

RIGHT PANEL — DESTROYED STATE (0 HP):
- The turret body is heavily damaged — blackened (#0A0C0E, scorched). Both barrels are drooping downward. The sensor lens is completely dark (#0A0A0A, no glow). Scorch marks (dark radial pattern #0A0806) spreading from the lens and barrel area. The pedestal is intact (it is hardened). The turret body is visibly dead.

COLOR PALETTE:
- Pedestal: #2A2E32
- Pedestal top: #3A4040
- Turret housing: #1A2028
- Turret housing highlights: #242C34 (barely lighter face)
- Barrel: #2A2A2A
- Barrel highlight: #3A3A3A (top edge)
- FORGE stripe: #8A1010 (dark red stripe)
- Sensor lens (active): #FF6020 center → #C02010 edge, glow halo #C02010 soft
- Sensor lens (disabled): #604000 (dull amber, very dim)
- Sensor lens (destroyed): #0A0A0A (dark, no glow)
- Damaged scorch: #0A0806
- Outline: #0A0A0A (2px)

SCALE REFERENCE: Include a faint isometric tile grid ghost.

OUTPUT: Two rows, six panels total. All labeled. Dark background.
```

---

## Checklist — What This Prompt Establishes

- [x] Camera angle (isometric 30-degree, SE facing)
- [x] Art style (stylized, self-illuminated sensor lens, angular militaristic)
- [x] Component breakdown (pedestal separate from turret body — for in-game rotation)
- [x] Assembled view
- [x] All states: active, damaged, disabled, destroyed
- [x] Critical: sensor lens is the identity element — prominent and glowing
- [x] Twin barrels (primary silhouette cue)
- [x] Color palette (all elements)
- [x] Scale reference
- [x] Dark background
