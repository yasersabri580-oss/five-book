# REFERENCE IMAGE PROMPT — SUPPLY BOX

---

## Purpose
This prompt generates the **canonical reference image** for the SupplyBox.
Both faction variants (FORGE and Rift) and both states (closed and open) are established here.

---

## Reference Image Generation Prompt

```
2.5D isometric game asset — Supply Box (two faction variants, two states each) for the game IRON BREACH.

CAMERA: Isometric 2.5D, 30-degree pitch, south-east facing. Objects shown as standalone sprites on flat near-black background (#121212). No environment.

ART STYLE: Stylized game asset. Crisp 2px black outline. Baked isometric lighting: top face (lid) is lightest, south face is mid-tone, east face is darkest. Stamped steel construction — smooth flat faces with slight bevel at edges. NOT pixel art. NOT photorealistic. This must clearly read as a MILITARY SUPPLY CONTAINER, not a random box.

REFERENCE SHEET: Two rows × two columns = 4 panels.

ROW 1 — FORGE VARIANT (military operational supply box):

LEFT PANEL (Row 1) — CLOSED / AVAILABLE:
- Box shape: 0.9 isometric tile wide × 0.7 tile deep × 0.6 tile tall. Wider and lower than the WoodenCrate. A flat rectangular box with a clearly defined lid line running horizontally at 0.4 tile height from the base (the lid occupies the upper 0.2 tile of the box height).
- BODY: Dark military green (#2A3820). Top face (lid): slightly lighter (#38481C). East/shadow face: darker (#1E2A14).
- RUBBER CORNER GUARDS: At each of the 8 corners, a slightly bulging rounded dark rubber bumper (#1A1A18, slightly lighter #242420 on the top-light corner). These are 3D-feeling — they protrude slightly from the main box body. They are the primary texture break on what would otherwise be a flat box.
- LID LINE: A clear horizontal seam where the lid meets the body. The seam is a dark gap line (#0A0A08). Two SPRING CLASPS on the south face (front): simple flat metal latch shapes (#3A3A38 dark metal), one at 1/3 from the left, one at 2/3 from the left. Each clasp: a small vertical bar with a T-shaped latch end. Clasps are closed (latched) in this state.
- LID HANDLE: On the lid top face, a flat bar handle in the center (#2A2A28 dark metal). A slight arch shape — the handle rises approximately 2–3 px above the lid face.
- STENCILS ON SOUTH FACE:
  - "AMMO" TRIANGLE: A yellow (#C8A020) stencil triangle (upward-pointing, simple) in the center of the south face body (below the lid seam line). Inside or below the triangle: a stylized bullet silhouette stencil — a simple bullet shape, flat yellow, same color. The whole mark is small (25% of the south face width), worn and faded slightly (not crisp — stencil look with rough edges).
  - FORGE DECAL: Upper area of the south face body, to the left of the AMMO triangle: a dark red (#6A1010) FORGE triangle mark — same as the SecurityDoor emblem. Small, stenciled, worn.
- EAST FACE (side face): Dark (#1E2A14). One CARRY HANDLE visible on the short end face (east face in isometric): a flat bar handle (#2A2A28), similar to the lid handle, mounted at the center of the east face, oriented vertically (for carrying by hand at the side). It is folded flat against the face.

RIGHT PANEL (Row 1) — OPEN / DEPLETED (lid flipped open):
- Same body, lid is now open. The lid is flipped UP and BACK from the front — in isometric view, the lid is now visible as a flap angled back (leaning toward the north at approximately 110° from its closed position, so it is angled slightly past vertical and visible from the camera as a flat surface tilting away). The lid clasps are sprung open (hanging free on the hinge side).
- INTERIOR: The box interior is visible. A dark recess (#0A0E08 very dark interior). Two or three spent brass shell casings on the interior floor (small cylindrical shapes, #C8A020 brass color, lying on their sides). The interior rim (the box body edge at the top) shows a thin dark metal border.
- SPRING CLASPS: Now unlatched — the clasp bars hang loosely downward on the south face.
- The "AMMO" stencil and FORGE mark on the south face are unchanged.

ROW 2 — RIFT VARIANT (scavenged/resistance supply box):

LEFT PANEL (Row 2) — CLOSED / AVAILABLE:
- Same box geometry. Different color and markings:
  - BODY: Dark matte grey (#282828). Top face: slightly lighter (#363636). East face: darker (#181818).
  - Rubber corner guards: same dark #1A1A18 but now slightly more worn — more scuffed.
  - RIFT LIGHTNING BOLT STENCIL: On the south face body center: a white (#E8E8E8, slightly off-white) jagged lightning bolt stencil — the same Rift faction design language as Rina's arm patch. Simple, angular, clearly hand-stenciled (rough spray-stencil edges, not crisp). This replaces the FORGE triangle.
  - "AMMO" triangle: same yellow (#C8A020) but on the Rift variant it reads "AMMO" in smaller text below the lightning bolt — or just the triangle and bullet silhouette, no faction text.
  - No FORGE decal — the FORGE branding is absent on Rift boxes.
  - The overall Rift box looks less official — more worn, more scratched, slightly more battered. Extra scuff marks on the south face.

RIGHT PANEL (Row 2) — OPEN / DEPLETED:
- Same as Row 1 right panel (open lid, interior visible) but on the grey Rift body.
- Interior: same dark recess and spent shell casings. Perhaps one shell casing is a different caliber (slightly different cylinder diameter) — flavor detail for the Rift's improvised supply situation.

COLOR PALETTE:
- FORGE body: #2A3820 (military green)
- FORGE top face: #38481C (lighter green)
- FORGE east face: #1E2A14 (dark green)
- Rift body: #282828 (matte grey)
- Rift top face: #363636
- Rift east face: #181818
- Rubber guards: #1A1A18 (with #242420 highlight)
- Clasps (closed): #3A3A38
- Lid handle: #2A2A28
- AMMO stencil: #C8A020 (worn yellow)
- FORGE faction mark: #6A1010 (dark red)
- Rift lightning bolt: #E8E8E8 (off-white)
- Interior dark: #0A0E08
- Spent casings: #C8A020 (brass)
- Outline: #0A0A0A (2px)

SCALE REFERENCE: Include a faint isometric tile grid ghost. Show that the box is 0.9 tile wide × 0.7 tile deep × 0.6 tile tall. Place the WoodenCrate (0.8×0.8×0.8 tile) silhouette ghost next to one panel for size comparison — the supply box should be wider and lower.

OUTPUT: One reference sheet, 2×2 grid of four panels. Row 1: FORGE closed + FORGE open. Row 2: Rift closed + Rift open. All labeled. Dark background.
```

---

## Checklist — What This Prompt Establishes

- [x] Camera angle (isometric 30-degree, SE facing)
- [x] Art style (stylized, military stamped steel, baked lighting, 2px outline)
- [x] Two faction variants (FORGE green + Rift grey)
- [x] Two states per variant (closed/available, open/depleted)
- [x] Critical: AMMO stencil + rubber corner guards + clasps communicate "military supply container"
- [x] Open state detail (lid angle, interior recess, spent casings, unlatched clasps)
- [x] Color palette (all elements with hex codes for both variants)
- [x] Scale comparison with WoodenCrate
- [x] Dark background
