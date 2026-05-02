# REFERENCE IMAGE PROMPT — CHAIN-LINK FENCE

---

## Purpose
This prompt generates the **canonical reference image** for the ChainLinkFence.
All fence variants and the crushed state must be consistent with this reference.

---

## Reference Image Generation Prompt

```
2.5D isometric game asset — Chain-Link Fence (full tile set) for the game IRON BREACH.

CAMERA: Isometric 2.5D, 30-degree pitch, south-east facing. Objects shown as standalone sprites on flat near-black background (#121212) or transparent. No environment.

ART STYLE: Stylized game asset. Crisp 2px black outline on structural elements (posts, footings). The mesh itself uses a 1px interior line for the diamond grid pattern. Baked isometric lighting — posts are lit from top-left (lighter on top face, darker on east face). NOT pixel art. NOT photorealistic. Clean and readable. Consistent with the IRON BREACH environment art palette.

REFERENCE SHEET: Four panels side by side.

PANEL 1 — FENCE SEGMENT (no posts):
- A 1-tile-wide chain-link mesh panel, 1.2 tiles tall. Framed by thin steel channel at top and bottom (horizontal rails) but no vertical posts — these are separate sprites.
- The mesh: simplified diamond/diagonal grid pattern. Each diamond cell is approximately 6–8 px at game resolution. Use a dark greenish-grey mesh color (#4A5040) against a lighter steel frame (#5A6050). The mesh is semi-transparent in feel — leave some space showing through, suggesting you can see through it.
- The mesh has a very slight sag/curve toward the center — the top rail is straight but the mesh hangs slightly.
- 2 barbed wire strands along the top rail — drawn as a dark line (#2A2A28) with evenly spaced small 4-point spike shapes (simple shorthand, not photorealistic barbs).
- A slight rust-stain streak down from the top-right corner of the rail: #5A3020 very subtle.

PANEL 2 — END POST:
- A single hollow steel square post, 1.4 tiles tall (extends slightly above the fence segment). Set in a small square concrete footing at the base. The post is matte grey-green steel (#3A3A38). The footing is concrete (#484644). A small bolt/cap at the very top of the post. Slight rust blush near the base at the footing junction.

PANEL 3 — MID POST (shared between two fence segments):
- Same as the end post but designed to appear between two fence segments — it has wire attachment points (small loops or hooks) on both the left and right faces.

PANEL 4 — CRUSHED / DESTROYED STATE:
- The fence flattened and bent by a vehicle impact. The panel is now lying at a low angle on the ground. The posts are knocked sideways or bent forward. The mesh is visibly distorted — buckled, irregular. This is a flat, on-ground sprite suggesting debris. The top barbed wire is still visible, tangled. Color matches intact variant — same materials, just deformed.

COLOR PALETTE:
- Mesh: #4A5040 dark greenish-grey
- Steel frame rails: #5A6050 lighter grey-green
- Posts: #3A3A38 matte dark steel
- Footing: #484644 concrete
- Barbed wire: #2A2A28 near-black dark line with small spikes
- Rust accents: #5A3020 very faint stain only
- Outline: #0A0A0A (2px for structural, 1px for mesh interior lines)

SCALE REFERENCE: Include a faint isometric tile grid ghost under each panel.

OUTPUT: One horizontal reference sheet, four panels left to right: Segment, End Post, Mid Post, Crushed State. All labeled. Dark background.
```

---

## Checklist — What This Prompt Establishes

- [x] Camera angle (isometric 30-degree, SE facing)
- [x] Art style (stylized, baked lighting, 2px structural outline, 1px mesh lines)
- [x] Four sprites required (segment, end post, mid post, crushed)
- [x] Mesh visual (simplified diamond grid, semi-transparent feel, slight sag)
- [x] Barbed wire (simple shorthand, dark spikes)
- [x] Color palette (mesh, rails, posts, footing, rust accents)
- [x] Crushed state (deformed, ground-lying)
- [x] Scale reference (tile grid ghost)
- [x] Dark background
