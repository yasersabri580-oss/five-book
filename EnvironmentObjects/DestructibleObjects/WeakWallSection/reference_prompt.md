# REFERENCE IMAGE PROMPT — WEAK WALL SECTION

---

## Purpose
This prompt generates the **canonical reference image** for the WeakWallSection.
The brick material and visible structural damage are the critical visual differentiators from the ConcreteWallSegment.

---

## Reference Image Generation Prompt

```
2.5D isometric game asset — Weak Wall Section (three damage states) for the game IRON BREACH.

CAMERA: Isometric 2.5D, 30-degree pitch, south-east facing. Objects shown as standalone sprites on flat near-black background (#121212). No environment.

ART STYLE: Stylized game asset. Crisp 2px black outline. Baked isometric lighting: top face is lightest, south face is mid-tone, east face is darkest. Same general style as ConcreteWallSegment but with aged brick material instead of smooth concrete. NOT pixel art. NOT photorealistic. Readable at tile size.

IMPORTANT: This wall must look DIFFERENT from the ConcreteWallSegment (smooth grey slab) at a glance. The brick coursing pattern and dramatic cracking are the key visual differentiators.

REFERENCE SHEET: Four panels side by side.

PANEL 1 — INTACT (but structurally weak) STATE:
- Same 1×1 tile footprint, 1.5 tiles tall as ConcreteWallSegment.
- SOUTH FACE: Visible brick coursing — rows of rectangular bricks, each brick approximately 0.15 tile tall × 0.3 tile wide in visual proportion, separated by mortar lines. Bricks are dusty red-brown (#7A5A44). Mortar lines are lighter grey-tan (#8A7A68), creating a visible grid pattern.
- CRACKING: A large diagonal crack running from upper-right to lower-left across the south face. Secondary smaller cracks branching from it. Near the top-right corner: 2–3 bricks are missing — dark gap holes showing the dark interior beyond (#1A1210). Near the lower-left corner: another 1–2 missing bricks.
- TOP FACE: Same brick pattern, slightly lighter (#8A6A54). One brick near the left edge is cracked in half — shows a raw break.
- EAST FACE: Darker than south face (#4A3428). Fewer details visible on this face — it is mostly in shadow. Faint vertical mortar lines only.
- SLIGHT LEAN: The top of the wall leans approximately 3° toward the south (toward the camera). This is visible as a slight top-edge overhang on the south face. Subtle but readable.
- BASE: Dark moisture staining at the very base of the south face (#2A1A10 dark streak, 20% of the wall height from the bottom).

PANEL 2 — HEAVILY DAMAGED STATE (75% HP → 1 HP):
- Same shape. Keep the wall still standing — it is damaged, not fallen.
- SOUTH FACE: Cracks now extend to the center and split the face in multiple directions. The central area of the wall has a large void/gap where multiple bricks have fallen out — a ragged hole approximately 0.2 tile wide × 0.3 tile tall in the center of the south face. Dark interior visible through the hole.
- TOP portion of wall: the top 0.3 tile section looks as if it is barely connected — cracks radiate from the top corners and top edge. Small brick fragments are detaching from the top (show 2–3 loose brick fragments at the very top edge, as if they are mid-fall).
- The slight lean is now 6–7° — more pronounced, the wall is clearly about to collapse.
- Color remains same as Panel 1 but with more exposed dark interior visible through gaps.

PANEL 3 — DESTROYED RUBBLE PILE (ground decal):
- The wall has collapsed. A rubble pile on the ground.
- The pile is low and spread: approximately 1.0 tile wide × 0.6 tile deep, about 0.3 tiles tall at the highest point. The silhouette is irregular — the pile is not symmetric.
- Loose bricks in the pile: recognizable as the same brick (#7A5A44) — some intact, some cracked in half, some just fragments. Mortar dust: lighter dusty tone (#B8A890) on the surrounding ground around the pile. A few brick fragments scattered outside the main pile radius.
- The rubble pile has no vertical collision (infantry can walk over it) but blocks vehicles (low collider box).

PANEL 4 — SCALE COMPARISON:
- Panel showing the Intact WeakWallSection (Panel 1) placed immediately to the right of a ConcreteWallSegment from that asset. They share the same footprint. The difference in material and visual condition must be immediately clear.

COLOR PALETTE:
- Brick: #7A5A44 (dusty red-brown)
- Mortar lines: #8A7A68 (grey-tan)
- Top face bricks: #8A6A54 (slightly lighter)
- East/shadow face: #4A3428 (dark)
- Brick interior (missing brick gaps): #1A1210 (near-black)
- Moisture stain at base: #2A1A10
- Rubble dust/mortar: #B8A890 (light dusty tan on ground)
- Outline: #0A0A0A (2px)

SCALE REFERENCE: Include a faint isometric tile grid ghost under each panel.

OUTPUT: One horizontal reference sheet, four panels: Intact, Heavily Damaged, Rubble Pile, Scale Comparison. All labeled. Dark background.
```

---

## Checklist — What This Prompt Establishes

- [x] Camera angle (isometric 30-degree, SE facing)
- [x] Art style (stylized, baked lighting, 2px outline, brick material)
- [x] Three damage states + scale comparison panel
- [x] Critical: brick coursing visible, clearly different from ConcreteWallSegment
- [x] Crack detail per state (diagonal cracks, missing bricks, central hole)
- [x] Rubble pile (passable, spread, mortar dust)
- [x] Slight lean visual (3° intact, 6° damaged)
- [x] Color palette (brick, mortar, shadow, gaps, dust)
- [x] Scale comparison with ConcreteWallSegment
- [x] Dark background
