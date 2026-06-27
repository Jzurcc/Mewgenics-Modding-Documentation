# Mewgenics Mod Developer Documentation: Engine: Event Keys

> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

## Engine: Event Keys

This document defines the schema shared by all Event Node blocks (`good`, `bad`, `main`, `reward`, `common`, `rare`). Each key in these blocks defines what happens as part of that event outcome.

> **Referenced by:** [`reward` (Events_and_Encounters)](./Events_and_Encounters.md#context-reward), [`common` (Events_and_Encounters)](./Events_and_Encounters.md#context-common), [`rare` (Events_and_Encounters)](./Events_and_Encounters.md#context-rare), [`good` (Events_and_Encounters)](./Events_and_Encounters.md#context-good), [`bad` (Events_and_Encounters)](./Events_and_Encounters.md#context-bad), [`main` (Events_and_Encounters)](./Events_and_Encounters.md#context-main), [`reward` (Miscellaneous)](./Miscellaneous.md#context-reward), [`common` (Miscellaneous)](./Miscellaneous.md#context-common), [`rare` (Miscellaneous)](./Miscellaneous.md#context-rare)

### Valid Property Keys

<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`common`](./Enums.md#enum-common) | Enum | Defines the common reward block for a boss encounter. | 1067 | `100`<br>`14`<br>`5` |
| [`rare`](./Enums.md#enum-rare) | Enum | Defines the rare reward block for a boss encounter. | 673 | `1`<br>`10`<br>`15` |
| [`cha`](./Enums.md#enum-cha) | Enum / Integer  | The Charisma stat value or modifier. | 468 | `+1`<br>`-1`<br>`-2` |
| [`spd`](./Enums.md#enum-spd) | Enum / Integer  | The Speed stat value or modifier. | 424 | `-1`<br>`-10`<br>`-2` |
| [`con`](./Enums.md#enum-con) | Enum / Integer  | The Constitution stat value or modifier. | 416 | `-1`<br>`-2`<br>`-3` |
| [`dex`](./Enums.md#enum-dex) | Enum / Integer  | The Dexterity stat value or modifier. | 301 | `-1`<br>`-2`<br>`-3` |
| [`main`](./Miscellaneous.md#object-main) | Object  | An object containing the primary prompt and options for an event. | 214 | `{ . . . }` |
| [`options`](./Arrays.md#array-options) | Array | An array of named option objects within an event, each defining a possible action the player can take. | 210 | `[smash bash open]` |
| [`play_animation`](./Enums.md#enum-play_animation) | Enum | Specifies an animation to play, optionally as an array with a probability weight. | 160 | `[resultBlessing .5]`<br>`[resultGood .5]`<br>`[resultLeave 0]` |
| `cursed` | Boolean | If true, the item is cursed and may have negative effects when equipped or used. | 154 | `true` |
| `parasite` | Boolean | If true, the item is a parasite that attaches to a unit and cannot be removed normally. | 102 | `true` |
| [`complete_chapter`](./Enums.md#enum-complete_chapter) | Enum | Specifies which chapter to mark as completed when this event triggers. | 90 | `alley`<br>`boneyard`<br>`bunker` |
| [`gain_disorder`](./Enums.md#enum-gain_disorder) | Enum | Specifies a disorder to add to the current cat when this event triggers. | 85 | `AcidReflux`<br>`Albinism`<br>`Anxiety` |
| `auto` | Variable | A variable that indicates an automatic or default behavior, often for AI decision-making. | 82 ||
| [`random_pool`](./Arrays.md#array-random_pool) | Array | An array of possible items or rewards from which one is randomly selected. | 79 | `[` |
| [`increment_legacy_counter`](./Enums.md#enum-increment_legacy_counter) | Enum | Specifies a legacy counter to increment by one when this event triggers. | 67 | `WorldEventLegacyCounter_CrackInTheWall`<br>`WorldEventLegacyCounter_CustomTokenString`<br>`WorldEventLegacyCounter_FooCounter` |
| [`event_now_same_cat`](./Enums.md#enum-event_now_same_cat) | Enum | Specifies a world event that will now occur for the same cat category as the current event. | 63 | `BigToe`<br>`Blessing`<br>`BodyOfGlorg_Gift` |
| [`get_item`](./Enums.md#enum-get_item) | Enum | Specifies an item to add to the player's inventory when this event triggers. | 61 | `AlienBlaster`<br>`BagOfGrass`<br>`BearTrapMask` |
| [`set_adventure_token`](./Enums.md#enum-set_adventure_token) | Enum | Specifies an adventure token to set (enable or mark as true) when this event triggers. | 52 | `AdventureToken_BlueNeedle`<br>`AdventureToken_HasRunFromDeath`<br>`AdventureToken_HasTakenNeedle` |
| `WorldEventLegacyCounter_Jack` | Variable | A legacy counter tracking the number of times a specific event related to 'Jack' has occurred. | 50 ||
| [`clear_adventure_token`](./Enums.md#enum-clear_adventure_token) | Enum | Specifies an adventure token to clear (disable or mark as false) when this event triggers. | 48 | `AdventureToken_BlueNeedle`<br>`AdventureToken_HasTakenNeedle`<br>`AdventureToken_RedNeedle` |
| [`gain_coins`](./Arrays.md#array-gain_coins) | Array | An array specifying the minimum and maximum amount of coins gained, or a single integer. | 47 | `1`<br>`10`<br>`15` |
| [`get_parasite`](./Enums.md#enum-get_parasite) | Enum | Specifies a parasite item to attach to a unit when this event triggers. | 41 | `AlluringDoodie`<br>`BadSplinters`<br>`Beepis` |
| [`spawn_unit_next_fight`](./Miscellaneous.md#object-spawn_unit_next_fight) | Object  | An object defining a unit to spawn during the next fight, including its object, count, and spawn side. | 40 | `{ . . . }` |
| [`prompt`](./Enums.md#enum-prompt) | String | The text or localization key for the popup or prompt displayed to the player. | 38 | `"Donate 3 times before you can receive a reward!"`<br>`"EVENT_ABEGGAR_LEAVE"`<br>`"EVENT_ABEGGAR_QUES"` |
| `set_frame` | Integer | The specific animation frame to set for an object or UI element. | 36 | `1`<br>`10`<br>`15` |
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum | Specifies a legacy token to set (enable or mark as true) when this event triggers. | 36 | `AlienOvergrowthUnlocked`<br>`AntennaQuest_Orb`<br>`AntennaQuest_Rift` |
| `resultHole` | Variable | A variable representing the result of an action that creates a hole or opening on the map. | 32 ||
| [`gain_food`](./Arrays.md#array-gain_food) | Array | An array specifying the minimum and maximum amount of food gained, or a single integer. | 28 | `-5`<br>`20`<br>`30` |
| [`dimensionx`](./Enums.md#enum-dimensionx) | Enum | An enum specifying the Dimension X chapter area, or an object with its specific properties. | 27 | `400`<br>`AREA_NAME_DIMENSIONX`<br>`[moon core bunker crater desert]` |
| [`party_damage`](./Arrays.md#array-party_damage) | Array | An array specifying the minimum and maximum damage dealt to the party, or a single integer or percentage. | 26 | `1`<br>`10`<br>`2` |
| [`meatworld`](./Enums.md#enum-meatworld) | Enum | An enum specifying the Meatworld chapter area, or an object with its specific properties. | 24 | `300`<br>`AREA_NAME_MEATWORLD`<br>`[caves boneyard junkyard sewers alley]` |
| [`party_status_next_fight`](./Miscellaneous.md#object-party_status_next_fight) | Object  | An object defining status effects to apply to the party at the start of the next fight. | 23 | `{ . . . }` |
| [`setup`](./Miscellaneous.md#object-setup) | Object  | Defines actions or checks to run before the main event logic, often setting up conditions or tokens. | 23 | `{ . . . }` |
| `override_end_option_prompt` | String | Specifies a custom prompt string to display for the end option of this event choice. | 21 | `"EVENT_LOCKEDDOOR_PROMPT1"`<br>`"EVENT_LOCKEDDOOR_PROMPT2"`<br>`"EVENT_MYSTERIOUSSTRANGER_END_AGAIN"` |
| [`random_mutation_from_set`](./Miscellaneous.md#object-random_mutation_from_set) | Object  | Defines a set of mutation categories and their specific IDs to apply a random mutation from. | 21 | `{ . . . }` |
| [`boneyard`](./Enums.md#enum-boneyard) | Enum | Specifies the name, map flag, or connection for the Boneyard area. | 21 | `200`<br>`AREA_NAME_BONEYARD`<br>`[junkyard alley]` |
| [`bunker`](./Enums.md#enum-bunker) | Enum | Specifies the name, map flag, or connection for the Bunker area. | 20 | `AREA_NAME_BUNKER`<br>`[desert]`<br>`mapflag_BunkerUnlocked` |
| [`core`](./Enums.md#enum-core) | Enum | Specifies the name, map flag, or connection for the Core area. | 20 | `300`<br>`AREA_NAME_CORE`<br>`[bunker desert]` |
| [`moon`](./Enums.md#enum-moon) | Enum | Specifies the name, map flag, or connection for the Moon area. | 20 | `300`<br>`AREA_NAME_MOON`<br>`[crater desert]` |
| `AdventureToken_HasTakenNeedle` | Variable | A token flag that tracks if the player has taken the needle in the associated adventure. | 18 ||
| [`complete_item_quest`](./Enums.md#enum-complete_item_quest) | Enum | Marks the specified item quest as completed. | 18 | `BlackShard`<br>`CryogenicTimeChamber_Empty`<br>`CryogenicTimeChamber_Full` |
| [`alley`](./Enums.md#enum-alley) | Enum | Specifies the name, map flag, or connection for the Alley area. | 18 | `AREA_NAME_ALLEY`<br>`[]`<br>`departed_first_real_adventure` |
| `ambush_next_basic_fights` | Integer | The number of basic fights to trigger as ambushes. | 17 | `1` |
| [`event_now`](./Enums.md#enum-event_now) | Enum | Triggers the specified event immediately. | 17 | `MeatGolem`<br>`Mirage`<br>`MysteriousMachine_Bad` |
| `full_heal` | Integer | If set to 1, fully restores the unit's health. | 16 | `1` |
| [`crater`](./Enums.md#enum-crater) | Enum | Specifies the name, map flag, or connection for the Crater area. | 16 | `AREA_NAME_CRATER`<br>`[desert]`<br>`mapflag_CraterUnlocked` |
| [`desert`](./Enums.md#enum-desert) | Enum | Specifies the name, map flag, or connection for the Desert area. | 16 | `AREA_NAME_DESERT`<br>`[]`<br>`mapflag_DesertUnlocked` |
| [`future`](./Enums.md#enum-future) | Enum | Specifies the name, map flag, or connection for the Future area. | 16 | `AREA_NAME_FUTURE`<br>`[lab]`<br>`mapflag_FutureUnlocked` |
| [`sewers`](./Enums.md#enum-sewers) | Enum | Specifies the name, map flag, or connection for the Sewers area. | 16 | `AREA_NAME_SEWERS`<br>`[alley]`<br>`mapflag_SewersUnlocked` |
| [`StatusEachTurnBegin`](./Passives_and_Statuses.md#object-statuseachturnbegin) | Object  | Specifies status effects applied to the unit at the start of each of its turns. | 16 | `{ . . . }` |
| [`kill`](./Enums.md#enum-kill) | Enum | Kills the specified target type (e.g., 'cat'). | 15 | `cat` |
| `AdventureToken_BlueNeedle` | Variable | A token flag that tracks the blue needle in the associated adventure. | 14 ||
| `AdventureToken_RedNeedle` | Variable | A token flag that tracks the red needle in the associated adventure. | 14 ||
| [`lose_item`](./Enums.md#enum-lose_item) | Enum | Specifies which item slot or type to lose (e.g., 'equipped', 'inventory'). | 14 | `equipped`<br>`inventory`<br>`parasite` |
| [`iceage`](./Enums.md#enum-iceage) | Enum | Specifies the name, map flag, or connection for the Ice Age area. | 14 | `AREA_NAME_ICEAGE`<br>`[lab]`<br>`mapflag_IceAgeUnlocked` |
| [`jurassic`](./Enums.md#enum-jurassic) | Enum | Specifies the name, map flag, or connection for the Jurassic area. | 14 | `400`<br>`AREA_NAME_JURASSIC`<br>`[iceage lab]` |
| [`lab`](./Enums.md#enum-lab) | Enum | Specifies the name, map flag, or connection for the Lab area. | 14 | `AREA_NAME_LAB`<br>`[]`<br>`mapflag_LabUnlocked` |
| [`theend`](./Enums.md#enum-theend) | Enum | Specifies the name, map flag, or connection for The End area. | 14 | `400`<br>`AREA_NAME_THEEND`<br>`[future lab]` |
| [`shop_now`](./Enums.md#enum-shop_now) | Enum | Triggers the specified shop to appear immediately. | 13 | `Event_RareShop`<br>`Event_SmallShop`<br>`Shop` |
| [`trigger_adventure_unlock`](./Enums.md#enum-trigger_adventure_unlock) | Enum | Triggers the specified adventure or map unlock quest. | 13 | `end_of_time_unlock`<br>`legacy_event_unlock_momsknife`<br>`map_unlock_dimensionx` |
| `all_disorders` | Variable | A variable or constant representing all possible disorders. | 12 ||
| [`begin_chapter`](./Enums.md#enum-begin_chapter) | Enum | Specifies the chapter file to begin, transitioning to that chapter. | 12 | `dimensionx.gon`<br>`endoftime.gon`<br>`future.gon` |
| [`lose_specific_item`](./Enums.md#enum-lose_specific_item) | Enum | Removes the specified item from the player's inventory. | 12 | `CryogenicTimeChamber_Full`<br>`PutridLeech`<br>`PyrophinasCollar` |
| `current_chapter_common` | Variable | A variable controlling the number of common item drops for the current chapter. | 12 | `55`<br>`auto` |
| `current_chapter_rare` | Variable | A variable controlling the number of rare item drops for the current chapter. | 12 | `10`<br>`auto` |
| [`caves`](./Enums.md#enum-caves) | Enum | Specifies the name, map flag, or connection for the Caves area. | 12 | `200`<br>`AREA_NAME_CAVES`<br>`[sewers alley]` |
| [`junkyard`](./Enums.md#enum-junkyard) | Enum | Specifies the name, map flag, or connection for the Junkyard area. | 12 | `AREA_NAME_JUNKYARD`<br>`[alley]`<br>`mapflag_JunkyardUnlocked` |
| [`get_item_from_pool`](./Enums.md#enum-get_item_from_pool) | Enum | Grants an item from the specified pool or a specific item name. | 11 | `Bird_items`<br>`Coin_items`<br>`Eye_items` |
| [`CharmedMaggot`](./Engine_EventKeys.md#object-charmedmaggot) | Object  | Defines a variant of the Maggot familiar with a green tint. | 11 | `{ . . . }` |
| [`food`](./Arrays.md#array-food) | Array | The range [min, max] of food items dropped. | 11 | `[1 3]`<br>`[10 15]`<br>`[2 5]` |
| [`cat`](Characters_and_Bosses.md#object-cat) | Variable | A variable or constant representing the 'cat' type. | 10 ||
| [`global_effect_next_fight`](./Miscellaneous.md#object-global_effect_next_fight) | Object  | Defines a global status effect or modifier to apply in the next fight. | 10 | `{ . . . }` |
| `HasPlayedMysteriousStranger` | Variable | A token flag that tracks if the Mysterious Stranger event has been played. | 10 ||
| [`learn_passive`](./Enums.md#enum-learn_passive) | Enum | Teaches the unit the specified passive ability. | 10 | `Blessed`<br>`CobraStyle`<br>`DeathProof` |
| [`set_subject`](./Enums.md#enum-set_subject) | Enum | Specifies which subject or frame to use for the event's visual. | 10 | `dimensionx_head2`<br>`endorb2`<br>`monkey_paw_1finger` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 10 | `{ . . . }` |
| [`weight`](./Enums.md#enum-weight) | Float | A multiplier or priority value for random selection or effect magnitude. | 10 | `.25`<br>`.5`<br>`1` |
| `chapter_rare` | Number | An integer or variable controlling the number of rare item drops for the current chapter. | 10 | `1` |
| [`good`](#good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 8 | `false`<br>`true` |
| `parasites` | Variable | A variable or constant representing parasites. | 8 ||
| `party_random_mutation` | Integer | The number of random mutations applied to the entire party. | 8 | `1` |
| [`permanent_stats`](./Miscellaneous.md#object-permanent_stats) | Object  | Defines permanent stat changes to apply to the unit (e.g., con, cha). | 7 | `{ . . . }` |
| `heal_disorder` | Integer | Specifies which disorder type to heal, or the number of disorders to heal. | 7 | `1`<br>`2`<br>`Anxiety` |
| [`leave_party_temporarily`](./Miscellaneous.md#object-leave_party_temporarily) | Object  | Defines parameters for a unit leaving the party temporarily, such as skipped fights and return conditions. | 7 | `{ . . . }` |
| [`next_event_from_set`](./Enums.md#enum-next_event_from_set) | Enum | Specifies the next event to trigger, or defines a set of events with count and category constraints. | 7 | `CatHole`<br>`Tragedy`<br>`WatchingHead2` |
| `chapter_common` | Number | The weight or probability for this entry to appear in the common loot pool for its chapter. | 7 | `1` |
| `consumables` | Number | The number of consumable items provided or available in this context. | 6 | `10`<br>`60` |
| [`decrement_legacy_counter`](./Enums.md#enum-decrement_legacy_counter) | Enum | Specifies which legacy counter or token to decrement by one. | 6 | `WorldEventLegacyCounter_CrackInTheWall`<br>`WorldEventLegacyCounter_CustomTokenString`<br>`WorldEventLegacyToken_StartDigging` |
| `hide_appearance_changes` | Integer | If set to 1, visual appearance changes from status effects or mutations are not shown on the unit. | 6 | `1` |
| `QEVENT_OBELISK_IGNORE` | Variable | A variable flag indicating the player chose to ignore or skip the Obelisk event. | 6 ||
| `QEVENT_OBELISK_REW1` | Variable | A variable flag indicating the first reward choice from the Obelisk event was selected. | 6 ||
| `QEVENT_OBELISK_REW2` | Variable | A variable flag indicating the second reward choice from the Obelisk event was selected. | 6 ||
| `QEVENT_OBELISK_REW3` | Variable | A variable flag indicating the third reward choice from the Obelisk event was selected. | 6 ||
| `QEVENT_OBELISK_REW4` | Variable | A variable flag indicating the fourth reward choice from the Obelisk event was selected. | 6 ||
| [`Stinky`](#object-stinky) | Variable | A named object definition for the 'Stinky' disorder, containing its display name, description, class, and passive effects. | 6 ||
| `WorldEventLegacyCounter_CrackInTheWall` | Variable | A variable tracking the number of times the 'CrackInTheWall' world event has occurred or been interacted with. | 6 ||
| `WorldEventLegacyToken_StartDigging` | Variable | A variable flag that, when set, allows the 'StartDigging' legacy action to trigger. | 6 ||
| [`chapter`](./Enums.md#enum-chapter) | Enum | Specifies which chapter or scenario this ability is available in. | 6 | `1`<br>`alley` |
| [`JarOfRadiation`](./Engine_EventKeys.md#object-jarofradiation) | Object  | An object definition for the 'Jar of Radiation' item or status, containing its properties and effects. | 6 | `{ . . . }` |
| [`reward`](./Miscellaneous.md#object-reward) | Object  | An object containing sub-objects defining the rewards for different rarity tiers (e.g., common, rare), each with their own set of actions and items. | 5 | `{ . . . }` |
| [`add_weather`](./Enums.md#enum-add_weather) | Enum | Specifies a weather effect type to apply to the current map. | 5 | `AlienOvergrowth`<br>`Birdemic`<br>`GeomagneticStorm` |
| `blood_altar_items` | Variable | A variable list or pool of items that can be received from a blood altar event. | 5 ||
| [`cutscene_on_exit`](./Enums.md#enum-cutscene_on_exit) | Enum | Determines which cutscene to play when the player leaves the current location. | 5 | `infinite_intro`<br>`king_intro` |
| `physical_disorders` | Variable | A variable list or pool of physical disorder definitions that can be applied or referenced. | 5 ||
| [`SlagTight`](./Engine_EventKeys.md#object-slagtight) | Object  | An object definition for the 'SlagTight' entity or item, containing its properties and effects. | 5 | `{ . . . }` |
| [`requires_flag`](./Enums.md#enum-requires_flag) | Enum | Specifies a named flag that must be unlocked or set for this event or option to appear. | 5 | `GeomagneticStormUnlocked`<br>`MeteorShowerUnlocked`<br>`SolarFlareUnlocked` |
| `diseases` | Variable | A variable list or pool of disease definitions that can be applied or referenced. | 4 ||
| `fleshhead_items` | Variable | A variable list or pool of items associated with the Fleshhead event or vendor. | 4 ||
| [`goto`](./Enums.md#enum-goto) | Enum | Determines which labeled point in the event's script to jump to next, controlling flow. | 4 | `end` |
| `heal_injury` | Integer | The number of injury points to heal on the target unit. | 4 | `1`<br>`5` |
| `inventory` | Variable | A variable list or pool of inventory item definitions that can be used or referenced. | 4 ||
| [`learn_ability`](./Enums.md#enum-learn_ability) | Enum | Specifies which specific ability the target unit learns. | 4 | `BarfBall`<br>`FutureSight` |
| [`learn_ability_from_pool`](./Arrays.md#array-learn_ability_from_pool) | Array | An array specifying a pool or list of abilities from which one is randomly selected and learned. The string 'AnyUnlocked' selects any unlocked ability. | 4 | `AnyUnlocked`<br>`Necromancer`<br>`[Smack Meow Hiss]` |
| `MysteriousStranger_HasLostFinger` | Variable | A variable flag indicating that the Mysterious Stranger event's 'lost finger' condition has been met. | 4 ||
| [`outcome`](./Miscellaneous.md#object-outcome) | Object  | An object defining the possible outcomes of an event, typically containing a random pool or weighted lists of rewards and animations. | 4 | `{ . . . }` |
| `party_heal_disorder` | Integer | The number of disorders to heal from all party members. | 4 | `2` |
| [`party_permanent_stats_exclude_self`](./Miscellaneous.md#object-party_permanent_stats_exclude_self) | Object  | An object specifying permanent stat bonuses (str, dex, con, int, spd) applied to all party members except the triggering unit. | 4 | `{ . . . }` |
| `QEVENT_THROBBINGARTERY_REW3` | Variable | A variable flag indicating the third reward choice from the Throbbing Artery quest line was selected. | 4 ||
| [`random_pool_consider_luck`](./Arrays.md#array-random_pool_consider_luck) | Array | An array or weighted pool of rewards that are rolled considering the unit's luck stat. | 4 | `[` |
| [`upgrade_ability`](./Enums.md#enum-upgrade_ability) | Enum | Specifies which ability to upgrade. The value 'random' selects a random eligible ability. | 4 | `random` |
| `WorldEventLegacyCounter_ToiletFlushes` | Variable | A variable tracking the number of times the toilet flushing legacy action has occurred. | 4 ||
| [`JarOfRadiatedBlood`](./Engine_EventKeys.md#object-jarofradiatedblood) | Object  | An object definition for the 'Jar of Radiated Blood' item or status, containing its properties and effects. | 4 | `{ . . . }` |
| [`spin`](./Enums.md#enum-spin) | Enum | Specifies an action to re-roll or spin again, such as for a random reward wheel. | 4 | `again` |
| [`JarOfChaos`](./Engine_EventKeys.md#object-jarofchaos) | Object  | An object definition for the 'Jar of Chaos' item or status, containing its properties and effects. | 4 | `{ . . . }` |
| [`gain_familiar`](./Enums.md#enum-gain_familiar) | Enum | Specifies which familiar type (by its class name) the unit gains. | 3 | `CharmedBear`<br>`CharmedDaddyShark`<br>`CharmedDustDevil` |
| `bone_armor` | Variable | A variable list or pool of bone armor definitions that can be applied or referenced. | 3 ||
| `bone_equipment` | Variable | A variable list or pool of bone equipment definitions that can be applied or referenced. | 3 ||
| [`chapter_specific_item`](#object-chapter_specific_item) | Variable | A variable list or pool of items that are unique to the current chapter. | 3 ||
| [`CryogenicTimeChamber_Full`](./Engine_EventKeys.md#object-cryogenictimechamber_full) | Object  | An object definition for the filled 'Cryogenic Time Chamber' entity, containing its properties and effects. | 3 | `{ . . . }` |
| [`end_of_time_unlock`](#object-end_of_time_unlock) | Variable | A variable or object used to set the mapgen flag that unlocks the End of Time area. | 3 ||
| [`learn_passive_from_pool`](./Arrays.md#array-learn_passive_from_pool) | Array | An array specifying a pool or list of passives from which one is randomly selected and learned. The string 'AnyUnlocked' selects any unlocked passive. | 3 | `AnyUnlocked`<br>`Necromancer`<br>`[MiniMe SkillShare]` |
| [`lose_item_from_inventory`](./Enums.md#enum-lose_item_from_inventory) | Enum | Specifies which item or item category is removed from the unit's inventory. | 3 | `cat` |
| [`make_old`](./Enums.md#enum-make_old) | Enum | Applies the 'old' status or age increase to the specified target, typically 'self'. | 3 | `self` |
| `max_options` | Integer | The maximum number of event options presented to the player. | 3 | `2`<br>`3` |
| `mental_disorders` | Variable | A variable list or pool of mental disorder definitions that can be applied or referenced. | 3 ||
| `QEVENT_OBELISK_QUES2` | Variable | A variable flag indicating the second quest choice from the Obelisk event was selected. | 3 ||
| `QEVENT_VOLCANO_REW2` | Variable | Represents the second reward state for the volcano event quest chain. | 3 ||
| `QEVENT_VOLCANO_REW3` | Variable | Represents the third reward state for the volcano event quest chain. | 3 ||
| [`radiated`](#object-radiated) | Variable | Tracks the radiated status or state of an entity. | 3 ||
| [`RestlessDead`](#object-restlessdead) | Variable | Tracks the Restless Dead event or status state. | 3 ||
| `resultVeryGood` | Variable | Represents a very good outcome state for an event result. | 3 ||
| [`Scatological`](#object-scatological) | Variable | Defines the Scatological disorder class with name, description, and passives. | 3 ||
| `shuffle_options` | Boolean | If true, randomizes the order of event options presented to the player. | 3 | `true` |
| [`SlagMight`](./Engine_EventKeys.md#object-slagmight) | Object  | Defines the SlagMight object or ability configuration. | 3 | `{ . . . }` |
| `spawn_reflection_next_fight` | Integer | The number of reflections to spawn in the next battle, optionally with a mutation. | 3 | `1` |
| [`transform_item`](./Arrays.md#array-transform_item) | Array | An array specifying source and destination item IDs to transform one into the other. | 3 | `[JarOfRadiatedBlood JarOfChaos]`<br>`[JarOfRadiation JarOfRadiatedBlood]` |
| [`unlock_item_quest`](./Enums.md#enum-unlock_item_quest) | Enum | Specifies the item whose quest is unlocked or advanced. | 3 | `CryogenicTimeChamber_Empty`<br>`CryogenicTimeChamber_Full`<br>`JarOfChaos` |
| [`upgrade_passive`](./Enums.md#enum-upgrade_passive) | Enum | Specifies which passive ability to upgrade, or 'random' for a random choice. | 3 | `random` |
| [`get_parasite_from_pool`](./Enums.md#enum-get_parasite_from_pool) | Enum | Specifies the pool name or explicit list of parasites to obtain from. | 2 | `[AmoebaHat AmoebaNeck AmoebaFace]`<br>`barbed_armor`<br>`barbed_items` |
| [`battle`](./Math_Equations.md) | Equation | Defines a battle encounter by preset, level file path, or reverb settings. | 2 | `"desert/boss/dustdevil/DustDevil.lvl"`<br>`"events/Death.lvl"`<br>`"events/GlowingBear"` |
| [`level_up`](./Enums.md#enum-level_up) | Enum | Specifies which units to level up, such as 'all' or 'self'. | 2 | `all`<br>`self` |
| [`Bottles`](./Engine_EventKeys.md#object-bottles) | Object  | Defines the Bottles item or object category. | 2 | `{ . . . }` |
| `pills` | Number | The amount of pills granted as a consumable reward. | 2 | `7` |
| `AdventureToken_YellowNeedle` | Variable | Tracks possession or use of the Yellow Needle adventure token. | 2 ||
| `all` | Variable | Represents the 'all' target or value, often used for selecting everything. | 2 ||
| [`Anxiety`](#object-anxiety) | Variable | Defines the Anxiety disorder class with name, description, and passives. | 2 ||
| [`Cancer`](./Engine_EventKeys.md#object-cancer) | Object  | Defines the Cancer item or disorder with name, description, rarity, and frame. | 2 | `{ . . . }` |
| [`CharmedPinky`](./Engine_EventKeys.md#object-charmedpinky) | Object  | Defines the CharmedPinky familiar variant with allied faction. | 2 | `{ . . . }` |
| [`CharmedRaptorBaby`](./Engine_EventKeys.md#object-charmedraptorbaby) | Object  | Defines the CharmedRaptorBaby familiar variant with allied faction. | 2 | `{ . . . }` |
| `clear_result_animation` | Integer | The number of result animations to clear or skip. | 2 | `1` |
| [`clear_surviving_kaiju`](./Enums.md#enum-clear_surviving_kaiju) | Enum | Specifies which surviving kaiju to clear or remove. | 2 | `pyrophina`<br>`zaratana` |
| [`Depression`](#object-depression) | Variable | Represents the Depression disorder or state. | 2 ||
| `flesh_items` | Variable | Represents a category of flesh-based items. | 2 ||
| [`gain_immortal_familiar`](./Enums.md#enum-gain_immortal_familiar) | Enum | Specifies the immortal familiar to add to the party. | 2 | `CharmedFlea`<br>`CharmedFleaSpecial`<br>`CharmedPooter` |
| [`get_and_equip_item`](./Enums.md#enum-get_and_equip_item) | Enum | Specifies the item to obtain and immediately equip. | 2 | `Catnip`<br>`FlyLarva` |
| `glitched_items` | Variable | Represents a category of glitched items. | 2 ||
| `HasHitPinata` | Variable | Tracks whether the player has hit a piñata event. | 2 ||
| [`HauntedNight`](#object-hauntednight) | Variable | Tracks the Haunted Night event or state. | 2 ||
| [`map_unlock_dimensionx`](#object-map_unlock_dimensionx) | Variable | Triggers the unlock of the Dimension X map area and sets the associated mapgen flag. | 2 ||
| [`party_gain_disorder_from_pool`](./Arrays.md#array-party_gain_disorder_from_pool) | Array | An array specifying the pool or list of disorders for the party to gain. | 2 | `[Dwarfism]`<br>`[Gigantism]`<br>`all_disorders` |
| `party_heal_injury` | Integer | The amount of injury to heal for the entire party. | 2 | `99` |
| [`party_permanent_stats`](./Miscellaneous.md#object-party_permanent_stats) | Object  | An object defining permanent stat increases applied to the party. | 2 | `{ . . . }` |
| [`party_random_mutation_from_set`](./Miscellaneous.md#object-party_random_mutation_from_set) | Object  | An object specifying the count and mutation parts to randomly apply to the party. | 2 | `{ . . . }` |
| [`PawShards`](./Engine_EventKeys.md#object-pawshards) | Object  | Defines the PawShards item or object. | 2 | `{ . . . }` |
| `poop_items` | Variable | Represents a category of poop-based items. | 2 ||
| [`PutridLeech`](./Engine_EventKeys.md#object-putridleech) | Object  | Defines the PutridLeech item or object. | 2 | `{ . . . }` |
| [`PyrophinasCollar`](./Engine_EventKeys.md#object-pyrophinascollar) | Object  | Defines the PyrophinasCollar item or object. | 2 | `{ . . . }` |
| `QEVENT_OBELISK_QUES1` | Variable | Represents the first quest step or state for the obelisk event. | 2 ||
| `QEVENT_THROBBINGARTERY_REW1` | Variable | Represents the first reward state for the Throbbing Artery quest chain. | 2 ||
| `QEVENT_THROBBINGARTERY_REW2` | Variable | Represents the second reward state for the Throbbing Artery quest chain. | 2 ||
| `QEVENT_VOLCANO_REW1` | Variable | Represents the first reward state for the volcano event quest chain. | 2 ||
| [`ReceiverAntenna`](./Engine_EventKeys.md#object-receiverantenna) | Object  | Defines the ReceiverAntenna item or object. | 2 | `{ . . . }` |
| `resultBad` | Variable | Represents a bad outcome state for an event result. | 2 ||
| [`Rocks`](./Engine_EventKeys.md#object-rocks) | Object  | Defines the Rocks item or object. | 2 | `{ . . . }` |
| [`scramble_abilities`](./Enums.md#enum-scramble_abilities) | Enum | Specifies which abilities to randomize, such as 'all'. | 2 | `all` |
| `set_age` | Integer | The age value to set for the target unit. | 2 | `1` |
| [`SignalAmplifier`](./Engine_EventKeys.md#object-signalamplifier) | Object  | An object defining properties for a signal amplifier mechanic. | 2 | `{ . . . }` |
| [`Snake`](./Engine_LogicKeys.md#object-snake) | Integer / Object  | The number of snake familiars spawned. | 2 | `{ . . . }`<br>`10` |
| [`ThrobbingGristle`](./Engine_EventKeys.md#object-throbbinggristle) | Object  | An object defining properties for a throbbing gristle mechanic. | 2 | `{ . . . }` |
| [`TransmitterAntenna`](./Engine_EventKeys.md#object-transmitterantenna) | Object  | An object defining properties for a transmitter antenna mechanic. | 2 | `{ . . . }` |
| [`ZaratanasCollar`](./Engine_EventKeys.md#object-zaratanascollar) | Object  | An object defining properties for a Zaratana's collar mechanic. | 2 | `{ . . . }` |
| [`CryogenicTimeChamber_Empty`](./Engine_EventKeys.md#object-cryogenictimechamber_empty) | Object  | An object defining properties for an empty cryogenic time chamber. | 2 | `{ . . . }` |
| [`EnchantingPoop`](./Engine_EventKeys.md#object-enchantingpoop) | Object  | An object defining a trinket item that can be acquired from various poop events. | 2 | `{ . . . }` |
| [`general_common`](./Enums.md#enum-general_common) | Enum | Specifies the common rarity tier for an item or event outcome. | 2 | `auto` |
| [`general_rare`](./Enums.md#enum-general_rare) | Enum | Specifies the rare rarity tier for an item or event outcome. | 2 | `auto` |
| [`GuillotinasHead`](./Engine_EventKeys.md#object-guillotinashead) | Object  | An object defining properties for a guillotine's head mechanic. | 2 | `{ . . . }` |
| [`MomsKnife`](./Engine_EventKeys.md#object-momsknife) | Object  | An object defining properties for a mom's knife mechanic. | 2 | `{ . . . }` |
| [`RaptorEgg`](./Engine_LogicKeys.md#object-raptoregg) | Object  | An object defining a raptor egg item with a probability or weight. | 2 | `{ . . . }` |
| [`StatusDamagers`](./Passives_and_Statuses.md#object-statusdamagers) | Object  | An object defining status effects that damage the unit, with parameters for each status. | 2 | `{ . . . }` |
| [`self_status_next_fight`](./Miscellaneous.md#object-self_status_next_fight) | Object  | An object defining status effects applied to the unit at the start of the next fight. | 1 | `{ . . . }` |
| [`injury`](./Enums.md#enum-injury) | Enum | Specifies the type of injury applied, such as bleeding or stat reduction. | 1 | `bleeding`<br>`burned`<br>`cha` |
| [`gain_disorder_from_pool`](./Enums.md#enum-gain_disorder_from_pool) | Enum | Specifies a pool of disorders from which one is randomly gained. | 1 | `Crazy_disorders`<br>`Steven_disorders`<br>`[BlackFetin OrangeFetin PurpleFetin]` |
| [`conditional_reward`](./Miscellaneous.md#object-conditional_reward) | Object  | An object defining a reward that is granted only if specified conditions are met. | 1 | `{ . . . }` |
| `random_mutation` | Integer | The number of random mutations applied to the unit. | 1 | `1`<br>`10`<br>`2` |
| `next_event_bonus` | Integer | A modifier to the next event's outcome roll or selection chance. | 1 | `-1`<br>`-2`<br>`1` |
| `party_heal` | Integer | The amount of health healed for the entire party. | 1 | `1`<br>`10`<br>`100%` |
| [`mutation`](./Miscellaneous.md#object-mutation) | Object  | An object defining specific body part mutations applied to the unit. | 1 | `{ . . . }` |
| `cutscene` | String | Specifies the name of a cutscene to play. | 1 | `"chaos_ending_bad"`<br>`"chaos_ending_good"`<br>`"chapterintros/bunker"` |
| `random` | Number | A random value used for stat or attribute adjustment. | 1 | `-1`<br>`-2`<br>`1` |
| `ally_ambush_next_fights` | Integer | The number of upcoming fights that will start with an ally ambush. | 1 | `1`<br>`2` |
| `gain_cat_familiar` | Integer | The number of cat familiars gained. | 1 | `1` |
| `AdventureToken_HasRunFromDeath` | Variable | A boolean flag indicating the unit has run from death before. | 1 ||
| `AdventureToken_MysteriousCave_FamiliarVoice` | Variable | A boolean flag indicating the unit has heard a familiar voice in the mysterious cave. | 1 ||
| `AdventureToken_MysteriousJarRepeat` | Variable | A boolean flag indicating the unit has repeated interaction with a mysterious jar. | 1 ||
| `AdventureToken_StevenTryAgain` | Variable | A boolean flag indicating a retry with Steven. | 1 ||
| `AdventureToken_StevenTryAgain2` | Variable | A boolean flag indicating a second retry with Steven. | 1 ||
| `AdventureToken_StevenTryAgain3` | Variable | A boolean flag indicating a third retry with Steven. | 1 ||
| `AdventureToken_TrippedOnBigToe` | Variable | A boolean flag indicating the unit tripped on a big toe. | 1 ||
| `AdventureToken_UnmarkedGraveForced` | Variable | A boolean flag indicating the unit was forced to interact with an unmarked grave. | 1 ||
| [`Albinism`](#object-albinism) | Variable | A variable representing the Albinism disorder, defining its name, description, and passive effects. | 1 ||
| [`AlienOvergrowth`](#object-alienovergrowth) | Variable | A variable representing the Alien Overgrowth weather effect, defining its name, description, and gameplay effects. | 1 ||
| [`ambush`](./Math_Equations.md) | Equation | Specifies the path to a level file for an ambush encounter. | 1 | `"events/chupacabra.lvl"`<br>`putalevelhere.lvl` |
| `AntennaQuest_Orb` | Variable | A boolean flag tracking progress for the Antenna Quest related to the orb. | 1 ||
| `AntennaQuest_Rift` | Variable | A boolean flag tracking progress for the Antenna Quest related to the rift. | 1 ||
| `AntennaQuest_Volcano` | Variable | A boolean flag tracking progress for the Antenna Quest related to the volcano. | 1 ||
| [`Beepis`](./Engine_EventKeys.md#object-beepis) | Object  | An object defining properties for a beepis mechanic. | 1 | `{ . . . }` |
| [`bleeding`](#object-bleeding) | Variable | A boolean flag indicating the unit is bleeding. | 1 ||
| `bloody_items` | Variable | A boolean flag indicating the unit has bloody items. | 1 ||
| [`BrainDamage`](#object-braindamage) | Variable | A boolean flag indicating the unit has brain damage. | 1 ||
| [`BrainDead`](#object-braindead) | Variable | A variable representing the BrainDead disorder, defining its name, description, class, and stat modifiers. | 1 ||
| [`Brave`](#object-brave) | Variable | A variable representing the Brave disorder, defining its name, description, class, and passive effects. | 1 ||
| [`burned`](#object-burned) | Variable | A boolean flag indicating the unit is burned. | 1 ||
| [`CharmedTarBaby`](./Engine_EventKeys.md#object-charmedtarbaby) | Object  | An object defining a charmed variant of the TarBaby unit, with faction and inheritance properties. | 1 | `{ . . . }` |
| `clone_self_to_party` | Integer | The number of clones of the unit added to the party. | 1 | `1` |
| `copy_items_to_party` | Integer | The number of times the unit's items are copied to the party. | 1 | `1` |
| `copy_party_items` | Integer | The number of times party items are copied to the unit. | 1 | `1` |
| [`Cunch`](./Engine_EventKeys.md#object-cunch) | Object  | An object defining properties for a cunch mechanic. | 1 | `{ . . . }` |
| [`CursedStickman`](./Engine_EventKeys.md#object-cursedstickman) | Object  | An item object that defines the cursed stickman trinket with rarity, name, description, and cursed flag. | 1 | `{ . . . }` |
| [`DeathsScythe`](./Engine_EventKeys.md#object-deathsscythe) | Object  | An item object that defines Death's Scythe, likely a trinket or weapon with associated properties. | 1 | `{ . . . }` |
| `dimensionx.gon` | Variable | A reference to a .gon file that likely contains data for the dimension x map or event. | 1 ||
| `EVENT_USETHETOILET_AGAIN` | Variable | A boolean flag indicating whether the 'Use the Toilet' event can be triggered again. | 1 ||
| [`FecalHood_Cursed`](./Engine_EventKeys.md#object-fecalhood_cursed) | Object  | An item object defining the cursed version of the Fecal Hood trinket. | 1 | `{ . . . }` |
| [`FecalMask_Cursed`](./Engine_EventKeys.md#object-fecalmask_cursed) | Object  | An item object defining the cursed version of the Fecal Mask trinket. | 1 | `{ . . . }` |
| [`Feebis`](./Engine_EventKeys.md#object-feebis) | Object  | An object likely representing a character, item, or entity named Feebis, with associated properties. | 1 | `{ . . . }` |
| [`gain_clone_familiar`](./Miscellaneous.md#object-gain_clone_familiar) | Object  | An object that triggers the gaining of a clone familiar, with a specified object name. | 1 | `{ . . . }` |
| [`GeomagneticStorm`](#object-geomagneticstorm) | Variable | A variable that defines a geomagnetic storm weather effect, applying status effects to characters on round end. | 1 ||
| [`get_full_item_set_from_pool`](./Enums.md#enum-get_full_item_set_from_pool) | Enum | Specifies the item pool rarity from which to generate a full set of items. | 1 | `common` |
| [`Gigachad`](#object-gigachad) | Variable | A variable that defines the Gigachad disorder, including its name, description, and stat modifications. | 1 ||
| `godly_items` | Variable | A variable likely referencing a pool or collection of godly-rarity items. | 1 ||
| `grass_items` | Variable | A variable likely referencing a pool or collection of grass-themed items. | 1 ||
| `hide_items` | Variable | A variable likely referencing a pool or collection of hide-related items. | 1 ||
| [`Host`](./Engine_EventKeys.md#object-host) | Object  | An object representing the host entity, possibly a character or event trigger. | 1 | `{ . . . }` |
| `iceage.gon` | Variable | A reference to a .gon file that likely contains data for the ice age map or event. | 1 ||
| `junkyard_items` | Variable | A variable likely referencing a pool or collection of junkyard-themed items. | 1 ||
| [`legacy_event_unlock_momsknife`](#object-legacy_event_unlock_momsknife) | Variable | A variable that triggers the unlocking of the MomsKnife item and displays an unlock popup. | 1 ||
| [`lose_all_equipped_items`](./Enums.md#enum-lose_all_equipped_items) | Enum | Specifies the target (e.g., 'cat') from which to remove all currently equipped items. | 1 | `cat` |
| [`map_unlock_iceage`](#object-map_unlock_iceage) | Variable | A variable that unlocks the ice age area and displays an unlock popup. | 1 ||
| `mapflag_ChaosAntennaAttached` | Variable | A boolean flag indicating whether the chaos antenna has been attached to the map. | 1 ||
| `mapflag_OrbAntennaAttached` | Variable | A boolean flag indicating whether the orb antenna has been attached to the map. | 1 ||
| `mapflag_ThrobbingArteryDone` | Variable | A boolean flag indicating whether the Throbbing Artery event or quest has been completed. | 1 ||
| `mapflag_VolcanoAntennaAttached` | Variable | A boolean flag indicating whether the volcano antenna has been attached to the map. | 1 ||
| `mapflag_WallOfFleshDone` | Variable | A boolean flag indicating whether the Wall of Flesh event or quest has been completed. | 1 ||
| [`meat_world_open`](#object-meat_world_open) | Variable | A variable that sets a mapgen flag to fully unlock the Meat World area and shows an unlock popup. | 1 ||
| `MeatWorldQuest_Gristle` | Variable | A variable likely defining a sub-quest involving the Gristle entity within the Meat World. | 1 ||
| `MeatWorldQuest_Leech` | Variable | A variable likely defining a sub-quest involving the Leech entity within the Meat World. | 1 ||
| `MeteorShowerUnlocked` | Variable | A boolean flag indicating whether the Meteor Shower event or weather has been unlocked. | 1 ||
| `monkey_paw_1finger` | Variable | A variable representing a monkey paw with one finger remaining, likely tracking wishes or uses. | 1 ||
| `monkey_paw_2fingers` | Variable | A variable representing a monkey paw with two fingers remaining. | 1 ||
| `monkey_paw_3fingers` | Variable | A variable representing a monkey paw with three fingers remaining. | 1 ||
| `monkey_paw_4fingers` | Variable | A variable representing a monkey paw with four fingers remaining. | 1 ||
| [`MysteriousTomb1`](#object-mysterioustomb1) | Variable | A variable representing the first mysterious tomb event or object. | 1 ||
| [`MysteriousTomb2`](#object-mysterioustomb2) | Variable | A variable representing the second mysterious tomb event or object. | 1 ||
| [`party_injury`](./Enums.md#enum-party_injury) | Enum | Specifies the type of injury to inflict on the party (e.g., 'random'). | 1 | `random` |
| [`play_result_animation`](./Enums.md#enum-play_result_animation) | Enum | Specifies which result animation to play (e.g., 'resultVeryGood'). | 1 | `resultVeryGood` |
| [`PuncturedEye`](#object-puncturedeye) | Variable | A variable representing a punctured eye injury or status effect. | 1 ||
| `QEVENT_BROKENTIMEMACHINE_QUES` | Variable | A variable representing the quest objective or state for the broken time machine event. | 1 ||
| `QEVENT_BROKENTIMEMACHINE_REW2` | Variable | A variable representing a reward (likely reward 2) for the broken time machine quest. | 1 ||
| `QEVENT_BROKENTIMEMACHINE_REW3` | Variable | A variable representing reward 3 for the broken time machine quest. | 1 ||
| `QEVENT_BROKENTIMEMACHINE_REW4` | Variable | A variable representing reward 4 for the broken time machine quest. | 1 ||
| `QEVENT_BROKENTIMEMACHINE_REW5` | Variable | A variable representing reward 5 for the broken time machine quest. | 1 ||
| `QEVENT_DEADGOD_QUES` | Variable | A variable representing the quest objective or state for the dead god event. | 1 ||
| `QEVENT_DEADGOD_REW1` | Variable | A variable representing reward 1 for the dead god quest. | 1 ||
| `QEVENT_DEADGOD_REW2` | Variable | A variable representing reward 2 for the dead god quest. | 1 ||
| `QEVENT_DEADGOD_REW3` | Variable | A variable representing reward 3 for the dead god quest. | 1 ||
| `QEVENT_DEADKING_QUES` | Variable | A variable representing the quest objective or state for the dead king event. | 1 ||
| `QEVENT_DEADKING_REW1` | Variable | A variable representing reward 1 for the dead king quest. | 1 ||
| `QEVENT_DEADKING_REW2` | Variable | A variable representing reward 2 for the dead king quest. | 1 ||
| `QEVENT_DEADKING_REW3` | Variable | A variable storing the reward index or item quantity for the third reward from the Dead King event. | 1 ||
| `QEVENT_DEADKING_REW4` | Variable | A variable storing the reward index or item quantity for the fourth reward from the Dead King event. | 1 ||
| `QEVENT_DEADKING_REW5` | Variable | A variable storing the reward index or item quantity for the fifth reward from the Dead King event. | 1 ||
| `QEVENT_DIMENSIONXPORTAL_ENTER_REW` | Variable | A variable storing the reward index or item quantity granted upon entering the Dimension X portal. | 1 ||
| `QEVENT_DIMENSIONXPORTAL_IGNORE_ANSW` | Variable | A variable storing the answer index that causes the Dimension X portal to be ignored. | 1 ||
| `QEVENT_DIMENSIONXPORTAL_QUES` | Variable | A variable storing the question index presented by the Dimension X portal. | 1 ||
| `QEVENT_GLOWINGORB_QUES` | Variable | A variable storing the question index for the first puzzle of the Glowing Orb event. | 1 ||
| `QEVENT_GLOWINGORB_QUES2` | Variable | A variable storing the question index for the second puzzle of the Glowing Orb event. | 1 ||
| `QEVENT_GLOWINGORB_REW1` | Variable | A variable storing the reward index or item quantity for the first reward from the Glowing Orb event. | 1 ||
| `QEVENT_GLOWINGORB_REW2` | Variable | A variable storing the reward index or item quantity for the second reward from the Glowing Orb event. | 1 ||
| `QEVENT_GLOWINGORB_REW3` | Variable | A variable storing the reward index or item quantity for the third reward from the Glowing Orb event. | 1 ||
| `QEVENT_GLOWINGORB_REW4` | Variable | A variable storing the reward index or item quantity for the fourth reward from the Glowing Orb event. | 1 ||
| `QEVENT_GLOWINGORB_REW5` | Variable | A variable storing the reward index or item quantity for the fifth reward from the Glowing Orb event. | 1 ||
| `QEVENT_GLOWINGORB_REW7` | Variable | A variable storing the reward index or item quantity for the seventh reward from the Glowing Orb event. | 1 ||
| `QEVENT_MEATALTAR_QUES1` | Variable | A variable storing the question index for the first puzzle of the Meat Altar event. | 1 ||
| `QEVENT_MEATALTAR_REW1` | Variable | A variable storing the reward index or item quantity for the first reward from the Meat Altar event. | 1 ||
| `QEVENT_MEATALTAR_REW_IGNORE` | Variable | A variable storing the reward index or item quantity granted when ignoring the Meat Altar. | 1 ||
| `QEVENT_OBELISK_CORE_REW_ZARA3` | Variable | A variable storing the reward index or item quantity for Zara's third reward from the Obelisk Core event. | 1 ||
| `QEVENT_OBELISK_MOON_REW_PYRO3` | Variable | A variable storing the reward index or item quantity for Pyro's third reward from the Obelisk Moon event. | 1 ||
| `QEVENT_OBELISK_QUES3` | Variable | A variable storing the question index for the third puzzle of the Obelisk event. | 1 ||
| `QEVENT_THEHEAD_QUES` | Variable | A variable storing the question index presented by The Head event. | 1 ||
| `QEVENT_THEHEAD_REW1` | Variable | A variable storing the reward index or item quantity for the first reward from The Head event. | 1 ||
| `QEVENT_THEHEAD_REW2` | Variable | A variable storing the reward index or item quantity for the second reward from The Head event. | 1 ||
| `QEVENT_THEHEAD_REW3` | Variable | A variable storing the reward index or item quantity for the third reward from The Head event. | 1 ||
| `QEVENT_THEHEAD_REW5` | Variable | A variable storing the reward index or item quantity for the fifth reward from The Head event. | 1 ||
| `QEVENT_THEHEAD_REW6` | Variable | A variable storing the reward index or item quantity for the sixth reward from The Head event. | 1 ||
| `QEVENT_THROBBINGARTERY2_QUES` | Variable | A variable storing the question index presented by the second Throbbing Artery event. | 1 ||
| `QEVENT_THROBBINGARTERY2_REW_IGNORE` | Variable | A variable storing the reward index or item quantity granted when ignoring the second Throbbing Artery. | 1 ||
| `QEVENT_THROBBINGARTERY_QUES1` | Variable | A variable storing the question index for the first puzzle of the Throbbing Artery event. | 1 ||
| `QEVENT_THROBBINGARTERY_QUES2` | Variable | A variable storing the question index for the second puzzle of the Throbbing Artery event. | 1 ||
| `QEVENT_THROBBINGARTERY_REW5` | Variable | A variable storing the reward index or item quantity for the fifth reward from the Throbbing Artery event. | 1 ||
| `QEVENT_THROBBINGARTERY_REW_IGNORE` | Variable | A variable storing the reward index or item quantity granted when ignoring the Throbbing Artery. | 1 ||
| `QEVENT_TIMEMACHINE_FUTURE_QUES` | Variable | A variable storing the question index presented by the Future timeline of the Time Machine. | 1 ||
| `QEVENT_TIMEMACHINE_FUTURE_REW1` | Variable | A variable storing the reward index or item quantity for the first reward from the Future timeline of the Time Machine. | 1 ||
| `QEVENT_TIMEMACHINE_FUTURE_REW2` | Variable | A variable storing the reward index or item quantity for the second reward from the Future timeline of the Time Machine. | 1 ||
| `QEVENT_TIMEMACHINE_ICEAGE_QUES` | Variable | A variable storing the question index presented by the Ice Age timeline of the Time Machine. | 1 ||
| `QEVENT_TIMEMACHINE_ICEAGE_REW1` | Variable | A variable storing the reward index or item quantity for the first reward from the Ice Age timeline of the Time Machine. | 1 ||
| `QEVENT_TIMEMACHINE_ICEAGE_REW2` | Variable | A variable storing the reward index or item quantity for the second reward from the Ice Age timeline of the Time Machine. | 1 ||
| `QEVENT_TIMEMACHINE_JURASSIC_QUES` | Variable | A variable storing the question index presented by the Jurassic timeline of the Time Machine. | 1 ||
| `QEVENT_TIMEMACHINE_JURASSIC_REW1` | Variable | A variable storing the reward index or item quantity for the first reward from the Jurassic timeline of the Time Machine. | 1 ||
| `QEVENT_TIMEMACHINE_JURASSIC_REW2` | Variable | A variable storing the reward index or item quantity for the second reward from the Jurassic timeline of the Time Machine. | 1 ||
| `QEVENT_TIMEMACHINE_QUES` | Variable | A variable storing the question index presented by the base Time Machine event. | 1 ||
| `QEVENT_TIMEMACHINE_REW1` | Variable | A variable storing the reward index or item quantity for the first reward from the base Time Machine event. | 1 ||
| `QEVENT_TIMEMACHINE_REW2` | Variable | A variable storing the reward index or item quantity for the second reward from the base Time Machine event. | 1 ||
| `QEVENT_TIMEMACHINE_REW3` | Variable | A variable storing the reward index or item quantity for the third reward from the base Time Machine event. | 1 ||
| `QEVENT_TIMEMACHINE_THEEND_QUES` | Variable | A variable storing the question index presented by The End timeline of the Time Machine. | 1 ||
| `QEVENT_TIMEMACHINE_THEEND_REW1` | Variable | A variable storing the reward index or item quantity for the first reward from The End timeline of the Time Machine. | 1 ||
| `QEVENT_TIMEMACHINE_THEEND_REW2` | Variable | A variable storing the reward index or item quantity for the second reward from The End timeline of the Time Machine. | 1 ||
| `QEVENT_VOLCANO_QUES` | Variable | A variable storing the question index for the first puzzle of the Volcano event. | 1 ||
| `QEVENT_VOLCANO_QUES2` | Variable | A variable storing the question index for the second puzzle of the Volcano event. | 1 ||
| `QEVENT_VOLCANO_REW4` | Variable | Stores a reward variable for the Volcano event, slot 4. | 1 ||
| `QEVENT_VOLCANO_REW5` | Variable | Stores a reward variable for the Volcano event, slot 5. | 1 ||
| `QEVENT_VOLCANO_REW7` | Variable | Stores a reward variable for the Volcano event, slot 7. | 1 ||
| `QEVENT_WALLOFFLESH2_QUES` | Variable | Stores the quest state variable for the second Wall of Flesh event. | 1 ||
| `QEVENT_WALLOFFLESH2_REW_IGNORE` | Variable | Controls whether to ignore the reward condition for the second Wall of Flesh event. | 1 ||
| `QEVENT_WALLOFFLESH_QUES1` | Variable | Stores the quest state variable for the first Wall of Flesh event, slot 1. | 1 ||
| `QEVENT_WALLOFFLESH_QUES2` | Variable | Stores the quest state variable for the first Wall of Flesh event, slot 2. | 1 ||
| `QEVENT_WALLOFFLESH_REW1` | Variable | Stores a reward variable for the Wall of Flesh event, slot 1. | 1 ||
| `QEVENT_WALLOFFLESH_REW10` | Variable | Stores a reward variable for the Wall of Flesh event, slot 10. | 1 ||
| `QEVENT_WALLOFFLESH_REW2` | Variable | Stores a reward variable for the Wall of Flesh event, slot 2. | 1 ||
| `QEVENT_WALLOFFLESH_REW3` | Variable | Stores a reward variable for the Wall of Flesh event, slot 3. | 1 ||
| `QEVENT_WALLOFFLESH_REW4` | Variable | Stores a reward variable for the Wall of Flesh event, slot 4. | 1 ||
| `QEVENT_WALLOFFLESH_REW5` | Variable | Stores a reward variable for the Wall of Flesh event, slot 5. | 1 ||
| `QEVENT_WALLOFFLESH_REW7` | Variable | Stores a reward variable for the Wall of Flesh event, slot 7. | 1 ||
| `QEVENT_WALLOFFLESH_REW8` | Variable | Stores a reward variable for the Wall of Flesh event, slot 8. | 1 ||
| `QEVENT_WALLOFFLESH_REW9` | Variable | Stores a reward variable for the Wall of Flesh event, slot 9. | 1 ||
| `QEVENT_WALLOFFLESH_REW_IGNORE` | Variable | Controls whether to ignore the reward condition for the Wall of Flesh event. | 1 ||
| [`random_chance`](./Miscellaneous.md#object-random_chance) | Object  | Defines a block with a percentage chance and an action to execute if the chance succeeds. | 1 | `{ . . . }` |
| `raptor_nest_eggs` | Variable | Tracks the number of eggs in a raptor nest. | 1 ||
| `resultConfused` | Variable | An event result indicating a confused outcome. | 1 ||
| `resultVeryBad` | Variable | An event result indicating a very bad outcome. | 1 ||
| `rock_items` | Variable | A pool of rock-themed items. | 1 ||
| [`scramble_basic_attack`](./Enums.md#enum-scramble_basic_attack) | Enum | Specifies which basic attacks to randomize or scramble. | 1 | `all` |
| [`scramble_passives`](./Enums.md#enum-scramble_passives) | Enum | Specifies which passive abilities to randomize or scramble. | 1 | `all` |
| [`select_item_from_pool_for_cutscene_only`](./Enums.md#enum-select_item_from_pool_for_cutscene_only) | Enum | Selects an item from a named pool for display in a cutscene without granting it. | 1 | `glitched_items` |
| `self_heal` | Integer | The amount of health the unit heals itself. | 1 | `10` |
| [`SludgeHat`](./Engine_EventKeys.md#object-sludgehat) | Object  | Defines the Sludge Hat item or trait. | 1 | `{ . . . }` |
| [`SludgeMask`](./Engine_EventKeys.md#object-sludgemask) | Object  | Defines the Sludge Mask item or trait. | 1 | `{ . . . }` |
| [`Soulless`](#object-soulless) | Variable | Defines the Soulless disorder, with its name, description, and passives. | 1 ||
| `Steven_disorders` | Variable | A collection of disorders associated with the character Steven. | 1 ||
| [`StrangeEggs`](#object-strangeeggs) | Variable | Defines the StrangeEggs weather, which spawns extra things on battle start. | 1 ||
| `tech_items` | Variable | A pool of technology-themed items. | 1 ||
| `TheRift_UsedPyrophina` | Variable | Tracks whether the Pyrophina item has been used in the Rift event. | 1 ||
| `TheRift_UsedZaratana` | Variable | Tracks whether the Zaratana item has been used in the Rift event. | 1 ||
| [`TheShimmer`](#object-theshimmer) | Variable | Defines the Shimmer weather, which adds a post-process visual effect. | 1 ||
| [`time_machine_quest_finalstep`](#object-time_machine_quest_finalstep) | Variable | Triggers the final step NPC sequence for the time machine quest. | 1 ||
| [`time_machine_quest_trigger`](#object-time_machine_quest_trigger) | Variable | Triggers the introductory NPC sequence for the time machine quest. | 1 ||
| [`Touched`](#object-touched) | Variable | Defines the Touched disorder, with its name, description, and stats. | 1 ||
| `trigger_butterfly_effect` | Integer | The number of times to trigger the butterfly effect event. | 1 | `1` |
| `WorldEventLegacyCounter_SealedCrypt` | Variable | Counter tracking how many times the Sealed Crypt has been encountered. | 1 ||
| `WorldEventLegacyToken_CryptOpened` | Variable | Boolean token indicating the Crypt has been opened. | 1 ||
| `WorldEventLegacyToken_HasRunFromDeath` | Variable | Boolean token indicating the player has run from death. | 1 ||
| `WorldEventLegacyToken_MomsKnife` | Variable | Boolean token related to acquiring Mom's Knife. | 1 ||
| `WorldEventLegacyToken_MonkeyPaw1` | Variable | Boolean token for the first Monkey Paw wish. | 1 ||
| `WorldEventLegacyToken_MonkeyPaw2` | Variable | Boolean token for the second Monkey Paw wish. | 1 ||
| `WorldEventLegacyToken_MonkeyPaw3` | Variable | Boolean token for the third Monkey Paw wish. | 1 ||
| `WorldEventLegacyToken_MonkeyPaw4` | Variable | Boolean token for the fourth Monkey Paw wish. | 1 ||
| `WorldEventLegacyToken_MonkeyPawGenes` | Variable | Boolean token for a Monkey Paw wish related to genes. | 1 ||
| `WorldEventLegacyToken_MonkeyPawItems` | Variable | Boolean token for a Monkey Paw wish related to items. | 1 ||
| `WorldEventLegacyToken_MonkeyPawKnowledge` | Variable | Boolean token for a Monkey Paw wish related to knowledge. | 1 ||
| `WorldEventLegacyToken_MonkeyPawStrength` | Variable | The strength modifier for the Monkey Paw legacy event token. | 1 ||
| `WorldEventLegacyToken_StacyMutant` | Variable | The value associated with the Stacy Mutant legacy event token. | 1 ||
| `spawn_reflection_next_fight` | Number | The number of reflections to spawn in the next battle, optionally with a mutation. | 0 | `1` |

</details>
### Valid Nested Objects

The following objects all behave as `{Event Keys}` containers. Each has its own unique parameters listed below its entry.


---


#### `bad`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 343

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prompt`](./Enums.md#enum-prompt) | String | The text or localization key for the popup or prompt displayed to the player. | 38 | `"Donate 3 times before you can receive a reward!"`<br>`"EVENT_ABEGGAR_LEAVE"`<br>`"EVENT_ABEGGAR_QUES"` |
| `set_frame` | Integer | The specific animation frame to set for an object or UI element. | 36 | `1`<br>`10`<br>`15` |
| [`permanent_stats`](./Miscellaneous.md#object-permanent_stats) | Object  | Defines permanent stat changes to apply to the unit (e.g., con, cha). | 7 | `{ . . . }` |
| [`play_animation`](./Arrays.md#array-play_animation) | Array / Enum | Specifies an animation to play, optionally as an array with a probability weight. | 5 | `[resultBlessing .5]`<br>`[resultGood .5]`<br>`[resultLeave 0]` |
| [`reward`](./Miscellaneous.md#object-reward) | Object  | An object containing sub-objects defining the rewards for different rarity tiers (e.g., common, rare), each with their own set of actions and items. | 5 | `{ . . . }` |
| [`kill`](./Enums.md#enum-kill) | Enum | Kills the specified target type (e.g., 'cat'). | 4 | `cat` |
| [`event_now`](./Enums.md#enum-event_now) | Enum | Triggers the specified event immediately. | 3 | `MeatGolem`<br>`Mirage`<br>`MysteriousMachine_Bad` |
| [`event_now_same_cat`](./Enums.md#enum-event_now_same_cat) | Enum | Specifies a world event that will now occur for the same cat category as the current event. | 3 | `BigToe`<br>`Blessing`<br>`BodyOfGlorg_Gift` |
| [`battle`](./Math_Equations.md) | String | Defines a battle encounter by preset, level file path, or reverb settings. | 2 | `"desert/boss/dustdevil/DustDevil.lvl"`<br>`"events/Death.lvl"`<br>`"events/GlowingBear"` |
| [`get_parasite_from_pool`](./Enums.md#enum-get_parasite_from_pool) | Enum | Specifies the pool name or explicit list of parasites to obtain from. | 2 | `[AmoebaHat AmoebaNeck AmoebaFace]`<br>`barbed_armor`<br>`barbed_items` |
| [`conditional_reward`](./Miscellaneous.md#object-conditional_reward) | Object  | An object defining a reward that is granted only if specified conditions are met. | 1 | `{ . . . }` |
| [`cutscene`](./Miscellaneous.md#object-cutscene) | Object  | Specifies the name of a cutscene to play. | 1 | `{ . . . }` |
| [`gain_disorder_from_pool`](./Enums.md#enum-gain_disorder_from_pool) | Enum | Specifies a pool of disorders from which one is randomly gained. | 1 | `Crazy_disorders`<br>`Steven_disorders`<br>`[BlackFetin OrangeFetin PurpleFetin]` |
| [`gain_immortal_familiar`](./Enums.md#enum-gain_immortal_familiar) | Enum | Specifies the immortal familiar to add to the party. | 1 | `CharmedFlea`<br>`CharmedFleaSpecial`<br>`CharmedPooter` |
| [`get_parasite`](./Enums.md#enum-get_parasite) | Enum | Specifies a parasite item to attach to a unit when this event triggers. | 1 | `AlluringDoodie`<br>`BadSplinters`<br>`Beepis` |
| [`injury`](./Enums.md#enum-injury) | Enum | Specifies the type of injury applied, such as bleeding or stat reduction. | 1 | `bleeding`<br>`burned`<br>`cha` |
| [`lose_item`](./Enums.md#enum-lose_item) | Enum | Specifies which item slot or type to lose (e.g., 'equipped', 'inventory'). | 1 | `equipped`<br>`inventory`<br>`parasite` |
| `next_event_bonus` | Integer | A modifier to the next event's outcome roll or selection chance. | 1 | `-1`<br>`-2`<br>`1` |
| [`party_random_mutation_from_set`](./Miscellaneous.md#object-party_random_mutation_from_set) | Object  | An object specifying the count and mutation parts to randomly apply to the party. | 1 | `{ . . . }` |
| [`select_item_from_pool_for_cutscene_only`](./Enums.md#enum-select_item_from_pool_for_cutscene_only) | Enum | Selects an item from a named pool for display in a cutscene without granting it. | 1 | `glitched_items` |
| [`self_status_next_fight`](./Miscellaneous.md#object-self_status_next_fight) | Object  | An object defining status effects applied to the unit at the start of the next fight. | 1 | `{ . . . }` |
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum | Specifies a legacy token to set (enable or mark as true) when this event triggers. | 1 | `AlienOvergrowthUnlocked`<br>`AntennaQuest_Orb`<br>`AntennaQuest_Rift` |

</details>


---


#### `common`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1197

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`self_damage`](./Miscellaneous.md#object-self_damage) | Boolean / Integer / Object  | Defines damage or effects applied to the caster when using the ability. | 436 | `{ . . . }`<br>`1`<br>`10`<br>`100%` |
| [`prompt`](./Enums.md#enum-prompt) | String | The text or localization key for the popup or prompt displayed to the player. | 38 | `"Donate 3 times before you can receive a reward!"`<br>`"EVENT_ABEGGAR_LEAVE"`<br>`"EVENT_ABEGGAR_QUES"` |
| `set_frame` | Integer | The specific animation frame to set for an object or UI element. | 36 | `1`<br>`10`<br>`15` |
| [`clear_adventure_token`](./Enums.md#enum-clear_adventure_token) | Enum | Specifies an adventure token to clear (disable or mark as false) when this event triggers. | 24 | `AdventureToken_BlueNeedle`<br>`AdventureToken_HasTakenNeedle`<br>`AdventureToken_RedNeedle` |
| [`event_now_same_cat`](./Enums.md#enum-event_now_same_cat) | Enum | Specifies a world event that will now occur for the same cat category as the current event. | 21 | `BigToe`<br>`Blessing`<br>`BodyOfGlorg_Gift` |
| [`spawn_unit_next_fight`](./Miscellaneous.md#object-spawn_unit_next_fight) | Object  | An object defining a unit to spawn during the next fight, including its object, count, and spawn side. | 18 | `{ . . . }` |
| [`get_item`](./Enums.md#enum-get_item) | Enum | Specifies an item to add to the player's inventory when this event triggers. | 14 | `AlienBlaster`<br>`BagOfGrass`<br>`BearTrapMask` |
| [`play_animation`](./Arrays.md#array-play_animation) | Array / Enum | Specifies an animation to play, optionally as an array with a probability weight. | 13 | `[resultBlessing .5]`<br>`[resultGood .5]`<br>`[resultLeave 0]` |
| [`gain_disorder`](./Enums.md#enum-gain_disorder) | Enum | Specifies a disorder to add to the current cat when this event triggers. | 12 | `AcidReflux`<br>`Albinism`<br>`Anxiety` |
| [`get_item_from_pool`](./Miscellaneous.md#object-get_item_from_pool) | Array / Enum / Object  | Grants an item from the specified pool or a specific item name. | 11 | `{ . . . }`<br>`Bird_items`<br>`Coin_items`<br>`Eye_items` |
| `override_end_option_prompt` | String | Specifies a custom prompt string to display for the end option of this event choice. | 11 | `"EVENT_LOCKEDDOOR_PROMPT1"`<br>`"EVENT_LOCKEDDOOR_PROMPT2"`<br>`"EVENT_MYSTERIOUSSTRANGER_END_AGAIN"` |
| [`party_status_next_fight`](./Miscellaneous.md#object-party_status_next_fight) | Object  | An object defining status effects to apply to the party at the start of the next fight. | 11 | `{ . . . }` |
| `full_heal` | Integer | If set to 1, fully restores the unit's health. | 10 | `1` |
| `ambush_next_basic_fights` | Integer | The number of basic fights to trigger as ambushes. | 9 | `1` |
| [`party_damage`](./Arrays.md#array-party_damage) | Array / Number | An array specifying the minimum and maximum damage dealt to the party, or a single integer or percentage. | 9 | `1`<br>`10`<br>`2` |
| [`set_adventure_token`](./Enums.md#enum-set_adventure_token) | Enum | Specifies an adventure token to set (enable or mark as true) when this event triggers. | 9 | `AdventureToken_BlueNeedle`<br>`AdventureToken_HasRunFromDeath`<br>`AdventureToken_HasTakenNeedle` |
| [`random_mutation_from_set`](./Miscellaneous.md#object-random_mutation_from_set) | Number / Object  | Defines a set of mutation categories and their specific IDs to apply a random mutation from. | 8 | `{ . . . }` |
| [`get_parasite`](./Enums.md#enum-get_parasite) | Enum | Specifies a parasite item to attach to a unit when this event triggers. | 7 | `AlluringDoodie`<br>`BadSplinters`<br>`Beepis` |
| [`permanent_stats`](./Miscellaneous.md#object-permanent_stats) | Object  | Defines permanent stat changes to apply to the unit (e.g., con, cha). | 7 | `{ . . . }` |
| [`gain_coins`](./Arrays.md#array-gain_coins) | Array / Number | An array specifying the minimum and maximum amount of coins gained, or a single integer. | 6 | `1`<br>`10`<br>`15` |
| [`global_effect_next_fight`](./Miscellaneous.md#object-global_effect_next_fight) | Object  | Defines a global status effect or modifier to apply in the next fight. | 6 | `{ . . . }` |
| [`increment_legacy_counter`](./Enums.md#enum-increment_legacy_counter) | Enum | Specifies a legacy counter to increment by one when this event triggers. | 6 | `WorldEventLegacyCounter_CrackInTheWall`<br>`WorldEventLegacyCounter_CustomTokenString`<br>`WorldEventLegacyCounter_FooCounter` |
| [`add_weather`](./Enums.md#enum-add_weather) | Enum | Specifies a weather effect type to apply to the current map. | 5 | `AlienOvergrowth`<br>`Birdemic`<br>`GeomagneticStorm` |
| [`kill`](./Enums.md#enum-kill) | Enum | Kills the specified target type (e.g., 'cat'). | 5 | `cat` |
| [`lose_item`](./Enums.md#enum-lose_item) | Enum | Specifies which item slot or type to lose (e.g., 'equipped', 'inventory'). | 5 | `equipped`<br>`inventory`<br>`parasite` |
| [`shop_now`](./Enums.md#enum-shop_now) | Enum | Triggers the specified shop to appear immediately. | 5 | `Event_RareShop`<br>`Event_SmallShop`<br>`Shop` |
| [`spin`](./Enums.md#enum-spin) | Enum | Specifies an action to re-roll or spin again, such as for a random reward wheel. | 4 | `again` |
| [`gain_familiar`](./Miscellaneous.md#object-gain_familiar) | Enum / Object  | Specifies which familiar type (by its class name) the unit gains. | 3 | `{ . . . }`<br>`CharmedBear`<br>`CharmedDaddyShark`<br>`CharmedDustDevil` |
| [`gain_food`](./Arrays.md#array-gain_food) | Array / Number | An array specifying the minimum and maximum amount of food gained, or a single integer. | 3 | `-5`<br>`20`<br>`30` |
| [`damage`](./Arrays.md#array-damage) | Array / Equation  | Specifies the amount of damage dealt, can be a number or expression. | 2 | `"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`event_now`](./Enums.md#enum-event_now) | Enum | Triggers the specified event immediately. | 2 | `MeatGolem`<br>`Mirage`<br>`MysteriousMachine_Bad` |
| [`get_parasite_from_pool`](./Arrays.md#array-get_parasite_from_pool) | Array / Enum  | Specifies the pool name or explicit list of parasites to obtain from. | 2 | `[AmoebaHat AmoebaNeck AmoebaFace]`<br>`barbed_armor`<br>`barbed_items` |
| [`lose_specific_item`](./Enums.md#enum-lose_specific_item) | Enum | Removes the specified item from the player's inventory. | 2 | `CryogenicTimeChamber_Full`<br>`PutridLeech`<br>`PyrophinasCollar` |
| [`next_event_from_set`](./Miscellaneous.md#object-next_event_from_set) | Object  | Specifies the next event to trigger, or defines a set of events with count and category constraints. | 2 | `{ . . . }` |
| `party_heal_disorder` | Integer | The number of disorders to heal from all party members. | 2 | `2` |
| [`party_permanent_stats_exclude_self`](./Miscellaneous.md#object-party_permanent_stats_exclude_self) | Object  | An object specifying permanent stat bonuses (str, dex, con, int, spd) applied to all party members except the triggering unit. | 2 | `{ . . . }` |
| `ally_ambush_next_fights` | Integer | The number of upcoming fights that will start with an ally ambush. | 1 | `1`<br>`2` |
| `clear_result_animation` | Integer | The number of result animations to clear or skip. | 1 | `1` |
| [`conditional_reward`](./Miscellaneous.md#object-conditional_reward) | Object  | An object defining a reward that is granted only if specified conditions are met. | 1 | `{ . . . }` |
| [`decrement_legacy_counter`](./Enums.md#enum-decrement_legacy_counter) | Enum | Specifies which legacy counter or token to decrement by one. | 1 | `WorldEventLegacyCounter_CrackInTheWall`<br>`WorldEventLegacyCounter_CustomTokenString`<br>`WorldEventLegacyToken_StartDigging` |
| [`gain_disorder_from_pool`](./Arrays.md#array-gain_disorder_from_pool) | Array / Enum  | Specifies a pool of disorders from which one is randomly gained. | 1 | `Crazy_disorders`<br>`Steven_disorders`<br>`[BlackFetin OrangeFetin PurpleFetin]` |
| [`get_and_equip_item`](./Enums.md#enum-get_and_equip_item) | Enum | Specifies the item to obtain and immediately equip. | 1 | `Catnip`<br>`FlyLarva` |
| `heal_disorder` | Integer | Specifies which disorder type to heal, or the number of disorders to heal. | 1 | `1`<br>`2`<br>`Anxiety` |
| `heal_injury` | Integer | The number of injury points to heal on the target unit. | 1 | `1`<br>`5` |
| [`injury`](./Enums.md#enum-injury) | Enum | Specifies the type of injury applied, such as bleeding or stat reduction. | 1 | `bleeding`<br>`burned`<br>`cha` |
| [`learn_ability_from_pool`](./Enums.md#enum-learn_ability_from_pool) | Enum | An array specifying a pool or list of abilities from which one is randomly selected and learned. The string 'AnyUnlocked' selects any unlocked ability. | 1 | `AnyUnlocked`<br>`Necromancer`<br>`[Smack Meow Hiss]` |
| [`mutation`](./Miscellaneous.md#object-mutation) | Object  | An object defining specific body part mutations applied to the unit. | 1 | `{ . . . }` |
| `next_event_bonus` | Integer | A modifier to the next event's outcome roll or selection chance. | 1 | `-1`<br>`-2`<br>`1` |
| `party_heal` | Integer | The amount of health healed for the entire party. | 1 | `1`<br>`10`<br>`100%` |
| `random_mutation` | Integer | The number of random mutations applied to the unit. | 1 | `1`<br>`10`<br>`2` |
| `self_heal` | Integer | The amount of health the unit heals itself. | 1 | `10` |
| [`self_status_next_fight`](./Miscellaneous.md#object-self_status_next_fight) | Object  | An object defining status effects applied to the unit at the start of the next fight. | 1 | `{ . . . }` |
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum | Specifies a legacy token to set (enable or mark as true) when this event triggers. | 1 | `AlienOvergrowthUnlocked`<br>`AntennaQuest_Orb`<br>`AntennaQuest_Rift` |
| [`upgrade_ability`](./Enums.md#enum-upgrade_ability) | Enum | Specifies which ability to upgrade. The value 'random' selects a random eligible ability. | 1 | `random` |
| [`random_pool`](./Arrays.md#array-random_pool) | Array | An array of possible items or rewards from which one is randomly selected. | 0 | `[` |

</details>


---


#### `good`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 572

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`rare`](./Enums.md#enum-rare) | Enum | Defines the rare reward block for a boss encounter. | 673 | `1`<br>`10`<br>`15` |
| [`increment_legacy_counter`](./Enums.md#enum-increment_legacy_counter) | Enum | Specifies a legacy counter to increment by one when this event triggers. | 52 | `WorldEventLegacyCounter_CrackInTheWall`<br>`WorldEventLegacyCounter_CustomTokenString`<br>`WorldEventLegacyCounter_FooCounter` |
| [`prompt`](./Enums.md#enum-prompt) | String | The text or localization key for the popup or prompt displayed to the player. | 38 | `"Donate 3 times before you can receive a reward!"`<br>`"EVENT_ABEGGAR_LEAVE"`<br>`"EVENT_ABEGGAR_QUES"` |
| `set_frame` | Integer | The specific animation frame to set for an object or UI element. | 36 | `1`<br>`10`<br>`15` |
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum | Specifies a legacy token to set (enable or mark as true) when this event triggers. | 26 | `AlienOvergrowthUnlocked`<br>`AntennaQuest_Orb`<br>`AntennaQuest_Rift` |
| [`play_animation`](./Arrays.md#array-play_animation) | Array / Enum  | Specifies an animation to play, optionally as an array with a probability weight. | 20 | `[resultBlessing .5]`<br>`[resultGood .5]`<br>`[resultLeave 0]` |
| [`complete_item_quest`](./Enums.md#enum-complete_item_quest) | Enum | Marks the specified item quest as completed. | 18 | `BlackShard`<br>`CryogenicTimeChamber_Empty`<br>`CryogenicTimeChamber_Full` |
| [`begin_chapter`](./Enums.md#enum-begin_chapter) | Enum | Specifies the chapter file to begin, transitioning to that chapter. | 12 | `dimensionx.gon`<br>`endoftime.gon`<br>`future.gon` |
| [`set_adventure_token`](./Enums.md#enum-set_adventure_token) | Enum | Specifies an adventure token to set (enable or mark as true) when this event triggers. | 12 | `AdventureToken_BlueNeedle`<br>`AdventureToken_HasRunFromDeath`<br>`AdventureToken_HasTakenNeedle` |
| [`get_item_from_pool`](./Enums.md#enum-get_item_from_pool) | Enum | Grants an item from the specified pool or a specific item name. | 11 | `Bird_items`<br>`Coin_items`<br>`Eye_items` |
| [`event_now`](./Enums.md#enum-event_now) | Enum | Triggers the specified event immediately. | 9 | `MeatGolem`<br>`Mirage`<br>`MysteriousMachine_Bad` |
| [`event_now_same_cat`](./Enums.md#enum-event_now_same_cat) | Enum | Specifies a world event that will now occur for the same cat category as the current event. | 9 | `BigToe`<br>`Blessing`<br>`BodyOfGlorg_Gift` |
| [`gain_disorder`](./Enums.md#enum-gain_disorder) | Enum | Specifies a disorder to add to the current cat when this event triggers. | 8 | `AcidReflux`<br>`Albinism`<br>`Anxiety` |
| [`lose_specific_item`](./Enums.md#enum-lose_specific_item) | Enum | Removes the specified item from the player's inventory. | 8 | `CryogenicTimeChamber_Full`<br>`PutridLeech`<br>`PyrophinasCollar` |
| [`trigger_adventure_unlock`](./Enums.md#enum-trigger_adventure_unlock) | Enum | Triggers the specified adventure or map unlock quest. | 7 | `end_of_time_unlock`<br>`legacy_event_unlock_momsknife`<br>`map_unlock_dimensionx` |
| [`add_weather`](./Enums.md#enum-add_weather) | Enum | Specifies a weather effect type to apply to the current map. | 5 | `AlienOvergrowth`<br>`Birdemic`<br>`GeomagneticStorm` |
| [`get_item`](./Enums.md#enum-get_item) | Enum | Specifies an item to add to the player's inventory when this event triggers. | 5 | `AlienBlaster`<br>`BagOfGrass`<br>`BearTrapMask` |
| [`heal_disorder`](./Enums.md#enum-heal_disorder) | Enum / Number   | Specifies which disorder type to heal, or the number of disorders to heal. | 5 | `1`<br>`2`<br>`Anxiety` |
| [`reward`](./Miscellaneous.md#object-reward) | Object  | An object containing sub-objects defining the rewards for different rarity tiers (e.g., common, rare), each with their own set of actions and items. | 5 | `{ . . . }` |
| [`get_parasite`](./Enums.md#enum-get_parasite) | Enum | Specifies a parasite item to attach to a unit when this event triggers. | 3 | `AlluringDoodie`<br>`BadSplinters`<br>`Beepis` |
| `heal_injury` | Integer | The number of injury points to heal on the target unit. | 3 | `1`<br>`5` |
| [`kill`](./Enums.md#enum-kill) | Enum | Kills the specified target type (e.g., 'cat'). | 3 | `cat` |
| [`unlock_item_quest`](./Enums.md#enum-unlock_item_quest) | Enum | Specifies the item whose quest is unlocked or advanced. | 3 | `CryogenicTimeChamber_Empty`<br>`CryogenicTimeChamber_Full`<br>`JarOfChaos` |
| [`clear_surviving_kaiju`](./Enums.md#enum-clear_surviving_kaiju) | Enum | Specifies which surviving kaiju to clear or remove. | 2 | `pyrophina`<br>`zaratana` |
| [`cutscene_on_exit`](./Enums.md#enum-cutscene_on_exit) | Enum / Object | Determines which cutscene to play when the player leaves the current location. | 2 | `{ . . . }`<br>`infinite_intro`<br>`king_intro` |
| `full_heal` | Integer | If set to 1, fully restores the unit's health. | 2 | `1` |
| [`level_up`](./Enums.md#enum-level_up) | Enum | Specifies which units to level up, such as 'all' or 'self'. | 2 | `all`<br>`self` |
| `override_end_option_prompt` | String | Specifies a custom prompt string to display for the end option of this event choice. | 2 | `"EVENT_LOCKEDDOOR_PROMPT1"`<br>`"EVENT_LOCKEDDOOR_PROMPT2"`<br>`"EVENT_MYSTERIOUSSTRANGER_END_AGAIN"` |
| `ally_ambush_next_fights` | Integer | The number of upcoming fights that will start with an ally ambush. | 1 | `1`<br>`2` |
| `clone_self_to_party` | Integer | The number of clones of the unit added to the party. | 1 | `1` |
| [`conditional_reward`](./Miscellaneous.md#object-conditional_reward) | Object  | An object defining a reward that is granted only if specified conditions are met. | 1 | `{ . . . }` |
| `copy_items_to_party` | Integer | The number of times the unit's items are copied to the party. | 1 | `1` |
| `copy_party_items` | Integer | The number of times party items are copied to the unit. | 1 | `1` |
| `cutscene` | String | Specifies the name of a cutscene to play. | 1 | `"chaos_ending_bad"`<br>`"chaos_ending_good"`<br>`"chapterintros/bunker"` |
| [`gain_clone_familiar`](./Miscellaneous.md#object-gain_clone_familiar) | Object  | An object that triggers the gaining of a clone familiar, with a specified object name. | 1 | `{ . . . }` |
| [`gain_disorder_from_pool`](./Enums.md#enum-gain_disorder_from_pool) | Enum | Specifies a pool of disorders from which one is randomly gained. | 1 | `Crazy_disorders`<br>`Steven_disorders`<br>`[BlackFetin OrangeFetin PurpleFetin]` |
| [`get_full_item_set_from_pool`](./Enums.md#enum-get_full_item_set_from_pool) | Enum | Specifies the item pool rarity from which to generate a full set of items. | 1 | `common` |
| [`global_effect_next_fight`](./Miscellaneous.md#object-global_effect_next_fight) | Object  | Defines a global status effect or modifier to apply in the next fight. | 1 | `{ . . . }` |
| [`injury`](./Enums.md#enum-injury) | Enum | Specifies the type of injury applied, such as bleeding or stat reduction. | 1 | `bleeding`<br>`burned`<br>`cha` |
| [`learn_ability_from_pool`](./Arrays.md#array-learn_ability_from_pool) | Array / Enum | An array specifying a pool or list of abilities from which one is randomly selected and learned. The string 'AnyUnlocked' selects any unlocked ability. | 1 | `AnyUnlocked`<br>`Necromancer`<br>`[Smack Meow Hiss]` |
| [`learn_passive_from_pool`](./Arrays.md#array-learn_passive_from_pool) | Array / Enum | An array specifying a pool or list of passives from which one is randomly selected and learned. The string 'AnyUnlocked' selects any unlocked passive. | 1 | `AnyUnlocked`<br>`Necromancer`<br>`[MiniMe SkillShare]` |
| [`lose_item`](./Enums.md#enum-lose_item) | Enum | Specifies which item slot or type to lose (e.g., 'equipped', 'inventory'). | 1 | `equipped`<br>`inventory`<br>`parasite` |
| [`mutation`](./Miscellaneous.md#object-mutation) | Object  | An object defining specific body part mutations applied to the unit. | 1 | `{ . . . }` |
| `next_event_bonus` | Integer | A modifier to the next event's outcome roll or selection chance. | 1 | `-1`<br>`-2`<br>`1` |
| [`next_event_from_set`](./Miscellaneous.md#object-next_event_from_set) | Object  | Specifies the next event to trigger, or defines a set of events with count and category constraints. | 1 | `{ . . . }` |
| [`random_mutation`](./Miscellaneous.md#object-random_mutation) | Number / Object  | The number of random mutations applied to the unit. | 1 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [`scramble_abilities`](./Enums.md#enum-scramble_abilities) | Enum | Specifies which abilities to randomize, such as 'all'. | 1 | `all` |
| [`scramble_passives`](./Enums.md#enum-scramble_passives) | Enum | Specifies which passive abilities to randomize or scramble. | 1 | `all` |
| [`shop_now`](./Enums.md#enum-shop_now) | Enum | Triggers the specified shop to appear immediately. | 1 | `Event_RareShop`<br>`Event_SmallShop`<br>`Shop` |
| `trigger_butterfly_effect` | Integer | The number of times to trigger the butterfly effect event. | 1 | `1` |
| [`upgrade_ability`](./Enums.md#enum-upgrade_ability) | Enum | Specifies which ability to upgrade. The value 'random' selects a random eligible ability. | 1 | `random` |
| [`upgrade_passive`](./Enums.md#enum-upgrade_passive) | Enum | Specifies which passive ability to upgrade, or 'random' for a random choice. | 1 | `random` |
| [`gain_food`](./Arrays.md#array-gain_food) | Array | An array specifying the minimum and maximum amount of food gained, or a single integer. | 0 | `-5`<br>`20`<br>`30` |
| [`party_gain_disorder_from_pool`](./Arrays.md#array-party_gain_disorder_from_pool) | Array | An array specifying the pool or list of disorders for the party to gain. | 0 | `[Dwarfism]`<br>`[Gigantism]`<br>`all_disorders` |
| [`random_pool`](./Arrays.md#array-random_pool) | Array | An array of possible items or rewards from which one is randomly selected. | 0 | `[` |
| [`random_pool_consider_luck`](./Arrays.md#array-random_pool_consider_luck) | Array | An array or weighted pool of rewards that are rolled considering the unit's luck stat. | 0 | `[` |
| [`transform_item`](./Arrays.md#array-transform_item) | Array | An array specifying source and destination item IDs to transform one into the other. | 0 | `[JarOfRadiatedBlood JarOfChaos]`<br>`[JarOfRadiation JarOfRadiatedBlood]` |

</details>


---


#### `main`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 215

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`rare`](./Enums.md#enum-rare) | Enum | Defines the rare reward block for a boss encounter. | 673 | `1`<br>`10`<br>`15` |
| [`options`](./Arrays.md#array-options) | Array | An array of named option objects within an event, each defining a possible action the player can take. | 210 | `[smash bash open]` |
| [`prompt`](./Enums.md#enum-prompt) | String | The text or localization key for the popup or prompt displayed to the player. | 38 | `"Donate 3 times before you can receive a reward!"`<br>`"EVENT_ABEGGAR_LEAVE"`<br>`"EVENT_ABEGGAR_QUES"` |
| `set_frame` | Integer | The specific animation frame to set for an object or UI element. | 36 | `1`<br>`10`<br>`15` |
| [`setup`](./Miscellaneous.md#object-setup) | Object  | Defines actions or checks to run before the main event logic, often setting up conditions or tokens. | 23 | `{ . . . }` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 10 | `{ . . . }` |
| [`weight`](./Enums.md#enum-weight) | Float | A multiplier or priority value for random selection or effect magnitude. | 10 | `.25`<br>`.5`<br>`1` |
| [`add_weather`](./Enums.md#enum-add_weather) | Enum | Specifies a weather effect type to apply to the current map. | 5 | `AlienOvergrowth`<br>`Birdemic`<br>`GeomagneticStorm` |
| [`requires_flag`](./Enums.md#enum-requires_flag) | Enum | Specifies a named flag that must be unlocked or set for this event or option to appear. | 5 | `GeomagneticStormUnlocked`<br>`MeteorShowerUnlocked`<br>`SolarFlareUnlocked` |
| [`goto`](./Enums.md#enum-goto) | Enum | Determines which labeled point in the event's script to jump to next, controlling flow. | 4 | `end` |
| [`outcome`](./Miscellaneous.md#object-outcome) | Object  | An object defining the possible outcomes of an event, typically containing a random pool or weighted lists of rewards and animations. | 4 | `{ . . . }` |
| [`gain_familiar`](./Enums.md#enum-gain_familiar) | Enum | Specifies which familiar type (by its class name) the unit gains. | 3 | `CharmedBear`<br>`CharmedDaddyShark`<br>`CharmedDustDevil` |
| `max_options` | Integer | The maximum number of event options presented to the player. | 3 | `2`<br>`3` |
| `shuffle_options` | Boolean | If true, randomizes the order of event options presented to the player. | 3 | `true` |
| [`next_event_from_set`](./Enums.md#enum-next_event_from_set) | Enum | Specifies the next event to trigger, or defines a set of events with count and category constraints. | 1 | `CatHole`<br>`Tragedy`<br>`WatchingHead2` |
| `party_heal` | Integer | The amount of health healed for the entire party. | 1 | `1`<br>`10`<br>`100%` |
| [`party_permanent_stats`](./Miscellaneous.md#object-party_permanent_stats) | Object  | An object defining permanent stat increases applied to the party. | 1 | `{ . . . }` |
| [`play_animation`](./Arrays.md#array-play_animation) | Array | Specifies an animation to play, optionally as an array with a probability weight. | 1 | `[resultBlessing .5]`<br>`[resultGood .5]`<br>`[resultLeave 0]` |
| [`self_status_next_fight`](./Miscellaneous.md#object-self_status_next_fight) | Object  | An object defining status effects applied to the unit at the start of the next fight. | 1 | `{ . . . }` |
| [`shop_now`](./Enums.md#enum-shop_now) | Enum | Triggers the specified shop to appear immediately. | 1 | `Event_RareShop`<br>`Event_SmallShop`<br>`Shop` |

</details>


---


#### `rare`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 996

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`self_damage`](./Miscellaneous.md#object-self_damage) | Boolean / Integer / Object  | Defines damage or effects applied to the caster when using the ability. | 436 | `{ . . . }`<br>`1`<br>`10`<br>`100%` |
| [`gain_disorder`](./Enums.md#enum-gain_disorder) | Enum | Specifies a disorder to add to the current cat when this event triggers. | 65 | `AcidReflux`<br>`Albinism`<br>`Anxiety` |
| [`get_item`](./Enums.md#enum-get_item) | Enum | Specifies an item to add to the player's inventory when this event triggers. | 41 | `AlienBlaster`<br>`BagOfGrass`<br>`BearTrapMask` |
| [`prompt`](./Enums.md#enum-prompt) | String | The text or localization key for the popup or prompt displayed to the player. | 38 | `"Donate 3 times before you can receive a reward!"`<br>`"EVENT_ABEGGAR_LEAVE"`<br>`"EVENT_ABEGGAR_QUES"` |
| `set_frame` | Integer | The specific animation frame to set for an object or UI element. | 36 | `1`<br>`10`<br>`15` |
| [`event_now_same_cat`](./Enums.md#enum-event_now_same_cat) | Enum | Specifies a world event that will now occur for the same cat category as the current event. | 30 | `BigToe`<br>`Blessing`<br>`BodyOfGlorg_Gift` |
| [`get_parasite`](./Enums.md#enum-get_parasite) | Enum | Specifies a parasite item to attach to a unit when this event triggers. | 30 | `AlluringDoodie`<br>`BadSplinters`<br>`Beepis` |
| [`set_adventure_token`](./Enums.md#enum-set_adventure_token) | Enum | Specifies an adventure token to set (enable or mark as true) when this event triggers. | 22 | `AdventureToken_BlueNeedle`<br>`AdventureToken_HasRunFromDeath`<br>`AdventureToken_HasTakenNeedle` |
| [`spawn_unit_next_fight`](./Miscellaneous.md#object-spawn_unit_next_fight) | Object  | An object defining a unit to spawn during the next fight, including its object, count, and spawn side. | 20 | `{ . . . }` |
| [`random_mutation_from_set`](./Miscellaneous.md#object-random_mutation_from_set) | Number / Object  | Defines a set of mutation categories and their specific IDs to apply a random mutation from. | 13 | `{ . . . }` |
| [`party_status_next_fight`](./Miscellaneous.md#object-party_status_next_fight) | Object  | An object defining status effects to apply to the party at the start of the next fight. | 12 | `{ . . . }` |
| [`get_item_from_pool`](./Miscellaneous.md#object-get_item_from_pool) | Array / Enum / Object  | Grants an item from the specified pool or a specific item name. | 11 | `{ . . . }`<br>`Bird_items`<br>`Coin_items`<br>`Eye_items` |
| [`learn_passive`](./Enums.md#enum-learn_passive) | Enum | Teaches the unit the specified passive ability. | 10 | `Blessed`<br>`CobraStyle`<br>`DeathProof` |
| [`play_animation`](./Arrays.md#array-play_animation) | Array / Enum | Specifies an animation to play, optionally as an array with a probability weight. | 10 | `[resultBlessing .5]`<br>`[resultGood .5]`<br>`[resultLeave 0]` |
| [`increment_legacy_counter`](./Enums.md#enum-increment_legacy_counter) | Enum | Specifies a legacy counter to increment by one when this event triggers. | 9 | `WorldEventLegacyCounter_CrackInTheWall`<br>`WorldEventLegacyCounter_CustomTokenString`<br>`WorldEventLegacyCounter_FooCounter` |
| `override_end_option_prompt` | String | Specifies a custom prompt string to display for the end option of this event choice. | 8 | `"EVENT_LOCKEDDOOR_PROMPT1"`<br>`"EVENT_LOCKEDDOOR_PROMPT2"`<br>`"EVENT_MYSTERIOUSSTRANGER_END_AGAIN"` |
| [`party_damage`](./Arrays.md#array-party_damage) | Array / Number | An array specifying the minimum and maximum damage dealt to the party, or a single integer or percentage. | 8 | `1`<br>`10`<br>`2` |
| `party_random_mutation` | Integer | The number of random mutations applied to the entire party. | 8 | `1` |
| `ambush_next_basic_fights` | String | The number of basic fights to trigger as ambushes. | 7 | `1` |
| [`leave_party_temporarily`](./Miscellaneous.md#object-leave_party_temporarily) | Object  | Defines parameters for a unit leaving the party temporarily, such as skipped fights and return conditions. | 7 | `{ . . . }` |
| [`lose_item`](./Enums.md#enum-lose_item) | Enum | Specifies which item slot or type to lose (e.g., 'equipped', 'inventory'). | 7 | `equipped`<br>`inventory`<br>`parasite` |
| [`permanent_stats`](./Miscellaneous.md#object-permanent_stats) | Object  | Defines permanent stat changes to apply to the unit (e.g., con, cha). | 7 | `{ . . . }` |
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum | Specifies a legacy token to set (enable or mark as true) when this event triggers. | 7 | `AlienOvergrowthUnlocked`<br>`AntennaQuest_Orb`<br>`AntennaQuest_Rift` |
| [`gain_coins`](./Arrays.md#array-gain_coins) | Array / Number | An array specifying the minimum and maximum amount of coins gained, or a single integer. | 6 | `1`<br>`10`<br>`15` |
| `hide_appearance_changes` | Integer | If set to 1, visual appearance changes from status effects or mutations are not shown on the unit. | 6 | `1` |
| [`shop_now`](./Enums.md#enum-shop_now) | Enum | Triggers the specified shop to appear immediately. | 6 | `Event_RareShop`<br>`Event_SmallShop`<br>`Shop` |
| [`add_weather`](./Enums.md#enum-add_weather) | Enum | Specifies a weather effect type to apply to the current map. | 5 | `AlienOvergrowth`<br>`Birdemic`<br>`GeomagneticStorm` |
| [`decrement_legacy_counter`](./Enums.md#enum-decrement_legacy_counter) | Enum | Specifies which legacy counter or token to decrement by one. | 5 | `WorldEventLegacyCounter_CrackInTheWall`<br>`WorldEventLegacyCounter_CustomTokenString`<br>`WorldEventLegacyToken_StartDigging` |
| `full_heal` | Integer | If set to 1, fully restores the unit's health. | 4 | `1` |
| [`learn_ability`](./Enums.md#enum-learn_ability) | Enum | Specifies which specific ability the target unit learns. | 4 | `BarfBall`<br>`FutureSight` |
| [`gain_familiar`](./Enums.md#enum-gain_familiar) | Enum | Specifies which familiar type (by its class name) the unit gains. | 3 | `CharmedBear`<br>`CharmedDaddyShark`<br>`CharmedDustDevil` |
| [`global_effect_next_fight`](./Miscellaneous.md#object-global_effect_next_fight) | Object  | Defines a global status effect or modifier to apply in the next fight. | 3 | `{ . . . }` |
| [`kill`](./Enums.md#enum-kill) | Enum | Kills the specified target type (e.g., 'cat'). | 3 | `cat` |
| [`lose_item_from_inventory`](./Enums.md#enum-lose_item_from_inventory) | Enum | Specifies which item or item category is removed from the unit's inventory. | 3 | `cat` |
| [`make_old`](./Enums.md#enum-make_old) | Enum | Applies the 'old' status or age increase to the specified target, typically 'self'. | 3 | `self` |
| [`next_event_from_set`](./Miscellaneous.md#object-next_event_from_set) | Enum / Object  | Specifies the next event to trigger, or defines a set of events with count and category constraints. | 3 | `{ . . . }`<br>`CatHole`<br>`Tragedy`<br>`WatchingHead2` |
| [`spawn_reflection_next_fight`](./Miscellaneous.md#object-spawn_reflection_next_fight) | Number / Object  | The number of reflections to spawn in the next battle, optionally with a mutation. | 3 | `{ . . . }`<br>`1` |
| [`damage`](./Arrays.md#array-damage) | Array / Equation  | Specifies the amount of damage dealt, can be a number or expression. | 2 | `"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`battle`](./Math_Equations.md) | Enum / String | Defines a battle encounter by preset, level file path, or reverb settings. | 2 | `"desert/boss/dustdevil/DustDevil.lvl"`<br>`"events/Death.lvl"`<br>`"events/GlowingBear"` |
| [`event_now`](./Enums.md#enum-event_now) | Enum | Triggers the specified event immediately. | 2 | `MeatGolem`<br>`Mirage`<br>`MysteriousMachine_Bad` |
| [`gain_food`](./Arrays.md#array-gain_food) | Array / Number | An array specifying the minimum and maximum amount of food gained, or a single integer. | 2 | `-5`<br>`20`<br>`30` |
| [`get_parasite_from_pool`](./Arrays.md#array-get_parasite_from_pool) | Array / Enum  | Specifies the pool name or explicit list of parasites to obtain from. | 2 | `[AmoebaHat AmoebaNeck AmoebaFace]`<br>`barbed_armor`<br>`barbed_items` |
| [`level_up`](./Enums.md#enum-level_up) | Enum | Specifies which units to level up, such as 'all' or 'self'. | 2 | `all`<br>`self` |
| [`lose_specific_item`](./Enums.md#enum-lose_specific_item) | Enum | Removes the specified item from the player's inventory. | 2 | `CryogenicTimeChamber_Full`<br>`PutridLeech`<br>`PyrophinasCollar` |
| `party_heal_disorder` | Integer | The number of disorders to heal from all party members. | 2 | `2` |
| `party_heal_injury` | Integer | The amount of injury to heal for the entire party. | 2 | `99` |
| [`party_permanent_stats_exclude_self`](./Miscellaneous.md#object-party_permanent_stats_exclude_self) | Object  | An object specifying permanent stat bonuses (str, dex, con, int, spd) applied to all party members except the triggering unit. | 2 | `{ . . . }` |
| `set_age` | Integer | The age value to set for the target unit. | 2 | `1` |
| [`upgrade_ability`](./Enums.md#enum-upgrade_ability) | Enum | Specifies which ability to upgrade. The value 'random' selects a random eligible ability. | 2 | `random` |
| [`upgrade_passive`](./Enums.md#enum-upgrade_passive) | Enum | Specifies which passive ability to upgrade, or 'random' for a random choice. | 2 | `random` |
| `ally_ambush_next_fights` | Integer | The number of upcoming fights that will start with an ally ambush. | 1 | `1`<br>`2` |
| [`ambush`](./Math_Equations.md) | Equation | Specifies the path to a level file for an ambush encounter. | 1 | `"events/chupacabra.lvl"`<br>`putalevelhere.lvl` |
| `clear_result_animation` | Integer | The number of result animations to clear or skip. | 1 | `1` |
| [`conditional_reward`](./Miscellaneous.md#object-conditional_reward) | Object  | An object defining a reward that is granted only if specified conditions are met. | 1 | `{ . . . }` |
| `gain_cat_familiar` | Integer | The number of cat familiars gained. | 1 | `1` |
| [`gain_disorder_from_pool`](./Arrays.md#array-gain_disorder_from_pool) | Array / Enum  | Specifies a pool of disorders from which one is randomly gained. | 1 | `Crazy_disorders`<br>`Steven_disorders`<br>`[BlackFetin OrangeFetin PurpleFetin]` |
| [`gain_immortal_familiar`](./Enums.md#enum-gain_immortal_familiar) | Enum | Specifies the immortal familiar to add to the party. | 1 | `CharmedFlea`<br>`CharmedFleaSpecial`<br>`CharmedPooter` |
| [`get_and_equip_item`](./Enums.md#enum-get_and_equip_item) | Enum | Specifies the item to obtain and immediately equip. | 1 | `Catnip`<br>`FlyLarva` |
| `heal_disorder` | Integer | Specifies which disorder type to heal, or the number of disorders to heal. | 1 | `1`<br>`2`<br>`Anxiety` |
| [`injury`](./Enums.md#enum-injury) | Enum | Specifies the type of injury applied, such as bleeding or stat reduction. | 1 | `bleeding`<br>`burned`<br>`cha` |
| [`learn_ability_from_pool`](./Enums.md#enum-learn_ability_from_pool) | Enum | An array specifying a pool or list of abilities from which one is randomly selected and learned. The string 'AnyUnlocked' selects any unlocked ability. | 1 | `AnyUnlocked`<br>`Necromancer`<br>`[Smack Meow Hiss]` |
| [`learn_passive_from_pool`](./Enums.md#enum-learn_passive_from_pool) | Enum | An array specifying a pool or list of passives from which one is randomly selected and learned. The string 'AnyUnlocked' selects any unlocked passive. | 1 | `AnyUnlocked`<br>`Necromancer`<br>`[MiniMe SkillShare]` |
| [`lose_all_equipped_items`](./Enums.md#enum-lose_all_equipped_items) | Enum | Specifies the target (e.g., 'cat') from which to remove all currently equipped items. | 1 | `cat` |
| [`mutation`](./Miscellaneous.md#object-mutation) | Object  | An object defining specific body part mutations applied to the unit. | 1 | `{ . . . }` |
| `next_event_bonus` | Integer | A modifier to the next event's outcome roll or selection chance. | 1 | `-1`<br>`-2`<br>`1` |
| `party_heal` | Integer | The amount of health healed for the entire party. | 1 | `1`<br>`10`<br>`100%` |
| [`party_injury`](./Enums.md#enum-party_injury) | Enum | Specifies the type of injury to inflict on the party (e.g., 'random'). | 1 | `random` |
| [`party_permanent_stats`](./Miscellaneous.md#object-party_permanent_stats) | Object  | An object defining permanent stat increases applied to the party. | 1 | `{ . . . }` |
| [`party_random_mutation_from_set`](./Miscellaneous.md#object-party_random_mutation_from_set) | Object  | An object specifying the count and mutation parts to randomly apply to the party. | 1 | `{ . . . }` |
| [`play_result_animation`](./Enums.md#enum-play_result_animation) | Enum | Specifies which result animation to play (e.g., 'resultVeryGood'). | 1 | `resultVeryGood` |
| `random_mutation` | Integer | The number of random mutations applied to the unit. | 1 | `1`<br>`10`<br>`2` |
| [`scramble_abilities`](./Enums.md#enum-scramble_abilities) | Enum | Specifies which abilities to randomize, such as 'all'. | 1 | `all` |
| [`scramble_basic_attack`](./Enums.md#enum-scramble_basic_attack) | Enum | Specifies which basic attacks to randomize or scramble. | 1 | `all` |
| [`self_status_next_fight`](./Miscellaneous.md#object-self_status_next_fight) | Object  | An object defining status effects applied to the unit at the start of the next fight. | 1 | `{ . . . }` |
| [`trigger_adventure_unlock`](./Enums.md#enum-trigger_adventure_unlock) | Enum | Triggers the specified adventure or map unlock quest. | 1 | `end_of_time_unlock`<br>`legacy_event_unlock_momsknife`<br>`map_unlock_dimensionx` |
| [`random_pool`](./Arrays.md#array-random_pool) | Array | An array of possible items or rewards from which one is randomly selected. | 0 | `[` |

</details>


---


#### `reward`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 760

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`common`](./Enums.md#enum-common) | Enum | Defines the common reward block for a boss encounter. | 1067 | `100`<br>`14`<br>`5` |
| [`rare`](./Enums.md#enum-rare) | Enum | Defines the rare reward block for a boss encounter. | 673 | `1`<br>`10`<br>`15` |
| [`prompt`](./Enums.md#enum-prompt) | String | The text or localization key for the popup or prompt displayed to the player. | 38 | `"Donate 3 times before you can receive a reward!"`<br>`"EVENT_ABEGGAR_LEAVE"`<br>`"EVENT_ABEGGAR_QUES"` |
| `set_frame` | Integer | The specific animation frame to set for an object or UI element. | 36 | `1`<br>`10`<br>`15` |
| [`clear_adventure_token`](./Enums.md#enum-clear_adventure_token) | Enum | Specifies an adventure token to clear (disable or mark as false) when this event triggers. | 24 | `AdventureToken_BlueNeedle`<br>`AdventureToken_HasTakenNeedle`<br>`AdventureToken_RedNeedle` |
| [`get_item_from_pool`](./Miscellaneous.md#object-get_item_from_pool) | Enum / Object  | Grants an item from the specified pool or a specific item name. | 11 | `{ . . . }`<br>`Bird_items`<br>`Coin_items`<br>`Eye_items` |
| [`set_subject`](./Enums.md#enum-set_subject) | Enum | Specifies which subject or frame to use for the event's visual. | 10 | `dimensionx_head2`<br>`endorb2`<br>`monkey_paw_1finger` |
| [`weight`](./Enums.md#enum-weight) | Float | A multiplier or priority value for random selection or effect magnitude. | 10 | `.25`<br>`.5`<br>`1` |
| [`set_adventure_token`](./Enums.md#enum-set_adventure_token) | Enum | Specifies an adventure token to set (enable or mark as true) when this event triggers. | 9 | `AdventureToken_BlueNeedle`<br>`AdventureToken_HasRunFromDeath`<br>`AdventureToken_HasTakenNeedle` |
| [`trigger_adventure_unlock`](./Enums.md#enum-trigger_adventure_unlock) | Enum | Triggers the specified adventure or map unlock quest. | 5 | `end_of_time_unlock`<br>`legacy_event_unlock_momsknife`<br>`map_unlock_dimensionx` |
| [`play_animation`](./Enums.md#enum-play_animation) | Enum  | Specifies an animation to play, optionally as an array with a probability weight. | 4 | `[resultBlessing .5]`<br>`[resultGood .5]`<br>`[resultLeave 0]` |
| [`cutscene_on_exit`](./Enums.md#enum-cutscene_on_exit) | Enum | Determines which cutscene to play when the player leaves the current location. | 3 | `infinite_intro`<br>`king_intro` |
| [`get_parasite_from_pool`](./Enums.md#enum-get_parasite_from_pool) | Enum | Specifies the pool name or explicit list of parasites to obtain from. | 2 | `[AmoebaHat AmoebaNeck AmoebaFace]`<br>`barbed_armor`<br>`barbed_items` |
| [`level_up`](./Enums.md#enum-level_up) | Enum | Specifies which units to level up, such as 'all' or 'self'. | 2 | `all`<br>`self` |
| [`spawn_unit_next_fight`](./Miscellaneous.md#object-spawn_unit_next_fight) | Object  | An object defining a unit to spawn during the next fight, including its object, count, and spawn side. | 2 | `{ . . . }` |
| `ambush_next_basic_fights` | Integer | The number of basic fights to trigger as ambushes. | 1 | `1` |
| [`event_now`](./Enums.md#enum-event_now) | Enum | Triggers the specified event immediately. | 1 | `MeatGolem`<br>`Mirage`<br>`MysteriousMachine_Bad` |
| [`gain_coins`](./Arrays.md#array-gain_coins) | Array / Number | An array specifying the minimum and maximum amount of coins gained, or a single integer. | 1 | `1`<br>`10`<br>`15` |
| [`gain_disorder_from_pool`](./Enums.md#enum-gain_disorder_from_pool) | Enum | Specifies a pool of disorders from which one is randomly gained. | 1 | `Crazy_disorders`<br>`Steven_disorders`<br>`[BlackFetin OrangeFetin PurpleFetin]` |
| [`get_item`](./Enums.md#enum-get_item) | Enum | Specifies an item to add to the player's inventory when this event triggers. | 1 | `AlienBlaster`<br>`BagOfGrass`<br>`BearTrapMask` |
| [`injury`](./Enums.md#enum-injury) | Enum | Specifies the type of injury applied, such as bleeding or stat reduction. | 1 | `bleeding`<br>`burned`<br>`cha` |
| `next_event_bonus` | Integer | A modifier to the next event's outcome roll or selection chance. | 1 | `-1`<br>`-2`<br>`1` |
| [`random_chance`](./Miscellaneous.md#object-random_chance) | Object  | Defines a block with a percentage chance and an action to execute if the chance succeeds. | 1 | `{ . . . }` |
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum | Specifies a legacy token to set (enable or mark as true) when this event triggers. | 1 | `AlienOvergrowthUnlocked`<br>`AntennaQuest_Orb`<br>`AntennaQuest_Rift` |
| [`party_damage`](./Arrays.md#array-party_damage) | Array | An array specifying the minimum and maximum damage dealt to the party, or a single integer or percentage. | 0 | `1`<br>`10`<br>`2` |
| [`random_pool`](./Arrays.md#array-random_pool) | Array | An array of possible items or rewards from which one is randomly selected. | 0 | `[` |

</details>


---


## Auto-Discovered Objects


### Object: `Albinism`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | String | Specifies the class that this ability belongs to, used for categorization and restrictions. | 1 | `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


### Object: `AlienOvergrowth`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 1 | `{ . . . }` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |

</details>


### Object: `Anxiety`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | String | Specifies the class that this ability belongs to, used for categorization and restrictions. | 1 | `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


### Object: `Beepis`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cursed` | Boolean | If true, the item is cursed and may have negative effects when equipped or used. | 1 | `true` |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Number | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `parasite` | Boolean | If true, the item is a parasite that attaches to a unit and cannot be removed normally. | 1 | `true` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


### Object: `Bottles`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | String | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `durability` | Number | The amount of durability consumed by this ability or required for its use. | 1 | `0`<br>`1`<br>`10` |
| `frame` | Number | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `rarity` | String | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |

</details>


### Object: `BrainDamage`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | String | Specifies the class that this ability belongs to, used for categorization and restrictions. | 1 | `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


### Object: `BrainDead`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | String | Specifies the class that this ability belongs to, used for categorization and restrictions. | 1 | `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |

</details>


### Object: `Brave`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | String | Specifies the class that this ability belongs to, used for categorization and restrictions. | 1 | `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


### Object: `Cancer`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Specifies the localized description string for the item or ability. | 2 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 2 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| `class` | String | Specifies the class that this ability belongs to, used for categorization and restrictions. | 1 | `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |
| `frame` | Number | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| `rarity` | String | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |
| `set` | String | Specifies the set name(s) the item belongs to for set bonuses. | 1 | `80s`<br>`90s`<br>`AdvancedAlloy` |

</details>


### Object: `CharmedMaggot`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `CharmedPinky`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `CharmedRaptorBaby`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `CharmedTarBaby`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `CryogenicTimeChamber_Empty`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Number | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| [`global_passives`](./Miscellaneous.md#object-global_passives) | Object  | An object containing global passive modifiers that apply to the entire run. | 1 | `{ . . . }` |
| `hint_destination` | String | Specifies the map destination hinted by this item or event. | 1 | `boneyard`<br>`caves`<br>`core` |
| `hint_prerequisite_flag` | String | Defines a map flag that must be set for the hint to appear. | 1 | `mapflag_BothObelisksUnlocked`<br>`mapflag_DimensionXUnlocked`<br>`mapflag_MeatWorldUnlocked` |
| `indestructible` | Boolean | If true, the item cannot be destroyed or removed. | 1 | `true` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| `legacy_quest` | Boolean | If true, this item is part of a legacy quest. | 1 | `true` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `quest_item` | Boolean | If true, this item is a quest item and cannot be sold or destroyed. | 1 | `false`<br>`true` |
| `rarity` | String | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |

</details>


### Object: `CryogenicTimeChamber_Full`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Number | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| [`global_passives`](./Miscellaneous.md#object-global_passives) | Object  | An object containing global passive modifiers that apply to the entire run. | 1 | `{ . . . }` |
| `hint_destination` | String | Specifies the map destination hinted by this item or event. | 1 | `boneyard`<br>`caves`<br>`core` |
| `indestructible` | Boolean | If true, the item cannot be destroyed or removed. | 1 | `true` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| `legacy_quest` | Boolean | If true, this item is part of a legacy quest. | 1 | `true` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `quest_item` | Boolean | If true, this item is a quest item and cannot be sold or destroyed. | 1 | `false`<br>`true` |
| `rarity` | String | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |

</details>


### Object: `Cunch`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cursed` | Boolean | If true, the item is cursed and may have negative effects when equipped or used. | 1 | `true` |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Number | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `parasite` | Boolean | If true, the item is a parasite that attaches to a unit and cannot be removed normally. | 1 | `true` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


### Object: `CursedStickman`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cursed` | Boolean | If true, the item is cursed and may have negative effects when equipped or used. | 1 | `true` |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Number | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `rarity` | String | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |
| [`set`](./Arrays.md#array-set) | Array  | Specifies the set name(s) the item belongs to for set bonuses. | 1 | `80s`<br>`90s`<br>`AdvancedAlloy` |

</details>


### Object: `DeathsScythe`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | String | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Number | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `rarity` | String | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |

</details>


### Object: `Depression`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | String | Specifies the class that this ability belongs to, used for categorization and restrictions. | 1 | `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |

</details>


### Object: `EnchantingPoop`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Number | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `set` | String | Specifies the set name(s) the item belongs to for set bonuses. | 1 | `80s`<br>`90s`<br>`AdvancedAlloy` |

</details>


### Object: `FecalHood_Cursed`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cursed` | Boolean | If true, the item is cursed and may have negative effects when equipped or used. | 1 | `true` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `FecalMask_Cursed`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cursed` | Boolean | If true, the item is cursed and may have negative effects when equipped or used. | 1 | `true` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `Feebis`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `attack` | String | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| `cursed` | Boolean | If true, the item is cursed and may have negative effects when equipped or used. | 1 | `true` |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Number | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `parasite` | Boolean | If true, the item is a parasite that attaches to a unit and cannot be removed normally. | 1 | `true` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


### Object: `GeomagneticStorm`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 1 | `{ . . . }` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |

</details>


### Object: `Gigachad`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | String | Specifies the class that this ability belongs to, used for categorization and restrictions. | 1 | `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |

</details>


### Object: `GuillotinasHead`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cursed` | Boolean | If true, the item is cursed and may have negative effects when equipped or used. | 1 | `true` |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Number | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| [`global_tags`](./Arrays.md#array-global_tags) | Array   | A list of global tags that modify the run's behavior. | 1 | `[`<br>`[all_cats_are_jester]`<br>`[all_normal_events_are_weather]` |
| `hint_destination` | String | Specifies the map destination hinted by this item or event. | 1 | `boneyard`<br>`caves`<br>`core` |
| `hint_prerequisite_flag` | String | Defines a map flag that must be set for the hint to appear. | 1 | `mapflag_BothObelisksUnlocked`<br>`mapflag_DimensionXUnlocked`<br>`mapflag_MeatWorldUnlocked` |
| `indestructible` | Boolean | If true, the item cannot be destroyed or removed. | 1 | `true` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| `legacy_quest` | Boolean | If true, this item is part of a legacy quest. | 1 | `true` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `quest_item` | Boolean | If true, this item is a quest item and cannot be sold or destroyed. | 1 | `false`<br>`true` |
| `rarity` | String | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |
| [`set`](./Arrays.md#array-set) | Array  | Specifies the set name(s) the item belongs to for set bonuses. | 1 | `80s`<br>`90s`<br>`AdvancedAlloy` |

</details>


### Object: `HauntedNight`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 1 | `{ . . . }` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |

</details>


### Object: `Host`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](./Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| `class` | String | Specifies the class that this ability belongs to, used for categorization and restrictions. | 1 | `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |

</details>


### Object: `JarOfChaos`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | String | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. | 1 | `1`<br>`2`<br>`true` |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `dont_destroy_on_0` | Boolean | If true, the item is not destroyed when its charges reach zero. | 1 | `true` |
| `durability` | Number | The amount of durability consumed by this ability or required for its use. | 1 | `0`<br>`1`<br>`10` |
| `failable` | Boolean | If true, the event or action has a chance to fail. | 1 | `true` |
| `frame` | Number | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| `indestructible` | Boolean | If true, the item cannot be destroyed or removed. | 1 | `true` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| `legacy_quest` | Boolean | If true, this item is part of a legacy quest. | 1 | `true` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `quest_item` | Boolean | If true, this item is a quest item and cannot be sold or destroyed. | 1 | `false`<br>`true` |
| `rarity` | String | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |
| `set` | String | Specifies the set name(s) the item belongs to for set bonuses. | 1 | `80s`<br>`90s`<br>`AdvancedAlloy` |

</details>


### Object: `JarOfRadiatedBlood`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `failable` | Boolean | If true, the event or action has a chance to fail. | 1 | `true` |
| `frame` | Number | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| `hint_destination` | String | Specifies the map destination hinted by this item or event. | 1 | `boneyard`<br>`caves`<br>`core` |
| `indestructible` | Boolean | If true, the item cannot be destroyed or removed. | 1 | `true` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| `legacy_quest` | Boolean | If true, this item is part of a legacy quest. | 1 | `true` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `quest_item` | Boolean | If true, this item is a quest item and cannot be sold or destroyed. | 1 | `false`<br>`true` |
| `rarity` | String | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |
| `set` | String | Specifies the set name(s) the item belongs to for set bonuses. | 1 | `80s`<br>`90s`<br>`AdvancedAlloy` |

</details>


### Object: `JarOfRadiation`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `failable` | Boolean | If true, the event or action has a chance to fail. | 1 | `true` |
| `frame` | Number | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| `hint_destination` | String | Specifies the map destination hinted by this item or event. | 1 | `boneyard`<br>`caves`<br>`core` |
| `indestructible` | Boolean | If true, the item cannot be destroyed or removed. | 1 | `true` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| `legacy_quest` | Boolean | If true, this item is part of a legacy quest. | 1 | `true` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `quest_item` | Boolean | If true, this item is a quest item and cannot be sold or destroyed. | 1 | `false`<br>`true` |
| `rarity` | String | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |
| `set` | String | Specifies the set name(s) the item belongs to for set bonuses. | 1 | `80s`<br>`90s`<br>`AdvancedAlloy` |

</details>


### Object: `MomsKnife`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | String | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Number | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `rarity` | String | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |
| `set` | String | Specifies the set name(s) the item belongs to for set bonuses. | 1 | `80s`<br>`90s`<br>`AdvancedAlloy` |

</details>


### Object: `MysteriousTomb1`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`intro`](./NPC_Scripts.md#object-intro) | Object  | An object defining the introductory cutscene for the event, including title, cat selection, and visuals. | 1 | `{ . . . }` |
| [`main`](./Miscellaneous.md#object-main) | Object  | An object containing the primary prompt and options for an event. | 1 | `{ . . . }` |

</details>


### Object: `MysteriousTomb2`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`intro`](./NPC_Scripts.md#object-intro) | Object  | An object defining the introductory cutscene for the event, including title, cat selection, and visuals. | 1 | `{ . . . }` |
| [`main`](./Miscellaneous.md#object-main) | Object  | An object containing the primary prompt and options for an event. | 1 | `{ . . . }` |

</details>


### Object: `PawShards`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cursed` | Boolean | If true, the item is cursed and may have negative effects when equipped or used. | 1 | `true` |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Number | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


### Object: `PuncturedEye`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bonus_items`](./Arrays.md#array-bonus_items) | Array   | An array of item names granted as bonus rewards. | 1 | `[Eyeball]`<br>`[FoodBig FoodBig FoodBig FoodBig]`<br>`[Pipe]` |
| `class` | String | Specifies the class that this ability belongs to, used for categorization and restrictions. | 1 | `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`lock_item_slot`](./Passives_and_Statuses.md#object-lock_item_slot) | Object  | An object that restricts which equipment slots can be used. | 1 | `{ . . . }` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


### Object: `PutridLeech`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cursed` | Boolean | If true, the item is cursed and may have negative effects when equipped or used. | 1 | `true` |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Number | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| `hint_destination` | String | Specifies the map destination hinted by this item or event. | 1 | `boneyard`<br>`caves`<br>`core` |
| `indestructible` | Boolean | If true, the item cannot be destroyed or removed. | 1 | `true` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| `legacy_quest` | Boolean | If true, this item is part of a legacy quest. | 1 | `true` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `parasite` | Boolean | If true, the item is a parasite that attaches to a unit and cannot be removed normally. | 1 | `true` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `prevent_level_up` | Boolean | If true, the cat cannot gain experience or level up. | 1 | `true` |
| `quest_item` | Boolean | If true, this item is a quest item and cannot be sold or destroyed. | 1 | `false`<br>`true` |
| `rarity` | String | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |
| `set` | String | Specifies the set name(s) the item belongs to for set bonuses. | 1 | `80s`<br>`90s`<br>`AdvancedAlloy` |

</details>


### Object: `PyrophinasCollar`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Number | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| [`global_tags`](./Arrays.md#array-global_tags) | Array   | A list of global tags that modify the run's behavior. | 1 | `[`<br>`[all_cats_are_jester]`<br>`[all_normal_events_are_weather]` |
| `hint_destination` | String | Specifies the map destination hinted by this item or event. | 1 | `boneyard`<br>`caves`<br>`core` |
| `hint_prerequisite_flag` | String | Defines a map flag that must be set for the hint to appear. | 1 | `mapflag_BothObelisksUnlocked`<br>`mapflag_DimensionXUnlocked`<br>`mapflag_MeatWorldUnlocked` |
| `indestructible` | Boolean | If true, the item cannot be destroyed or removed. | 1 | `true` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| `legacy_quest` | Boolean | If true, this item is part of a legacy quest. | 1 | `true` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `quest_item` | Boolean | If true, this item is a quest item and cannot be sold or destroyed. | 1 | `false`<br>`true` |
| `rarity` | String | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |
| `set` | String | Specifies the set name(s) the item belongs to for set bonuses. | 1 | `80s`<br>`90s`<br>`AdvancedAlloy` |

</details>


### Object: `ReceiverAntenna`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Number | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| [`global_tags`](./Arrays.md#array-global_tags) | Array   | A list of global tags that modify the run's behavior. | 1 | `[`<br>`[all_cats_are_jester]`<br>`[all_normal_events_are_weather]` |
| `hint_destination` | String | Specifies the map destination hinted by this item or event. | 1 | `boneyard`<br>`caves`<br>`core` |
| `indestructible` | Boolean | If true, the item cannot be destroyed or removed. | 1 | `true` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| `legacy_quest` | Boolean | If true, this item is part of a legacy quest. | 1 | `true` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `quest_item` | Boolean | If true, this item is a quest item and cannot be sold or destroyed. | 1 | `false`<br>`true` |
| `rarity` | String | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |
| [`set`](./Arrays.md#array-set) | Array  | Specifies the set name(s) the item belongs to for set bonuses. | 1 | `80s`<br>`90s`<br>`AdvancedAlloy` |
| `shield` | Number | The shield value granted by this mutation, or 'aux' to use the unit's auxiliary stat. | 1 | `"max((aux-1)*2, 0)"`<br>`1`<br>`10` |

</details>


### Object: `RestlessDead`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 1 | `{ . . . }` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |

</details>


### Object: `Rocks`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | String | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `durability` | Number | The amount of durability consumed by this ability or required for its use. | 1 | `0`<br>`1`<br>`10` |
| `frame` | Number | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `rarity` | String | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |
| `set` | String | Specifies the set name(s) the item belongs to for set bonuses. | 1 | `80s`<br>`90s`<br>`AdvancedAlloy` |

</details>


### Object: `Scatological`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | String | Specifies the class that this ability belongs to, used for categorization and restrictions. | 1 | `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


### Object: `SignalAmplifier`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | String | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Number | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| `hint_destination` | String | Specifies the map destination hinted by this item or event. | 1 | `boneyard`<br>`caves`<br>`core` |
| `hint_prerequisite_flag` | String | Defines a map flag that must be set for the hint to appear. | 1 | `mapflag_BothObelisksUnlocked`<br>`mapflag_DimensionXUnlocked`<br>`mapflag_MeatWorldUnlocked` |
| `indestructible` | Boolean | If true, the item cannot be destroyed or removed. | 1 | `true` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| `legacy_quest` | Boolean | If true, this item is part of a legacy quest. | 1 | `true` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `quest_item` | Boolean | If true, this item is a quest item and cannot be sold or destroyed. | 1 | `false`<br>`true` |
| `rarity` | String | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |
| [`set`](./Arrays.md#array-set) | Array  | Specifies the set name(s) the item belongs to for set bonuses. | 1 | `80s`<br>`90s`<br>`AdvancedAlloy` |

</details>


### Object: `SlagMight`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | String | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Number | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `rarity` | String | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |
| `set` | String | Specifies the set name(s) the item belongs to for set bonuses. | 1 | `80s`<br>`90s`<br>`AdvancedAlloy` |

</details>


### Object: `SlagTight`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cursed` | Boolean | If true, the item is cursed and may have negative effects when equipped or used. | 1 | `true` |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Number | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| `int` | Number | The Intelligence stat value or modifier. | 1 | `-1`<br>`-10`<br>`-2` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `shield` | Number | The shield value granted by this mutation, or 'aux' to use the unit's auxiliary stat. | 1 | `"max((aux-1)*2, 0)"`<br>`1`<br>`10` |

</details>


### Object: `SludgeHat`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cha` | Number | The Charisma stat value or modifier. | 1 | `+1`<br>`-1`<br>`-2` |
| `cursed` | Boolean | If true, the item is cursed and may have negative effects when equipped or used. | 1 | `true` |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Number | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `set` | String | Specifies the set name(s) the item belongs to for set bonuses. | 1 | `80s`<br>`90s`<br>`AdvancedAlloy` |
| `shield` | Number | The shield value granted by this mutation, or 'aux' to use the unit's auxiliary stat. | 1 | `"max((aux-1)*2, 0)"`<br>`1`<br>`10` |

</details>


### Object: `SludgeMask`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cha` | Number | The Charisma stat value or modifier. | 1 | `+1`<br>`-1`<br>`-2` |
| `cursed` | Boolean | If true, the item is cursed and may have negative effects when equipped or used. | 1 | `true` |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Number | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `set` | String | Specifies the set name(s) the item belongs to for set bonuses. | 1 | `80s`<br>`90s`<br>`AdvancedAlloy` |
| `shield` | Number | The shield value granted by this mutation, or 'aux' to use the unit's auxiliary stat. | 1 | `"max((aux-1)*2, 0)"`<br>`1`<br>`10` |

</details>


### Object: `Soulless`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | String | Specifies the class that this ability belongs to, used for categorization and restrictions. | 1 | `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


### Object: `Stinky`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | String | Specifies the class that this ability belongs to, used for categorization and restrictions. | 1 | `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


### Object: `StrangeEggs`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 1 | `{ . . . }` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |

</details>


### Object: `TheShimmer`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 1 | `{ . . . }` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |

</details>


### Object: `ThrobbingGristle`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | String | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Number | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| [`global_passives`](./Miscellaneous.md#object-global_passives) | Object  | An object containing global passive modifiers that apply to the entire run. | 1 | `{ . . . }` |
| `hint_destination` | String | Specifies the map destination hinted by this item or event. | 1 | `boneyard`<br>`caves`<br>`core` |
| `indestructible` | Boolean | If true, the item cannot be destroyed or removed. | 1 | `true` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| `legacy_quest` | Boolean | If true, this item is part of a legacy quest. | 1 | `true` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `quest_item` | Boolean | If true, this item is a quest item and cannot be sold or destroyed. | 1 | `false`<br>`true` |
| `rarity` | String | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |
| `set` | String | Specifies the set name(s) the item belongs to for set bonuses. | 1 | `80s`<br>`90s`<br>`AdvancedAlloy` |

</details>


### Object: `Touched`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | String | Specifies the class that this ability belongs to, used for categorization and restrictions. | 1 | `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |

</details>


### Object: `TransmitterAntenna`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Number | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| `hint_destination` | String | Specifies the map destination hinted by this item or event. | 1 | `boneyard`<br>`caves`<br>`core` |
| `indestructible` | Boolean | If true, the item cannot be destroyed or removed. | 1 | `true` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| `legacy_quest` | Boolean | If true, this item is part of a legacy quest. | 1 | `true` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `quest_item` | Boolean | If true, this item is a quest item and cannot be sold or destroyed. | 1 | `false`<br>`true` |
| `rarity` | String | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |
| [`set`](./Arrays.md#array-set) | Array  | Specifies the set name(s) the item belongs to for set bonuses. | 1 | `80s`<br>`90s`<br>`AdvancedAlloy` |

</details>


### Object: `ZaratanasCollar`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Number | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| [`global_tags`](./Arrays.md#array-global_tags) | Array   | A list of global tags that modify the run's behavior. | 1 | `[`<br>`[all_cats_are_jester]`<br>`[all_normal_events_are_weather]` |
| `hint_destination` | String | Specifies the map destination hinted by this item or event. | 1 | `boneyard`<br>`caves`<br>`core` |
| `hint_prerequisite_flag` | String | Defines a map flag that must be set for the hint to appear. | 1 | `mapflag_BothObelisksUnlocked`<br>`mapflag_DimensionXUnlocked`<br>`mapflag_MeatWorldUnlocked` |
| `indestructible` | Boolean | If true, the item cannot be destroyed or removed. | 1 | `true` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| `legacy_quest` | Boolean | If true, this item is part of a legacy quest. | 1 | `true` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `quest_item` | Boolean | If true, this item is a quest item and cannot be sold or destroyed. | 1 | `false`<br>`true` |
| `rarity` | String | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |
| `set` | String | Specifies the set name(s) the item belongs to for set bonuses. | 1 | `80s`<br>`90s`<br>`AdvancedAlloy` |

</details>


### Object: `bleeding`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `deathsound` | String | The name of the sound effect played when the unit dies from this injury. | 1 | `Injury_Bleed`<br>`Injury_BrokenLeg`<br>`Injury_BrokenPaw` |
| `id` | Number | The unique numerical identifier for this injury or status effect. | 1 | `-1`<br>`0`<br>`1` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| `text` | String | The localization key for the name of this injury. | 1 | `""`<br>`"COMBAT_POPUP_RECHARGED"`<br>`"INJURY_NAME_BROKENLEG"` |

</details>


### Object: `burned`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `deathsound` | String | The name of the sound effect played when the unit dies from this injury. | 1 | `Injury_Bleed`<br>`Injury_BrokenLeg`<br>`Injury_BrokenPaw` |
| `id` | Number | The unique numerical identifier for this injury or status effect. | 1 | `-1`<br>`0`<br>`1` |
| [`scars`](./Miscellaneous.md#object-scars) | Object  | An object mapping body parts to ranges of scar texture indices applied on injury. | 1 | `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| `text` | String | The localization key for the name of this injury. | 1 | `""`<br>`"COMBAT_POPUP_RECHARGED"`<br>`"INJURY_NAME_BROKENLEG"` |

</details>


### Object: `chapter_specific_item`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `current_chapter_common` | Number | A variable controlling the number of common item drops for the current chapter. | 1 | `55`<br>`auto` |
| `current_chapter_rare` | Number | A variable controlling the number of rare item drops for the current chapter. | 1 | `10`<br>`auto` |
| `current_chapter_uncommon` | Number | The weight or value for uncommon items specific to the current chapter. | 1 | `35`<br>`auto` |
| `current_chapter_very_rare` | Number | The weight or value for very rare items specific to the current chapter. | 1 | `1`<br>`auto` |

</details>


### Object: `end_of_time_unlock`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `set_mapgen_flag` | String | The name of a map generation flag to set when this event triggers. | 1 | `BoneyardUnlocked`<br>`BothObelisksUnlocked`<br>`BunkerUnlocked` |

</details>


### Object: `legacy_event_unlock_momsknife`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`popup`](./Progression_Unlocks.md#object-popup) | Object  | An object defining a popup notification with prompt and optional unlock. | 1 | `{ . . . }` |
| `unlock_item` | String | The name of the item unlocked by this event. | 1 | `MomsKnife` |

</details>


### Object: `map_unlock_dimensionx`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `set_mapgen_flag` | String | The name of a map generation flag to set when this event triggers. | 1 | `BoneyardUnlocked`<br>`BothObelisksUnlocked`<br>`BunkerUnlocked` |

</details>


### Object: `map_unlock_iceage`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`popup`](./Progression_Unlocks.md#object-popup) | Object  | An object defining a popup notification with prompt and optional unlock. | 1 | `{ . . . }` |
| `set_mapgen_flag` | String | The name of a map generation flag to set when this event triggers. | 1 | `BoneyardUnlocked`<br>`BothObelisksUnlocked`<br>`BunkerUnlocked` |

</details>


### Object: `meat_world_open`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `set_mapgen_flag` | String | The name of a map generation flag to set when this event triggers. | 1 | `BoneyardUnlocked`<br>`BothObelisksUnlocked`<br>`BunkerUnlocked` |

</details>


### Object: `radiated`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `deathsound` | String | The name of the sound effect played when the unit dies from this injury. | 1 | `Injury_Bleed`<br>`Injury_BrokenLeg`<br>`Injury_BrokenPaw` |
| `id` | Number | The unique numerical identifier for this injury or status effect. | 1 | `-1`<br>`0`<br>`1` |
| [`scars`](./Miscellaneous.md#object-scars) | Object  | An object mapping body parts to ranges of scar texture indices applied on injury. | 1 | `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| `text` | String | The localization key for the name of this injury. | 1 | `""`<br>`"COMBAT_POPUP_RECHARGED"`<br>`"INJURY_NAME_BROKENLEG"` |

</details>


### Object: `time_machine_quest_finalstep`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `trigger_npc_sequence` | String | The name of an NPC dialogue sequence to trigger. | 1 | `beanies_begin_accepting_cats`<br>`beanies_bombquest_2`<br>`beanies_bombquest_3` |

</details>


### Object: `time_machine_quest_trigger`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `trigger_npc_sequence` | String | The name of an NPC dialogue sequence to trigger. | 1 | `beanies_begin_accepting_cats`<br>`beanies_bombquest_2`<br>`beanies_bombquest_3` |

</details>