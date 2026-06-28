# Mewgenics Mod Developer Documentation: Biomes and Map Generation API

This document details the internal `.gon` schema used to construct the world map, individual biomes (Chapters), and the nodes that populate the player's route during a run. These files are typically found in the `data/maps/` directory.

---

## 1. The Macro Structure (`world.gon`)

The highest level of map generation is defined in `world.gon`. This file strictly dictates the layout of the Acts and how different Chapters link together to form the branching path of a run.

```gon
nodes {
	alley {}
		sewers {}
		caves {}
		junkyard {}
		boneyard {}
        // ...
}
```
* **Routing Strategy:** Modders can edit this file to add entirely new routing branches, force specific biomes to follow others, or add special tags (like `spin_cats true` used in late-game areas) that affect the physics or visuals of the world map.

---

## 2. Chapter/Biome Definition (e.g., `alley.gon`)

Each individual biome is defined by its own `.gon` file. This acts as the master configuration for everything the player encounters while in that biome.

### A. Meta Data
```gon
graphics Map_Alley
chapter_id alley
tileset alley
area_name AREA_NAME_ALLEY
act 1
chapter 1
```
This defines the visual rendering (`tileset`), the localization key (`area_name`), and where it sits in the overall progression (`act 1`, `chapter 1`).

### B. Combat Layouts (`levels`)
```gon
levels {
    folder alley
    easy [easy]
    hard [easy] 
    rare [rare]
    boss [boss]
    miniboss [miniboss]
    special [special]
}
```
This points the engine to the specific combat room layouts (tile configurations, obstacles) used when generating standard battle nodes, hard battles, or boss fights for this biome.

### C. Enemies and Bosses
```gon
bosses {
    radicalrat auto 
    queenhippo auto
}

enemy_pools {
    small [Maggot Fly Flea Pinky]
    medium [Rat Leaper Pooter Kitten TomTom Mangy CatCaller]
    large []
}
```
* **`bosses` / `minibosses`**: Lists the exact bosses that can spawn at the end of the chapter. `auto` tells the engine to automatically link the boss's subfolder and cutscene based on their ID.
* **`enemy_pools`**: This is critical. It defines the random encounters for standard battle nodes. Modders can inject custom enemies here to make them spawn natively in the Alley.

### D. Events and Items
```gon
events {
    normal [
        common
        alley_events.gon
    ]
}
item_pools {
    chapter_item_pool alleyitems
}
```
Links the biome to its specific story events and loot tables.

### E. Progression Flags and Exits
```gon
flags {
    SewersUnlocked {
        exit0 { locked false }
    }
}
```
Map flags are used to physically lock or hide exits until the player completes specific metaprogression achievements (e.g., you cannot travel to the Sewers until `SewersUnlocked` is flagged as true in the save file).

---

## 3. Map Nodes (`standard_nodes.gon`)

The actual "web" the player clicks through is populated by Nodes. While `standard_nodes.gon` defines the universal types, individual biomes can override or add to them.

### Core Node Types:
* **`battle`**: A standard combat encounter.
* **`hard`**: A difficult combat encounter, usually rewarding higher tier loot or specific item pools.
* **`miniboss` / `boss`**: Major progression blockers.
* **`event` / `optional_event`**: Non-combat story nodes that offer choices or gambles.
* **`npc` / `shop`**: Safe nodes containing vendors or upgrade mechanics.
* **`treasure`**: A node containing loot.

### Hard Path Rewards:
Mewgenics uses specific node variants to act as high-value rewards at the end of `hard` branching paths. Modders can inject these into custom maps:
* `foodbox`
* `largemeteor` / `smallmeteor`
* `furniturebox` (Rewards meta-progression house items)
* `abilityneedle` (Rewards immediate active ability upgrades)
* `treasure_radiated` / `ancestor_bones` (Cursed or highly specialized loot)

---

## Summary for Modders

To create a completely custom biome, you must:
1. Create a new `custom_biome.gon` in `data/maps/`.
2. Define its `levels`, `enemy_pools`, and `events`.
3. Add the biome to `world.gon` so the engine knows where it connects.
4. Ensure you have the corresponding `tileset` and `graphics` defined in your art folder.



---

## 4. Master Biome Database

The following tables outline the specific bosses, minibosses, and enemy pools native to each biome, grouped by Act.

### Act 0

| Chapter | Area Name | Bosses | Minibosses | Small Enemies | Medium Enemies | Large Enemies |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | **The Path** | pebbles | None | Maggot, Fly, Flea, Pinky | Rat, Leaper, Pooter, Kitten, TomTom, Mangy, CatCaller | None |
### Act 1

| Chapter | Area Name | Bosses | Minibosses | Small Enemies | Medium Enemies | Large Enemies |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | **The Alley** | radicalrat, queenhippo | fightercat, huntercat, magecat, tankcat, jestercat | Maggot, Fly, Flea, Pinky | Rat, Leaper, Pooter, Kitten, TomTom, Mangy, CatCaller | None |
| 2 | **The Junkyard** | cancreeper, trampy, chubsandnubs | cancreeper, trampy | Maggot, Fly | Lumpy, GlassSpitter, Siren, Jekyll, SpikedCat, PopeyeCat, ChumBag, Chummy, Host | None |
| 2 | **The Sewers** | flushmaster, ratking, boris | flushmaster, ratking | Dip | BabyShark, GassyCat, SharkyCat, BoomerCat, WaterKitten, Pile, Floater, WaterLeech, Fetus, FetusGusher | DaddyShark |
| 3 | **The Boneyard** | mamamaggot, dybbuk | mamamaggot | Flea, Wisp, Fly, Maggot | ZombieCat, SkeletonCat, TallSkeletonCat, WolfCat, Tatters, Spookie, Scary, Reaper, TallRobes, GraveWorm, ButtZombie | Shambler |
| 3 | **The Caves** | slime, spiderkitten | slime | TinySpider | SkullOoze, BrainDrain, Bat, TallSpiderCat, SpiderCat, Toadie, AlbinoTomTom, KirbyFetus, TenTickles | MegaFetus |
| 4 | **The Throbbing Domain** | throbbingking | None | Clot, Maggot | Skinned, ThrobbingTurret, FleshLad, Parasiter, MeatSlime, StemCat, TumorousMaggot, ChargeyMaggot, SwappyMaggot | None |
### Act 2

| Chapter | Area Name | Bosses | Minibosses | Small Enemies | Medium Enemies | Large Enemies |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | **The Desert** | zodiac, gambit | thiefcat, clericcat, butchercat, necrocat, jestercat | RattleSnake | FlySwarm, SnakeyBones, Carcus, Peashy, BabyDeathWorm, HornyCat, GunCat, Mangy2, ScorpionCat | SkeletonShambler, Thump, DeathWorm |
| 2 | **The Bunker** | lenny, bumblefoot, johnny | lenny, bumblefoot | None | AtomicKitten, RoboTom, CatCultist, Cultist, CultistZealot, CultistMutant, CultistBishop, BishopHat, LoveBot, SecurityBot, Hive, FloatingHive | KillDozer |
| 2 | **The Crater** | rockybobo, infestedduo, alienqueen | rockybobo, infestedduo | Amoeba | GeoLad, BrambleBaby, Hemlock, Nettle, Birthwort, Tremblo, Infested, RockHead, NoHead, CraterCreeper | Carnibulb |
| 3 | **The Core** | cerberubs, coven | cerberubs | None | CoreFreak, PokerDemon, Whisperer, CloakedDemon, BigDemon, HeadTumor, TallTumor, DemonHooker, Belcher, TumorCat | MegaTumor |
| 3 | **The Moon** | abandonedones, moonhead | abandonedones | MoonWorm | BigAsteroid, SmallAsteroid, SmallUFO, YellowBlaster, GreyAlien, GreenProber, Waggle, MoonWorm, Rover, Astro | BigUFO |
| 4 | **The Rift** | chaos | None | FrankPinky | JackCat, ChaosStacy, FrankFetus, BeaniesRat | ButchTinkBoris, TracyFetus |
### Act 3

| Chapter | Area Name | Bosses | Minibosses | Small Enemies | Medium Enemies | Large Enemies |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | **The Lab** | stacy, spewer | druidcat, monkcat, psychiccat, tinkerercat, jestercat | None | RatCat, Gamete, NubsCat, CatHuman, HumanCat, CopBot, DrDitto, Drcat, Mangy3, Needlecat, Stacy2p0 | MegaMutant |
| 2 | **Das Füture** | lightningelemental, drmangler, hitler | lightningelemental, drmangler | Invader | FatCat, FutureBot, SoldierBot, HangerBot, DoctorBot, TallBot, TVBot, JarHead, FetusJar, FetusNoJar | FatMan, FatWoman |
| 2 | **The Ice Age** | iceelemental, cavecatfamily, lordbunga | iceelemental, cavecatfamily | None | CaveBaby, CaveMan, CaveWoman, WereMan, CaveChief, Yeti, Yeticat, SabertoothCat, SabertoothCub, MammothBaby, Fuzzer | Mammoth |
| 3 | **The Jurassic** | dinocouple, megadino | dinocouple | None | PrehistoricPooter, Pterodactyl, Raptor, RaptorBaby, Ankylosaurus, Parasaurolophus, Maelestes, DinoEggs | Trex, Stegosaurus, Triceratops |
| 3 | **The End** | thebloat, themother | thebloat | None | BoyShade, GirlShade, Gasper, Floast, TumorBarrier, Husk, ConjoinedHusk, CancerCat, CollectiveCat, ShadeCat | Slag |
| 4 | **The Infinite** | thecreator | None | None | Cherubim, Seraphim, Gatekeeper, AngelicKitten, AngelicCat | None |
