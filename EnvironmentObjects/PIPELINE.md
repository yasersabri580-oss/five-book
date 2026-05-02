# IRON BREACH — ENVIRONMENT OBJECT & PROP ASSET PIPELINE

### Production-Ready Object Design Document

---

## SCOPE

This pipeline covers all **environment objects and interactive props** for IRON BREACH Chapter 1.

**INCLUDED:**
- Terrain props (walls, rocks, barriers, ruins)
- Destructible objects (crates, barrels, weak walls)
- Interactive objects (doors, terminals, repair stations)
- Combat environment objects (turrets, traps, mines, generators)
- Cover objects (sandbags, concrete blocks)
- Utility props (fuel tanks, power nodes, supply boxes)

**NOT INCLUDED:**
- Characters or character weapons
- Bullets, VFX, or particle effects
- Cinematic full backgrounds or skyboxes

---

## STYLE REFERENCE

- **Visual style:** 2.5D isometric, dieselpunk / near-future militarism
- **Color palette:** Desaturated greens, greys, oranges. Sharp red/yellow danger highlights
- **Camera:** Fixed isometric, 30-degree pitch, south-east facing
- **Art style:** Stylized but readable. Crisp 2px black outline. NOT pixel art. NOT full 3D
- **Readability rule:** Every object's function must be visually clear at game resolution

---

## DESIGN RULES

1. **All objects are gameplay-driven.** No decoration for decoration's sake.
2. **Destructible objects are clearly identifiable.** Damage visual = immediate readability.
3. **Hazards are readable before they activate.** Players must see danger before it kills them.
4. **Shapes are simple and distinctive.** Silhouette reads at small screen size.
5. **Objects communicate function visually.** A repair station looks repairable. A mine looks dangerous.
6. **Avoid over-detailing.** High-frequency noise on a sprite kills gameplay readability.
7. **Grid alignment is mandatory.** All objects must align to the isometric tile grid.
8. **Consistent lighting direction.** All objects lit from the same top-left direction.
9. **Color hierarchy:** Neutral base → accent color codes function (red = danger, yellow = interactive, green = utility/heal).

---

## LIMITATION RULES

- Do NOT include character art in any object sprite
- Do NOT include bullets, projectiles, or particle sources in object sprites
- Do NOT include full environmental backgrounds or skyboxes
- Keep all props self-contained: pivot, shadow, and outline are baked into the sprite

---

## OBJECT CATEGORY LIST

### 1. TERRAIN PROPS
Static non-destructible world geometry and environmental dressing.

| Object | File |
|---|---|
| ConcreteWallSegment | `TerrainProps/ConcreteWallSegment/` |
| RockFormation | `TerrainProps/RockFormation/` |
| RuinedPillar | `TerrainProps/RuinedPillar/` |
| ChainLinkFence | `TerrainProps/ChainLinkFence/` |

### 2. DESTRUCTIBLE OBJECTS
Objects that can be damaged and destroyed. Must show damage stages visually.

| Object | File |
|---|---|
| WoodenCrate | `DestructibleObjects/WoodenCrate/` |
| ExplosiveBarrel | `DestructibleObjects/ExplosiveBarrel/` |
| WeakWallSection | `DestructibleObjects/WeakWallSection/` |

### 3. INTERACTIVE OBJECTS
Objects the player can interact with (E key / Circle). Require trigger or usable interaction type.

| Object | File |
|---|---|
| SecurityDoor | `InteractiveObjects/SecurityDoor/` |
| ControlTerminal | `InteractiveObjects/ControlTerminal/` |
| RepairStation | `InteractiveObjects/RepairStation/` |

### 4. COMBAT ENVIRONMENT OBJECTS
Objects that actively affect combat — enemy-controlled or environment-controlled.

| Object | File |
|---|---|
| AutoTurret | `CombatEnvironment/AutoTurret/` |
| ProximityMine | `CombatEnvironment/ProximityMine/` |
| Generator | `CombatEnvironment/Generator/` |

### 5. COVER OBJECTS
Objects specifically designed to provide player cover in combat.

| Object | File |
|---|---|
| SandbagBarrier | `CoverObjects/SandbagBarrier/` |
| ConcreteBlock | `CoverObjects/ConcreteBlock/` |

### 6. UTILITY PROPS
World props that provide resources or environmental narrative.

| Object | File |
|---|---|
| FuelTank | `UtilityProps/FuelTank/` |
| PowerNode | `UtilityProps/PowerNode/` |
| SupplyBox | `UtilityProps/SupplyBox/` |

---

## FOLDER STRUCTURE TEMPLATE

```
/EnvironmentObjects/CategoryName/ObjectName/
  ObjectName.md           ← Main object design file
  reference_prompt.md     ← Image generation prompt for reference art
  animation_prompts/      ← Animation prompts (or no_animation_note.md if static)
  notes.md                ← Unity integration notes and pipeline details
```

---

## UNITY INTEGRATION OVERVIEW

| Component | Usage |
|---|---|
| Static terrain/cover | SpriteRenderer on static GameObject, Tilemap if tiling |
| Destructible objects | Prefab with multiple sprite variants swapped by damage state |
| Interactive objects | Prefab with Animator (state machine) + InteractableComponent script |
| Combat objects | Prefab with Animator + AI/TriggerComponent script |
| All objects | Sorting layer: `Environment` (sub-sorted by Y position) |
| Grid alignment | All pivots at isometric base-center, snapped to grid |
| Shadow | Baked into sprite — no real-time shadow needed |

---

## ANIMATION STATE GUIDE

Only objects that logically require animation get animation prompts.

| Animation Type | Objects |
|---|---|
| Idle loop | AutoTurret (scan), Generator (hum), ControlTerminal (screen flicker) |
| Active state | AutoTurret (aim + fire), SecurityDoor (opening) |
| Triggered | RepairStation in use |
| Damage stages | WoodenCrate, ExplosiveBarrel, WeakWallSection |
| Destroyed | All destructible objects |
| No animation | RockFormation, ConcreteWallSegment, SandbagBarrier, ConcreteBlock, ChainLinkFence, RuinedPillar, ProximityMine (static — only LED blink), FuelTank, SupplyBox, PowerNode (idle pulse only) |
