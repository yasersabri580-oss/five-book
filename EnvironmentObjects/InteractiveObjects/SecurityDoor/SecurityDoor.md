# OBJECT PROFILE — SECURITY DOOR

---

## Object Name
**SecurityDoor**

---

## Category
Interactive Objects

---

## Gameplay Purpose
Controlled access point. Blocks player movement until unlocked via an adjacent ControlTerminal or by meeting a mission trigger. Provides a clear navigational gate — players understand that some doors are locked, some are unlockable, and locked ones must be dealt with before progressing. Security doors create tension (player knows something is behind the door) and reward exploration (finding a control terminal to open it). The door must visually communicate whether it is locked or unlocked at a glance.

---

## Where It Is Used
- FORGE-controlled facilities: vault doors, restricted zones, server rooms
- Military bases: armory access, commander quarters, vehicle bays
- Appears in any level where gated access is required

---

## Interaction Type
**Trigger** — Player cannot directly interact with the door (no E prompt). Door opens only when the linked ControlTerminal or script event triggers it. Once unlocked, door opens automatically when player approaches within 1.5 tiles.

---

## Visual Description

| Property | Detail |
|---|---|
| Shape | Thick rectangular slab door, fits a 1-tile-wide opening. Door itself: 1 tile wide × 1.8 tiles tall × 0.15 tile thick. Set into a steel door frame that is flush with the wall. |
| Material | Heavy reinforced steel — brushed industrial finish. Angular panels on the face. |
| Color | Dark steel grey (#2A2E32). Panel highlights: slightly lighter (#3A4044). Door frame: near-black (#1A1E22). Locked indicator light: red (#C42020). Unlocked indicator: green (#20C440). |
| Size | 1 tile wide × 1.8 tile tall (fits the ConcreteWallSegment gap). |
| Silhouette | Vertical rectangle, clearly a door. Angular panel design on face. Indicator light on the frame at eye level. |
| Details | 3 horizontal panel seams across the door face (suggesting armored plate sections). Brushed metal texture. A small backlit status indicator on the left door frame post: red when locked, green when unlocked. Hinge details on the right side (not functional — the door slides, the hinges are decorative). An optional FORGE emblem or access-level symbol (stylized triangle) on the door center panel. |

---

## Damage Behavior
**Not destructible by infantry.** Tank shells can destroy the door if it is in a vehicle-accessible path (optional — set per-level). If designated destructible by the level designer:
- 1 tank shell: door is bent/destroyed (replaced with a dented open-frame sprite)
- The destroyed state shows a crumpled steel door hanging partially off the frame

---

## Collision Type
- **Locked/Closed:** Full block — same as concrete wall (1 tile full blocker)
- **Open:** Zero collision — the door is slid into the wall (disappears into the wall thickness). Passage is fully clear.

---

## Animation Needs
**Required:** Open/close animation (the door slides horizontally into the wall). Indicator light state change (red to green). See animation_prompts/.

---

## Technical Constraints
- Door must read as sealed and impenetrable when locked — no gaps around the frame
- Indicator light must be visible and color-coded — red = locked is a universal game language the player already knows
- The door open animation must be fast enough to not feel sluggish (0.4s max)
- The open door state (door slid into wall pocket) is a hidden sprite state — the door effectively disappears. The door frame remains visible as a decorative element.
- Two orientation variants required: door facing south-east (south wall) and door facing north-east (east wall) — for isometric grid compatibility
