# GROUND OBJECT — SHADOW AND SURFACE DECALS

---

## Asset Name
**ShadowAndSurfaceDecals**

## Category
Surface Decals

## Gameplay Purpose
Transparent sprite overlays placed on top of floor tiles to add:
1. **Shadow decals:** Cast shadows from props and characters (baked static shadows beneath static props)
2. **Surface detail decals:** Small ground-level details that add environmental storytelling without cluttering gameplay readability

Decals are NOT floor tiles — they are sprite-based objects placed on a separate sorting layer above the ground but below characters and props. They are transparent PNG sprites.

---

## SHADOW DECALS

### Visual Description
Soft isometric drop shadows placed beneath static props (walls, crates, generators, etc.). These are pre-baked static shadow sprites that match each prop's footprint. The shadow communicates the prop's presence on the ground plane and reinforces depth.

Shadow rules:
- Shadow direction: Always top-left source — shadow falls toward bottom-right in isometric view
- Shadow color: Near-black with transparency — `#000000` at 35–45% opacity
- Shadow shape: Soft-edge ellipse or prop-matched silhouette, blurred/diffused at edges
- Shadow size: Scaled to match the prop it accompanies (each prop has its own shadow decal)

### Reference Image Prompt — Generic Prop Shadow Decal

```
Isometric 2.5D ground shadow decal — soft cast shadow from an upright prop, dieselpunk game sprite.

Shape: An irregular ellipse / slightly elongated soft shadow shape. The shadow is widest at the base of where the prop sits and tapers slightly toward the right-bottom direction (isometric light source is top-left — shadow falls bottom-right).

Color: Flat near-black (#000000) at the core, fading to completely transparent at the outer edges. Gradient: solid at center, 35–40% opacity mid-zone, 0% at edge. Very soft diffused edges — not hard-cut.

Size: Approximately 80×50 px at the standard 192×192 sprite scale (scales proportionally with each prop).

Background: Completely transparent PNG. The decal is designed to be layered above floor tiles.

No outlines. No fills other than the gradient shadow shape. The shadow is the only content.

Style: Clean, simple, production-ready shadow sprite. No artistic detail — pure functional shadow.
```

### Required Shadow Decal Set

Each major prop category needs a shadow decal variant:

| Prop Category | Shadow Shape | Notes |
|---|---|---|
| 1×1 tile props (crates, barrels) | Small ellipse | Approximately 80×50 px |
| 2×1 tile props (sandbags, barriers) | Wide ellipse | Approximately 150×50 px |
| 1×1 tall props (terminals, fuel tanks) | Tall ellipse — slightly elongated | Taller shadow length |
| 1×2 tile props (wall segments) | Elongated directional | Follows wall axis direction |
| Character shadow | Small oval | Placed at character feet, animates with character Y position |

---

## SURFACE DETAIL DECALS

### Visual Description
Small environmental storytelling details placed on the ground surface. These decals add world-building without cluttering gameplay. They are read as "background detail" and must never compete with interactive props, enemies, or HUD elements.

Design rules for all surface decals:
- Size: Maximum 1 tile footprint (64×32 px equivalent)
- Must be immediately readable as non-interactive (no yellow/orange/green — those are gameplay signal colors)
- Maximum contrast: Very low. These are whisper-details, not feature elements.
- Transparent background PNG

### Surface Detail Decal Set

---

#### DECAL — OIL STAIN

```
Isometric 2.5D surface decal — oil stain on concrete/metal floor, dieselpunk war-zone style.

Shape: Irregular organic splatter shape — a central dark pool with 3–5 irregular splatter arms radiating outward. The shape reads immediately as a spilled liquid stain.

Color: Very dark near-black-brown (#1A1408), with the very center slightly darker and the edges fading to transparent. Low overall opacity — this is a stain, not a solid shape. Core opacity: approximately 50%. Edge opacity: 0%.

Size: Approximately 60×40 px at 128×64 tile scale.

Background: Fully transparent PNG. Overlay sprite only.

Style: Clean, simple, readable. No texture detail within the stain — pure color shape with transparency fade.

Do NOT make this look like blood. It must read as mechanical oil or fuel.
```

---

#### DECAL — TREAD MARK (Single)

```
Isometric 2.5D surface decal — single vehicle tread mark impression on a soft surface (dirt or mud), dieselpunk game style.

Shape: A single compressed tread impression — a rectangular stripe approximately 8–10px wide at 128×64 scale, with very subtle tread pattern texture (faint diamond or block pattern suggesting a tire tread, barely readable at small scale). The tread mark runs diagonally in the isometric east-west direction.

Color: Slightly darker than the surface it's placed on. As a neutral decal: desaturated dark brown (#3A2A18) at approximately 50% opacity, fully transparent at edges.

Background: Fully transparent PNG.

Note: This decal is placed manually by level designers on dirt or mud tiles to suggest vehicle activity without requiring a tile variant.
```

---

#### DECAL — SPENT SHELL CASINGS

```
Isometric 2.5D surface decal — scattered spent bullet casings on a floor or ground surface, dieselpunk game style.

Content: 4–6 small cylindrical shell casings scattered loosely in a loose cluster. Each casing: approximately 3–5px tall at 128×64 scale. Brass-colored (#A07830), slightly reflective on the upper face (tiny bright highlight on each casing top). Casings are oriented in slightly different directions — not perfectly aligned.

Background: Fully transparent PNG.

Size: Cluster fits within approximately 50×35 px at 128×64 scale.

Lighting: Very subtle isometric top-left catch-light on each casing top. Shadow below each casing: 1px dark dot.

Style: Clean, tiny, readable as shell casings at game zoom. NOT pixel art but abstracted enough to read at small size.

Do NOT include weapons, characters, or blood in this decal.
```

---

#### DECAL — DUST / DIRT GROUND SCATTER

```
Isometric 2.5D surface decal — scattered dust and small dirt particles on a concrete or metal surface, dieselpunk style.

Content: A loose irregular scatter of fine dust and tiny pebble particles — not a solid shape, a loose cloud pattern. 8–12 tiny dark-grey dots/particles of varying sizes, loosely scattered within a 60×40 px area. The overall shape is diffuse, not concentrated.

Color: Dark grey (#484848) at 30–40% opacity per particle. Very subtle. This decal should barely be visible — it adds texture, not presence.

Background: Fully transparent PNG.

Do NOT create a solid cloud shape. The decal should be a scattered collection of individual tiny marks.
```

---

#### DECAL — BLOOD POOL (Optional / M-rated toggle)

```
[ENGINE TOGGLE: This decal is hidden when Violence display setting is set to "Minimal"]

Isometric 2.5D surface decal — dark blood pool on a ground surface, dieselpunk war-zone style.

Shape: An irregular organic spreading pool shape — wider than tall, with irregular edges suggesting fluid spread. A slightly darker core at the center, fading to transparent at the edge.

Color: Very dark desaturated red-brown (#4A1818) — deliberately dark and desaturated. NOT bright red. The color reads as blood only when the context (a dead enemy nearby) provides the read cue. Maximum 50% opacity at core, 0% at edges.

Background: Fully transparent PNG.

Size: Approximately 70×45 px at 128×64 scale.

Note: This decal is instantiated at enemy death positions as an engine-driven runtime decal, not placed by level designers.
```

---

## Tiling Note
**Non-tiling — all decals are individual sprites.** Placed as SpriteRenderer GameObjects, not Tilemap tiles.

## Animation Requirement
**None.** All decals are static. (Character shadow decal position updates via code to follow character Y position — no animation frames required, position is driven by code.)

## Unity Usage Note
- Component: SpriteRenderer on GameObject
- Sorting layer: `Decals` (above `Ground`, below `Props`)
- Sorting order: 0 within `Decals` layer (below prop base shadows, above tile)
- Transparency: All decals require alpha channel in PNG — use `Sprite Import: Alpha Is Transparency`
- Shadow decals: Attached as child GameObjects to each prop — `[PropName]_Shadow` child object
- Surface detail decals: Placed manually by level designers in scene (or instantiated at runtime for battle damage)
- Character shadow: Attached to character prefab as child object at Y offset 0, Z-sorted below character sprite

## Folder Name Suggestion
`/GroundObjects/SurfaceDecals/`
