# GROUND OBJECT — DIRT TRACK

---

## Asset Name
**DirtTrack**

## Category
Road Surfaces

## Gameplay Purpose
Unpaved vehicle path for rural and off-road mission areas. Dirt tracks are natural vehicle routes compressed by repeated use — not constructed roads. Used in Missions 2, 3, and 5 (rural and field approaches). Tank movement has a slight penalty on dirt tracks (less than DirtGround, more than AsphaltRoad).

## Visual Description
A well-worn dirt path created by vehicle and foot traffic. Two parallel tire-groove channels run along the track direction, with a central ridge and outside shoulder areas of harder compressed earth. Color is slightly darker than surrounding DirtGround because of compression and moisture retention in the grooves. The track reads immediately as "a path vehicles travel on" without the infrastructure of a built road.

Tile variants:
- **Straight (E-W and N-S):** The track runs across the tile. Two tire grooves visible, central ridge, compressed shoulders.
- **Corner variants (4):** Same 4 corners as AsphaltRoad
- **Damaged/rutted:** Extra-deep ruts, more mud-like, used near wetlands transitions

## Material / Style
- Track base: Compressed tan-brown (#786040), darker than DirtGround
- Tire groove interior: Dark compressed earth (#4A3820), slightly wet-looking at base
- Central ridge: Slightly lighter than base (#8A7050) — the less-traveled center
- Shoulder: DirtGround color (#8A7050) blending outward to surrounding ground
- No road markings — this is a natural track, not a constructed road
- Lighting: Top-left directional bake. Groove interior darker on right face. Ridge top catches slightly more light.

## Reference Image Prompt

```
Isometric 2.5D floor tile — unpaved dirt track / vehicle path, rural war-zone dieselpunk game style.

Tile shape: Isometric diamond (parallelogram), 128×64 px. Flat top-down isometric view, 30-degree pitch.

Primary variant: Track running east-west (track runs left-right across the full isometric tile width).

Track surface: Compressed dirt and earth. Base color: compressed tan-brown (#786040), darker than surrounding field dirt. The track has a classic unpaved-path structure: two parallel tire groove channels running along the track direction (~15px wide each at 128px resolution), a central ridge between the grooves, and compressed shoulder areas on each outer edge that blend into surrounding ground color. 

Tire grooves: Slightly darker, compressed-earth (#4A3820). Grooves have slightly rougher texture — more soil grain visible from the repeated compression and moisture. Central ridge: slightly lighter than groove base (#8A7050). Shoulders: transition outward into surrounding DirtGround tone.

No road markings, no painted lines. This is a natural track, not a built road.

Lighting: Top-left directional bake. Groove bases slightly darker on their right face. Ridge top catches slightly more light.

Edges: NO black outline on tile. Track edges blend softly to adjacent ground color.

Seamless: Track tiles must connect seamlessly to adjacent track tiles. Groove lines must align across tile edges.

Style: Semi-realistic painterly, readable at 64×32 px. IRON BREACH art direction. NOT pixel art. NOT photorealistic.

Do NOT include: built road features, painted lines, curbs, or any infrastructure element. This must read as natural.
```

## Tiling Note
**Directional — not random.** Same Rule Tile system as AsphaltRoad. Corner and intersection variants required. Fewer intersection variants needed (dirt tracks rarely have 4-way intersections — T-junctions are more common).

## Animation Requirement
**None.** Static tile.

## Unity Usage Note
- Component: Unity Tilemap, `Ground` tilemap layer
- Rule Tile: Directional Rule Tile for track direction matching
- Tag: `TerrainType.DirtTrack` — used by tank movement system (moderate movement penalty)
- Sorting layer: `Ground`
- Use in: Rural mission areas, field approaches, off-road vehicle routes, outskirts paths

## Folder Name Suggestion
`/GroundObjects/RoadSurfaces/DirtTrack/`
