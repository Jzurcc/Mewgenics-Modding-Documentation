---
title: "Map Gen & Routing Schema"
description: "Biome layout rules and node generation logic."
---

# Map Gen & Routing Schema

## Overview
> [!NOTE]
> This schema feeds the procedural generator. It defines node types (combat, event, shop) and how they link together to form a playable map.

## Usage Example
Here is a real example of this object being defined in the game's data:
```gon
levels {
    folder alley
    easy [easy]
    hard [easy] //switch this to "hard" in the brackets if we get specific hard levels in!
    rare [rare]
    boss [boss]
    miniboss [miniboss]
    special [special]
}
```

## Associated Directory Files
To see extracted instances of this schema in the base game, refer to:
- [`Map_Generation_and_Routing.md`](../../Directory/World_and_Events/Map_Generation_and_Routing.md)

---



This document is an exhaustive, auto-generated dictionary of `.gon` properties relevant to this subsystem. While the overview above provides high-level context, you may still need to infer exact engine execution rules through testing or context clues.

## Map Generation & Routing

> **Associated Files:** `data/maps/`


### Object: `ROOT`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 39

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 883 | `common`<br>`rare`<br>`cha` |
| [`boss`](../Reference_and_Meta/Miscellaneous.md#object-boss) | Object  | An object defining the properties of a boss encounter, such as rewards or level. | 131 | `{ . . . }` |
| `rare` | `Array`  | Defines the rare reward block for a boss encounter. | 34 | `1`<br>`10`<br>`15` |
| [`repeat`](../Reference_and_Meta/Enums.md#enum-repeat) | Enum | Determines how many times an event, song, or unlock can be triggered. Accepts a positive integer or the string "infinite". | 33 | `1`<br>`2`<br>`20` |
| [`special`](../Reference_and_Meta/Arrays.md#array-special) | Array | An array or boolean indicating that an item or entry is a special container or category. | 29 | `[special]`<br>`true` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 27 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`battle`](../Reference_and_Meta/Miscellaneous.md#object-battle) | Object | Defines a battle encounter by preset, level file path, or reverb settings. | 25 | `{ . . . }` |
| [`hard`](../Reference_and_Meta/Arrays.md#array-hard) | Array | Configuration for hard difficulty, including elite/champ budgets and rewards. | 23 | `[easy bigsharklevels]`<br>`[easy]`<br>`[hard]` |
| [`miniboss`](../Reference_and_Meta/Arrays.md#array-miniboss) | Array | An array or object defining the reward table for miniboss encounters, including coin ranges, food ranges, and loot chances. | 23 | `[miniboss]` |
| [`normal`](../Reference_and_Meta/Arrays.md#array-normal) | Array | An array or object defining the reward table for normal encounters, including coin ranges, food ranges, and loot chances. | 23 | `[` |
| [`event`](../Reference_and_Meta/Enums.md#enum-event) | Enum | Specifies the event to force, either by name or by a nested object defining its type and level. | 22 | `Blessing`<br>`Death`<br>`Tragedy` |
| [`level`](../Reference_and_Meta/Enums.md#enum-level) | Enum | The level or quest identifier to load. | 21 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| [`folder`](../Reference_and_Meta/Enums.md#enum-folder) | Enum | The subdirectory or group name used to organize related levels or content. | 20 | `alley`<br>`boneyard`<br>`bunker` |
| [`easy`](../Reference_and_Meta/Arrays.md#array-easy) | Array | Configuration for easy difficulty, including elite/champ budgets and rewards. | 20 | `[easy bigsharklevels]`<br>`[easy]` |
| [`chapter_item_pool`](../Reference_and_Meta/Enums.md#enum-chapter_item_pool) | Enum | Specifies the item pool identifier used by a chapter or boss to determine which items can be found. | 19 | `alleyitems`<br>`boneyarditems`<br>`bunkeritems` |
| `include` | String | Specifies the path to another file to include and merge into the current schema definition. | 19 ||
| [`large`](../Reference_and_Meta/Arrays.md#array-large) | Array | An array of enemy unit identifiers used as the large enemy pool for an area or boss encounter. | 19 | `[Carnibulb]`<br>`[KillDozer]`<br>`[MegaFetus]` |
| [`medium`](../Reference_and_Meta/Arrays.md#array-medium) | Array | An array of enemy unit identifiers used as the medium enemy pool for an area or boss encounter. | 19 | `[Rat Leaper Pooter Kitten TomTom Mangy CatCaller]` |
| [`small`](../Reference_and_Meta/Arrays.md#array-small) | Array | An array of enemy unit identifiers used as the small enemy pool for an area or boss encounter. | 19 | `[Amoeba]`<br>`[Flea Wisp Fly Maggot]`<br>`[Maggot Fly Flea Pinky]` |
| [`exit0`](../Reference_and_Meta/Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 15 | `{ . . . }` |
| [`override_art`](../Reference_and_Meta/Enums.md#enum-override_art) | Enum | Specifies the visual art key used to override the default node appearance on the map. | 12 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |
| [`quest_event`](../Reference_and_Meta/Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 9 | `{ . . . }` |
| [`time_machine`](../Reference_and_Meta/Miscellaneous.md#object-time_machine) | Object | Defines a special event node that leads to a time machine quest level. | 4 | `{ . . . }` |
| [`dimensionx`](../Reference_and_Meta/Miscellaneous.md#object-dimensionx) | Object | An enum specifying the Dimension X chapter area, or an object with its specific properties. | 3 | `{ . . . }` |
| [`meatworld`](../Reference_and_Meta/Miscellaneous.md#object-meatworld) | Object | An enum specifying the Meatworld chapter area, or an object with its specific properties. | 3 | `{ . . . }` |
| [`boneyard`](../Reference_and_Meta/Miscellaneous.md#object-boneyard) | Object | Specifies the name, map flag, or connection for the Boneyard area. | 3 | `{ . . . }` |
| [`bunker`](../Reference_and_Meta/Miscellaneous.md#object-bunker) | Object | Specifies the name, map flag, or connection for the Bunker area. | 3 | `{ . . . }` |
| [`core`](../Reference_and_Meta/Miscellaneous.md#object-core) | Object | Specifies the name, map flag, or connection for the Core area. | 3 | `{ . . . }` |
| [`moon`](../Reference_and_Meta/Miscellaneous.md#object-moon) | Object | Specifies the name, map flag, or connection for the Moon area. | 3 | `{ . . . }` |
| [`alley`](../Reference_and_Meta/Miscellaneous.md#object-alley) | Object | Specifies the name, map flag, or connection for the Alley area. | 3 | `{ . . . }` |
| [`endoftime`](../Reference_and_Meta/Miscellaneous.md#object-endoftime) | Object | Configures various attributes of the End of Time area, depending on context. | 3 | `{ . . . }` |
| [`crater`](../Reference_and_Meta/Miscellaneous.md#object-crater) | Object | Specifies the name, map flag, or connection for the Crater area. | 3 | `{ . . . }` |
| [`desert`](../Reference_and_Meta/Miscellaneous.md#object-desert) | Object | Specifies the name, map flag, or connection for the Desert area. | 3 | `{ . . . }` |
| [`future`](../Reference_and_Meta/Miscellaneous.md#object-future) | Object | Specifies the name, map flag, or connection for the Future area. | 3 | `{ . . . }` |
| [`sewers`](../Reference_and_Meta/Miscellaneous.md#object-sewers) | Object | Specifies the name, map flag, or connection for the Sewers area. | 3 | `{ . . . }` |
| [`iceage`](../Reference_and_Meta/Miscellaneous.md#object-iceage) | Object | Specifies the name, map flag, or connection for the Ice Age area. | 3 | `{ . . . }` |
| [`jurassic`](../Reference_and_Meta/Miscellaneous.md#object-jurassic) | Object | Specifies the name, map flag, or connection for the Jurassic area. | 3 | `{ . . . }` |
| [`lab`](../Reference_and_Meta/Miscellaneous.md#object-lab) | Object | Specifies the name, map flag, or connection for the Lab area. | 3 | `{ . . . }` |
| [`theend`](../Reference_and_Meta/Miscellaneous.md#object-theend) | Object | Specifies the name, map flag, or connection for The End area. | 3 | `{ . . . }` |
| [`caves`](../Reference_and_Meta/Miscellaneous.md#object-caves) | Object | Specifies the name, map flag, or connection for the Caves area. | 3 | `{ . . . }` |
| [`junkyard`](../Reference_and_Meta/Miscellaneous.md#object-junkyard) | Object | Specifies the name, map flag, or connection for the Junkyard area. | 3 | `{ . . . }` |
| [`jestercat`](../Reference_and_Meta/Enums.md#enum-jestercat) | Enum | Specifies the boss or miniboss configuration for JesterCat, often set to "auto" for procedural generation. | 3 | `auto` |
| [`exit1`](../Reference_and_Meta/Miscellaneous.md#object-exit1) | Object  | An object defining the properties of the second exit from this node. | 3 | `{ . . . }` |
| [`BothObelisksUnlocked`](../Reference_and_Meta/Miscellaneous.md#object-bothobelisksunlocked) | Object  | Configures the map event and art when both obelisks have been unlocked. | 2 | `{ . . . }` |
| [`MeatWorldUnlocked`](../Reference_and_Meta/Miscellaneous.md#object-meatworldunlocked) | Object  | Configures the map event and routes when MeatWorld is initially unlocked. | 2 | `{ . . . }` |
| [`DimensionXUnlocked`](../Reference_and_Meta/Miscellaneous.md#object-dimensionxunlocked) | Object  | Configures the map event and art when Dimension X is unlocked. | 2 | `{ . . . }` |
| [`EndOfTimeUnlocked`](../Reference_and_Meta/Miscellaneous.md#object-endoftimeunlocked) | Object  | Configures the map event and route visibility when End of Time is unlocked. | 2 | `{ . . . }` |
| [`hard_initial`](../Reference_and_Meta/Miscellaneous.md#object-hard_initial) | Object  | An object defining the properties of the initial hard path node. | 2 | `{ . . . }` |
| [`HardPathUnlocked`](../Reference_and_Meta/Miscellaneous.md#object-hardpathunlocked) | Object  | Unlocks the hard difficulty path on the map, usually by setting a node's locked state to false. | 2 | `{ . . . }` |
| [`VolcanoAntennaAttached`](../Reference_and_Meta/Miscellaneous.md#object-volcanoantennaattached) | Object  | Configures the map event and art when the Volcano Antenna has been attached. | 2 | `{ . . . }` |
| [`treasure`](./Shops.md#object-treasure) | Object | Defines a treasure node containing items or item pools. | 1 | `{ . . . }` |
| [`CoreObeliskUnlocked`](../Reference_and_Meta/Miscellaneous.md#object-coreobeliskunlocked) | Object  | Configures the map event and art when the Core Obelisk is raised and unlocked. | 1 | `{ . . . }` |
| [`MoonObeliskUnlocked`](../Reference_and_Meta/Miscellaneous.md#object-moonobeliskunlocked) | Object  | Configures the map event and art when the Moon Obelisk is raised and unlocked. | 1 | `{ . . . }` |
| [`queenhippo`](../Reference_and_Meta/Enums.md#enum-queenhippo) | Enum | Specifies the boss configuration for QueenHippo. Setting to "auto" generates it procedurally, or an inline object can define custom subfolder and cutscene. | 1 | `auto` |
| [`butchercat`](../Reference_and_Meta/Enums.md#enum-butchercat) | Enum | Specifies the miniboss configuration for ButcherCat, typically set to "auto". | 1 | `auto` |
| [`fightercat`](../Reference_and_Meta/Enums.md#enum-fightercat) | Enum | Specifies the miniboss configuration for FighterCat, typically set to "auto". | 1 | `auto` |
| [`magecat`](../Reference_and_Meta/Enums.md#enum-magecat) | Enum | Specifies the miniboss configuration for MageCat, typically set to "auto". | 1 | `auto` |
| [`monkcat`](../Reference_and_Meta/Enums.md#enum-monkcat) | Enum | Specifies the miniboss configuration for MonkCat, typically set to "auto". | 1 | `auto` |
| [`necrocat`](../Reference_and_Meta/Enums.md#enum-necrocat) | Enum | Specifies the miniboss configuration for NecroCat, typically set to "auto". | 1 | `auto` |
| [`psychiccat`](../Reference_and_Meta/Enums.md#enum-psychiccat) | Enum | Specifies the miniboss configuration for PsychicCat, typically set to "auto". | 1 | `auto` |
| [`start`](../Reference_and_Meta/Enums.md#enum-start) | Enum | Specifies the initial animation state played at the beginning of an ability. | 1 | `attack`<br>`lickAttack`<br>`monkAttack` |
| [`thiefcat`](../Reference_and_Meta/Enums.md#enum-thiefcat) | Enum | Specifies the miniboss configuration for ThiefCat, typically set to "auto". | 1 | `auto` |
| [`tinkerercat`](../Reference_and_Meta/Enums.md#enum-tinkerercat) | Enum | Specifies the miniboss configuration for TinkerCat, typically set to "auto". | 1 | `auto` |
| [`bumblefoot`](../Reference_and_Meta/Enums.md#enum-bumblefoot) | Enum | Specifies the Bumblefoot miniboss encounter. | 1 | `auto` |
| [`flushmaster`](../Reference_and_Meta/Enums.md#enum-flushmaster) | Enum | Specifies the Flushmaster miniboss encounter. | 1 | `auto` |
| [`gambit`](../Reference_and_Meta/Enums.md#enum-gambit) | Enum | Determines which Gambit boss encounter occurs. | 1 | `auto` |
| [`radicalrat`](../Reference_and_Meta/Enums.md#enum-radicalrat) | Enum | Specifies the Radical Rat boss encounter. | 1 | `auto` |
| [`spewer`](../Reference_and_Meta/Enums.md#enum-spewer) | Enum | Specifies the Spewer boss encounter. | 1 | `auto` |
| [`zodiac`](../Reference_and_Meta/Enums.md#enum-zodiac) | Enum | Specifies the Zodiac boss encounter. | 1 | `auto` |
| [`abandonedones`](../Reference_and_Meta/Enums.md#enum-abandonedones) | Enum | Specifies the Abandoned Ones miniboss encounter. | 1 | `auto` |
| `advance` | Number | The number of levels the nemesis advances when triggered. | 1 | `1` |
| [`BoneyardUnlocked`](../Reference_and_Meta/Miscellaneous.md#object-boneyardunlocked) | Object  | Unlocks an exit route to the Boneyard on the map. | 1 | `{ . . . }` |
| [`BunkerUnlocked`](../Reference_and_Meta/Miscellaneous.md#object-bunkerunlocked) | Object  | Unlocks an exit route to the Bunker on the map. | 1 | `{ . . . }` |
| [`cancreeper`](../Reference_and_Meta/Enums.md#enum-cancreeper) | Enum | Specifies the Cancreeper miniboss encounter. | 1 | `auto` |
| [`cavecatfamily`](../Reference_and_Meta/Enums.md#enum-cavecatfamily) | Enum | Specifies the Cave Cat Family miniboss encounter. | 1 | `auto` |
| [`CavesUnlocked`](../Reference_and_Meta/Miscellaneous.md#object-cavesunlocked) | Object  | Unlocks an exit route to the Caves on the map. | 1 | `{ . . . }` |
| [`cerberubs`](../Reference_and_Meta/Enums.md#enum-cerberubs) | Enum | Specifies the Cerberubs miniboss encounter. | 1 | `auto` |
| [`ChaosAntennaAttached`](../Reference_and_Meta/Miscellaneous.md#object-chaosantennaattached) | Object  | Configures the map event and art when the Chaos Antenna has been attached. | 1 | `{ . . . }` |
| [`clericcat`](../Reference_and_Meta/Enums.md#enum-clericcat) | Enum | Specifies the Cleric Cat miniboss encounter. | 1 | `auto` |
| [`CoreUnlocked`](../Reference_and_Meta/Miscellaneous.md#object-coreunlocked) | Object  | Unlocks an exit route to the Core on the map. | 1 | `{ . . . }` |
| [`CraterUnlocked`](../Reference_and_Meta/Miscellaneous.md#object-craterunlocked) | Object  | Unlocks an exit route to the Crater on the map. | 1 | `{ . . . }` |
| [`dinocouple`](../Reference_and_Meta/Enums.md#enum-dinocouple) | Enum | Specifies the Dino Couple miniboss encounter. | 1 | `auto` |
| [`drmangler`](../Reference_and_Meta/Enums.md#enum-drmangler) | Enum | Specifies the Dr. Mangler miniboss encounter. | 1 | `auto` |
| [`druidcat`](../Reference_and_Meta/Enums.md#enum-druidcat) | Enum | Specifies the Druid Cat miniboss encounter. | 1 | `auto` |
| [`exit_desert`](../Reference_and_Meta/Miscellaneous.md#object-exit_desert) | Object | Defines the exit node properties for the desert map, including type, next map, lock state, and art. | 1 | `{ . . . }` |
| [`exit_lab`](../Reference_and_Meta/Miscellaneous.md#object-exit_lab) | Object | Defines the exit node properties for the lab map, including type, next map, lock state, and art. | 1 | `{ . . . }` |
| [`FutureUnlocked`](../Reference_and_Meta/Miscellaneous.md#object-futureunlocked) | Object  | Configures the map event and art when the Future is unlocked. | 1 | `{ . . . }` |
| [`GenFlag_Boss_Spewer`](../Reference_and_Meta/Miscellaneous.md#object-genflag_boss_spewer) | Object  | Configures the boss encounter event for the Spewer boss on the map. | 1 | `{ . . . }` |
| [`GenFlag_Boss_Stacy`](../Reference_and_Meta/Miscellaneous.md#object-genflag_boss_stacy) | Object  | Configures the miniboss and boss encounter events for the Stacy Mutant boss on the map. | 1 | `{ . . . }` |
| `head_start` | Number | The initial number of turns the nemesis has before the player can act. | 1 | `99` |
| [`home`](../Reference_and_Meta/Miscellaneous.md#object-home) | Object | Specifies the option to go home (exit to the main hub). | 1 | `{ . . . }` |
| [`huntercat`](../Reference_and_Meta/Enums.md#enum-huntercat) | Enum | Specifies the Hunter Cat miniboss encounter. | 1 | `auto` |
| [`IceAgeUnlocked`](../Reference_and_Meta/Miscellaneous.md#object-iceageunlocked) | Object  | Configures the map event and art when Ice Age is unlocked. | 1 | `{ . . . }` |
| [`iceelemental`](../Reference_and_Meta/Enums.md#enum-iceelemental) | Enum | Specifies the Ice Elemental miniboss encounter. | 1 | `auto` |
| [`infestedduo`](../Reference_and_Meta/Enums.md#enum-infestedduo) | Enum | Specifies the Infested Duo miniboss encounter. | 1 | `auto` |
| [`JunkyardUnlocked`](../Reference_and_Meta/Miscellaneous.md#object-junkyardunlocked) | Object  | Unlocks an exit route to the Junkyard on the map. | 1 | `{ . . . }` |
| [`JurassicUnlocked`](../Reference_and_Meta/Miscellaneous.md#object-jurassicunlocked) | Object  | Unlocks an exit route to the Jurassic area on the map. | 1 | `{ . . . }` |
| [`lenny`](../Reference_and_Meta/Enums.md#enum-lenny) | Enum | Specifies the Lenny miniboss encounter. | 1 | `auto` |
| [`lightningelemental`](../Reference_and_Meta/Enums.md#enum-lightningelemental) | Enum | Specifies the Lightning Elemental miniboss encounter. | 1 | `auto` |
| `locked` | Boolean | If true, this exit is locked and cannot be used until unlocked by a condition. | 1 | `false`<br>`true` |
| [`mamamaggot`](../Reference_and_Meta/Enums.md#enum-mamamaggot) | Enum | Specifies the Mama Maggot miniboss encounter. | 1 | `auto` |
| [`MeatWorldUnlockedFull`](../Reference_and_Meta/Miscellaneous.md#object-meatworldunlockedfull) | Object  | Unlocks hidden battle and hard nodes within the MeatWorld area on the map. | 1 | `{ . . . }` |
| [`miniboss_event`](../Reference_and_Meta/Miscellaneous.md#object-miniboss_event) | Object  | An object defining the properties of a mini-boss event at this node. | 1 | `{ . . . }` |
| [`MoonUnlocked`](../Reference_and_Meta/Miscellaneous.md#object-moonunlocked) | Object  | Unlocks an exit route to the Moon on the map. | 1 | `{ . . . }` |
| [`musiclayer`](../Reference_and_Meta/Enums.md#enum-musiclayer) | Enum | Specifies the music layer to play for this node (e.g., 'boss'). | 1 | `boss` |
| [`mw_altar`](../Reference_and_Meta/Miscellaneous.md#object-mw_altar) | Object | A map node that represents a Meat World special event altar with custom art. | 1 | `{ . . . }` |
| [`mw_battle1`](../Reference_and_Meta/Miscellaneous.md#object-mw_battle1) | Object  | An object defining the properties of the first MeatWorld battle node. | 1 | `{ . . . }` |
| [`mw_boss`](../Reference_and_Meta/Miscellaneous.md#object-mw_boss) | Object  | An object defining the properties of the MeatWorld boss node. | 1 | `{ . . . }` |
| [`mw_earlyhome`](../Reference_and_Meta/Miscellaneous.md#object-mw_earlyhome) | Object  | An object defining the properties of the MeatWorld early home node. | 1 | `{ . . . }` |
| [`mw_event1`](../Reference_and_Meta/Miscellaneous.md#object-mw_event1) | Object  | An object defining the properties of the first MeatWorld event node. | 1 | `{ . . . }` |
| [`mw_hard1`](../Reference_and_Meta/Miscellaneous.md#object-mw_hard1) | Object  | An object defining the properties of the first MeatWorld hard path node. | 1 | `{ . . . }` |
| [`mw_home`](../Reference_and_Meta/Miscellaneous.md#object-mw_home) | Object  | An object defining the properties of the MeatWorld home node. | 1 | `{ . . . }` |
| [`mw_quest_event`](../Reference_and_Meta/Miscellaneous.md#object-mw_quest_event) | Object  | An object defining the properties of the MeatWorld quest event node. | 1 | `{ . . . }` |
| [`mw_treasure`](../Reference_and_Meta/Miscellaneous.md#object-mw_treasure) | Object  | An object defining the properties of the MeatWorld treasure node. | 1 | `{ . . . }` |
| [`ratking`](../Reference_and_Meta/Enums.md#enum-ratking) | Enum | Specifies the Rat King miniboss encounter. | 1 | `auto` |
| [`rockybobo`](../Reference_and_Meta/Enums.md#enum-rockybobo) | Enum | Specifies the Rocky Bobo miniboss encounter. | 1 | `auto` |
| [`SewersUnlocked`](../Reference_and_Meta/Miscellaneous.md#object-sewersunlocked) | Object  | Unlocks an exit route to the Sewers on the map. | 1 | `{ . . . }` |
| [`shop_cheapwater`](../Reference_and_Meta/Miscellaneous.md#object-shop_cheapwater) | Object | Node definition for a cheap water shop, specifying its type, level, and override art. | 1 | `{ . . . }` |
| [`shop_water`](../Reference_and_Meta/Miscellaneous.md#object-shop_water) | Object | Node definition for a water shop, specifying its type, level, and override art. | 1 | `{ . . . }` |
| [`slime`](../Reference_and_Meta/Enums.md#enum-slime) | Enum | Specifies the Slime miniboss encounter. | 1 | `auto` |
| [`spawn_node`](../Reference_and_Meta/Enums.md#enum-spawn_node) | Enum | The name of the node where the nemesis first spawns on the map. | 1 | `start` |
| [`stacy`](../Reference_and_Meta/Enums.md#enum-stacy) | Enum | Specifies the Stacy boss encounter. | 1 | `auto` |
| [`tankcat`](../Reference_and_Meta/Enums.md#enum-tankcat) | Enum | Specifies the Tank Cat miniboss encounter. | 1 | `auto` |
| [`thebloat`](../Reference_and_Meta/Enums.md#enum-thebloat) | Enum | Specifies The Bloat miniboss encounter. | 1 | `auto` |
| [`TheEndUnlocked`](../Reference_and_Meta/Miscellaneous.md#object-theendunlocked) | Object  | An object that stores flags related to unlocking the 'The End' chapter. | 1 | `{ . . . }` |
| [`ThrobbingArteryDone`](../Reference_and_Meta/Miscellaneous.md#object-throbbingarterydone) | Object  | An object that stores flags related to completing the Throbbing Artery quest. | 1 | `{ . . . }` |
| [`trampy`](../Reference_and_Meta/Enums.md#enum-trampy) | Enum | Specifies the Trampy miniboss encounter. | 1 | `auto` |
| [`WallOfFleshDone`](../Reference_and_Meta/Miscellaneous.md#object-walloffleshdone) | Object  | An object that stores flags related to completing the Wall of Flesh quest. | 1 | `{ . . . }` |
| [`weather_event`](../Reference_and_Meta/Miscellaneous.md#object-weather_event) | Object | Defines a special event that triggers a crater weather level. | 1 | `{ . . . }` |
| [`choose_one`](../Reference_and_Meta/Arrays.md#array-choose_one) | Array | A list of generation flags from which exactly one is randomly selected. | 1 | `[GenFlag_Boss_Stacy, GenFlag_Boss_Spewer]` |
| [`nemesis`](../Reference_and_Meta/Arrays.md#array-nemesis) | Array | A list of nemesis definitions to use for this level. | 1 | `[nemesis]` |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `boss`


**Definition:** An object defining the properties of a boss encounter, such as rewards or level.  
**Total Count:** 41

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`GenFlag_Boss_Spewer`](./Map_Generation_and_Routing.md#object-genflag_boss_spewer), [`GenFlag_Boss_Stacy`](./Map_Generation_and_Routing.md#object-genflag_boss_stacy), [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 19 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`boss_cutscene`](../Reference_and_Meta/Enums.md#enum-boss_cutscene) | Enum | Specifies which boss cutscene to play before this encounter. | 16 | `alienqueen`<br>`coven`<br>`dybbuk` |
| `is_final_boss` | Boolean | If true, this encounter is the final boss of the chapter. | 2 | `true` |
| [`level`](../Reference_and_Meta/Enums.md#enum-level) | Enum | The level or quest identifier to load. | 2 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| [`override_music`](../Reference_and_Meta/Enums.md#enum-override_music) | Enum | Specifies an alternative music track to play during this boss encounter. | 2 | `chaos_boss`<br>`finalboss`<br>`throbbingking` |
| [`tileset`](../Reference_and_Meta/Enums.md#enum-tileset) | Enum | Specifies the tileset to use for this boss arena. | 1 | `finalboss` |
| [`unlockcheck_on_complete`](../Reference_and_Meta/Enums.md#enum-unlockcheck_on_complete) | Enum | The unlock check that is performed upon completing this boss encounter. | 1 | `map_unlock_junkyard` |

</details>


---


### Object: `exit0`


**Definition:** An object defining the properties of the first exit from this node.  
**Total Count:** 27

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BoneyardUnlocked`](./Map_Generation_and_Routing.md#object-boneyardunlocked), [`BunkerUnlocked`](./Map_Generation_and_Routing.md#object-bunkerunlocked), [`CavesUnlocked`](./Map_Generation_and_Routing.md#object-cavesunlocked), [`CoreUnlocked`](./Map_Generation_and_Routing.md#object-coreunlocked), [`EndOfTimeUnlocked`](./Map_Generation_and_Routing.md#object-endoftimeunlocked), [`JurassicUnlocked`](./Map_Generation_and_Routing.md#object-jurassicunlocked), [`MeatWorldUnlocked`](./Map_Generation_and_Routing.md#object-meatworldunlocked), [`MoonUnlocked`](./Map_Generation_and_Routing.md#object-moonunlocked), [`ROOT`](./Map_Generation_and_Routing.md#object-root), [`SewersUnlocked`](./Map_Generation_and_Routing.md#object-sewersunlocked), [`TheEndUnlocked`](./Map_Generation_and_Routing.md#object-theendunlocked)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `locked` | Boolean | If true, this exit is locked and cannot be used until unlocked by a condition. | 17 | `false`<br>`true` |
| [`next_map`](../Reference_and_Meta/Enums.md#enum-next_map) | Enum | Specifies which map file to load when this exit is used. | 15 | `bunker.gon`<br>`core.gon`<br>`crater.gon` |
| [`override_art`](../Reference_and_Meta/Enums.md#enum-override_art) | Enum | Specifies the visual art key used to override the default node appearance on the map. | 15 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 15 | `[attack move spell]`<br>`attack`<br>`battle` |
| `hidden` | Boolean | If true, this exit is not shown on the map until it is discovered. | 10 | `false`<br>`true` |

</details>


---


### Object: `quest_event`


**Definition:** An object defining the properties of a quest-related event at this node, such as its level and art.  
**Total Count:** 24

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BothObelisksUnlocked`](./Map_Generation_and_Routing.md#object-bothobelisksunlocked), [`ChaosAntennaAttached`](./Map_Generation_and_Routing.md#object-chaosantennaattached), [`CoreObeliskUnlocked`](./Map_Generation_and_Routing.md#object-coreobeliskunlocked), [`DimensionXUnlocked`](./Map_Generation_and_Routing.md#object-dimensionxunlocked), [`FutureUnlocked`](./Map_Generation_and_Routing.md#object-futureunlocked), [`IceAgeUnlocked`](./Map_Generation_and_Routing.md#object-iceageunlocked), [`MeatWorldUnlocked`](./Map_Generation_and_Routing.md#object-meatworldunlocked), [`MoonObeliskUnlocked`](./Map_Generation_and_Routing.md#object-moonobeliskunlocked), [`ROOT`](./Map_Generation_and_Routing.md#object-root), [`ThrobbingArteryDone`](./Map_Generation_and_Routing.md#object-throbbingarterydone), [`VolcanoAntennaAttached`](./Map_Generation_and_Routing.md#object-volcanoantennaattached), [`WallOfFleshDone`](./Map_Generation_and_Routing.md#object-walloffleshdone)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`override_art`](../Reference_and_Meta/Enums.md#enum-override_art) | Enum | Specifies the visual art key used to override the default node appearance on the map. | 24 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |
| [`level`](../Reference_and_Meta/Enums.md#enum-level) | Enum | The level or quest identifier to load. | 19 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 11 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `exit1`


**Definition:** An object defining the properties of the second exit from this node.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CraterUnlocked`](./Map_Generation_and_Routing.md#object-craterunlocked), [`JunkyardUnlocked`](./Map_Generation_and_Routing.md#object-junkyardunlocked), [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `locked` | Boolean | If true, this exit is locked and cannot be used until unlocked by a condition. | 5 | `false`<br>`true` |
| [`next_map`](../Reference_and_Meta/Enums.md#enum-next_map) | Enum | Specifies which map file to load when this exit is used. | 3 | `bunker.gon`<br>`core.gon`<br>`crater.gon` |
| [`override_art`](../Reference_and_Meta/Enums.md#enum-override_art) | Enum | Specifies the visual art key used to override the default node appearance on the map. | 3 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 3 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `hard_initial`


**Definition:** An object defining the properties of the initial hard path node.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`HardPathUnlocked`](./Map_Generation_and_Routing.md#object-hardpathunlocked), [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `locked` | Boolean | If true, this exit is locked and cannot be used until unlocked by a condition. | 4 | `false`<br>`true` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 2 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `time_machine`


**Definition:** Defines a special event node that leads to a time machine quest level.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`level`](../Reference_and_Meta/Enums.md#enum-level) | Enum | The level or quest identifier to load. | 4 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| [`override_art`](../Reference_and_Meta/Enums.md#enum-override_art) | Enum | Specifies the visual art key used to override the default node appearance on the map. | 4 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 4 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `BothObelisksUnlocked`


**Definition:** Configures the map event and art when both obelisks have been unlocked.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](../Reference_and_Meta/Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 2 | `{ . . . }` |

</details>


---


### Object: `DimensionXUnlocked`


**Definition:** Configures the map event and art when Dimension X is unlocked.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](../Reference_and_Meta/Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 2 | `{ . . . }` |

</details>


---


### Object: `EndOfTimeUnlocked`


**Definition:** Configures the map event and route visibility when End of Time is unlocked.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](../Reference_and_Meta/Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 2 | `{ . . . }` |

</details>


---


### Object: `HardPathUnlocked`


**Definition:** Unlocks the hard difficulty path on the map, usually by setting a node's locked state to false.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`hard_initial`](../Reference_and_Meta/Miscellaneous.md#object-hard_initial) | Object  | An object defining the properties of the initial hard path node. | 2 | `{ . . . }` |

</details>


---


### Object: `MeatWorldUnlocked`


**Definition:** Configures the map event and routes when MeatWorld is initially unlocked.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](../Reference_and_Meta/Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 2 | `{ . . . }` |
| [`quest_event`](../Reference_and_Meta/Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 2 | `{ . . . }` |

</details>


---


### Object: `miniboss_event`


**Definition:** An object defining the properties of a mini-boss event at this node.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`GenFlag_Boss_Stacy`](./Map_Generation_and_Routing.md#object-genflag_boss_stacy), [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 2 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`level`](../Reference_and_Meta/Enums.md#enum-level) | Enum | The level or quest identifier to load. | 1 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |

</details>


---


### Object: `mw_battle1`


**Definition:** An object defining the properties of the first MeatWorld battle node.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#object-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean | If true, this exit is not shown on the map until it is discovered. | 2 | `false`<br>`true` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `mw_boss`


**Definition:** An object defining the properties of the MeatWorld boss node.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#object-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean | If true, this exit is not shown on the map until it is discovered. | 2 | `false`<br>`true` |
| [`boss_cutscene`](../Reference_and_Meta/Enums.md#enum-boss_cutscene) | Enum | Specifies which boss cutscene to play before this encounter. | 1 | `alienqueen`<br>`coven`<br>`dybbuk` |
| [`override_music`](../Reference_and_Meta/Enums.md#enum-override_music) | Enum | Specifies an alternative music track to play during this boss encounter. | 1 | `chaos_boss`<br>`finalboss`<br>`throbbingking` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `mw_earlyhome`


**Definition:** An object defining the properties of the MeatWorld early home node.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#object-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean | If true, this exit is not shown on the map until it is discovered. | 1 | `false`<br>`true` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `mw_event1`


**Definition:** An object defining the properties of the first MeatWorld event node.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#object-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean | If true, this exit is not shown on the map until it is discovered. | 2 | `false`<br>`true` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `mw_hard1`


**Definition:** An object defining the properties of the first MeatWorld hard path node.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#object-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean | If true, this exit is not shown on the map until it is discovered. | 2 | `false`<br>`true` |
| [`musiclayer`](../Reference_and_Meta/Enums.md#enum-musiclayer) | Enum | Specifies the music layer to play for this node (e.g., 'boss'). | 1 | `boss` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `mw_home`


**Definition:** An object defining the properties of the MeatWorld home node.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#object-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean | If true, this exit is not shown on the map until it is discovered. | 2 | `false`<br>`true` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `mw_quest_event`


**Definition:** An object defining the properties of the MeatWorld quest event node.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#object-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean | If true, this exit is not shown on the map until it is discovered. | 2 | `false`<br>`true` |
| [`level`](../Reference_and_Meta/Enums.md#enum-level) | Enum | The level or quest identifier to load. | 1 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| [`override_art`](../Reference_and_Meta/Enums.md#enum-override_art) | Enum | Specifies the visual art key used to override the default node appearance on the map. | 1 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `mw_treasure`


**Definition:** An object defining the properties of the MeatWorld treasure node.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#object-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean | If true, this exit is not shown on the map until it is discovered. | 2 | `false`<br>`true` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `VolcanoAntennaAttached`


**Definition:** Configures the map event and art when the Volcano Antenna has been attached.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](../Reference_and_Meta/Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 2 | `{ . . . }` |

</details>


---


### Object: `battle`


**Definition:** Defines a battle encounter by preset, level file path, or reverb settings.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `BoneyardUnlocked`


**Definition:** Unlocks an exit route to the Boneyard on the map.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](../Reference_and_Meta/Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 1 | `{ . . . }` |

</details>


---


### Object: `BunkerUnlocked`


**Definition:** Unlocks an exit route to the Bunker on the map.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](../Reference_and_Meta/Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 1 | `{ . . . }` |

</details>


---


### Object: `CavesUnlocked`


**Definition:** Unlocks an exit route to the Caves on the map.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](../Reference_and_Meta/Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 1 | `{ . . . }` |

</details>


---


### Object: `ChaosAntennaAttached`


**Definition:** Configures the map event and art when the Chaos Antenna has been attached.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](../Reference_and_Meta/Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 1 | `{ . . . }` |

</details>


---


### Object: `CoreObeliskUnlocked`


**Definition:** Configures the map event and art when the Core Obelisk is raised and unlocked.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](../Reference_and_Meta/Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 1 | `{ . . . }` |

</details>


---


### Object: `CoreUnlocked`


**Definition:** Unlocks an exit route to the Core on the map.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](../Reference_and_Meta/Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 1 | `{ . . . }` |

</details>


---


### Object: `CraterUnlocked`


**Definition:** Unlocks an exit route to the Crater on the map.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit1`](../Reference_and_Meta/Miscellaneous.md#object-exit1) | Object  | An object defining the properties of the second exit from this node. | 1 | `{ . . . }` |

</details>


---


### Object: `dimensionx`


**Definition:** An enum specifying the Dimension X chapter area, or an object with its specific properties.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean | If true, cats on this node will rotate to face their movement direction. | 1 | `true` |

</details>


---


### Object: `endoftime`


**Definition:** Configures various attributes of the End of Time area, depending on context.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean | If true, cats on this node will rotate to face their movement direction. | 1 | `true` |

</details>


---


### Object: `event`


**Definition:** Specifies the event to force, either by name or by a nested object defining its type and level.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`level`](../Reference_and_Meta/Enums.md#enum-level) | Enum | The level or quest identifier to load. | 1 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `exit_desert`


**Definition:** Defines the exit node properties for the desert map, including type, next map, lock state, and art.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean | If true, this exit is not shown on the map until it is discovered. | 1 | `false`<br>`true` |
| `locked` | Boolean | If true, this exit is locked and cannot be used until unlocked by a condition. | 1 | `false`<br>`true` |
| [`next_map`](../Reference_and_Meta/Enums.md#enum-next_map) | Enum | Specifies which map file to load when this exit is used. | 1 | `bunker.gon`<br>`core.gon`<br>`crater.gon` |
| [`override_art`](../Reference_and_Meta/Enums.md#enum-override_art) | Enum | Specifies the visual art key used to override the default node appearance on the map. | 1 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `exit_lab`


**Definition:** Defines the exit node properties for the lab map, including type, next map, lock state, and art.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean | If true, this exit is not shown on the map until it is discovered. | 1 | `false`<br>`true` |
| `locked` | Boolean | If true, this exit is locked and cannot be used until unlocked by a condition. | 1 | `false`<br>`true` |
| [`next_map`](../Reference_and_Meta/Enums.md#enum-next_map) | Enum | Specifies which map file to load when this exit is used. | 1 | `bunker.gon`<br>`core.gon`<br>`crater.gon` |
| [`override_art`](../Reference_and_Meta/Enums.md#enum-override_art) | Enum | Specifies the visual art key used to override the default node appearance on the map. | 1 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `future`


**Definition:** Specifies the name, map flag, or connection for the Future area.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean | If true, cats on this node will rotate to face their movement direction. | 1 | `true` |

</details>


---


### Object: `FutureUnlocked`


**Definition:** Configures the map event and art when the Future is unlocked.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](../Reference_and_Meta/Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 1 | `{ . . . }` |

</details>


---


### Object: `GenFlag_Boss_Spewer`


**Definition:** Configures the boss encounter event for the Spewer boss on the map.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`boss`](../Reference_and_Meta/Miscellaneous.md#object-boss) | Object  | An object defining the properties of a boss encounter, such as rewards or level. | 1 | `{ . . . }` |

</details>


---


### Object: `GenFlag_Boss_Stacy`


**Definition:** Configures the miniboss and boss encounter events for the Stacy Mutant boss on the map.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`boss`](../Reference_and_Meta/Miscellaneous.md#object-boss) | Object  | An object defining the properties of a boss encounter, such as rewards or level. | 1 | `{ . . . }` |
| [`miniboss_event`](../Reference_and_Meta/Miscellaneous.md#object-miniboss_event) | Object  | An object defining the properties of a mini-boss event at this node. | 1 | `{ . . . }` |

</details>


---


### Object: `home`


**Definition:** Specifies the option to go home (exit to the main hub).  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `iceage`


**Definition:** Specifies the name, map flag, or connection for the Ice Age area.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean | If true, cats on this node will rotate to face their movement direction. | 1 | `true` |

</details>


---


### Object: `IceAgeUnlocked`


**Definition:** Configures the map event and art when Ice Age is unlocked.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](../Reference_and_Meta/Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 1 | `{ . . . }` |

</details>


---


### Object: `JunkyardUnlocked`


**Definition:** Unlocks an exit route to the Junkyard on the map.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit1`](../Reference_and_Meta/Miscellaneous.md#object-exit1) | Object  | An object defining the properties of the second exit from this node. | 1 | `{ . . . }` |

</details>


---


### Object: `jurassic`


**Definition:** Specifies the name, map flag, or connection for the Jurassic area.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean | If true, cats on this node will rotate to face their movement direction. | 1 | `true` |

</details>


---


### Object: `JurassicUnlocked`


**Definition:** Unlocks an exit route to the Jurassic area on the map.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](../Reference_and_Meta/Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 1 | `{ . . . }` |

</details>


---


### Object: `MeatWorldUnlockedFull`


**Definition:** Unlocks hidden battle and hard nodes within the MeatWorld area on the map.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`mw_battle1`](../Reference_and_Meta/Miscellaneous.md#object-mw_battle1) | Object  | An object defining the properties of the first MeatWorld battle node. | 1 | `{ . . . }` |
| [`mw_boss`](../Reference_and_Meta/Miscellaneous.md#object-mw_boss) | Object  | An object defining the properties of the MeatWorld boss node. | 1 | `{ . . . }` |
| [`mw_earlyhome`](../Reference_and_Meta/Miscellaneous.md#object-mw_earlyhome) | Object  | An object defining the properties of the MeatWorld early home node. | 1 | `{ . . . }` |
| [`mw_event1`](../Reference_and_Meta/Miscellaneous.md#object-mw_event1) | Object  | An object defining the properties of the first MeatWorld event node. | 1 | `{ . . . }` |
| [`mw_hard1`](../Reference_and_Meta/Miscellaneous.md#object-mw_hard1) | Object  | An object defining the properties of the first MeatWorld hard path node. | 1 | `{ . . . }` |
| [`mw_home`](../Reference_and_Meta/Miscellaneous.md#object-mw_home) | Object  | An object defining the properties of the MeatWorld home node. | 1 | `{ . . . }` |
| [`mw_quest_event`](../Reference_and_Meta/Miscellaneous.md#object-mw_quest_event) | Object  | An object defining the properties of the MeatWorld quest event node. | 1 | `{ . . . }` |
| [`mw_treasure`](../Reference_and_Meta/Miscellaneous.md#object-mw_treasure) | Object  | An object defining the properties of the MeatWorld treasure node. | 1 | `{ . . . }` |

</details>


---


### Object: `MoonObeliskUnlocked`


**Definition:** Configures the map event and art when the Moon Obelisk is raised and unlocked.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](../Reference_and_Meta/Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 1 | `{ . . . }` |

</details>


---


### Object: `MoonUnlocked`


**Definition:** Unlocks an exit route to the Moon on the map.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](../Reference_and_Meta/Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 1 | `{ . . . }` |

</details>


---


### Object: `mw_altar`


**Definition:** A map node that represents a Meat World special event altar with custom art.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`level`](../Reference_and_Meta/Enums.md#enum-level) | Enum | The level or quest identifier to load. | 1 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| [`override_art`](../Reference_and_Meta/Enums.md#enum-override_art) | Enum | Specifies the visual art key used to override the default node appearance on the map. | 1 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `SewersUnlocked`


**Definition:** Unlocks an exit route to the Sewers on the map.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](../Reference_and_Meta/Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 1 | `{ . . . }` |

</details>


---


### Object: `shop_cheapwater`


**Definition:** Node definition for a cheap water shop, specifying its type, level, and override art.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`level`](../Reference_and_Meta/Enums.md#enum-level) | Enum | The level or quest identifier to load. | 1 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| [`override_art`](../Reference_and_Meta/Enums.md#enum-override_art) | Enum | Specifies the visual art key used to override the default node appearance on the map. | 1 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `shop_water`


**Definition:** Node definition for a water shop, specifying its type, level, and override art.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`level`](../Reference_and_Meta/Enums.md#enum-level) | Enum | The level or quest identifier to load. | 1 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| [`override_art`](../Reference_and_Meta/Enums.md#enum-override_art) | Enum | Specifies the visual art key used to override the default node appearance on the map. | 1 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `start`


**Definition:** Specifies the initial animation state played at the beginning of an ability.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `theend`


**Definition:** Specifies the name, map flag, or connection for The End area.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean | If true, cats on this node will rotate to face their movement direction. | 1 | `true` |

</details>


---


### Object: `TheEndUnlocked`


**Definition:** An object that stores flags related to unlocking the 'The End' chapter.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](../Reference_and_Meta/Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 1 | `{ . . . }` |

</details>


---


### Object: `ThrobbingArteryDone`


**Definition:** An object that stores flags related to completing the Throbbing Artery quest.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](../Reference_and_Meta/Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 1 | `{ . . . }` |

</details>


---


### Object: `treasure`


**Definition:** Defines a treasure node containing items or item pools.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`level`](../Reference_and_Meta/Enums.md#enum-level) | Enum | The level or quest identifier to load. | 1 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `WallOfFleshDone`


**Definition:** An object that stores flags related to completing the Wall of Flesh quest.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](../Reference_and_Meta/Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 1 | `{ . . . }` |

</details>


---


### Object: `weather_event`


**Definition:** Defines a special event that triggers a crater weather level.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`level`](../Reference_and_Meta/Enums.md#enum-level) | Enum | The level or quest identifier to load. | 1 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


---


## Auto-Discovered Objects


### Object: `alley`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


### Object: `boneyard`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


### Object: `bunker`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


### Object: `caves`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


### Object: `core`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


### Object: `crater`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


### Object: `desert`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


### Object: `junkyard`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


### Object: `lab`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


### Object: `meatworld`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


### Object: `moon`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


### Object: `sewers`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>