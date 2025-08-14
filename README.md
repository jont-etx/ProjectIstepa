Trade Empire Game Design Document

Overview

A real-time strategy (RTS) and massively multiplayer online (MMO) trade and transport game where players build a trade empire starting from a chosen location on a dynamic world map. Players manage resources, trade with others, and develop transportation networks across land, air, and water through 10 technological ages. The game supports 16 to 128 players per session, with AI-controlled entities to fill gaps if needed.

Core Mechanics

1. World Setup





Map: Procedurally generated with random resource distribution (e.g., minerals, timber, food, rare materials). Maps vary in size based on player count (16–128 players).



Starting Location: Players choose a starting point on the map for their home base. A buffer zone prevents other players from claiming land too close for the first 2 in-game days (e.g., 48 hours real-time or accelerated game time).



Starting Resources: Players begin with a fixed amount of in-game currency (e.g., $10,000) to purchase initial land and basic infrastructure.

2. Resources and Trade





Resources: Categorized into raw materials (e.g., ore, wood, crops) and processed goods (e.g., steel, furniture, packaged food). Each map region has unique resource availability, encouraging trade.



Trade System:





Players trade with other players or AI-controlled NPC cities.



Goods include:





People: Workers, specialists, or passengers with varying transport needs.



Mail: Low-weight, high-priority cargo.



Goods: Industrial products, luxury items, or raw materials.



Food: Perishable, high-demand for population growth.



Animals: Livestock or exotic creatures for trade or production.



Demand varies by home base or NPC city based on their economy, population, and development level.



Import/Export: Players must import scarce resources from other regions or players, creating interdependency.



Home Base Growth:





The home base serves as the player's central hub with the highest trade influence and return on investment (ROI).



Growth is driven by investing in trade connections and importing resources (e.g., food for population, materials for infrastructure).



Players do not directly build the home base but invest currency and resources to upgrade its economy, population, and trade capacity.

3. Transportation





Transport Modes:





Land: Roads, railways, or pipelines.



Water: Rivers, canals, or ocean routes.



Air: Airports and airships (unlocked in later ages).



Ages:





10 technological ages, each unlocking advanced transport options.



Age 1: Crude land (e.g., carts, pack animals) and water (e.g., rafts, small boats) transport.



Age 10: Advanced land (e.g., high-speed trains, autonomous trucks), water (e.g., mega-freighters), and air (e.g., cargo planes, drones).



Progression through ages is time-based, with each age lasting a fixed duration (e.g., 12 hours real-time or 1 in-game week).



Specific technologies are locked to each age and can only be researched during that age.



Transport Units:





Vary by age and mode (e.g., ox carts in Age 1, steamships in Age 4, jets in Age 10).



Each unit has capacity, speed, and maintenance costs.

4. Factions





Number: 7 factions, each with a unique bonus to balance gameplay.



Faction Bonuses (tentative):





Land Masters: 10% reduced cost and 15% faster construction for land-based transport (roads, railways).



Sea Traders: 10% increased cargo capacity and 15% faster water transport.



Sky Pioneers: 10% reduced cost for air transport and 20% faster air research.



Land-Water Synergy: 5% efficiency bonus when combining land and water transport routes.



Air-Water Innovators: 5% reduced maintenance for air and water units and 10% faster joint research.



Resource Haulers: 10% increased capacity for raw material transport across all modes.



Logistics Experts: 10% reduced transport time for high-priority goods (e.g., mail, passengers).



Balance: Bonuses are designed to be equivalent in impact, with no faction inherently stronger.

5. Gameplay Loop





Build: Purchase land, construct transport infrastructure (e.g., roads, docks, airports), and establish production facilities.



Trade: Negotiate deals with players or NPCs to import/export goods based on supply and demand.



Transport: Manage routes and fleets to deliver goods efficiently, balancing speed, cost, and capacity.



Invest: Allocate resources and currency to grow the home base’s economy, population, and trade influence.



Research: Unlock age-specific technologies to enhance capabilities.



Win Conditions:





Trade Dominance: Achieve 80% of the map’s total trade influence (measured by trade volume, routes controlled, and home base economic power).



Hostile Takeover: Purchase controlling shares of in-debt players’ trade empires, absorbing their assets and influence.



Last Standing: Be among the last 5% of players remaining on the map (e.g., last 1–6 players for a 16–128 player map).



Highest Score: If no player achieves the above by the end of Age 10, the player with the highest score (based on wealth, trade influence, infrastructure, and home base development) wins.

6. Player and NPC Interaction





Home Base: The player’s central hub, where trade influence and ROI are highest. Growth depends on trade and resource imports.



NPC Cities: AI-controlled cities with dynamic economies that trade with players, providing consistent demand/supply if player count is low.



Diplomacy: Players can form trade alliances, set tariffs, or embargo others to influence the market.



Hostile Takeovers:





Players in debt (negative balance due to loans or mismanagement) become vulnerable.



Other players can purchase shares of their trade empire (e.g., trade routes, infrastructure) using currency.



Acquiring 51% of shares allows full control, absorbing the target’s assets and influence into the buyer’s empire.

Research System

A complex research system drives progression within each of the 10 ages. Research is divided into five categories, with technologies locked to specific ages based on the game’s time-based progression. Players allocate resources (currency, materials, and research points) to unlock technologies, enhancing transport, trade, building, and other systems.

Research Mechanics





Time-Based Ages:





Each age lasts a fixed duration (e.g., 12 hours real-time or 1 in-game week).



Technologies are locked to their respective age and cannot be researched until that age is active.



Players must complete a minimum number of technologies (e.g., 3–5 per category) to maximize competitiveness before the age ends.



Research Points (RP): Generated by research facilities (e.g., libraries in Age 1, universities in Age 5). RP production scales with home base population and building techs.



Costs: Each technology requires RP, currency, and specific resources (e.g., Steam Engine needs 100 RP, $500, and 50 units of iron).



Time: Research takes in-game time (e.g., 30 minutes per 50 RP), adjustable by faction bonuses or techs.



Collaboration: Players can share RP with allies, speeding up research but splitting rewards.

Research Categories





Transport Technologies





Focuses on improving land, water, and air transport methods.



Age-Locked Examples:





Age 1: Basic Carts (unlocks dirt roads, +10% land speed), Rafts (basic water transport).



Age 3: Early Railways (unlocks basic trains), Sailing Ships (+20% water capacity).



Age 5: Steam Engines (unlocks steam trains), Steamships (+30% water speed).



Age 10: Maglev Trains (high-speed land transport), Cargo Drones (automated air delivery).



Prerequisites: Technologies within the same age or prior ages.



Faction Bonus: Sky Pioneers research air technologies 20% faster.



Trade Technologies





Enhances trade efficiency, market access, and diplomacy.



Age-Locked Examples:





Age 1: Barter Systems (unlocks local markets, +10% trade income).



Age 4: Currency Standardization (unlocks trade posts, +15% NPC trade efficiency).



Age 7: Global Trade Networks (unlocks stock exchanges, +20% trade volume).



Age 10: Blockchain Trade (automated contracts, -50% negotiation time).



Prerequisites: Requires transport or building techs from the same or prior ages.



Faction Bonus: Logistics Experts reduce trade tech research time by 10%.



Building Technologies





Improves infrastructure and production facilities to support home base growth.



Age-Locked Examples:





Age 1: Wooden Warehouses (+500 storage units).



Age 3: Brick Buildings (unlocks medium factories, +20% production).



Age 6: Steel-Framed Structures (-15% building maintenance).



Age 10: Automated Warehouses (+50% storage efficiency).



Prerequisites: Tied to Industry techs from the same or prior ages.



Faction Bonus: Resource Haulers gain 10% reduced building costs for storage facilities.



Industry Technologies





Focuses on resource extraction, processing, and production efficiency.



Age-Locked Examples:





Age 1: Manual Tools (+10% resource extraction).



Age 4: Mechanized Mining (doubles raw material output).



Age 7: Assembly Lines (-20% production costs).



Age 10: Nanofabrication (-50% resource cost for high-tech goods).



Prerequisites: Requires building or transport techs from the same or prior ages.



Faction Bonus: Land-Water Synergy reduces industry tech resource costs by 5%.



Economy Technologies





Enhances financial systems, workforce management, and home base development.



Age-Locked Examples:





Age 1: Tax Collection (+10% home base income).



Age 3: Banking (+20% available capital via loans).



Age 6: Universal Education (+15% worker efficiency).



Age 10: AI Workforce (-30% labor costs).



Prerequisites: Tied to trade or building techs from the same or prior ages.



Faction Bonus: Air-Water Innovators research economy techs 10% faster.

Research Tree Structure





Each category has ~5–7 technologies per age, totaling ~25–35 technologies per category across 10 ages (~125–175 total technologies).



Cross-category dependencies within the same age (e.g., Steam Engines in Transport require Mechanized Mining in Industry).



Players prioritize technologies based on their faction bonuses and trade strategy.

Next Steps for Refinement





Define specific transport units per age and mode (e.g., cart types, ship classes).



Detail resource types and their production chains (e.g., ore → steel → machinery).



Finalize research tree with exact RP costs, prerequisites, and time requirements.



Specify mechanics for trade influence calculation and hostile takeover share purchasing.



Set specific age durations and minimum research requirements per age.



Develop UI/UX concepts for research, trade, hostile takeover, and home base investment interfaces.