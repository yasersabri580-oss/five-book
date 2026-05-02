# CHARACTER PROFILE — RECLAIMER MILITIA SOLDIER

---

## Character Name
**Reclaimer Militia Soldier** *(no individual name — faction grunt unit)*
*In-game faction name: The Reclaimer Militia*

---

## Role in the Game
**Human enemy — Reclaimer faction infantry.**
Reclaimer Militia Soldiers are opportunistic human fighters who loot the battlefield and attempt to seize enemy vehicles for themselves. They appear in Missions 2, 5, and 9. They are chaotic, aggressive, and unpredictable — a contrast to the mechanical precision of FORGE and the disciplined structure of SENTINEL.

---

## Visual Identity
A Reclaimer looks like a soldier built from whatever was left after the war started. Mismatched gear, improvised armor, spray-painted surplus. They look dangerous because they are — but they also look like people who are barely holding it together.

- **Helmet:** No standard helmet. Some soldiers wear a beaten steel construction helmet spray-painted in flat brown or rust red. Others have no head protection at all and wear a wrapped cloth balaclava or a beaten leather cap. **Use: spray-painted steel construction helmet variant (brown #6A4020, with peeling edges and paint splatter).**
- **Upper body:** Mismatched jacket — a combination of different military surplus: an olive field jacket (worn, patches stripped off) with a half-attached piece of vehicle tire rubber bolted to the left shoulder as improvised armor. The bolts are visible and obviously field-made. Shirt collar visible underneath — dark grey or black.
- **Chest:** No formal chest rig. A wide canvas sling across the chest holding two ammo bandoliers (cartridge loops visible). A single large pouch on the left hip (handmade from a repurposed bag).
- **Arms:** Right arm in a fingerless work glove (heavy duty, dark worn leather). Left arm bare below the shoulder armor — forearm visible with a crude black ink tattoo ("RECLAIM" text, blocky letters, visible on left forearm).
- **Legs:** Mix of cargo trousers (brown/tan) and knee-high military boots with mismatched lacing. Right boot has a section of duct tape over a split in the leather.
- **Color scheme:** Warm earthy tones throughout. Brown, tan, rust-red, worn olive. No clean lines, no uniformity.

---

## Personality
Reclaimers are loud, aggressive, and tribal. They communicate in shouted taunts and fight in reckless charges. They loot mid-battle if given the opportunity — an enemy tank destroyed near them is a priority target for scavenging. They have no loyalty to FORGE or SENTINEL; they have loyalty to the spoils of war.

Some Reclaimers want to fight FORGE (they lost homes to it). Others are purely opportunistic. In battle they mix Aggressors (who charge), Suppressors (who pin-and-wait), and Looters (who run to any destroyed vehicle). They retreat only when outnumbered badly.

---

## Story Relevance
Reclaimers demonstrate that Verak's civilian population did not simply flee — some became predators. They complicate the moral landscape: they are enemies of Kael, but also victims of FORGE's destruction. Rina confirms in Mission 2 that the Reclaimer faction has split — some want to fight FORGE, others want to exploit the chaos.

---

## Gameplay Purpose
- Enemy infantry in Missions 2, 5, and 9
- AI behaviors: Aggressor (charge), Suppressor (pin), and unique Scavenge Rush (sprint to destroyed vehicle to claim it)
- Use of molotovs as secondary attack (throwing animation required)
- Will commandeer destroyed player tank if able (Scavenge Rush mechanic)
- Less accurate than SENTINEL but more erratic — harder to predict

---

## Size / Silhouette / Body Type
- **Height:** Medium, approximately same height as Kael (1.8–1.85m)
- **Build:** Stocky, solid. Not lean — these are physical workers and fighters.
- **Silhouette key features:** Improvised shoulder armor (left shoulder bulk), spray-painted helmet, bandoliers across chest, mismatched boots
- **Sprite height:** 3 tiles (same as Kael — human scale)
- **Isometric footprint:** 1×1 tile

---

## Color Palette
| Element | Color |
|---|---|
| Helmet | Flat brown (#6A4020) with rust-red and tan paint splatter |
| Jacket | Worn olive (#5A5040) |
| Shoulder armor (rubber) | Matte dark grey-black (#2A2A22) with bolt head highlights |
| Bandoliers | Tan canvas (#9A8060), brass cartridge heads (#B08840) |
| Cargo trousers | Worn tan-brown (#8A7050) |
| Boots | Dark worn brown (#4A3020) |
| Glove (right) | Dark leather grey-brown (#4A3828) |
| Left forearm skin | Weathered tan (#8A6A48) |
| Tattoo | Flat black (#1A1A1A) |
| Hip pouch | Repurposed fabric, dark olive (#4A4830) |

---

## Weapon / Tool
| Slot | Item | Description |
|---|---|---|
| Primary | Assault rifle (surplus) | Beat-up AK-variant style, scratched dark finish, wooden stock, curved 30-round mag |
| Secondary | Molotov cocktail | Glass bottle with rag wick, visible liquid sloshing in bottle (for held frame) |
| Melee | None defined — charges with rifle butt in gameplay |

---

## Movement Style
- Aggressive and forward-leaning. Less disciplined than SENTINEL or Kael.
- Walk: heavier, stomping, slightly hunched. Confidence through bulk.
- Run: all-out sprint with arms pumping and rifle held one-handed at the side (loose grip).
- Scavenge rush: same sprint but angled toward a vehicle target, rifle held loosely.

---

## Combat Style
- Aggressor variant: charges toward player in a straight line, shooting from the hip.
- Suppressor variant: drops into cover and fires sustained burst.
- Molotov throw: stops, pulls molotov from hip pouch, lights it (lighter flicker — 1-frame), throws overhead arc.
- When reinforced by numbers: charges in groups of 2–3 from different directions.

---

## Animation Requirements
| State | Loop | Notes |
|---|---|---|
| Idle | Yes | Slightly shifting weight, impatient energy |
| Walk (all 8 directions) | Yes | Heavy, stomping gait |
| Run (all 8 directions) | Yes | One-handed rifle, aggressive sprint |
| Attack — rifle (all 8 directions) | Yes (while firing) | Hip-fire style — not a careful aim |
| Attack — molotov throw (4 directions) | No | Stop → light → throw overhead |
| Hurt (all 8 directions) | No | Violent stagger, louder read than FORGE drone |
| Death (4 directions) | No | Dramatic collapse |
| Scavenge sprint (toward vehicle — 4 directions) | Yes | Same as run but no shooting |

---

## Direction Requirements
All states: **8 directions** for combat states, **4 directions** for special actions (molotov, scavenge).

---

## Technical Constraints for Consistency
- The improvised shoulder armor on the LEFT shoulder must be visible in most directional views. In right-profile view it will be partially occluded — this is acceptable.
- The RECLAIM tattoo on the left forearm is a detail for close-up views and cutscenes. In small sprite display it may not be readable — do not sacrifice readability for the tattoo.
- The spray-painted helmet color splatters must be recognizable as deliberate markings (painted, not battle damage) — this distinguishes Reclaimers from SENTINEL at a glance.
- Molotov: the bottle and rag must be readable at sprite scale. Keep it a simple silhouette — round bottle, rag at top.
