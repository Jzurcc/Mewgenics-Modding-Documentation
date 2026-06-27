# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Map Generation & Routing

> **Associated Files:** `data/maps/`


### Object: `ROOT`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 39

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 883 | `common`<br>`rare`<br>`cha` |
| [`boss`](./Miscellaneous.md#object-boss) | Object  | An object defining the properties of a boss encounter, such as rewards or level. | 131 | `{ . . . }` |
| [`rare`](./Arrays.md#array-rare) | `Array`  | Defines the rare reward block for a boss encounter. | 34 | `1`<br>`10`<br>`15` |
| [`repeat`](./Enums.md#enum-repeat) | Enum | Determines how many times an event, song, or unlock can be triggered. Accepts a positive integer or the string "infinite". | 33 | `1`<br>`2`<br>`20` |
| [`special`](./Arrays.md#array-special) | Array | An array or boolean indicating that an item or entry is a special container or category. | 29 | `[special]`<br>`true` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 27 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`battle`](./Miscellaneous.md#object-battle) | Object | Defines a battle encounter by preset, level file path, or reverb settings. | 25 | `{ . . . }` |
| [`hard`](./Arrays.md#array-hard) | Array | Configuration for hard difficulty, including elite/champ budgets and rewards. | 23 | `[easy bigsharklevels]`<br>`[easy]`<br>`[hard]` |
| [`miniboss`](./Arrays.md#array-miniboss) | Array | An array or object defining the reward table for miniboss encounters, including coin ranges, food ranges, and loot chances. | 23 | `[miniboss]` |
| [`normal`](./Arrays.md#array-normal) | Array | An array or object defining the reward table for normal encounters, including coin ranges, food ranges, and loot chances. | 23 | `[` |
| [`event`](./Enums.md#enum-event) | Enum | Specifies the event to force, either by name or by a nested object defining its type and level. | 22 | `Blessing`<br>`Death`<br>`Tragedy` |
| [`level`](./Enums.md#enum-level) | Enum | The level or quest identifier to load. | 21 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| [`folder`](./Enums.md#enum-folder) | Enum | The subdirectory or group name used to organize related levels or content. | 20 | `alley`<br>`boneyard`<br>`bunker` |
| [`easy`](./Arrays.md#array-easy) | Array | Configuration for easy difficulty, including elite/champ budgets and rewards. | 20 | `[easy bigsharklevels]`<br>`[easy]` |
| [`chapter_item_pool`](./Enums.md#enum-chapter_item_pool) | Enum | Specifies the item pool identifier used by a chapter or boss to determine which items can be found. | 19 | `alleyitems`<br>`boneyarditems`<br>`bunkeritems` |
| [`include`](./Strings.md#string-include) | String | Specifies the path to another file to include and merge into the current schema definition. | 19 ||
| [`large`](./Arrays.md#array-large) | Array | An array of enemy unit identifiers used as the large enemy pool for an area or boss encounter. | 19 | `[Carnibulb]`<br>`[KillDozer]`<br>`[MegaFetus]` |
| [`medium`](./Arrays.md#array-medium) | Array | An array of enemy unit identifiers used as the medium enemy pool for an area or boss encounter. | 19 | `[Rat Leaper Pooter Kitten TomTom Mangy CatCaller]` |
| [`small`](./Arrays.md#array-small) | Array | An array of enemy unit identifiers used as the small enemy pool for an area or boss encounter. | 19 | `[Amoeba]`<br>`[Flea Wisp Fly Maggot]`<br>`[Maggot Fly Flea Pinky]` |
| [`exit0`](./Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 15 | `{ . . . }` |
| [`override_art`](./Enums.md#enum-override_art) | Enum | Specifies the visual art key used to override the default node appearance on the map. | 12 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |
| [`quest_event`](./Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 9 | `{ . . . }` |
| [`time_machine`](./Miscellaneous.md#object-time_machine) | Object | Defines a special event node that leads to a time machine quest level. | 4 | `{ . . . }` |
| [`dimensionx`](./Miscellaneous.md#object-dimensionx) | Object | An enum specifying the Dimension X chapter area, or an object with its specific properties. | 3 | `{ . . . }` |
| [`meatworld`](./Miscellaneous.md#object-meatworld) | Object | An enum specifying the Meatworld chapter area, or an object with its specific properties. | 3 | `{ . . . }` |
| [`boneyard`](./Miscellaneous.md#object-boneyard) | Object | Specifies the name, map flag, or connection for the Boneyard area. | 3 | `{ . . . }` |
| [`bunker`](./Miscellaneous.md#object-bunker) | Object | Specifies the name, map flag, or connection for the Bunker area. | 3 | `{ . . . }` |
| [`core`](./Miscellaneous.md#object-core) | Object | Specifies the name, map flag, or connection for the Core area. | 3 | `{ . . . }` |
| [`moon`](./Miscellaneous.md#object-moon) | Object | Specifies the name, map flag, or connection for the Moon area. | 3 | `{ . . . }` |
| [`alley`](./Miscellaneous.md#object-alley) | Object | Specifies the name, map flag, or connection for the Alley area. | 3 | `{ . . . }` |
| [`endoftime`](./Miscellaneous.md#object-endoftime) | Object | Configures various attributes of the End of Time area, depending on context. | 3 | `{ . . . }` |
| [`crater`](./Miscellaneous.md#object-crater) | Object | Specifies the name, map flag, or connection for the Crater area. | 3 | `{ . . . }` |
| [`desert`](./Miscellaneous.md#object-desert) | Object | Specifies the name, map flag, or connection for the Desert area. | 3 | `{ . . . }` |
| [`future`](./Miscellaneous.md#object-future) | Object | Specifies the name, map flag, or connection for the Future area. | 3 | `{ . . . }` |
| [`sewers`](./Miscellaneous.md#object-sewers) | Object | Specifies the name, map flag, or connection for the Sewers area. | 3 | `{ . . . }` |
| [`iceage`](./Miscellaneous.md#object-iceage) | Object | Specifies the name, map flag, or connection for the Ice Age area. | 3 | `{ . . . }` |
| [`jurassic`](./Miscellaneous.md#object-jurassic) | Object | Specifies the name, map flag, or connection for the Jurassic area. | 3 | `{ . . . }` |
| [`lab`](./Miscellaneous.md#object-lab) | Object | Specifies the name, map flag, or connection for the Lab area. | 3 | `{ . . . }` |
| [`theend`](./Miscellaneous.md#object-theend) | Object | Specifies the name, map flag, or connection for The End area. | 3 | `{ . . . }` |
| [`caves`](./Miscellaneous.md#object-caves) | Object | Specifies the name, map flag, or connection for the Caves area. | 3 | `{ . . . }` |
| [`junkyard`](./Miscellaneous.md#object-junkyard) | Object | Specifies the name, map flag, or connection for the Junkyard area. | 3 | `{ . . . }` |
| [`jestercat`](./Enums.md#enum-jestercat) | Enum | Specifies the boss or miniboss configuration for JesterCat, often set to "auto" for procedural generation. | 3 | `auto` |
| [`exit1`](./Miscellaneous.md#object-exit1) | Object  | An object defining the properties of the second exit from this node. | 3 | `{ . . . }` |
| [`BothObelisksUnlocked`](./Miscellaneous.md#object-bothobelisksunlocked) | Object  | Configures the map event and art when both obelisks have been unlocked. | 2 | `{ . . . }` |
| [`MeatWorldUnlocked`](./Miscellaneous.md#object-meatworldunlocked) | Object  | Configures the map event and routes when MeatWorld is initially unlocked. | 2 | `{ . . . }` |
| [`DimensionXUnlocked`](./Miscellaneous.md#object-dimensionxunlocked) | Object  | Configures the map event and art when Dimension X is unlocked. | 2 | `{ . . . }` |
| [`EndOfTimeUnlocked`](./Miscellaneous.md#object-endoftimeunlocked) | Object  | Configures the map event and route visibility when End of Time is unlocked. | 2 | `{ . . . }` |
| [`hard_initial`](./Miscellaneous.md#object-hard_initial) | Object  | An object defining the properties of the initial hard path node. | 2 | `{ . . . }` |
| [`HardPathUnlocked`](./Miscellaneous.md#object-hardpathunlocked) | Object  | Unlocks the hard difficulty path on the map, usually by setting a node's locked state to false. | 2 | `{ . . . }` |
| [`VolcanoAntennaAttached`](./Miscellaneous.md#object-volcanoantennaattached) | Object  | Configures the map event and art when the Volcano Antenna has been attached. | 2 | `{ . . . }` |
| [`treasure`](./Shops.md#object-treasure) | Object | Defines a treasure node containing items or item pools. | 1 | `{ . . . }` |
| [`CoreObeliskUnlocked`](./Miscellaneous.md#object-coreobeliskunlocked) | Object  | Configures the map event and art when the Core Obelisk is raised and unlocked. | 1 | `{ . . . }` |
| [`MoonObeliskUnlocked`](./Miscellaneous.md#object-moonobeliskunlocked) | Object  | Configures the map event and art when the Moon Obelisk is raised and unlocked. | 1 | `{ . . . }` |
| [`queenhippo`](./Enums.md#enum-queenhippo) | Enum | Specifies the boss configuration for QueenHippo. Setting to "auto" generates it procedurally, or an inline object can define custom subfolder and cutscene. | 1 | `auto` |
| [`butchercat`](./Enums.md#enum-butchercat) | Enum | Specifies the miniboss configuration for ButcherCat, typically set to "auto". | 1 | `auto` |
| [`fightercat`](./Enums.md#enum-fightercat) | Enum | Specifies the miniboss configuration for FighterCat, typically set to "auto". | 1 | `auto` |
| [`magecat`](./Enums.md#enum-magecat) | Enum | Specifies the miniboss configuration for MageCat, typically set to "auto". | 1 | `auto` |
| [`monkcat`](./Enums.md#enum-monkcat) | Enum | Specifies the miniboss configuration for MonkCat, typically set to "auto". | 1 | `auto` |
| [`necrocat`](./Enums.md#enum-necrocat) | Enum | Specifies the miniboss configuration for NecroCat, typically set to "auto". | 1 | `auto` |
| [`psychiccat`](./Enums.md#enum-psychiccat) | Enum | Specifies the miniboss configuration for PsychicCat, typically set to "auto". | 1 | `auto` |
| [`start`](./Enums.md#enum-start) | Enum | Specifies the initial animation state played at the beginning of an ability. | 1 | `attack`<br>`lickAttack`<br>`monkAttack` |
| [`thiefcat`](./Enums.md#enum-thiefcat) | Enum | Specifies the miniboss configuration for ThiefCat, typically set to "auto". | 1 | `auto` |
| [`tinkerercat`](./Enums.md#enum-tinkerercat) | Enum | Specifies the miniboss configuration for TinkerCat, typically set to "auto". | 1 | `auto` |
| [`bumblefoot`](./Enums.md#enum-bumblefoot) | Enum | Specifies the Bumblefoot miniboss encounter. | 1 | `auto` |
| [`flushmaster`](./Enums.md#enum-flushmaster) | Enum | Specifies the Flushmaster miniboss encounter. | 1 | `auto` |
| [`gambit`](./Enums.md#enum-gambit) | Enum | Determines which Gambit boss encounter occurs. | 1 | `auto` |
| [`radicalrat`](./Enums.md#enum-radicalrat) | Enum | Specifies the Radical Rat boss encounter. | 1 | `auto` |
| [`spewer`](./Enums.md#enum-spewer) | Enum | Specifies the Spewer boss encounter. | 1 | `auto` |
| [`zodiac`](./Enums.md#enum-zodiac) | Enum | Specifies the Zodiac boss encounter. | 1 | `auto` |
| [`abandonedones`](./Enums.md#enum-abandonedones) | Enum | Specifies the Abandoned Ones miniboss encounter. | 1 | `auto` |
| `advance` | Number | The number of levels the nemesis advances when triggered. | 1 | `1` |
| [`BoneyardUnlocked`](./Miscellaneous.md#object-boneyardunlocked) | Object  | Unlocks an exit route to the Boneyard on the map. | 1 | `{ . . . }` |
| [`BunkerUnlocked`](./Miscellaneous.md#object-bunkerunlocked) | Object  | Unlocks an exit route to the Bunker on the map. | 1 | `{ . . . }` |
| [`cancreeper`](./Enums.md#enum-cancreeper) | Enum | Specifies the Cancreeper miniboss encounter. | 1 | `auto` |
| [`cavecatfamily`](./Enums.md#enum-cavecatfamily) | Enum | Specifies the Cave Cat Family miniboss encounter. | 1 | `auto` |
| [`CavesUnlocked`](./Miscellaneous.md#object-cavesunlocked) | Object  | Unlocks an exit route to the Caves on the map. | 1 | `{ . . . }` |
| [`cerberubs`](./Enums.md#enum-cerberubs) | Enum | Specifies the Cerberubs miniboss encounter. | 1 | `auto` |
| [`ChaosAntennaAttached`](./Miscellaneous.md#object-chaosantennaattached) | Object  | Configures the map event and art when the Chaos Antenna has been attached. | 1 | `{ . . . }` |
| [`clericcat`](./Enums.md#enum-clericcat) | Enum | Specifies the Cleric Cat miniboss encounter. | 1 | `auto` |
| [`CoreUnlocked`](./Miscellaneous.md#object-coreunlocked) | Object  | Unlocks an exit route to the Core on the map. | 1 | `{ . . . }` |
| [`CraterUnlocked`](./Miscellaneous.md#object-craterunlocked) | Object  | Unlocks an exit route to the Crater on the map. | 1 | `{ . . . }` |
| [`dinocouple`](./Enums.md#enum-dinocouple) | Enum | Specifies the Dino Couple miniboss encounter. | 1 | `auto` |
| [`drmangler`](./Enums.md#enum-drmangler) | Enum | Specifies the Dr. Mangler miniboss encounter. | 1 | `auto` |
| [`druidcat`](./Enums.md#enum-druidcat) | Enum | Specifies the Druid Cat miniboss encounter. | 1 | `auto` |
| [`exit_desert`](./Miscellaneous.md#object-exit_desert) | Object | Defines the exit node properties for the desert map, including type, next map, lock state, and art. | 1 | `{ . . . }` |
| [`exit_lab`](./Miscellaneous.md#object-exit_lab) | Object | Defines the exit node properties for the lab map, including type, next map, lock state, and art. | 1 | `{ . . . }` |
| [`FutureUnlocked`](./Miscellaneous.md#object-futureunlocked) | Object  | Configures the map event and art when the Future is unlocked. | 1 | `{ . . . }` |
| [`GenFlag_Boss_Spewer`](./Miscellaneous.md#object-genflag_boss_spewer) | Object  | Configures the boss encounter event for the Spewer boss on the map. | 1 | `{ . . . }` |
| [`GenFlag_Boss_Stacy`](./Miscellaneous.md#object-genflag_boss_stacy) | Object  | Configures the miniboss and boss encounter events for the Stacy Mutant boss on the map. | 1 | `{ . . . }` |
| `head_start` | Number | The initial number of turns the nemesis has before the player can act. | 1 | `99` |
| [`home`](./Miscellaneous.md#object-home) | Object | Specifies the option to go home (exit to the main hub). | 1 | `{ . . . }` |
| [`huntercat`](./Enums.md#enum-huntercat) | Enum | Specifies the Hunter Cat miniboss encounter. | 1 | `auto` |
| [`IceAgeUnlocked`](./Miscellaneous.md#object-iceageunlocked) | Object  | Configures the map event and art when Ice Age is unlocked. | 1 | `{ . . . }` |
| [`iceelemental`](./Enums.md#enum-iceelemental) | Enum | Specifies the Ice Elemental miniboss encounter. | 1 | `auto` |
| [`infestedduo`](./Enums.md#enum-infestedduo) | Enum | Specifies the Infested Duo miniboss encounter. | 1 | `auto` |
| [`JunkyardUnlocked`](./Miscellaneous.md#object-junkyardunlocked) | Object  | Unlocks an exit route to the Junkyard on the map. | 1 | `{ . . . }` |
| [`JurassicUnlocked`](./Miscellaneous.md#object-jurassicunlocked) | Object  | Unlocks an exit route to the Jurassic area on the map. | 1 | `{ . . . }` |
| [`lenny`](./Enums.md#enum-lenny) | Enum | Specifies the Lenny miniboss encounter. | 1 | `auto` |
| [`lightningelemental`](./Enums.md#enum-lightningelemental) | Enum | Specifies the Lightning Elemental miniboss encounter. | 1 | `auto` |
| `locked` | Boolean | If true, this exit is locked and cannot be used until unlocked by a condition. | 1 | `false`<br>`true` |
| [`mamamaggot`](./Enums.md#enum-mamamaggot) | Enum | Specifies the Mama Maggot miniboss encounter. | 1 | `auto` |
| [`MeatWorldUnlockedFull`](./Miscellaneous.md#object-meatworldunlockedfull) | Object  | Unlocks hidden battle and hard nodes within the MeatWorld area on the map. | 1 | `{ . . . }` |
| [`miniboss_event`](./Miscellaneous.md#object-miniboss_event) | Object  | An object defining the properties of a mini-boss event at this node. | 1 | `{ . . . }` |
| [`MoonUnlocked`](./Miscellaneous.md#object-moonunlocked) | Object  | Unlocks an exit route to the Moon on the map. | 1 | `{ . . . }` |
| [`musiclayer`](./Enums.md#enum-musiclayer) | Enum | Specifies the music layer to play for this node (e.g., 'boss'). | 1 | `boss` |
| [`mw_altar`](./Miscellaneous.md#object-mw_altar) | Object | A map node that represents a Meat World special event altar with custom art. | 1 | `{ . . . }` |
| [`mw_battle1`](./Miscellaneous.md#object-mw_battle1) | Object  | An object defining the properties of the first MeatWorld battle node. | 1 | `{ . . . }` |
| [`mw_boss`](./Miscellaneous.md#object-mw_boss) | Object  | An object defining the properties of the MeatWorld boss node. | 1 | `{ . . . }` |
| [`mw_earlyhome`](./Miscellaneous.md#object-mw_earlyhome) | Object  | An object defining the properties of the MeatWorld early home node. | 1 | `{ . . . }` |
| [`mw_event1`](./Miscellaneous.md#object-mw_event1) | Object  | An object defining the properties of the first MeatWorld event node. | 1 | `{ . . . }` |
| [`mw_hard1`](./Miscellaneous.md#object-mw_hard1) | Object  | An object defining the properties of the first MeatWorld hard path node. | 1 | `{ . . . }` |
| [`mw_home`](./Miscellaneous.md#object-mw_home) | Object  | An object defining the properties of the MeatWorld home node. | 1 | `{ . . . }` |
| [`mw_quest_event`](./Miscellaneous.md#object-mw_quest_event) | Object  | An object defining the properties of the MeatWorld quest event node. | 1 | `{ . . . }` |
| [`mw_treasure`](./Miscellaneous.md#object-mw_treasure) | Object  | An object defining the properties of the MeatWorld treasure node. | 1 | `{ . . . }` |
| [`ratking`](./Enums.md#enum-ratking) | Enum | Specifies the Rat King miniboss encounter. | 1 | `auto` |
| [`rockybobo`](./Enums.md#enum-rockybobo) | Enum | Specifies the Rocky Bobo miniboss encounter. | 1 | `auto` |
| [`SewersUnlocked`](./Miscellaneous.md#object-sewersunlocked) | Object  | Unlocks an exit route to the Sewers on the map. | 1 | `{ . . . }` |
| [`shop_cheapwater`](./Miscellaneous.md#object-shop_cheapwater) | Object | Node definition for a cheap water shop, specifying its type, level, and override art. | 1 | `{ . . . }` |
| [`shop_water`](./Miscellaneous.md#object-shop_water) | Object | Node definition for a water shop, specifying its type, level, and override art. | 1 | `{ . . . }` |
| [`slime`](./Enums.md#enum-slime) | Enum | Specifies the Slime miniboss encounter. | 1 | `auto` |
| [`spawn_node`](./Enums.md#enum-spawn_node) | Enum | The name of the node where the nemesis first spawns on the map. | 1 | `start` |
| [`stacy`](./Enums.md#enum-stacy) | Enum | Specifies the Stacy boss encounter. | 1 | `auto` |
| [`tankcat`](./Enums.md#enum-tankcat) | Enum | Specifies the Tank Cat miniboss encounter. | 1 | `auto` |
| [`thebloat`](./Enums.md#enum-thebloat) | Enum | Specifies The Bloat miniboss encounter. | 1 | `auto` |
| [`TheEndUnlocked`](./Miscellaneous.md#object-theendunlocked) | Object  | An object that stores flags related to unlocking the 'The End' chapter. | 1 | `{ . . . }` |
| [`ThrobbingArteryDone`](./Miscellaneous.md#object-throbbingarterydone) | Object  | An object that stores flags related to completing the Throbbing Artery quest. | 1 | `{ . . . }` |
| [`trampy`](./Enums.md#enum-trampy) | Enum | Specifies the Trampy miniboss encounter. | 1 | `auto` |
| [`WallOfFleshDone`](./Miscellaneous.md#object-walloffleshdone) | Object  | An object that stores flags related to completing the Wall of Flesh quest. | 1 | `{ . . . }` |
| [`weather_event`](./Miscellaneous.md#object-weather_event) | Object | Defines a special event that triggers a crater weather level. | 1 | `{ . . . }` |
| [`choose_one`](./Arrays.md#array-choose_one) | Array | A list of generation flags from which exactly one is randomly selected. | 1 | `[GenFlag_Boss_Stacy, GenFlag_Boss_Spewer]` |
| [`nemesis`](./Arrays.md#array-nemesis) | Array | A list of nemesis definitions to use for this level. | 1 | `[nemesis]` |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `boss`


**Definition:** An object defining the properties of a boss encounter, such as rewards or level.
**Total Count:** 41

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`GenFlag_Boss_Spewer`](./Map_Generation_and_Routing.md#context-genflag_boss_spewer), [`GenFlag_Boss_Stacy`](./Map_Generation_and_Routing.md#context-genflag_boss_stacy), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 19 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`boss_cutscene`](./Enums.md#enum-boss_cutscene) | Enum | Specifies which boss cutscene to play before this encounter. | 16 | `alienqueen`<br>`coven`<br>`dybbuk` |
| `is_final_boss` | Boolean | If true, this encounter is the final boss of the chapter. | 2 | `true` |
| [`level`](./Enums.md#enum-level) | Enum | The level or quest identifier to load. | 2 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| [`override_music`](./Enums.md#enum-override_music) | Enum | Specifies an alternative music track to play during this boss encounter. | 2 | `chaos_boss`<br>`finalboss`<br>`throbbingking` |
| [`tileset`](./Enums.md#enum-tileset) | Enum | Specifies the tileset to use for this boss arena. | 1 | `finalboss` |
| [`unlockcheck_on_complete`](./Enums.md#enum-unlockcheck_on_complete) | Enum | The unlock check that is performed upon completing this boss encounter. | 1 | `map_unlock_junkyard` |

</details>


---


### Object: `exit0`


**Definition:** An object defining the properties of the first exit from this node.
**Total Count:** 27

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BoneyardUnlocked`](./Map_Generation_and_Routing.md#context-boneyardunlocked), [`BunkerUnlocked`](./Map_Generation_and_Routing.md#context-bunkerunlocked), [`CavesUnlocked`](./Map_Generation_and_Routing.md#context-cavesunlocked), [`CoreUnlocked`](./Map_Generation_and_Routing.md#context-coreunlocked), [`EndOfTimeUnlocked`](./Map_Generation_and_Routing.md#context-endoftimeunlocked), [`JurassicUnlocked`](./Map_Generation_and_Routing.md#context-jurassicunlocked), [`MeatWorldUnlocked`](./Map_Generation_and_Routing.md#context-meatworldunlocked), [`MoonUnlocked`](./Map_Generation_and_Routing.md#context-moonunlocked), [`ROOT`](./Map_Generation_and_Routing.md#context-root), [`SewersUnlocked`](./Map_Generation_and_Routing.md#context-sewersunlocked), [`TheEndUnlocked`](./Map_Generation_and_Routing.md#context-theendunlocked)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `locked` | Boolean | If true, this exit is locked and cannot be used until unlocked by a condition. | 17 | `false`<br>`true` |
| [`next_map`](./Enums.md#enum-next_map) | Enum | Specifies which map file to load when this exit is used. | 15 | `bunker.gon`<br>`core.gon`<br>`crater.gon` |
| [`override_art`](./Enums.md#enum-override_art) | Enum | Specifies the visual art key used to override the default node appearance on the map. | 15 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 15 | `[attack move spell]`<br>`attack`<br>`battle` |
| `hidden` | Boolean | If true, this exit is not shown on the map until it is discovered. | 10 | `false`<br>`true` |

</details>


---


### Object: `quest_event`


**Definition:** An object defining the properties of a quest-related event at this node, such as its level and art.
**Total Count:** 24

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BothObelisksUnlocked`](./Map_Generation_and_Routing.md#context-bothobelisksunlocked), [`ChaosAntennaAttached`](./Map_Generation_and_Routing.md#context-chaosantennaattached), [`CoreObeliskUnlocked`](./Map_Generation_and_Routing.md#context-coreobeliskunlocked), [`DimensionXUnlocked`](./Map_Generation_and_Routing.md#context-dimensionxunlocked), [`FutureUnlocked`](./Map_Generation_and_Routing.md#context-futureunlocked), [`IceAgeUnlocked`](./Map_Generation_and_Routing.md#context-iceageunlocked), [`MeatWorldUnlocked`](./Map_Generation_and_Routing.md#context-meatworldunlocked), [`MoonObeliskUnlocked`](./Map_Generation_and_Routing.md#context-moonobeliskunlocked), [`ROOT`](./Map_Generation_and_Routing.md#context-root), [`ThrobbingArteryDone`](./Map_Generation_and_Routing.md#context-throbbingarterydone), [`VolcanoAntennaAttached`](./Map_Generation_and_Routing.md#context-volcanoantennaattached), [`WallOfFleshDone`](./Map_Generation_and_Routing.md#context-walloffleshdone)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`override_art`](./Enums.md#enum-override_art) | Enum | Specifies the visual art key used to override the default node appearance on the map. | 24 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |
| [`level`](./Enums.md#enum-level) | Enum | The level or quest identifier to load. | 19 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 11 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `exit1`


**Definition:** An object defining the properties of the second exit from this node.
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CraterUnlocked`](./Map_Generation_and_Routing.md#context-craterunlocked), [`JunkyardUnlocked`](./Map_Generation_and_Routing.md#context-junkyardunlocked), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `locked` | Boolean | If true, this exit is locked and cannot be used until unlocked by a condition. | 5 | `false`<br>`true` |
| [`next_map`](./Enums.md#enum-next_map) | Enum | Specifies which map file to load when this exit is used. | 3 | `bunker.gon`<br>`core.gon`<br>`crater.gon` |
| [`override_art`](./Enums.md#enum-override_art) | Enum | Specifies the visual art key used to override the default node appearance on the map. | 3 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 3 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `hard_initial`


**Definition:** An object defining the properties of the initial hard path node.
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`HardPathUnlocked`](./Map_Generation_and_Routing.md#context-hardpathunlocked), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `locked` | Boolean | If true, this exit is locked and cannot be used until unlocked by a condition. | 4 | `false`<br>`true` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 2 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `time_machine`


**Definition:** Defines a special event node that leads to a time machine quest level.
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum | The level or quest identifier to load. | 4 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| [`override_art`](./Enums.md#enum-override_art) | Enum | Specifies the visual art key used to override the default node appearance on the map. | 4 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 4 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `BothObelisksUnlocked`


**Definition:** Configures the map event and art when both obelisks have been unlocked.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](./Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 2 | `{ . . . }` |

</details>


---


### Object: `DimensionXUnlocked`


**Definition:** Configures the map event and art when Dimension X is unlocked.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](./Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 2 | `{ . . . }` |

</details>


---


### Object: `EndOfTimeUnlocked`


**Definition:** Configures the map event and route visibility when End of Time is unlocked.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](./Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 2 | `{ . . . }` |

</details>


---


### Object: `HardPathUnlocked`


**Definition:** Unlocks the hard difficulty path on the map, usually by setting a node's locked state to false.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`hard_initial`](./Miscellaneous.md#object-hard_initial) | Object  | An object defining the properties of the initial hard path node. | 2 | `{ . . . }` |

</details>


---


### Object: `MeatWorldUnlocked`


**Definition:** Configures the map event and routes when MeatWorld is initially unlocked.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](./Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 2 | `{ . . . }` |
| [`quest_event`](./Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 2 | `{ . . . }` |

</details>


---


### Object: `miniboss_event`


**Definition:** An object defining the properties of a mini-boss event at this node.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`GenFlag_Boss_Stacy`](./Map_Generation_and_Routing.md#context-genflag_boss_stacy), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 2 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`level`](./Enums.md#enum-level) | Enum | The level or quest identifier to load. | 1 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |

</details>


---


### Object: `mw_battle1`


**Definition:** An object defining the properties of the first MeatWorld battle node.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean | If true, this exit is not shown on the map until it is discovered. | 2 | `false`<br>`true` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `mw_boss`


**Definition:** An object defining the properties of the MeatWorld boss node.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean | If true, this exit is not shown on the map until it is discovered. | 2 | `false`<br>`true` |
| [`boss_cutscene`](./Enums.md#enum-boss_cutscene) | Enum | Specifies which boss cutscene to play before this encounter. | 1 | `alienqueen`<br>`coven`<br>`dybbuk` |
| [`override_music`](./Enums.md#enum-override_music) | Enum | Specifies an alternative music track to play during this boss encounter. | 1 | `chaos_boss`<br>`finalboss`<br>`throbbingking` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `mw_earlyhome`


**Definition:** An object defining the properties of the MeatWorld early home node.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean | If true, this exit is not shown on the map until it is discovered. | 1 | `false`<br>`true` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `mw_event1`


**Definition:** An object defining the properties of the first MeatWorld event node.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean | If true, this exit is not shown on the map until it is discovered. | 2 | `false`<br>`true` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `mw_hard1`


**Definition:** An object defining the properties of the first MeatWorld hard path node.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean | If true, this exit is not shown on the map until it is discovered. | 2 | `false`<br>`true` |
| [`musiclayer`](./Enums.md#enum-musiclayer) | Enum | Specifies the music layer to play for this node (e.g., 'boss'). | 1 | `boss` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `mw_home`


**Definition:** An object defining the properties of the MeatWorld home node.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean | If true, this exit is not shown on the map until it is discovered. | 2 | `false`<br>`true` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `mw_quest_event`


**Definition:** An object defining the properties of the MeatWorld quest event node.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean | If true, this exit is not shown on the map until it is discovered. | 2 | `false`<br>`true` |
| [`level`](./Enums.md#enum-level) | Enum | The level or quest identifier to load. | 1 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| [`override_art`](./Enums.md#enum-override_art) | Enum | Specifies the visual art key used to override the default node appearance on the map. | 1 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `mw_treasure`


**Definition:** An object defining the properties of the MeatWorld treasure node.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean | If true, this exit is not shown on the map until it is discovered. | 2 | `false`<br>`true` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `VolcanoAntennaAttached`


**Definition:** Configures the map event and art when the Volcano Antenna has been attached.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](./Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 2 | `{ . . . }` |

</details>


---


### Object: `battle`


**Definition:** Defines a battle encounter by preset, level file path, or reverb settings.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `BoneyardUnlocked`


**Definition:** Unlocks an exit route to the Boneyard on the map.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](./Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 1 | `{ . . . }` |

</details>


---


### Object: `BunkerUnlocked`


**Definition:** Unlocks an exit route to the Bunker on the map.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](./Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 1 | `{ . . . }` |

</details>


---


### Object: `CavesUnlocked`


**Definition:** Unlocks an exit route to the Caves on the map.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](./Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 1 | `{ . . . }` |

</details>


---


### Object: `ChaosAntennaAttached`


**Definition:** Configures the map event and art when the Chaos Antenna has been attached.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](./Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 1 | `{ . . . }` |

</details>


---


### Object: `CoreObeliskUnlocked`


**Definition:** Configures the map event and art when the Core Obelisk is raised and unlocked.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](./Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 1 | `{ . . . }` |

</details>


---


### Object: `CoreUnlocked`


**Definition:** Unlocks an exit route to the Core on the map.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](./Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 1 | `{ . . . }` |

</details>


---


### Object: `CraterUnlocked`


**Definition:** Unlocks an exit route to the Crater on the map.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit1`](./Miscellaneous.md#object-exit1) | Object  | An object defining the properties of the second exit from this node. | 1 | `{ . . . }` |

</details>


---


### Object: `dimensionx`


**Definition:** An enum specifying the Dimension X chapter area, or an object with its specific properties.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

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

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

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

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum | The level or quest identifier to load. | 1 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `exit_desert`


**Definition:** Defines the exit node properties for the desert map, including type, next map, lock state, and art.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean | If true, this exit is not shown on the map until it is discovered. | 1 | `false`<br>`true` |
| `locked` | Boolean | If true, this exit is locked and cannot be used until unlocked by a condition. | 1 | `false`<br>`true` |
| [`next_map`](./Enums.md#enum-next_map) | Enum | Specifies which map file to load when this exit is used. | 1 | `bunker.gon`<br>`core.gon`<br>`crater.gon` |
| [`override_art`](./Enums.md#enum-override_art) | Enum | Specifies the visual art key used to override the default node appearance on the map. | 1 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `exit_lab`


**Definition:** Defines the exit node properties for the lab map, including type, next map, lock state, and art.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean | If true, this exit is not shown on the map until it is discovered. | 1 | `false`<br>`true` |
| `locked` | Boolean | If true, this exit is locked and cannot be used until unlocked by a condition. | 1 | `false`<br>`true` |
| [`next_map`](./Enums.md#enum-next_map) | Enum | Specifies which map file to load when this exit is used. | 1 | `bunker.gon`<br>`core.gon`<br>`crater.gon` |
| [`override_art`](./Enums.md#enum-override_art) | Enum | Specifies the visual art key used to override the default node appearance on the map. | 1 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `future`


**Definition:** Specifies the name, map flag, or connection for the Future area.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

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

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](./Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 1 | `{ . . . }` |

</details>


---


### Object: `GenFlag_Boss_Spewer`


**Definition:** Configures the boss encounter event for the Spewer boss on the map.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`boss`](./Miscellaneous.md#object-boss) | Object  | An object defining the properties of a boss encounter, such as rewards or level. | 1 | `{ . . . }` |

</details>


---


### Object: `GenFlag_Boss_Stacy`


**Definition:** Configures the miniboss and boss encounter events for the Stacy Mutant boss on the map.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`boss`](./Miscellaneous.md#object-boss) | Object  | An object defining the properties of a boss encounter, such as rewards or level. | 1 | `{ . . . }` |
| [`miniboss_event`](./Miscellaneous.md#object-miniboss_event) | Object  | An object defining the properties of a mini-boss event at this node. | 1 | `{ . . . }` |

</details>


---


### Object: `home`


**Definition:** Specifies the option to go home (exit to the main hub).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `iceage`


**Definition:** Specifies the name, map flag, or connection for the Ice Age area.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

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

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](./Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 1 | `{ . . . }` |

</details>


---


### Object: `JunkyardUnlocked`


**Definition:** Unlocks an exit route to the Junkyard on the map.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit1`](./Miscellaneous.md#object-exit1) | Object  | An object defining the properties of the second exit from this node. | 1 | `{ . . . }` |

</details>


---


### Object: `jurassic`


**Definition:** Specifies the name, map flag, or connection for the Jurassic area.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

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

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](./Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 1 | `{ . . . }` |

</details>


---


### Object: `MeatWorldUnlockedFull`


**Definition:** Unlocks hidden battle and hard nodes within the MeatWorld area on the map.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`mw_battle1`](./Miscellaneous.md#object-mw_battle1) | Object  | An object defining the properties of the first MeatWorld battle node. | 1 | `{ . . . }` |
| [`mw_boss`](./Miscellaneous.md#object-mw_boss) | Object  | An object defining the properties of the MeatWorld boss node. | 1 | `{ . . . }` |
| [`mw_earlyhome`](./Miscellaneous.md#object-mw_earlyhome) | Object  | An object defining the properties of the MeatWorld early home node. | 1 | `{ . . . }` |
| [`mw_event1`](./Miscellaneous.md#object-mw_event1) | Object  | An object defining the properties of the first MeatWorld event node. | 1 | `{ . . . }` |
| [`mw_hard1`](./Miscellaneous.md#object-mw_hard1) | Object  | An object defining the properties of the first MeatWorld hard path node. | 1 | `{ . . . }` |
| [`mw_home`](./Miscellaneous.md#object-mw_home) | Object  | An object defining the properties of the MeatWorld home node. | 1 | `{ . . . }` |
| [`mw_quest_event`](./Miscellaneous.md#object-mw_quest_event) | Object  | An object defining the properties of the MeatWorld quest event node. | 1 | `{ . . . }` |
| [`mw_treasure`](./Miscellaneous.md#object-mw_treasure) | Object  | An object defining the properties of the MeatWorld treasure node. | 1 | `{ . . . }` |

</details>


---


### Object: `MoonObeliskUnlocked`


**Definition:** Configures the map event and art when the Moon Obelisk is raised and unlocked.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](./Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 1 | `{ . . . }` |

</details>


---


### Object: `MoonUnlocked`


**Definition:** Unlocks an exit route to the Moon on the map.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](./Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 1 | `{ . . . }` |

</details>


---


### Object: `mw_altar`


**Definition:** A map node that represents a Meat World special event altar with custom art.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum | The level or quest identifier to load. | 1 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| [`override_art`](./Enums.md#enum-override_art) | Enum | Specifies the visual art key used to override the default node appearance on the map. | 1 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `SewersUnlocked`


**Definition:** Unlocks an exit route to the Sewers on the map.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](./Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 1 | `{ . . . }` |

</details>


---


### Object: `shop_cheapwater`


**Definition:** Node definition for a cheap water shop, specifying its type, level, and override art.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum | The level or quest identifier to load. | 1 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| [`override_art`](./Enums.md#enum-override_art) | Enum | Specifies the visual art key used to override the default node appearance on the map. | 1 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `shop_water`


**Definition:** Node definition for a water shop, specifying its type, level, and override art.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum | The level or quest identifier to load. | 1 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| [`override_art`](./Enums.md#enum-override_art) | Enum | Specifies the visual art key used to override the default node appearance on the map. | 1 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `start`


**Definition:** Specifies the initial animation state played at the beginning of an ability.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `theend`


**Definition:** Specifies the name, map flag, or connection for The End area.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

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

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](./Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 1 | `{ . . . }` |

</details>


---


### Object: `ThrobbingArteryDone`


**Definition:** An object that stores flags related to completing the Throbbing Artery quest.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](./Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 1 | `{ . . . }` |

</details>


---


### Object: `treasure`


**Definition:** Defines a treasure node containing items or item pools.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum | The level or quest identifier to load. | 1 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `WallOfFleshDone`


**Definition:** An object that stores flags related to completing the Wall of Flesh quest.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](./Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 1 | `{ . . . }` |

</details>


---


### Object: `weather_event`


**Definition:** Defines a special event that triggers a crater weather level.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum | The level or quest identifier to load. | 1 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

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