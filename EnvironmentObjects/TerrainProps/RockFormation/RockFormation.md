# OBJECT PROFILE — ROCK FORMATION

---

## Object Name
**RockFormation**

---

## Category
Terrain Props

---

## Gameplay Purpose
Natural terrain obstacle. Provides irregular cover and movement blocking in outdoor, ruined, or field-battle environments. Breaks up the visual regularity of concrete geometry. Creates organic choke points and natural-looking level dressing. Not interactive, not destructible — a permanent hard blocker.

---

## Where It Is Used
- Outdoor levels: open fields, craters, rocky ridgelines
- Ruined sectors: collapsed walls leave rubble piles that use this asset
- Perimeter areas: natural borders that feel less constructed than walls
- Used in clusters of 2–4 rocks of varying sizes for natural groupings

---

## Interaction Type
**Static** — No interaction. Impassable terrain obstacle.

---

## Visual Description

| Property | Detail |
|---|---|
| Shape | Irregular angular boulder cluster. 1–2 isometric tiles wide. Jagged top silhouette. Flat base (sits flush on ground tile). |
| Material | Stone — basalt/granite look. Faceted, angular breaks. Not smooth or round. |
| Color | Dark desaturated brown-grey (#4A4440). Lighter face on top (#5E5850). Dark undercut shadow (#2A2420). |
| Size | Small variant: 0.75 tile footprint. Medium variant: 1×1 tile. Large variant: 1×2 tile (elongated). |
| Silhouette | Angular, asymmetric. Clearly stone, not concrete. Top edge is jagged, not flat. |
| Details | Faint layered cracks on the rock faces suggesting natural geological breaks. Small loose rock chips at the base. Subtle lichen patch (muted green #3A4030) on one upper face — minimal. |

---

## Damage Behavior
**Not destructible.** Rock formations are permanent map geometry. They cannot be damaged, destroyed, or moved by any gameplay action including tank shells.

---

## Collision Type
**Full block** — Impassable to infantry and vehicles. No passable edges or gaps within a single rock object.

---

## Animation Needs
**None.** Static sprite only. Three size variants (small, medium, large) — all static sprites.

---

## Technical Constraints
- Provide three size variants: small (0.75 tile), medium (1×1 tile), large (1×2 tile)
- Each variant must have its own sprite with correct pivot at base-center
- The base of the rock must sit flush on the ground tile — no floating
- Rock silhouette must be distinct from concrete walls and wooden crates at a glance
- Large variant (1×2) must have a collider matching its actual irregular base — not a simple box
- Must be readable in both bright (outdoor) and dark (indoor/night) lighting conditions — bake in enough contrast
