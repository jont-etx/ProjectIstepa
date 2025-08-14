================= Overview/10. Overview.md =================

```
Dungeon Realm Builder Game Design Document - Overview

Overview
Dungeon Realm Builder is a voxel/isometric-based multiplayer dungeon creator game blending kingdom management, resource gathering, hero-led exploration, and user-generated content. Players control a kingdom, expanding it by gathering resources from dungeons they explore with hired heroes or create for others to challenge. The game emphasizes creativity in dungeon design (monsters, puzzles, traps) and strategic kingdom growth through buildings, services, and multiplayer interactions like hiring or trading.

Core Loop: Explore dungeons for resources → Build/upgrade kingdom buildings to unlock assets → Create dungeons for others → Earn rewards from player challenges → Repeat to gain prestige and rank up.

The game supports up to 100+ players per server shard, with cross-server dungeon sharing. It's free-to-play, with all content earnable through gameplay, achievements, and events. Optional cosmetics (themes for kingdoms, dungeons, heroes, buildings) are purchasable. Progression focuses on kingdom ranks (1-10), unlocking advanced assets, larger maps, and faction-specific features. No pay-to-win elements; cosmetics are purely visual.

Key Features:
- Voxel/isometric view for intuitive building and exploration.
- Multiplayer economy: Hire heroes/services from other players, trade resources, share dungeons.
- Faction system with strengths, weaknesses, and nemeses for strategic depth.
- Procedural and player-created dungeons with puzzles, monsters, and feats.
- Kingdom building on a 128x128 tile map with free placement.
- Upgradable buildings (5 tiers) unlocking new services, hero types, and buffs.
- 10 dungeon difficulty levels with scalable sizes (32x32 min, increments of 16 tiles).
- Multiple currencies/resources for diverse building/economy.
- Cross-platform compatibility: Seamless play across PC, mobile, web, and potential consoles.

Target Audience: Fans of Minecraft, Roblox, Dungeon Keeper, and The Legend of Zelda (for puzzles), aged 12+, seeking creative, social, and strategic gameplay. Sessions last 30-60 minutes, with persistent kingdoms for long-term progression.
```

================= Overview/20. Core Gameplay.md =================

```
Core Gameplay
Players manage a kingdom while creating and exploring dungeons in a persistent multiplayer world. The gameplay loop integrates resource gathering, building, creation, and social interactions for a balanced experience.

Core Mechanics:
1. Kingdom Management: Build and upgrade structures (5 tiers) on a 128x128 tile map using resources. Buildings generate passive income, attract heroes, offer hireable services (e.g., blacksmith for gear upgrades), and unlock advanced features at higher tiers.
2. Hero Exploration: Hire heroes from your tavern or other players. Lead squads (up to 4 heroes) through dungeons to gather resources, defeat monsters, solve puzzles, and complete feats for rewards.
3. Dungeon Creation: Design custom dungeons using unlocked assets (monsters, traps, tilesets). Place elements strategically; a point system auto-calculates difficulty and rewards. Share for others to play, earning resources based on completions.
4. Multiplayer Interactions: Trade resources, hire heroes/services, collaborate on dungeons, or compete via leaderboards (e.g., most challenging dungeon).
5. Progression: Earn prestige from dungeon completions/creations to rank up your kingdom (1-10). Higher ranks unlock assets, larger dungeon sizes, and advanced building upgrades.
6. Combat and Puzzles: Isometric real-time combat with hero abilities (faction-specific). Puzzles include lever systems, rune matching, or environmental challenges.

Win Conditions (Per Session/Season):
- Prestige Leader: Highest kingdom prestige at season end (e.g., 3 months real-time).
- Dungeon Master: Most player completions/rewards from created dungeons.
- Explorer Elite: Most resources gathered from explorations.
- Cooperative Victory: Alliances achieve shared goals (e.g., collective prestige milestones for server-wide rewards).

Strategic Considerations:
- Early Game: Focus on basic resources (Wood, Stone) and low-level dungeons; upgrade Tavern/Blacksmith to Tier 2 for early boosts.
- Mid Game: Build specialized buildings (e.g., Library for puzzle assets); upgrade to Tier 3 for multiplayer services; explore nemesis dungeons for high-risk/high-reward.
- Late Game: Create massive dungeons (up to 256x256+); upgrade buildings to Tier 5 for epic unlocks; trade for rare resources like Mythril.
Balance Notes: Resource scarcity encourages trading. Dungeon difficulty scales to prevent exploits (e.g., over-trapping inflates points but risks low completions). Building upgrades are platform-agnostic with unified UI for cross-platform play.
```

================= Overview/20.1 Factions.md =================

```
Factions
Nine factions provide unique playstyles, strengths, weaknesses, and nemeses. Each has a thematic tileset for dungeons/kingdoms (e.g., overgrown vines for Nature). Choosing a faction locks core assets but allows cross-faction hires. Free players start with 1 of 3 random factions; unlock others via achievements (e.g., complete 50 dungeons). Nemesis matchups increase difficulty (e.g., +20% enemy health) but boost rewards (e.g., +30% rare drops).

Faction Details:

| Faction | Strength | Weakness | Nemesis | Tileset Theme | Strategy |
|---------|----------|----------|---------|---------------|----------|
| Ogres | High health/damage in melee; bonus to trap durability. | Slow movement; vulnerable to magic. | Nature | Rocky, brutish caves with boulders. | Tanky dungeon defense; overwhelm with monsters. |
| Trolls | Regeneration; excel in dark/swamp terrains. | Weak to fire/light puzzles. | Mythical | Misty swamps with regenerative flora. | Sustained fights; puzzles involving healing mechanics. |
| Goblins | High speed/agility; bonus traps and ambushes. | Low health; poor against armored foes. | Dwarves | Cluttered tunnels with gadgets/explosives. | Hit-and-run tactics; puzzle-heavy with tricks. |
| Humans | Versatile; bonus to resource gathering/trading. | No extremes; average stats. | Undead | Medieval castles/towns with banners. | Balanced exploration; service-focused kingdoms. |
| Elves | Magic/ranged prowess; enhanced puzzle-solving. | Fragile in close combat. | Trolls | Enchanted forests with glowing runes. | Spell-based combat; intricate rune puzzles. |
| Dwarves | Defense/engineering; bonus to building durability. | Slow; weak to aerial threats. | Ogres | Underground forges with mechanical traps. | Fortified dungeons; gear-crafting focus. |
| Undead | Summoning/hordes; immune to poison/fear. | Vulnerable to holy/light. | Elves | Necrotic graveyards with skeletal decor. | Swarm tactics; horror-themed feats. |
| Mythical | Flight/illusions; high evasion. | Low physical defense. | Dwarves | Ethereal realms with floating islands/mirrors. | Deceptive puzzles; aerial combat. |
| Nature | Summon animals/plants; terrain manipulation. | Weak to fire/industrial traps. | Humans | Overgrown jungles with vines/animals. | Environmental control; adaptive dungeons. |

Balance Notes: Strengths/weaknesses are quantified (e.g., +15% stat bonuses). Nemeses encourage diverse hero squads. Faction unlocks promote replayability without gating core fun.
```

================= Overview/20.2 Maps and World Generation.md =================

```
Maps and World Generation
The game features persistent player kingdoms and shareable dungeons in a voxel/isometric view for precise placement and navigation.

Kingdom Maps:
- Size: 128x128 tiles (voxels for 3D building, isometric projection).
- Generation: Procedural base terrain (e.g., hills, rivers) customized by faction (e.g., forests for Elves). Free placement for buildings; no grid restrictions beyond boundaries.
- Expansion: Unlock border extensions via prestige (e.g., +16 tiles at Rank 5).

Dungeon Maps:
- Levels: 10 difficulty/reward tiers.
- Base Size: Starts at 32x32 (Level 1); max increases by 16x16 per level (e.g., Level 10: 32 + 9*16 = 176x176 base max).
- Customization: Creators set any size >=32x32 in 16-tile increments (e.g., 48x1024 for linear adventures, 256x256 for sprawling mazes). Bonuses (e.g., achievements) add extra size.
- Generation: Procedural seeds for inspiration, but fully editable. Faction tilesets auto-apply (e.g., Goblin gadgets).

Strategic Considerations: Larger dungeons yield more rewards but require more resources to build. Kingdom maps encourage efficient layouts (e.g., central tavern for hero access). Cross-platform optimization ensures consistent rendering (e.g., scalable voxel density for mobile).
```

================= Overview/20.3 Kingdom Progression and Ranks.md =================

```
Kingdom Progression and Ranks
Kingdoms progress through 10 ranks, unlocked by prestige (earned from dungeon explorations, creations, and services). Higher ranks grant access to advanced assets, larger maps, and building upgrades.

Progression Mechanics:
- Prestige Sources: Dungeon completions (+10-100 based on difficulty), creations (+5 per player completion), services hired (+2 per transaction), building upgrades (+20 per tier upgrade).
- Rank Requirements: Cumulative prestige (e.g., Rank 1: 0, Rank 2: 500, Rank 10: 50,000).
- Unlocks: Per rank, gain new assets (e.g., Rank 3: Basic puzzles; Rank 7: Epic monsters), dungeon size bonuses (+16x16 max), and building upgrade tiers (e.g., Tier 3 at Rank 4).

Strategic Considerations:
- Early Ranks (1-3): Basic buildings/resources; upgrade Tavern/Market to Tier 2 for early income.
- Mid Ranks (4-6): Specialized assets and building upgrades (Tier 3-4); emphasize multiplayer hires.
- Late Ranks (7-10): Complex feats and Tier 5 buildings; optimize for high-reward dungeons.
Balance Notes: Prestige grind is mitigated by events (double prestige weekends) and achievements (e.g., "First Dungeon Creator: +500 prestige"). Building upgrades require rank gates to pace progression. Cross-platform syncing ensures progress carries over devices.
```

================= Overview/20.4 Dungeons and Creation.md =================

```
Dungeons and Creation
Dungeons are player-created challenges with monsters, puzzles, and feats. Creators place assets; explorers navigate with heroes.

Creation Mechanics:
- Editor: Voxel-based tools for terrain, asset placement. Point system: Assets have costs/points (e.g., Goblin Minion: 10 points/cost 50 Iron). Total points set difficulty (1-10) and rewards (random with % chances, e.g., 20% Gem drop at Level 5+).
- Elements: Monsters (faction-themed, AI behaviors), Traps (spikes, illusions), Puzzles (levers, riddles), Feats (boss fights, time trials).
- Sharing: Upload to server; rated by players for visibility/leaderboards.

Exploration Mechanics:
- Squad Control: Isometric real-time; command heroes (auto-pathing, abilities).
- Rewards: Scaled by difficulty/nemesis (e.g., +50% vs. nemesis). Random rolls with modifiers (e.g., higher rank heroes boost %).

Strategic Considerations: Over-design risks low completions (fewer earnings); balanced dungeons attract repeat plays. Editor tools are unified across platforms for consistent creation.
```

================= Overview/20.4.1 Resources and Currencies.md =================

```
Resources and Currencies
11 resources drive building, creation, and trading. Gathered from dungeons, services, or trades.

| Resource | Sources | Uses | Rarity |
|----------|---------|------|--------|
| Iron | Basic dungeons/mining feats. | Weapons/traps. | Common |
| Wood | Nature-themed dungeons. | Buildings/structures. | Common |
| Stone | Dwarf/Ogre dungeons. | Walls/foundations. | Common |
| Copper | Mid-level trades. | Wiring/puzzles. | Uncommon |
| Gold | High completions. | Currency for hires. | Uncommon |
| Crystals | Magic puzzles. | Enchantments. | Rare |
| Gems | Nemesis rewards. | Upgrades/cosmetics. | Rare |
| Mythril | Late dungeons. | Epic gear. | Very Rare |
| Artifacts | Boss feats. | Unique buffs. | Very Rare |
| Runes | Elf/Undead puzzles. | Spell assets. | Rare |
| Manuscripts | Library services. | Blueprints/unlocks. | Uncommon |

Mechanics: Storage limits scale with banks; trading via markets. Events boost yields (e.g., "Resource Rush"). Building upgrades consume scaled resources (e.g., Tavern Tier 5: 1000 Wood, 50 Mythril).
Balance: Commons for basics; rares for endgame to encourage multiplayer.
```

================= Overview/20.5 Buildings.md =================

```
Buildings
Players build 9 core structures (faction-renamed/themed, e.g., Ogre "Grog Hall" for Tavern). Placed freely on a 128x128 kingdom map, each building has 5 upgrade tiers unlocking new features, services, or buffs. Upgrades require resources, kingdom rank, and prestige rewards (+20 per tier). Higher tiers enhance passive income, hero attraction, and multiplayer services.

Building Details and Upgrade Tiers:

| Building | Function | Unlocks At | Upgrade Costs (Tiers 1-5) | Upgrade Unlocks |
|----------|----------|------------|---------------------------|-----------------|
| Tavern | Hire heroes; attract visitors. | Rank 1 | T1: 200 Wood, 100 Stone<br>T2: 300 Wood, 150 Stone, 50 Iron<br>T3: 500 Wood, 200 Stone, 100 Copper<br>T4: 800 Wood, 300 Stone, 50 Gold<br>T5: 1000 Wood, 400 Stone, 50 Mythril | T1: Basic heroes (Common)<br>T2: Uncommon heroes; +1/hour prestige<br>T3: Hireable by others; +10% hero XP<br>T4: Rare heroes; +2/hour prestige<br>T5: Epic heroes; +20% hire income |
| Jeweler | Craft gems; sell cosmetics. | Rank 2 | T1: 150 Copper, 50 Gems<br>T2: 200 Copper, 100 Gems, 20 Crystals<br>T3: 300 Copper, 150 Gems, 50 Crystals<br>T4: 500 Copper, 200 Gems, 20 Runes<br>T5: 700 Copper, 300 Gems, 50 Mythril | T1: Basic cosmetics<br>T2: +10% Gem drop rate<br>T3: Sell to players; +1/hour prestige<br>T4: Rare cosmetics; +10% craft speed<br>T5: Epic cosmetics; +2/hour prestige |
| Library | Research manuscripts; unlock puzzles. | Rank 3 | T1: 300 Stone, 20 Runes<br>T2: 400 Stone, 50 Runes, 50 Copper<br>T3: 600 Stone, 100 Runes, 20 Crystals<br>T4: 800 Stone, 150 Runes, 50 Gold<br>T5: 1000 Stone, 200 Runes, 50 Artifacts | T1: Basic puzzles<br>T2: +10% puzzle solve speed<br>T3: Shareable puzzle blueprints<br>T4: Advanced puzzles; +1/hour prestige<br>T5: Epic puzzles; +20% Manuscript yield |
| Blacksmith | Forge gear; hero upgrades. | Rank 2 | T1: 250 Iron, 100 Copper<br>T2: 400 Iron, 150 Copper, 50 Stone<br>T3: 600 Iron, 200 Copper, 20 Gold<br>T4: 800 Iron, 300 Copper, 50 Crystals<br>T5: 1000 Iron, 400 Copper, 50 Mythril | T1: Basic gear<br>T2: +10% gear durability<br>T3: Hireable forging; +1/hour prestige<br>T4: Rare gear; +10% forge speed<br>T5: Epic gear; +2/hour prestige |
| Market | Trade resources; hire services. | Rank 1 | T1: 150 Wood, 50 Gold<br>T2: 250 Wood, 100 Gold, 50 Copper<br>T3: 400 Wood, 150 Gold, 20 Crystals<br>T4: 600 Wood, 200 Gold, 50 Runes<br>T5: 800 Wood, 300 Gold, 50 Mythril | T1: Basic trading<br>T2: +10% trade profit<br>T3: Global market access; +1/hour prestige<br>T4: Rare resource trades; +10% trade speed<br>T5: +20% trade profit; +2/hour prestige |
| Bank | Store resources; interest on gold. | Rank 4 | T1: 400 Stone, 200 Gold<br>T2: 600 Stone, 300 Gold, 50 Copper<br>T3: 800 Stone, 400 Gold, 20 Crystals<br>T4: 1000 Stone, 500 Gold, 50 Runes<br>T5: 1200 Stone, 600 Gold, 50 Artifacts | T1: +1000 storage<br>T2: +5% gold interest<br>T3: +2000 storage; +1/hour prestige<br>T4: +10% interest; +3000 storage<br>T5: +20% interest; +5000 storage |
| Magicians School | Train magic heroes; rune crafting. | Rank 3 | T1: 200 Crystals, 30 Runes<br>T2: 300 Crystals, 50 Runes, 50 Copper<br>T3: 400 Crystals, 100 Runes, 20 Gold<br>T4: 600 Crystals, 150 Runes, 50 Mythril<br>T5: 800 Crystals, 200 Runes, 50 Artifacts | T1: Basic magic heroes<br>T2: +10% rune craft speed<br>T3: Hireable training; +1/hour prestige<br>T4: Rare magic heroes; +10% spell power<br>T5: Epic magic heroes; +2/hour prestige |
| Archeologist | Excavate artifacts; dungeon blueprints. | Rank 5 | T1: 300 Iron, 50 Artifacts<br>T2: 400 Iron, 100 Artifacts, 50 Stone<br>T3: 600 Iron, 150 Artifacts, 20 Gold<br>T4: 800 Iron, 200 Artifacts, 50 Crystals<br>T5: 1000 Iron, 300 Artifacts, 50 Mythril | T1: Basic blueprints<br>T2: +10% artifact drop rate<br>T3: Shareable blueprints; +1/hour prestige<br>T4: Epic blueprints; +10% excavation speed<br>T5: Legendary blueprints; +2/hour prestige |
| Carpenter | Build advanced structures; wood efficiency. | Rank 2 | T1: 400 Wood, 100 Stone<br>T2: 600 Wood, 150 Stone, 50 Iron<br>T3: 800 Wood, 200 Stone, 20 Gold<br>T4: 1000 Wood, 300 Stone, 50 Copper<br>T5: 1200 Wood, 400 Stone, 50 Mythril | T1: Basic structures<br>T2: +10% wood efficiency<br>T3: Hireable crafting; +1/hour prestige<br>T4: Advanced structures; +10% build speed<br>T5: Epic structures; +2/hour prestige |

Strategic Considerations:
- Early Game: Upgrade Tavern/Market to Tier 2 for hero hiring and trading boosts.
- Mid Game: Focus on Library/Blacksmith (Tier 3-4) for puzzle/gear advantages; enables multiplayer services.
- Late Game: Max out Bank/Magicians School (Tier 5) for storage and epic heroes.
Balance Notes: Upgrade costs scale to prevent early rushes. Faction-themed visuals (e.g., Undead Library as a crypt) support cosmetic purchases. Cross-platform UI ensures intuitive upgrade interactions.
```

================= Overview/20.6 Heroes and Exploration.md =================

```
Heroes and Exploration
Heroes are hireable units for dungeon runs, with faction ties, levels, and abilities.

Mechanics:
- Hiring: From tavern (NPCs) or players (multiplayer). Cost: Gold/resources; higher Tavern tiers unlock better heroes.
- Stats: Health, Damage, Speed, Magic (faction bonuses). Level up via explorations.
- Squads: Mix factions for nemesis coverage (e.g., Elf mage vs. Trolls).
- Exploration: Real-time isometric; pause for commands. Failures lose resources but grant partial rewards.

Strategic: Hire specialists (e.g., Dwarf for traps). Prestige and Tavern upgrades attract better heroes (e.g., Rank 5/Tier 5: Epic-tier). Balance: Hero permadeath risk in high-difficulty (revivable with artifacts). Input schemes adapt to platform (e.g., touch gestures on mobile).
```

================= Overview/30. Multiplayer and Economy.md =================

```
Multiplayer and Economy
Persistent servers with shard-based worlds. Interactions: Trade chats, alliances, dungeon queues.

Economy: Player-driven; markets set prices. Services: Hire blacksmiths, magicians, etc., from upgraded buildings (fee to owner). Events: Server-wide dungeon challenges for bonuses.

Balance: Anti-griefing via ratings/reports. Cross-server dungeons via global library. Cross-platform matchmaking ensures seamless play.
```

================= Overview/40. Monetization and Accessibility.md =================

```
Monetization and Accessibility
Free-to-play: All content earnable (e.g., faction unlocks via 100+ hours/achievements). Events accelerate progress.

Monetization: Cosmetics only (e.g., $5 neon tileset, hero skins, building upgrade visuals like glowing Dwarven forges). No loot boxes; direct purchases.

Accessibility: Tutorials, adjustable difficulty, color-blind modes. Cross-platform support includes PC (Windows/Mac/Linux), Mobile (iOS/Android), Web (WebGL), with potential console ports (Xbox, PlayStation, Switch). Unified controls (keyboard/mouse, touch, controller) and cloud saves for device switching. Building upgrade UI is responsive for all platforms.
```

================= Overview/50. Tech Stack.md =================

```
Tech Stack
Unity is the core engine for cross-platform compatibility, supporting voxel/isometric rendering and multiplayer features.

Key Components:
- Engine: Unity 2025 LTS for stable voxel/isometric rendering. Tilemap system for isometric views; Voxel plugins for 3D elements.
- Platforms Supported:
  - PC: Windows, Mac, Linux (standalone builds).
  - Mobile: iOS, Android (optimized for touch input, lower voxel resolution).
  - Web: WebGL for browser play (progressive web app support).
  - Consoles: Potential ports to Xbox, PlayStation, Nintendo Switch.
- Networking: Photon Networking or Unity Netcode for real-time multiplayer, dungeon sharing, and cross-platform syncing.
- Backend: Firebase or AWS for persistent data (kingdoms, dungeons, building upgrades). Cloud saves for cross-device progression.
- Frontend/UI: Unity UI Toolkit for responsive interfaces, including building upgrade menus. Isometric camera with unified controls.
- Asset Management: Addressables for efficient loading of voxel assets and building upgrade visuals.

Development Considerations:
- Build Pipeline: Unity Cloud Build for automated cross-platform testing.
- Optimization: Platform-specific profiles (e.g., reduce building effects on mobile).
- Testing: Prototype building upgrades for PC/mobile parity.
Balance Notes: Cross-platform ensures fair multiplayer; no platform-exclusive features.
```

================= Overview/60. Future Expansions (Placeholder) =================

```
Future Expansions
- New Factions (e.g., Aquatic).
- PvP Dungeons.
- VR Mode.
- Seasonal Events.
- Expanded Console Support.
```