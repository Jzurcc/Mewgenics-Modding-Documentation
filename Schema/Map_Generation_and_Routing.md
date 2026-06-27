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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 664 | `common`<br>`rare`<br>`cha` |
| [`boss`](./Miscellaneous.md#object-boss) | Object  | An object defining the properties of a boss encounter, such as rewards or level. | 131 | `{ . . . }` |
| [`rare`](./Arrays.md#array-rare) | `Array`  | Defines the rare reward block for a boss encounter. | 34 | `1`<br>`10`<br>`15` |
| [`repeat`](./Enums.md#enum-repeat) | Enum |  | 33 | `1`<br>`2`<br>`20` |
| [`special`](./Arrays.md#array-special) | Array || 29 | `[special]`<br>`true` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 27 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`battle`](./Miscellaneous.md#object-battle) | Object  || 25 | `{ . . . }` |
| [`hard`](./Arrays.md#array-hard) | Array | Configuration for hard difficulty, including elite/champ budgets and rewards. | 23 | `[easy bigsharklevels]`<br>`[easy]`<br>`[hard]` |
| [`miniboss`](./Arrays.md#array-miniboss) | Array || 23 | `[miniboss]` |
| [`normal`](./Arrays.md#array-normal) | Array || 23 | `[` |
| [`event`](./Enums.md#enum-event) | Enum  || 22 | `Blessing`<br>`Death`<br>`Tragedy` |
| [`level`](./Enums.md#enum-level) | Enum || 21 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| [`folder`](./Enums.md#enum-folder) | Enum || 20 | `alley`<br>`boneyard`<br>`bunker` |
| [`easy`](./Arrays.md#array-easy) | Array | Configuration for easy difficulty, including elite/champ budgets and rewards. | 20 | `[easy bigsharklevels]`<br>`[easy]` |
| [`chapter_item_pool`](./Enums.md#enum-chapter_item_pool) | Enum || 19 | `alleyitems`<br>`boneyarditems`<br>`bunkeritems` |
| [`include`](./Strings.md#string-include) | String | Specifies the path to another file to include and merge into the current schema definition. | 19 ||
| [`large`](./Arrays.md#array-large) | Array || 19 | `[Carnibulb]`<br>`[KillDozer]`<br>`[MegaFetus]` |
| [`medium`](./Arrays.md#array-medium) | Array || 19 | `[Rat Leaper Pooter Kitten TomTom Mangy CatCaller]` |
| [`small`](./Arrays.md#array-small) | Array || 19 | `[Amoeba]`<br>`[Flea Wisp Fly Maggot]`<br>`[Maggot Fly Flea Pinky]` |
| [`exit0`](./Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 15 | `{ . . . }` |
| [`override_art`](./Enums.md#enum-override_art) | Enum || 12 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |
| [`quest_event`](./Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 9 | `{ . . . }` |
| [`time_machine`](./Miscellaneous.md#object-time_machine) | Object  || 4 | `{ . . . }` |
| [`dimensionx`](./Miscellaneous.md#object-dimensionx) | Object  || 3 | `{ . . . }` |
| [`meatworld`](./Miscellaneous.md#object-meatworld) | Object  || 3 | `{ . . . }` |
| [`boneyard`](./Miscellaneous.md#object-boneyard) | Object  || 3 | `{ . . . }` |
| [`bunker`](./Miscellaneous.md#object-bunker) | Object  || 3 | `{ . . . }` |
| [`core`](./Miscellaneous.md#object-core) | Object  || 3 | `{ . . . }` |
| [`moon`](./Miscellaneous.md#object-moon) | Object  || 3 | `{ . . . }` |
| [`alley`](./Miscellaneous.md#object-alley) | Object  || 3 | `{ . . . }` |
| [`endoftime`](./Miscellaneous.md#object-endoftime) | Object  || 3 | `{ . . . }` |
| [`crater`](./Miscellaneous.md#object-crater) | Object  || 3 | `{ . . . }` |
| [`desert`](./Miscellaneous.md#object-desert) | Object  || 3 | `{ . . . }` |
| [`future`](./Miscellaneous.md#object-future) | Object  || 3 | `{ . . . }` |
| [`sewers`](./Miscellaneous.md#object-sewers) | Object  || 3 | `{ . . . }` |
| [`iceage`](./Miscellaneous.md#object-iceage) | Object  || 3 | `{ . . . }` |
| [`jurassic`](./Miscellaneous.md#object-jurassic) | Object  || 3 | `{ . . . }` |
| [`lab`](./Miscellaneous.md#object-lab) | Object  || 3 | `{ . . . }` |
| [`theend`](./Miscellaneous.md#object-theend) | Object  || 3 | `{ . . . }` |
| [`caves`](./Miscellaneous.md#object-caves) | Object  || 3 | `{ . . . }` |
| [`junkyard`](./Miscellaneous.md#object-junkyard) | Object  || 3 | `{ . . . }` |
| [`jestercat`](./Enums.md#enum-jestercat) | Enum || 3 | `auto` |
| [`exit1`](./Miscellaneous.md#object-exit1) | Object  | An object defining the properties of the second exit from this node. | 3 | `{ . . . }` |
| [`BothObelisksUnlocked`](./Miscellaneous.md#object-bothobelisksunlocked) | Object  | Configures the map event and art when both obelisks have been unlocked. | 2 | `{ . . . }` |
| [`MeatWorldUnlocked`](./Miscellaneous.md#object-meatworldunlocked) | Object  | Configures the map event and routes when MeatWorld is initially unlocked. | 2 | `{ . . . }` |
| [`DimensionXUnlocked`](./Miscellaneous.md#object-dimensionxunlocked) | Object  | Configures the map event and art when Dimension X is unlocked. | 2 | `{ . . . }` |
| [`EndOfTimeUnlocked`](./Miscellaneous.md#object-endoftimeunlocked) | Object  | Configures the map event and route visibility when End of Time is unlocked. | 2 | `{ . . . }` |
| [`hard_initial`](./Miscellaneous.md#object-hard_initial) | Object  | An object defining the properties of the initial hard path node. | 2 | `{ . . . }` |
| [`HardPathUnlocked`](./Miscellaneous.md#object-hardpathunlocked) | Object  | Unlocks the hard difficulty path on the map, usually by setting a node's locked state to false. | 2 | `{ . . . }` |
| [`VolcanoAntennaAttached`](./Miscellaneous.md#object-volcanoantennaattached) | Object  | Configures the map event and art when the Volcano Antenna has been attached. | 2 | `{ . . . }` |
| [`treasure`](./Shops.md#object-treasure) | Object  || 1 | `{ . . . }` |
| [`CoreObeliskUnlocked`](./Miscellaneous.md#object-coreobeliskunlocked) | Object  | Configures the map event and art when the Core Obelisk is raised and unlocked. | 1 | `{ . . . }` |
| [`MoonObeliskUnlocked`](./Miscellaneous.md#object-moonobeliskunlocked) | Object  | Configures the map event and art when the Moon Obelisk is raised and unlocked. | 1 | `{ . . . }` |
| [`queenhippo`](./Enums.md#enum-queenhippo) | Enum || 1 | `auto` |
| [`butchercat`](./Enums.md#enum-butchercat) | Enum || 1 | `auto` |
| [`fightercat`](./Enums.md#enum-fightercat) | Enum || 1 | `auto` |
| [`magecat`](./Enums.md#enum-magecat) | Enum || 1 | `auto` |
| [`monkcat`](./Enums.md#enum-monkcat) | Enum || 1 | `auto` |
| [`necrocat`](./Enums.md#enum-necrocat) | Enum || 1 | `auto` |
| [`psychiccat`](./Enums.md#enum-psychiccat) | Enum || 1 | `auto` |
| [`start`](./Enums.md#enum-start) | Enum  || 1 | `attack`<br>`lickAttack`<br>`monkAttack` |
| [`thiefcat`](./Enums.md#enum-thiefcat) | Enum || 1 | `auto` |
| [`tinkerercat`](./Enums.md#enum-tinkerercat) | Enum || 1 | `auto` |
| [`bumblefoot`](./Enums.md#enum-bumblefoot) | Enum || 1 | `auto` |
| [`flushmaster`](./Enums.md#enum-flushmaster) | Enum || 1 | `auto` |
| [`gambit`](./Enums.md#enum-gambit) | Enum || 1 | `auto` |
| [`radicalrat`](./Enums.md#enum-radicalrat) | Enum || 1 | `auto` |
| [`spewer`](./Enums.md#enum-spewer) | Enum || 1 | `auto` |
| [`zodiac`](./Enums.md#enum-zodiac) | Enum || 1 | `auto` |
| [`abandonedones`](./Enums.md#enum-abandonedones) | Enum || 1 | `auto` |
| `advance` | Number || 1 | `1` |
| [`BoneyardUnlocked`](./Miscellaneous.md#object-boneyardunlocked) | Object  | Unlocks an exit route to the Boneyard on the map. | 1 | `{ . . . }` |
| [`BunkerUnlocked`](./Miscellaneous.md#object-bunkerunlocked) | Object  | Unlocks an exit route to the Bunker on the map. | 1 | `{ . . . }` |
| [`cancreeper`](./Enums.md#enum-cancreeper) | Enum || 1 | `auto` |
| [`cavecatfamily`](./Enums.md#enum-cavecatfamily) | Enum || 1 | `auto` |
| [`CavesUnlocked`](./Miscellaneous.md#object-cavesunlocked) | Object  | Unlocks an exit route to the Caves on the map. | 1 | `{ . . . }` |
| [`cerberubs`](./Enums.md#enum-cerberubs) | Enum || 1 | `auto` |
| [`ChaosAntennaAttached`](./Miscellaneous.md#object-chaosantennaattached) | Object  | Configures the map event and art when the Chaos Antenna has been attached. | 1 | `{ . . . }` |
| [`clericcat`](./Enums.md#enum-clericcat) | Enum || 1 | `auto` |
| [`CoreUnlocked`](./Miscellaneous.md#object-coreunlocked) | Object  | Unlocks an exit route to the Core on the map. | 1 | `{ . . . }` |
| [`CraterUnlocked`](./Miscellaneous.md#object-craterunlocked) | Object  | Unlocks an exit route to the Crater on the map. | 1 | `{ . . . }` |
| [`dinocouple`](./Enums.md#enum-dinocouple) | Enum || 1 | `auto` |
| [`drmangler`](./Enums.md#enum-drmangler) | Enum || 1 | `auto` |
| [`druidcat`](./Enums.md#enum-druidcat) | Enum || 1 | `auto` |
| [`exit_desert`](./Miscellaneous.md#object-exit_desert) | Object  || 1 | `{ . . . }` |
| [`exit_lab`](./Miscellaneous.md#object-exit_lab) | Object  || 1 | `{ . . . }` |
| [`FutureUnlocked`](./Miscellaneous.md#object-futureunlocked) | Object  | Configures the map event and art when the Future is unlocked. | 1 | `{ . . . }` |
| [`GenFlag_Boss_Spewer`](./Miscellaneous.md#object-genflag_boss_spewer) | Object  | Configures the boss encounter event for the Spewer boss on the map. | 1 | `{ . . . }` |
| [`GenFlag_Boss_Stacy`](./Miscellaneous.md#object-genflag_boss_stacy) | Object  | Configures the miniboss and boss encounter events for the Stacy Mutant boss on the map. | 1 | `{ . . . }` |
| `head_start` | Number || 1 | `99` |
| [`home`](./Miscellaneous.md#object-home) | Object  || 1 | `{ . . . }` |
| [`huntercat`](./Enums.md#enum-huntercat) | Enum || 1 | `auto` |
| [`IceAgeUnlocked`](./Miscellaneous.md#object-iceageunlocked) | Object  | Configures the map event and art when Ice Age is unlocked. | 1 | `{ . . . }` |
| [`iceelemental`](./Enums.md#enum-iceelemental) | Enum || 1 | `auto` |
| [`infestedduo`](./Enums.md#enum-infestedduo) | Enum || 1 | `auto` |
| [`JunkyardUnlocked`](./Miscellaneous.md#object-junkyardunlocked) | Object  | Unlocks an exit route to the Junkyard on the map. | 1 | `{ . . . }` |
| [`JurassicUnlocked`](./Miscellaneous.md#object-jurassicunlocked) | Object  | Unlocks an exit route to the Jurassic area on the map. | 1 | `{ . . . }` |
| [`lenny`](./Enums.md#enum-lenny) | Enum || 1 | `auto` |
| [`lightningelemental`](./Enums.md#enum-lightningelemental) | Enum || 1 | `auto` |
| `locked` | Boolean || 1 | `false`<br>`true` |
| [`mamamaggot`](./Enums.md#enum-mamamaggot) | Enum || 1 | `auto` |
| [`MeatWorldUnlockedFull`](./Miscellaneous.md#object-meatworldunlockedfull) | Object  | Unlocks hidden battle and hard nodes within the MeatWorld area on the map. | 1 | `{ . . . }` |
| [`miniboss_event`](./Miscellaneous.md#object-miniboss_event) | Object  | An object defining the properties of a mini-boss event at this node. | 1 | `{ . . . }` |
| [`MoonUnlocked`](./Miscellaneous.md#object-moonunlocked) | Object  | Unlocks an exit route to the Moon on the map. | 1 | `{ . . . }` |
| [`musiclayer`](./Enums.md#enum-musiclayer) | Enum || 1 | `boss` |
| [`mw_altar`](./Miscellaneous.md#object-mw_altar) | Object  || 1 | `{ . . . }` |
| [`mw_battle1`](./Miscellaneous.md#object-mw_battle1) | Object  | An object defining the properties of the first MeatWorld battle node. | 1 | `{ . . . }` |
| [`mw_boss`](./Miscellaneous.md#object-mw_boss) | Object  | An object defining the properties of the MeatWorld boss node. | 1 | `{ . . . }` |
| [`mw_earlyhome`](./Miscellaneous.md#object-mw_earlyhome) | Object  | An object defining the properties of the MeatWorld early home node. | 1 | `{ . . . }` |
| [`mw_event1`](./Miscellaneous.md#object-mw_event1) | Object  | An object defining the properties of the first MeatWorld event node. | 1 | `{ . . . }` |
| [`mw_hard1`](./Miscellaneous.md#object-mw_hard1) | Object  | An object defining the properties of the first MeatWorld hard path node. | 1 | `{ . . . }` |
| [`mw_home`](./Miscellaneous.md#object-mw_home) | Object  | An object defining the properties of the MeatWorld home node. | 1 | `{ . . . }` |
| [`mw_quest_event`](./Miscellaneous.md#object-mw_quest_event) | Object  | An object defining the properties of the MeatWorld quest event node. | 1 | `{ . . . }` |
| [`mw_treasure`](./Miscellaneous.md#object-mw_treasure) | Object  | An object defining the properties of the MeatWorld treasure node. | 1 | `{ . . . }` |
| [`ratking`](./Enums.md#enum-ratking) | Enum || 1 | `auto` |
| [`rockybobo`](./Enums.md#enum-rockybobo) | Enum || 1 | `auto` |
| [`SewersUnlocked`](./Miscellaneous.md#object-sewersunlocked) | Object  | Unlocks an exit route to the Sewers on the map. | 1 | `{ . . . }` |
| [`shop_cheapwater`](./Miscellaneous.md#object-shop_cheapwater) | Object  || 1 | `{ . . . }` |
| [`shop_water`](./Miscellaneous.md#object-shop_water) | Object  || 1 | `{ . . . }` |
| [`slime`](./Enums.md#enum-slime) | Enum || 1 | `auto` |
| [`spawn_node`](./Enums.md#enum-spawn_node) | Enum || 1 | `start` |
| [`stacy`](./Enums.md#enum-stacy) | Enum || 1 | `auto` |
| [`tankcat`](./Enums.md#enum-tankcat) | Enum || 1 | `auto` |
| [`thebloat`](./Enums.md#enum-thebloat) | Enum || 1 | `auto` |
| [`TheEndUnlocked`](./Miscellaneous.md#object-theendunlocked) | Object  | An object that stores flags related to unlocking the 'The End' chapter. | 1 | `{ . . . }` |
| [`ThrobbingArteryDone`](./Miscellaneous.md#object-throbbingarterydone) | Object  | An object that stores flags related to completing the Throbbing Artery quest. | 1 | `{ . . . }` |
| [`trampy`](./Enums.md#enum-trampy) | Enum || 1 | `auto` |
| [`WallOfFleshDone`](./Miscellaneous.md#object-walloffleshdone) | Object  | An object that stores flags related to completing the Wall of Flesh quest. | 1 | `{ . . . }` |
| [`weather_event`](./Miscellaneous.md#object-weather_event) | Object  || 1 | `{ . . . }` |
| [`choose_one`](./Arrays.md#array-choose_one) | Array || 1 | `[GenFlag_Boss_Stacy, GenFlag_Boss_Spewer]` |
| [`nemesis`](./Arrays.md#array-nemesis) | Array || 1 | `[nemesis]` |
| :--- | :--- | :--- | :--- | :--- |

</details>
---

### Object: `boss`


**Definition:** No definition provided.  
**Total Count:** 41


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`GenFlag_Boss_Spewer`](./Map_Generation_and_Routing.md#context-genflag_boss_spewer), [`GenFlag_Boss_Stacy`](./Map_Generation_and_Routing.md#context-genflag_boss_stacy), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 19 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`boss_cutscene`](./Enums.md#enum-boss_cutscene) | Enum || 16 | `alienqueen`<br>`coven`<br>`dybbuk` |
| `is_final_boss` | Boolean || 2 | `true` |
| [`level`](./Enums.md#enum-level) | Enum || 2 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| [`override_music`](./Enums.md#enum-override_music) | Enum || 2 | `chaos_boss`<br>`finalboss`<br>`throbbingking` |
| [`tileset`](./Enums.md#enum-tileset) | Enum || 1 | `finalboss` |
| [`unlockcheck_on_complete`](./Enums.md#enum-unlockcheck_on_complete) | Enum || 1 | `map_unlock_junkyard` |

</details>
---

### Object: `exit0`


**Definition:** No definition provided.  
**Total Count:** 27


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BoneyardUnlocked`](./Map_Generation_and_Routing.md#context-boneyardunlocked), [`BunkerUnlocked`](./Map_Generation_and_Routing.md#context-bunkerunlocked), [`CavesUnlocked`](./Map_Generation_and_Routing.md#context-cavesunlocked), [`CoreUnlocked`](./Map_Generation_and_Routing.md#context-coreunlocked), [`EndOfTimeUnlocked`](./Map_Generation_and_Routing.md#context-endoftimeunlocked), [`JurassicUnlocked`](./Map_Generation_and_Routing.md#context-jurassicunlocked), [`MeatWorldUnlocked`](./Map_Generation_and_Routing.md#context-meatworldunlocked), [`MoonUnlocked`](./Map_Generation_and_Routing.md#context-moonunlocked), [`ROOT`](./Map_Generation_and_Routing.md#context-root), [`SewersUnlocked`](./Map_Generation_and_Routing.md#context-sewersunlocked), [`TheEndUnlocked`](./Map_Generation_and_Routing.md#context-theendunlocked)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `locked` | Boolean || 17 | `false`<br>`true` |
| [`next_map`](./Enums.md#enum-next_map) | Enum || 15 | `bunker.gon`<br>`core.gon`<br>`crater.gon` |
| [`override_art`](./Enums.md#enum-override_art) | Enum || 15 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 15 | `[attack move spell]`<br>`attack`<br>`battle` |
| `hidden` | Boolean || 10 | `false`<br>`true` |

</details>
---

### Object: `quest_event`


**Definition:** No definition provided.  
**Total Count:** 24


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BothObelisksUnlocked`](./Map_Generation_and_Routing.md#context-bothobelisksunlocked), [`ChaosAntennaAttached`](./Map_Generation_and_Routing.md#context-chaosantennaattached), [`CoreObeliskUnlocked`](./Map_Generation_and_Routing.md#context-coreobeliskunlocked), [`DimensionXUnlocked`](./Map_Generation_and_Routing.md#context-dimensionxunlocked), [`FutureUnlocked`](./Map_Generation_and_Routing.md#context-futureunlocked), [`IceAgeUnlocked`](./Map_Generation_and_Routing.md#context-iceageunlocked), [`MeatWorldUnlocked`](./Map_Generation_and_Routing.md#context-meatworldunlocked), [`MoonObeliskUnlocked`](./Map_Generation_and_Routing.md#context-moonobeliskunlocked), [`ROOT`](./Map_Generation_and_Routing.md#context-root), [`ThrobbingArteryDone`](./Map_Generation_and_Routing.md#context-throbbingarterydone), [`VolcanoAntennaAttached`](./Map_Generation_and_Routing.md#context-volcanoantennaattached), [`WallOfFleshDone`](./Map_Generation_and_Routing.md#context-walloffleshdone)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`override_art`](./Enums.md#enum-override_art) | Enum || 24 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |
| [`level`](./Enums.md#enum-level) | Enum || 19 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 11 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>
---

### Object: `exit1`


**Definition:** No definition provided.  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CraterUnlocked`](./Map_Generation_and_Routing.md#context-craterunlocked), [`JunkyardUnlocked`](./Map_Generation_and_Routing.md#context-junkyardunlocked), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `locked` | Boolean || 5 | `false`<br>`true` |
| [`next_map`](./Enums.md#enum-next_map) | Enum || 3 | `bunker.gon`<br>`core.gon`<br>`crater.gon` |
| [`override_art`](./Enums.md#enum-override_art) | Enum || 3 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 3 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>
---

### Object: `hard_initial`


**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`HardPathUnlocked`](./Map_Generation_and_Routing.md#context-hardpathunlocked), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `locked` | Boolean || 4 | `false`<br>`true` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 2 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>
---

### Object: `time_machine`


**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum || 4 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| [`override_art`](./Enums.md#enum-override_art) | Enum || 4 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 4 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>
---

### Object: `BothObelisksUnlocked`


**Definition:** No definition provided.  
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


**Definition:** No definition provided.  
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


**Definition:** No definition provided.  
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


**Definition:** No definition provided.  
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


**Definition:** No definition provided.  
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


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`GenFlag_Boss_Stacy`](./Map_Generation_and_Routing.md#context-genflag_boss_stacy), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 2 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`level`](./Enums.md#enum-level) | Enum || 1 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |

</details>
---

### Object: `mw_battle1`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean || 2 | `false`<br>`true` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>
---

### Object: `mw_boss`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean || 2 | `false`<br>`true` |
| [`boss_cutscene`](./Enums.md#enum-boss_cutscene) | Enum || 1 | `alienqueen`<br>`coven`<br>`dybbuk` |
| [`override_music`](./Enums.md#enum-override_music) | Enum || 1 | `chaos_boss`<br>`finalboss`<br>`throbbingking` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>
---

### Object: `mw_earlyhome`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean || 1 | `false`<br>`true` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>
---

### Object: `mw_event1`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean || 2 | `false`<br>`true` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>
---

### Object: `mw_hard1`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean || 2 | `false`<br>`true` |
| [`musiclayer`](./Enums.md#enum-musiclayer) | Enum || 1 | `boss` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>
---

### Object: `mw_home`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean || 2 | `false`<br>`true` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>
---

### Object: `mw_quest_event`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean || 2 | `false`<br>`true` |
| [`level`](./Enums.md#enum-level) | Enum || 1 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| [`override_art`](./Enums.md#enum-override_art) | Enum || 1 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>
---

### Object: `mw_treasure`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean || 2 | `false`<br>`true` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>
---

### Object: `VolcanoAntennaAttached`


**Definition:** No definition provided.  
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


**Definition:** No definition provided.  
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


**Definition:** No definition provided.  
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


**Definition:** No definition provided.  
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


**Definition:** No definition provided.  
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


**Definition:** No definition provided.  
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


**Definition:** No definition provided.  
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


**Definition:** No definition provided.  
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


**Definition:** No definition provided.  
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


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean || 1 | `true` |

</details>
---

### Object: `endoftime`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean || 1 | `true` |

</details>
---

### Object: `event`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum || 1 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>
---

### Object: `exit_desert`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean || 1 | `false`<br>`true` |
| `locked` | Boolean || 1 | `false`<br>`true` |
| [`next_map`](./Enums.md#enum-next_map) | Enum || 1 | `bunker.gon`<br>`core.gon`<br>`crater.gon` |
| [`override_art`](./Enums.md#enum-override_art) | Enum || 1 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>
---

### Object: `exit_lab`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean || 1 | `false`<br>`true` |
| `locked` | Boolean || 1 | `false`<br>`true` |
| [`next_map`](./Enums.md#enum-next_map) | Enum || 1 | `bunker.gon`<br>`core.gon`<br>`crater.gon` |
| [`override_art`](./Enums.md#enum-override_art) | Enum || 1 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>
---

### Object: `future`


**Definition:** Event Node: Story branch or dialog option representing the 'Future' action.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean || 1 | `true` |

</details>
---

### Object: `FutureUnlocked`


**Definition:** No definition provided.  
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


**Definition:** No definition provided.  
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


**Definition:** No definition provided.  
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


**Definition:** No definition provided.  
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


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean || 1 | `true` |

</details>
---

### Object: `IceAgeUnlocked`


**Definition:** No definition provided.  
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


**Definition:** No definition provided.  
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


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean || 1 | `true` |

</details>
---

### Object: `JurassicUnlocked`


**Definition:** No definition provided.  
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


**Definition:** No definition provided.  
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


**Definition:** No definition provided.  
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


**Definition:** No definition provided.  
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


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum || 1 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| [`override_art`](./Enums.md#enum-override_art) | Enum || 1 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>
---

### Object: `SewersUnlocked`


**Definition:** No definition provided.  
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


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum || 1 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| [`override_art`](./Enums.md#enum-override_art) | Enum || 1 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>
---

### Object: `shop_water`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum || 1 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| [`override_art`](./Enums.md#enum-override_art) | Enum || 1 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>
---

### Object: `start`


**Definition:** No definition provided.  
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


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean || 1 | `true` |

</details>
---

### Object: `TheEndUnlocked`


**Definition:** No definition provided.  
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


**Definition:** No definition provided.  
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


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum || 1 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>
---

### Object: `WallOfFleshDone`


**Definition:** No definition provided.  
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


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum || 1 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
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