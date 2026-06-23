# Mewgenics Mod Developer Documentation: Engine: Event Keys

## Engine: Event Keys

This document defines the schema shared by all Event Node blocks (`good`, `bad`, `main`, `reward`, `common`, `rare`). Each key in these blocks defines what happens as part of that event outcome.

> **Referenced by:** [`reward` (Events_and_Encounters)](./Events_and_Encounters.md#context-reward), [`common` (Events_and_Encounters)](./Events_and_Encounters.md#context-common), [`rare` (Events_and_Encounters)](./Events_and_Encounters.md#context-rare), [`good` (Events_and_Encounters)](./Events_and_Encounters.md#context-good), [`bad` (Events_and_Encounters)](./Events_and_Encounters.md#context-bad), [`main` (Events_and_Encounters)](./Events_and_Encounters.md#context-main), [`reward` (Miscellaneous)](./Miscellaneous.md#context-reward), [`common` (Miscellaneous)](./Miscellaneous.md#context-common), [`rare` (Miscellaneous)](./Miscellaneous.md#context-rare)

### Valid Property Keys

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `prompt` | String |  | 1730 |
| `set_frame` | Integer |  | 897 |
| [`common`](#common) | Block | Event Node: Story branch or dialog option representing the 'Common' action. | 634 |
| [`reward`](#reward) | Block | Event Node: Story branch or dialog option representing the 'Reward' action. | 633 |
| [`rare`](#rare) | Block | Event Node: Story branch or dialog option representing the 'Rare' action. | 629 |
| [`good`](#good) | Block |  | 550 |
| [`main`](#main) | Block |  | 215 |
| [`options`](#options) | Block | Event Block: Lists the available clickable dialog choices for the current story node. | 210 |
| [`get_item_from_pool`](./Enums.md#enum-get_item_from_pool) | Enum | Event Action: Rewards the player with an item drawn from a specific loot pool. | 195 |
| [`self_status_next_fight`](#self_status_next_fight) | Block | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 138 |
| [`permanent_stats`](#permanent_stats) | Block | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 126 |
| [`injury`](./Enums.md#enum-injury) | Enum |  | 92 |
| [`gain_disorder`](./Enums.md#enum-gain_disorder) | Enum |  | 85 |
| [`conditional_reward`](#conditional_reward) | Block | Event Action: Provides a reward only if a specific condition is met. | 78 |
| `random_mutation` | Integer | Event Reward: Applies a completely random mutation to a character. | 77 |
| [`gain_disorder_from_pool`](./Enums.md#enum-gain_disorder_from_pool) | Enum |  | 76 |
| [`increment_legacy_counter`](./Enums.md#enum-increment_legacy_counter) | Enum |  | 67 |
| [`event_now_same_cat`](./Enums.md#enum-event_now_same_cat) | Enum |  | 63 |
| [`get_item`](./Enums.md#enum-get_item) | Enum |  | 61 |
| [`play_animation`](./Enums.md#enum-play_animation) | Enum |  | 53 |
| [`set_adventure_token`](./Enums.md#enum-set_adventure_token) | Enum |  | 52 |
| `WorldEventLegacyCounter_Jack` | Variable |  | 50 |
| [`gain_familiar`](./Enums.md#enum-gain_familiar) | Enum | Event Action: Adds a specific familiar to the party. | 49 |
| [`clear_adventure_token`](./Enums.md#enum-clear_adventure_token) | Enum |  | 48 |
| [`get_parasite`](./Enums.md#enum-get_parasite) | Enum |  | 41 |
| [`spawn_unit_next_fight`](#spawn_unit_next_fight) | Block | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. | 40 |
| `damage` | Integer | Event Node: Story branch or dialog option representing the 'Damage' action. | 39 |
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum |  | 36 |
| [`get_parasite_from_pool`](./Enums.md#enum-get_parasite_from_pool) | Enum |  | 34 |
| `self_damage` | Integer | Recoil or self-inflicted damage/effects applied to the caster. | 34 |
| `resultHole` | Variable |  | 32 |
| `next_event_bonus` | Integer |  | 29 |
| `party_heal` | Integer |  | 26 |
| [`mutation`](#mutation) | Block | Event Node: Story branch or dialog option representing the 'Mutation' action. | 23 |
| [`party_status_next_fight`](#party_status_next_fight) | Block | Event Penalty/Reward: Applies a status effect to the entire party at the start of the next combat encounter. | 23 |
| [`setup`](#setup) | Block | Event Block: Pre-initialization logic executed before the event UI is drawn. | 23 |
| `cutscene` | String | Event Node: Triggers a narrative cutscene. | 22 |
| [`random_mutation_from_set`](#random_mutation_from_set) | Block | Event Reward: Applies a random mutation to a character from a specific pool. | 21 |
| `override_end_option_prompt` | String |  | 21 |
| `random` | Variable |  | 19 |
| `AdventureToken_HasTakenNeedle` | Variable |  | 18 |
| `complete_chapter` | Variable |  | 18 |
| [`event_now`](./Enums.md#enum-event_now) | Enum |  | 17 |
| [`party_damage`](./Arrays.md#array-party_damage) | Array |  | 17 |
| `ambush_next_basic_fights` | Integer |  | 17 |
| `ally_ambush_next_fights` | Integer |  | 16 |
| `full_heal` | Integer |  | 16 |
| [`add_weather`](./Enums.md#enum-add_weather) | Enum |  | 15 |
| [`kill`](./Enums.md#enum-kill) | Enum |  | 15 |
| [`lose_item`](./Enums.md#enum-lose_item) | Enum |  | 14 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 14 |
| `AdventureToken_BlueNeedle` | Variable |  | 14 |
| `AdventureToken_RedNeedle` | Variable |  | 14 |
| `cat` | Variable |  | 14 |
| [`battle`](./Math_Equations.md) | Equation |  | 13 |
| [`gain_coins`](./Arrays.md#array-gain_coins) | Array |  | 13 |
| [`shop_now`](./Enums.md#enum-shop_now) | Enum |  | 13 |
| [`trigger_adventure_unlock`](./Enums.md#enum-trigger_adventure_unlock) | Enum |  | 13 |
| [`begin_chapter`](./Enums.md#enum-begin_chapter) | Enum |  | 12 |
| [`complete_item_quest`](./Enums.md#enum-complete_item_quest) | Enum |  | 12 |
| [`lose_specific_item`](./Enums.md#enum-lose_specific_item) | Enum |  | 12 |
| `all_disorders` | Variable |  | 12 |
| `CharmedMaggot` | Variable |  | 11 |
| [`global_effect_next_fight`](#global_effect_next_fight) | Block | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 10 |
| [`learn_passive`](./Enums.md#enum-learn_passive) | Enum |  | 10 |
| [`set_subject`](./Enums.md#enum-set_subject) | Enum |  | 10 |
| `HasPlayedMysteriousStranger` | Variable |  | 10 |
| `auto` | Variable |  | 10 |
| `consumables` | Variable |  | 10 |
| [`level_up`](./Enums.md#enum-level_up) | Enum |  | 8 |
| `parasites` | Variable |  | 8 |
| `party_random_mutation` | Integer |  | 8 |
| [`leave_party_temporarily`](#leave_party_temporarily) | Block | Event Action: Removes a character from the active team until the next hub area. | 7 |
| [`next_event_from_set`](./Enums.md#enum-next_event_from_set) | Enum | Event Action: Chains immediately into a randomly selected subsequent story event. | 7 |
| `heal_disorder` | Integer |  | 7 |
| `spd` | Variable |  | 7 |
| [`decrement_legacy_counter`](./Enums.md#enum-decrement_legacy_counter) | Enum |  | 6 |
| `QEVENT_OBELISK_IGNORE` | Variable |  | 6 |
| `QEVENT_OBELISK_REW1` | Variable |  | 6 |
| `QEVENT_OBELISK_REW2` | Variable |  | 6 |
| `QEVENT_OBELISK_REW3` | Variable |  | 6 |
| `QEVENT_OBELISK_REW4` | Variable |  | 6 |
| `Stinky` | Variable |  | 6 |
| `WorldEventLegacyCounter_CrackInTheWall` | Variable |  | 6 |
| `WorldEventLegacyToken_StartDigging` | Variable |  | 6 |
| `hide_appearance_changes` | Integer |  | 6 |
| [`cutscene_on_exit`](./Enums.md#enum-cutscene_on_exit) | Enum |  | 5 |
| [`gain_food`](./Arrays.md#array-gain_food) | Array |  | 5 |
| `Bottles` | Variable |  | 5 |
| `SlagTight` | Variable |  | 5 |
| `blood_altar_items` | Variable |  | 5 |
| `cha` | Variable |  | 5 |
| `current_chapter_common` | Variable |  | 5 |
| `current_chapter_rare` | Variable |  | 5 |
| `food` | Variable |  | 5 |
| `physical_disorders` | Variable |  | 5 |
| [`bad`](#bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 4 |
| [`goto`](./Enums.md#enum-goto) | Enum |  | 4 |
| [`learn_ability`](./Enums.md#enum-learn_ability) | Enum |  | 4 |
| [`outcome`](#outcome) | Block | Event Block: Logic and text executed after selecting a specific dialog option. | 4 |
| [`party_permanent_stats_exclude_self`](#party_permanent_stats_exclude_self) | Block | Event Reward: Permanently modifies stats for all party members except the one who initiated the action. | 4 |
| [`upgrade_ability`](./Enums.md#enum-upgrade_ability) | Enum |  | 4 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 4 |
| `MysteriousStranger_HasLostFinger` | Variable |  | 4 |
| `QEVENT_THROBBINGARTERY_REW3` | Variable |  | 4 |
| `WorldEventLegacyCounter_ToiletFlushes` | Variable |  | 4 |
| `con` | Variable |  | 4 |
| `diseases` | Variable |  | 4 |
| `fleshhead_items` | Variable |  | 4 |
| `heal_injury` | Integer |  | 4 |
| `inventory` | Variable |  | 4 |
| `party_heal_disorder` | Integer |  | 4 |
| `pills` | Variable |  | 4 |
| [`learn_ability_from_pool`](./Arrays.md#array-learn_ability_from_pool) | Array |  | 3 |
| [`lose_item_from_inventory`](./Enums.md#enum-lose_item_from_inventory) | Enum |  | 3 |
| [`make_old`](./Enums.md#enum-make_old) | Enum |  | 3 |
| [`unlock_item_quest`](./Enums.md#enum-unlock_item_quest) | Enum |  | 3 |
| [`upgrade_passive`](./Enums.md#enum-upgrade_passive) | Enum |  | 3 |
| `CryogenicTimeChamber_Full` | Variable |  | 3 |
| `QEVENT_OBELISK_QUES2` | Variable |  | 3 |
| `QEVENT_VOLCANO_REW2` | Variable |  | 3 |
| `QEVENT_VOLCANO_REW3` | Variable |  | 3 |
| `RestlessDead` | Variable |  | 3 |
| `Scatological` | Variable |  | 3 |
| `SlagMight` | Variable |  | 3 |
| `bone_armor` | Variable |  | 3 |
| `bone_equipment` | Variable |  | 3 |
| `chapter_common` | Variable |  | 3 |
| `chapter_specific_item` | Variable |  | 3 |
| `end_of_time_unlock` | Variable |  | 3 |
| `gain_cat_familiar` | Integer |  | 3 |
| `max_options` | Integer |  | 3 |
| `mental_disorders` | Variable |  | 3 |
| `radiated` | Variable |  | 3 |
| `resultVeryGood` | Variable |  | 3 |
| `shuffle_options` | Boolean |  | 3 |
| `spawn_reflection_next_fight` | Integer | Event Penalty: Spawns dark clones/reflections of the party in the next combat encounter. | 3 |
| `weight` | Float | Probability weight for this outcome. | 3 |
| [`clear_surviving_kaiju`](./Enums.md#enum-clear_surviving_kaiju) | Enum |  | 2 |
| [`gain_immortal_familiar`](./Enums.md#enum-gain_immortal_familiar) | Enum |  | 2 |
| [`get_and_equip_item`](./Enums.md#enum-get_and_equip_item) | Enum |  | 2 |
| [`learn_passive_from_pool`](./Arrays.md#array-learn_passive_from_pool) | Array |  | 2 |
| [`party_permanent_stats`](#party_permanent_stats) | Block | Event Reward: Permanently increases (or decreases) the core stats of all party members. | 2 |
| [`party_random_mutation_from_set`](#party_random_mutation_from_set) | Block | Event Reward: Applies a random mutation to the entire party from a specific pool. | 2 |
| [`scramble_abilities`](./Enums.md#enum-scramble_abilities) | Enum |  | 2 |
| [`spin`](./Enums.md#enum-spin) | Enum |  | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| `AdventureToken_YellowNeedle` | Variable |  | 2 |
| `Anxiety` | Variable |  | 2 |
| `Cancer` | Variable |  | 2 |
| `CharmedPinky` | Variable |  | 2 |
| `CharmedRaptorBaby` | Variable |  | 2 |
| `Depression` | Variable |  | 2 |
| `HasHitPinata` | Variable |  | 2 |
| `HauntedNight` | Variable |  | 2 |
| `JarOfRadiatedBlood` | Variable |  | 2 |
| `PawShards` | Variable |  | 2 |
| `PutridLeech` | Variable |  | 2 |
| `PyrophinasCollar` | Variable |  | 2 |
| `QEVENT_OBELISK_QUES1` | Variable |  | 2 |
| `QEVENT_THROBBINGARTERY_REW1` | Variable |  | 2 |
| `QEVENT_THROBBINGARTERY_REW2` | Variable |  | 2 |
| `QEVENT_VOLCANO_REW1` | Variable |  | 2 |
| `ReceiverAntenna` | Variable |  | 2 |
| `Rocks` | Variable |  | 2 |
| `SignalAmplifier` | Variable |  | 2 |
| `Snake` | Variable |  | 2 |
| `ThrobbingGristle` | Variable |  | 2 |
| `TransmitterAntenna` | Variable |  | 2 |
| `ZaratanasCollar` | Variable |  | 2 |
| `all` | Variable |  | 2 |
| `clear_result_animation` | Integer |  | 2 |
| `flesh_items` | Variable |  | 2 |
| `glitched_items` | Variable |  | 2 |
| `map_unlock_dimensionx` | Variable |  | 2 |
| `party_heal_injury` | Integer |  | 2 |
| `poop_items` | Variable |  | 2 |
| `resultBad` | Variable |  | 2 |
| `set_age` | Integer |  | 2 |
| [`ambush`](./Math_Equations.md) | Equation |  | 1 |
| [`gain_clone_familiar`](#gain_clone_familiar) | Block | Event Action: Adds a clone of a character to the party as a familiar. | 1 |
| [`get_full_item_set_from_pool`](./Enums.md#enum-get_full_item_set_from_pool) | Enum |  | 1 |
| [`leave`](#leave) | Block | Event Node: Story branch or dialog option representing the 'Leave' action. | 1 |
| [`lose_all_equipped_items`](./Enums.md#enum-lose_all_equipped_items) | Enum |  | 1 |
| [`party_injury`](./Enums.md#enum-party_injury) | Enum |  | 1 |
| [`play_result_animation`](./Enums.md#enum-play_result_animation) | Enum |  | 1 |
| [`random_chance`](#random_chance) | Block | Event Logic: Executes the nested outcome based on a percentage roll. | 1 |
| [`requires_flag`](./Enums.md#enum-requires_flag) | Enum | Prerequisite: Must meet this condition. | 1 |
| [`scramble_basic_attack`](./Enums.md#enum-scramble_basic_attack) | Enum |  | 1 |
| [`scramble_passives`](./Enums.md#enum-scramble_passives) | Enum |  | 1 |
| [`select_item_from_pool_for_cutscene_only`](./Enums.md#enum-select_item_from_pool_for_cutscene_only) | Enum |  | 1 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| `AdventureToken_HasRunFromDeath` | Variable |  | 1 |
| `AdventureToken_MysteriousCave_FamiliarVoice` | Variable |  | 1 |
| `AdventureToken_MysteriousJarRepeat` | Variable |  | 1 |
| `AdventureToken_StevenTryAgain2` | Variable |  | 1 |
| `AdventureToken_StevenTryAgain3` | Variable |  | 1 |
| `AdventureToken_StevenTryAgain` | Variable |  | 1 |
| `AdventureToken_TrippedOnBigToe` | Variable |  | 1 |
| `AdventureToken_UnmarkedGraveForced` | Variable |  | 1 |
| `Albinism` | Variable |  | 1 |
| `AlienOvergrowth` | Variable |  | 1 |
| `AntennaQuest_Orb` | Variable |  | 1 |
| `AntennaQuest_Rift` | Variable |  | 1 |
| `AntennaQuest_Volcano` | Variable |  | 1 |
| `Beepis` | Variable |  | 1 |
| `BrainDamage` | Variable |  | 1 |
| `BrainDead` | Variable |  | 1 |
| `Brave` | Variable |  | 1 |
| `CharmedTarBaby` | Variable |  | 1 |
| `CryogenicTimeChamber_Empty` | Variable |  | 1 |
| `Cunch` | Variable |  | 1 |
| `CursedStickman` | Variable |  | 1 |
| `DeathsScythe` | Variable |  | 1 |
| `EVENT_USETHETOILET_AGAIN` | Variable |  | 1 |
| `EnchantingPoop` | Variable |  | 1 |
| `FecalHood_Cursed` | Variable |  | 1 |
| `FecalMask_Cursed` | Variable |  | 1 |
| `Feebis` | Variable |  | 1 |
| `GeomagneticStorm` | Variable |  | 1 |
| `Gigachad` | Variable |  | 1 |
| `GuillotinasHead` | Variable |  | 1 |
| `Host` | Variable |  | 1 |
| `JarOfChaos` | Variable |  | 1 |
| `JarOfRadiation` | Variable |  | 1 |
| `MeatWorldQuest_Gristle` | Variable |  | 1 |
| `MeatWorldQuest_Leech` | Variable |  | 1 |
| `MeteorShowerUnlocked` | Variable |  | 1 |
| `MomsKnife` | Variable |  | 1 |
| `MysteriousTomb1` | Variable |  | 1 |
| `MysteriousTomb2` | Variable |  | 1 |
| `PuncturedEye` | Variable |  | 1 |
| `QEVENT_BROKENTIMEMACHINE_QUES` | Variable |  | 1 |
| `QEVENT_BROKENTIMEMACHINE_REW2` | Variable |  | 1 |
| `QEVENT_BROKENTIMEMACHINE_REW3` | Variable |  | 1 |
| `QEVENT_BROKENTIMEMACHINE_REW4` | Variable |  | 1 |
| `QEVENT_BROKENTIMEMACHINE_REW5` | Variable |  | 1 |
| `QEVENT_DEADGOD_QUES` | Variable |  | 1 |
| `QEVENT_DEADGOD_REW1` | Variable |  | 1 |
| `QEVENT_DEADGOD_REW2` | Variable |  | 1 |
| `QEVENT_DEADGOD_REW3` | Variable |  | 1 |
| `QEVENT_DEADKING_QUES` | Variable |  | 1 |
| `QEVENT_DEADKING_REW1` | Variable |  | 1 |
| `QEVENT_DEADKING_REW2` | Variable |  | 1 |
| `QEVENT_DEADKING_REW3` | Variable |  | 1 |
| `QEVENT_DEADKING_REW4` | Variable |  | 1 |
| `QEVENT_DEADKING_REW5` | Variable |  | 1 |
| `QEVENT_DIMENSIONXPORTAL_ENTER_REW` | Variable |  | 1 |
| `QEVENT_DIMENSIONXPORTAL_IGNORE_ANSW` | Variable |  | 1 |
| `QEVENT_DIMENSIONXPORTAL_QUES` | Variable |  | 1 |
| `QEVENT_GLOWINGORB_QUES2` | Variable |  | 1 |
| `QEVENT_GLOWINGORB_QUES` | Variable |  | 1 |
| `QEVENT_GLOWINGORB_REW1` | Variable |  | 1 |
| `QEVENT_GLOWINGORB_REW2` | Variable |  | 1 |
| `QEVENT_GLOWINGORB_REW3` | Variable |  | 1 |
| `QEVENT_GLOWINGORB_REW4` | Variable |  | 1 |
| `QEVENT_GLOWINGORB_REW5` | Variable |  | 1 |
| `QEVENT_GLOWINGORB_REW7` | Variable |  | 1 |
| `QEVENT_MEATALTAR_QUES1` | Variable |  | 1 |
| `QEVENT_MEATALTAR_REW1` | Variable |  | 1 |
| `QEVENT_MEATALTAR_REW_IGNORE` | Variable |  | 1 |
| `QEVENT_OBELISK_CORE_REW_ZARA3` | Variable |  | 1 |
| `QEVENT_OBELISK_MOON_REW_PYRO3` | Variable |  | 1 |
| `QEVENT_OBELISK_QUES3` | Variable |  | 1 |
| `QEVENT_THEHEAD_QUES` | Variable |  | 1 |
| `QEVENT_THEHEAD_REW1` | Variable |  | 1 |
| `QEVENT_THEHEAD_REW2` | Variable |  | 1 |
| `QEVENT_THEHEAD_REW3` | Variable |  | 1 |
| `QEVENT_THEHEAD_REW5` | Variable |  | 1 |
| `QEVENT_THEHEAD_REW6` | Variable |  | 1 |
| `QEVENT_THROBBINGARTERY2_QUES` | Variable |  | 1 |
| `QEVENT_THROBBINGARTERY2_REW_IGNORE` | Variable |  | 1 |
| `QEVENT_THROBBINGARTERY_QUES1` | Variable |  | 1 |
| `QEVENT_THROBBINGARTERY_QUES2` | Variable |  | 1 |
| `QEVENT_THROBBINGARTERY_REW5` | Variable |  | 1 |
| `QEVENT_THROBBINGARTERY_REW_IGNORE` | Variable |  | 1 |
| `QEVENT_TIMEMACHINE_FUTURE_QUES` | Variable |  | 1 |
| `QEVENT_TIMEMACHINE_FUTURE_REW1` | Variable |  | 1 |
| `QEVENT_TIMEMACHINE_FUTURE_REW2` | Variable |  | 1 |
| `QEVENT_TIMEMACHINE_ICEAGE_QUES` | Variable |  | 1 |
| `QEVENT_TIMEMACHINE_ICEAGE_REW1` | Variable |  | 1 |
| `QEVENT_TIMEMACHINE_ICEAGE_REW2` | Variable |  | 1 |
| `QEVENT_TIMEMACHINE_JURASSIC_QUES` | Variable |  | 1 |
| `QEVENT_TIMEMACHINE_JURASSIC_REW1` | Variable |  | 1 |
| `QEVENT_TIMEMACHINE_JURASSIC_REW2` | Variable |  | 1 |
| `QEVENT_TIMEMACHINE_QUES` | Variable |  | 1 |
| `QEVENT_TIMEMACHINE_REW1` | Variable |  | 1 |
| `QEVENT_TIMEMACHINE_REW2` | Variable |  | 1 |
| `QEVENT_TIMEMACHINE_REW3` | Variable |  | 1 |
| `QEVENT_TIMEMACHINE_THEEND_QUES` | Variable |  | 1 |
| `QEVENT_TIMEMACHINE_THEEND_REW1` | Variable |  | 1 |
| `QEVENT_TIMEMACHINE_THEEND_REW2` | Variable |  | 1 |
| `QEVENT_VOLCANO_QUES2` | Variable |  | 1 |
| `QEVENT_VOLCANO_QUES` | Variable |  | 1 |
| `QEVENT_VOLCANO_REW4` | Variable |  | 1 |
| `QEVENT_VOLCANO_REW5` | Variable |  | 1 |
| `QEVENT_VOLCANO_REW7` | Variable |  | 1 |
| `QEVENT_WALLOFFLESH2_QUES` | Variable |  | 1 |
| `QEVENT_WALLOFFLESH2_REW_IGNORE` | Variable |  | 1 |
| `QEVENT_WALLOFFLESH_QUES1` | Variable |  | 1 |
| `QEVENT_WALLOFFLESH_QUES2` | Variable |  | 1 |
| `QEVENT_WALLOFFLESH_REW10` | Variable |  | 1 |
| `QEVENT_WALLOFFLESH_REW1` | Variable |  | 1 |
| `QEVENT_WALLOFFLESH_REW2` | Variable |  | 1 |
| `QEVENT_WALLOFFLESH_REW3` | Variable |  | 1 |
| `QEVENT_WALLOFFLESH_REW4` | Variable |  | 1 |
| `QEVENT_WALLOFFLESH_REW5` | Variable |  | 1 |
| `QEVENT_WALLOFFLESH_REW7` | Variable |  | 1 |
| `QEVENT_WALLOFFLESH_REW8` | Variable |  | 1 |
| `QEVENT_WALLOFFLESH_REW9` | Variable |  | 1 |
| `QEVENT_WALLOFFLESH_REW_IGNORE` | Variable |  | 1 |
| `RaptorEgg` | Variable |  | 1 |
| `SludgeHat` | Variable |  | 1 |
| `SludgeMask` | Variable |  | 1 |
| `Soulless` | Variable |  | 1 |
| `Steven_disorders` | Variable |  | 1 |
| `StrangeEggs` | Variable |  | 1 |
| `TheRift_UsedPyrophina` | Variable |  | 1 |
| `TheRift_UsedZaratana` | Variable |  | 1 |
| `TheShimmer` | Variable |  | 1 |
| `Touched` | Variable |  | 1 |
| `WorldEventLegacyCounter_SealedCrypt` | Variable |  | 1 |
| `WorldEventLegacyToken_CryptOpened` | Variable |  | 1 |
| `WorldEventLegacyToken_HasRunFromDeath` | Variable |  | 1 |
| `WorldEventLegacyToken_MomsKnife` | Variable |  | 1 |
| `WorldEventLegacyToken_MonkeyPaw1` | Variable |  | 1 |
| `WorldEventLegacyToken_MonkeyPaw2` | Variable |  | 1 |
| `WorldEventLegacyToken_MonkeyPaw3` | Variable |  | 1 |
| `WorldEventLegacyToken_MonkeyPaw4` | Variable |  | 1 |
| `WorldEventLegacyToken_MonkeyPawGenes` | Variable |  | 1 |
| `WorldEventLegacyToken_MonkeyPawItems` | Variable |  | 1 |
| `WorldEventLegacyToken_MonkeyPawKnowledge` | Variable |  | 1 |
| `WorldEventLegacyToken_MonkeyPawStrength` | Variable |  | 1 |
| `WorldEventLegacyToken_StacyMutant` | Variable |  | 1 |
| `alley` | Variable |  | 1 |
| `bleeding` | Variable |  | 1 |
| `bloody_items` | Variable |  | 1 |
| `boneyard` | Variable |  | 1 |
| `bunker` | Variable |  | 1 |
| `burned` | Variable |  | 1 |
| `caves` | Variable |  | 1 |
| `chapter_rare` | Variable |  | 1 |
| `chapter` | Variable |  | 1 |
| `clone_self_to_party` | Integer |  | 1 |
| `copy_items_to_party` | Integer |  | 1 |
| `copy_party_items` | Integer |  | 1 |
| `core` | Variable |  | 1 |
| `crater` | Variable |  | 1 |
| `cursed` | Variable |  | 1 |
| `desert` | Variable |  | 1 |
| `dex` | Variable |  | 1 |
| `dimensionx.gon` | Variable |  | 1 |
| `dimensionx` | Variable |  | 1 |
| `future` | Variable |  | 1 |
| `general_common` | Variable |  | 1 |
| `general_rare` | Variable |  | 1 |
| `godly_items` | Variable |  | 1 |
| `grass_items` | Variable |  | 1 |
| `hide_items` | Variable |  | 1 |
| `iceage.gon` | Variable |  | 1 |
| `iceage` | Variable |  | 1 |
| `junkyard_items` | Variable |  | 1 |
| `junkyard` | Variable |  | 1 |
| `jurassic` | Variable |  | 1 |
| `lab` | Variable |  | 1 |
| `legacy_event_unlock_momsknife` | Variable |  | 1 |
| `map_unlock_iceage` | Variable |  | 1 |
| `mapflag_ChaosAntennaAttached` | Variable |  | 1 |
| `mapflag_OrbAntennaAttached` | Variable |  | 1 |
| `mapflag_ThrobbingArteryDone` | Variable |  | 1 |
| `mapflag_VolcanoAntennaAttached` | Variable |  | 1 |
| `mapflag_WallOfFleshDone` | Variable |  | 1 |
| `meat_world_open` | Variable |  | 1 |
| `meatworld` | Variable |  | 1 |
| `monkey_paw_1finger` | Variable |  | 1 |
| `monkey_paw_2fingers` | Variable |  | 1 |
| `monkey_paw_3fingers` | Variable |  | 1 |
| `monkey_paw_4fingers` | Variable |  | 1 |
| `moon` | Variable |  | 1 |
| `parasite` | Variable |  | 1 |
| `raptor_nest_eggs` | Variable |  | 1 |
| `resultConfused` | Variable |  | 1 |
| `resultVeryBad` | Variable |  | 1 |
| `rock_items` | Variable |  | 1 |
| `self_heal` | Integer |  | 1 |
| `sewers` | Variable |  | 1 |
| `tech_items` | Variable |  | 1 |
| `theend` | Variable |  | 1 |
| `time_machine_quest_finalstep` | Variable |  | 1 |
| `time_machine_quest_trigger` | Variable |  | 1 |
| `trigger_butterfly_effect` | Integer |  | 1 |

</details>

### Valid Nested Blocks

The following blocks all behave as `{Event Keys}` containers. Each has its own unique parameters listed below its entry.

---

#### `bad`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 343

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward`](#reward) | Block | Event Node: Story branch or dialog option representing the 'Reward' action. | 307 |
| `set_frame` | Integer |  | 224 |
| `prompt` | String |  | 42 |
| [`conditional_reward`](#conditional_reward) | Block | Event Action: Provides a reward only if a specific condition is met. | 9 |
| [`injury`](./Enums.md#enum-injury) | Enum |  | 8 |
| [`play_animation`](./Arrays.md#array-play_animation) | Array |  | 5 |
| [`battle`](./Math_Equations.md) | Equation |  | 4 |
| [`gain_disorder_from_pool`](./Enums.md#enum-gain_disorder_from_pool) | Enum |  | 4 |
| [`kill`](./Enums.md#enum-kill) | Enum |  | 4 |
| [`self_status_next_fight`](#self_status_next_fight) | Block | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 4 |
| [`cutscene`](#cutscene) | Block | Event Node: Triggers a narrative cutscene. | 3 |
| [`event_now_same_cat`](./Enums.md#enum-event_now_same_cat) | Enum |  | 3 |
| [`event_now`](./Enums.md#enum-event_now) | Enum |  | 3 |
| [`get_parasite_from_pool`](./Enums.md#enum-get_parasite_from_pool) | Enum |  | 3 |
| `next_event_bonus` | Integer |  | 2 |
| [`gain_immortal_familiar`](./Enums.md#enum-gain_immortal_familiar) | Enum |  | 1 |
| [`get_parasite`](./Enums.md#enum-get_parasite) | Enum |  | 1 |
| [`lose_item`](./Enums.md#enum-lose_item) | Enum |  | 1 |
| [`party_random_mutation_from_set`](#party_random_mutation_from_set) | Block | Event Reward: Applies a random mutation to the entire party from a specific pool. | 1 |
| [`permanent_stats`](#permanent_stats) | Block | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 1 |
| [`select_item_from_pool_for_cutscene_only`](./Enums.md#enum-select_item_from_pool_for_cutscene_only) | Enum |  | 1 |
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `common`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1197

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `prompt` | String |  | 609 |
| `set_frame` | Integer |  | 151 |
| [`self_status_next_fight`](#self_status_next_fight) | Block | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 93 |
| [`get_item_from_pool`](./Enums.md#enum-get_item_from_pool) | Enum | Event Action: Rewards the player with an item drawn from a specific loot pool. | 64 |
| [`permanent_stats`](#permanent_stats) | Block | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 41 |
| [`injury`](./Enums.md#enum-injury) | Enum |  | 27 |
| `random_mutation` | Integer | Event Reward: Applies a completely random mutation to a character. | 25 |
| [`clear_adventure_token`](./Enums.md#enum-clear_adventure_token) | Enum |  | 24 |
| `damage` | Integer | Event Node: Story branch or dialog option representing the 'Damage' action. | 24 |
| [`gain_disorder_from_pool`](./Enums.md#enum-gain_disorder_from_pool) | Enum |  | 23 |
| `self_damage` | Integer | Recoil or self-inflicted damage/effects applied to the caster. | 22 |
| [`event_now_same_cat`](./Enums.md#enum-event_now_same_cat) | Enum |  | 21 |
| [`gain_familiar`](./Enums.md#enum-gain_familiar) | Enum | Event Action: Adds a specific familiar to the party. | 19 |
| [`spawn_unit_next_fight`](#spawn_unit_next_fight) | Block | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. | 18 |
| `party_heal` | Integer |  | 15 |
| [`get_item`](./Enums.md#enum-get_item) | Enum |  | 14 |
| [`play_animation`](./Arrays.md#array-play_animation) | Array |  | 13 |
| `heal` | Integer |  | 13 |
| [`gain_disorder`](./Enums.md#enum-gain_disorder) | Enum |  | 12 |
| [`party_status_next_fight`](#party_status_next_fight) | Block | Event Penalty/Reward: Applies a status effect to the entire party at the start of the next combat encounter. | 11 |
| `override_end_option_prompt` | String |  | 11 |
| `ally_ambush_next_fights` | Integer |  | 10 |
| `full_heal` | Integer |  | 10 |
| [`conditional_reward`](#conditional_reward) | Block | Event Action: Provides a reward only if a specific condition is met. | 9 |
| [`get_parasite_from_pool`](./Enums.md#enum-get_parasite_from_pool) | Enum |  | 9 |
| [`party_damage`](./Arrays.md#array-party_damage) | Array |  | 9 |
| [`set_adventure_token`](./Enums.md#enum-set_adventure_token) | Enum |  | 9 |
| `ambush_next_basic_fights` | Integer |  | 9 |
| [`random_mutation_from_set`](#random_mutation_from_set) | Block | Event Reward: Applies a random mutation to a character from a specific pool. | 8 |
| [`get_parasite`](./Enums.md#enum-get_parasite) | Enum |  | 7 |
| `next_event_bonus` | Integer |  | 7 |
| [`gain_coins`](./Arrays.md#array-gain_coins) | Array |  | 6 |
| [`global_effect_next_fight`](#global_effect_next_fight) | Block | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 6 |
| [`increment_legacy_counter`](./Enums.md#enum-increment_legacy_counter) | Enum |  | 6 |
| [`kill`](./Enums.md#enum-kill) | Enum |  | 5 |
| [`lose_item`](./Enums.md#enum-lose_item) | Enum |  | 5 |
| [`shop_now`](./Enums.md#enum-shop_now) | Enum |  | 5 |
| [`add_weather`](./Enums.md#enum-add_weather) | Enum |  | 4 |
| [`gain_food`](./Arrays.md#array-gain_food) | Array |  | 3 |
| [`event_now`](./Enums.md#enum-event_now) | Enum |  | 2 |
| [`lose_specific_item`](./Enums.md#enum-lose_specific_item) | Enum |  | 2 |
| [`next_event_from_set`](#next_event_from_set) | Block | Event Action: Chains immediately into a randomly selected subsequent story event. | 2 |
| [`party_permanent_stats_exclude_self`](#party_permanent_stats_exclude_self) | Block | Event Reward: Permanently modifies stats for all party members except the one who initiated the action. | 2 |
| [`spin`](./Enums.md#enum-spin) | Enum |  | 2 |
| `party_heal_disorder` | Integer |  | 2 |
| [`decrement_legacy_counter`](./Enums.md#enum-decrement_legacy_counter) | Enum |  | 1 |
| [`get_and_equip_item`](./Enums.md#enum-get_and_equip_item) | Enum |  | 1 |
| [`learn_ability_from_pool`](./Enums.md#enum-learn_ability_from_pool) | Enum |  | 1 |
| [`mutation`](#mutation) | Block | Event Node: Story branch or dialog option representing the 'Mutation' action. | 1 |
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum |  | 1 |
| [`upgrade_ability`](./Enums.md#enum-upgrade_ability) | Enum |  | 1 |
| `clear_result_animation` | Integer |  | 1 |
| `heal_disorder` | Integer |  | 1 |
| `heal_injury` | Integer |  | 1 |
| `self_heal` | Integer |  | 1 |
| [`random_pool`](./Arrays.md#array-random_pool) | Array |  | 0 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `good`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 572

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward`](#reward) | Block | Event Node: Story branch or dialog option representing the 'Reward' action. | 326 |
| `set_frame` | Integer |  | 285 |
| `prompt` | String |  | 185 |
| [`increment_legacy_counter`](./Enums.md#enum-increment_legacy_counter) | Enum |  | 52 |
| [`conditional_reward`](#conditional_reward) | Block | Event Action: Provides a reward only if a specific condition is met. | 38 |
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum |  | 26 |
| [`play_animation`](./Enums.md#enum-play_animation) | Enum |  | 20 |
| `cutscene` | String | Event Node: Triggers a narrative cutscene. | 19 |
| [`begin_chapter`](./Enums.md#enum-begin_chapter) | Enum |  | 12 |
| [`complete_item_quest`](./Enums.md#enum-complete_item_quest) | Enum |  | 12 |
| [`set_adventure_token`](./Enums.md#enum-set_adventure_token) | Enum |  | 12 |
| `random_mutation` | Integer | Event Reward: Applies a completely random mutation to a character. | 12 |
| [`event_now_same_cat`](./Enums.md#enum-event_now_same_cat) | Enum |  | 9 |
| [`event_now`](./Enums.md#enum-event_now) | Enum |  | 9 |
| [`gain_disorder`](./Enums.md#enum-gain_disorder) | Enum |  | 8 |
| [`lose_specific_item`](./Enums.md#enum-lose_specific_item) | Enum |  | 8 |
| [`trigger_adventure_unlock`](./Enums.md#enum-trigger_adventure_unlock) | Enum |  | 7 |
| [`add_weather`](./Enums.md#enum-add_weather) | Enum |  | 6 |
| [`get_item_from_pool`](./Enums.md#enum-get_item_from_pool) | Enum | Event Action: Rewards the player with an item drawn from a specific loot pool. | 5 |
| [`get_item`](./Enums.md#enum-get_item) | Enum |  | 5 |
| `heal_disorder` | Integer |  | 5 |
| [`injury`](./Enums.md#enum-injury) | Enum |  | 4 |
| [`level_up`](./Enums.md#enum-level_up) | Enum |  | 4 |
| [`mutation`](#mutation) | Block | Event Node: Story branch or dialog option representing the 'Mutation' action. | 4 |
| [`rare`](#rare) | Block | Event Node: Story branch or dialog option representing the 'Rare' action. | 4 |
| [`get_parasite`](./Enums.md#enum-get_parasite) | Enum |  | 3 |
| [`kill`](./Enums.md#enum-kill) | Enum |  | 3 |
| [`unlock_item_quest`](./Enums.md#enum-unlock_item_quest) | Enum |  | 3 |
| `heal_injury` | Integer |  | 3 |
| [`clear_surviving_kaiju`](./Enums.md#enum-clear_surviving_kaiju) | Enum |  | 2 |
| [`cutscene_on_exit`](./Enums.md#enum-cutscene_on_exit) | Enum |  | 2 |
| [`gain_disorder_from_pool`](./Enums.md#enum-gain_disorder_from_pool) | Enum |  | 2 |
| `full_heal` | Integer |  | 2 |
| `override_end_option_prompt` | String |  | 2 |
| [`gain_clone_familiar`](#gain_clone_familiar) | Block | Event Action: Adds a clone of a character to the party as a familiar. | 1 |
| [`get_full_item_set_from_pool`](./Enums.md#enum-get_full_item_set_from_pool) | Enum |  | 1 |
| [`global_effect_next_fight`](#global_effect_next_fight) | Block | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 1 |
| [`learn_ability_from_pool`](./Arrays.md#array-learn_ability_from_pool) | Array |  | 1 |
| [`learn_passive_from_pool`](./Arrays.md#array-learn_passive_from_pool) | Array |  | 1 |
| [`lose_item`](./Enums.md#enum-lose_item) | Enum |  | 1 |
| [`next_event_from_set`](#next_event_from_set) | Block | Event Action: Chains immediately into a randomly selected subsequent story event. | 1 |
| [`scramble_abilities`](./Enums.md#enum-scramble_abilities) | Enum |  | 1 |
| [`scramble_passives`](./Enums.md#enum-scramble_passives) | Enum |  | 1 |
| [`shop_now`](./Enums.md#enum-shop_now) | Enum |  | 1 |
| [`upgrade_ability`](./Enums.md#enum-upgrade_ability) | Enum |  | 1 |
| [`upgrade_passive`](./Enums.md#enum-upgrade_passive) | Enum |  | 1 |
| `ally_ambush_next_fights` | Integer |  | 1 |
| `clone_self_to_party` | Integer |  | 1 |
| `copy_items_to_party` | Integer |  | 1 |
| `copy_party_items` | Integer |  | 1 |
| `heal` | Integer |  | 1 |
| `next_event_bonus` | Integer |  | 1 |
| `trigger_butterfly_effect` | Integer |  | 1 |
| [`gain_food`](./Arrays.md#array-gain_food) | Array |  | 0 |
| [`party_gain_disorder_from_pool`](./Arrays.md#array-party_gain_disorder_from_pool) | Array |  | 0 |
| [`random_pool_consider_luck`](./Arrays.md#array-random_pool_consider_luck) | Array |  | 0 |
| [`random_pool`](./Arrays.md#array-random_pool) | Array |  | 0 |
| [`transform_item`](./Arrays.md#array-transform_item) | Array |  | 0 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `main`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 215

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`options`](#options) | Block | Event Block: Lists the available clickable dialog choices for the current story node. | 210 |
| `prompt` | String |  | 208 |
| [`setup`](#setup) | Block | Event Block: Pre-initialization logic executed before the event UI is drawn. | 23 |
| [`bad`](#bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 4 |
| [`goto`](./Enums.md#enum-goto) | Enum |  | 4 |
| [`outcome`](#outcome) | Block | Event Block: Logic and text executed after selecting a specific dialog option. | 4 |
| `max_options` | Integer |  | 3 |
| `set_frame` | Integer |  | 3 |
| `shuffle_options` | Boolean |  | 3 |
| `weight` | Float | Probability weight for this outcome. | 2 |
| [`add_weather`](./Enums.md#enum-add_weather) | Enum |  | 1 |
| [`gain_familiar`](./Enums.md#enum-gain_familiar) | Enum | Event Action: Adds a specific familiar to the party. | 1 |
| [`leave`](#leave) | Block | Event Node: Story branch or dialog option representing the 'Leave' action. | 1 |
| [`next_event_from_set`](./Enums.md#enum-next_event_from_set) | Enum | Event Action: Chains immediately into a randomly selected subsequent story event. | 1 |
| [`party_permanent_stats`](#party_permanent_stats) | Block | Event Reward: Permanently increases (or decreases) the core stats of all party members. | 1 |
| [`play_animation`](./Arrays.md#array-play_animation) | Array |  | 1 |
| [`rare`](#rare) | Block | Event Node: Story branch or dialog option representing the 'Rare' action. | 1 |
| [`requires_flag`](./Enums.md#enum-requires_flag) | Enum | Prerequisite: Must meet this condition. | 1 |
| [`self_status_next_fight`](#self_status_next_fight) | Block | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 1 |
| [`shop_now`](./Enums.md#enum-shop_now) | Enum |  | 1 |
| `party_heal` | Integer |  | 1 |
| [`self_damage`](./Arrays.md#array-self_damage) | Array | Recoil or self-inflicted damage/effects applied to the caster. | 0 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `rare`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 996

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `prompt` | String |  | 613 |
| `set_frame` | Integer |  | 180 |
| [`get_item_from_pool`](./Enums.md#enum-get_item_from_pool) | Enum | Event Action: Rewards the player with an item drawn from a specific loot pool. | 113 |
| [`permanent_stats`](#permanent_stats) | Block | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 84 |
| [`gain_disorder`](./Enums.md#enum-gain_disorder) | Enum |  | 65 |
| [`injury`](./Enums.md#enum-injury) | Enum |  | 51 |
| [`gain_disorder_from_pool`](./Enums.md#enum-gain_disorder_from_pool) | Enum |  | 45 |
| [`get_item`](./Enums.md#enum-get_item) | Enum |  | 41 |
| [`self_status_next_fight`](#self_status_next_fight) | Block | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 40 |
| `random_mutation` | Integer | Event Reward: Applies a completely random mutation to a character. | 40 |
| [`event_now_same_cat`](./Enums.md#enum-event_now_same_cat) | Enum |  | 30 |
| [`get_parasite`](./Enums.md#enum-get_parasite) | Enum |  | 30 |
| [`gain_familiar`](./Enums.md#enum-gain_familiar) | Enum | Event Action: Adds a specific familiar to the party. | 29 |
| [`conditional_reward`](#conditional_reward) | Block | Event Action: Provides a reward only if a specific condition is met. | 22 |
| [`set_adventure_token`](./Enums.md#enum-set_adventure_token) | Enum |  | 22 |
| [`get_parasite_from_pool`](./Enums.md#enum-get_parasite_from_pool) | Enum |  | 21 |
| [`spawn_unit_next_fight`](#spawn_unit_next_fight) | Block | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. | 20 |
| [`mutation`](#mutation) | Block | Event Node: Story branch or dialog option representing the 'Mutation' action. | 18 |
| `damage` | Integer | Event Node: Story branch or dialog option representing the 'Damage' action. | 15 |
| `next_event_bonus` | Integer |  | 14 |
| [`random_mutation_from_set`](#random_mutation_from_set) | Block | Event Reward: Applies a random mutation to a character from a specific pool. | 13 |
| [`party_status_next_fight`](#party_status_next_fight) | Block | Event Penalty/Reward: Applies a status effect to the entire party at the start of the next combat encounter. | 12 |
| `self_damage` | Integer | Recoil or self-inflicted damage/effects applied to the caster. | 12 |
| [`learn_passive`](./Enums.md#enum-learn_passive) | Enum |  | 10 |
| [`play_animation`](./Arrays.md#array-play_animation) | Array |  | 10 |
| `party_heal` | Integer |  | 10 |
| [`battle`](./Math_Equations.md) | Equation |  | 9 |
| [`increment_legacy_counter`](./Enums.md#enum-increment_legacy_counter) | Enum |  | 9 |
| `override_end_option_prompt` | String |  | 8 |
| `party_damage` | Integer |  | 8 |
| `party_random_mutation` | Integer |  | 8 |
| [`leave_party_temporarily`](#leave_party_temporarily) | Block | Event Action: Removes a character from the active team until the next hub area. | 7 |
| [`lose_item`](./Enums.md#enum-lose_item) | Enum |  | 7 |
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum |  | 7 |
| `ambush_next_basic_fights` | Integer |  | 7 |
| [`gain_coins`](./Arrays.md#array-gain_coins) | Array |  | 6 |
| [`shop_now`](./Enums.md#enum-shop_now) | Enum |  | 6 |
| `hide_appearance_changes` | Integer |  | 6 |
| [`decrement_legacy_counter`](./Enums.md#enum-decrement_legacy_counter) | Enum |  | 5 |
| `ally_ambush_next_fights` | Integer |  | 5 |
| [`add_weather`](./Enums.md#enum-add_weather) | Enum |  | 4 |
| [`learn_ability`](./Enums.md#enum-learn_ability) | Enum |  | 4 |
| `full_heal` | Integer |  | 4 |
| [`global_effect_next_fight`](#global_effect_next_fight) | Block | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 3 |
| [`kill`](./Enums.md#enum-kill) | Enum |  | 3 |
| [`level_up`](./Enums.md#enum-level_up) | Enum |  | 3 |
| [`lose_item_from_inventory`](./Enums.md#enum-lose_item_from_inventory) | Enum |  | 3 |
| [`make_old`](./Enums.md#enum-make_old) | Enum |  | 3 |
| [`next_event_from_set`](./Enums.md#enum-next_event_from_set) | Enum | Event Action: Chains immediately into a randomly selected subsequent story event. | 3 |
| `gain_cat_familiar` | Integer |  | 3 |
| `spawn_reflection_next_fight` | Integer | Event Penalty: Spawns dark clones/reflections of the party in the next combat encounter. | 3 |
| [`event_now`](./Enums.md#enum-event_now) | Enum |  | 2 |
| [`gain_food`](./Arrays.md#array-gain_food) | Array |  | 2 |
| [`lose_specific_item`](./Enums.md#enum-lose_specific_item) | Enum |  | 2 |
| [`party_permanent_stats_exclude_self`](#party_permanent_stats_exclude_self) | Block | Event Reward: Permanently modifies stats for all party members except the one who initiated the action. | 2 |
| [`upgrade_ability`](./Enums.md#enum-upgrade_ability) | Enum |  | 2 |
| [`upgrade_passive`](./Enums.md#enum-upgrade_passive) | Enum |  | 2 |
| `party_heal_disorder` | Integer |  | 2 |
| `party_heal_injury` | Integer |  | 2 |
| `set_age` | Integer |  | 2 |
| [`ambush`](./Math_Equations.md) | Equation |  | 1 |
| [`gain_immortal_familiar`](./Enums.md#enum-gain_immortal_familiar) | Enum |  | 1 |
| [`get_and_equip_item`](./Enums.md#enum-get_and_equip_item) | Enum |  | 1 |
| [`learn_ability_from_pool`](./Enums.md#enum-learn_ability_from_pool) | Enum |  | 1 |
| [`learn_passive_from_pool`](./Enums.md#enum-learn_passive_from_pool) | Enum |  | 1 |
| [`lose_all_equipped_items`](./Enums.md#enum-lose_all_equipped_items) | Enum |  | 1 |
| [`party_injury`](./Enums.md#enum-party_injury) | Enum |  | 1 |
| [`party_permanent_stats`](#party_permanent_stats) | Block | Event Reward: Permanently increases (or decreases) the core stats of all party members. | 1 |
| [`party_random_mutation_from_set`](#party_random_mutation_from_set) | Block | Event Reward: Applies a random mutation to the entire party from a specific pool. | 1 |
| [`play_result_animation`](./Enums.md#enum-play_result_animation) | Enum |  | 1 |
| [`scramble_abilities`](./Enums.md#enum-scramble_abilities) | Enum |  | 1 |
| [`scramble_basic_attack`](./Enums.md#enum-scramble_basic_attack) | Enum |  | 1 |
| [`trigger_adventure_unlock`](./Enums.md#enum-trigger_adventure_unlock) | Enum |  | 1 |
| `clear_result_animation` | Integer |  | 1 |
| `heal_disorder` | Integer |  | 1 |
| [`random_pool`](./Arrays.md#array-random_pool) | Array |  | 0 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `reward`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 760

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`common`](#common) | Block | Event Node: Story branch or dialog option representing the 'Common' action. | 634 |
| [`rare`](#rare) | Block | Event Node: Story branch or dialog option representing the 'Rare' action. | 624 |
| `prompt` | String |  | 73 |
| `set_frame` | Integer |  | 54 |
| [`clear_adventure_token`](./Enums.md#enum-clear_adventure_token) | Enum |  | 24 |
| [`get_item_from_pool`](./Enums.md#enum-get_item_from_pool) | Enum | Event Action: Rewards the player with an item drawn from a specific loot pool. | 13 |
| [`set_subject`](./Enums.md#enum-set_subject) | Enum |  | 10 |
| [`set_adventure_token`](./Enums.md#enum-set_adventure_token) | Enum |  | 9 |
| [`trigger_adventure_unlock`](./Enums.md#enum-trigger_adventure_unlock) | Enum |  | 5 |
| `next_event_bonus` | Integer |  | 5 |
| [`play_animation`](./Arrays.md#array-play_animation) | Array |  | 4 |
| [`cutscene_on_exit`](./Enums.md#enum-cutscene_on_exit) | Enum |  | 3 |
| [`gain_disorder_from_pool`](./Enums.md#enum-gain_disorder_from_pool) | Enum |  | 2 |
| [`injury`](./Enums.md#enum-injury) | Enum |  | 2 |
| [`spawn_unit_next_fight`](#spawn_unit_next_fight) | Block | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. | 2 |
| [`event_now`](./Enums.md#enum-event_now) | Enum |  | 1 |
| [`gain_coins`](./Arrays.md#array-gain_coins) | Array |  | 1 |
| [`get_item`](./Enums.md#enum-get_item) | Enum |  | 1 |
| [`get_parasite_from_pool`](./Enums.md#enum-get_parasite_from_pool) | Enum |  | 1 |
| [`level_up`](./Enums.md#enum-level_up) | Enum |  | 1 |
| [`random_chance`](#random_chance) | Block | Event Logic: Executes the nested outcome based on a percentage roll. | 1 |
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum |  | 1 |
| `ambush_next_basic_fights` | Integer |  | 1 |
| `weight` | Float | Probability weight for this outcome. | 1 |
| [`party_damage`](./Arrays.md#array-party_damage) | Array |  | 0 |
| [`random_pool`](./Arrays.md#array-random_pool) | Array |  | 0 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

