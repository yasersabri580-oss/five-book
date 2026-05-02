# REFERENCE IMAGE PROMPT — SECURITY DOOR

---

## Purpose
This prompt generates the **canonical reference image** for the SecurityDoor.
Both orientation variants and all key states must be established here.

---

## Reference Image Generation Prompt

```
2.5D isometric game asset — Security Door (two orientations, three states) for the game IRON BREACH.

CAMERA: Isometric 2.5D, 30-degree pitch, south-east facing. Shown as a standalone set on flat near-black background (#121212). No full environment, but show the door set into a single ConcreteWallSegment-style wall section on each side (so the door opening and frame context is visible).

ART STYLE: Stylized game asset. Crisp 2px black outline. Baked isometric lighting: top faces are lightest, south face mid-tone, east face darkest. Brushed steel look — subtle parallel directional lines on the steel face panels. NOT pixel art. NOT photorealistic. Heavy, industrial, FORGE-controlled architecture feel. Consistent with the IRON BREACH dieselpunk palette.

REFERENCE SHEET: Two rows.

ROW 1 — SOUTH-FACING DOOR (facing the camera — fits a south-wall opening):
Three panels:
- LEFT PANEL: CLOSED / LOCKED STATE — The full door filling the opening. Heavy steel slab door with 3 horizontal armored panel sections visible on the south face. Each panel section has beveled edges and a slightly lighter center area (#3A4044) vs the border (#2A2E32). On the left door frame post: a small indicator light box (a flat square box, 5×5 px in game, set into the frame). The indicator light is RED (#C42020) — backlit, a clean small square of bright red on the dark frame. An angular stylized symbol (FORGE faction — a downward-pointing triangle with three horizontal bars, stencil-style) on the center panel of the door. Very subtle — same dark steel color family, slightly lighter. The door fills the 1-tile opening completely — no gaps.
- CENTER PANEL: UNLOCKED / OPENING STATE — The door mid-slide. The door slab is partially slid into the right wall section (sliding right). The left portion of the opening is clear (show dark interior visible beyond). The right portion still has the door covering it. The indicator light on the left frame post is now GREEN (#20C440). The door slab itself shows the same paneled face, now at about 50% position mid-slide.
- RIGHT PANEL: FULLY OPEN STATE — The door slab is fully slid into the right wall pocket (not visible). Only the door frame remains — two thin vertical frame posts (left and right of the opening) and a horizontal header above. The indicator light is GREEN. The opening is fully clear — dark interior visible beyond.

ROW 2 — EAST-FACING DOOR (fits an east-wall opening — the door faces the east):
- Same three panels as Row 1, but oriented for the east-wall variant. The door face (with panels and FORGE emblem) faces east (the darker shadow face in isometric). The indicator light is visible on the south-facing frame post instead of the left post.
- Color note: the east-facing door face is the shadow face — use the darker east-face color (#1E2428 very dark steel), but the panel bevels and indicator light must still be visible.

COLOR PALETTE:
- Door body: #2A2E32 (dark steel grey)
- Panel highlights/bevels: #3A4044 (slightly lighter steel)
- Door frame: #1A1E22 (near-black steel frame)
- Indicator light: RED = #C42020 (locked), GREEN = #20C440 (unlocked). The light glows slightly — add a very faint 2px glow halo around the light square.
- FORGE emblem: #323840 on #2A2E32 (subtle — same color family, slight contrast)
- Opening interior visible: #0A0A08 (dark, no detail inside needed)
- Outline: #0A0A0A (2px)

SCALE REFERENCE: Include a faint isometric tile grid ghost. Show that the door fits exactly in a 1-tile-wide wall opening.

OUTPUT: One reference sheet with two rows × three columns = 6 panels total. Labels for each state. Dark background.
```

---

## Checklist — What This Prompt Establishes

- [x] Camera angle (isometric 30-degree, SE facing)
- [x] Art style (stylized, brushed steel, baked lighting, 2px outline)
- [x] Both orientation variants (south-facing and east-facing)
- [x] Three door states per orientation (closed-locked, mid-open, fully open)
- [x] Indicator light detail (red = locked, green = unlocked, subtle glow)
- [x] FORGE emblem (subtle, angular, faction branding)
- [x] Door frame context (shown in wall opening)
- [x] Color palette (all elements with hex codes)
- [x] Scale reference (tile grid ghost)
- [x] Dark background
