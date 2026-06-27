# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Events & Encounters

> **Associated Files:** `data/events/`


### Object: `ROOT`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 214

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 664 | `common`<br>`rare`<br>`cha` |
| [`intro`](./NPC_Scripts.md#object-intro) | Object  | An object defining the introductory cutscene for the event, including title, cat selection, and visuals. | 239 | `{ . . . }` |
| [`main`](./Miscellaneous.md#object-main) | Object  | An object containing the primary prompt and options for an event. | 227 | `{ . . . }` |
| [`self_damage`](./Miscellaneous.md#object-self_damage) | Boolean / Integer / Object  | Defines damage or effects applied to the caster when using the ability. | 218 | `{ . . . }`<br>`1`<br>`10`<br>`100%` |
| [`cha`](./Enums.md#enum-cha) | Enum / Integer  | The Charisma stat value or modifier. | 89 | `+1`<br>`-1`<br>`-2` |
| [`con`](./Enums.md#enum-con) | Enum / Integer  | The Constitution stat value or modifier. | 79 | `-1`<br>`-2`<br>`-3` |
| [`spd`](./Enums.md#enum-spd) | Enum / Integer  | The Speed stat value or modifier. | 78 | `-1`<br>`-10`<br>`-2` |
| [`int`](./Enums.md#enum-int) | Enum / Integer  || 66 | `-1`<br>`-10`<br>`-2` |
| [`lck`](./Enums.md#enum-lck) | Enum / Integer  || 53 | `-1`<br>`-2`<br>`-3` |
| [`str`](./Enums.md#enum-str) | Enum / Integer  || 45 | `-1`<br>`-2`<br>`-3` |
| [`rare`](./Enums.md#enum-rare) | Enum  | Defines the rare reward block for a boss encounter. | 34 | `1`<br>`10`<br>`15` |
| [`dex`](./Enums.md#enum-dex) | Enum / Integer  || 30 | `-1`<br>`-2`<br>`-3` |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String || 25 | `"desert/boss/dustdevil/DustDevil.lvl"`<br>`"events/Death.lvl"`<br>`"events/GlowingBear"` |
| [`normal`](./Arrays.md#array-normal) | Array  || 23 | `[` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 13 | `{ . . . }` |
| [`common`](./Enums.md#enum-common) | Enum  | Defines the common reward block for a boss encounter. | 11 | `100`<br>`14`<br>`5` |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | String || 9 | `BlackShard`<br>`CryogenicTimeChamber_Empty`<br>`CryogenicTimeChamber_Full` |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String || 4 | `"Donate 3 times before you can receive a reward!"`<br>`"EVENT_ABEGGAR_LEAVE"`<br>`"EVENT_ABEGGAR_QUES"` |
| `set_frame` | `Number` || 4 | `1`<br>`10`<br>`15` |
| [`label`](./Strings.md#string-label) | String || 3 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Variable || 3 | `cha`<br>`coins`<br>`con` |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 3 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 3 | `false`<br>`true` |
| [`reward`](./Miscellaneous.md#object-reward) | Object  | An object containing sub-objects defining the rewards for different rarity tiers (e.g., common, rare), each with their own set of actions and items. | 3 | `{ . . . }` |
| [`pick`](./Miscellaneous.md#object-pick) | Object  | An object defining the player action to pick or collect an object, including its stat check and outcomes. | 2 | `{ . . . }` |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | String | Grants an item from the specified pool or a specific item name. | 1 | `Bird_items`<br>`Coin_items`<br>`Eye_items` |
| `weight` | `Number` | A multiplier or priority value for random selection or effect magnitude. | 1 | `.25`<br>`.5`<br>`1` |
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum || 1 | `choice_no_coins` |
| `stat_max` | Number || 1 | `1`<br>`10`<br>`15` |
| `stat_min` | Number || 1 | `1`<br>`10`<br>`15` |
| [`open`](./Miscellaneous.md#object-open) | Object  | An object defining the player action to open a container, including its stat check and outcomes. | 1 | `{ . . . }` |
| [`smash`](./Miscellaneous.md#object-smash) | Object  | An object defining the player action to smash an object, including its stat check and outcomes. | 1 | `{ . . . }` |
| [`conditional_reward`](./Miscellaneous.md#object-conditional_reward) | Object  | An object defining a reward that is granted only if specified conditions are met. | 1 | `{ . . . }` |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Specifies the name of a cutscene to play. | 1 | `"chaos_ending_bad"`<br>`"chaos_ending_good"`<br>`"chapterintros/bunker"` |
| [`destroy`](./Miscellaneous.md#object-destroy) | Object  | An object defining the player action to destroy an object, including its stat check and outcomes. | 1 | `{ . . . }` |
| [`mutation`](./Miscellaneous.md#object-mutation) | Object  | An object defining specific body part mutations applied to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `reward`


**Definition:** Event Object: Story branch or dialog option representing the 'Reward' action.  
**Total Count:** 757

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`bad`](./Events_and_Encounters.md#context-bad), [`conditional_reward`](./Events_and_Encounters.md#context-conditional_reward), [`good`](./Events_and_Encounters.md#context-good)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 759 | `common`<br>`rare`<br>`cha` |
| [`common`](./Enums.md#enum-common) | Enum  | Defines the common reward block for a boss encounter. | 633 | `100`<br>`14`<br>`5` |
| [`rare`](./Enums.md#enum-rare) | Enum  | Defines the rare reward block for a boss encounter. | 623 | `1`<br>`10`<br>`15` |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String || 70 | `"Donate 3 times before you can receive a reward!"`<br>`"EVENT_ABEGGAR_LEAVE"`<br>`"EVENT_ABEGGAR_QUES"` |
| `set_frame` | `Number` || 53 | `1`<br>`10`<br>`15` |
| [`set_subject`](./Engine_EventKeys.md#valid-property-keys) | `String` || 10 | `dimensionx_head2`<br>`endorb2`<br>`monkey_paw_1finger` |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | String | Grants an item from the specified pool or a specific item name. | 9 | `Bird_items`<br>`Coin_items`<br>`Eye_items` |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | `String` || 9 | `AdventureToken_BlueNeedle`<br>`AdventureToken_HasRunFromDeath`<br>`AdventureToken_HasTakenNeedle` |
| [`random_pool`](./Arrays.md#array-random_pool) | Array  || 8 | `[` |
| [`clear_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | String || 6 | `AdventureToken_BlueNeedle`<br>`AdventureToken_HasTakenNeedle`<br>`AdventureToken_RedNeedle` |
| `next_event_bonus` | Number || 5 | `-1`<br>`-2`<br>`1` |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | `String` || 5 | `end_of_time_unlock`<br>`legacy_event_unlock_momsknife`<br>`map_unlock_dimensionx` |
| [`play_animation`](./Arrays.md#array-play_animation) | Array  || 4 | `[resultBlessing .5]`<br>`[resultGood .5]`<br>`[resultLeave 0]` |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | `String` || 3 | `infinite_intro`<br>`king_intro` |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | String || 2 | `Crazy_disorders`<br>`Steven_disorders`<br>`[BlackFetin OrangeFetin PurpleFetin]` |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | String || 2 | `bleeding`<br>`burned`<br>`cha` |
| [`gain_coins`](./Arrays.md#array-gain_coins) | Array  || 2 | `1`<br>`10`<br>`15` |
| `ambush_next_basic_fights` | Number || 1 | `1` |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | String || 1 | `MeatGolem`<br>`Mirage`<br>`MysteriousMachine_Bad` |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | String || 1 | `[AmoebaHat AmoebaNeck AmoebaFace]`<br>`barbed_armor`<br>`barbed_items` |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | String || 1 | `all`<br>`self` |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 | `AlienOvergrowthUnlocked`<br>`AntennaQuest_Orb`<br>`AntennaQuest_Rift` |
| [`party_damage`](./Arrays.md#array-party_damage) | Array / Integer  || 1 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `common`


**Definition:** Event Node: Story branch or dialog option representing the 'Common' action.  
**Total Count:** 633

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`reward`](./Events_and_Encounters.md#context-reward)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 634 | `common`<br>`rare`<br>`cha` |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | `String` || 606 | `"Donate 3 times before you can receive a reward!"`<br>`"EVENT_ABEGGAR_LEAVE"`<br>`"EVENT_ABEGGAR_QUES"` |
| `set_frame` | `Number` || 151 | `1`<br>`10`<br>`15` |
| [`self_status_next_fight`](./Miscellaneous.md#object-self_status_next_fight) | Object  | An object defining status effects applied to the unit at the start of the next fight. | 92 | `{ . . . }` |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | `String` | Grants an item from the specified pool or a specific item name. | 66 | `Bird_items`<br>`Coin_items`<br>`Eye_items` |
| [`permanent_stats`](./Miscellaneous.md#object-permanent_stats) | Object  | Defines permanent stat changes to apply to the unit (e.g., con, cha). | 39 | `{ . . . }` |
| [`damage`](./Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 35 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`random_pool`](./Arrays.md#array-random_pool) | Array  || 35 | `[` |
| [`gain_coins`](./Arrays.md#array-gain_coins) | `Array`  || 28 | `1`<br>`10`<br>`15` |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | `String` || 26 | `bleeding`<br>`burned`<br>`cha` |
| `self_damage` | `Number` | Defines damage or effects applied to the caster when using the ability. | 26 | `1`<br>`10`<br>`100%` |
| `random_mutation` | `Number` | The number of random mutations applied to the unit. | 25 | `1`<br>`10`<br>`2` |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | `String` || 24 | `Crazy_disorders`<br>`Steven_disorders`<br>`[BlackFetin OrangeFetin PurpleFetin]` |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | `String` || 23 | `[resultBlessing .5]`<br>`[resultGood .5]`<br>`[resultLeave 0]` |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | `String` || 21 | `BigToe`<br>`Blessing`<br>`BodyOfGlorg_Gift` |
| `gain_food` | `Number` || 21 | `-5`<br>`20`<br>`30` |
| [`spawn_unit_next_fight`](./Miscellaneous.md#object-spawn_unit_next_fight) | Object  | An object defining a unit to spawn during the next fight, including its object, count, and spawn side. | 18 | `{ . . . }` |
| [`gain_familiar`](./Events_and_Encounters.md#object-gain-familiar) | `String` | Specifies which familiar type (by its class name) the unit gains. | 15 | `CharmedBear`<br>`CharmedDaddyShark`<br>`CharmedDustDevil` |
| `party_heal` | `Number` || 15 | `1`<br>`10`<br>`100%` |
| `party_damage` | `Number` || 15 | `1`<br>`10`<br>`2` |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | `String` || 14 | `AlienBlaster`<br>`BagOfGrass`<br>`BearTrapMask` |
| `heal` | `Number` | An equation string that determines the amount of health restored by this damage instance. | 13 | `"ceil(X*item_aux/100)"`<br>`0`<br>`1` |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | `String` || 12 | `AcidReflux`<br>`Albinism`<br>`Anxiety` |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | `String` || 11 | `"EVENT_LOCKEDDOOR_PROMPT1"`<br>`"EVENT_LOCKEDDOOR_PROMPT2"`<br>`"EVENT_MYSTERIOUSSTRANGER_END_AGAIN"` |
| [`party_status_next_fight`](./Miscellaneous.md#object-party_status_next_fight) | Object  | An object defining status effects to apply to the party at the start of the next fight. | 11 | `{ . . . }` |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | `String` || 11 | `[AmoebaHat AmoebaNeck AmoebaFace]`<br>`barbed_armor`<br>`barbed_items` |
| `ally_ambush_next_fights` | `Number` || 10 | `1`<br>`2` |
| `full_heal` | `Number` || 10 | `1` |
| `ambush_next_basic_fights` | `Number` || 9 | `1` |
| [`conditional_reward`](./Miscellaneous.md#object-conditional_reward) | Object  | An object defining a reward that is granted only if specified conditions are met. | 9 | `{ . . . }` |
| [`random_mutation_from_set`](./Miscellaneous.md#object-random_mutation_from_set) | Object  | Defines a set of mutation categories and their specific IDs to apply a random mutation from. | 8 | `{ . . . }` |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | `String` || 7 | `AdventureToken_BlueNeedle`<br>`AdventureToken_HasRunFromDeath`<br>`AdventureToken_HasTakenNeedle` |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | `String` || 7 | `AlluringDoodie`<br>`BadSplinters`<br>`Beepis` |
| `next_event_bonus` | `Number` || 7 | `-1`<br>`-2`<br>`1` |
| [`clear_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | `String` || 6 | `AdventureToken_BlueNeedle`<br>`AdventureToken_HasTakenNeedle`<br>`AdventureToken_RedNeedle` |
| [`global_effect_next_fight`](./Miscellaneous.md#object-global_effect_next_fight) | Object  | Defines a global status effect or modifier to apply in the next fight. | 6 | `{ . . . }` |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | `String` || 6 | `WorldEventLegacyCounter_CrackInTheWall`<br>`WorldEventLegacyCounter_CustomTokenString`<br>`WorldEventLegacyCounter_FooCounter` |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | `String` || 5 | `cat` |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | `String` || 5 | `equipped`<br>`inventory`<br>`parasite` |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | `String` || 5 | `Event_RareShop`<br>`Event_SmallShop`<br>`Shop` |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | `String` || 4 | `AlienOvergrowth`<br>`Birdemic`<br>`GeomagneticStorm` |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | `String` || 2 | `MeatGolem`<br>`Mirage`<br>`MysteriousMachine_Bad` |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | `String` || 2 | `CryogenicTimeChamber_Full`<br>`PutridLeech`<br>`PyrophinasCollar` |
| [`next_event_from_set`](./Miscellaneous.md#object-next_event_from_set) | Object  | Specifies the next event to trigger, or defines a set of events with count and category constraints. | 2 | `{ . . . }` |
| `party_heal_disorder` | `Number` || 2 | `2` |
| [`party_permanent_stats_exclude_self`](./Miscellaneous.md#object-party_permanent_stats_exclude_self) | Object  | An object specifying permanent stat bonuses (str, dex, con, int, spd) applied to all party members except the triggering unit. | 2 | `{ . . . }` |
| [`spin`](./Engine_EventKeys.md#valid-property-keys) | `String` || 2 | `again` |
| `clear_result_animation` | `Number` || 1 | `1` |
| [`decrement_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 | `WorldEventLegacyCounter_CrackInTheWall`<br>`WorldEventLegacyCounter_CustomTokenString`<br>`WorldEventLegacyToken_StartDigging` |
| [`get_and_equip_item`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 | `Catnip`<br>`FlyLarva` |
| `heal_disorder` | `Number` || 1 | `1`<br>`2`<br>`Anxiety` |
| `heal_injury` | `Number` || 1 | `1`<br>`5` |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 | `AnyUnlocked`<br>`Necromancer`<br>`[Smack Meow Hiss]` |
| [`mutation`](./Miscellaneous.md#object-mutation) | Object  | An object defining specific body part mutations applied to the unit. | 1 | `{ . . . }` |
| `self_heal` | `Number` || 1 | `10` |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 | `AlienOvergrowthUnlocked`<br>`AntennaQuest_Orb`<br>`AntennaQuest_Rift` |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 | `random` |

</details>


---


### Object: `rare`


**Definition:** Event Node: Story branch or dialog option representing the 'Rare' action.  
**Total Count:** 633

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`attack`](./Events_and_Encounters.md#context-attack), [`good`](./Events_and_Encounters.md#context-good), [`loot`](./Events_and_Encounters.md#context-loot), [`main`](./Events_and_Encounters.md#context-main), [`options`](./Events_and_Encounters.md#context-options), [`reward`](./Events_and_Encounters.md#context-reward)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 634 | `common`<br>`rare`<br>`cha` |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | `String` || 611 | `"Donate 3 times before you can receive a reward!"`<br>`"EVENT_ABEGGAR_LEAVE"`<br>`"EVENT_ABEGGAR_QUES"` |
| `set_frame` | `Number` || 180 | `1`<br>`10`<br>`15` |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | `String` | Grants an item from the specified pool or a specific item name. | 84 | `Bird_items`<br>`Coin_items`<br>`Eye_items` |
| [`permanent_stats`](./Miscellaneous.md#object-permanent_stats) | Object  | Defines permanent stat changes to apply to the unit (e.g., con, cha). | 84 | `{ . . . }` |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | `String` || 65 | `AcidReflux`<br>`Albinism`<br>`Anxiety` |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | `String` || 46 | `bleeding`<br>`burned`<br>`cha` |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | `String` || 45 | `Crazy_disorders`<br>`Steven_disorders`<br>`[BlackFetin OrangeFetin PurpleFetin]` |
| [`self_status_next_fight`](./Miscellaneous.md#object-self_status_next_fight) | Object  | An object defining status effects applied to the unit at the start of the next fight. | 40 | `{ . . . }` |
| `random_mutation` | `Number` | The number of random mutations applied to the unit. | 38 | `1`<br>`10`<br>`2` |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | `String` || 35 | `AlienBlaster`<br>`BagOfGrass`<br>`BearTrapMask` |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | `String` || 30 | `BigToe`<br>`Blessing`<br>`BodyOfGlorg_Gift` |
| [`random_pool`](./Arrays.md#array-random_pool) | Array  || 28 | `[` |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | `String` || 26 | `AlluringDoodie`<br>`BadSplinters`<br>`Beepis` |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | `String` || 21 | `[AmoebaHat AmoebaNeck AmoebaFace]`<br>`barbed_armor`<br>`barbed_items` |
| [`spawn_unit_next_fight`](./Miscellaneous.md#object-spawn_unit_next_fight) | Object  | An object defining a unit to spawn during the next fight, including its object, count, and spawn side. | 20 | `{ . . . }` |
| [`conditional_reward`](./Miscellaneous.md#object-conditional_reward) | Object  | An object defining a reward that is granted only if specified conditions are met. | 18 | `{ . . . }` |
| [`mutation`](./Miscellaneous.md#object-mutation) | Object  | An object defining specific body part mutations applied to the unit. | 18 | `{ . . . }` |
| [`damage`](./Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 18 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`gain_coins`](./Arrays.md#array-gain_coins) | `Array`  || 17 | `1`<br>`10`<br>`15` |
| [`gain_familiar`](./Events_and_Encounters.md#object-gain-familiar) | `String` | Specifies which familiar type (by its class name) the unit gains. | 15 | `CharmedBear`<br>`CharmedDaddyShark`<br>`CharmedDustDevil` |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | `String` || 14 | `AdventureToken_BlueNeedle`<br>`AdventureToken_HasRunFromDeath`<br>`AdventureToken_HasTakenNeedle` |
| `next_event_bonus` | `Number` || 14 | `-1`<br>`-2`<br>`1` |
| `self_damage` | `Number` | Defines damage or effects applied to the caster when using the ability. | 13 | `1`<br>`10`<br>`100%` |
| [`party_status_next_fight`](./Miscellaneous.md#object-party_status_next_fight) | Object  | An object defining status effects to apply to the party at the start of the next fight. | 12 | `{ . . . }` |
| [`random_mutation_from_set`](./Miscellaneous.md#object-random_mutation_from_set) | Object  | Defines a set of mutation categories and their specific IDs to apply a random mutation from. | 11 | `{ . . . }` |
| [`play_animation`](./Arrays.md#array-play_animation) | `Array`  || 11 | `[resultBlessing .5]`<br>`[resultGood .5]`<br>`[resultLeave 0]` |
| [`learn_passive`](./Engine_EventKeys.md#valid-property-keys) | `String` || 10 | `Blessed`<br>`CobraStyle`<br>`DeathProof` |
| `party_heal` | `Number` || 10 | `1`<br>`10`<br>`100%` |
| `party_damage` | `Number` || 10 | `1`<br>`10`<br>`2` |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | `String` || 9 | `"desert/boss/dustdevil/DustDevil.lvl"`<br>`"events/Death.lvl"`<br>`"events/GlowingBear"` |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | `String` || 8 | `"EVENT_LOCKEDDOOR_PROMPT1"`<br>`"EVENT_LOCKEDDOOR_PROMPT2"`<br>`"EVENT_MYSTERIOUSSTRANGER_END_AGAIN"` |
| `party_random_mutation` | `Number` || 8 | `1` |
| `ambush_next_basic_fights` | `Number` || 7 | `1` |
| [`leave_party_temporarily`](./Miscellaneous.md#object-leave_party_temporarily) | Object  | Defines parameters for a unit leaving the party temporarily, such as skipped fights and return conditions. | 7 | `{ . . . }` |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | `String` || 7 | `AlienOvergrowthUnlocked`<br>`AntennaQuest_Orb`<br>`AntennaQuest_Rift` |
| `hide_appearance_changes` | `Number` || 6 | `1` |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | `String` || 6 | `Event_RareShop`<br>`Event_SmallShop`<br>`Shop` |
| [`gain_food`](./Arrays.md#array-gain_food) | `Array`  || 6 | `-5`<br>`20`<br>`30` |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | `String` || 5 | `WorldEventLegacyCounter_CrackInTheWall`<br>`WorldEventLegacyCounter_CustomTokenString`<br>`WorldEventLegacyCounter_FooCounter` |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | `String` || 5 | `equipped`<br>`inventory`<br>`parasite` |
| `ally_ambush_next_fights` | `Number` || 5 | `1`<br>`2` |
| `full_heal` | `Number` || 4 | `1` |
| [`learn_ability`](./Engine_EventKeys.md#valid-property-keys) | `String` || 4 | `BarfBall`<br>`FutureSight` |
| [`decrement_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | `String` || 3 | `WorldEventLegacyCounter_CrackInTheWall`<br>`WorldEventLegacyCounter_CustomTokenString`<br>`WorldEventLegacyToken_StartDigging` |
| `gain_cat_familiar` | `Number` || 3 | `1` |
| [`global_effect_next_fight`](./Miscellaneous.md#object-global_effect_next_fight) | Object  | Defines a global status effect or modifier to apply in the next fight. | 3 | `{ . . . }` |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | `String` || 3 | `cat` |
| [`make_old`](./Engine_EventKeys.md#valid-property-keys) | `String` || 3 | `self` |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | `String` | Specifies the next event to trigger, or defines a set of events with count and category constraints. | 3 | `CatHole`<br>`Tragedy`<br>`WatchingHead2` |
| `spawn_reflection_next_fight` | `Number` | The number of reflections to spawn in the next battle, optionally with a mutation. | 3 | `1` |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | `String` || 2 | `AlienOvergrowth`<br>`Birdemic`<br>`GeomagneticStorm` |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | `String` || 2 | `all`<br>`self` |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | `String` || 2 | `MeatGolem`<br>`Mirage`<br>`MysteriousMachine_Bad` |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | `String` || 2 | `CryogenicTimeChamber_Full`<br>`PutridLeech`<br>`PyrophinasCollar` |
| `party_heal_disorder` | `Number` || 2 | `2` |
| `party_heal_injury` | `Number` || 2 | `99` |
| [`party_permanent_stats_exclude_self`](./Miscellaneous.md#object-party_permanent_stats_exclude_self) | Object  | An object specifying permanent stat bonuses (str, dex, con, int, spd) applied to all party members except the triggering unit. | 2 | `{ . . . }` |
| `set_age` | `Number` || 2 | `1` |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | `String` || 2 | `random` |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | `String` || 2 | `random` |
| [`lose_item_from_inventory`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 | `cat` |
| [`ambush`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 | `"events/chupacabra.lvl"`<br>`putalevelhere.lvl` |
| `clear_result_animation` | `Number` || 1 | `1` |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 | `CharmedFlea`<br>`CharmedFleaSpecial`<br>`CharmedPooter` |
| [`get_and_equip_item`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 | `Catnip`<br>`FlyLarva` |
| `heal_disorder` | `Number` || 1 | `1`<br>`2`<br>`Anxiety` |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 | `AnyUnlocked`<br>`Necromancer`<br>`[Smack Meow Hiss]` |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 | `AnyUnlocked`<br>`Necromancer`<br>`[MiniMe SkillShare]` |
| [`lose_all_equipped_items`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 | `cat` |
| [`party_injury`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 | `random` |
| [`party_permanent_stats`](./Miscellaneous.md#object-party_permanent_stats) | Object  | An object defining permanent stat increases applied to the party. | 1 | `{ . . . }` |
| [`party_random_mutation_from_set`](./Miscellaneous.md#object-party_random_mutation_from_set) | Object  | An object specifying the count and mutation parts to randomly apply to the party. | 1 | `{ . . . }` |
| [`play_result_animation`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 | `resultVeryGood` |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 | `all` |
| [`scramble_basic_attack`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 | `all` |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 | `end_of_time_unlock`<br>`legacy_event_unlock_momsknife`<br>`map_unlock_dimensionx` |

</details>


---


### Object: `good`


**Definition:** `false`, `true`  
**Total Count:** 550

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`a`](./Events_and_Encounters.md#context-a), [`activate_p`](./Events_and_Encounters.md#context-activate_p), [`activate_z`](./Events_and_Encounters.md#context-activate_z), [`altar_sacrifice`](./Events_and_Encounters.md#context-altar_sacrifice), [`arm`](./Events_and_Encounters.md#context-arm), [`attach_amplifier`](./Events_and_Encounters.md#context-attach_amplifier), [`attach_antenna`](./Events_and_Encounters.md#context-attach_antenna), [`attach_leech`](./Events_and_Encounters.md#context-attach_leech), [`attack`](./Events_and_Encounters.md#context-attack), [`b`](./Events_and_Encounters.md#context-b), [`bash`](./Events_and_Encounters.md#context-bash), [`bash_past_alt`](./Events_and_Encounters.md#context-bash_past_alt), [`bite`](./Events_and_Encounters.md#context-bite), [`bite_it_off`](./Events_and_Encounters.md#context-bite_it_off), [`blue_needle`](./Events_and_Encounters.md#context-blue_needle), [`boogers`](./Events_and_Encounters.md#context-boogers), [`book`](./Events_and_Encounters.md#context-book), [`brace`](./Events_and_Encounters.md#context-brace), [`break_ice`](./Events_and_Encounters.md#context-break_ice), and 177 more...

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 545 | `common`<br>`rare`<br>`cha` |
| [`reward`](./Miscellaneous.md#object-reward) | Object  | An object containing sub-objects defining the rewards for different rarity tiers (e.g., common, rare), each with their own set of actions and items. | 326 | `{ . . . }` |
| `set_frame` | `Number` || 285 | `1`<br>`10`<br>`15` |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String || 184 | `"Donate 3 times before you can receive a reward!"`<br>`"EVENT_ABEGGAR_LEAVE"`<br>`"EVENT_ABEGGAR_QUES"` |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | String || 111 | `[resultBlessing .5]`<br>`[resultGood .5]`<br>`[resultLeave 0]` |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | `String` || 21 | `AlienOvergrowthUnlocked`<br>`AntennaQuest_Orb`<br>`AntennaQuest_Rift` |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | `String` | Specifies the name of a cutscene to play. | 19 | `"chaos_ending_bad"`<br>`"chaos_ending_good"`<br>`"chapterintros/bunker"` |
| [`conditional_reward`](./Miscellaneous.md#object-conditional_reward) | Object  | An object defining a reward that is granted only if specified conditions are met. | 14 | `{ . . . }` |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | `String` || 12 | `dimensionx.gon`<br>`endoftime.gon`<br>`future.gon` |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | `String` || 12 | `BlackShard`<br>`CryogenicTimeChamber_Empty`<br>`CryogenicTimeChamber_Full` |
| `random_mutation` | Number | The number of random mutations applied to the unit. | 12 | `1`<br>`10`<br>`2` |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | `String` || 12 | `AdventureToken_BlueNeedle`<br>`AdventureToken_HasRunFromDeath`<br>`AdventureToken_HasTakenNeedle` |
| [`rare`](./Enums.md#enum-rare) | Enum  | Defines the rare reward block for a boss encounter. | 10 | `1`<br>`10`<br>`15` |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | String || 9 | `MeatGolem`<br>`Mirage`<br>`MysteriousMachine_Bad` |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | String || 9 | `BigToe`<br>`Blessing`<br>`BodyOfGlorg_Gift` |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | String || 8 | `CryogenicTimeChamber_Full`<br>`PutridLeech`<br>`PyrophinasCollar` |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | String || 7 | `AcidReflux`<br>`Albinism`<br>`Anxiety` |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | `String` || 7 | `end_of_time_unlock`<br>`legacy_event_unlock_momsknife`<br>`map_unlock_dimensionx` |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | String || 6 | `WorldEventLegacyCounter_CrackInTheWall`<br>`WorldEventLegacyCounter_CustomTokenString`<br>`WorldEventLegacyCounter_FooCounter` |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | String || 6 | `AlienOvergrowth`<br>`Birdemic`<br>`GeomagneticStorm` |
| [`random_pool`](./Arrays.md#array-random_pool) | Array  || 5 | `[` |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | String || 4 | `AlienBlaster`<br>`BagOfGrass`<br>`BearTrapMask` |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | String | Grants an item from the specified pool or a specific item name. | 4 | `Bird_items`<br>`Coin_items`<br>`Eye_items` |
| [`mutation`](./Miscellaneous.md#object-mutation) | Object  | An object defining specific body part mutations applied to the unit. | 4 | `{ . . . }` |
| [`random_pool_consider_luck`](./Arrays.md#array-random_pool_consider_luck) | Array  || 4 | `[` |
| `heal_disorder` | Number || 3 | `1`<br>`2`<br>`Anxiety` |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | String || 3 | `all`<br>`self` |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | String || 3 | `AlluringDoodie`<br>`BadSplinters`<br>`Beepis` |
| `heal_injury` | `Number` || 3 | `1`<br>`5` |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | String || 3 | `cat` |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | `String` || 3 | `CryogenicTimeChamber_Empty`<br>`CryogenicTimeChamber_Full`<br>`JarOfChaos` |
| [`transform_item`](./Arrays.md#array-transform_item) | Array  || 3 | `[JarOfRadiatedBlood JarOfChaos]`<br>`[JarOfRadiation JarOfRadiatedBlood]` |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | String || 2 | `bleeding`<br>`burned`<br>`cha` |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | `String` || 2 | `pyrophina`<br>`zaratana` |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | String || 2 | `infinite_intro`<br>`king_intro` |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String || 2 | `"EVENT_LOCKEDDOOR_PROMPT1"`<br>`"EVENT_LOCKEDDOOR_PROMPT2"`<br>`"EVENT_MYSTERIOUSSTRANGER_END_AGAIN"` |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | String || 2 | `AnyUnlocked`<br>`Necromancer`<br>`[Smack Meow Hiss]` |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | String || 2 | `AnyUnlocked`<br>`Necromancer`<br>`[MiniMe SkillShare]` |
| [`party_gain_disorder_from_pool`](./Arrays.md#array-party_gain_disorder_from_pool) | Array  || 2 | `[Dwarfism]`<br>`[Gigantism]`<br>`all_disorders` |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | String || 1 | `Crazy_disorders`<br>`Steven_disorders`<br>`[BlackFetin OrangeFetin PurpleFetin]` |
| `ally_ambush_next_fights` | Number || 1 | `1`<br>`2` |
| `clone_self_to_party` | `Number` || 1 | `1` |
| `copy_items_to_party` | `Number` || 1 | `1` |
| `copy_party_items` | `Number` || 1 | `1` |
| [`gain_clone_familiar`](./Miscellaneous.md#object-gain_clone_familiar) | Object  | An object that triggers the gaining of a clone familiar, with a specified object name. | 1 | `{ . . . }` |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 | `common` |
| [`global_effect_next_fight`](./Miscellaneous.md#object-global_effect_next_fight) | Object  | Defines a global status effect or modifier to apply in the next fight. | 1 | `{ . . . }` |
| `heal` | `Number` | An equation string that determines the amount of health restored by this damage instance. | 1 | `"ceil(X*item_aux/100)"`<br>`0`<br>`1` |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | String || 1 | `equipped`<br>`inventory`<br>`parasite` |
| `next_event_bonus` | Number || 1 | `-1`<br>`-2`<br>`1` |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | String | Specifies the next event to trigger, or defines a set of events with count and category constraints. | 1 | `CatHole`<br>`Tragedy`<br>`WatchingHead2` |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 | `all` |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 | `all` |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 | `Event_RareShop`<br>`Event_SmallShop`<br>`Shop` |
| `trigger_butterfly_effect` | `Number` || 1 | `1` |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 | `random` |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 | `random` |

</details>


---


### Object: `bad`


**Definition:** Event Object: Story branch or dialog option representing the 'Bad' action.  
**Total Count:** 341

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`arm`](./Events_and_Encounters.md#context-arm), [`attack`](./Events_and_Encounters.md#context-attack), [`bash`](./Events_and_Encounters.md#context-bash), [`bash_past_alt`](./Events_and_Encounters.md#context-bash_past_alt), [`bite`](./Events_and_Encounters.md#context-bite), [`bite_it_off`](./Events_and_Encounters.md#context-bite_it_off), [`blue_needle`](./Events_and_Encounters.md#context-blue_needle), [`body`](./Events_and_Encounters.md#context-body), [`break_ice`](./Events_and_Encounters.md#context-break_ice), [`break_lock`](./Events_and_Encounters.md#context-break_lock), [`bribe`](./Events_and_Encounters.md#context-bribe), [`catch`](./Events_and_Encounters.md#context-catch), [`challenge_to_game`](./Events_and_Encounters.md#context-challenge_to_game), [`charm`](./Events_and_Encounters.md#context-charm), [`charm_past_alt`](./Events_and_Encounters.md#context-charm_past_alt), [`climb`](./Events_and_Encounters.md#context-climb), [`comfort`](./Events_and_Encounters.md#context-comfort), [`communicate`](./Events_and_Encounters.md#context-communicate), [`concheck`](./Events_and_Encounters.md#context-concheck), and 106 more...

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 339 | `common`<br>`rare`<br>`cha` |
| [`reward`](./Miscellaneous.md#object-reward) | Object  | An object containing sub-objects defining the rewards for different rarity tiers (e.g., common, rare), each with their own set of actions and items. | 305 | `{ . . . }` |
| `set_frame` | `Number` || 222 | `1`<br>`10`<br>`15` |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String || 38 | `"Donate 3 times before you can receive a reward!"`<br>`"EVENT_ABEGGAR_LEAVE"`<br>`"EVENT_ABEGGAR_QUES"` |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | String || 10 | `[resultBlessing .5]`<br>`[resultGood .5]`<br>`[resultLeave 0]` |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | `String` || 4 | `"desert/boss/dustdevil/DustDevil.lvl"`<br>`"events/Death.lvl"`<br>`"events/GlowingBear"` |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | String || 4 | `Crazy_disorders`<br>`Steven_disorders`<br>`[BlackFetin OrangeFetin PurpleFetin]` |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | `String` || 4 | `cat` |
| [`self_status_next_fight`](./Miscellaneous.md#object-self_status_next_fight) | Object  | An object defining status effects applied to the unit at the start of the next fight. | 4 | `{ . . . }` |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Specifies the name of a cutscene to play. | 3 | `"chaos_ending_bad"`<br>`"chaos_ending_good"`<br>`"chapterintros/bunker"` |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | String || 3 | `MeatGolem`<br>`Mirage`<br>`MysteriousMachine_Bad` |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | `String` || 3 | `BigToe`<br>`Blessing`<br>`BodyOfGlorg_Gift` |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | String || 3 | `[AmoebaHat AmoebaNeck AmoebaFace]`<br>`barbed_armor`<br>`barbed_items` |
| [`conditional_reward`](./Miscellaneous.md#object-conditional_reward) | Object  | An object defining a reward that is granted only if specified conditions are met. | 2 | `{ . . . }` |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | String || 2 | `bleeding`<br>`burned`<br>`cha` |
| `next_event_bonus` | Number || 2 | `-1`<br>`-2`<br>`1` |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 | `CharmedFlea`<br>`CharmedFleaSpecial`<br>`CharmedPooter` |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 | `AlluringDoodie`<br>`BadSplinters`<br>`Beepis` |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 | `equipped`<br>`inventory`<br>`parasite` |
| [`party_random_mutation_from_set`](./Miscellaneous.md#object-party_random_mutation_from_set) | Object  | An object specifying the count and mutation parts to randomly apply to the party. | 1 | `{ . . . }` |
| [`permanent_stats`](./Miscellaneous.md#object-permanent_stats) | Object  | Defines permanent stat changes to apply to the unit (e.g., con, cha). | 1 | `{ . . . }` |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 | `glitched_items` |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 | `AlienOvergrowthUnlocked`<br>`AntennaQuest_Orb`<br>`AntennaQuest_Rift` |

</details>


---


### Object: `intro`


**Definition:** No definition provided.  
**Total Count:** 214

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cat_choice`](./Enums.md#enum-cat_choice) | Enum || 214 | `random` |
| [`event_clip`](./Enums.md#enum-event_clip) | Enum || 214 | `NonWheelEvent` |
| [`subject_clip`](./Enums.md#enum-subject_clip) | Enum || 214 | `EventSubject` |
| [`subject_frame`](./Enums.md#enum-subject_frame) | Enum || 214 | `a_beggar`<br>`a_few_coins`<br>`a_large_poop` |
| [`title`](./Strings.md#string-title) | String || 214 | `"Ability Pool Test"`<br>`"Blessing!"`<br>`"EVENT_ABEGGAR_NAME"` |
| [`choose_cat_with_item`](./Enums.md#enum-choose_cat_with_item) | Enum || 17 | `CryogenicTimeChamber_Full`<br>`GuillotinasHead`<br>`PutridLeech` |
| `different_from_last_x_cats` | Number || 3 | `1`<br>`2`<br>`3` |
| `subject_frame_inner` | Number || 3 | `2`<br>`4` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`choose_cat_with_highest_stat`](./Math_Equations.md) | Equation || 1 | `int` |
| [`choose_cat_with_item_slot_equipped`](./Enums.md#enum-choose_cat_with_item_slot_equipped) | Enum || 1 | `weapon` |
| `choose_cat_with_min_health` | Number || 1 | `75%` |
| `choose_cat_with_most_injuries` | Boolean || 1 | `true` |
| `choose_cat_with_parasite` | Boolean || 1 | `true` |
| `set_frame` | `Number` || 1 | `1`<br>`10`<br>`15` |

</details>


---


### Object: `main`


**Definition:** Event Object: The central hub or recurring menu of a story event.  
**Total Count:** 214

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 214 | `common`<br>`rare`<br>`cha` |
| [`options`](./Arrays.md#array-options) | Array  | An array of named option objects within an event, each defining a possible action the player can take. | 210 | `[smash bash open]` |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String || 203 | `"Donate 3 times before you can receive a reward!"`<br>`"EVENT_ABEGGAR_LEAVE"`<br>`"EVENT_ABEGGAR_QUES"` |
| [`setup`](./Miscellaneous.md#object-setup) | Object  | Defines actions or checks to run before the main event logic, often setting up conditions or tokens. | 23 | `{ . . . }` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 4 | `{ . . . }` |
| [`goto`](./Engine_EventKeys.md#valid-property-keys) | `String` || 4 | `end` |
| [`outcome`](./Miscellaneous.md#object-outcome) | Object  | An object defining the possible outcomes of an event, typically containing a random pool or weighted lists of rewards and animations. | 4 | `{ . . . }` |
| `max_options` | `Number` || 3 | `2`<br>`3` |
| `shuffle_options` | `Boolean` || 3 | `true` |
| [`leave`](./Miscellaneous.md#object-leave) | Object  | An object defining the player action to leave or ignore the event, including its stat check and outcomes. | 3 | `{ . . . }` |
| [`ignore`](./Miscellaneous.md#object-ignore) | Object  || 2 | `{ . . . }` |
| [`open`](./Miscellaneous.md#object-open) | Object  || 2 | `{ . . . }` |
| [`buy2`](./Miscellaneous.md#object-buy2) | Object  || 1 | `{ . . . }` |
| [`buy3`](./Miscellaneous.md#object-buy3) | Object  || 1 | `{ . . . }` |
| [`examine`](./Miscellaneous.md#object-examine) | Object  || 1 | `{ . . . }` |
| [`pick`](./Miscellaneous.md#object-pick) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `options`


**Definition:** Event Object: Lists the available clickable dialog choices for the current story node.  
**Total Count:** 210

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`main`](./Events_and_Encounters.md#context-main)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ignore`](./Miscellaneous.md#object-ignore) | Object  | An object defining the player action to ignore the event, including its stat check and outcomes. | 55 | `{ . . . }` |
| [`examine`](./Miscellaneous.md#object-examine) | Object  | An object defining the player action to examine an object, including its stat check and outcomes. | 43 | `{ . . . }` |
| [`leave`](./Miscellaneous.md#object-leave) | Object  | An object defining the player action to leave or ignore the event, including its stat check and outcomes. | 29 | `{ . . . }` |
| [`loot`](./Miscellaneous.md#object-loot) | Object  | An object defining the player action to loot a container or corpse, including its stat check and outcomes. | 25 | `{ . . . }` |
| [`eat`](./Miscellaneous.md#object-eat) | Object  | An object defining the player action to consume something, including its stat check and outcomes. | 23 | `{ . . . }` |
| [`smash`](./Miscellaneous.md#object-smash) | Object  | An object defining the player action to smash an object, including its stat check and outcomes. | 15 | `{ . . . }` |
| [`destroy`](./Miscellaneous.md#object-destroy) | Object  | An object defining the player action to destroy an object, including its stat check and outcomes. | 13 | `{ . . . }` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 12 | `common`<br>`rare`<br>`cha` |
| [`bash`](./Miscellaneous.md#object-bash) | Object  | An object defining the player action to bash open a container, including its stat check and outcomes. | 12 | `{ . . . }` |
| [`sneak`](./Miscellaneous.md#object-sneak) | Object  | An object defining the player action to sneak past a threat, including its stat check and outcomes. | 11 | `{ . . . }` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 10 | `{ . . . }` |
| [`open`](./Miscellaneous.md#object-open) | Object  | An object defining the player action to open a container, including its stat check and outcomes. | 8 | `{ . . . }` |
| [`take`](./Miscellaneous.md#object-take) | Object  | An object defining the player action to take an item, including its stat check and outcomes. | 8 | `{ . . . }` |
| [`a`](./Miscellaneous.md#object-a) | Object  | An object defining the first custom option in a test or debug event. | 7 | `{ . . . }` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 7 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`b`](./Miscellaneous.md#object-b) | Object  | An object defining the second custom option in a test or debug event. | 7 | `{ . . . }` |
| [`c`](./Miscellaneous.md#object-c) | Object  | An object defining the third custom option in a test or debug event. | 7 | `{ . . . }` |
| [`charm`](./Miscellaneous.md#object-charm) | Object  | Specifies the player character's attempt to charm or persuade the encounter. | 7 | `{ . . . }` |
| [`fight`](./Miscellaneous.md#object-fight) | Object  | Specifies the player character's attempt to fight or force their way through the encounter. | 7 | `{ . . . }` |
| [`touch`](./Miscellaneous.md#object-touch) | Object  | Specifies the player character's attempt to physically touch or interact with the encounter. | 7 | `{ . . . }` |
| [`activate_p`](./Miscellaneous.md#object-activate_p) | Object  | Specifies the player character's attempt to activate the object (press a button/lever). | 6 | `{ . . . }` |
| [`activate_z`](./Miscellaneous.md#object-activate_z) | Object  | Specifies the player character's attempt to activate the object (pull a lever/switch). | 6 | `{ . . . }` |
| [`d`](./Miscellaneous.md#object-d) | Object  | Specifies a debug or test option for game development purposes. | 6 | `{ . . . }` |
| [`enter`](./Miscellaneous.md#object-enter) | Object  | Specifies the player character's attempt to enter or go inside the encounter location. | 6 | `{ . . . }` |
| [`inspect`](./Miscellaneous.md#object-inspect) | Object  | Specifies the player character's attempt to inspect or examine the encounter. | 6 | `{ . . . }` |
| [`lick`](./Miscellaneous.md#object-lick) | Object  | Specifies the player character's attempt to lick the encounter. | 6 | `{ . . . }` |
| [`drink`](./Miscellaneous.md#object-drink) | Object  | Specifies the player character's attempt to drink from or consume the encounter. | 5 | `{ . . . }` |
| [`kiss`](./Miscellaneous.md#object-kiss) | Object  | Specifies the player character's attempt to kiss the encounter. | 5 | `{ . . . }` |
| [`run`](./Miscellaneous.md#object-run) | Object  | Specifies the player character's attempt to run away or flee from the encounter. | 5 | `{ . . . }` |
| [`bite`](./Miscellaneous.md#object-bite) | Object  | Specifies the player character's attempt to bite the encounter. | 4 | `{ . . . }` |
| [`damage`](./Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 4 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`go_around`](./Miscellaneous.md#object-go_around) | Object  | Specifies the player character's attempt to go around or bypass the encounter. | 4 | `{ . . . }` |
| [`home`](./Miscellaneous.md#object-home) | Object  | Specifies the option to go home (exit to the main hub). | 4 | `{ . . . }` |
| [`past`](./Miscellaneous.md#object-past) | Object  | Specifies the option to travel to a past era (Ice Age, Jurassic, etc.). | 4 | `{ . . . }` |
| [`skip`](./Miscellaneous.md#object-skip) | Object  | Specifies the option to skip or decline the current encounter. | 4 | `{ . . . }` |
| [`investigate`](./Miscellaneous.md#object-investigate) | Object  | Specifies the player character's attempt to investigate the encounter. | 3 | `{ . . . }` |
| [`repell`](./Miscellaneous.md#object-repell) | Object  | Specifies the player character's attempt to rappel down or climb into the encounter. | 3 | `{ . . . }` |
| [`attach_antenna`](./Miscellaneous.md#object-attach_antenna) | Object  | Specifies the player character's attempt to attach a device or antenna to the encounter. | 2 | `{ . . . }` |
| [`boogers`](./Miscellaneous.md#object-boogers) | Object  | Specifies the player character's attempt to pick or examine boogers. | 2 | `{ . . . }` |
| [`copy`](./Miscellaneous.md#object-copy) | Object  | Specifies the player character's attempt to copy or replicate something from the encounter. | 2 | `{ . . . }` |
| [`find_another_way`](./Miscellaneous.md#object-find_another_way) | Object  | Specifies the player character's attempt to find an alternative path around the encounter. | 2 | `{ . . . }` |
| [`move_closer`](./Miscellaneous.md#object-move_closer) | Object  | Specifies the player character's attempt to move closer to the encounter. | 2 | `{ . . . }` |
| [`play`](./Miscellaneous.md#object-play) | Object  | Specifies the player character's attempt to play or interact playfully with the encounter. | 2 | `{ . . . }` |
| [`poop`](./Miscellaneous.md#object-poop) | Object  | Defines a poop event or interaction, often part of a random encounter or response in dialogue. | 2 | `{ . . . }` |
| [`print`](./Miscellaneous.md#object-print) | Object  | Specifies the player character's attempt to print or output something from the encounter. | 2 | `{ . . . }` |
| [`protection`](./Miscellaneous.md#object-protection) | Object  | Specifies the player character's attempt to offer or ask for protection. | 2 | `{ . . . }` |
| [`repair`](./Miscellaneous.md#object-repair) | Object  | Specifies the player character's attempt to repair the encounter object. | 2 | `{ . . . }` |
| [`sacrifice`](./Miscellaneous.md#object-sacrifice) | Object  | Specifies the player character's attempt to make a sacrifice at the encounter. | 2 | `{ . . . }` |
| [`scale`](./Events_and_Encounters.md#context-scale) | Number | The scale multiplier applied to the unit's visual size. | 2 | `.5`<br>`.6`<br>`.7` |
| [`turnon`](./Miscellaneous.md#object-turnon) | Object  | Specifies the player character's attempt to turn on or activate the encounter. | 2 | `{ . . . }` |
| [`altar_sacrifice`](./Miscellaneous.md#object-altar_sacrifice) | Object  | Specifies the player character's attempt to sacrifice a cat at the altar. | 1 | `{ . . . }` |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum || 1 | `choice_no_coins` |
| [`arm`](./Miscellaneous.md#object-arm) | Object  | Specifies the player character's attempt to put their arm inside the encounter. | 1 | `{ . . . }` |
| [`attach_amplifier`](./Miscellaneous.md#object-attach_amplifier) | Object  | Specifies the player character's attempt to attach an amplifier to the encounter. | 1 | `{ . . . }` |
| [`attach_leech`](./Miscellaneous.md#object-attach_leech) | Object  | Specifies the player character's attempt to attach a leech to the encounter. | 1 | `{ . . . }` |
| [`bash_past_alt`](./Miscellaneous.md#object-bash_past_alt) | Object  | Specifies the player character's attempt to bash through the encounter (alternate version for specific chapters). | 1 | `{ . . . }` |
| [`bite_it_off`](./Miscellaneous.md#object-bite_it_off) | Object  | Specifies the player character's attempt to bite off part of the encounter. | 1 | `{ . . . }` |
| [`blue`](./Miscellaneous.md#object-blue) | Object  | Specifies the player character's attempt to choose the blue option. | 1 | `{ . . . }` |
| [`blue_needle`](./Miscellaneous.md#object-blue_needle) | Object  | Specifies the player character's attempt to take the blue needle. | 1 | `{ . . . }` |
| [`body`](./Events_and_Encounters.md#context-body) | Number | The catalog ID for the cat's body part. | 1 | `-1`<br>`1`<br>`1.1` |
| [`book`](./Miscellaneous.md#object-book) | Object  | Specifies the player character's attempt to read or take the book. | 1 | `{ . . . }` |
| [`brace`](./Miscellaneous.md#object-brace) | Object  | Specifies the player character's attempt to brace themselves for the encounter. | 1 | `{ . . . }` |
| [`break_ice`](./Miscellaneous.md#object-break_ice) | Object  | Specifies the player character's attempt to break the ice covering the encounter. | 1 | `{ . . . }` |
| [`break_lock`](./Miscellaneous.md#object-break_lock) | Object  | Specifies the player character's attempt to break the lock on the encounter. | 1 | `{ . . . }` |
| [`bribe`](./Miscellaneous.md#object-bribe) | Object  | Specifies the player character's attempt to bribe the encounter. | 1 | `{ . . . }` |
| [`button`](./Miscellaneous.md#object-button) | Object  | Specifies the player character's attempt to push the button. | 1 | `{ . . . }` |
| [`buy1`](./Miscellaneous.md#object-buy1) | Object  | Specifies the player character's attempt to buy one of the offered items. | 1 | `{ . . . }` |
| [`catch`](./Miscellaneous.md#object-catch) | Object  | An object defining a response option for catching an entity, including stat checks and rewards. | 1 | `{ . . . }` |
| [`challenge_to_game`](./Miscellaneous.md#object-challenge_to_game) | Object  | Specifies the player character's attempt to challenge the encounter to a game. | 1 | `{ . . . }` |
| [`chaos_ending`](./Miscellaneous.md#object-chaos_ending) | Object  | Specifies the option to trigger the chaos ending cutscene. | 1 | `{ . . . }` |
| [`chapter_cutscene`](./Miscellaneous.md#object-chapter_cutscene) | Object  | Specifies the option to trigger a chapter intro cutscene. | 1 | `{ . . . }` |
| [`charm_past_alt`](./Miscellaneous.md#object-charm_past_alt) | Object  | Specifies the player character's attempt to charm the encounter (alternate version for specific chapters). | 1 | `{ . . . }` |
| [`climb`](./Miscellaneous.md#object-climb) | Object  | Specifies the player character's attempt to climb over the encounter. | 1 | `{ . . . }` |
| [`comfort`](./Miscellaneous.md#object-comfort) | Object  | A charisma-based event response that soothes the encounter subject. | 1 | `{ . . . }` |
| [`communicate`](./Miscellaneous.md#object-communicate) | Object  | A charisma-based event response to establish communication. | 1 | `{ . . . }` |
| [`concheck`](./Miscellaneous.md#object-concheck) | Object  | A constitution-based event response to test endurance. | 1 | `{ . . . }` |
| [`counter`](./Miscellaneous.md#object-counter) | Object  | An event response that uses a countering action, with no stat requirement. | 1 | `{ . . . }` |
| [`crack_open`](./Miscellaneous.md#object-crack_open) | Object  | A strength-based event response to break something open. | 1 | `{ . . . }` |
| [`cross`](./Miscellaneous.md#object-cross) | Object  | An event response to traverse an obstacle, with no stat requirement. | 1 | `{ . . . }` |
| [`cut_wires`](./Miscellaneous.md#object-cut_wires) | Object  | An intelligence-based event response to disable wires. | 1 | `{ . . . }` |
| [`damage_1`](./Miscellaneous.md#object-damage_1) | Object  | A constitution-based event response that deals minor damage. | 1 | `{ . . . }` |
| [`damage_full`](./Miscellaneous.md#object-damage_full) | Object  | A constitution-based event response that deals full damage. | 1 | `{ . . . }` |
| [`damage_half`](./Miscellaneous.md#object-damage_half) | Object  | A constitution-based event response that deals halved damage. | 1 | `{ . . . }` |
| [`desert_cutscene`](./Miscellaneous.md#object-desert_cutscene) | Object  | An event response that triggers a desert-themed cutscene, with no stat requirement. | 1 | `{ . . . }` |
| [`dexcheck`](./Miscellaneous.md#object-dexcheck) | Object  | A dexterity-based event response to test agility. | 1 | `{ . . . }` |
| [`dig`](./Miscellaneous.md#object-dig) | Object  | A strength-based event response to excavate, limited by a token counter maximum. | 1 | `{ . . . }` |
| [`disarm`](./Miscellaneous.md#object-disarm) | Object  | A dexterity-based event response to remove a trap. | 1 | `{ . . . }` |
| [`dive`](./Miscellaneous.md#object-dive) | Object  | A dexterity-based event response to plunge into water. | 1 | `{ . . . }` |
| [`donate`](./Miscellaneous.md#object-donate) | Object  | An event response to give a donation, with no stat requirement but a coin cost. | 1 | `{ . . . }` |
| [`donate_10`](./Miscellaneous.md#object-donate_10) | Object  | An event response to donate 10 coins. | 1 | `{ . . . }` |
| [`donate_15`](./Miscellaneous.md#object-donate_15) | Object  | An event response to donate 15 coins. | 1 | `{ . . . }` |
| [`donate_20`](./Miscellaneous.md#object-donate_20) | Object  | An event response to donate 20 coins. | 1 | `{ . . . }` |
| [`donate_5`](./Miscellaneous.md#object-donate_5) | Object  | An event response to donate 5 coins. | 1 | `{ . . . }` |
| [`double`](./Miscellaneous.md#object-double) | Object  | An event response that doubles something, with no stat requirement. | 1 | `{ . . . }` |
| [`eat_meat`](./Miscellaneous.md#object-eat_meat) | Object  | A constitution-based event response to consume meat. | 1 | `{ . . . }` |
| [`enter_crater`](./Miscellaneous.md#object-enter_crater) | Object  | A luck-based event response to enter a crater. | 1 | `{ . . . }` |
| [`face`](./Enums.md#enum-face) | Enum  | The face equipment item assigned to the unit. | 1 | `1004`<br>`1019`<br>`AtomicMark` |
| [`fiddle`](./Miscellaneous.md#object-fiddle) | Object  | A quest-based event response to tamper, requiring no specific quest token. | 1 | `{ . . . }` |
| [`fill_jar`](./Miscellaneous.md#object-fill_jar) | Object  | A quest-based event response to fill a jar, with no stat requirement. | 1 | `{ . . . }` |
| [`find`](./Miscellaneous.md#object-find) | Object  | An event response to search, with no stat requirement. | 1 | `{ . . . }` |
| [`fire`](./Passives_and_Statuses.md#object-fire) | Object  | An event response that uses fire, with no stat requirement. | 1 | `{ . . . }` |
| [`flush_yourself`](./Miscellaneous.md#object-flush_yourself) | Object  | An event response to flush oneself, requiring a minimum counter value. | 1 | `{ . . . }` |
| [`follow`](./Miscellaneous.md#object-follow) | Object  | A speed-based event response to pursue. | 1 | `{ . . . }` |
| [`free`](./Miscellaneous.md#object-free) | Object  | If true, this option requires no cost to activate. | 1 | `{ . . . }` |
| [`future`](./Miscellaneous.md#object-future) | Object  | Specifies the name, map flag, or connection for the Future area. | 1 | `{ . . . }` |
| [`give_parasite`](./Miscellaneous.md#object-give_parasite) | Object  | An event response to give a parasite, requiring the cat to have a parasite. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`hack`](./Miscellaneous.md#object-hack) | Object  | An intelligence-based event response to hack a system. | 1 | `{ . . . }` |
| [`head`](./Enums.md#enum-head) | Enum / Number  | The catalog ID for the cat's head part. | 1 | `-1`<br>`1`<br>`1.3` |
| [`holy`](./Miscellaneous.md#object-holy) | Object  | An event response that uses holy power, with no stat requirement. | 1 | `{ . . . }` |
| [`hp`](./Miscellaneous.md#object-hp) | Object  | An event response that trades health, with no stat requirement. | 1 | `{ . . . }` |
| [`ice`](./Passives_and_Statuses.md#object-ice) | Object  | An event response that uses ice, with no stat requirement. | 1 | `{ . . . }` |
| [`infinite`](./Miscellaneous.md#object-infinite) | Object  | An event response to choose infinite, with a chapter exit hint and no stat requirement. | 1 | `{ . . . }` |
| [`intcheck`](./Miscellaneous.md#object-intcheck) | Object  | An intelligence-based event response to test intellect. | 1 | `{ . . . }` |
| [`intimidation`](./Miscellaneous.md#object-intimidation) | Object  | An event response that intimidates, with no stat requirement. | 1 | `{ . . . }` |
| [`itchies`](./Miscellaneous.md#object-itchies) | Object  | An event response that causes itches, with no stat requirement. | 1 | `{ . . . }` |
| [`join`](./Miscellaneous.md#object-join) | Object  | A charisma-based event response to join in. | 1 | `{ . . . }` |
| [`jump`](./Miscellaneous.md#object-jump) | Object  | A speed-based event response to leap. | 1 | `{ . . . }` |
| [`jump_over`](./Miscellaneous.md#object-jump_over) | Object  | A dexterity-based event response to vault over. | 1 | `{ . . . }` |
| [`keep_going`](./Miscellaneous.md#object-keep_going) | Object  | An event response to persevere, with no stat requirement. | 1 | `{ . . . }` |
| [`kiss_meat`](./Miscellaneous.md#object-kiss_meat) | Object  | A charisma-based event response to kiss meat. | 1 | `{ . . . }` |
| [`knife`](./Miscellaneous.md#object-knife) | Object  | An event response to obtain a knife, with no stat requirement. | 1 | `{ . . . }` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`leave_it_in`](./Miscellaneous.md#object-leave_it_in) | Object  | An event response to leave an object in place, with no stat requirement. | 1 | `{ . . . }` |
| [`leg`](./Miscellaneous.md#object-leg) | Object  | A luck-based event response to use a leg. | 1 | `{ . . . }` |
| [`lever`](./Miscellaneous.md#object-lever) | Object  | An event response to pull a lever, with a fixed chance and no stat requirement. | 1 | `{ . . . }` |
| [`lick_alt`](./Miscellaneous.md#object-lick_alt) | Object  | A constitution-based event response to lick, restricted to specific chapters. | 1 | `{ . . . }` |
| [`lightning`](./Passives_and_Statuses.md#object-lightning) | Object  | An event response using lightning, with no stat requirement. | 1 | `{ . . . }` |
| [`listen`](./Miscellaneous.md#object-listen) | Object  | An intelligence-based event response to listen. | 1 | `{ . . . }` |
| [`looks`](./Miscellaneous.md#object-looks) | Object  | The dialogue option for the Genie good event that selects the looks reward. | 1 | `{ . . . }` |
| [`loot_heart`](./Miscellaneous.md#object-loot_heart) | Object  | The dialogue option to take the heart from the Dead King as a quest action. | 1 | `{ . . . }` |
| [`makeup`](./Miscellaneous.md#object-makeup) | Object  | The dialogue option for the makeup event, associated with the Tink2 encounter. | 1 | `{ . . . }` |
| [`mind`](./Miscellaneous.md#object-mind) | Object  | The dialogue option for the Genie bad event that selects the curse mind reward. | 1 | `{ . . . }` |
| [`neck`](./Enums.md#enum-neck) | Enum  | The neck equipment item assigned to the unit. | 1 | `AngelicAura`<br>`AngelicAura_Terminator`<br>`DruidNeck` |
| [`nothanks`](./Miscellaneous.md#object-nothanks) | Object  | The generic decline dialogue option that triggers a leave animation. | 1 | `{ . . . }` |
| [`outsmart`](./Miscellaneous.md#object-outsmart) | Object  | The dialogue option that uses the int stat to outsmart the tutorial encounter. | 1 | `{ . . . }` |
| [`patch_up`](./Miscellaneous.md#object-patch_up) | Object  | The dialogue option that uses the int stat to patch up the dying fetus. | 1 | `{ . . . }` |
| [`pick_lock`](./Miscellaneous.md#object-pick_lock) | Object  | The dialogue option that uses the dex stat to pick a lock on a crate. | 1 | `{ . . . }` |
| [`pilfer`](./Miscellaneous.md#object-pilfer) | Object  | The dialogue option that uses the lck stat to pilfer from a pile of skulls. | 1 | `{ . . . }` |
| [`pirouette`](./Miscellaneous.md#object-pirouette) | Object  | The dialogue option for the Tink1 encounter that performs a pirouette. | 1 | `{ . . . }` |
| [`place_gristle`](./Miscellaneous.md#object-place_gristle) | Object  | The dialogue option to place gristle on the Wall of Flesh as a quest action. | 1 | `{ . . . }` |
| [`power`](./Miscellaneous.md#object-power) | Object  | The dialogue option for the Genie good event that selects the power reward. | 1 | `{ . . . }` |
| [`pull`](./Miscellaneous.md#object-pull) | Object  | The dialogue option that uses the str stat to pull a knife from a wall. | 1 | `{ . . . }` |
| [`pull_it_out`](./Miscellaneous.md#object-pull_it_out) | Object  | The dialogue option to pull out a stalactite from the Jagged Pathway. | 1 | `{ . . . }` |
| [`pull_lever`](./Miscellaneous.md#object-pull_lever) | Object  | The dialogue option to pull the lever on the Odd Device. | 1 | `{ . . . }` |
| [`purify`](./Miscellaneous.md#object-purify) | Object  | The dialogue option that uses the lck stat to purify the Mysterious Chamber. | 1 | `{ . . . }` |
| [`push_buttons`](./Miscellaneous.md#object-push_buttons) | Object  | The dialogue option to push buttons on the Odd Device. | 1 | `{ . . . }` |
| [`push_through`](./Miscellaneous.md#object-push_through) | Object  | The dialogue option that uses the str stat to push through the Jagged Pathway. | 1 | `{ . . . }` |
| [`put_in_coins`](./Miscellaneous.md#object-put_in_coins) | Object  | The dialogue option to put coins into the Vending Machine, requiring a minimum of 10 coins. | 1 | `{ . . . }` |
| [`put_out_of_misery`](./Miscellaneous.md#object-put_out_of_misery) | Object  | The dialogue option that uses the str stat to put the dying fetus out of its misery. | 1 | `{ . . . }` |
| [`reach_inside`](./Miscellaneous.md#object-reach_inside) | Object  | The dialogue option that uses the spd stat to reach inside a Small Black Hole. | 1 | `{ . . . }` |
| [`read`](./Miscellaneous.md#object-read) | Object  | The dialogue option that uses the int stat to read the Mysterious Manual. | 1 | `{ . . . }` |
| [`receive`](./Miscellaneous.md#object-receive) | Object  | The dialogue option to receive an item from a legacy event. | 1 | `{ . . . }` |
| [`red`](./Miscellaneous.md#object-red) | Object  | Configuration for one of the dialog options (label 'EVENT_RED_ANSW'), with a fixed chance and associated animation, in a choice event. | 1 | `{ . . . }` |
| [`red_needle`](./Miscellaneous.md#object-red_needle) | Object  | The dialogue option that uses the lck stat to select the red needle, requiring not having the RedNeedle token. | 1 | `{ . . . }` |
| [`reflect`](./Miscellaneous.md#object-reflect) | Object  | The dialogue option for the StacyMutant4 encounter that chooses to reflect. | 1 | `{ . . . }` |
| [`remove`](./Miscellaneous.md#object-remove) | Object  | The dialogue option that uses the str stat to remove a stuck corpse. | 1 | `{ . . . }` |
| [`remove_the_nail`](./Miscellaneous.md#object-remove_the_nail) | Object  | The dialogue option that uses the dex stat to remove the nail from a big toe. | 1 | `{ . . . }` |
| [`repair_quest`](./Miscellaneous.md#object-repair_quest) | Object  | The dialogue option to repair the broken time machine as a quest action. | 1 | `{ . . . }` |
| [`rest`](./Miscellaneous.md#object-rest) | Object  | The dialogue option that uses the lck stat to rest on a cat bed. | 1 | `{ . . . }` |
| [`revive`](./Miscellaneous.md#object-revive) | Object  | The dialogue option that uses the lck stat to revive the Dead Mammoth. | 1 | `{ . . . }` |
| [`rub`](./Miscellaneous.md#object-rub) | Object  | The dialogue option that uses the lck stat to rub the Genie Lamp. | 1 | `{ . . . }` |
| [`run_again`](./Miscellaneous.md#object-run_again) | Object  | The dialogue option that uses the spd stat to run away from Death again, requiring he hasn't chased you yet. | 1 | `{ . . . }` |
| [`run_away`](./Miscellaneous.md#object-run_away) | Object  | The dialogue option that uses the spd stat to run away from a Giant Sleeping Shark. | 1 | `{ . . . }` |
| [`sacrifice_full_favor`](./Miscellaneous.md#object-sacrifice_full_favor) | Object  | The dialogue option to sacrifice a cat at the Volcano with full favor as a quest action. | 1 | `{ . . . }` |
| [`sacrifice_normal`](./Miscellaneous.md#object-sacrifice_normal) | Object  | The dialogue option to perform a normal sacrifice at the Meat Altar, requiring the GuillotinasHead not equipped. | 1 | `{ . . . }` |
| [`sacrifice_partial_favor`](./Miscellaneous.md#object-sacrifice_partial_favor) | Object  | The dialogue option to sacrifice a cat at the Volcano with partial favor as a quest action. | 1 | `{ . . . }` |
| [`sacrifice_quest`](./Miscellaneous.md#object-sacrifice_quest) | Object  | The dialogue option to perform a quest sacrifice at the Meat Altar, requiring the GuillotinasHead equipped. | 1 | `{ . . . }` |
| [`scream`](./Miscellaneous.md#object-scream) | Object  | The dialogue option to scream at the Meat Golem with no stat requirement. | 1 | `{ . . . }` |
| [`shake`](./Miscellaneous.md#object-shake) | Object  | The dialogue option that uses the str stat to shake the Vending Machine. | 1 | `{ . . . }` |
| [`slip_through`](./Miscellaneous.md#object-slip_through) | Object  | The dialogue option that uses the dex stat to slip through a Barbed Wire Fence. | 1 | `{ . . . }` |
| [`sneak_by`](./Miscellaneous.md#object-sneak_by) | Object  | The dialogue option that uses the dex stat to sneak by a Giant Sleeping Shark. | 1 | `{ . . . }` |
| [`sneak_past_alt`](./Miscellaneous.md#object-sneak_past_alt) | Object  | The dialogue option using dex to sneak past a stray cat, available only in the Ice Age or Jurassic chapters. | 1 | `{ . . . }` |
| [`soul`](./Miscellaneous.md#object-soul) | Object  | The dialogue option for the Genie bad event that selects the curse soul reward. | 1 | `{ . . . }` |
| [`speed`](./Arrays.md#array-speed) | Array / Number  | The speed of the projectile or move, can be a value or a range. | 1 | `-30`<br>`-4`<br>`.5` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |
| `stat_max` | Number || 1 | `1`<br>`10`<br>`15` |
| `stat_min` | Number || 1 | `1`<br>`10`<br>`15` |
| [`surprise`](./Miscellaneous.md#object-surprise) | Object  | The dialogue option for the Butch2 encounter that surprises the target. | 1 | `{ . . . }` |
| [`sweet_talk`](./Miscellaneous.md#object-sweet_talk) | Object  | The dialogue option that uses the cha stat to sweet-talk Death. | 1 | `{ . . . }` |
| [`swim`](./Miscellaneous.md#object-swim) | Object  | The dialogue option that uses the str stat to swim through a Strong Current. | 1 | `{ . . . }` |
| [`tail`](./Events_and_Encounters.md#context-tail) | Integer | The catalog ID for the cat's tail part. | 1 | `-1`<br>`1000`<br>`1001` |
| [`take_blood`](./Miscellaneous.md#object-take_blood) | Object  | The dialogue option to drain blood from the Dead King as a quest action. | 1 | `{ . . . }` |
| [`talk`](./Miscellaneous.md#object-talk) | Object  | The dialogue option that uses the cha stat to talk to a Spookie Apparation. | 1 | `{ . . . }` |
| [`talk_to`](./Miscellaneous.md#object-talk_to) | Object  | The dialogue option that uses the cha stat to talk to someone during a Dust Storm. | 1 | `{ . . . }` |
| [`tappytoes`](./Miscellaneous.md#object-tappytoes) | Object  | The dialogue option for the Tink1 encounter that performs a tappytoes action. | 1 | `{ . . . }` |
| [`teleport`](./Miscellaneous.md#object-teleport) | Object  | Defines a dialogue option that transports the unit to an alternative location in the event. | 1 | `{ . . . }` |
| [`thorns`](./Miscellaneous.md#object-thorns) | Object  | Defines a dialogue option that applies a thorns effect to the unit. | 1 | `{ . . . }` |
| [`throw`](./Miscellaneous.md#object-throw) | Object  | Defines a dialogue option that allows the unit to throw an object. | 1 | `{ . . . }` |
| [`timemachine`](./Miscellaneous.md#object-timemachine) | Object  | Defines a dialogue option that triggers a time travel sequence. | 1 | `{ . . . }` |
| [`traverse`](./Miscellaneous.md#object-traverse) | Object  | Defines a dialogue option that moves the unit through a traversal area. | 1 | `{ . . . }` |
| [`upgrade_yourself`](./Miscellaneous.md#object-upgrade_yourself) | Object  | Defines a dialogue option that upgrades the unit's attributes or abilities. | 1 | `{ . . . }` |
| [`use_item`](./Miscellaneous.md#object-use_item) | Object  | Defines a dialogue option that prompts the unit to use an item from their inventory. | 1 | `{ . . . }` |
| [`use_toilet_con`](./Miscellaneous.md#object-use_toilet_con) | Object  | Defines a dialogue option that interacts with a toilet using the Constitution stat. | 1 | `{ . . . }` |
| [`use_toilet_str`](./Miscellaneous.md#object-use_toilet_str) | Object  | Defines a dialogue option that interacts with a toilet using the Strength stat. | 1 | `{ . . . }` |
| [`use_weapon`](./NPC_Scripts.md#object-use_weapon) | Object  | Defines a dialogue option that prompts the unit to use their equipped weapon. | 1 | `{ . . . }` |
| [`w1`](./Miscellaneous.md#object-w1) | Object  | Defines a dialogue option for the first weather choice in the Crater Weather event. | 1 | `{ . . . }` |
| [`w2`](./Miscellaneous.md#object-w2) | Object  | Defines a dialogue option for the second weather choice in the Crater Weather event. | 1 | `{ . . . }` |
| [`w3`](./Miscellaneous.md#object-w3) | Object  | Defines a dialogue option for the third weather choice in the Crater Weather event. | 1 | `{ . . . }` |
| [`w4`](./Miscellaneous.md#object-w4) | Object  | Defines a dialogue option for the fourth weather choice in the Crater Weather event. | 1 | `{ . . . }` |
| [`w5`](./Miscellaneous.md#object-w5) | Object  | Defines a dialogue option for the fifth weather choice in the Crater Weather event. | 1 | `{ . . . }` |
| [`w6`](./Miscellaneous.md#object-w6) | Object  | Defines a dialogue option for the sixth weather choice in the Crater Weather event. | 1 | `{ . . . }` |
| [`wealth`](./Miscellaneous.md#object-wealth) | Object  | Defines a dialogue option that grants the unit money or valuable items. | 1 | `{ . . . }` |
| [`wheezies`](./Miscellaneous.md#object-wheezies) | Object  | Defines a dialogue option that triggers a wheezing effect or condition. | 1 | `{ . . . }` |
| [`wish_genes`](./Miscellaneous.md#object-wish_genes) | Object  | Defines a dialogue option in the Monkey Paw event that modifies the unit's genetics. | 1 | `{ . . . }` |
| [`wish_items`](./Miscellaneous.md#object-wish_items) | Object  | Defines a dialogue option in the Monkey Paw event that grants items. | 1 | `{ . . . }` |
| [`wish_levelups`](./Miscellaneous.md#object-wish_levelups) | Object  | Defines a dialogue option in the Monkey Paw event that grants level-ups. | 1 | `{ . . . }` |
| [`wish_strength`](./Miscellaneous.md#object-wish_strength) | Object  | Defines a dialogue option in the Monkey Paw event that increases Strength. | 1 | `{ . . . }` |
| [`withstand`](./Miscellaneous.md#object-withstand) | Object  | Defines a dialogue option that allows the unit to withstand a hazard using Constitution. | 1 | `{ . . . }` |
| [`yank_it_out`](./Miscellaneous.md#object-yank_it_out) | Object  | Defines a dialogue option that yanks out an object using Strength. | 1 | `{ . . . }` |
| [`yellow_needle`](./Miscellaneous.md#object-yellow_needle) | Object  | Defines a dialogue option to interact with a yellow needle. | 1 | `{ . . . }` |

</details>


---


### Object: `requirements`


**Definition:** No definition provided.  
**Total Count:** 203

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`activate_p`](./Events_and_Encounters.md#context-activate_p), [`activate_z`](./Events_and_Encounters.md#context-activate_z), [`attach_amplifier`](./Events_and_Encounters.md#context-attach_amplifier), [`attach_antenna`](./Events_and_Encounters.md#context-attach_antenna), [`attach_leech`](./Events_and_Encounters.md#context-attach_leech), [`bash`](./Events_and_Encounters.md#context-bash), [`bash_past_alt`](./Events_and_Encounters.md#context-bash_past_alt), [`blue_needle`](./Events_and_Encounters.md#context-blue_needle), [`charm`](./Events_and_Encounters.md#context-charm), [`charm_past_alt`](./Events_and_Encounters.md#context-charm_past_alt), [`conditional_reward`](./Events_and_Encounters.md#context-conditional_reward), [`dig`](./Events_and_Encounters.md#context-dig), [`donate_10`](./Events_and_Encounters.md#context-donate_10), [`donate_15`](./Events_and_Encounters.md#context-donate_15), [`donate_20`](./Events_and_Encounters.md#context-donate_20), [`donate_5`](./Events_and_Encounters.md#context-donate_5), [`fiddle`](./Events_and_Encounters.md#context-fiddle), [`fight`](./Events_and_Encounters.md#context-fight), [`fill_jar`](./Events_and_Encounters.md#context-fill_jar), and 31 more...

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`has_token`](./Enums.md#enum-has_token) | Enum || 63 | `AdventureToken_BlueNeedle`<br>`AdventureToken_HasRunFromDeath`<br>`AdventureToken_HasTakenNeedle` |
| [`counter_range`](./Arrays.md#array-counter_range) | Array || 38 | `[WorldEventLegacyCounter_CrackInTheWall 1 1]`<br>`[WorldEventLegacyCounter_CrackInTheWall 2 2]`<br>`[WorldEventLegacyCounter_CrackInTheWall 3 3]` |
| [`not_has_token`](./Enums.md#enum-not_has_token) | Enum || 30 | `AdventureToken_BlueNeedle`<br>`AdventureToken_HasRunFromDeath`<br>`AdventureToken_MysteriousJarRepeat` |
| [`counter_minimum`](./Arrays.md#array-counter_minimum) | Array || 26 | `[WorldEventLegacyCounter_CrackInTheWall 4]`<br>`[WorldEventLegacyCounter_FooCounter 5]`<br>`[WorldEventLegacyCounter_Jack 100]` |
| [`cat_has_item_equipped`](./Enums.md#enum-cat_has_item_equipped) | Enum || 23 | `CryogenicTimeChamber_Empty`<br>`CryogenicTimeChamber_Full`<br>`FaceCovering` |
| [`counter_maximum`](./Arrays.md#array-counter_maximum) | Array || 19 | `[WorldEventLegacyCounter_CrackInTheWall 0]`<br>`[WorldEventLegacyCounter_CrackInTheWall 3]`<br>`[WorldEventLegacyCounter_FooCounter 10]` |
| [`is_not_chapter`](./Arrays.md#array-is_not_chapter) | Array || 16 | `[future theend]`<br>`[iceage jurassic]`<br>`[jurassic iceage]` |
| [`is_chapter`](./Arrays.md#array-is_chapter) | Array || 8 | `[future theend]`<br>`[future]`<br>`[iceage jurassic]` |
| [`not_cat_has_item_equipped`](./Enums.md#enum-not_cat_has_item_equipped) | Enum || 3 | `CryogenicTimeChamber_Full`<br>`GuillotinasHead`<br>`Horns` |
| `minimum_party_size` | Number || 2 | `2` |
| `not_on_quest` | Number || 2 | `1` |
| `cat_has_injury_count_min` | Number || 1 | `2` |
| [`cat_has_item_slot_equipped`](./Enums.md#enum-cat_has_item_slot_equipped) | Enum || 1 | `weapon` |
| `cat_has_parasite` | Boolean || 1 | `true` |

</details>


---


### Object: `self_status_next_fight`


**Definition:** Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter.  
**Total Count:** 143

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`bad`](./Events_and_Encounters.md#context-bad), [`buy1`](./Events_and_Encounters.md#context-buy1), [`common`](./Events_and_Encounters.md#context-common), [`else`](./Events_and_Encounters.md#context-else), [`main`](./Events_and_Encounters.md#context-main), [`rare`](./Events_and_Encounters.md#context-rare)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 131 | `passives`<br>`class`<br>`tag` |
| [`Fear`](./Enums.md) | Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 29 | `1`<br>`10`<br>`2` |
| [`Poison`](./Enums.md) | Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 28 | `1`<br>`10`<br>`2` |
| [`Bleed`](./Enums.md) | Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 20 | `1`<br>`10`<br>`2` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 13 | `Default`<br>`FormChange`<br>`Druid` | [`AllStatsUp`](./Enums.md) | Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 7 | `-1`<br>`-2`<br>`1` |
| [`SpeedUp`](./Enums.md) | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 5 | `-1`<br>`-2`<br>`-4` |
| [`StrengthUp`](./Enums.md) | Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 5 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| [`AbilityOnBattleStart_Immediate`](./Enums.md#enum-abilityonbattlestart_immediate) | Enum  || 4 | `BrambleRandomTileEvent`<br>`FlowerEventSleep`<br>`Flush` |
| [`ConstitutionUp`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 4 | `-1`<br>`-2`<br>`1` |
| [`AddStartingMana`](./Enums.md) | Integer | The amount of bonus mana the unit starts each battle with. | 3 | `20`<br>`5` |
| [`Burn`](./Enums.md) | Integer | The amount of Burn applied, either as a fixed number or a formula string. | 3 | `1`<br>`10`<br>`2` |
| [`CharismaUp`](./Enums.md) | Integer | The amount of charisma change, or a keyword like 'item_aux'. | 3 | `-1`<br>`-2`<br>`1` |
| [`Confusion`](./Enums.md) | Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 3 | `1`<br>`10`<br>`2` |
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 3 | `1`<br>`2`<br>`3` |
| [`Webbed`](./Enums.md) | Integer | The amount of webbed stacks applied, or an [stacks, probability] array. | 3 | `1`<br>`2`<br>`[1 .1]` |
| [`Blind`](./Enums.md) | Integer | The amount of blind stacks applied, or an [stacks, probability] array. | 2 | `-1`<br>`1`<br>`2` |
| [`Bruise`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 2 | `1`<br>`2`<br>`3` |
| [`DexterityUp`](./Enums.md) | Integer | The amount of dexterity change, or a keyword like 'item_aux'. | 2 | `-1`<br>`1`<br>`2` |
| [`IntelligenceUp`](./Enums.md) | Integer | The amount of Intelligence added as a flat bonus. | 2 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| [`NoHealthRegen`](./Enums.md) | Integer | Prevents the unit from regenerating health normally. | 2 | `1` |
| [`Sleep`](./Enums.md) | Integer | The amount of sleep stacks applied, or an [stacks, probability] array. | 2 | `1`<br>`2`<br>`3` |
| [`Stun`](./Enums.md) | Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`2`<br>`3` |
| [`AbilityOnBattleStart`](./Enums.md#enum-abilityonbattlestart) | Enum  || 1 | `Flush`<br>`Heathens`<br>`Heathens2` |
| [`AddInitiative`](./Enums.md) | Integer | The amount of bonus or penalty to the unit's turn order initiative value. | 1 | `-10`<br>`-100`<br>`-20` |
| [`AlphaTurns`](./Enums.md) | Integer | The number of turns the unit acts first in battle; negative values may indicate last. | 1 | `-1`<br>`1` |
| [`ChangeTileUnderCharacterAtStart`](./Enums.md#enum-changetileundercharacteratstart) | Enum  || 1 | `GlassTile` |
| [`DivineShield`](./Enums.md) | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | `1`<br>`2`<br>`4` |
| [`Fights`](./Enums.md) | Integer || 1 | `1`<br>`3`<br>`99` |
| [`LuckUp`](./Enums.md) | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 1 | `-1`<br>`-2`<br>`-4` |
| [`Madness`](./Enums.md) | Integer | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 1 | `1`<br>`2`<br>`3` |
| [`MissChance`](./Enums.md) | Integer | The flat percentage chance that the unit's attacks will miss. | 1 | `10`<br>`15`<br>`20` |
| [`NoManaRegen`](./Enums.md) | Integer | The unit does not naturally regenerate mana per turn. Value indicates the stage or flag enabling this restriction. | 1 | `1` |
| [`PermanentConfusion`](./Enums.md) | Integer | If set to 1, the unit is permanently confused and cannot be cured. | 1 | `1` |
| [`ProbeCharmed`](./Enums.md) | Integer | The number of charm stacks applied by a probe. | 1 | `1` |
| [`RandomStatUp`](./Enums.md) | Integer | The amount of random stat increase applied, either as a fixed number or a formula string. | 1 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| [`Rot`](./Enums.md) | Integer | Integer, or an array [stacks, probability] specifying the amount of Rot stacks applied with the given probability. | 1 | `-999999`<br>`1`<br>`2` |
| [`Slow`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 1 | `-1`<br>`1`<br>`2` |
| [`SpiderInfested`](./Enums.md) | Integer | The number of spider infestation stacks applied. | 1 | `1`<br>`2`<br>`4` |
| [`Tarred`](./Enums.md) | Integer | The amount of tarred stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`2`<br>`[1 .1]` |
| [`TempStrengthUp`](./Enums.md) | Integer | The number of stacks of temporary Strength Up applied to the unit. | 1 | `1`<br>`2`<br>`X` |

</details>


---


### Object: `permanent_stats`


**Definition:** Event Reward: Permanently increases (or decreases) the core stats of a single character.  
**Total Count:** 134

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`bad`](./Events_and_Encounters.md#context-bad), [`common`](./Events_and_Encounters.md#context-common), [`rare`](./Events_and_Encounters.md#context-rare)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`con`](./Enums.md#enum-con) | Enum / Integer  | The Constitution stat value or modifier. | 37 | `-1`<br>`-2`<br>`-3` |
| `random` | Number || 25 | `-1`<br>`-2`<br>`1` |
| [`int`](./Enums.md#enum-int) | Enum / Integer  || 23 | `-1`<br>`-10`<br>`-2` |
| [`lck`](./Enums.md#enum-lck) | Enum / Integer  || 20 | `-1`<br>`-2`<br>`-3` |
| [`spd`](./Enums.md#enum-spd) | Enum / Integer  | The Speed stat value or modifier. | 20 | `-1`<br>`-10`<br>`-2` |
| [`str`](./Enums.md#enum-str) | Enum / Integer  || 18 | `-1`<br>`-2`<br>`-3` |
| [`cha`](./Engine_EventKeys.md#valid-property-keys) | Variable | The Charisma stat value or modifier. | 16 | `+1`<br>`-1`<br>`-2` |
| [`dex`](./Enums.md#enum-dex) | Enum / Integer  || 10 | `-1`<br>`-2`<br>`-3` |

</details>


---


### Object: `conditional_reward`


**Definition:** Event Action: Provides a reward only if a specific condition is met.  
**Total Count:** 126

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bad`](./Events_and_Encounters.md#context-bad), [`common`](./Events_and_Encounters.md#context-common), [`else`](./Events_and_Encounters.md#context-else), [`good`](./Events_and_Encounters.md#context-good), [`rare`](./Events_and_Encounters.md#context-rare), [`setup`](./Events_and_Encounters.md#context-setup)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 125 | `common`<br>`rare`<br>`cha` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 125 | `{ . . . }` |
| [`reward`](./Miscellaneous.md#object-reward) | Object  | An object containing sub-objects defining the rewards for different rarity tiers (e.g., common, rare), each with their own set of actions and items. | 125 | `{ . . . }` |
| [`else`](./Miscellaneous.md#object-else) | Object  | Specifies the fallback outcome when the primary condition in a conditional reward is not met. | 37 | `{ . . . }` |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String || 2 | `"Donate 3 times before you can receive a reward!"`<br>`"EVENT_ABEGGAR_LEAVE"`<br>`"EVENT_ABEGGAR_QUES"` |

</details>


---


### Object: `ignore`


**Definition:** No definition provided.  
**Total Count:** 57

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 57 | `common`<br>`rare`<br>`cha` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 57 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | Variable || 57 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Variable || 56 | `cha`<br>`coins`<br>`con` |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 55 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 4 | `{ . . . }` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 3 | `{ . . . }` |
| [`hint_chapter_exit`](./Enums.md#enum-hint_chapter_exit) | Enum || 2 | `dimensionx`<br>`endoftime`<br>`future` |

</details>


---


### Object: `examine`


**Definition:** No definition provided.  
**Total Count:** 44

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`label`](./Strings.md#string-label) | Variable || 44 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 44 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 41 | `common`<br>`rare`<br>`cha` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 41 | `false`<br>`true` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 32 | `{ . . . }` |
| [`copy_results`](./Enums.md#enum-copy_results) | Enum || 3 | `examine`<br>`lever`<br>`open` |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |

</details>


---


### Object: `spawn_unit_next_fight`


**Definition:** Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter.  
**Total Count:** 41

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`rare`](./Events_and_Encounters.md#context-rare), [`reward`](./Events_and_Encounters.md#context-reward)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array / Enum | Specifies the object or unit to be spawned. | 40 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`count`](./Arrays.md#array-count) | Array / Integer | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 34 | `0`<br>`1`<br>`10` |
| [`spawn_side`](./Enums.md#enum-spawn_side) | Enum || 31 | `"cats"`<br>`anywhere`<br>`cats` |
| [`side`](./Enums.md#enum-side) | Enum || 3 | `enemies` |

</details>


---


### Object: `get_item_from_pool`


**Definition:** Event Action: Rewards the player with an item drawn from a specific loot pool.  
**Total Count:** 40

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`rare`](./Events_and_Encounters.md#context-rare), [`reward`](./Events_and_Encounters.md#context-reward)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`pool`](./Arrays.md#array-pool) | Array / Enum  | Specifies the name of the pool from which an ability is learned or an item is crafted. | 39 | `2`<br>`3`<br>`4` |
| [`restrict`](./Arrays.md#array-restrict) | Array || 30 | `[weapon armor]`<br>`[weapon consumables armor]`<br>`[weapon, trinket, armor]` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 | `"Donate 3 times before you can receive a reward!"`<br>`"EVENT_ABEGGAR_LEAVE"`<br>`"EVENT_ABEGGAR_QUES"` |

</details>


---


### Object: `else`


**Definition:** Fallback object that executes if the preceding `Conditional_` block evaluated to false.  
**Total Count:** 37

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`conditional_reward`](./Events_and_Encounters.md#context-conditional_reward)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 38 | `common`<br>`rare`<br>`cha` |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | `String` || 20 | `"Donate 3 times before you can receive a reward!"`<br>`"EVENT_ABEGGAR_LEAVE"`<br>`"EVENT_ABEGGAR_QUES"` |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | `String` || 6 | `BigToe`<br>`Blessing`<br>`BodyOfGlorg_Gift` |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | `String` || 6 | `AdventureToken_BlueNeedle`<br>`AdventureToken_HasRunFromDeath`<br>`AdventureToken_HasTakenNeedle` |
| `party_damage` | `Number` || 6 | `1`<br>`10`<br>`2` |
| `set_frame` | `Number` || 5 | `1`<br>`10`<br>`15` |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | `String` || 4 | `MeatGolem`<br>`Mirage`<br>`MysteriousMachine_Bad` |
| [`conditional_reward`](./Miscellaneous.md#object-conditional_reward) | Object  || 4 | `{ . . . }` |
| [`random_pool`](./Arrays.md#array-random_pool) | Array  || 3 | `[` |
| [`get_item_from_pool`](./Arrays.md#array-get_item_from_pool) | `Array`  | Grants an item from the specified pool or a specific item name. | 2 | `Bird_items`<br>`Coin_items`<br>`Eye_items` |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | `String` || 2 | `AcidReflux`<br>`Albinism`<br>`Anxiety` |
| [`damage`](./Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 1 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| `next_event_bonus` | `Number` || 1 | `-1`<br>`-2`<br>`1` |
| [`random_mutation`](./Miscellaneous.md#object-random_mutation) | Object  | The number of random mutations applied to the unit. | 1 | `{ . . . }` |
| [`self_status_next_fight`](./Miscellaneous.md#object-self_status_next_fight) | Object  | An object defining status effects applied to the unit at the start of the next fight. | 1 | `{ . . . }` |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 | `AlienOvergrowthUnlocked`<br>`AntennaQuest_Orb`<br>`AntennaQuest_Rift` |

</details>


---


### Object: `leave`


**Definition:** Event Node: Story branch or dialog option representing the 'Leave' action.  
**Total Count:** 32

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`main`](./Events_and_Encounters.md#context-main), [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 32 | `common`<br>`rare`<br>`cha` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 32 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 32 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Variable || 32 | `cha`<br>`coins`<br>`con` |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 30 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 3 | `{ . . . }` |

</details>


---


### Object: `loot`


**Definition:** No definition provided.  
**Total Count:** 25

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 25 | `common`<br>`rare`<br>`cha` |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 25 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 25 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | Variable || 25 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 25 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 23 | `{ . . . }` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 2 | `{ . . . }` |

</details>


---


### Object: `mutation`


**Definition:** Event Object: Story branch or dialog option representing the 'Mutation' action.  
**Total Count:** 24

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`good`](./Events_and_Encounters.md#context-good), [`rare`](./Events_and_Encounters.md#context-rare), [`spawn_reflection_next_fight`](./Events_and_Encounters.md#context-spawn_reflection_next_fight)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `eyes` | Number || 13 | `-1`<br>`-2`<br>`1029` |
| `mouth` | Number | The catalog ID for the cat's mouth part. | 11 | `-1`<br>`-2`<br>`1` |
| `ears` | Number || 10 | `-1`<br>`-2`<br>`1500` |
| `eyebrows` | Number || 8 | `-1`<br>`-2`<br>`440` |
| [`head`](./Enums.md#enum-head) | Enum / Number  | The catalog ID for the cat's head part. | 7 | `-1`<br>`1`<br>`1.3` |
| `legs` | Number || 7 | `-1`<br>`306`<br>`322` |
| `arms` | Number || 6 | `900`<br>`[10 20]` |
| `body` | Number | The catalog ID for the cat's body part. | 6 | `-1`<br>`1`<br>`1.1` |
| `tail` | Integer | The catalog ID for the cat's tail part. | 6 | `-1`<br>`1000`<br>`1001` |
| `eye1` | Integer | The catalog ID for the cat's first eye part. | 3 | `-1`<br>`-2`<br>`1013` |
| `arm1` | Number | The catalog ID for the cat's first arm part. | 2 | `-1`<br>`-2`<br>`1` |
| `ear1` | Integer || 2 | `-2`<br>`1005`<br>`1013` |
| `eyebrow1` | Integer | The catalog ID for the cat's first eyebrow part. | 2 | `-2`<br>`1069` |
| `leg1` | Integer | The catalog ID for the cat's first leg part. | 2 | `-1`<br>`-2`<br>`1` |
| `eye2` | Integer | The catalog ID for the cat's second eye part. | 1 | `-1`<br>`1013`<br>`1057` |

</details>


---


### Object: `party_status_next_fight`


**Definition:** Event Penalty/Reward: Applies a status effect to the entire party at the start of the next combat encounter.  
**Total Count:** 24

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`rare`](./Events_and_Encounters.md#context-rare)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 22 | `passives`<br>`class`<br>`tag` |
| [`Fear`](./Enums.md) | Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 6 | `1`<br>`10`<br>`2` |
| [`Poison`](./Enums.md) | Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 5 | `1`<br>`10`<br>`2` |
| [`AbilityOnBattleStart_Immediate`](./Enums.md#enum-abilityonbattlestart_immediate) | Enum  || 3 | `BrambleRandomTileEvent`<br>`FlowerEventSleep`<br>`Flush` |
| [`NoHealthRegen`](./Enums.md) | Integer | Prevents the unit from regenerating health normally. | 3 | `1` |
| [`Bleed`](./Enums.md) | Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`10`<br>`2` |
| [`DivineShield`](./Enums.md) | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | `1`<br>`2`<br>`4` |
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 1 | `1`<br>`2`<br>`3` |
| [`Immobile`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 1 | `0`<br>`1`<br>`10%` |
| [`Tangled`](./Enums.md) | Integer | The number of stacks of the Tangled status effect applied, or an object defining its properties such as `stacks` and `alt_art`. | 1 | `1`<br>`2`<br>`[1, .05]` |
| [`Tarred`](./Enums.md) | Integer | The amount of tarred stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`2`<br>`[1 .1]` |
| [`Webbed`](./Enums.md) | Integer | The amount of webbed stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`2`<br>`[1 .1]` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `eat`


**Definition:** No definition provided.  
**Total Count:** 23

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 23 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 23 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 23 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | Variable || 23 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 23 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `setup`


**Definition:** Event Object: Pre-initialization logic executed before the event UI is drawn.  
**Total Count:** 23

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`main`](./Events_and_Encounters.md#context-main)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 23 | `common`<br>`rare`<br>`cha` |
| [`conditional_reward`](./Miscellaneous.md#object-conditional_reward) | Object  | An object defining a reward that is granted only if specified conditions are met. | 20 | `{ . . . }` |
| `set_frame` | `Number` || 3 | `1`<br>`10`<br>`15` |

</details>


---


### Object: `cutscene`


**Definition:** Event Object: Triggers a narrative cutscene.  
**Total Count:** 22

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bad`](./Events_and_Encounters.md#context-bad), [`good`](./Events_and_Encounters.md#context-good)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 21 | `common`<br>`rare`<br>`cha` |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | `String` | Specifies the name of a cutscene to play. | 21 | `"chaos_ending_bad"`<br>`"chaos_ending_good"`<br>`"chapterintros/bunker"` |
| `skip_result_screen` | Boolean || 21 | `true` |

</details>


---


### Object: `random_mutation_from_set`


**Definition:** Event Reward: Applies a random mutation to a character from a specific pool.  
**Total Count:** 22

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`rare`](./Events_and_Encounters.md#context-rare)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `mouth` | Number | The catalog ID for the cat's mouth part. | 9 | `-1`<br>`-2`<br>`1` |
| [`count`](./Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 8 | `0`<br>`1`<br>`10` |
| `tail` | Integer | The catalog ID for the cat's tail part. | 6 | `-1`<br>`1000`<br>`1001` |
| `ears` | Number || 5 | `-1`<br>`-2`<br>`1500` |
| `eyes` | Number || 5 | `-1`<br>`-2`<br>`1029` |
| `legs` | Number || 5 | `-1`<br>`306`<br>`322` |
| `body` | Number | The catalog ID for the cat's body part. | 3 | `-1`<br>`1`<br>`1.1` |
| `eyebrows` | Number || 3 | `-1`<br>`-2`<br>`440` |
| [`head`](./Enums.md#enum-head) | Enum / Number  | The catalog ID for the cat's head part. | 3 | `-1`<br>`1`<br>`1.3` |
| `arm1` | Number | The catalog ID for the cat's first arm part. | 2 | `-1`<br>`-2`<br>`1` |
| `arm2` | Number | The catalog ID for the cat's second arm part. | 2 | `-1`<br>`-2`<br>`1` |
| `leg1` | Integer | The catalog ID for the cat's first leg part. | 1 | `-1`<br>`-2`<br>`1` |
| `leg2` | Integer | The catalog ID for the cat's second leg part. | 1 | `-1`<br>`1`<br>`10` |
| `texture` | Integer | The catalog ID for the cat's texture. | 1 | `-1`<br>`1`<br>`1000` |

</details>


---


### Object: `random_mutation`


**Definition:** Event Reward: Applies a completely random mutation to a character.  
**Total Count:** 19

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`else`](./Events_and_Encounters.md#context-else), [`rare`](./Events_and_Encounters.md#context-rare)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`count`](./Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 15 | `0`<br>`1`<br>`10` |
| [`tag`](./Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 12 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| `asymmetric` | Boolean || 8 | `false`<br>`true` |

</details>


---


### Object: `smash`


**Definition:** No definition provided.  
**Total Count:** 16

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`label`](./Strings.md#string-label) | String || 16 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Variable || 16 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 14 | `common`<br>`rare`<br>`cha` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 14 | `false`<br>`true` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 12 | `{ . . . }` |
| [`copy_results`](./Enums.md#enum-copy_results) | Enum || 2 | `examine`<br>`lever`<br>`open` |

</details>


---


### Object: `destroy`


**Definition:** No definition provided.  
**Total Count:** 14

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 14 | `common`<br>`rare`<br>`cha` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 14 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 14 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 14 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 13 | `{ . . . }` |

</details>


---


### Object: `bash`


**Definition:** No definition provided.  
**Total Count:** 12

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 12 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 12 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 12 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 12 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 12 | `cha`<br>`coins`<br>`con` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |

</details>


---


### Object: `global_effect_next_fight`


**Definition:** Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter.  
**Total Count:** 11

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`good`](./Events_and_Encounters.md#context-good), [`rare`](./Events_and_Encounters.md#context-rare)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 8 | `passives`<br>`class`<br>`tag` |
| [`Fights`](./Enums.md) | Integer || 6 | `1`<br>`3`<br>`99` |
| [`CharacterTypeGainsStatusAtBattleStart`](./Miscellaneous.md#object-charactertypegainsstatusatbattlestart) | Object  || 5 | `{ . . . }` |
| [`StatusRandomEnemiesOnBattleStart`](./Passives_and_Statuses.md#object-statusrandomenemiesonbattlestart) | Object  || 3 | `{ . . . }` |
| [`KillEnemyOfTypeAtBattleStart`](./Miscellaneous.md#object-killenemyoftypeatbattlestart) | Object  | Specifies that a specific enemy type is killed at the start of the next battle. | 2 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `open`


**Definition:** Character Form: Behavior and stats for the 'Open' state.  
**Total Count:** 11

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`label`](./Strings.md#string-label) | String || 11 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 11 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 7 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 7 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 7 | `false`<br>`true` |
| [`copy_results`](./Enums.md#enum-copy_results) | Enum || 4 | `examine`<br>`lever`<br>`open` |

</details>


---


### Object: `sneak`


**Definition:** No definition provided.  
**Total Count:** 11

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 11 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 11 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 11 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | Variable || 11 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 11 | `cha`<br>`coins`<br>`con` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |

</details>


---


### Object: `leave_party_temporarily`


**Definition:** Event Action: Removes a character from the active team until the next hub area.  
**Total Count:** 9

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`rare`](./Events_and_Encounters.md#context-rare)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `fights_skipped` | Number || 7 | `0`<br>`1` |
| [`return_as`](./Enums.md#enum-return_as) | Enum || 3 | `enemy` |
| [`return_during`](./Enums.md#enum-return_during) | Enum || 3 | `boss` |

</details>


---


### Object: `take`


**Definition:** No definition provided.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 8 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 8 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 8 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 8 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 8 | `cha`<br>`coins`<br>`con` |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |

</details>


---


### Object: `a`


**Definition:** No definition provided.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 7 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 7 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 7 | `cha`<br>`coins`<br>`con` |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 5 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |

</details>


---


### Object: `attack`


**Definition:** No definition provided.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 7 | `common`<br>`rare`<br>`cha` |
| [`label`](./Strings.md#string-label) | String || 7 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 7 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 6 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 6 | `false`<br>`true` |

</details>


---


### Object: `b`


**Definition:** No definition provided.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 7 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 7 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 7 | `cha`<br>`coins`<br>`con` |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 5 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |

</details>


---


### Object: `c`


**Definition:** No definition provided.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 7 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 7 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 7 | `cha`<br>`coins`<br>`con` |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 5 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |

</details>


---


### Object: `charm`


**Definition:** No definition provided.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 7 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 7 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 7 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | Variable || 7 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 7 | `cha`<br>`coins`<br>`con` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |

</details>


---


### Object: `fight`


**Definition:** No definition provided.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 7 | `common`<br>`rare`<br>`cha` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 7 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | Variable || 7 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 7 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 6 | `{ . . . }` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |

</details>


---


### Object: `touch`


**Definition:** No definition provided.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 7 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | Variable || 7 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Variable || 7 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 7 | `common`<br>`rare`<br>`cha` |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 6 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 6 | `{ . . . }` |

</details>


---


### Object: `activate_p`


**Definition:** No definition provided.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 6 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 6 | `false`<br>`true` |
| [`label`](./Enums.md#enum-label) | Enum || 6 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 6 | `{ . . . }` |
| [`stat`](./Enums.md#enum-stat) | Enum || 6 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `activate_z`


**Definition:** No definition provided.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 6 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 6 | `false`<br>`true` |
| [`label`](./Enums.md#enum-label) | Enum || 6 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 6 | `{ . . . }` |
| [`stat`](./Enums.md#enum-stat) | Enum || 6 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `d`


**Definition:** No definition provided.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 6 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 6 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 6 | `cha`<br>`coins`<br>`con` |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 5 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |

</details>


---


### Object: `enter`


**Definition:** No definition provided.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 6 | `common`<br>`rare`<br>`cha` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 6 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | Variable || 6 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 5 | `{ . . . }` |
| [`stat`](./Enums.md#enum-stat) | Variable || 5 | `cha`<br>`coins`<br>`con` |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`hint_chapter_exit`](./Enums.md#enum-hint_chapter_exit) | Enum || 1 | `dimensionx`<br>`endoftime`<br>`future` |

</details>


---


### Object: `inspect`


**Definition:** No definition provided.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 6 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 6 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 6 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 6 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 6 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `lick`


**Definition:** No definition provided.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 6 | `common`<br>`rare`<br>`cha` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 6 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | Variable || 6 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Variable || 6 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 5 | `{ . . . }` |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |

</details>


---


### Object: `next_event_from_set`


**Definition:** Event Action: Chains immediately into a randomly selected subsequent story event.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`good`](./Events_and_Encounters.md#context-good), [`rare`](./Events_and_Encounters.md#context-rare)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`event`](./Enums.md#enum-event) | Enum || 5 | `Blessing`<br>`Death`<br>`Tragedy` |
| `same_cat` | Boolean || 5 | `true` |
| [`count`](./Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 4 | `0`<br>`1`<br>`10` |

</details>


---


### Object: `CharacterTypeGainsStatusAtBattleStart`


**Definition:** Encounter Modifier: Applies a status effect to all characters of a specific type (e.g., Cats, Bosses) at the start of battle.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`global_effect_next_fight`](./Events_and_Encounters.md#context-global_effect_next_fight)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](./Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 8 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 8 | `passives`<br>`class`<br>`tag` |
| [`Fear`](./Enums.md) | Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 3 | `1`<br>`10`<br>`2` |
| [`Stun`](./Enums.md) | Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`2`<br>`3` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid` | [`AllStatsUp`](./Enums.md) | Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | `-1`<br>`-2`<br>`1` |

</details>


---


### Object: `drink`


**Definition:** No definition provided.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 5 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 5 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 5 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | Variable || 5 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 5 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `kiss`


**Definition:** No definition provided.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 5 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 5 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 5 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 5 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 5 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `run`


**Definition:** No definition provided.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 5 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 5 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 5 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 5 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 5 | `cha`<br>`coins`<br>`con` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 2 | `{ . . . }` |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |

</details>


---


### Object: `bite`


**Definition:** No definition provided.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 4 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 4 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 4 | `false`<br>`true` |
| [`label`](./Enums.md#enum-label) | Enum || 4 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 4 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 4 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `damage`


**Definition:** The base damage properties of an attack.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 4 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 4 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 3 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`stat`](./Enums.md#enum-stat) | Enum || 3 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `go_around`


**Definition:** No definition provided.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 4 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 4 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 4 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 4 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Variable || 3 | `cha`<br>`coins`<br>`con` |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 2 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |

</details>


---


### Object: `home`


**Definition:** No definition provided.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 4 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 4 | `false`<br>`true` |
| [`hint_chapter_exit`](./Enums.md#enum-hint_chapter_exit) | Enum || 4 | `dimensionx`<br>`endoftime`<br>`future` |
| [`label`](./Enums.md#enum-label) | Enum || 4 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 4 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `outcome`


**Definition:** Event Object: Logic and text executed after selecting a specific dialog option.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`main`](./Events_and_Encounters.md#context-main)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 4 | `common`<br>`rare`<br>`cha` |
| [`play_animation`](./Arrays.md#array-play_animation) | Array / Enum  || 4 | `[resultBlessing .5]`<br>`[resultGood .5]`<br>`[resultLeave 0]` |
| [`random_pool`](./Arrays.md#array-random_pool) | Array  || 3 | `[` |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 | `AlienOvergrowth`<br>`Birdemic`<br>`GeomagneticStorm` |
| [`weather_roll`](./Arrays.md#array-weather_roll) | Array || 1 | `[` |

</details>


---


### Object: `party_permanent_stats_exclude_self`


**Definition:** Event Reward: Permanently modifies stats for all party members except the one who initiated the action.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`rare`](./Events_and_Encounters.md#context-rare)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cha`](./Enums.md#enum-cha) | Enum / Integer  | The Charisma stat value or modifier. | 4 | `+1`<br>`-1`<br>`-2` |
| [`con`](./Enums.md#enum-con) | Enum / Integer  | The Constitution stat value or modifier. | 4 | `-1`<br>`-2`<br>`-3` |
| [`dex`](./Enums.md#enum-dex) | Enum / Integer  || 4 | `-1`<br>`-2`<br>`-3` |
| [`int`](./Enums.md#enum-int) | Enum / Integer  || 4 | `-1`<br>`-10`<br>`-2` |
| [`lck`](./Enums.md#enum-lck) | Enum / Integer  || 4 | `-1`<br>`-2`<br>`-3` |
| [`spd`](./Enums.md#enum-spd) | Enum / Integer  | The Speed stat value or modifier. | 4 | `-1`<br>`-10`<br>`-2` |
| [`str`](./Enums.md#enum-str) | Enum / Integer  || 4 | `-1`<br>`-2`<br>`-3` |

</details>


---


### Object: `past`


**Definition:** No definition provided.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 4 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 4 | `false`<br>`true` |
| [`hint_chapter_exit`](./Enums.md#enum-hint_chapter_exit) | Enum || 4 | `dimensionx`<br>`endoftime`<br>`future` |
| [`label`](./Enums.md#enum-label) | Enum || 4 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 4 | `{ . . . }` |
| [`stat`](./Enums.md#enum-stat) | Enum || 4 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `skip`


**Definition:** No definition provided.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 4 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 4 | `{ . . . }` |
| [`label`](./Strings.md#string-label) | String || 4 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 4 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 4 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `investigate`


**Definition:** No definition provided.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 3 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 3 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 3 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 3 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 3 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `party_permanent_stats`


**Definition:** Event Reward: Permanently increases (or decreases) the core stats of all party members.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`main`](./Events_and_Encounters.md#context-main), [`rare`](./Events_and_Encounters.md#context-rare)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`con`](./Enums.md#enum-con) | Enum / Integer  | The Constitution stat value or modifier. | 2 | `-1`<br>`-2`<br>`-3` |

</details>


---


### Object: `repell`


**Definition:** No definition provided.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 3 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 3 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 3 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 3 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 3 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `spawn_reflection_next_fight`


**Definition:** No definition provided.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`rare`](./Events_and_Encounters.md#context-rare)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `StatusRandomEnemiesOnBattleStart`


**Definition:** Applies or references the 'StatusRandomEnemiesOnBattleStart' effect/state.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`global_effect_next_fight`](./Events_and_Encounters.md#context-global_effect_next_fight)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`count`](./Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 7 | `0`<br>`1`<br>`10` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 7 | `passives`<br>`class`<br>`tag` |
| [`Fear`](./Enums.md) | Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 3 | `1`<br>`10`<br>`2` |
| [`Bleed`](./Enums.md) | Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `attach_antenna`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 2 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 | `false`<br>`true` |
| [`label`](./Enums.md#enum-label) | Enum || 2 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 2 | `{ . . . }` |
| [`stat`](./Enums.md#enum-stat) | Enum || 2 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `boogers`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 2 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 2 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 2 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `copy`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 2 | `"1 injury"`<br>`"1"`<br>`"5"` |

</details>


---


### Object: `find_another_way`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 2 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 2 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 2 | `common`<br>`rare`<br>`cha` |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `gain_familiar`


**Definition:** Event Action: Adds a specific familiar to the party.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `initial_health` | Integer | The starting health of the unit when spawned. | 1 | `1`<br>`10`<br>`14` |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 1 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |

</details>


---


### Object: `KillEnemyOfTypeAtBattleStart`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`global_effect_next_fight`](./Events_and_Encounters.md#context-global_effect_next_fight)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`enemy_type`](./Enums.md#enum-enemy_type) | Enum || 2 | `any`<br>`cat` |
| [`fallback_spawn`](./Arrays.md#array-fallback_spawn) | Array || 1 | `[TomTom Kitten CatCaller Mangy]` |

</details>


---


### Object: `move_closer`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 2 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 2 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 2 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 2 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `party_random_mutation_from_set`


**Definition:** Event Reward: Applies a random mutation to the entire party from a specific pool.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bad`](./Events_and_Encounters.md#context-bad), [`rare`](./Events_and_Encounters.md#context-rare)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`count`](./Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 2 | `0`<br>`1`<br>`10` |
| `ears` | Number || 2 | `-1`<br>`-2`<br>`1500` |
| `eyebrows` | Number || 2 | `-1`<br>`-2`<br>`440` |
| `eyes` | Number || 2 | `-1`<br>`-2`<br>`1029` |
| `mouth` | Number | The catalog ID for the cat's mouth part. | 2 | `-1`<br>`-2`<br>`1` |

</details>


---


### Object: `play`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 2 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 2 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 2 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 2 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `poop`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 2 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 2 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 2 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `print`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 2 | `"1 injury"`<br>`"1"`<br>`"5"` |

</details>


---


### Object: `protection`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 2 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 2 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 2 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `random_chance`


**Definition:** Event Logic: Executes the nested outcome based on a percentage roll.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`reward`](./Events_and_Encounters.md#context-reward)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | `String` | Grants an item from the specified pool or a specific item name. | 1 | `Bird_items`<br>`Coin_items`<br>`Eye_items` |

</details>


---


### Object: `repair`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | Variable || 2 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Variable || 2 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 2 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |

</details>


---


### Object: `sacrifice`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 2 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 2 | `common`<br>`rare`<br>`cha` |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `scale`


**Definition:** Examples: `.75, 1.33, 1`  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 2 | `"1 injury"`<br>`"1"`<br>`"5"` |

</details>


---


### Object: `turnon`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 2 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 2 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 2 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 2 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `altar_sacrifice`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `arm`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `attach_amplifier`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Enums.md#enum-label) | Enum || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `attach_leech`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Enums.md#enum-label) | Enum || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `bash_past_alt`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `bite_it_off`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `blue`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`copy_results`](./Enums.md#enum-copy_results) | Enum || 1 | `examine`<br>`lever`<br>`open` |
| `fixed_chance` | Number || 1 | `50%` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `blue_needle`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `body`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`label`](./Enums.md#enum-label) | Enum || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `book`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `brace`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `break_ice`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `break_lock`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `bribe`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Enums.md#enum-label) | Enum || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `button`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`copy_results`](./Enums.md#enum-copy_results) | Enum || 1 | `examine`<br>`lever`<br>`open` |
| `fixed_chance` | Number || 1 | `50%` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `buy1`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum || 1 | `choice_no_coins` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |
| `stat_max` | Number || 1 | `1`<br>`10`<br>`15` |
| `stat_min` | Number || 1 | `1`<br>`10`<br>`15` |

</details>


---


### Object: `catch`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `challenge_to_game`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `chaos_ending`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `chapter_cutscene`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `charm_past_alt`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `climb`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `comfort`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `communicate`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `concheck`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `counter`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `crack_open`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `cross`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `cut_wires`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `damage_1`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `damage_full`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `damage_half`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `desert_cutscene`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `dexcheck`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `dig`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `disarm`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `dive`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `donate`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `donate_10`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum || 1 | `choice_no_coins` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |
| `stat_max` | Number || 1 | `1`<br>`10`<br>`15` |
| `stat_min` | Number || 1 | `1`<br>`10`<br>`15` |

</details>


---


### Object: `donate_15`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum || 1 | `choice_no_coins` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |
| `stat_max` | Number || 1 | `1`<br>`10`<br>`15` |
| `stat_min` | Number || 1 | `1`<br>`10`<br>`15` |

</details>


---


### Object: `donate_20`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum || 1 | `choice_no_coins` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |
| `stat_max` | Number || 1 | `1`<br>`10`<br>`15` |
| `stat_min` | Number || 1 | `1`<br>`10`<br>`15` |

</details>


---


### Object: `donate_5`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum || 1 | `choice_no_coins` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |
| `stat_max` | Number || 1 | `1`<br>`10`<br>`15` |
| `stat_min` | Number || 1 | `1`<br>`10`<br>`15` |

</details>


---


### Object: `double`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `eat_meat`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `enter_crater`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `face`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |

</details>


---


### Object: `fiddle`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Enums.md#enum-label) | Enum || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `fill_jar`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Enums.md#enum-label) | Enum || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `find`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `fire`


**Definition:** Character Form: Behavior and stats for the 'Fire' state.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `flush_yourself`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |

</details>


---


### Object: `follow`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `free`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `future`


**Definition:** Event Node: Story branch or dialog option representing the 'Future' action.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`hint_chapter_exit`](./Enums.md#enum-hint_chapter_exit) | Enum || 1 | `dimensionx`<br>`endoftime`<br>`future` |
| [`label`](./Enums.md#enum-label) | Enum || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `gain_clone_familiar`


**Definition:** Event Action: Adds a clone of a character to the party as a familiar.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`good`](./Events_and_Encounters.md#context-good)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 1 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |

</details>


---


### Object: `give_parasite`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |

</details>


---


### Object: `hack`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `head`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |

</details>


---


### Object: `holy`


**Definition:** Character Form: Behavior and stats for the \'Holy\' state.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `hp`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `ice`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `infinite`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`hint_chapter_exit`](./Enums.md#enum-hint_chapter_exit) | Enum || 1 | `dimensionx`<br>`endoftime`<br>`future` |
| [`label`](./Enums.md#enum-label) | Enum || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `intcheck`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `intimidation`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `itchies`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `join`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `jump`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `jump_over`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `keep_going`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `kiss_meat`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `knife`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `leave_it_in`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `leg`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `lever`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| `fixed_chance` | Number || 1 | `50%` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `lick_alt`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `lightning`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `listen`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `looks`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Enums.md#enum-label) | Enum || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `loot_heart`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Enums.md#enum-label) | Enum || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `makeup`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `mind`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`label`](./Enums.md#enum-label) | Enum || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `neck`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |

</details>


---


### Object: `nothanks`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `outsmart`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `patch_up`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `pick_lock`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `pilfer`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `pirouette`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `place_gristle`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Enums.md#enum-label) | Enum || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `power`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Enums.md#enum-label) | Enum || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `pull`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `pull_it_out`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `pull_lever`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |

</details>


---


### Object: `purify`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `push_buttons`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |

</details>


---


### Object: `push_through`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `put_in_coins`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum || 1 | `choice_no_coins` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |
| `stat_max` | Number || 1 | `1`<br>`10`<br>`15` |
| `stat_min` | Number || 1 | `1`<br>`10`<br>`15` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `put_out_of_misery`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `reach_inside`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `read`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `receive`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `red`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| `fixed_chance` | Number || 1 | `50%` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `red_needle`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `reflect`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `remove`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `remove_the_nail`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `repair_quest`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Enums.md#enum-label) | Enum || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `rest`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `revive`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `rub`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `run_again`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `run_away`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `sacrifice_full_favor`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `sacrifice_normal`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Enums.md#enum-label) | Enum || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `sacrifice_partial_favor`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `sacrifice_quest`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Enums.md#enum-label) | Enum || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `scream`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `shake`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `slip_through`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `sneak_by`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `sneak_past_alt`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `soul`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`label`](./Enums.md#enum-label) | Enum || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `speed`


**Definition:** Examples: `.5, 2, 20`  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `surprise`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `sweet_talk`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `swim`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `tail`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `take_blood`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Enums.md#enum-label) | Enum || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `talk`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Enums.md#enum-label) | Enum || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `talk_to`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `tappytoes`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `teleport`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `thorns`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `throw`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `timemachine`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `traverse`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |

</details>


---


### Object: `upgrade_yourself`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `use_item`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `use_toilet_con`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `use_toilet_str`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `use_weapon`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `w1`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `w2`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `w3`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `w4`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `w5`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `w6`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `wealth`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Enums.md#enum-label) | Enum || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `wheezies`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `wish_genes`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `wish_items`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `wish_levelups`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `wish_strength`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`stat`](./Enums.md#enum-stat) | Enum || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `withstand`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `yank_it_out`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `yellow_needle`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`label`](./Strings.md#string-label) | String || 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](./Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`stat`](./Math_Equations.md) | Equation || 1 | `cha`<br>`coins`<br>`con` |

</details>


---


---


## Auto-Discovered Objects


### Object: `buy2`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation` | String | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `animation_fail` | String | Specifies the animation to play when an action fails. | 1 | `choice_no_coins` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Miscellaneous.md#object-good) | Object  | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `{ . . . }` |
| `label` | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | String | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| `stat_max` | Number | The maximum stat value required for an event option to succeed. | 1 | `1`<br>`10`<br>`15` |
| `stat_min` | Number | The minimum stat value required for an event option to succeed. | 1 | `1`<br>`10`<br>`15` |

</details>


### Object: `buy3`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation` | String | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `animation_fail` | String | Specifies the animation to play when an action fails. | 1 | `choice_no_coins` |
| [`bad`](./Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`good`](./Miscellaneous.md#object-good) | Object  | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `{ . . . }` |
| `label` | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | String | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| `stat_max` | Number | The maximum stat value required for an event option to succeed. | 1 | `1`<br>`10`<br>`15` |
| `stat_min` | Number | The minimum stat value required for an event option to succeed. | 1 | `1`<br>`10`<br>`15` |

</details>


### Object: `pick`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation` | String | Specifies the animation played when the ability is used. | 3 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `copy_results` | String | Specifies the identifier of another option whose outcomes are replicated. | 3 | `examine`<br>`lever`<br>`open` |
| `label` | String | Specifies the localization key or display string for an event option. | 3 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | String | Specifies the stat used for a success check in an event option. | 3 | `cha`<br>`coins`<br>`con` |

</details>