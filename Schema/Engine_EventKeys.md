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
| [`prompt`](./Enums.md#enum-prompt) | String | Examples: `"woah", "EVENT_TRASHBIN_REW3", "EVENT_ABEGGAR_REW2"` | 38 |  |
| `set_frame` | Integer | Examples: `4, 2, 5` | 36 |  |
| [`common`](./Enums.md#enum-common) | Enum | Event Object: Story branch or dialog option representing the 'Common' action. | 1067 |  |
| [`reward`](#reward) | Object | Event Object: Story branch or dialog option representing the 'Reward' action. | 5 |  |
| [`rare`](./Enums.md#enum-rare) | Enum | Event Object: Story branch or dialog option representing the 'Rare' action. | 673 |  |
| [`good`](#good) | Boolean | `false`, `true` | 8 |  |
| [`main`](#main) | Object | Event Object: The central hub or recurring menu of a story event. | 214 |  |
| [`get_item_from_pool`](./Enums.md#enum-get_item_from_pool) | Enum | Event Action: Rewards the player with an item drawn from a specific loot pool. | 11 |  |
| [`options`](./Arrays.md#array-options) | Array | Event Object: Lists the available clickable dialog choices for the current story node. | 210 |  |
| [`play_animation`](./Enums.md#enum-play_animation) | Enum | Examples: `resultVeryGood, resultBad` | 160 |  |
| [`self_status_next_fight`](#self_status_next_fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 1 |  |
| [`permanent_stats`](#permanent_stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 7 |  |
| [`injury`](./Enums.md#enum-injury) | Enum | Examples: `random` | 1 |  |
| [`gain_disorder`](./Enums.md#enum-gain_disorder) | Enum | Examples: `BorrowedTime, Brave, Dyslexia` | 85 |  |
| [`gain_disorder_from_pool`](./Enums.md#enum-gain_disorder_from_pool) | Enum | Examples: `Crazy_disorders` | 1 |  |
| [`random_pool`](./Arrays.md#array-random_pool) | Array | Examples: `[ { weight 90 prompt "EVENT_ABEGGAR_REW1" set_frame 3 ran..., [ { weight 85 p...` | 79 |  |
| [`conditional_reward`](#conditional_reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 1 |  |
| `random_mutation` | Integer | Event Reward: Applies a completely random mutation to a character. | 1 |  |
| [`increment_legacy_counter`](./Enums.md#enum-increment_legacy_counter) | Enum | Examples: `WorldEventLegacyToken_StartDigging, WorldEventLegacyCounter_CrackInTheWall, W...` | 67 |  |
| [`event_now_same_cat`](./Enums.md#enum-event_now_same_cat) | Enum | Examples: `BigToe, SpookieApparation, CatHole` | 63 |  |
| [`get_item`](./Enums.md#enum-get_item) | Enum | Examples: `BrokenWindow` | 61 |  |
| [`set_adventure_token`](./Enums.md#enum-set_adventure_token) | Enum | Examples: `AdventureToken_Mirage2, AdventureToken_StevenTryAgain3, HasPlayedMysteriousSt...` | 52 |  |
| `WorldEventLegacyCounter_Jack` | Variable |  | 50 |  |
| [`gain_familiar`](./Enums.md#enum-gain_familiar) | Enum | Event Action: Adds a specific familiar to the party. | 3 |  |
| [`clear_adventure_token`](./Enums.md#enum-clear_adventure_token) | Enum | Examples: `AdventureToken_BlueNeedle, AdventureToken_HasTakenNeedle, AdventureToken_RedN...` | 48 |  |
| [`gain_coins`](./Arrays.md#array-gain_coins) | Array | Examples: `[ 4 15 ], 5` | 47 |  |
| [`get_parasite`](./Enums.md#enum-get_parasite) | Enum | Examples: `FaceShards, BigToeCursed, MetalRod` | 41 |  |
| [`spawn_unit_next_fight`](#spawn_unit_next_fight) | Object | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. | 40 |  |
| [`get_parasite_from_pool`](./Enums.md#enum-get_parasite_from_pool) | Enum | Examples: `cursed_items, parasites` | 2 |  |
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum | Examples: `WorldEventLegacyToken_CryptOpened` | 36 |  |
| `resultHole` | Variable |  | 32 |  |
| `next_event_bonus` | Integer | Examples: `2` | 1 |  |
| [`gain_food`](./Arrays.md#array-gain_food) | Array | Examples: `[ 5 10 ]` | 28 |  |
| [`party_damage`](./Arrays.md#array-party_damage) | Array | Examples: `[ 5 10 ]` | 26 |  |
| `party_heal` | Integer | Examples: `10` | 1 |  |
| [`mutation`](#mutation) | Object | Event Object: Story branch or dialog option representing the 'Mutation' action. | 1 |  |
| [`party_status_next_fight`](#party_status_next_fight) | Object | Event Penalty/Reward: Applies a status effect to the entire party at the start of the next combat encounter. | 23 |  |
| [`setup`](#setup) | Object | Event Object: Pre-initialization logic executed before the event UI is drawn. | 23 |  |
| `cutscene` | String | Event Object: Triggers a narrative cutscene. | 1 |  |
| `override_end_option_prompt` | String | Examples: `"EVENT_MYSTERIOUSSTRANGER_END_AGAIN2", "EVENT_LOCKEDDOOR_PROMPT2", "EVENT_MYS...` | 21 |  |
| [`random_mutation_from_set`](#random_mutation_from_set) | Object | Event Reward: Applies a random mutation to a character from a specific pool. | 21 |  |
| `random` | Number | Examples: `4` | 1 |  |
| `AdventureToken_HasTakenNeedle` | Variable |  | 18 |  |
| [`complete_chapter`](./Enums.md#enum-complete_chapter) | Enum | `alley`, `boneyard`, `bunker`, `caves`, `core` | 90 |  |
| `ambush_next_basic_fights` | Integer | Examples: `1` | 17 |  |
| [`event_now`](./Enums.md#enum-event_now) | Enum | Examples: `MeatGolem` | 17 |  |
| `ally_ambush_next_fights` | Integer | Examples: `1` | 1 |  |
| `full_heal` | Integer | Examples: `1` | 16 |  |
| [`add_weather`](./Enums.md#enum-add_weather) | Enum | Examples: `TheShimmer, SolarFlare, GeomagneticStorm` | 5 |  |
| [`kill`](./Enums.md#enum-kill) | Enum | Examples: `cat` | 15 |  |
| `AdventureToken_BlueNeedle` | Variable |  | 14 |  |
| `AdventureToken_RedNeedle` | Variable |  | 14 |  |
| `cat` | Variable |  | 10 |  |
| [`lose_item`](./Enums.md#enum-lose_item) | Enum | Examples: `equipped, inventory` | 14 |  |
| [`battle`](./Math_Equations.md) | Equation | Examples: `{ ... }` | 2 |  |
| [`shop_now`](./Enums.md#enum-shop_now) | Enum | Examples: `TreasureHard, Event_SmallShop, Event_RareShop` | 13 |  |
| [`trigger_adventure_unlock`](./Enums.md#enum-trigger_adventure_unlock) | Enum | Examples: `end_of_time_unlock, meat_world_unlock` | 13 |  |
| `all_disorders` | Variable |  | 12 |  |
| [`begin_chapter`](./Enums.md#enum-begin_chapter) | Enum | Examples: `iceage.gon, dimensionx.gon, future.gon` | 12 |  |
| [`complete_item_quest`](./Enums.md#enum-complete_item_quest) | Enum | Examples: `BlackShard, JarOfRadiation, ScaldingOrb` | 18 |  |
| [`lose_specific_item`](./Enums.md#enum-lose_specific_item) | Enum | Examples: `SlagTight` | 12 |  |
| `CharmedMaggot` | Object |  | 11 |  |
| `auto` | Variable |  | 82 |  |
| `consumables` | Number | Examples: `60, 10` | 6 |  |
| [`global_effect_next_fight`](#global_effect_next_fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 10 |  |
| `HasPlayedMysteriousStranger` | Variable |  | 10 |  |
| [`learn_passive`](./Enums.md#enum-learn_passive) | Enum | Examples: `CobraStyle, PoisonTips, DeathProof` | 10 |  |
| [`set_subject`](./Enums.md#enum-set_subject) | Enum | Examples: `subject_frame, wall_of_flesh_noartery, throbbing_artery_noflesh` | 10 |  |
| [`level_up`](./Enums.md#enum-level_up) | Enum | Examples: `all, self` | 2 |  |
| `parasites` | Variable |  | 8 |  |
| `party_random_mutation` | Integer | Examples: `1` | 8 |  |
| `heal_disorder` | Integer | Examples: `2` | 7 |  |
| [`leave_party_temporarily`](#leave_party_temporarily) | Object | Event Action: Removes a character from the active team until the next hub area. | 7 |  |
| [`next_event_from_set`](./Enums.md#enum-next_event_from_set) | Enum | Event Action: Chains immediately into a randomly selected subsequent story event. | 7 |  |
| `spd` | Enum / Integer | `aux` | 424 |  |
| [`decrement_legacy_counter`](./Enums.md#enum-decrement_legacy_counter) | Enum | Examples: `WorldEventLegacyToken_StartDigging, WorldEventLegacyCounter_CrackInTheWall` | 6 |  |
| `hide_appearance_changes` | Integer | Examples: `1` | 6 |  |
| `QEVENT_OBELISK_IGNORE` | Variable |  | 6 |  |
| `QEVENT_OBELISK_REW1` | Variable |  | 6 |  |
| `QEVENT_OBELISK_REW2` | Variable |  | 6 |  |
| `QEVENT_OBELISK_REW3` | Variable |  | 6 |  |
| `QEVENT_OBELISK_REW4` | Variable |  | 6 |  |
| `Stinky` | Variable |  | 6 |  |
| `WorldEventLegacyCounter_CrackInTheWall` | Variable |  | 6 |  |
| `WorldEventLegacyToken_StartDigging` | Variable |  | 6 |  |
| `blood_altar_items` | Variable |  | 5 |  |
| `Bottles` | Object |  | 2 |  |
| `cha` | Enum / Integer | `+1`, `aux` | 468 |  |
| `current_chapter_common` | Mixed | `auto` | 12 |  |
| `current_chapter_rare` | Mixed | `auto` | 12 |  |
| [`cutscene_on_exit`](./Enums.md#enum-cutscene_on_exit) | Enum | Examples: `infinite_intro` | 5 |  |
| [`food`](./Arrays.md#array-food) | Array | Examples: `[ 4 8 ], [ 1 3 ], [ 4 7 ]` | 11 |  |
| `physical_disorders` | Variable |  | 5 |  |
| `SlagTight` | Object |  | 5 |  |
| [`bad`](#bad) | Object | Event Object: Story branch or dialog option representing the 'Bad' action. | 10 |  |
| `con` | Enum / Integer | `aux` | 416 |  |
| `diseases` | Variable |  | 4 |  |
| `fleshhead_items` | Variable |  | 4 |  |
| [`goto`](./Enums.md#enum-goto) | Enum | Examples: `end` | 4 |  |
| `heal_injury` | Integer | Examples: `1` | 4 |  |
| `inventory` | Variable |  | 4 |  |
| [`learn_ability`](./Enums.md#enum-learn_ability) | Enum | Examples: `BarfBall, FutureSight` | 4 |  |
| [`learn_ability_from_pool`](./Arrays.md#array-learn_ability_from_pool) | Array | Examples: `Necromancer` | 4 |  |
| `MysteriousStranger_HasLostFinger` | Variable |  | 4 |  |
| [`outcome`](#outcome) | Object | Event Object: Logic and text executed after selecting a specific dialog option. | 4 |  |
| `party_heal_disorder` | Integer | Examples: `2` | 4 |  |
| [`party_permanent_stats_exclude_self`](#party_permanent_stats_exclude_self) | Object | Event Reward: Permanently modifies stats for all party members except the one who initiated the action. | 4 |  |
| `pills` | Number | Examples: `7` | 2 |  |
| `QEVENT_THROBBINGARTERY_REW3` | Variable |  | 4 |  |
| [`random_pool_consider_luck`](./Arrays.md#array-random_pool_consider_luck) | Array | Examples: `[ { prompt "EVENT_TRACY_REW11" weight 1 get_item_from_poo..., [ { prompt "EVE...` | 4 |  |
| [`upgrade_ability`](./Enums.md#enum-upgrade_ability) | Enum | Examples: `random` | 4 |  |
| `WorldEventLegacyCounter_ToiletFlushes` | Variable |  | 4 |  |
| `bone_armor` | Variable |  | 3 |  |
| `bone_equipment` | Variable |  | 3 |  |
| `chapter_common` | Number | Examples: `1` | 7 |  |
| `chapter_specific_item` | Variable |  | 3 |  |
| `CryogenicTimeChamber_Full` | Object |  | 3 |  |
| `end_of_time_unlock` | Variable |  | 3 |  |
| `gain_cat_familiar` | Integer | Examples: `1` | 1 |  |
| [`learn_passive_from_pool`](./Arrays.md#array-learn_passive_from_pool) | Array | Examples: `AnyUnlocked` | 3 |  |
| [`lose_item_from_inventory`](./Enums.md#enum-lose_item_from_inventory) | Enum | Examples: `cat` | 3 |  |
| [`make_old`](./Enums.md#enum-make_old) | Enum | Examples: `self` | 3 |  |
| `max_options` | Integer | Examples: `3, 2` | 3 |  |
| `mental_disorders` | Variable |  | 3 |  |
| `QEVENT_OBELISK_QUES2` | Variable |  | 3 |  |
| `QEVENT_VOLCANO_REW2` | Variable |  | 3 |  |
| `QEVENT_VOLCANO_REW3` | Variable |  | 3 |  |
| `radiated` | Variable |  | 3 |  |
| `RestlessDead` | Variable |  | 3 |  |
| `resultVeryGood` | Variable |  | 3 |  |
| `Scatological` | Variable |  | 3 |  |
| `shuffle_options` | Boolean | Examples: `true` | 3 |  |
| `SlagMight` | Object |  | 3 |  |
| `spawn_reflection_next_fight` | Integer | Event Penalty: Spawns dark clones/reflections of the party in the next combat encounter. | 3 |  |
| [`transform_item`](./Arrays.md#array-transform_item) | Array | Examples: `[ CryogenicTimeChamber_Empty CryogenicTimeChamber_Full ], [ JarOfRadiation Ja...` | 3 |  |
| [`unlock_item_quest`](./Enums.md#enum-unlock_item_quest) | Enum | Examples: `CryogenicTimeChamber_Full, JarOfChaos, JarOfRadiatedBlood` | 3 |  |
| [`upgrade_passive`](./Enums.md#enum-upgrade_passive) | Enum | Examples: `random` | 3 |  |
| [`weight`](./Enums.md#enum-weight) | Float | Probability weight for this outcome. | 10 |  |
| `AdventureToken_YellowNeedle` | Variable |  | 2 |  |
| `all` | Variable |  | 2 |  |
| `Anxiety` | Variable |  | 2 |  |
| `Cancer` | Object |  | 2 |  |
| `CharmedPinky` | Object |  | 2 |  |
| `CharmedRaptorBaby` | Object |  | 2 |  |
| `clear_result_animation` | Integer | Examples: `1` | 2 |  |
| [`clear_surviving_kaiju`](./Enums.md#enum-clear_surviving_kaiju) | Enum | Examples: `pyrophina, zaratana` | 2 |  |
| `Depression` | Variable |  | 2 |  |
| `flesh_items` | Variable |  | 2 |  |
| [`gain_immortal_familiar`](./Enums.md#enum-gain_immortal_familiar) | Enum | Examples: `CharmedFleaSpecial` | 2 |  |
| [`get_and_equip_item`](./Enums.md#enum-get_and_equip_item) | Enum | Examples: `FlyLarva` | 2 |  |
| `glitched_items` | Variable |  | 2 |  |
| `HasHitPinata` | Variable |  | 2 |  |
| `HauntedNight` | Variable |  | 2 |  |
| `JarOfRadiatedBlood` | Object |  | 4 |  |
| `map_unlock_dimensionx` | Variable |  | 2 |  |
| [`party_gain_disorder_from_pool`](./Arrays.md#array-party_gain_disorder_from_pool) | Array | Examples: `[ Dwarfism ], [ Gigantism ]` | 2 |  |
| `party_heal_injury` | Integer | Examples: `99` | 2 |  |
| [`party_permanent_stats`](#party_permanent_stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of all party members. | 2 |  |
| [`party_random_mutation_from_set`](#party_random_mutation_from_set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 2 |  |
| `PawShards` | Object |  | 2 |  |
| `poop_items` | Variable |  | 2 |  |
| `PutridLeech` | Object |  | 2 |  |
| `PyrophinasCollar` | Object |  | 2 |  |
| `QEVENT_OBELISK_QUES1` | Variable |  | 2 |  |
| `QEVENT_THROBBINGARTERY_REW1` | Variable |  | 2 |  |
| `QEVENT_THROBBINGARTERY_REW2` | Variable |  | 2 |  |
| `QEVENT_VOLCANO_REW1` | Variable |  | 2 |  |
| `ReceiverAntenna` | Object |  | 2 |  |
| `resultBad` | Variable |  | 2 |  |
| `Rocks` | Object |  | 2 |  |
| [`scramble_abilities`](./Enums.md#enum-scramble_abilities) | Enum | Examples: `all` | 2 |  |
| `set_age` | Integer | Examples: `1` | 2 |  |
| `SignalAmplifier` | Object |  | 2 |  |
| `Snake` | Integer / Object | Applies or references the 'Snake' effect/state. | 2 |  |
| [`spin`](./Enums.md#enum-spin) | Enum | Examples: `again` | 4 |  |
| `ThrobbingGristle` | Object |  | 2 |  |
| `TransmitterAntenna` | Object |  | 2 |  |
| `ZaratanasCollar` | Object |  | 2 |  |
| `AdventureToken_HasRunFromDeath` | Variable |  | 1 |  |
| `AdventureToken_MysteriousCave_FamiliarVoice` | Variable |  | 1 |  |
| `AdventureToken_MysteriousJarRepeat` | Variable |  | 1 |  |
| `AdventureToken_StevenTryAgain` | Variable |  | 1 |  |
| `AdventureToken_StevenTryAgain2` | Variable |  | 1 |  |
| `AdventureToken_StevenTryAgain3` | Variable |  | 1 |  |
| `AdventureToken_TrippedOnBigToe` | Variable |  | 1 |  |
| `AdventureToken_UnmarkedGraveForced` | Variable |  | 1 |  |
| `Albinism` | Variable |  | 1 |  |
| `AlienOvergrowth` | Variable |  | 1 |  |
| [`alley`](./Enums.md#enum-alley) | Enum | `AREA_NAME_ALLEY`, `departed_first_real_adventure` | 18 |  |
| [`ambush`](./Math_Equations.md) | Equation | Examples: `"events/chupacabra.lvl"` | 1 |  |
| `AntennaQuest_Orb` | Variable |  | 1 |  |
| `AntennaQuest_Rift` | Variable |  | 1 |  |
| `AntennaQuest_Volcano` | Variable |  | 1 |  |
| `Beepis` | Object |  | 1 |  |
| `bleeding` | Variable |  | 1 |  |
| `bloody_items` | Variable |  | 1 |  |
| [`boneyard`](./Enums.md#enum-boneyard) | Enum | `AREA_NAME_BONEYARD`, `mapflag_BoneyardUnlocked` | 21 |  |
| `BrainDamage` | Variable |  | 1 |  |
| `BrainDead` | Variable |  | 1 |  |
| `Brave` | Variable |  | 1 |  |
| [`bunker`](./Enums.md#enum-bunker) | Enum | `AREA_NAME_BUNKER`, `mapflag_BunkerUnlocked` | 20 |  |
| `burned` | Variable |  | 1 |  |
| [`caves`](./Enums.md#enum-caves) | Enum | `AREA_NAME_CAVES`, `mapflag_CavesUnlocked` | 12 |  |
| [`chapter`](./Enums.md#enum-chapter) | Enum | `alley` | 6 |  |
| `chapter_rare` | Number | Examples: `1` | 10 |  |
| `CharmedTarBaby` | Object |  | 1 |  |
| `clone_self_to_party` | Integer | Examples: `1` | 1 |  |
| `copy_items_to_party` | Integer | Examples: `1` | 1 |  |
| `copy_party_items` | Integer | Examples: `1` | 1 |  |
| [`core`](./Enums.md#enum-core) | Enum | `AREA_NAME_CORE`, `mapflag_CoreUnlocked`, `mapflag_IceAgeUnlocked` | 20 |  |
| [`crater`](./Enums.md#enum-crater) | Enum | `AREA_NAME_CRATER`, `mapflag_CraterUnlocked` | 16 |  |
| `CryogenicTimeChamber_Empty` | Object |  | 2 |  |
| `Cunch` | Object |  | 1 |  |
| `cursed` | Boolean | `true` | 154 |  |
| `CursedStickman` | Object |  | 1 |  |
| `DeathsScythe` | Object |  | 1 |  |
| [`desert`](./Enums.md#enum-desert) | Enum | `AREA_NAME_DESERT`, `mapflag_DesertUnlocked` | 16 |  |
| `dex` | Enum / Integer | `aux` | 301 |  |
| [`dimensionx`](./Enums.md#enum-dimensionx) | Enum | `AREA_NAME_DIMENSIONX`, `mapflag_DimensionXUnlocked`, `mapflag_IceAgeUnlocked` | 27 |  |
| `dimensionx.gon` | Variable |  | 1 |  |
| `EnchantingPoop` | Object |  | 2 |  |
| `EVENT_USETHETOILET_AGAIN` | Variable |  | 1 |  |
| `FecalHood_Cursed` | Object |  | 1 |  |
| `FecalMask_Cursed` | Object |  | 1 |  |
| `Feebis` | Object |  | 1 |  |
| [`future`](./Enums.md#enum-future) | Enum | `AREA_NAME_FUTURE`, `mapflag_FutureUnlocked` | 16 |  |
| [`gain_clone_familiar`](#gain_clone_familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 1 |  |
| [`general_common`](./Enums.md#enum-general_common) | Enum | `auto` | 2 |  |
| [`general_rare`](./Enums.md#enum-general_rare) | Enum | `auto` | 2 |  |
| `GeomagneticStorm` | Variable |  | 1 |  |
| [`get_full_item_set_from_pool`](./Enums.md#enum-get_full_item_set_from_pool) | Enum | Examples: `common` | 1 |  |
| `Gigachad` | Variable |  | 1 |  |
| `godly_items` | Variable |  | 1 |  |
| `grass_items` | Variable |  | 1 |  |
| `GuillotinasHead` | Object |  | 2 |  |
| `hide_items` | Variable |  | 1 |  |
| `Host` | Object |  | 1 |  |
| [`iceage`](./Enums.md#enum-iceage) | Enum | `AREA_NAME_ICEAGE`, `mapflag_IceAgeUnlocked` | 14 |  |
| `iceage.gon` | Variable |  | 1 |  |
| `JarOfChaos` | Object |  | 4 |  |
| `JarOfRadiation` | Object |  | 6 |  |
| [`junkyard`](./Enums.md#enum-junkyard) | Enum | `AREA_NAME_JUNKYARD`, `mapflag_JunkyardUnlocked` | 12 |  |
| `junkyard_items` | Variable |  | 1 |  |
| [`jurassic`](./Enums.md#enum-jurassic) | Enum | `AREA_NAME_JURASSIC`, `endoftime`, `mapflag_JurassicUnlocked` | 14 |  |
| [`lab`](./Enums.md#enum-lab) | Enum | `AREA_NAME_LAB`, `mapflag_LabUnlocked` | 14 |  |
| `legacy_event_unlock_momsknife` | Variable |  | 1 |  |
| [`lose_all_equipped_items`](./Enums.md#enum-lose_all_equipped_items) | Enum | Examples: `cat` | 1 |  |
| `map_unlock_iceage` | Variable |  | 1 |  |
| `mapflag_ChaosAntennaAttached` | Variable |  | 1 |  |
| `mapflag_OrbAntennaAttached` | Variable |  | 1 |  |
| `mapflag_ThrobbingArteryDone` | Variable |  | 1 |  |
| `mapflag_VolcanoAntennaAttached` | Variable |  | 1 |  |
| `mapflag_WallOfFleshDone` | Variable |  | 1 |  |
| `meat_world_open` | Variable |  | 1 |  |
| [`meatworld`](./Enums.md#enum-meatworld) | Enum | `AREA_NAME_MEATWORLD`, `mapflag_MeatWorldUnlockedFull` | 24 |  |
| `MeatWorldQuest_Gristle` | Variable |  | 1 |  |
| `MeatWorldQuest_Leech` | Variable |  | 1 |  |
| `MeteorShowerUnlocked` | Variable |  | 1 |  |
| `MomsKnife` | Object |  | 2 |  |
| `monkey_paw_1finger` | Variable |  | 1 |  |
| `monkey_paw_2fingers` | Variable |  | 1 |  |
| `monkey_paw_3fingers` | Variable |  | 1 |  |
| `monkey_paw_4fingers` | Variable |  | 1 |  |
| [`moon`](./Enums.md#enum-moon) | Enum | `AREA_NAME_MOON`, `mapflag_IceAgeUnlocked`, `mapflag_MoonUnlocked` | 20 |  |
| `MysteriousTomb1` | Variable |  | 1 |  |
| `MysteriousTomb2` | Variable |  | 1 |  |
| `parasite` | Boolean | `true` | 102 |  |
| [`party_injury`](./Enums.md#enum-party_injury) | Enum | Examples: `random` | 1 |  |
| [`play_result_animation`](./Enums.md#enum-play_result_animation) | Enum | Examples: `resultVeryGood` | 1 |  |
| `PuncturedEye` | Variable |  | 1 |  |
| `QEVENT_BROKENTIMEMACHINE_QUES` | Variable |  | 1 |  |
| `QEVENT_BROKENTIMEMACHINE_REW2` | Variable |  | 1 |  |
| `QEVENT_BROKENTIMEMACHINE_REW3` | Variable |  | 1 |  |
| `QEVENT_BROKENTIMEMACHINE_REW4` | Variable |  | 1 |  |
| `QEVENT_BROKENTIMEMACHINE_REW5` | Variable |  | 1 |  |
| `QEVENT_DEADGOD_QUES` | Variable |  | 1 |  |
| `QEVENT_DEADGOD_REW1` | Variable |  | 1 |  |
| `QEVENT_DEADGOD_REW2` | Variable |  | 1 |  |
| `QEVENT_DEADGOD_REW3` | Variable |  | 1 |  |
| `QEVENT_DEADKING_QUES` | Variable |  | 1 |  |
| `QEVENT_DEADKING_REW1` | Variable |  | 1 |  |
| `QEVENT_DEADKING_REW2` | Variable |  | 1 |  |
| `QEVENT_DEADKING_REW3` | Variable |  | 1 |  |
| `QEVENT_DEADKING_REW4` | Variable |  | 1 |  |
| `QEVENT_DEADKING_REW5` | Variable |  | 1 |  |
| `QEVENT_DIMENSIONXPORTAL_ENTER_REW` | Variable |  | 1 |  |
| `QEVENT_DIMENSIONXPORTAL_IGNORE_ANSW` | Variable |  | 1 |  |
| `QEVENT_DIMENSIONXPORTAL_QUES` | Variable |  | 1 |  |
| `QEVENT_GLOWINGORB_QUES` | Variable |  | 1 |  |
| `QEVENT_GLOWINGORB_QUES2` | Variable |  | 1 |  |
| `QEVENT_GLOWINGORB_REW1` | Variable |  | 1 |  |
| `QEVENT_GLOWINGORB_REW2` | Variable |  | 1 |  |
| `QEVENT_GLOWINGORB_REW3` | Variable |  | 1 |  |
| `QEVENT_GLOWINGORB_REW4` | Variable |  | 1 |  |
| `QEVENT_GLOWINGORB_REW5` | Variable |  | 1 |  |
| `QEVENT_GLOWINGORB_REW7` | Variable |  | 1 |  |
| `QEVENT_MEATALTAR_QUES1` | Variable |  | 1 |  |
| `QEVENT_MEATALTAR_REW1` | Variable |  | 1 |  |
| `QEVENT_MEATALTAR_REW_IGNORE` | Variable |  | 1 |  |
| `QEVENT_OBELISK_CORE_REW_ZARA3` | Variable |  | 1 |  |
| `QEVENT_OBELISK_MOON_REW_PYRO3` | Variable |  | 1 |  |
| `QEVENT_OBELISK_QUES3` | Variable |  | 1 |  |
| `QEVENT_THEHEAD_QUES` | Variable |  | 1 |  |
| `QEVENT_THEHEAD_REW1` | Variable |  | 1 |  |
| `QEVENT_THEHEAD_REW2` | Variable |  | 1 |  |
| `QEVENT_THEHEAD_REW3` | Variable |  | 1 |  |
| `QEVENT_THEHEAD_REW5` | Variable |  | 1 |  |
| `QEVENT_THEHEAD_REW6` | Variable |  | 1 |  |
| `QEVENT_THROBBINGARTERY2_QUES` | Variable |  | 1 |  |
| `QEVENT_THROBBINGARTERY2_REW_IGNORE` | Variable |  | 1 |  |
| `QEVENT_THROBBINGARTERY_QUES1` | Variable |  | 1 |  |
| `QEVENT_THROBBINGARTERY_QUES2` | Variable |  | 1 |  |
| `QEVENT_THROBBINGARTERY_REW5` | Variable |  | 1 |  |
| `QEVENT_THROBBINGARTERY_REW_IGNORE` | Variable |  | 1 |  |
| `QEVENT_TIMEMACHINE_FUTURE_QUES` | Variable |  | 1 |  |
| `QEVENT_TIMEMACHINE_FUTURE_REW1` | Variable |  | 1 |  |
| `QEVENT_TIMEMACHINE_FUTURE_REW2` | Variable |  | 1 |  |
| `QEVENT_TIMEMACHINE_ICEAGE_QUES` | Variable |  | 1 |  |
| `QEVENT_TIMEMACHINE_ICEAGE_REW1` | Variable |  | 1 |  |
| `QEVENT_TIMEMACHINE_ICEAGE_REW2` | Variable |  | 1 |  |
| `QEVENT_TIMEMACHINE_JURASSIC_QUES` | Variable |  | 1 |  |
| `QEVENT_TIMEMACHINE_JURASSIC_REW1` | Variable |  | 1 |  |
| `QEVENT_TIMEMACHINE_JURASSIC_REW2` | Variable |  | 1 |  |
| `QEVENT_TIMEMACHINE_QUES` | Variable |  | 1 |  |
| `QEVENT_TIMEMACHINE_REW1` | Variable |  | 1 |  |
| `QEVENT_TIMEMACHINE_REW2` | Variable |  | 1 |  |
| `QEVENT_TIMEMACHINE_REW3` | Variable |  | 1 |  |
| `QEVENT_TIMEMACHINE_THEEND_QUES` | Variable |  | 1 |  |
| `QEVENT_TIMEMACHINE_THEEND_REW1` | Variable |  | 1 |  |
| `QEVENT_TIMEMACHINE_THEEND_REW2` | Variable |  | 1 |  |
| `QEVENT_VOLCANO_QUES` | Variable |  | 1 |  |
| `QEVENT_VOLCANO_QUES2` | Variable |  | 1 |  |
| `QEVENT_VOLCANO_REW4` | Variable |  | 1 |  |
| `QEVENT_VOLCANO_REW5` | Variable |  | 1 |  |
| `QEVENT_VOLCANO_REW7` | Variable |  | 1 |  |
| `QEVENT_WALLOFFLESH2_QUES` | Variable |  | 1 |  |
| `QEVENT_WALLOFFLESH2_REW_IGNORE` | Variable |  | 1 |  |
| `QEVENT_WALLOFFLESH_QUES1` | Variable |  | 1 |  |
| `QEVENT_WALLOFFLESH_QUES2` | Variable |  | 1 |  |
| `QEVENT_WALLOFFLESH_REW1` | Variable |  | 1 |  |
| `QEVENT_WALLOFFLESH_REW10` | Variable |  | 1 |  |
| `QEVENT_WALLOFFLESH_REW2` | Variable |  | 1 |  |
| `QEVENT_WALLOFFLESH_REW3` | Variable |  | 1 |  |
| `QEVENT_WALLOFFLESH_REW4` | Variable |  | 1 |  |
| `QEVENT_WALLOFFLESH_REW5` | Variable |  | 1 |  |
| `QEVENT_WALLOFFLESH_REW7` | Variable |  | 1 |  |
| `QEVENT_WALLOFFLESH_REW8` | Variable |  | 1 |  |
| `QEVENT_WALLOFFLESH_REW9` | Variable |  | 1 |  |
| `QEVENT_WALLOFFLESH_REW_IGNORE` | Variable |  | 1 |  |
| [`random_chance`](#random_chance) | Object | Event Logic: Executes the nested outcome based on a percentage roll. | 1 |  |
| `raptor_nest_eggs` | Variable |  | 1 |  |
| [`RaptorEgg`](./Enums.md#enum-raptoregg) | Object | Examples: `.1` | 2 |  |
| [`requires_flag`](./Enums.md#enum-requires_flag) | Enum | Prerequisite: Must meet this condition. | 5 |  |
| `resultConfused` | Variable |  | 1 |  |
| `resultVeryBad` | Variable |  | 1 |  |
| `rock_items` | Variable |  | 1 |  |
| [`scramble_basic_attack`](./Enums.md#enum-scramble_basic_attack) | Enum | Examples: `all` | 1 |  |
| [`scramble_passives`](./Enums.md#enum-scramble_passives) | Enum | Examples: `all` | 1 |  |
| [`select_item_from_pool_for_cutscene_only`](./Enums.md#enum-select_item_from_pool_for_cutscene_only) | Enum | Examples: `glitched_items` | 1 |  |
| `self_heal` | Integer | Examples: `10` | 1 |  |
| [`sewers`](./Enums.md#enum-sewers) | Enum | `AREA_NAME_SEWERS`, `mapflag_SewersUnlocked` | 16 |  |
| `SludgeHat` | Object |  | 1 |  |
| `SludgeMask` | Object |  | 1 |  |
| `Soulless` | Variable |  | 1 |  |
| `Steven_disorders` | Variable |  | 1 |  |
| `StrangeEggs` | Variable |  | 1 |  |
| `tech_items` | Variable |  | 1 |  |
| [`theend`](./Enums.md#enum-theend) | Enum | `AREA_NAME_THEEND`, `endoftime`, `mapflag_TheEndUnlocked` | 14 |  |
| `TheRift_UsedPyrophina` | Variable |  | 1 |  |
| `TheRift_UsedZaratana` | Variable |  | 1 |  |
| `TheShimmer` | Variable |  | 1 |  |
| `time_machine_quest_finalstep` | Variable |  | 1 |  |
| `time_machine_quest_trigger` | Variable |  | 1 |  |
| `Touched` | Variable |  | 1 |  |
| `trigger_butterfly_effect` | Integer | Examples: `1` | 1 |  |
| `WorldEventLegacyCounter_SealedCrypt` | Variable |  | 1 |  |
| `WorldEventLegacyToken_CryptOpened` | Variable |  | 1 |  |
| `WorldEventLegacyToken_HasRunFromDeath` | Variable |  | 1 |  |
| `WorldEventLegacyToken_MomsKnife` | Variable |  | 1 |  |
| `WorldEventLegacyToken_MonkeyPaw1` | Variable |  | 1 |  |
| `WorldEventLegacyToken_MonkeyPaw2` | Variable |  | 1 |  |
| `WorldEventLegacyToken_MonkeyPaw3` | Variable |  | 1 |  |
| `WorldEventLegacyToken_MonkeyPaw4` | Variable |  | 1 |  |
| `WorldEventLegacyToken_MonkeyPawGenes` | Variable |  | 1 |  |
| `WorldEventLegacyToken_MonkeyPawItems` | Variable |  | 1 |  |
| `WorldEventLegacyToken_MonkeyPawKnowledge` | Variable |  | 1 |  |
| `WorldEventLegacyToken_MonkeyPawStrength` | Variable |  | 1 |  |
| `WorldEventLegacyToken_StacyMutant` | Variable |  | 1 |  |
| `spawn_reflection_next_fight` | Number | Event Penalty: Spawns dark clones/reflections of the party in the next combat encounter. | 0 |  |
| `StatusDamagers` | Object | Event Trigger: Applies nested statuses to damagers. | 2 |  |
| `StatusEachTurnBegin` | Object | Event Trigger: Applies nested statuses to each turn begin. | 16 |  |
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
| [`prompt`](./Enums.md#enum-prompt) | String | Examples: `"woah", "EVENT_TRASHBIN_REW3", "EVENT_ABEGGAR_REW2"` | 38 |  |
| `set_frame` | Integer | Examples: `4, 2, 5` | 36 |  |
| [`permanent_stats`](#permanent_stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 7 |  |
| [`play_animation`](./Arrays.md#array-play_animation) | Array / Enum | Examples: `resultVeryGood, resultBad` | 5 |  |
| [`reward`](#reward) | Object | Event Object: Story branch or dialog option representing the 'Reward' action. | 5 |  |
| [`kill`](./Enums.md#enum-kill) | Enum | Examples: `cat` | 4 |  |
| [`event_now`](./Enums.md#enum-event_now) | Enum | Examples: `MeatGolem` | 3 |  |
| [`event_now_same_cat`](./Enums.md#enum-event_now_same_cat) | Enum | Examples: `BigToe, SpookieApparation, CatHole` | 3 |  |
| [`battle`](./Math_Equations.md) | String | Examples: `{ ... }` | 2 |  |
| [`get_parasite_from_pool`](./Enums.md#enum-get_parasite_from_pool) | Enum | Examples: `cursed_items, parasites` | 2 |  |
| [`conditional_reward`](#conditional_reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 1 |  |
| [`cutscene`](#cutscene) | Object | Event Object: Triggers a narrative cutscene. | 1 |  |
| [`gain_disorder_from_pool`](./Enums.md#enum-gain_disorder_from_pool) | Enum | Examples: `Crazy_disorders` | 1 |  |
| [`gain_immortal_familiar`](./Enums.md#enum-gain_immortal_familiar) | Enum | Examples: `CharmedFleaSpecial` | 1 |  |
| [`get_parasite`](./Enums.md#enum-get_parasite) | Enum | Examples: `FaceShards, BigToeCursed, MetalRod` | 1 |  |
| [`injury`](./Enums.md#enum-injury) | Enum | Examples: `random` | 1 |  |
| [`lose_item`](./Enums.md#enum-lose_item) | Enum | Examples: `equipped, inventory` | 1 |  |
| `next_event_bonus` | Integer | Examples: `2` | 1 |  |
| [`party_random_mutation_from_set`](#party_random_mutation_from_set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 1 |  |
| [`select_item_from_pool_for_cutscene_only`](./Enums.md#enum-select_item_from_pool_for_cutscene_only) | Enum | Examples: `glitched_items` | 1 |  |
| [`self_status_next_fight`](#self_status_next_fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 1 |  |
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum | Examples: `WorldEventLegacyToken_CryptOpened` | 1 |  |

</details>

---

#### `common`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1197

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prompt`](./Enums.md#enum-prompt) | String | Examples: `"woah", "EVENT_TRASHBIN_REW3", "EVENT_ABEGGAR_REW2"` | 38 |  |
| `damage` | Array / Equation |  | 2 | `[3 6]` (Array), `[5 10]` (Array), `8` (Equation), `5` (Equation) |
| `self_damage` | Boolean / Integer / Object |  | 436 | `[4 8]` (Array), `[5 10]` (Array), `50` (Number), `8` (Number) |
| `set_frame` | Integer | Examples: `4, 2, 5` | 36 |  |
| [`clear_adventure_token`](./Enums.md#enum-clear_adventure_token) | Enum | Examples: `AdventureToken_BlueNeedle, AdventureToken_HasTakenNeedle, AdventureToken_RedN...` | 24 |  |
| [`event_now_same_cat`](./Enums.md#enum-event_now_same_cat) | Enum | Examples: `BigToe, SpookieApparation, CatHole` | 21 |  |
| [`spawn_unit_next_fight`](#spawn_unit_next_fight) | Object | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. | 18 |  |
| [`get_item`](./Enums.md#enum-get_item) | Enum | Examples: `BrokenWindow` | 14 |  |
| [`play_animation`](./Arrays.md#array-play_animation) | Array / Enum | Examples: `resultVeryGood, resultBad` | 13 |  |
| [`gain_disorder`](./Enums.md#enum-gain_disorder) | Enum | Examples: `BorrowedTime, Brave, Dyslexia` | 12 |  |
| [`get_item_from_pool`](./Enums.md#enum-get_item_from_pool) | Array / Enum / Object | Event Action: Rewards the player with an item drawn from a specific loot pool. | 11 |  |
| `override_end_option_prompt` | String | Examples: `"EVENT_MYSTERIOUSSTRANGER_END_AGAIN2", "EVENT_LOCKEDDOOR_PROMPT2", "EVENT_MYS...` | 11 |  |
| [`party_status_next_fight`](#party_status_next_fight) | Object | Event Penalty/Reward: Applies a status effect to the entire party at the start of the next combat encounter. | 11 |  |
| `full_heal` | Integer | Examples: `1` | 10 |  |
| `ambush_next_basic_fights` | Integer | Examples: `1` | 9 |  |
| [`party_damage`](./Arrays.md#array-party_damage) | Array / Number | Examples: `[ 5 10 ]` | 9 |  |
| [`set_adventure_token`](./Enums.md#enum-set_adventure_token) | Enum | Examples: `AdventureToken_Mirage2, AdventureToken_StevenTryAgain3, HasPlayedMysteriousSt...` | 9 |  |
| [`random_mutation_from_set`](#random_mutation_from_set) | Number / Object | Event Reward: Applies a random mutation to a character from a specific pool. | 8 |  |
| [`get_parasite`](./Enums.md#enum-get_parasite) | Enum | Examples: `FaceShards, BigToeCursed, MetalRod` | 7 |  |
| [`permanent_stats`](#permanent_stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 7 |  |
| [`gain_coins`](./Arrays.md#array-gain_coins) | Array / Number | Examples: `[ 4 15 ], 5` | 6 |  |
| [`global_effect_next_fight`](#global_effect_next_fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 6 |  |
| [`increment_legacy_counter`](./Enums.md#enum-increment_legacy_counter) | Enum | Examples: `WorldEventLegacyToken_StartDigging, WorldEventLegacyCounter_CrackInTheWall, W...` | 6 |  |
| [`add_weather`](./Enums.md#enum-add_weather) | Enum | Examples: `TheShimmer, SolarFlare, GeomagneticStorm` | 5 |  |
| [`kill`](./Enums.md#enum-kill) | Enum | Examples: `cat` | 5 |  |
| [`lose_item`](./Enums.md#enum-lose_item) | Enum | Examples: `equipped, inventory` | 5 |  |
| [`shop_now`](./Enums.md#enum-shop_now) | Enum | Examples: `TreasureHard, Event_SmallShop, Event_RareShop` | 5 |  |
| [`spin`](./Enums.md#enum-spin) | Enum | Examples: `again` | 4 |  |
| [`gain_familiar`](./Enums.md#enum-gain_familiar) | Enum / Object | Event Action: Adds a specific familiar to the party. | 3 |  |
| [`gain_food`](./Arrays.md#array-gain_food) | Array / Number | Examples: `[ 5 10 ]` | 3 |  |
| [`event_now`](./Enums.md#enum-event_now) | Enum | Examples: `MeatGolem` | 2 |  |
| [`get_parasite_from_pool`](./Enums.md#enum-get_parasite_from_pool) | Array / Enum | Examples: `cursed_items, parasites` | 2 |  |
| [`lose_specific_item`](./Enums.md#enum-lose_specific_item) | Enum | Examples: `SlagTight` | 2 |  |
| [`next_event_from_set`](./Enums.md#enum-next_event_from_set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 2 |  |
| `party_heal_disorder` | Integer | Examples: `2` | 2 |  |
| [`party_permanent_stats_exclude_self`](#party_permanent_stats_exclude_self) | Object | Event Reward: Permanently modifies stats for all party members except the one who initiated the action. | 2 |  |
| `ally_ambush_next_fights` | Integer | Examples: `1` | 1 |  |
| `clear_result_animation` | Integer | Examples: `1` | 1 |  |
| [`conditional_reward`](#conditional_reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 1 |  |
| [`decrement_legacy_counter`](./Enums.md#enum-decrement_legacy_counter) | Enum | Examples: `WorldEventLegacyToken_StartDigging, WorldEventLegacyCounter_CrackInTheWall` | 1 |  |
| [`gain_disorder_from_pool`](./Enums.md#enum-gain_disorder_from_pool) | Array / Enum | Examples: `Crazy_disorders` | 1 |  |
| [`get_and_equip_item`](./Enums.md#enum-get_and_equip_item) | Enum | Examples: `FlyLarva` | 1 |  |
| `heal_disorder` | Integer | Examples: `2` | 1 |  |
| `heal_injury` | Integer | Examples: `1` | 1 |  |
| [`injury`](./Enums.md#enum-injury) | Enum | Examples: `random` | 1 |  |
| [`learn_ability_from_pool`](./Enums.md#enum-learn_ability_from_pool) | Enum | Examples: `Necromancer` | 1 |  |
| [`mutation`](#mutation) | Object | Event Object: Story branch or dialog option representing the 'Mutation' action. | 1 |  |
| `next_event_bonus` | Integer | Examples: `2` | 1 |  |
| `party_heal` | Integer | Examples: `10` | 1 |  |
| `random_mutation` | Integer | Event Reward: Applies a completely random mutation to a character. | 1 |  |
| `self_heal` | Integer | Examples: `10` | 1 |  |
| [`self_status_next_fight`](#self_status_next_fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 1 |  |
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum | Examples: `WorldEventLegacyToken_CryptOpened` | 1 |  |
| [`upgrade_ability`](./Enums.md#enum-upgrade_ability) | Enum | Examples: `random` | 1 |  |
| [`random_pool`](./Arrays.md#array-random_pool) | Array | Examples: `[ { weight 90 prompt "EVENT_ABEGGAR_REW1" set_frame 3 ran..., [ { weight 85 p...` | 0 |  |

</details>

---

#### `good`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 572

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`rare`](./Enums.md#enum-rare) | Enum | Event Object: Story branch or dialog option representing the 'Rare' action. | 673 |  |
| [`increment_legacy_counter`](./Enums.md#enum-increment_legacy_counter) | Enum | Examples: `WorldEventLegacyToken_StartDigging, WorldEventLegacyCounter_CrackInTheWall, W...` | 52 |  |
| [`prompt`](./Enums.md#enum-prompt) | String | Examples: `"woah", "EVENT_TRASHBIN_REW3", "EVENT_ABEGGAR_REW2"` | 38 |  |
| `set_frame` | Integer | Examples: `4, 2, 5` | 36 |  |
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum | Examples: `WorldEventLegacyToken_CryptOpened` | 26 |  |
| [`play_animation`](./Enums.md#enum-play_animation) | Array / Enum | Examples: `resultVeryGood, resultBad` | 20 |  |
| [`complete_item_quest`](./Enums.md#enum-complete_item_quest) | Enum | Examples: `BlackShard, JarOfRadiation, ScaldingOrb` | 18 |  |
| [`begin_chapter`](./Enums.md#enum-begin_chapter) | Enum | Examples: `iceage.gon, dimensionx.gon, future.gon` | 12 |  |
| [`set_adventure_token`](./Enums.md#enum-set_adventure_token) | Enum | Examples: `AdventureToken_Mirage2, AdventureToken_StevenTryAgain3, HasPlayedMysteriousSt...` | 12 |  |
| [`get_item_from_pool`](./Enums.md#enum-get_item_from_pool) | Enum | Event Action: Rewards the player with an item drawn from a specific loot pool. | 11 |  |
| [`event_now`](./Enums.md#enum-event_now) | Enum | Examples: `MeatGolem` | 9 |  |
| [`event_now_same_cat`](./Enums.md#enum-event_now_same_cat) | Enum | Examples: `BigToe, SpookieApparation, CatHole` | 9 |  |
| [`gain_disorder`](./Enums.md#enum-gain_disorder) | Enum | Examples: `BorrowedTime, Brave, Dyslexia` | 8 |  |
| [`lose_specific_item`](./Enums.md#enum-lose_specific_item) | Enum | Examples: `SlagTight` | 8 |  |
| [`trigger_adventure_unlock`](./Enums.md#enum-trigger_adventure_unlock) | Enum | Examples: `end_of_time_unlock, meat_world_unlock` | 7 |  |
| [`add_weather`](./Enums.md#enum-add_weather) | Enum | Examples: `TheShimmer, SolarFlare, GeomagneticStorm` | 5 |  |
| [`get_item`](./Enums.md#enum-get_item) | Enum | Examples: `BrokenWindow` | 5 |  |
| `heal_disorder` | Enum / Number | Examples: `2` | 5 |  |
| [`reward`](#reward) | Object | Event Object: Story branch or dialog option representing the 'Reward' action. | 5 |  |
| [`get_parasite`](./Enums.md#enum-get_parasite) | Enum | Examples: `FaceShards, BigToeCursed, MetalRod` | 3 |  |
| `heal_injury` | Integer | Examples: `1` | 3 |  |
| [`kill`](./Enums.md#enum-kill) | Enum | Examples: `cat` | 3 |  |
| [`unlock_item_quest`](./Enums.md#enum-unlock_item_quest) | Enum | Examples: `CryogenicTimeChamber_Full, JarOfChaos, JarOfRadiatedBlood` | 3 |  |
| [`clear_surviving_kaiju`](./Enums.md#enum-clear_surviving_kaiju) | Enum | Examples: `pyrophina, zaratana` | 2 |  |
| [`cutscene_on_exit`](./Enums.md#enum-cutscene_on_exit) | Enum / Object | Examples: `infinite_intro` | 2 |  |
| `full_heal` | Integer | Examples: `1` | 2 |  |
| [`level_up`](./Enums.md#enum-level_up) | Enum | Examples: `all, self` | 2 |  |
| `override_end_option_prompt` | String | Examples: `"EVENT_MYSTERIOUSSTRANGER_END_AGAIN2", "EVENT_LOCKEDDOOR_PROMPT2", "EVENT_MYS...` | 2 |  |
| `ally_ambush_next_fights` | Integer | Examples: `1` | 1 |  |
| `clone_self_to_party` | Integer | Examples: `1` | 1 |  |
| [`conditional_reward`](#conditional_reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 1 |  |
| `copy_items_to_party` | Integer | Examples: `1` | 1 |  |
| `copy_party_items` | Integer | Examples: `1` | 1 |  |
| `cutscene` | String | Event Object: Triggers a narrative cutscene. | 1 |  |
| [`gain_clone_familiar`](#gain_clone_familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 1 |  |
| [`gain_disorder_from_pool`](./Enums.md#enum-gain_disorder_from_pool) | Enum | Examples: `Crazy_disorders` | 1 |  |
| [`get_full_item_set_from_pool`](./Enums.md#enum-get_full_item_set_from_pool) | Enum | Examples: `common` | 1 |  |
| [`global_effect_next_fight`](#global_effect_next_fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 1 |  |
| [`injury`](./Enums.md#enum-injury) | Enum | Examples: `random` | 1 |  |
| [`learn_ability_from_pool`](./Arrays.md#array-learn_ability_from_pool) | Array / Enum | Examples: `Necromancer` | 1 |  |
| [`learn_passive_from_pool`](./Arrays.md#array-learn_passive_from_pool) | Array / Enum | Examples: `AnyUnlocked` | 1 |  |
| [`lose_item`](./Enums.md#enum-lose_item) | Enum | Examples: `equipped, inventory` | 1 |  |
| [`mutation`](#mutation) | Object | Event Object: Story branch or dialog option representing the 'Mutation' action. | 1 |  |
| `next_event_bonus` | Integer | Examples: `2` | 1 |  |
| [`next_event_from_set`](./Enums.md#enum-next_event_from_set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 1 |  |
| `random_mutation` | Number / Object | Event Reward: Applies a completely random mutation to a character. | 1 |  |
| [`scramble_abilities`](./Enums.md#enum-scramble_abilities) | Enum | Examples: `all` | 1 |  |
| [`scramble_passives`](./Enums.md#enum-scramble_passives) | Enum | Examples: `all` | 1 |  |
| [`shop_now`](./Enums.md#enum-shop_now) | Enum | Examples: `TreasureHard, Event_SmallShop, Event_RareShop` | 1 |  |
| `trigger_butterfly_effect` | Integer | Examples: `1` | 1 |  |
| [`upgrade_ability`](./Enums.md#enum-upgrade_ability) | Enum | Examples: `random` | 1 |  |
| [`upgrade_passive`](./Enums.md#enum-upgrade_passive) | Enum | Examples: `random` | 1 |  |
| [`gain_food`](./Arrays.md#array-gain_food) | Array | Examples: `[ 5 10 ]` | 0 |  |
| [`party_gain_disorder_from_pool`](./Arrays.md#array-party_gain_disorder_from_pool) | Array | Examples: `[ Dwarfism ], [ Gigantism ]` | 0 |  |
| [`random_pool`](./Arrays.md#array-random_pool) | Array | Examples: `[ { weight 90 prompt "EVENT_ABEGGAR_REW1" set_frame 3 ran..., [ { weight 85 p...` | 0 |  |
| [`random_pool_consider_luck`](./Arrays.md#array-random_pool_consider_luck) | Array | Examples: `[ { prompt "EVENT_TRACY_REW11" weight 1 get_item_from_poo..., [ { prompt "EVE...` | 0 |  |
| [`transform_item`](./Arrays.md#array-transform_item) | Array | Examples: `[ CryogenicTimeChamber_Empty CryogenicTimeChamber_Full ], [ JarOfRadiation Ja...` | 0 |  |

</details>

---

#### `main`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 215

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`rare`](./Enums.md#enum-rare) | Enum | Event Object: Story branch or dialog option representing the 'Rare' action. | 673 |  |
| [`options`](./Arrays.md#array-options) | Array | Event Object: Lists the available clickable dialog choices for the current story node. | 210 |  |
| [`prompt`](./Enums.md#enum-prompt) | String | Examples: `"woah", "EVENT_TRASHBIN_REW3", "EVENT_ABEGGAR_REW2"` | 38 |  |
| `set_frame` | Integer | Examples: `4, 2, 5` | 36 |  |
| [`setup`](#setup) | Object | Event Object: Pre-initialization logic executed before the event UI is drawn. | 23 |  |
| [`bad`](#bad) | Object | Event Object: Story branch or dialog option representing the 'Bad' action. | 10 |  |
| [`weight`](./Enums.md#enum-weight) | Float | Probability weight for this outcome. | 10 |  |
| [`add_weather`](./Enums.md#enum-add_weather) | Enum | Examples: `TheShimmer, SolarFlare, GeomagneticStorm` | 5 |  |
| [`requires_flag`](./Enums.md#enum-requires_flag) | Enum | Prerequisite: Must meet this condition. | 5 |  |
| [`goto`](./Enums.md#enum-goto) | Enum | Examples: `end` | 4 |  |
| [`outcome`](#outcome) | Object | Event Object: Logic and text executed after selecting a specific dialog option. | 4 |  |
| [`gain_familiar`](./Enums.md#enum-gain_familiar) | Enum | Event Action: Adds a specific familiar to the party. | 3 |  |
| `max_options` | Integer | Examples: `3, 2` | 3 |  |
| `shuffle_options` | Boolean | Examples: `true` | 3 |  |
| [`next_event_from_set`](./Enums.md#enum-next_event_from_set) | Enum | Event Action: Chains immediately into a randomly selected subsequent story event. | 1 |  |
| `party_heal` | Integer | Examples: `10` | 1 |  |
| [`party_permanent_stats`](#party_permanent_stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of all party members. | 1 |  |
| [`play_animation`](./Arrays.md#array-play_animation) | Array | Examples: `resultVeryGood, resultBad` | 1 |  |
| [`self_status_next_fight`](#self_status_next_fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 1 |  |
| [`shop_now`](./Enums.md#enum-shop_now) | Enum | Examples: `TreasureHard, Event_SmallShop, Event_RareShop` | 1 |  |

</details>

---

#### `rare`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 996

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`gain_disorder`](./Enums.md#enum-gain_disorder) | Enum | Examples: `BorrowedTime, Brave, Dyslexia` | 65 |  |
| [`get_item`](./Enums.md#enum-get_item) | Enum | Examples: `BrokenWindow` | 41 |  |
| [`prompt`](./Enums.md#enum-prompt) | String | Examples: `"woah", "EVENT_TRASHBIN_REW3", "EVENT_ABEGGAR_REW2"` | 38 |  |
| `damage` | Array / Equation |  | 2 | `[3 4]` (Array), `[2 5]` (Array), `5` (Equation), `7` (Equation) |
| `self_damage` | Boolean / Integer / Object |  | 436 | `[6 10]` (Array), `50` (Number), `10` (Number) |
| `set_frame` | Integer | Examples: `4, 2, 5` | 36 |  |
| [`event_now_same_cat`](./Enums.md#enum-event_now_same_cat) | Enum | Examples: `BigToe, SpookieApparation, CatHole` | 30 |  |
| [`get_parasite`](./Enums.md#enum-get_parasite) | Enum | Examples: `FaceShards, BigToeCursed, MetalRod` | 30 |  |
| [`set_adventure_token`](./Enums.md#enum-set_adventure_token) | Enum | Examples: `AdventureToken_Mirage2, AdventureToken_StevenTryAgain3, HasPlayedMysteriousSt...` | 22 |  |
| [`spawn_unit_next_fight`](#spawn_unit_next_fight) | Object | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. | 20 |  |
| [`random_mutation_from_set`](#random_mutation_from_set) | Number / Object | Event Reward: Applies a random mutation to a character from a specific pool. | 13 |  |
| [`party_status_next_fight`](#party_status_next_fight) | Object | Event Penalty/Reward: Applies a status effect to the entire party at the start of the next combat encounter. | 12 |  |
| [`get_item_from_pool`](./Enums.md#enum-get_item_from_pool) | Array / Enum / Object | Event Action: Rewards the player with an item drawn from a specific loot pool. | 11 |  |
| [`learn_passive`](./Enums.md#enum-learn_passive) | Enum | Examples: `CobraStyle, PoisonTips, DeathProof` | 10 |  |
| [`play_animation`](./Arrays.md#array-play_animation) | Array / Enum | Examples: `resultVeryGood, resultBad` | 10 |  |
| [`increment_legacy_counter`](./Enums.md#enum-increment_legacy_counter) | Enum | Examples: `WorldEventLegacyToken_StartDigging, WorldEventLegacyCounter_CrackInTheWall, W...` | 9 |  |
| `override_end_option_prompt` | String | Examples: `"EVENT_MYSTERIOUSSTRANGER_END_AGAIN2", "EVENT_LOCKEDDOOR_PROMPT2", "EVENT_MYS...` | 8 |  |
| [`party_damage`](./Arrays.md#array-party_damage) | Array / Number | Examples: `[ 5 10 ]` | 8 |  |
| `party_random_mutation` | Integer | Examples: `1` | 8 |  |
| `ambush_next_basic_fights` | String | Examples: `1` | 7 |  |
| [`leave_party_temporarily`](#leave_party_temporarily) | Object | Event Action: Removes a character from the active team until the next hub area. | 7 |  |
| [`lose_item`](./Enums.md#enum-lose_item) | Enum | Examples: `equipped, inventory` | 7 |  |
| [`permanent_stats`](#permanent_stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 7 |  |
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum | Examples: `WorldEventLegacyToken_CryptOpened` | 7 |  |
| [`gain_coins`](./Arrays.md#array-gain_coins) | Array / Number | Examples: `[ 4 15 ], 5` | 6 |  |
| `hide_appearance_changes` | Integer | Examples: `1` | 6 |  |
| [`shop_now`](./Enums.md#enum-shop_now) | Enum | Examples: `TreasureHard, Event_SmallShop, Event_RareShop` | 6 |  |
| [`add_weather`](./Enums.md#enum-add_weather) | Enum | Examples: `TheShimmer, SolarFlare, GeomagneticStorm` | 5 |  |
| [`decrement_legacy_counter`](./Enums.md#enum-decrement_legacy_counter) | Enum | Examples: `WorldEventLegacyToken_StartDigging, WorldEventLegacyCounter_CrackInTheWall` | 5 |  |
| `full_heal` | Integer | Examples: `1` | 4 |  |
| [`learn_ability`](./Enums.md#enum-learn_ability) | Enum | Examples: `BarfBall, FutureSight` | 4 |  |
| [`gain_familiar`](./Enums.md#enum-gain_familiar) | Enum | Event Action: Adds a specific familiar to the party. | 3 |  |
| [`global_effect_next_fight`](#global_effect_next_fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 3 |  |
| [`kill`](./Enums.md#enum-kill) | Enum | Examples: `cat` | 3 |  |
| [`lose_item_from_inventory`](./Enums.md#enum-lose_item_from_inventory) | Enum | Examples: `cat` | 3 |  |
| [`make_old`](./Enums.md#enum-make_old) | Enum | Examples: `self` | 3 |  |
| [`next_event_from_set`](./Enums.md#enum-next_event_from_set) | Enum / Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 3 |  |
| `spawn_reflection_next_fight` | Number / Object | Event Penalty: Spawns dark clones/reflections of the party in the next combat encounter. | 3 |  |
| [`battle`](./Math_Equations.md) | Enum / String | Examples: `{ ... }` | 2 |  |
| [`event_now`](./Enums.md#enum-event_now) | Enum | Examples: `MeatGolem` | 2 |  |
| [`gain_food`](./Arrays.md#array-gain_food) | Array / Number | Examples: `[ 5 10 ]` | 2 |  |
| [`get_parasite_from_pool`](./Enums.md#enum-get_parasite_from_pool) | Array / Enum | Examples: `cursed_items, parasites` | 2 |  |
| [`level_up`](./Enums.md#enum-level_up) | Enum | Examples: `all, self` | 2 |  |
| [`lose_specific_item`](./Enums.md#enum-lose_specific_item) | Enum | Examples: `SlagTight` | 2 |  |
| `party_heal_disorder` | Integer | Examples: `2` | 2 |  |
| `party_heal_injury` | Integer | Examples: `99` | 2 |  |
| [`party_permanent_stats_exclude_self`](#party_permanent_stats_exclude_self) | Object | Event Reward: Permanently modifies stats for all party members except the one who initiated the action. | 2 |  |
| `set_age` | Integer | Examples: `1` | 2 |  |
| [`upgrade_ability`](./Enums.md#enum-upgrade_ability) | Enum | Examples: `random` | 2 |  |
| [`upgrade_passive`](./Enums.md#enum-upgrade_passive) | Enum | Examples: `random` | 2 |  |
| `ally_ambush_next_fights` | Integer | Examples: `1` | 1 |  |
| [`ambush`](./Math_Equations.md) | Equation | Examples: `"events/chupacabra.lvl"` | 1 |  |
| `clear_result_animation` | Integer | Examples: `1` | 1 |  |
| [`conditional_reward`](#conditional_reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 1 |  |
| `gain_cat_familiar` | Integer | Examples: `1` | 1 |  |
| [`gain_disorder_from_pool`](./Enums.md#enum-gain_disorder_from_pool) | Array / Enum | Examples: `Crazy_disorders` | 1 |  |
| [`gain_immortal_familiar`](./Enums.md#enum-gain_immortal_familiar) | Enum | Examples: `CharmedFleaSpecial` | 1 |  |
| [`get_and_equip_item`](./Enums.md#enum-get_and_equip_item) | Enum | Examples: `FlyLarva` | 1 |  |
| `heal_disorder` | Integer | Examples: `2` | 1 |  |
| [`injury`](./Enums.md#enum-injury) | Enum | Examples: `random` | 1 |  |
| [`learn_ability_from_pool`](./Enums.md#enum-learn_ability_from_pool) | Enum | Examples: `Necromancer` | 1 |  |
| [`learn_passive_from_pool`](./Enums.md#enum-learn_passive_from_pool) | Enum | Examples: `AnyUnlocked` | 1 |  |
| [`lose_all_equipped_items`](./Enums.md#enum-lose_all_equipped_items) | Enum | Examples: `cat` | 1 |  |
| [`mutation`](#mutation) | Object | Event Object: Story branch or dialog option representing the 'Mutation' action. | 1 |  |
| `next_event_bonus` | Integer | Examples: `2` | 1 |  |
| `party_heal` | Integer | Examples: `10` | 1 |  |
| [`party_injury`](./Enums.md#enum-party_injury) | Enum | Examples: `random` | 1 |  |
| [`party_permanent_stats`](#party_permanent_stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of all party members. | 1 |  |
| [`party_random_mutation_from_set`](#party_random_mutation_from_set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 1 |  |
| [`play_result_animation`](./Enums.md#enum-play_result_animation) | Enum | Examples: `resultVeryGood` | 1 |  |
| `random_mutation` | Integer | Event Reward: Applies a completely random mutation to a character. | 1 |  |
| [`scramble_abilities`](./Enums.md#enum-scramble_abilities) | Enum | Examples: `all` | 1 |  |
| [`scramble_basic_attack`](./Enums.md#enum-scramble_basic_attack) | Enum | Examples: `all` | 1 |  |
| [`self_status_next_fight`](#self_status_next_fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 1 |  |
| [`trigger_adventure_unlock`](./Enums.md#enum-trigger_adventure_unlock) | Enum | Examples: `end_of_time_unlock, meat_world_unlock` | 1 |  |
| [`random_pool`](./Arrays.md#array-random_pool) | Array | Examples: `[ { weight 90 prompt "EVENT_ABEGGAR_REW1" set_frame 3 ran..., [ { weight 85 p...` | 0 |  |

</details>

---

#### `reward`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 760

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`common`](./Enums.md#enum-common) | Enum | Event Object: Story branch or dialog option representing the 'Common' action. | 1067 |  |
| [`rare`](./Enums.md#enum-rare) | Enum | Event Object: Story branch or dialog option representing the 'Rare' action. | 673 |  |
| [`prompt`](./Enums.md#enum-prompt) | String | Examples: `"woah", "EVENT_TRASHBIN_REW3", "EVENT_ABEGGAR_REW2"` | 38 |  |
| `set_frame` | Integer | Examples: `4, 2, 5` | 36 |  |
| [`clear_adventure_token`](./Enums.md#enum-clear_adventure_token) | Enum | Examples: `AdventureToken_BlueNeedle, AdventureToken_HasTakenNeedle, AdventureToken_RedN...` | 24 |  |
| [`get_item_from_pool`](./Enums.md#enum-get_item_from_pool) | Enum / Object | Event Action: Rewards the player with an item drawn from a specific loot pool. | 11 |  |
| [`set_subject`](./Enums.md#enum-set_subject) | Enum | Examples: `subject_frame, wall_of_flesh_noartery, throbbing_artery_noflesh` | 10 |  |
| [`weight`](./Enums.md#enum-weight) | Float | Probability weight for this outcome. | 10 |  |
| [`set_adventure_token`](./Enums.md#enum-set_adventure_token) | Enum | Examples: `AdventureToken_Mirage2, AdventureToken_StevenTryAgain3, HasPlayedMysteriousSt...` | 9 |  |
| [`trigger_adventure_unlock`](./Enums.md#enum-trigger_adventure_unlock) | Enum | Examples: `end_of_time_unlock, meat_world_unlock` | 5 |  |
| [`play_animation`](./Arrays.md#array-play_animation) | Enum | Examples: `resultVeryGood, resultBad` | 4 |  |
| [`cutscene_on_exit`](./Enums.md#enum-cutscene_on_exit) | Enum | Examples: `infinite_intro` | 3 |  |
| [`get_parasite_from_pool`](./Enums.md#enum-get_parasite_from_pool) | Enum | Examples: `cursed_items, parasites` | 2 |  |
| [`level_up`](./Enums.md#enum-level_up) | Enum | Examples: `all, self` | 2 |  |
| [`spawn_unit_next_fight`](#spawn_unit_next_fight) | Object | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. | 2 |  |
| `ambush_next_basic_fights` | Integer | Examples: `1` | 1 |  |
| [`event_now`](./Enums.md#enum-event_now) | Enum | Examples: `MeatGolem` | 1 |  |
| [`gain_coins`](./Arrays.md#array-gain_coins) | Array / Number | Examples: `[ 4 15 ], 5` | 1 |  |
| [`gain_disorder_from_pool`](./Enums.md#enum-gain_disorder_from_pool) | Enum | Examples: `Crazy_disorders` | 1 |  |
| [`get_item`](./Enums.md#enum-get_item) | Enum | Examples: `BrokenWindow` | 1 |  |
| [`injury`](./Enums.md#enum-injury) | Enum | Examples: `random` | 1 |  |
| `next_event_bonus` | Integer | Examples: `2` | 1 |  |
| [`random_chance`](#random_chance) | Object | Event Logic: Executes the nested outcome based on a percentage roll. | 1 |  |
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum | Examples: `WorldEventLegacyToken_CryptOpened` | 1 |  |
| [`party_damage`](./Arrays.md#array-party_damage) | Array | Examples: `[ 5 10 ]` | 0 |  |
| [`random_pool`](./Arrays.md#array-random_pool) | Array | Examples: `[ { weight 90 prompt "EVENT_ABEGGAR_REW1" set_frame 3 ran..., [ { weight 85 p...` | 0 |  |

</details>



---

## Auto-Discovered Objects


### Object: `Albinism`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | String | Undocumented. | 1 | `Disorder` |
| `desc` | String | Undocumented. | 1 | `"DISORDER_ALBINISM_DESC"` |
| `name` | String | Undocumented. | 1 | `"DISORDER_ALBINISM_NAME"` |
| `passives` | Object | Undocumented. | 1 |  |

</details>

### Object: `AlienOvergrowth`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Undocumented. | 1 | `"WEATHER_ALIENOVERGROWTH_DESC"` |
| `effects` | Object | Undocumented. | 1 |  |
| `name` | String | Undocumented. | 1 | `"WEATHER_ALIENOVERGROWTH_NAME"` |

</details>

### Object: `Anxiety`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | String | Undocumented. | 1 | `Disorder` |
| `desc` | String | Undocumented. | 1 | `"DISORDER_ANXIETY_DESC"` |
| `name` | String | Undocumented. | 1 | `"DISORDER_ANXIETY_NAME"` |
| `passives` | Object | Undocumented. | 1 |  |

</details>

### Object: `Beepis`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cursed` | Boolean | Undocumented. | 1 | `true` |
| `desc` | String | Undocumented. | 1 | `"ARMOR_BEEPIS_DESC"` |
| `frame` | Number | Undocumented. | 1 | `224` |
| `kind` | String | Undocumented. | 1 | `head` |
| `name` | String | Undocumented. | 1 | `"ARMOR_BEEPIS_NAME"` |
| `parasite` | Boolean | Undocumented. | 1 | `true` |
| `passives` | Object | Undocumented. | 1 |  |

</details>

### Object: `Bottles`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | String | Undocumented. | 1 | `wp_Bottles` |
| `desc` | String | Undocumented. | 1 | `"ITEM_BOTTLES_DESC"` |
| `durability` | Number | Undocumented. | 1 | `6` |
| `frame` | Number | Undocumented. | 1 | `17` |
| `kind` | String | Undocumented. | 1 | `weapon` |
| `name` | String | Undocumented. | 1 | `"ITEM_BOTTLES_NAME"` |
| `rarity` | String | Undocumented. | 1 | `common` |

</details>

### Object: `BrainDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | String | Undocumented. | 1 | `Disorder` |
| `desc` | String | Undocumented. | 1 | `"DISORDER_BRAINDAMAGE_DESC"` |
| `name` | String | Undocumented. | 1 | `"DISORDER_BRAINDAMAGE_NAME"` |
| `passives` | Object | Undocumented. | 1 |  |

</details>

### Object: `BrainDead`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | String | Undocumented. | 1 | `Disorder` |
| `desc` | String | Undocumented. | 1 | `"DISORDER_BRAINDEAD_DESC"` |
| `name` | String | Undocumented. | 1 | `"DISORDER_BRAINDEAD_NAME"` |
| `passives` | Object | Undocumented. | 1 |  |
| `stats` | Object | Undocumented. | 1 |  |

</details>

### Object: `Brave`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | String | Undocumented. | 1 | `Disorder` |
| `desc` | String | Undocumented. | 1 | `"DISORDER_BRAVE_DESC"` |
| `name` | String | Undocumented. | 1 | `"DISORDER_BRAVE_NAME"` |
| `passives` | Object | Undocumented. | 1 |  |

</details>

### Object: `Cancer`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | String | Undocumented. | 1 | `Disorder` |
| `desc` | String | Undocumented. | 2 | `"DISORDER_CANCER_DESC"`<br>`"ITEM_CANCER_DESC"` |
| `frame` | Number | Undocumented. | 1 | `152` |
| `kind` | String | Undocumented. | 1 | `trinket` |
| `name` | String | Undocumented. | 2 | `"DISORDER_CANCER_NAME"`<br>`"ITEM_CANCER_NAME"` |
| `passives` | Object | Undocumented. | 2 |  |
| `rarity` | String | Undocumented. | 1 | `rare` |
| `set` | String | Undocumented. | 1 | `Mother` |

</details>

### Object: `CharmedMaggot`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `graphics` | Object | Undocumented. | 1 |  |
| `properties` | Object | Undocumented. | 1 |  |
| `variant_of` | String | Undocumented. | 1 | `Maggot` |

</details>

### Object: `CharmedPinky`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `properties` | Object | Undocumented. | 1 |  |
| `variant_of` | String | Undocumented. | 1 | `Pinky` |

</details>

### Object: `CharmedRaptorBaby`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `properties` | Object | Undocumented. | 1 |  |
| `variant_of` | String | Undocumented. | 1 | `RaptorBaby` |

</details>

### Object: `CharmedTarBaby`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `properties` | Object | Undocumented. | 1 |  |
| `variant_of` | String | Undocumented. | 1 | `TarBaby` |

</details>

### Object: `CryogenicTimeChamber_Empty`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Undocumented. | 1 | `"ITEM_CRYOGENICTIMECHAMBER_EMP` |
| `frame` | Number | Undocumented. | 1 | `224` |
| `global_passives` | Object | Undocumented. | 1 |  |
| `hint_destination` | String | Undocumented. | 1 | `meatworld` |
| `hint_prerequisite_flag` | String | Undocumented. | 1 | `mapflag_MeatWorldUnlockedFull` |
| `indestructible` | Boolean | Undocumented. | 1 | `true` |
| `kind` | String | Undocumented. | 1 | `trinket` |
| `legacy_quest` | Boolean | Undocumented. | 1 | `true` |
| `name` | String | Undocumented. | 1 | `"ITEM_CRYOGENICTIMECHAMBER_EMP` |
| `passives` | Object | Undocumented. | 1 |  |
| `quest_item` | Boolean | Undocumented. | 1 | `true` |
| `rarity` | String | Undocumented. | 1 | `quest` |

</details>

### Object: `CryogenicTimeChamber_Full`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Undocumented. | 1 | `"ITEM_CRYOGENICTIMECHAMBER_FUL` |
| `frame` | Number | Undocumented. | 1 | `225` |
| `global_passives` | Object | Undocumented. | 1 |  |
| `hint_destination` | String | Undocumented. | 1 | `lab` |
| `indestructible` | Boolean | Undocumented. | 1 | `true` |
| `kind` | String | Undocumented. | 1 | `trinket` |
| `legacy_quest` | Boolean | Undocumented. | 1 | `true` |
| `name` | String | Undocumented. | 1 | `"ITEM_CRYOGENICTIMECHAMBER_FUL` |
| `passives` | Object | Undocumented. | 1 |  |
| `quest_item` | Boolean | Undocumented. | 1 | `true` |
| `rarity` | String | Undocumented. | 1 | `quest` |

</details>

### Object: `Cunch`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cursed` | Boolean | Undocumented. | 1 | `true` |
| `desc` | String | Undocumented. | 1 | `"ARMOR_CUNCH_DESC"` |
| `frame` | Number | Undocumented. | 1 | `199` |
| `kind` | String | Undocumented. | 1 | `neck` |
| `name` | String | Undocumented. | 1 | `"ARMOR_CUNCH_NAME"` |
| `parasite` | Boolean | Undocumented. | 1 | `true` |
| `passives` | Object | Undocumented. | 1 |  |

</details>

### Object: `CursedStickman`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cursed` | Boolean | Undocumented. | 1 | `true` |
| `desc` | String | Undocumented. | 1 | `"ITEM_CURSEDSTICKMAN_DESC"` |
| `frame` | Number | Undocumented. | 1 | `68` |
| `kind` | String | Undocumented. | 1 | `trinket` |
| `name` | String | Undocumented. | 1 | `"ITEM_CURSEDSTICKMAN_NAME"` |
| `passives` | Object | Undocumented. | 1 |  |
| `rarity` | String | Undocumented. | 1 | `rare` |
| `set` | Array | Undocumented. | 1 | `Wood Demonic` |

</details>

### Object: `DeathsScythe`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | String | Undocumented. | 1 | `wp_DeathsScythe` |
| `desc` | String | Undocumented. | 1 | `"ITEM_DEATHSSCYTHE_DESC"` |
| `frame` | Number | Undocumented. | 1 | `122` |
| `kind` | String | Undocumented. | 1 | `weapon` |
| `name` | String | Undocumented. | 1 | `"ITEM_DEATHSSCYTHE_NAME"` |
| `rarity` | String | Undocumented. | 1 | `rare` |

</details>

### Object: `Depression`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | String | Undocumented. | 1 | `Disorder` |
| `desc` | String | Undocumented. | 1 | `"DISORDER_DEPRESSION_DESC"` |
| `name` | String | Undocumented. | 1 | `"DISORDER_DEPRESSION_NAME"` |
| `passives` | Object | Undocumented. | 1 |  |
| `stats` | Object | Undocumented. | 1 |  |

</details>

### Object: `EnchantingPoop`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Undocumented. | 1 | `"ITEM_ENCHANTINGPOOP_DESC"` |
| `frame` | Number | Undocumented. | 1 | `159` |
| `kind` | String | Undocumented. | 1 | `trinket` |
| `name` | String | Undocumented. | 1 | `"ITEM_ENCHANTINGPOOP_NAME"` |
| `passives` | Object | Undocumented. | 1 |  |
| `set` | String | Undocumented. | 1 | `Fecal` |

</details>

### Object: `FecalHood_Cursed`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cursed` | Boolean | Undocumented. | 1 | `true` |
| `variant_of` | String | Undocumented. | 1 | `FecalHood` |

</details>

### Object: `FecalMask_Cursed`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cursed` | Boolean | Undocumented. | 1 | `true` |
| `variant_of` | String | Undocumented. | 1 | `FecalMask` |

</details>

### Object: `Feebis`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `attack` | String | Undocumented. | 1 | `BasicPoke` |
| `cursed` | Boolean | Undocumented. | 1 | `true` |
| `desc` | String | Undocumented. | 1 | `"ARMOR_FEEBIS_DESC"` |
| `frame` | Number | Undocumented. | 1 | `204` |
| `kind` | String | Undocumented. | 1 | `face` |
| `name` | String | Undocumented. | 1 | `"ARMOR_FEEBIS_NAME"` |
| `parasite` | Boolean | Undocumented. | 1 | `true` |
| `passives` | Object | Undocumented. | 1 |  |

</details>

### Object: `GeomagneticStorm`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Undocumented. | 1 | `"WEATHER_GEOMAGSTORM_DESC"` |
| `effects` | Object | Undocumented. | 1 |  |
| `name` | String | Undocumented. | 1 | `"WEATHER_GEOMAGSTORM_NAME"` |

</details>

### Object: `Gigachad`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | String | Undocumented. | 1 | `Disorder` |
| `desc` | String | Undocumented. | 1 | `"DISORDER_GIGACHAD_DESC"` |
| `name` | String | Undocumented. | 1 | `"DISORDER_GIGACHAD_NAME"` |
| `stats` | Object | Undocumented. | 1 |  |

</details>

### Object: `GuillotinasHead`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cursed` | Boolean | Undocumented. | 1 | `true` |
| `desc` | String | Undocumented. | 1 | `"ARMOR_GUILLOTINASHEAD_DESC"` |
| `frame` | Number | Undocumented. | 1 | `95` |
| `global_tags` | Array | Undocumented. | 1 | `upgrade_basic_combats_to_hard` |
| `hint_destination` | String | Undocumented. | 1 | `meatworld` |
| `hint_prerequisite_flag` | String | Undocumented. | 1 | `mapflag_MeatWorldUnlocked` |
| `indestructible` | Boolean | Undocumented. | 1 | `true` |
| `kind` | String | Undocumented. | 1 | `face` |
| `legacy_quest` | Boolean | Undocumented. | 1 | `true` |
| `name` | String | Undocumented. | 1 | `"ARMOR_GUILLOTINASHEAD_NAME"` |
| `passives` | Object | Undocumented. | 1 |  |
| `quest_item` | Boolean | Undocumented. | 1 | `true` |
| `rarity` | String | Undocumented. | 1 | `quest` |
| `set` | Array | Undocumented. | 1 | `Meat Guts` |

</details>

### Object: `HauntedNight`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Undocumented. | 1 | `"WEATHER_HAUNTED_DESC"` |
| `effects` | Object | Undocumented. | 1 |  |
| `name` | String | Undocumented. | 1 | `"WEATHER_HAUNTED_NAME"` |

</details>

### Object: `Host`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `abilities` | Object | Undocumented. | 1 |  |
| `ai` | Object | Undocumented. | 1 |  |
| `class` | String | Undocumented. | 1 | `Hunter` |
| `desc` | String | Undocumented. | 1 | `"PASSIVE_HOST_DESC"` |
| `graphics` | Object | Undocumented. | 1 |  |
| `name` | String | Undocumented. | 1 | `"PASSIVE_HOST_NAME"` |
| `passives` | Object | Undocumented. | 1 |  |
| `properties` | Object | Undocumented. | 1 |  |
| `stats` | Object | Undocumented. | 1 |  |

</details>

### Object: `JarOfChaos`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | String | Undocumented. | 1 | `cm_JarOfChaos` |
| `consumable` | Boolean | Undocumented. | 1 | `true` |
| `desc` | String | Undocumented. | 1 | `"ITEM_JAROFCHAOS_DESC"` |
| `dont_destroy_on_0` | Boolean | Undocumented. | 1 | `true` |
| `durability` | Number | Undocumented. | 1 | `1` |
| `failable` | Boolean | Undocumented. | 1 | `true` |
| `frame` | Number | Undocumented. | 1 | `239` |
| `indestructible` | Boolean | Undocumented. | 1 | `true` |
| `kind` | String | Undocumented. | 1 | `trinket` |
| `legacy_quest` | Boolean | Undocumented. | 1 | `true` |
| `name` | String | Undocumented. | 1 | `"ITEM_JAROFCHAOS_NAME"` |
| `passives` | Object | Undocumented. | 1 |  |
| `quest_item` | Boolean | Undocumented. | 1 | `true` |
| `rarity` | String | Undocumented. | 1 | `quest` |
| `set` | String | Undocumented. | 1 | `Radioactive` |

</details>

### Object: `JarOfRadiatedBlood`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Undocumented. | 1 | `"ITEM_JAROFRADIATEDBLOOD_DESC"` |
| `failable` | Boolean | Undocumented. | 1 | `true` |
| `frame` | Number | Undocumented. | 1 | `223` |
| `hint_destination` | String | Undocumented. | 1 | `dimensionx` |
| `indestructible` | Boolean | Undocumented. | 1 | `true` |
| `kind` | String | Undocumented. | 1 | `trinket` |
| `legacy_quest` | Boolean | Undocumented. | 1 | `true` |
| `name` | String | Undocumented. | 1 | `"ITEM_JAROFRADIATEDBLOOD_NAME"` |
| `passives` | Object | Undocumented. | 1 |  |
| `quest_item` | Boolean | Undocumented. | 1 | `true` |
| `rarity` | String | Undocumented. | 1 | `quest` |
| `set` | String | Undocumented. | 1 | `Radioactive` |

</details>

### Object: `JarOfRadiation`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Undocumented. | 1 | `"ITEM_JAROFRADIATION_DESC"` |
| `failable` | Boolean | Undocumented. | 1 | `true` |
| `frame` | Number | Undocumented. | 1 | `222` |
| `hint_destination` | String | Undocumented. | 1 | `meatworld` |
| `indestructible` | Boolean | Undocumented. | 1 | `true` |
| `kind` | String | Undocumented. | 1 | `trinket` |
| `legacy_quest` | Boolean | Undocumented. | 1 | `true` |
| `name` | String | Undocumented. | 1 | `"ITEM_JAROFRADIATION_NAME"` |
| `passives` | Object | Undocumented. | 1 |  |
| `quest_item` | Boolean | Undocumented. | 1 | `true` |
| `rarity` | String | Undocumented. | 1 | `quest` |
| `set` | String | Undocumented. | 1 | `Radioactive` |

</details>

### Object: `MomsKnife`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | String | Undocumented. | 1 | `wp_MomsKnife` |
| `desc` | String | Undocumented. | 1 | `"ITEM_MOMSKNIFE_DESC"` |
| `frame` | Number | Undocumented. | 1 | `126` |
| `kind` | String | Undocumented. | 1 | `weapon` |
| `name` | String | Undocumented. | 1 | `"ITEM_MOMSKNIFE_NAME"` |
| `rarity` | String | Undocumented. | 1 | `very_rare` |
| `set` | String | Undocumented. | 1 | `Mother` |

</details>

### Object: `MysteriousTomb1`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `intro` | Object | Undocumented. | 1 |  |
| `main` | Object | Undocumented. | 1 |  |

</details>

### Object: `MysteriousTomb2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `intro` | Object | Undocumented. | 1 |  |
| `main` | Object | Undocumented. | 1 |  |

</details>

### Object: `PawShards`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cursed` | Boolean | Undocumented. | 1 | `true` |
| `desc` | String | Undocumented. | 1 | `"ITEM_PAWSHARDS_DESC"` |
| `frame` | Number | Undocumented. | 1 | `23` |
| `kind` | String | Undocumented. | 1 | `weapon` |
| `name` | String | Undocumented. | 1 | `"ITEM_PAWSHARDS_NAME"` |
| `passives` | Object | Undocumented. | 1 |  |

</details>

### Object: `PuncturedEye`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `bonus_items` | Array | Undocumented. | 1 | `Eyeball` |
| `class` | String | Undocumented. | 1 | `Disorder` |
| `desc` | String | Undocumented. | 1 | `"DISORDER_PUNCTUREDEYE_DESC"` |
| `lock_item_slot` | Object | Undocumented. | 1 |  |
| `name` | String | Undocumented. | 1 | `"DISORDER_PUNCTUREDEYE_NAME"` |
| `passives` | Object | Undocumented. | 1 |  |

</details>

### Object: `PutridLeech`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cursed` | Boolean | Undocumented. | 1 | `true` |
| `desc` | String | Undocumented. | 1 | `"ARMOR_PUTRIDLEECH_DESC"` |
| `frame` | Number | Undocumented. | 1 | `97` |
| `hint_destination` | String | Undocumented. | 1 | `boneyard` |
| `indestructible` | Boolean | Undocumented. | 1 | `true` |
| `kind` | String | Undocumented. | 1 | `head` |
| `legacy_quest` | Boolean | Undocumented. | 1 | `true` |
| `name` | String | Undocumented. | 1 | `"ARMOR_PUTRIDLEECH_NAME"` |
| `parasite` | Boolean | Undocumented. | 1 | `true` |
| `passives` | Object | Undocumented. | 1 |  |
| `prevent_level_up` | Boolean | Undocumented. | 1 | `true` |
| `quest_item` | Boolean | Undocumented. | 1 | `true` |
| `rarity` | String | Undocumented. | 1 | `quest` |
| `set` | String | Undocumented. | 1 | `Leech` |

</details>

### Object: `PyrophinasCollar`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Undocumented. | 1 | `"ITEM_PYROPHINASCOLLAR_DESC"` |
| `frame` | Number | Undocumented. | 1 | `219` |
| `global_tags` | Array | Undocumented. | 1 | `pyrophina_following` |
| `hint_destination` | String | Undocumented. | 1 | `moon` |
| `hint_prerequisite_flag` | String | Undocumented. | 1 | `mapflag_BothObelisksUnlocked` |
| `indestructible` | Boolean | Undocumented. | 1 | `true` |
| `kind` | String | Undocumented. | 1 | `trinket` |
| `legacy_quest` | Boolean | Undocumented. | 1 | `true` |
| `name` | String | Undocumented. | 1 | `"ITEM_PYROPHINASCOLLAR_NAME"` |
| `passives` | Object | Undocumented. | 1 |  |
| `quest_item` | Boolean | Undocumented. | 1 | `true` |
| `rarity` | String | Undocumented. | 1 | `quest` |
| `set` | String | Undocumented. | 1 | `Used` |

</details>

### Object: `ReceiverAntenna`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Undocumented. | 1 | `"ARMOR_RECEIVERANTENNA_DESC"` |
| `frame` | Number | Undocumented. | 1 | `98` |
| `global_tags` | Array | Undocumented. | 1 | `all_normal_events_are_weather` |
| `hint_destination` | String | Undocumented. | 1 | `jurassic` |
| `indestructible` | Boolean | Undocumented. | 1 | `true` |
| `kind` | String | Undocumented. | 1 | `head` |
| `legacy_quest` | Boolean | Undocumented. | 1 | `true` |
| `name` | String | Undocumented. | 1 | `"ARMOR_RECEIVERANTENNA_NAME"` |
| `passives` | Object | Undocumented. | 1 |  |
| `quest_item` | Boolean | Undocumented. | 1 | `true` |
| `rarity` | String | Undocumented. | 1 | `quest` |
| `set` | Array | Undocumented. | 1 | `Bionic Cyborg` |
| `shield` | Number | Undocumented. | 1 | `8` |

</details>

### Object: `RestlessDead`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Undocumented. | 1 | `"WEATHER_RESTLESS_DESC"` |
| `effects` | Object | Undocumented. | 1 |  |
| `name` | String | Undocumented. | 1 | `"WEATHER_RESTLESS_NAME"` |

</details>

### Object: `Rocks`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | String | Undocumented. | 1 | `wp_Rocks` |
| `desc` | String | Undocumented. | 1 | `"ITEM_ROCKS_DESC"` |
| `durability` | Number | Undocumented. | 1 | `8` |
| `frame` | Number | Undocumented. | 1 | `55` |
| `kind` | String | Undocumented. | 1 | `weapon` |
| `name` | String | Undocumented. | 1 | `"ITEM_ROCKS_NAME"` |
| `rarity` | String | Undocumented. | 1 | `common` |
| `set` | String | Undocumented. | 1 | `Rock` |

</details>

### Object: `Scatological`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | String | Undocumented. | 1 | `Disorder` |
| `desc` | String | Undocumented. | 1 | `"DISORDER_SCATOLOGICAL_DESC"` |
| `name` | String | Undocumented. | 1 | `"DISORDER_SCATOLOGICAL_NAME"` |
| `passives` | Object | Undocumented. | 1 |  |

</details>

### Object: `SignalAmplifier`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | String | Undocumented. | 1 | `wp_SignalAmplifier` |
| `desc` | String | Undocumented. | 1 | `"ITEM_SIGNALAMPLIFIER_DESC"` |
| `frame` | Number | Undocumented. | 1 | `165` |
| `hint_destination` | String | Undocumented. | 1 | `dimensionx` |
| `hint_prerequisite_flag` | String | Undocumented. | 1 | `mapflag_DimensionXUnlocked` |
| `indestructible` | Boolean | Undocumented. | 1 | `true` |
| `kind` | String | Undocumented. | 1 | `weapon` |
| `legacy_quest` | Boolean | Undocumented. | 1 | `true` |
| `name` | String | Undocumented. | 1 | `"ITEM_SIGNALAMPLIFIER_NAME"` |
| `passives` | Object | Undocumented. | 1 |  |
| `quest_item` | Boolean | Undocumented. | 1 | `true` |
| `rarity` | String | Undocumented. | 1 | `quest` |
| `set` | Array | Undocumented. | 1 | `Bionic Cyborg` |

</details>

### Object: `SlagMight`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | String | Undocumented. | 1 | `wp_SlagMight` |
| `desc` | String | Undocumented. | 1 | `"ITEM_SLAGMIGHT_DESC"` |
| `frame` | Number | Undocumented. | 1 | `173` |
| `kind` | String | Undocumented. | 1 | `weapon` |
| `name` | String | Undocumented. | 1 | `"ITEM_SLAGMIGHT_NAME"` |
| `rarity` | String | Undocumented. | 1 | `very_rare` |
| `set` | String | Undocumented. | 1 | `Rock` |

</details>

### Object: `SlagTight`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cursed` | Boolean | Undocumented. | 1 | `true` |
| `desc` | String | Undocumented. | 1 | `"ITEM_SLAGTIGHT_DESC"` |
| `frame` | Number | Undocumented. | 1 | `170` |
| `int` | Number | Undocumented. | 1 | `-4` |
| `kind` | String | Undocumented. | 1 | `head` |
| `name` | String | Undocumented. | 1 | `"ITEM_SLAGTIGHT_NAME"` |
| `passives` | Object | Undocumented. | 1 |  |
| `shield` | Number | Undocumented. | 1 | `5` |

</details>

### Object: `SludgeHat`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cha` | Number | Undocumented. | 1 | `-1` |
| `cursed` | Boolean | Undocumented. | 1 | `true` |
| `desc` | String | Undocumented. | 1 | `"ARMOR_SLUDGEHAT_DESC"` |
| `frame` | Number | Undocumented. | 1 | `14` |
| `kind` | String | Undocumented. | 1 | `head` |
| `name` | String | Undocumented. | 1 | `"ARMOR_SLUDGEHAT_NAME"` |
| `set` | String | Undocumented. | 1 | `Sludge` |
| `shield` | Number | Undocumented. | 1 | `1` |

</details>

### Object: `SludgeMask`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cha` | Number | Undocumented. | 1 | `-1` |
| `cursed` | Boolean | Undocumented. | 1 | `true` |
| `desc` | String | Undocumented. | 1 | `"ARMOR_SLUDGEMASK_DESC"` |
| `frame` | Number | Undocumented. | 1 | `23` |
| `kind` | String | Undocumented. | 1 | `face` |
| `name` | String | Undocumented. | 1 | `"ARMOR_SLUDGEMASK_NAME"` |
| `set` | String | Undocumented. | 1 | `Sludge` |
| `shield` | Number | Undocumented. | 1 | `1` |

</details>

### Object: `Soulless`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | String | Undocumented. | 1 | `Disorder` |
| `desc` | String | Undocumented. | 1 | `"DISORDER_SOULLESS_DESC"` |
| `name` | String | Undocumented. | 1 | `"DISORDER_SOULLESS_NAME"` |
| `passives` | Object | Undocumented. | 1 |  |

</details>

### Object: `Stinky`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | String | Undocumented. | 1 | `Disorder` |
| `desc` | String | Undocumented. | 1 | `"DISORDER_STINKY_DESC"` |
| `name` | String | Undocumented. | 1 | `"DISORDER_STINKY_NAME"` |
| `passives` | Object | Undocumented. | 1 |  |

</details>

### Object: `StrangeEggs`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Undocumented. | 1 | `"WEATHER_STRANGEEGGS_DESC"` |
| `effects` | Object | Undocumented. | 1 |  |
| `name` | String | Undocumented. | 1 | `"WEATHER_STRANGEEGGS_NAME"` |

</details>

### Object: `TheShimmer`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Undocumented. | 1 | `"WEATHER_SHIMMER_DESC"` |
| `effects` | Object | Undocumented. | 1 |  |
| `name` | String | Undocumented. | 1 | `"WEATHER_SHIMMER_NAME"` |

</details>

### Object: `ThrobbingGristle`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | String | Undocumented. | 1 | `wp_ThrobbingGristle` |
| `desc` | String | Undocumented. | 1 | `"ITEM_THROBBINGGRISTLE_DESC"` |
| `frame` | Number | Undocumented. | 1 | `162` |
| `global_passives` | Object | Undocumented. | 1 |  |
| `hint_destination` | String | Undocumented. | 1 | `caves` |
| `indestructible` | Boolean | Undocumented. | 1 | `true` |
| `kind` | String | Undocumented. | 1 | `weapon` |
| `legacy_quest` | Boolean | Undocumented. | 1 | `true` |
| `name` | String | Undocumented. | 1 | `"ITEM_THROBBINGGRISTLE_NAME"` |
| `quest_item` | Boolean | Undocumented. | 1 | `true` |
| `rarity` | String | Undocumented. | 1 | `quest` |
| `set` | String | Undocumented. | 1 | `Meat` |

</details>

### Object: `Touched`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | String | Undocumented. | 1 | `Disorder` |
| `desc` | String | Undocumented. | 1 | `"DISORDER_TOUCHED_DESC"` |
| `name` | String | Undocumented. | 1 | `"DISORDER_TOUCHED_NAME"` |
| `passives` | Object | Undocumented. | 1 |  |
| `stats` | Object | Undocumented. | 1 |  |

</details>

### Object: `TransmitterAntenna`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Undocumented. | 1 | `"ARMOR_TRANSMITTERANTENNA_DESC` |
| `frame` | Number | Undocumented. | 1 | `99` |
| `hint_destination` | String | Undocumented. | 1 | `theend` |
| `indestructible` | Boolean | Undocumented. | 1 | `true` |
| `kind` | String | Undocumented. | 1 | `head` |
| `legacy_quest` | Boolean | Undocumented. | 1 | `true` |
| `name` | String | Undocumented. | 1 | `"ARMOR_TRANSMITTERANTENNA_NAME` |
| `passives` | Object | Undocumented. | 1 |  |
| `quest_item` | Boolean | Undocumented. | 1 | `true` |
| `rarity` | String | Undocumented. | 1 | `quest` |
| `set` | Array | Undocumented. | 1 | `Bionic Cyborg` |

</details>

### Object: `ZaratanasCollar`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Undocumented. | 1 | `"ITEM_ZARATANASCOLLAR_DESC"` |
| `frame` | Number | Undocumented. | 1 | `220` |
| `global_tags` | Array | Undocumented. | 1 | `zaratana_following` |
| `hint_destination` | String | Undocumented. | 1 | `core` |
| `hint_prerequisite_flag` | String | Undocumented. | 1 | `mapflag_BothObelisksUnlocked` |
| `indestructible` | Boolean | Undocumented. | 1 | `true` |
| `kind` | String | Undocumented. | 1 | `trinket` |
| `legacy_quest` | Boolean | Undocumented. | 1 | `true` |
| `name` | String | Undocumented. | 1 | `"ITEM_ZARATANASCOLLAR_NAME"` |
| `passives` | Object | Undocumented. | 1 |  |
| `quest_item` | Boolean | Undocumented. | 1 | `true` |
| `rarity` | String | Undocumented. | 1 | `quest` |
| `set` | String | Undocumented. | 1 | `Used` |

</details>

### Object: `bleeding`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `deathsound` | String | Undocumented. | 1 | `Injury_Bleed` |
| `id` | Number | Undocumented. | 1 | `8` |
| `stats` | Object | Undocumented. | 1 |  |
| `text` | String | Undocumented. | 1 | `"INJURY_NAME_EXSANGUINATED"` |

</details>

### Object: `burned`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `deathsound` | String | Undocumented. | 1 | `Injury_Burn` |
| `id` | Number | Undocumented. | 1 | `7` |
| `scars` | Object | Undocumented. | 1 |  |
| `stats` | Object | Undocumented. | 1 |  |
| `text` | String | Undocumented. | 1 | `"INJURY_NAME_IMMOLATED"` |

</details>

### Object: `chapter_specific_item`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `current_chapter_common` | Number | Undocumented. | 1 | `55` |
| `current_chapter_rare` | Number | Undocumented. | 1 | `10` |
| `current_chapter_uncommon` | Number | Undocumented. | 1 | `35` |
| `current_chapter_very_rare` | Number | Undocumented. | 1 | `1` |

</details>

### Object: `end_of_time_unlock`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `set_mapgen_flag` | String | Undocumented. | 1 | `EndOfTimeUnlocked` |

</details>

### Object: `legacy_event_unlock_momsknife`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `popup` | Object | Undocumented. | 1 |  |
| `unlock_item` | String | Undocumented. | 1 | `MomsKnife` |

</details>

### Object: `map_unlock_dimensionx`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `set_mapgen_flag` | String | Undocumented. | 1 | `DimensionXUnlocked` |

</details>

### Object: `map_unlock_iceage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `popup` | Object | Undocumented. | 1 |  |
| `set_mapgen_flag` | String | Undocumented. | 1 | `IceAgeUnlocked` |

</details>

### Object: `meat_world_open`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `set_mapgen_flag` | String | Undocumented. | 1 | `MeatWorldUnlockedFull` |

</details>

### Object: `radiated`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `deathsound` | String | Undocumented. | 1 | `Injury_Burn` |
| `id` | Number | Undocumented. | 1 | `11` |
| `scars` | Object | Undocumented. | 1 |  |
| `stats` | Object | Undocumented. | 1 |  |
| `text` | String | Undocumented. | 1 | `"INJURY_NAME_RADIATED"` |

</details>

### Object: `time_machine_quest_finalstep`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `trigger_npc_sequence` | String | Undocumented. | 1 | `beanies_timemachine_2` |

</details>

### Object: `time_machine_quest_trigger`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `trigger_npc_sequence` | String | Undocumented. | 1 | `beanies_timemachine_intro` |

</details>
