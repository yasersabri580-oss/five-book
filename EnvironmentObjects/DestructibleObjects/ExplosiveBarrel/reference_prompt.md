# REFERENCE IMAGE PROMPT — EXPLOSIVE BARREL

---

## Purpose
This prompt generates the **canonical reference image** for the ExplosiveBarrel.
The red hazard color and warning stencil are the most critical visual elements — they must be immediately readable.

---

## Reference Image Generation Prompt

```
2.5D isometric game asset — Explosive Barrel (two variants: single and double) for the game IRON BREACH.

CAMERA: Isometric 2.5D, 30-degree pitch, south-east facing. Objects shown as standalone sprites on flat near-black background (#121212). No environment.

ART STYLE: Stylized game asset. Crisp 2px black outline. Baked isometric lighting: top face is lightest, south face is mid-tone, east face is darkest. Cylindrical form — the barrel's south face curves slightly. NOT pixel art. NOT photorealistic. Clean, bold, immediately readable as a danger object. The red color must be the most visually striking element in the image.

REFERENCE SHEET: Three panels side by side.

PANEL 1 — INTACT BARREL (single):
- Cylindrical steel drum. 0.5 isometric tile footprint, 0.9 tiles tall.
- Two rolled circumferential ridges (rings) around the barrel body: one at 1/4 height from bottom, one at 3/4 height from bottom. These rings are darker than the main body and create a strong readable ring silhouette.
- BODY COLOR: Bright danger red (#C42020). This is the primary color — bold and saturated. The barrel is RED. Top face: lighter red (#D83030). East face: dark red (#7A1010). South face: base red (#C42020).
- Diagonal hazard stripes on the SOUTH face: 3 diagonal stripes angled at 45°, alternating RED (#C42020) and WARNING YELLOW (#E8B800). The yellow stripes are about 20% of the south face width each. The stripes run from upper-left to lower-right across the south face, between the two ring ridges.
- Hazard stencil on the south face, between the ring ridges, centered: a simple skull silhouette (white #F0F0F0, simplified — circular skull head, two dark eye sockets, simple crossbones below). The skull must be readable at 32×32 px. Keep it as a flat simple silhouette, not detailed.
- Flat top face with two circular bung holes: one center and one at 1/3 position. Both are dark (#2A0A0A) circles. Optional: a rust-dark drip stain running down from the right bung hole toward the south face, color #5A1010.
- Base: a slight corrosion/rust darkening at the very base ring (#5A1010 rust orange-red on dark).
- Overall: the barrel looks USED and slightly aged but structurally intact. Not pristine, not destroyed.

PANEL 2 — DAMAGED BARREL (50% HP state):
- Same barrel, visibly damaged. Keep shape and size identical.
- A dent on the south face: one of the ring ridges is bent inward on the left side — a visible impact dent, concave area on the barrel.
- One bung hole has a dripping stain — larger than the intact version. The drip stain runs down the south face and is slightly greenish-dark (#3A1A0A oily dark liquid), suggesting fuel/oil leaking.
- The barrel surface has additional chipping: the red paint is chipped near the dent revealing the raw metal underneath (#4A3A30 dark grey metal showing through).
- The hazard stripes are still visible but one is partially obscured by the dent damage.
- Skull stencil: still readable but slightly smudged/scratched.

PANEL 3 — DOUBLE BARREL VARIANT (two intact barrels side by side):
- Two barrels from Panel 1, placed side by side on a shared 1×0.5 tile footprint. The barrels touch at their sides.
- One barrel faces south (standard), one is rotated slightly (10°) to show it is a separate object, not a mirrored duplicate — small visual break in strict symmetry.
- Same visual treatment as Panel 1 on both. No additional damage.

COLOR PALETTE:
- Barrel body (south face): #C42020 (danger red)
- Barrel top face: #D83030 (lighter red)
- Barrel east/shadow face: #7A1010 (dark red)
- Ring ridges: slightly darker than face color (#A01818 front ring)
- Hazard stripes: #E8B800 (warning yellow)
- Skull stencil: #F0F0F0 (white, flat silhouette)
- Bung holes: #2A0A0A (dark)
- Drip stain (intact): #5A1010 (rust-red)
- Drip stain (damaged): #3A1A0A (dark oily liquid)
- Metal showing through chip: #4A3A30 (raw grey-metal)
- Outline: #0A0A0A (2px)

SCALE REFERENCE: Include a faint isometric tile grid ghost under each panel.

OUTPUT: One horizontal reference sheet, three panels: Intact, Damaged, Double-Variant. All labeled. Dark background.
```

---

## Checklist — What This Prompt Establishes

- [x] Camera angle (isometric 30-degree, SE facing)
- [x] Art style (stylized, bold, immediately readable as danger)
- [x] Intact, damaged, and double-barrel variants
- [x] Critical: red body color with hazard stripes and skull stencil
- [x] Material detail (rings, bung holes, drip stain, paint chipping)
- [x] Color palette (all elements with hex codes)
- [x] Damage state details (dent, larger drip, chipped paint)
- [x] Scale reference (tile grid ghost)
- [x] Dark background
