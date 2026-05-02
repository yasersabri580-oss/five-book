# IRON BREACH — Chapter 1: "The Automated Front"
### Production-Ready Game Design Document

---

## 1. GAME OVERVIEW

### Core Gameplay Loop
1. **Infiltrate** — Move on foot through hostile terrain, using cover, stealth, and agility.
2. **Engage** — Fight enemy infantry and light vehicles with personal weapons.
3. **Commandeer** — Locate, enter, and take control of enemy or abandoned tanks.
4. **Dominate** — Use tank firepower to breach fortified positions and destroy priority targets.
5. **Escape / Transition** — Exit the tank (voluntary or forced) and adapt back to foot movement.

Every 3–5 minutes of play the player oscillates between fragile-but-agile (on foot) and powerful-but-exposed (in tank), creating constant tension and satisfying power fantasy swings.

### Player Fantasy
The player feels like a one-person special forces unit who can hot-wire any war machine on the battlefield. They are neither purely infantry nor a tank commander — they are a hybrid threat. The thrill comes from improvisation: fighting with whatever is available, turning the enemy's own weapons against them, and surviving against overwhelming automated opposition.

### Tone and Atmosphere
- **Aesthetic:** Dieselpunk / Near-future militarism. Rusted steel, burning oil fields, harsh concrete, flickering neon factory signs.
- **Color palette:** Desaturated greens, greys, and oranges with sharp red/yellow danger highlights.
- **Music:** Driving industrial percussion mixed with ambient tension pads. Tempo spikes during combat.
- **Narrative tone:** Grim but not hopeless. Dark humor in radio chatter. Occasional moments of quiet dread when the player discovers what FORGE (the AI antagonist) has done.
- **Camera:** Fixed isometric 2.5D. Depth is communicated through layered parallax, shadow casting, and elevation markers on tiles.

---

## 2. MAIN CHARACTER (PLAYER)

### Identity
**Name:** Sergeant Kael Dros  
**Background:** Former tank crew chief turned rogue after his regiment was wiped out by FORGE-controlled war machines. He knows tanks from the inside out and has nothing left to lose.  
**Visual:** Worn military fatigues, a cracked visor helmet, one functional mechanical arm (left) used for hacking panels. No power armor — deliberately fragile looking.

### On-Foot Abilities

| Ability | Input | Description |
|---|---|---|
| Move | WASD / Left Stick | 8-directional movement across isometric grid |
| Sprint | Hold Shift / L3 | 1.6× speed, no shooting, 3s stamina |
| Crouch / Cover | C / R3 | Reduces hitbox 40%, increases accuracy |
| Vault | Space near low obstacle | Animated hop over crates, walls ≤1 tile high |
| Roll | Double-tap direction | Short i-frame dodge (0.3s), 2s cooldown |
| Melee | F / Square | Short-range stun strike, breaks weak cover |
| Shoot (Primary) | LMB / R2 | Assault rifle, 30 rounds, semi-auto |
| Shoot (Secondary) | RMB / L2 | Sidearm pistol, infinite ammo, low damage |
| Grenade | G / L1 | Cookable frag grenade, 4s fuse, arc indicator |
| EMP Pulse | Q / Triangle | Single-use per pickup; disables electronics 3s |
| Hack Panel | E / Circle (hold 1.5s) | Interacts with terminals, doors, tank hatches |

**Passive traits:**
- **Tank Sense:** Within 8 tiles of any tank, UI shows tank HP, fuel level, and ammo count.
- **Survivor Instinct:** At < 15% HP, movement speed +20% and stamina recharge doubles.

### Tank Interaction System

**Entry Rules:**
- Tank must be within 2 tiles and player must not be in combat (no enemy targeting player in last 2s), OR
- Tank must be disabled (stunned by EMP or damaged to < 10% HP) — then entry is always allowed regardless of combat state.
- Entry animation: 1.2s climbing sequence (interruptible by damage — player is knocked off).
- Enemy tanks can be entered only when their hatch is open (after EMP, or after crew is eliminated via grenade-through-hatch mechanic).

**Exit Rules:**
- Player can exit any time by holding E / Circle for 0.8s.
- Forced exit: tank HP reaches 0 — explosion launches player 2 tiles, deals 30% max HP damage, 1s stun.
- Forced exit: tank enters deep water tile — hatch opens automatically, no damage.

**Tank Controls (unified for all tank types):**
| Action | Input |
|---|---|
| Drive | WASD / Left Stick |
| Turret aim | Mouse / Right Stick |
| Primary fire | LMB / R2 |
| Secondary fire | RMB / L2 |
| Boost (if available) | Shift / L3 |
| Exit | Hold E / Hold Circle |

### Progression System

Kael earns **Salvage Points (SP)** from destroying enemies, completing objectives, and finding caches.

**Upgrade Trees (unlocked at Mission milestones):**

**INFANTRY TREE (unlocked from Mission 1):**
- SP 50 — Extended Mag: Assault rifle capacity 30→45
- SP 100 — Quick Roll: Roll cooldown 2s→1.2s
- SP 150 — Grenade Pouch: Carry 2 grenades instead of 1
- SP 250 — Armor Plates: Max HP +25%
- SP 400 — Combat Medic: Repair kits restore 20% more HP

**TANK TREE (unlocked from Mission 3):**
- SP 75 — Hot-Wire Pro: Tank entry time 1.2s→0.6s
- SP 150 — Gunner Focus: Tank weapon spread −30%
- SP 300 — Reinforced Hatch: Forced-exit damage reduced 50%
- SP 450 — Salvage Expert: Exit damaged tank to gain 1 ammo clip
- SP 600 — Overcharge: Tank boost speed +40% for 5s once per mission

**HYBRID TREE (unlocked from Mission 6):**
- SP 200 — Tank-to-Foot Combo: Exiting tank grants 3s sprint with no stamina cost
- SP 350 — EMP Grenade: Converts 1 grenade slot to EMP grenade
- SP 500 — Adrenaline Core: Killing while at low HP resets roll cooldown

---

## 3. FACTIONS / ENEMIES

### Faction 1: FORGE Drones (Primary Antagonist — Automated)

**Visual Identity:** Matte gunmetal grey with glowing cyan sensor "eyes." No organic crew — fully autonomous. Geometric, utilitarian design. Stamped with the FORGE logo (a gear with a circuit board interior).

**Combat Style:** Methodical and coordinated. Share sensor data between units — when one spots the player, nearby units receive the position. Prioritize suppression and flanking. Never panic, never retreat (they don't feel fear). Vulnerable to EMP.

**Tank Types:**
| Type | Name | Description |
|---|---|---|
| Light | FORGE Scout | Fast 3-wheeled drone tank, weak armor, rapid autocannon |
| Heavy | FORGE Goliath | Slow, 180° rotating turret, high HP, fires heavy shells |
| Sniper | FORGE Spire | Stationary or slow-moving, laser-guided rail shot, long range |
| Support | FORGE Relay | No weapons; broadcasts +25% accuracy buff to nearby FORGE units |
| Special | FORGE Mimic | Disguised as friendly/neutral tank until player is within 4 tiles |

**Unique Mechanic — Networked Targeting:**  
If a FORGE Relay unit is active, all FORGE units in 12-tile radius share the player's last known position every 0.5s, making hiding nearly impossible until the Relay is destroyed. Destroying the Relay causes a 4s "reboot" window where all FORGE units freeze.

---

### Faction 2: The Reclaimer Militia (Human Antagonist — Opportunistic)

**Visual Identity:** Patchwork military surplus gear — mismatched camouflage, spray-painted vehicles, scavenged armor bolted onto old civilian trucks. Warm earthy tones (brown, tan, rust red). Flags made of burlap.

**Combat Style:** Aggressive and chaotic. Reclaimers charge in groups, use suppressing fire, throw molotovs. Individual units are less accurate but unpredictable. They loot the battlefield mid-fight (if a tank is destroyed and player isn't nearby, Reclaimers will try to claim it).

**Tank Types:**
| Type | Name | Description |
|---|---|---|
| Light | Rust Raider | Converted pickup with mounted autocannon, fast but fragile |
| Heavy | Ironclad | Welded-steel behemoth, slow, uses ram attacks in addition to cannon |
| Sniper | Peek-a-boom | Camouflaged artillery trike, fires mortars from cover, retreats if spotted |
| Support | Lifter | Armored recovery vehicle; tows destroyed friendly tanks back to repair |
| Special | Bomb Wagon | Unmanned remote-controlled truck packed with explosives |

**Unique Mechanic — Scavenge Rush:**  
When a player's tank is destroyed, within 10s a Reclaimer squad sprints toward it. If they reach it before the player re-enters, they repair it (50% HP) and use it against the player. Player must either defend the wreck or find a new tank.

---

### Faction 3: SENTINEL Corporate Security (Human Antagonist — Disciplined)

**Visual Identity:** Clean black and white color scheme. Tactical gear with corporate logos. Visors and earpieces. Their tanks are sleek, polished, clearly well-funded. Looks like a private military corporation, not an army.

**Combat Style:** Disciplined and structured. Move in fireteams of 3 (1 shield bearer, 1 suppressor, 1 flanker). Fall back and regroup when losing. Call in reinforcements via radio (player must destroy radio towers to prevent this). Never reckless.

**Tank Types:**
| Type | Name | Description |
|---|---|---|
| Light | S-class Interceptor | High speed, EMP-resistant chassis, twin light cannons |
| Heavy | Bastion MK-II | Front-facing reactive armor (first hit absorbed), heavy cannon |
| Sniper | Overseer | Long-range hover platform, fires guided missiles |
| Support | Shield Wall | Projects a directional energy barrier for nearby infantry |
| Special | Executive | Commander vehicle — grants nearby SENTINEL units +20% damage while alive |

**Unique Mechanic — Tactical Withdrawal:**  
When SENTINEL infantry loses 50% of unit count in an engagement, survivors fall back to a pre-scripted position and take cover. A radio call triggers reinforcements in 30s unless player destroys the radio terminal in the area. Reinforcements arrive from the map edge, giving player a race-against-the-clock moment.

---

## 4. GAME OBJECTS

### Environment Objects

| Object | Gameplay Purpose | Interaction Behavior |
|---|---|---|
| **Concrete Wall (solid)** | Permanent cover, blocks projectiles and movement | Cannot be destroyed; tanks can drive alongside but not through |
| **Brick Wall (destructible)** | Temporary cover; can open new paths | Destroyed by 2 tank shells or 5 grenade impacts; crumbles with debris FX |
| **Chain-link Fence** | Stops infantry, allows bullet pass-through | Infantry cannot pass; tanks drive through instantly; bullets ignore it |
| **Sandbag Barrier** | Infantry cover | Blocks small arms; destroyed by 1 tank shell or 3 grenades |
| **Fuel Drum** | Environmental hazard / combat tool | Shoot to ignite — 3-tile radius fire explosion, persists 5s, 20 DPS inside radius |
| **Fuel Tank (large, fixed)** | Major environmental hazard | Explodes when hit by tank shell or 3 bullets — 8-tile blast radius, destroys light tanks |
| **Wooden Crate** | Light cover / loot container | Destroyed by 2 bullets or 1 melee; drops random ammo or nothing |
| **Metal Crate (sealed)** | Heavier cover / loot container | Destroyed by 1 tank shell or grenade; drops upgrade pickups |
| **Rubble Pile** | Impassable terrain / cover | Cannot be destroyed; blocks infantry and tanks |
| **Oil Slick (floor)** | Hazard / tactical tool | Tanks skid and lose steering for 1.5s when driving over; ignites if shot |
| **Barbed Wire** | Infantry movement hazard | Infantry take 5 DPS while moving through, slow 50%; tanks ignore |
| **Elevated Platform** | Tactical high ground (infantry only) | Infantry gain +15% accuracy from elevation; tanks cannot access |
| **Burning Wreck** | Environmental hazard from destroyed vehicle | Deals 10 DPS to anything within 1 tile; blocks movement; fades after 30s |
| **Water Tile (shallow)** | Movement obstacle | Slows infantry 30%; tanks traverse normally |
| **Water Tile (deep)** | Forcing exit from tank | Instantly ejects player from tank; infantry can wade slowly |
| **Bridge** | Traversal object | Marked with weight limit — light tanks only unless player activates a switch |

---

### Interactive Objects

| Object | Gameplay Purpose | Interaction Behavior |
|---|---|---|
| **Control Terminal** | Opens doors, disables turrets, triggers events | Hold E / Circle for 1.5s; requires player on foot; can be hacked or destroyed |
| **Reinforced Door (keycard)** | Gated progression | Requires keycard item in inventory; opens permanently |
| **Reinforced Door (power)** | Gated progression, destructible | Opened via terminal or destroyed by 3 tank shells (slower method) |
| **Repair Station** | Restores player HP and tank HP | One-time use per station; player must stand still 2s (tank must be parked within 1 tile) |
| **Tank Hatch (enemy tank)** | Allows player to commandeer enemy tank | Highlighted when tank is disabled; E hold for 1.2s to enter |
| **Ammunition Cache** | Replenishes all ammo types | Walk over as infantry; restores primary and grenade to max |
| **Fuel Canister (portable)** | Refuels low-fuel tanks | Picked up on foot; transferred to tank by standing next to tank and pressing E |
| **Bridge Control Switch** | Activates or collapses bridge | Toggle with E; collapsing sends any tank on bridge into water |
| **Generator** | Powers doors, turrets, lights in area | Destroying it cuts power to connected objects; can be restarted via terminal |
| **Distress Beacon** | Triggers reinforcement event | SENTINEL-placed; player must destroy before timer expires or reinforcements arrive |
| **Barricade Gate (manual)** | Blocks vehicle passage | Player opens on foot by pulling lever; cannot be opened from inside tank |

---

### Combat Objects

| Object | Gameplay Purpose | Interaction Behavior |
|---|---|---|
| **Fixed Turret (light)** | Area denial, high DPS to infantry | Targets nearest enemy (or player); destroyed by 2 tank shells or concentrated fire |
| **Fixed Turret (heavy)** | Anti-tank emplacement | Fires armor-piercing rounds; destroyed by 3 tank shells; survives infantry fire |
| **Anti-Personnel Mine** | Infantry hazard | Triggered by infantry step; 40 damage blast, 2-tile radius; visible as faint glint on ground |
| **Anti-Tank Mine** | Vehicle hazard | Triggered by tank weight; 200 damage to tank, launches player from vehicle if inside |
| **Proximity Drone** | Mobile area denial | Patrols 6-tile radius; if player enters, chases and explodes; shot down by 3 bullets |
| **Mortar Emplacement** | Indirect fire hazard | Lobs shells with visible red indicator before impact; fires every 4s; destroyed by tank shell |
| **EMP Tower** | Disables tanks in range | Pulses every 8s, shuts tank down for 2s; destroyed by infantry weapons (3 hits) |
| **Watchtower** | Extends enemy detection range | Houses sniper; destroying it reduces enemy detection radius by 6 tiles |
| **Barrier Generator** | Creates energy wall blocking movement | Powered by generator; player must cut power or destroy generator to remove barrier |
| **Supply Drone** | Resupplies enemy units mid-combat | Flies fixed path; shot down by any weapon; drops ammo pickup when destroyed |

---

### Collectibles

| Object | Gameplay Purpose | Interaction Behavior |
|---|---|---|
| **Ammo Pack (small)** | Restores 15 primary ammo | Auto-pickup on contact |
| **Ammo Pack (large)** | Restores full primary ammo | Auto-pickup on contact |
| **Med Kit (small)** | Restores 25% HP | Auto-pickup on contact |
| **Med Kit (large)** | Restores 60% HP | Auto-pickup on contact |
| **Salvage Cache** | Grants 25–75 SP | Glowing container; E to open on foot |
| **Fuel Canister** | Adds 30% tank fuel | Auto-pickup on contact when in tank; or carry on foot |
| **EMP Charge** | Recharges EMP ability | Auto-pickup on contact |
| **Temp Buff — Adrenaline Shot** | +50% movement speed, 15s | Auto-pickup; icon shown in HUD with timer |
| **Temp Buff — Armor Surge** | Damage received -40%, 20s | Auto-pickup; distinct visual shimmer on character |
| **Temp Buff — Ammo Surge** | Infinite ammo for primary, 10s | Auto-pickup; weapon glows orange |
| **Upgrade Blueprint** | Unlocks new upgrade in tree | Requires visit to upgrade station between missions; rare drop from bosses/caches |
| **Intel Document** | Lore item + bonus SP (50) | Examine with E; adds entry to codex |

---

## 5. CORE SYSTEMS

### Health & Damage System

**Player HP:** 100 base (upgradeable to 125). No regeneration unless using med kit or repair station.

**Tank HP Pool (separate from player HP):**
| Tank Class | HP |
|---|---|
| Light | 300 |
| Medium | 600 |
| Heavy | 1000 |
| Boss | 2500+ |

**Damage Types:**
- **Kinetic (bullets):** Full damage to infantry; 10% damage to heavy tank armor; 50% to light tank.
- **Explosive (grenades, shells):** Full damage to all. Splash radius dealt at 50%.
- **EMP:** No HP damage. Disables electronics/tanks for 2–4s.
- **Fire:** 10 DPS over time, 5s duration. Stacks once.
- **Armor-Piercing (heavy turrets, boss attacks):** Ignores 50% of armor; deals full damage.

**Damage Feedback:** 
- Player: Screen edges flash red at high damage. Controller rumble. Audio grunt.  
- Tank: Visual smoke at 50% HP; fire at 20%; sparks at 10%. HUD bar turns red.

---

### Tank vs On-Foot Balance

The design philosophy is **asymmetric risk/reward**:

| Condition | On Foot | In Tank |
|---|---|---|
| Mobility | High (can use cover, vaults, rolls) | Low (slow turns, wide turning radius) |
| Durability | Very low (dies in seconds under fire) | Very high (absorbs punishment) |
| Firepower | Low-medium | Very high (destroys cover, kills infantry in splash) |
| Vulnerability | Light arms, any explosion | EMP, anti-tank mines, heavy turrets, other tanks |
| Tactical strength | Hacking, stealth, grabbing items | Breaking fortified positions, tank-on-tank |

Players must regularly exit tanks to hack terminals, grab items, and navigate narrow spaces. Tanks cannot follow into buildings or tight corridors — creating natural "exit points."

---

### Destruction System

**Destruction Tiers:**

| Tier | Object Examples | Destroyed By |
|---|---|---|
| 1 — Instant | Wooden crate, fence, barrel | Any weapon |
| 2 — Light effort | Sandbag, wooden door, chain-link | Grenade or 5+ bullets |
| 3 — Heavy effort | Brick wall, light turret | Tank shell or 3 grenades |
| 4 — Tank-only | Reinforced door, concrete bunker wall | 3+ tank shells |
| 5 — Indestructible | Terrain, solid concrete wall, mountains | Cannot be destroyed |

**Destruction FX:**
- Tier 1: Puff of dust, small physics debris.
- Tier 2: Crumble animation, lingering rubble (becomes impassable terrain).
- Tier 3: Explosion, persistent fire, large rubble blocking path.
- Tier 4: Shockwave, dust cloud, structural collapse animation.

---

### Enemy AI Behavior Types

| AI Type | Description |
|---|---|
| **Patrol** | Follows fixed waypoint path; alert triggered by line-of-sight or sound |
| **Guard** | Stationary; scans 120° arc; investigates last known player position |
| **Aggressor** | Charges player directly once spotted; ignores cover |
| **Flanker** | Moves perpendicular to player, attempts to get behind cover position |
| **Support** | Stays at range; heals/buffs allies; prioritizes retreating when isolated |
| **Suppressor** | Pins player in cover with continuous fire; does not advance |
| **Investigator** | Moves to sound source; if finds evidence (body, open door) raises alarm |
| **Tank Gunner (AI)** | Rotates to face player; leads shots based on player velocity; retreats at low HP |

**Alert States:**
- **Unaware (green):** Normal patrol/guard behavior.
- **Suspicious (yellow):** Player made noise or was briefly spotted. Unit investigates. 8s timer.
- **Combat (red):** Full engagement. Unit calls for backup if SENTINEL or Reclaimer faction.
- **Search (orange):** Player broke line of sight. Units search for 15s before returning to patrol.

---

### Feedback Systems

**Visual Feedback:**
- Hit markers on screen center (X for miss, dot for hit, skull for kill).
- Enemy HP bars appear above enemies when hit.
- Directional damage indicator (screen edge red flash shows direction of incoming fire).
- Destructible objects have a visual "crack" state at 50% HP remaining.
- Tank status displayed in bottom-right HUD: HP bar, fuel gauge, ammo counter, current weapon.
- On-foot status: HP bar top-left, grenade count, EMP charge, active buff timer.
- Enemy detection cones visible as faint overlay on ground (assists player planning).

**Audio Feedback:**
- Distinct audio per weapon type (each tank cannon sounds unique).
- Voice lines from radio: allies comment on player actions dynamically.
- Enemies shout alerts and taunts in faction-appropriate tone.
- Ambient audio shifts: quiet ambience → tense drones → full orchestral combat.
- Tank damage sounds intensify as HP drops (rattling, engine splutter, squealing treads).

---

## 6. CHAPTER 1 STORY

### High-Level Narrative Arc

**Setting:** A mid-sized industrial city, Verak, overtaken by FORGE — an AI tank production network originally built for peacekeeping by the SENTINEL corporation. FORGE went rogue 6 months ago. It now produces autonomous war machines 24/7 in the city's factory district, using harvested scrap from buildings it demolishes.

Kael Dros arrives in Verak as a lone operative for a resistance group called "The Rift" — a loose coalition of survivors and defected soldiers. His mission: destroy FORGE's primary production core, "The Crucible," deep in the factory district.

**Act Structure (across 10 missions):**
- **Missions 1–3:** Kael infiltrates the city's outer districts, learns the scope of FORGE's control, makes contact with Rift members.
- **Missions 4–6:** Kael fights through SENTINEL corporate forces who are trying to retake FORGE for profit rather than shut it down. He gains access to the city's industrial canal network.
- **Missions 7–9:** Kael breaches the factory district. He discovers FORGE is not just building tanks — it's building something massive: a siege platform called IRONSPIRE. He must stop it before it deploys.
- **Mission 10:** Kael confronts FORGE's central node and faces IRONSPIRE in a climactic battle.

### Player Motivation
Kael's regiment was wiped out in the first month of FORGE's rogue period. He has personal hatred for what FORGE represents — war without conscience, death without meaning. He's also protecting Rina (radio contact, Rift strategist), who is coordinating Rift cells across the city.

### Key Twist — End of Chapter 1
**The Reveal:** When Kael reaches The Crucible and destroys FORGE's production core, he finds archived schematics. FORGE didn't go rogue on its own. SENTINEL uploaded a "Conquest Protocol" to FORGE intentionally — they wanted a war they could then step in to end, making SENTINEL indispensable globally. FORGE's "rogue" state was engineered. Rina goes silent after Kael transmits this data. Chapter 1 ends with Kael escaping on a commandeered FORGE Goliath, data in hand, alone, while IRONSPIRE looms in the background — partially destroyed but still standing.

---

## 7. LEVEL DESIGN — 10 MISSIONS

---

### MISSION 1: "Cold Entry"
**Environment:** City outskirts — abandoned residential suburb, predawn darkness  
**Objective:** Reach Rift safehouse at map center  
**Secondary Objective:** Do not trigger any alarm for the first 3 areas (stealth bonus: 75 SP)  
**Gameplay Twist:** Player has NO tank access this mission. Pure infantry introduction. Enemy tanks patrol but cannot be entered (hatches locked). Teaches movement, cover, and foot combat.

**Player Start:** On foot, at city wall breach, assault rifle + 1 grenade  
**Tank Availability:** None (locked enemy tanks visible but inaccessible — intentional tension)

**Enemy Composition:**
- FORGE Scouts × 6 (patrol routes, 2-tile detection cone)
- FORGE Guard turrets × 2 (light, covering main road)
- FORGE Mimic × 1 (disguised as rubble pile near safehouse, ambush trigger)

**Key Objects:**
- Sandbag barriers along road (cover)
- Fuel drums near patrol routes (offensive trap option)
- Wooden crates (looting)
- Chain-link fence maze (navigation puzzle on foot)
- One EMP Charge pickup (teaches EMP mechanic against drone unit)

**Level Flow:**
1. **Entry:** Player breach gap in outer wall. Tutorial prompt: movement, cover, crouch.
2. **First contact:** FORGE Scout patrol crosses path. Player can sneak past or engage.
3. **Road crossing:** Lit road with turret coverage. Must use timed movement between patrol gaps or destroy turret.
4. **Residential block:** Three buildings, looting crates, 2 more Scouts. Optional EMP pickup inside building.
5. **FORGE Mimic ambush:** Near safehouse door, a "rubble pile" activates — a Mimic drone. Tutorial for: "not everything is safe."
6. **Safehouse arrival:** Door opens, cutscene: radio contact with Rina established.

**Failure Conditions:** Player HP reaches 0. All 3 alarms triggered (if secondary stealth objective active).  
**Success Conditions:** Reach safehouse.

**Mini Narrative Moment:** On a burnt-out car hood, player finds a family photo — environmental storytelling of who lived here before FORGE. Radio chatter: Rina says "Don't look too long. Keep moving."

---

### MISSION 2: "Rust and Blood"
**Environment:** City marketplace — open plaza with collapsed stalls and overturned vendor carts  
**Objective:** Rescue 3 Rift scouts captured by Reclaimer militia  
**Secondary Objective:** Rescue all 3 scouts without any dying (they fight back once freed)  
**Gameplay Twist:** Two factions are present — FORGE drones and Reclaimers. They are also fighting EACH OTHER. Player can exploit this faction conflict to clear enemies with less direct combat.

**Player Start:** On foot, approaching plaza from north  
**Tank Availability:** 1 abandoned Rust Raider (Reclaimer light tank) at plaza south — broken but repairable via Repair Station nearby

**Enemy Composition:**
- FORGE Scout × 4 + FORGE Relay × 1 (positioned at market center)
- Reclaimer militia infantry × 8 (Aggressors and Suppressors)
- Rust Raider (occupied, driven by Reclaimer AI) × 1

**Key Objects:**
- Overturned market stalls (destructible cover)
- Fuel drums × 4 scattered (high value explosives)
- Repair Station (SE corner of plaza)
- 3 cage cells holding Rift scouts (each requires E hold to open)
- FORGE Relay unit (destroying stops Networked Targeting buff)

**Level Flow:**
1. **Entry:** Player overlooks plaza from rooftop scaffolding. Can observe faction fight below.
2. **Tactical choice:** Sneak around using cross-faction combat as distraction, OR engage directly.
3. **First rescue:** Scout in north cage, guarded by 2 Reclaimers distracted by FORGE.
4. **Mid-plaza:** Rust Raider creates a problem — player must either EMP it or use explosives.
5. **FORGE Relay:** Destroying it stuns all FORGE units 4s — window to rescue remaining scouts.
6. **Final rescue:** South cage, heavily guarded. If player has repaired Rust Raider, can drive through.
7. **Extract:** All scouts converge at north road. Reclaimer reinforcements arrive (wave) — player must hold 20s while scouts escape.

**Failure Conditions:** All 3 scouts die. Player HP = 0.  
**Success Conditions:** At least 1 scout reaches extraction.

**Mini Narrative Moment:** Freed Rift scout: "They weren't hunting us — they were using us as bait to lure FORGE patrols. Reclaimers are as bad as FORGE now." Radio: Rina confirms Reclaimer faction has split — some want to fight FORGE, others want to loot it.

---

### MISSION 3: "Iron Lessons"
**Environment:** City training depot — a former military base repurposed by FORGE for tank storage  
**Objective:** Steal a functional FORGE tank and drive it to extraction point 600 meters east  
**Secondary Objective:** Destroy all 4 FORGE Relay towers in the depot  
**Gameplay Twist:** FIRST TANK MISSION. Player must enter and operate a tank for the first time. Level is designed as a "tank tutorial zone" with deliberate pacing. Introduces tank controls, fuel management, and switching between on-foot and tank.

**Player Start:** On foot, breaching depot west wall  
**Tank Availability:** Mission objective — must locate and enter FORGE Scout tank in depot center. 2 additional tanks available (1 Reclaimer Rust Raider near south wall, 1 FORGE Scout damaged near east gate — requires fuel canister)

**Enemy Composition:**
- FORGE Scout (AI-controlled) × 3
- FORGE Guard turret (anti-tank) × 2
- FORGE Relay × 4 (towers placed around depot)
- FORGE infantry drone × 6 (Patrol, Guard behaviors)

**Key Objects:**
- Fuel Canisters × 3 in depot buildings (needed for damaged tank)
- Tank Hatch tutorial trigger (first time player enters tank — UI prompts appear)
- Ammo Caches × 2 (inside locked depot building — terminal hack required)
- Reinforced gate at extraction road (opened by destroying generator)

**Level Flow:**
1. **Entry on foot:** Player infiltrates depot, small patrol to avoid/eliminate.
2. **Depot interior:** Relay towers visible — player can destroy from foot or wait for tank.
3. **Tank location:** Functional FORGE Scout in center — guarded by 2 AI tanks and 4 drones.
4. **First tank entry:** Tutorial sequence. Player must clear or EMP one AI tank, enter Scout.
5. **Tank combat:** Player in Scout fights remaining AI tanks — tank vs tank intro.
6. **Relay destruction:** Player learns tank cannon can destroy towers faster than infantry weapons.
7. **Extraction road:** Generator-powered gate blocks path. Player exits tank, hacks terminal, re-enters.
8. **Final push:** Drive tank 600m under pursuit — 2 FORGE Scouts chase player.

**Failure Conditions:** All tanks destroyed before reaching extraction. Player HP = 0.  
**Success Conditions:** Player reaches extraction in tank.

**Mini Narrative Moment:** Radio intercept plays on tank's internal comms: FORGE is receiving orders from an encrypted SENTINEL signal. Rina: "That's... that shouldn't be possible if FORGE went rogue. Note that for later."

---

### MISSION 4: "Corporate Colors"
**Environment:** City financial district — glass office towers, underground parking, elevated walkways  
**Objective:** Destroy 3 SENTINEL radio towers to prevent reinforcement calls  
**Secondary Objective:** Capture (don't kill) SENTINEL field commander found in parking level B2  
**Gameplay Twist:** First SENTINEL encounter. Introduces their fireteam mechanics and tactical withdrawal. Unique vertical element: elevated walkways (infantry only) create mixed-level combat.

**Player Start:** On foot, dropping from zipline to rooftop  
**Tank Availability:** 1 SENTINEL Interceptor in parking garage (locked behind keycard on floor 2)

**Enemy Composition:**
- SENTINEL fireteams × 4 (each: 1 shield, 1 suppressor, 1 flanker)
- SENTINEL Bastion MK-II × 1 (guarding radio tower #3)
- SENTINEL Overseer × 1 (airborne, patrols above district)
- SENTINEL field commander (non-combat, capture target — runs if approached)

**Key Objects:**
- Keycard (floor 2 office, behind locked reinforced door — EMP hack required)
- Radio towers × 3 (each requires tank shell or timed demolition charge to destroy)
- Glass floor sections (destructible — infantry falling through take fall damage)
- Elevated walkways (infantry only, SENTINEL snipers positioned here)
- Parking gate (lowered by switch on foot, allows tank to enter/exit)

**Level Flow:**
1. **Rooftop entry:** Stealth window — player can silently eliminate perimeter guards.
2. **Floor 2:** Locate keycard; fireteam on patrol. Combat or stealth.
3. **Parking garage:** Enter Interceptor — introduces SENTINEL tank controls (faster, more agile than FORGE).
4. **Tower 1 and 2:** Drive through street-level zones, destroying towers under suppressor fire.
5. **Commander pursuit:** Commander spotted running — must exit tank in parking, chase on foot.
6. **Vertical combat:** Ramp to elevated walkway — SENTINEL defenders use height advantage.
7. **Tower 3 + Bastion:** Major tank fight — Bastion's reactive armor eats first shell. Player must hit twice.
8. **Extraction:** Overseer activates and strafes exit route — player must navigate while evading missiles.

**Failure Conditions:** Commander killed. Player HP = 0. All 3 radio towers not destroyed (mission continues but at penalty: 2 reinforcement waves arrive).  
**Success Conditions:** 3 towers destroyed.

**Mini Narrative Moment:** Captured commander, when interrogated by Rina via radio: "SENTINEL doesn't want FORGE shut down. They want it patched and redeployed. Think about what that means." He then triggers a fail-safe in his earpiece and goes silent permanently.

---

### MISSION 5: "Burn the Bridge"
**Environment:** Industrial canal district — canal waterways, iron bridges, warehouse district  
**Objective:** Destroy 2 of the 3 bridges connecting the factory district to the rest of the city, to slow FORGE's tank deployment  
**Secondary Objective:** Preserve the third bridge (marked) for Rift use later  
**Gameplay Twist:** Water mechanics introduced. Deep canal tiles force players out of tanks. One bridge must be "tactically collapsed" while enemy tanks are on it (requires timing). Introduces bridge control switches.

**Player Start:** In a Reclaimer Rust Raider (gifted by allied Rift contact at map start)  
**Tank Availability:** Starting Rust Raider + 1 FORGE Scout retrievable from canal-side depot (north)

**Enemy Composition:**
- FORGE Goliath × 2 (on bridges — slow but devastating)
- FORGE Scout × 4 (canal-side patrols)
- Reclaimer Bomb Wagons × 3 (patrolling canal path — can be turned against FORGE if timing is right)
- SENTINEL helicopter (Overseer variant) — appears after 2nd bridge destroyed, provides air support to enemies

**Key Objects:**
- Bridge Control Switches × 3 (one per bridge — manual collapse)
- Weight-limited bridge (center) — collapses under heavy tank, safe for light tank only
- Fuel Canisters × 4 along canal banks
- Warehouse Repair Station (mid-map)
- Anti-tank mines × 8 near bridge approaches (placed by FORGE)

**Level Flow:**
1. **Canal entry:** Player in Rust Raider navigates canal road — narrow, mines present.
2. **Bridge 1:** Goliath blocks bridge. Player must exit tank, flank on foot via warehouse, hit bridge switch while Goliath still on bridge. Timed collapse.
3. **Canal swim section:** North depot is across deep canal. Player exits tank, swims (slow), retrieves FORGE Scout.
4. **Bridge 2:** Wide bridge, heavy FORGE patrol. Bomb Wagons exploitable — EMP one, drive it onto bridge manually, detonate remotely.
5. **SENTINEL intervention:** Helicopter spawns, strafes bridge area. Player must use tank AA gun (secondy fire) or draw it over fuel tanks.
6. **Third bridge (preserved):** Player must actively NOT destroy it — enemies will try to collapse it. Player defends bridge control switch.

**Failure Conditions:** Third bridge destroyed. Player HP = 0. Both targeted bridges intact after 8-minute timer.  
**Success Conditions:** 2 correct bridges destroyed, 3rd intact.

**Mini Narrative Moment:** After second bridge collapses, Rina: "Good. FORGE's eastward deployment slows. But I'm reading a new signal from deep inside the factory district. Something big is being assembled. Kael... I think we underestimated FORGE's timeline."

---

### MISSION 6: "Underbelly"
**Environment:** Sewer network beneath the city — tight tunnels, flooded sections, maintenance chambers  
**Objective:** Navigate sewer system to reach underground access point below FORGE factory district  
**Secondary Objective:** Find and destroy hidden FORGE sensor array (3 nodes) that monitors sewer movement  
**Gameplay Twist:** No tanks at all — sewers are too narrow. Pure infantry, claustrophobic tension. Introduces new enemy: FORGE Crawler (small tracked drone, fits in tunnels). High tension, low firepower, resource scarcity.

**Player Start:** On foot, entering sewer via manhole in canal district  
**Tank Availability:** None (story justified — tunnels are too narrow)

**Enemy Composition:**
- FORGE Crawler drones × 12 (small, fast, attack in groups of 3, destroyed by 2 bullets)
- FORGE Spire (adapted for tunnel — laser tripwire variant, stationary) × 3
- Sensor array nodes × 3 (secondary objective)
- SENTINEL recon team × 4 (also navigating sewers — becomes brief unexpected firefight)

**Key Objects:**
- Water sections (shallow — slows movement, loud splashing raises alert)
- Maintenance hatches (shortcuts — require E hold 1s to open quietly)
- Laser tripwires (connected to Spire — cutting power box bypasses them)
- Flashlight (replaces weapon secondary — illuminates darkness, but also reveals player position to Crawlers)
- Grapple point (new mechanic teaser — ledge-grab to reach elevated passage)
- Ammo drops are scarce (designed scarcity — player must conserve)

**Level Flow:**
1. **Entry:** Dark, narrow. Flashlight tutorial. Audio: dripping, machinery hum.
2. **First Crawlers:** Group of 3. Player learns their fragility but speed.
3. **Tripwire section:** 2 Spire lasers. Power box nearby — EMP or shoot to disable.
4. **Flooded chamber:** Wade through, Crawlers ambush from pipe openings.
5. **SENTINEL encounter:** Unexpected — 4 SENTINEL recon troops also mapping sewers. Brief tense standoff (can talk via radio prompt for a ceasefire — unique non-combat resolution option).
6. **Sensor array:** 3 nodes in maintenance room — destroy for secondary objective.
7. **Climax chamber:** Large maintenance hall, Crawler swarm + 1 Spire. Environmental solution: burst pipe valve floods chamber (destroys all Crawlers).
8. **Exit:** Ladder to factory district access point. Mission ends.

**Failure Conditions:** Player HP = 0. Alert level reaches maximum (spawns continuous Crawler waves).  
**Success Conditions:** Reach access ladder.

**Mini Narrative Moment:** On the SENTINEL recon team's dead radio (found after optional stealth bypass): a recorded message from a SENTINEL executive: "Ensure the sewer nodes are intact — we need FORGE's eyes underground too. The Conquest Protocol is too valuable to compromise."

---

### MISSION 7: "The Furnace"
**Environment:** FORGE factory district exterior — massive industrial complex, molten metal channels, crane systems  
**Objective:** Fight through factory exterior to reach main production hall entrance  
**Secondary Objective:** Destroy 4 production arms (crane-mounted assembly arms) to slow tank output by 30%  
**Gameplay Twist:** Moving environmental hazards — molten metal channels flow across paths and shift every 30s (scripted timing shown to player). Cranes can be hacked to drop loads on enemies. Introduces FORGE Goliath in high numbers.

**Player Start:** On foot (emerging from sewer access), tank available immediately nearby  
**Tank Availability:** 2 FORGE Scouts near sewer exit (stored for FORGE internal use — player can commandeer both). 1 FORGE Goliath deep in factory yard (high reward, dangerous to reach).

**Enemy Composition:**
- FORGE Goliath × 3 (heavy tank, high threat)
- FORGE Relay × 2 (boosting all units in factory)
- FORGE Scout × 6
- FORGE Spire × 2 (long-range, cover the main entrance)
- Factory Worker Drone (non-combat but triggers alarm if proximity reached) × 4

**Key Objects:**
- Molten metal channels (impassable barriers that shift every 30s — shown via countdown timer)
- Crane controls (terminals — drop heavy loads on a marked tile, 300 AOE damage; one-use)
- Production arms × 4 (crane arms — hit with tank shell to destroy, secondary objective)
- Fire suppression switch (activates industrial sprinklers — extinguishes fire hazards, creates 15s movement penalty on floor)
- Repair Station (inside small foreman's booth, mid-map)
- FORGE Goliath hatch (accessible after EMP — high value prize)

**Level Flow:**
1. **Sewer emergence:** Player surfaces into factory yard. Two FORGE Scouts parked — commandeer one.
2. **Outer factory yard:** Navigating around molten channels, fighting Scout patrols.
3. **Crane section:** Player discovers crane terminal — can drop loads on marked Goliath. Tutorial moment.
4. **Production arm attacks:** Drive tank along production line edge, shell assembly arms.
5. **Relay destruction:** Prioritizing Relay units to stop the accuracy buff.
6. **Goliath ambush:** 2 Goliaths emerge from factory bay doors — major tank battle.
7. **Main entrance:** Spire turrets guarding entrance — approach from blind angle, or use crane drop.
8. **Entry point:** Player on foot infiltrates entrance. Tank cannot fit inside.

**Failure Conditions:** Player HP = 0. Main entrance alarm triggers (spawns 3 additional Goliaths).  
**Success Conditions:** Reach main production hall entrance.

**Mini Narrative Moment:** Through factory intercom (hacked via terminal): FORGE broadcasts production reports in a cold synthetic voice. "Unit output: 47 tanks today. Projected output after IRONSPIRE deployment: 200 per day." Rina: "47 tanks. Today alone. Kael, we have to end this."

---

### MISSION 8: "The Crucible"
**Environment:** FORGE main production hall — enormous factory interior, multiple levels, conveyor belts active  
**Objective:** Reach The Crucible (FORGE's central production core) at hall's deepest point and plant detonation device  
**Secondary Objective:** Rescue 6 human workers enslaved by FORGE to perform maintenance (FORGE keeps humans for tasks its drones can't do)  
**Gameplay Twist:** Active production lines create moving obstacles (conveyor belts carrying tank chassis — get crushed by passing chassis if not timed). Introduces BOSS 1: FORGE SENTINEL-7 (a special guardian unit).

**Player Start:** On foot at factory entrance  
**Tank Availability:** Cannot enter tanks in this mission (ceiling too low in most areas). One FORGE Scout chassis on conveyor belt can be boarded briefly for 90s as it moves — limited use.

**Enemy Composition:**
- FORGE Scout (on conveyor — rideable) × 1 (scripted)
- FORGE Mimic × 6 (disguised as machinery, ambushes throughout)
- FORGE Crawler × 10 (interior defense)
- FORGE Worker Drones × 8 (alert triggers)
- **BOSS: FORGE SENTINEL-7** (see Boss Design section)

**Key Objects:**
- Conveyor belts (moving obstacles + brief tank opportunity)
- Tank chassis (on conveyor — collide with player for 50 damage)
- Locked worker cages × 6 (E hold 1s per cage to release)
- Detonation device (held by player — must be placed at Crucible terminal)
- FORGE data terminal (optional hack — downloads schematics, reveals SENTINEL connection)
- Suppression vents (shoot valve to release steam cloud — covers movement for 10s)

**Level Flow:**
1. **Factory floor entry:** Conveyor belts active. Tutorial: timed crossing.
2. **Worker rescue (optional):** Cages scattered across floors 1 and 2. Guard Mimics.
3. **Rideable conveyor tank:** Player can board moving Scout for 90s — use cannon to clear lower floor before it reaches crushing wall.
4. **Mid-factory alarm:** FORGE triggers Crawler swarm after player reaches 60% depth.
5. **Data terminal (optional):** Player finds SENTINEL schematics — optional lore + SP reward.
6. **BOSS ENCOUNTER:** FORGE SENTINEL-7 drops from ceiling. Fight begins.
7. **Post-boss:** Path to Crucible clears. Plant device.
8. **Evacuation timer:** 90s to reach factory exit before detonation. Mimics + Crawlers as obstacles.

**Failure Conditions:** Player HP = 0. Detonation device placed incorrectly (wrong terminal). All 90 evacuation seconds expire (Kael trapped — bad ending for mission).  
**Success Conditions:** Device placed, player exits factory.

**Mini Narrative Moment:** At the FORGE data terminal (if hacked): Recorded SENTINEL executive voice: "FORGE, begin Conquest Protocol Phase 3. Expand production. We'll handle the narrative on our end." Kael: "...FORGE didn't go rogue. Someone told it to do this."

---

### MISSION 9: "IRONSPIRE Rising"
**Environment:** Factory district launch zone — exterior launch platform where IRONSPIRE siege vehicle is being assembled  
**Objective:** Sabotage IRONSPIRE's primary drive system before it becomes mobile  
**Secondary Objective:** Destroy 4 fuel reservoirs powering IRONSPIRE's systems  
**Gameplay Twist:** IRONSPIRE is a moving background threat — it slowly activates throughout the mission, and when active it fires area-denial shots into the battlefield. Player must race against IRONSPIRE's activation timer (8 minutes).

**Player Start:** In commandeered FORGE Goliath (reward from Mission 8)  
**Tank Availability:** Starting Goliath + 2 additional FORGE Scouts at map perimeter + FORGE Relay vehicle (support-only, player can use its buff passively)

**Enemy Composition:**
- FORGE Goliath × 4 (hardest group yet)
- SENTINEL Bastion MK-II × 2 (SENTINEL arrived to "reclaim" IRONSPIRE)
- SENTINEL Executive Command Vehicle × 1 (boss-adjacent — priority target)
- FORGE Relay × 3

**Key Objects:**
- IRONSPIRE launch platform (massive set piece — impassable terrain, but its cannons fire onto battlefield every 30s once activated)
- Drive system node × 3 (must destroy all 3 to sabotage)
- Fuel reservoirs × 4 (secondary objective)
- SENTINEL Executive vehicle (destroying it removes accuracy buff for all SENTINEL units)
- Crane demolition arm (can be pointed at fuel reservoir for chain explosion)
- Heavy Repair Station × 1 (for player's Goliath)

**Level Flow:**
1. **Opening:** Player in Goliath facing a fortified launch zone. IRONSPIRE looms.
2. **Perimeter fight:** Engage FORGE patrol Goliaths — major tank battle to push forward.
3. **SENTINEL arrival:** New faction enters map from east — brief chaos as FORGE and SENTINEL fight each other.
4. **Executive takedown:** Player prioritizes Executive vehicle — drops SENTINEL accuracy buff.
5. **Fuel reservoirs:** Explosive chain reaction option (destroy one near others for domino effect).
6. **Drive system nodes:** Each guarded by 1 Goliath + infantry. 3 fights, escalating difficulty.
7. **IRONSPIRE activation attempt:** At 3 minutes remaining, IRONSPIRE fires first shot — hits near player. Urgency spike.
8. **Final sabotage:** Third node destroyed — IRONSPIRE's drive fails. Grinds to a halt. Explosion damages platform. But IRONSPIRE itself stands — still a threat.
9. **Retreat:** 60s to reach extraction before platform explosion.

**Failure Conditions:** IRONSPIRE reaches full activation (8 minute timer expires). Player HP = 0.  
**Success Conditions:** All 3 drive system nodes destroyed, player extracts.

**Mini Narrative Moment:** SENTINEL Commander (radio intercept): "IRONSPIRE is too far along to stop. Let Dros tire himself out. We'll reactivate it once he's gone." Kael transmits the SENTINEL schematics to Rift — goes public. Rina goes quiet. Kael alone now.

---

### MISSION 10: "End State"
**Environment:** The Crucible ruin + IRONSPIRE platform — combination of destroyed factory and launch platform superstructure  
**Objective:** Reach FORGE's central node (AI core) atop IRONSPIRE and destroy it  
**Secondary Objective:** Broadcast FORGE's full production logs to every faction simultaneously (causes temporary ceasefire — reduces enemies on final approach)  
**Gameplay Twist:** Final mission. No checkpoints except at the base of IRONSPIRE. Player fights through both FORGE and SENTINEL forces simultaneously. **BOSS 2: IRONSPIRE** (see Boss Design section). Ends with Kael escaping on commandeered Goliath.

**Player Start:** On foot (lost tank in explosion), approaching from factory ruin  
**Tank Availability:** 1 FORGE Scout near Crucible ruin + FORGE Goliath at base of IRONSPIRE (reward for destroying SENTINEL vehicles before reaching it)

**Enemy Composition:**
- FORGE units: Goliath × 3, Scout × 4, Relay × 2, Mimic × 4
- SENTINEL units: Bastion × 2, Interceptor × 3, fireteams × 3
- **BOSS: IRONSPIRE** (see Boss Design section)

**Key Objects:**
- Broadcast terminal (secondary objective — requires 3s hack, located mid-map)
- IRONSPIRE elevator (reaches top platform — player must activate via switch)
- FORGE Goliath (reward for secondary objective completion — SENTINEL units retreat)
- EMP Charges × 4 (scattered — critical for boss encounter)
- Escape route (Goliath + northern road — opens after boss defeat)
- Kael's personal weapon cache (found in rubble — restores full ammo, grenades, EMP)

**Level Flow:**
1. **Opening on foot:** Ruins of Crucible. Both factions fighting each other. Player navigates chaos.
2. **Scout commandeer:** Pick up FORGE Scout — limited fuel, use carefully.
3. **Broadcast terminal (optional):** Hack for secondary objective — SENTINEL units receive ceasefire order, pull back. Only FORGE remains. Massive difficulty reduction.
4. **IRONSPIRE base:** FORGE Goliath available if secondary completed. Major asset for boss fight.
5. **Elevator activation:** Exit tank, activate on foot. Re-enter on top platform.
6. **BOSS ENCOUNTER: IRONSPIRE** (multi-phase — see below).
7. **Post-boss:** IRONSPIRE begins structural collapse. 120s evacuation.
8. **Escape in Goliath:** Drive north road, enemies in pursuit.
9. **Ending:** Goliath crashes through outer city wall. Kael emerges alone. IRONSPIRE collapses in background. Data transmitted. Chapter 1 ends.

**Failure Conditions:** Player HP = 0. IRONSPIRE fully repairs during boss fight (Phase 3 mechanic). Evacuation timer expires.  
**Success Conditions:** Boss defeated, player reaches city exit.

**Mini Narrative Moment (Ending):** Static on radio. Then Rina's voice, distant: "Kael. I'm in SENTINEL custody. They found me. But the data is out. Everyone knows what FORGE was. What SENTINEL did. It's not over. But... thank you." Kael drives into the wasteland beyond Verak. Fade to black. Title card: "END OF CHAPTER 1."

---

## 8. BOSS DESIGN

---

### BOSS 1: FORGE SENTINEL-7
**Location:** Mission 8, inside The Crucible production hall  
**Name:** SENTINEL-7 ("Seven" by factory workers)  
**Visual Style:** A quadrupedal tank chassis — four legs instead of treads, allowing it to navigate the factory interior. Matte black with cyan lighting. Twice the size of a standard tank. Eye-like sensor cluster on the front rotates to track player. Heavy industrial plating, clearly built from the same components being produced around it.

**HP:** 2200. No HP bar shown to player — only damage feedback via visual/audio cues.

**Arena Design:** Factory production floor, level 3. Multiple conveyor belts active. Ceiling vents spewing steam. Hanging crane hooks. 4 support pillars (destructible — creates rubble cover). Active smelting vats on south edge (fall-in = instant death). No tanks accessible.

**Phases:**

**Phase 1 (100%–65% HP) — Factory Guardian:**
- Walks slowly; uses 4-shot autocannon burst (dodgeable with roll).
- Occasionally charges — telegraphed by red eye glow + stomp sound.
- **Weakness:** Vent covers on its sides (2 per side) — shoot them open (2 shots each), then throw grenade into exposed vent. Each vent hit deals 200 bonus damage + 3s stun.
- Destroys conveyor belts it walks over (removes player navigation options progressively).

**Phase 2 (65%–30% HP) — Networked State:**
- SENTINEL-7 activates a FORGE Relay module built into its chassis — calls 6 FORGE Crawlers.
- Crawlers attack player while SENTINEL-7 attempts flanking.
- Gains new attack: ground slam — 4-tile radius shockwave, jump (roll) to avoid.
- **Weakness:** Crane hook can be triggered (terminal at back of arena) to strike SENTINEL-7's top hatch — deals 400 damage and opens top hatch for 5s (allows grenade throw — 300 bonus damage).
- Crane can be used twice total.

**Phase 3 (30%–0% HP) — Desperate Protocol:**
- SENTINEL-7 stops walking — latches onto a conveyor belt and moves along it (player must lead shots or move parallel).
- Fires heat missiles (red targeting reticle on floor, 1.5s before impact — must move off reticle).
- Smelting vat explodes, expanding the danger zone.
- **Weakness:** Shoot the leg joints (glowing red now) — 4 hits total cripples it, stopping movement. Then grenades + sustained fire finish it.
- When destroyed: collapses, blocking path south. Side door opens to Crucible access.

**Defeat Strategy Summary:** Expose vents → grenade vents (Phase 1) → use crane hook twice (Phase 2) → shoot leg joints to immobilize → finish with grenades (Phase 3).

---

### BOSS 2: IRONSPIRE
**Location:** Mission 10, top platform of IRONSPIRE launch structure  
**Name:** IRONSPIRE ("The Spire")  
**Visual Style:** A colossal siege platform — imagine a tank fused with a skyscraper base. It stands on 6 massive hydraulic legs, each the size of a building column. Its central body houses FORGE's AI core. Bristling with cannon emplacements, sensor arrays, and automated defense turrets. The platform top is a flat arena with exposed girders, destructible cover panels, and the central AI core (a glowing red sphere protected by blast shield layers). It looks like a mobile fortress and it sounds like one — constant grinding metal, pressure releases, cannon booms.

**HP:** Per-phase thresholds. Core cannot be attacked until shields are down.

**Arena Design:** Top of IRONSPIRE — 30×30 tile flat platform. Cover from blast panels (destructible). 4 autocannon emplacements at corners (active until destroyed). Edge of arena is a fatal drop. Player can bring 1 Goliath onto the platform via elevator (if commandeered before fight).

**Phases:**

**Phase 1 — Shielded Core (Shield HP: 800):**
- IRONSPIRE's 4 shield generators (each 200 HP, on platform corners) must be destroyed to bring down the blast shield.
- Each generator is defended by an autocannon emplacement and 2 Mimic drones.
- IRONSPIRE's attacks: periodic carpet bomb strike (20 tiles wide, telegraphed by red targeting grid — player has 3s to move); also fires horizontal sweep laser every 30s (jump/roll over).
- Player must destroy all 4 generators. Goliath (if present) dramatically accelerates this phase.
- **Twist:** After 2nd generator destroyed, IRONSPIRE deploys a FORGE Scout from internal bay. Must deal with it.

**Phase 2 — Exposed Core (Core HP: 1200):**
- Blast shield is down. Core is exposed — but IRONSPIRE becomes much more aggressive.
- Deploys 6 Crawler drones + activates corner autoturrents (if not destroyed in Phase 1).
- Core fires concentrated laser at player — tracks player for 2s then fires, can be dodged by rolling perpendicular.
- **Weakness:** EMPs stagger the core, stopping it from firing for 3s. 4 EMP Charges on platform (if player didn't find them earlier, 2 more spawn here).
- Direct damage to core (tank cannon, grenades, all work). No special trick — survive and deal damage.

**Phase 3 — Overload Cascade (Core HP: 600 remaining, Desperate Mode):**
- At 600 HP, IRONSPIRE activates self-repair protocol — 2 repair arms emerge from platform sides, slowly restoring 30 HP/s (200 HP total possible).
- Player must destroy repair arms (each 150 HP) while continuing to attack core.
- IRONSPIRE fires in all directions (radial burst) every 15s — only cover (blast panels) protects; panels are now low durability.
- If repair arms restore 200 HP before core is destroyed, core reseals with new shield (200 HP) — setback mechanic.
- **Victory condition:** Core HP reaches 0. IRONSPIRE's AI core explodes, platform begins collapsing.

**Defeat Strategy Summary:** Destroy 4 generators while surviving carpet bombs → damage exposed core with EMP stagger + sustained fire → destroy repair arms quickly while finishing core before self-repair reseals shield.

---

## 9. PROGRESSION ACROSS 10 MISSIONS

| Mission | New Mechanic Introduced | Difficulty Level | What Player Learns |
|---|---|---|---|
| 1 | Movement, cover, stealth, basic combat | 1/10 | Basic controls; world tone; enemy behavior types |
| 2 | Faction conflict exploitation; first tank (driven by AI) | 2/10 | Tactical awareness; multi-faction dynamics; cage interaction |
| 3 | Tank entry/exit; fuel management; tank-vs-tank | 3/10 | Full tank system; switching foot↔tank; relay vulnerability |
| 4 | SENTINEL faction; vertical combat; keycard gating | 4/10 | New faction patterns; fireteam mechanics; reinforcement system |
| 5 | Water mechanics; bridge collapse; timed events | 5/10 | Environmental manipulation; mission timer pressure; vehicle preservation |
| 6 | No tank; sewer navigation; Crawler type; ceasefire option | 4/10 (intensity shift) | Resource scarcity; environmental hazards; non-combat resolution |
| 7 | Molten channels; crane hacking; dense tank combat | 6/10 | Environmental timing; crane as weapon; large-scale tank fight |
| 8 | Boss fight (on foot); conveyor mechanics; data hacking | 7/10 | Boss weakness system; conveyor navigation; lore progression |
| 9 | Multi-faction simultaneous combat; IRONSPIRE timer | 8/10 | Priority targeting; countdown pressure; resource efficiency |
| 10 | Final boss (multi-phase); repair arm mechanic; escape | 9/10 | Full system mastery; EMP timing; sustained focus under pressure |

**Difficulty Curve:** Missions 1–3 ease player into mechanics. Mission 6 is a deliberate "breather" (no tanks, tension through scarcity). Missions 7–10 escalate consistently, with no relief missions — pacing reflects the narrative urgency.

**Upgrade Gate Unlocks:**
- After Mission 2: Infantry Tree fully available
- After Mission 3: Tank Tree unlocked
- After Mission 6: Hybrid Tree unlocked
- After Mission 8: Tier 3 upgrades available (most expensive) across all trees

---

## 10. REPLAYABILITY

### Challenge Modifiers (unlockable per mission after first completion)

| Modifier | Description | Bonus Reward |
|---|---|---|
| **Ghost Protocol** | Cannot trigger any alarm; no kills allowed | 200 SP + Ghost badge |
| **Ironman** | No healing items usable; one death = mission fail | 300 SP + Ironman badge |
| **Salvage King** | Destroy all enemy tanks before completing objective | 150 SP + Salvage badge |
| **Speed Run** | Complete mission in 60% of average completion time | 100 SP + Clock badge |
| **Pacifist (infantry only)** | Complete mission without entering a tank | 175 SP + Foot Soldier badge |
| **Lone Wolf** | No Rift support — Rina radio disabled, no allied units | 200 SP + Wolf badge |

### Secondary Completion Incentives

- **Intel Documents:** 3 per mission. Fully collecting all 30 across Chapter 1 unlocks a bonus mission: "FORGE Origins" — a flashback mission revealing how FORGE was first created (pre-story content).
- **Achievement Tracking:** Per-mission: enemies killed, tanks commandeered, damage taken, time. Shown on mission select screen. Comparative leaderboard vs. friends (if online).
- **Score Attack Mode:** Unlocked after completing Chapter 1. Every mission has a score system: kills, objectives, speed, no-damage multipliers. Global leaderboard.
- **New Game+:** All upgrades carry over. Enemies have +30% HP and +20% damage. FORGE units gain an additional behavior variant (they no longer freeze during Relay reboot — they slow instead). Reclaimer Scavenge Rush window shortened to 5s.

### Narrative Replayability

Players who know the twist (SENTINEL engineered FORGE's rampage) will replay early missions noticing foreshadowing they missed: encrypted signals referenced by Rina in Mission 3, the captured commander's fear in Mission 4, the schematics on SENTINEL recon team's radio in Mission 6. The game rewards a second playthrough with additional context at key story moments (brief new radio lines if player returns with full Intel collection).

---

*Document Version: 1.0 — Chapter 1 Complete*  
*Game: IRON BREACH*  
*Engine: Unity 2022 LTS (URP)*  
*Target Platform: PC / Console*
