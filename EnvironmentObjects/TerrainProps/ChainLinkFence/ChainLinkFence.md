# OBJECT PROFILE — CHAIN-LINK FENCE

---

## Object Name
**ChainLinkFence**

---

## Category
Terrain Props

---

## Gameplay Purpose
Low visibility blocker and soft movement barrier. The fence blocks infantry movement but does NOT block projectiles or line-of-sight. Creates areas that feel fenced-off without being hard walls. Players can see threats through the fence and shoot through it — it creates vulnerability near fence lines. Tanks can drive through and destroy a fence segment (purely visual — fence collider deactivates, fence is replaced with bent/broken variant).

---

## Where It Is Used
- Military bases: perimeter fencing, compound divisions
- Industrial zones: facility borders, restricted-area markers
- Can be used at the very edge of playable areas to suggest boundary without a hard concrete wall

---

## Interaction Type
**Static** (default) / **Destructible by vehicle only** — Infantry cannot break it. Tanks crush it.

---

## Visual Description

| Property | Detail |
|---|---|
| Shape | Vertical chain-link panel, 1 tile wide × 1.2 tiles tall. Supported by two steel posts (one at each end). Slight forward lean angle to suggest real-world sag. |
| Material | Galvanized steel wire mesh + steel hollow-square posts with concrete base footings |
| Color | Wire mesh: desaturated green-grey (#5A6050). Posts: dark steel grey (#3A3A38). Base footing: concrete (#484644). |
| Size | 1 tile wide × 1.2 tiles tall. Tileable horizontally with post variants (end post, mid post shared between segments). |
| Silhouette | Rectangular panel. The mesh pattern must be visible but not dominant — use a simplified mesh representation, not a full photorealistic weave. |
| Details | Slight sag in the mesh center. 1–2 barbed wire strands along the top (simple dark line with small thorn bumps). Top-corner post has a faint rust stain running down. |

---

## Damage Behavior
**Two states only:**

| State | Visual | Trigger |
|---|---|---|
| Intact | Normal upright fence | Default |
| Crushed / Destroyed | Flattened bent mesh on the ground, post knocked sideways | Tank drives through |

When a tank exits the fence tile, the intact sprite is replaced with the crushed sprite (a flat distorted mesh on the ground). The crushed state has no collider — it is purely decorative ground dressing.

---

## Collision Type
**Partial block** — Blocks infantry movement. Does NOT block projectiles or line-of-sight. No collision against bullets, grenades, or tank shells.

---

## Animation Needs
**None for intact state.** The transition from intact to crushed is a sprite swap, not an animation. If budget allows: a simple 3-frame collapse animation (fence tilts → bends → flat) is a nice-to-have, not required.

---

## Technical Constraints
- Mesh visual must be readable at small size — do NOT attempt a realistic wire weave; use a simplified diamond grid pattern at 45° that reads as chain-link
- Tileable: left and right edges must connect (mid-post is shared between two adjacent segments, placed as a separate sprite)
- Provide: `fence_segment.png` (no posts), `fence_post_end.png` (post for end of run), `fence_post_mid.png` (post shared between segments), `fence_crushed.png` (destroyed flat state)
- Barbed wire at top: simple shorthand — a dark line with evenly spaced small spike shapes, not photorealistic barbs
