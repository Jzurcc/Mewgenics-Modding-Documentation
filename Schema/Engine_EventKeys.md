# Mewgenics Mod Developer Documentation: Engine: Event Keys

## Engine: Event Keys

This document defines the schema shared by all Event Node blocks (`good`, `bad`, `main`, `reward`, `common`, `rare`). Each key in these blocks defines what happens as part of that event outcome.

> **Referenced by:** [`reward` (Events_and_Encounters)](./Events_and_Encounters.md#context-reward), [`common` (Events_and_Encounters)](./Events_and_Encounters.md#context-common), [`rare` (Events_and_Encounters)](./Events_and_Encounters.md#context-rare), [`good` (Events_and_Encounters)](./Events_and_Encounters.md#context-good), [`bad` (Events_and_Encounters)](./Events_and_Encounters.md#context-bad), [`main` (Events_and_Encounters)](./Events_and_Encounters.md#context-main), [`reward` (Miscellaneous)](./Miscellaneous.md#context-reward), [`common` (Miscellaneous)](./Miscellaneous.md#context-common), [`rare` (Miscellaneous)](./Miscellaneous.md#context-rare)

### Valid Property Keys

<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prompt`](./Enums.md#enum-prompt) | String | Examples: `"woah", "EVENT_TRASHBIN_REW3", "EVENT_ABEGGAR_REW2"` | 1730 |
| `set_frame` | Integer | Examples: `4, 2, 5` | 897 |
| [`common`](./Enums.md#enum-common) | Object | Event Object: Story branch or dialog option representing the 'Common' action. | 634 |
| [`reward`](#reward) | Object | Event Object: Story branch or dialog option representing the 'Reward' action. | 633 |
| [`rare`](./Enums.md#enum-rare) | Object | Event Object: Story branch or dialog option representing the 'Rare' action. | 629 |
| [`good`](#good) | Object | `false`, `true` | 550 |
| [`main`](#main) | Object | Event Object: The central hub or recurring menu of a story event. | 215 |
| [`get_item_from_pool`](./Enums.md#enum-get_item_from_pool) | Enum | Event Action: Rewards the player with an item drawn from a specific loot pool. | 214 |
| [`options`](./Arrays.md#array-options) | Object | Event Object: Lists the available clickable dialog choices for the current story node. | 210 |
| [`play_animation`](./Enums.md#enum-play_animation) | Enum | Examples: `resultVeryGood, resultBad` | 160 |
| [`self_status_next_fight`](#self_status_next_fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 138 |
| [`permanent_stats`](#permanent_stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 126 |
| [`injury`](./Enums.md#enum-injury) | Enum | Examples: `random` | 92 |
| [`gain_disorder`](./Enums.md#enum-gain_disorder) | Enum | Examples: `BorrowedTime, Brave, Dyslexia` | 85 |
| [`gain_disorder_from_pool`](./Enums.md#enum-gain_disorder_from_pool) | Enum | Examples: `Crazy_disorders` | 83 |
| [`random_pool`](./Arrays.md#array-random_pool) | Array | Examples: `[ { weight 90 prompt "EVENT_ABEGGAR_REW1" set_frame 3 ran..., [ { weight 85 p...` | 79 |
| [`conditional_reward`](#conditional_reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 78 |
| `random_mutation` | Integer | Event Reward: Applies a completely random mutation to a character. | 77 |
| [`increment_legacy_counter`](./Enums.md#enum-increment_legacy_counter) | Enum | Examples: `WorldEventLegacyToken_StartDigging, WorldEventLegacyCounter_CrackInTheWall, W...` | 67 |
| [`event_now_same_cat`](./Enums.md#enum-event_now_same_cat) | Enum | Examples: `BigToe, SpookieApparation, CatHole` | 63 |
| [`get_item`](./Enums.md#enum-get_item) | Enum | Examples: `BrokenWindow` | 61 |
| [`set_adventure_token`](./Enums.md#enum-set_adventure_token) | Enum | Examples: `AdventureToken_Mirage2, AdventureToken_StevenTryAgain3, HasPlayedMysteriousSt...` | 52 |
| `WorldEventLegacyCounter_Jack` | Variable |  | 50 |
| [`gain_familiar`](./Enums.md#enum-gain_familiar) | Enum | Event Action: Adds a specific familiar to the party. | 49 |
| [`clear_adventure_token`](./Enums.md#enum-clear_adventure_token) | Enum | Examples: `AdventureToken_BlueNeedle, AdventureToken_HasTakenNeedle, AdventureToken_RedN...` | 48 |
| [`gain_coins`](./Arrays.md#array-gain_coins) | Array | Examples: `[ 4 15 ], 5` | 47 |
| [`get_parasite`](./Enums.md#enum-get_parasite) | Enum | Examples: `FaceShards, BigToeCursed, MetalRod` | 41 |
| [`spawn_unit_next_fight`](#spawn_unit_next_fight) | Object | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. | 40 |
| [`get_parasite_from_pool`](./Enums.md#enum-get_parasite_from_pool) | Enum | Examples: `cursed_items, parasites` | 39 |
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum | Examples: `WorldEventLegacyToken_CryptOpened` | 36 |
| `resultHole` | Variable |  | 32 |
| `next_event_bonus` | Integer | Examples: `2` | 29 |
| [`gain_food`](./Arrays.md#array-gain_food) | Array | Examples: `[ 5 10 ]` | 28 |
| [`party_damage`](./Arrays.md#array-party_damage) | Array | Examples: `[ 5 10 ]` | 26 |
| `party_heal` | Integer | Examples: `10` | 26 |
| [`mutation`](#mutation) | Object | Event Object: Story branch or dialog option representing the 'Mutation' action. | 23 |
| [`party_status_next_fight`](#party_status_next_fight) | Object | Event Penalty/Reward: Applies a status effect to the entire party at the start of the next combat encounter. | 23 |
| [`setup`](#setup) | Object | Event Object: Pre-initialization logic executed before the event UI is drawn. | 23 |
| `cutscene` | String | Event Object: Triggers a narrative cutscene. | 22 |
| `override_end_option_prompt` | String | Examples: `"EVENT_MYSTERIOUSSTRANGER_END_AGAIN2", "EVENT_LOCKEDDOOR_PROMPT2", "EVENT_MYS...` | 21 |
| [`random_mutation_from_set`](#random_mutation_from_set) | Object | Event Reward: Applies a random mutation to a character from a specific pool. | 21 |
| `random` | Number | Examples: `4` | 19 |
| `AdventureToken_HasTakenNeedle` | Variable |  | 18 |
| [`complete_chapter`](./Enums.md#enum-complete_chapter) | Enum | `alley`, `boneyard`, `bunker`, `caves`, `core` | 18 |
| `ambush_next_basic_fights` | Integer | Examples: `1` | 17 |
| [`event_now`](./Enums.md#enum-event_now) | Enum | Examples: `MeatGolem` | 17 |
| `ally_ambush_next_fights` | Integer | Examples: `1` | 16 |
| `full_heal` | Integer | Examples: `1` | 16 |
| [`add_weather`](./Enums.md#enum-add_weather) | Enum | Examples: `TheShimmer, SolarFlare, GeomagneticStorm` | 15 |
| [`kill`](./Enums.md#enum-kill) | Enum | Examples: `cat` | 15 |
| `AdventureToken_BlueNeedle` | Variable |  | 14 |
| `AdventureToken_RedNeedle` | Variable |  | 14 |
| `cat` | Variable |  | 14 |
| [`lose_item`](./Enums.md#enum-lose_item) | Enum | Examples: `equipped, inventory` | 14 |
| [`battle`](./Math_Equations.md) | Equation | Examples: `{ ... }` | 13 |
| [`shop_now`](./Enums.md#enum-shop_now) | Enum | Examples: `TreasureHard, Event_SmallShop, Event_RareShop` | 13 |
| [`trigger_adventure_unlock`](./Enums.md#enum-trigger_adventure_unlock) | Enum | Examples: `end_of_time_unlock, meat_world_unlock` | 13 |
| `all_disorders` | Variable |  | 12 |
| [`begin_chapter`](./Enums.md#enum-begin_chapter) | Enum | Examples: `iceage.gon, dimensionx.gon, future.gon` | 12 |
| [`complete_item_quest`](./Enums.md#enum-complete_item_quest) | Enum | Examples: `BlackShard, JarOfRadiation, ScaldingOrb` | 12 |
| [`lose_specific_item`](./Enums.md#enum-lose_specific_item) | Enum | Examples: `SlagTight` | 12 |
| `CharmedMaggot` | Variable |  | 11 |
| `auto` | Variable |  | 10 |
| `consumables` | Number | Examples: `60, 10` | 10 |
| [`global_effect_next_fight`](#global_effect_next_fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 10 |
| `HasPlayedMysteriousStranger` | Variable |  | 10 |
| [`learn_passive`](./Enums.md#enum-learn_passive) | Enum | Examples: `CobraStyle, PoisonTips, DeathProof` | 10 |
| [`set_subject`](./Enums.md#enum-set_subject) | Enum | Examples: `subject_frame, wall_of_flesh_noartery, throbbing_artery_noflesh` | 10 |
| [`level_up`](./Enums.md#enum-level_up) | Enum | Examples: `all, self` | 8 |
| `parasites` | Variable |  | 8 |
| `party_random_mutation` | Integer | Examples: `1` | 8 |
| `heal_disorder` | Integer | Examples: `2` | 7 |
| [`leave_party_temporarily`](#leave_party_temporarily) | Object | Event Action: Removes a character from the active team until the next hub area. | 7 |
| [`next_event_from_set`](./Enums.md#enum-next_event_from_set) | Enum | Event Action: Chains immediately into a randomly selected subsequent story event. | 7 |
| `spd` | Number | `aux` | 7 |
| [`decrement_legacy_counter`](./Enums.md#enum-decrement_legacy_counter) | Enum | Examples: `WorldEventLegacyToken_StartDigging, WorldEventLegacyCounter_CrackInTheWall` | 6 |
| `hide_appearance_changes` | Integer | Examples: `1` | 6 |
| `QEVENT_OBELISK_IGNORE` | Variable |  | 6 |
| `QEVENT_OBELISK_REW1` | Variable |  | 6 |
| `QEVENT_OBELISK_REW2` | Variable |  | 6 |
| `QEVENT_OBELISK_REW3` | Variable |  | 6 |
| `QEVENT_OBELISK_REW4` | Variable |  | 6 |
| `Stinky` | Variable |  | 6 |
| `WorldEventLegacyCounter_CrackInTheWall` | Variable |  | 6 |
| `WorldEventLegacyToken_StartDigging` | Variable |  | 6 |
| `blood_altar_items` | Variable |  | 5 |
| `Bottles` | Variable |  | 5 |
| `cha` | Number | `+1`, `aux` | 5 |
| `current_chapter_common` | Mixed | `auto` | 5 |
| `current_chapter_rare` | Mixed | `auto` | 5 |
| [`cutscene_on_exit`](./Enums.md#enum-cutscene_on_exit) | Enum | Examples: `infinite_intro` | 5 |
| [`food`](./Arrays.md#array-food) | Array | Examples: `[ 4 8 ], [ 1 3 ], [ 4 7 ]` | 5 |
| `physical_disorders` | Variable |  | 5 |
| `SlagTight` | Variable |  | 5 |
| [`bad`](#bad) | Object | Event Object: Story branch or dialog option representing the 'Bad' action. | 4 |
| `con` | Number | `aux` | 4 |
| `diseases` | Variable |  | 4 |
| `fleshhead_items` | Variable |  | 4 |
| [`goto`](./Enums.md#enum-goto) | Enum | Examples: `end` | 4 |
| `heal_injury` | Integer | Examples: `1` | 4 |
| `inventory` | Variable |  | 4 |
| [`learn_ability`](./Enums.md#enum-learn_ability) | Enum | Examples: `BarfBall, FutureSight` | 4 |
| [`learn_ability_from_pool`](./Arrays.md#array-learn_ability_from_pool) | Array | Examples: `Necromancer` | 4 |
| `MysteriousStranger_HasLostFinger` | Variable |  | 4 |
| [`outcome`](#outcome) | Object | Event Object: Logic and text executed after selecting a specific dialog option. | 4 |
| `party_heal_disorder` | Integer | Examples: `2` | 4 |
| [`party_permanent_stats_exclude_self`](#party_permanent_stats_exclude_self) | Object | Event Reward: Permanently modifies stats for all party members except the one who initiated the action. | 4 |
| `pills` | Number | Examples: `7` | 4 |
| `QEVENT_THROBBINGARTERY_REW3` | Variable |  | 4 |
| [`random_pool_consider_luck`](./Arrays.md#array-random_pool_consider_luck) | Array | Examples: `[ { prompt "EVENT_TRACY_REW11" weight 1 get_item_from_poo..., [ { prompt "EVE...` | 4 |
| [`upgrade_ability`](./Enums.md#enum-upgrade_ability) | Enum | Examples: `random` | 4 |
| `WorldEventLegacyCounter_ToiletFlushes` | Variable |  | 4 |
| `bone_armor` | Variable |  | 3 |
| `bone_equipment` | Variable |  | 3 |
| `chapter_common` | Number | Examples: `1` | 3 |
| `chapter_specific_item` | Variable |  | 3 |
| `CryogenicTimeChamber_Full` | Variable |  | 3 |
| `end_of_time_unlock` | Variable |  | 3 |
| `gain_cat_familiar` | Integer | Examples: `1` | 3 |
| [`learn_passive_from_pool`](./Arrays.md#array-learn_passive_from_pool) | Array | Examples: `AnyUnlocked` | 3 |
| [`lose_item_from_inventory`](./Enums.md#enum-lose_item_from_inventory) | Enum | Examples: `cat` | 3 |
| [`make_old`](./Enums.md#enum-make_old) | Enum | Examples: `self` | 3 |
| `max_options` | Integer | Examples: `3, 2` | 3 |
| `mental_disorders` | Variable |  | 3 |
| `QEVENT_OBELISK_QUES2` | Variable |  | 3 |
| `QEVENT_VOLCANO_REW2` | Variable |  | 3 |
| `QEVENT_VOLCANO_REW3` | Variable |  | 3 |
| `radiated` | Variable |  | 3 |
| `RestlessDead` | Variable |  | 3 |
| `resultVeryGood` | Variable |  | 3 |
| `Scatological` | Variable |  | 3 |
| `shuffle_options` | Boolean | Examples: `true` | 3 |
| `SlagMight` | Variable |  | 3 |
| `spawn_reflection_next_fight` | Integer | Event Penalty: Spawns dark clones/reflections of the party in the next combat encounter. | 3 |
| [`transform_item`](./Arrays.md#array-transform_item) | Array | Examples: `[ CryogenicTimeChamber_Empty CryogenicTimeChamber_Full ], [ JarOfRadiation Ja...` | 3 |
| [`unlock_item_quest`](./Enums.md#enum-unlock_item_quest) | Enum | Examples: `CryogenicTimeChamber_Full, JarOfChaos, JarOfRadiatedBlood` | 3 |
| [`upgrade_passive`](./Enums.md#enum-upgrade_passive) | Enum | Examples: `random` | 3 |
| [`weight`](./Enums.md#enum-weight) | Float | Probability weight for this outcome. | 3 |
| `AdventureToken_YellowNeedle` | Variable |  | 2 |
| `all` | Variable |  | 2 |
| `Anxiety` | Variable |  | 2 |
| `Cancer` | Variable |  | 2 |
| `CharmedPinky` | Variable |  | 2 |
| `CharmedRaptorBaby` | Variable |  | 2 |
| `clear_result_animation` | Integer | Examples: `1` | 2 |
| [`clear_surviving_kaiju`](./Enums.md#enum-clear_surviving_kaiju) | Enum | Examples: `pyrophina, zaratana` | 2 |
| `Depression` | Variable |  | 2 |
| `flesh_items` | Variable |  | 2 |
| [`gain_immortal_familiar`](./Enums.md#enum-gain_immortal_familiar) | Enum | Examples: `CharmedFleaSpecial` | 2 |
| [`get_and_equip_item`](./Enums.md#enum-get_and_equip_item) | Enum | Examples: `FlyLarva` | 2 |
| `glitched_items` | Variable |  | 2 |
| `HasHitPinata` | Variable |  | 2 |
| `HauntedNight` | Variable |  | 2 |
| `JarOfRadiatedBlood` | Variable |  | 2 |
| `map_unlock_dimensionx` | Variable |  | 2 |
| [`party_gain_disorder_from_pool`](./Arrays.md#array-party_gain_disorder_from_pool) | Array | Examples: `[ Dwarfism ], [ Gigantism ]` | 2 |
| `party_heal_injury` | Integer | Examples: `99` | 2 |
| [`party_permanent_stats`](#party_permanent_stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of all party members. | 2 |
| [`party_random_mutation_from_set`](#party_random_mutation_from_set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 2 |
| `PawShards` | Variable |  | 2 |
| `poop_items` | Variable |  | 2 |
| `PutridLeech` | Variable |  | 2 |
| `PyrophinasCollar` | Variable |  | 2 |
| `QEVENT_OBELISK_QUES1` | Variable |  | 2 |
| `QEVENT_THROBBINGARTERY_REW1` | Variable |  | 2 |
| `QEVENT_THROBBINGARTERY_REW2` | Variable |  | 2 |
| `QEVENT_VOLCANO_REW1` | Variable |  | 2 |
| `ReceiverAntenna` | Variable |  | 2 |
| `resultBad` | Variable |  | 2 |
| `Rocks` | Variable |  | 2 |
| [`scramble_abilities`](./Enums.md#enum-scramble_abilities) | Enum | Examples: `all` | 2 |
| `set_age` | Integer | Examples: `1` | 2 |
| `SignalAmplifier` | Variable |  | 2 |
| `Snake` | Number | Applies or references the 'Snake' effect/state. | 2 |
| [`spin`](./Enums.md#enum-spin) | Enum | Examples: `again` | 2 |
| `ThrobbingGristle` | Variable |  | 2 |
| `TransmitterAntenna` | Variable |  | 2 |
| `ZaratanasCollar` | Variable |  | 2 |
| `AdventureToken_HasRunFromDeath` | Variable |  | 1 |
| `AdventureToken_MysteriousCave_FamiliarVoice` | Variable |  | 1 |
| `AdventureToken_MysteriousJarRepeat` | Variable |  | 1 |
| `AdventureToken_StevenTryAgain` | Variable |  | 1 |
| `AdventureToken_StevenTryAgain2` | Variable |  | 1 |
| `AdventureToken_StevenTryAgain3` | Variable |  | 1 |
| `AdventureToken_TrippedOnBigToe` | Variable |  | 1 |
| `AdventureToken_UnmarkedGraveForced` | Variable |  | 1 |
| `Albinism` | Variable |  | 1 |
| `AlienOvergrowth` | Variable |  | 1 |
| [`alley`](./Enums.md#enum-alley) | Enum | `AREA_NAME_ALLEY`, `departed_first_real_adventure` | 1 |
| [`ambush`](./Math_Equations.md) | Equation | Examples: `"events/chupacabra.lvl"` | 1 |
| `AntennaQuest_Orb` | Variable |  | 1 |
| `AntennaQuest_Rift` | Variable |  | 1 |
| `AntennaQuest_Volcano` | Variable |  | 1 |
| `Beepis` | Variable |  | 1 |
| `bleeding` | Variable |  | 1 |
| `bloody_items` | Variable |  | 1 |
| [`boneyard`](./Enums.md#enum-boneyard) | Enum | `AREA_NAME_BONEYARD`, `mapflag_BoneyardUnlocked` | 1 |
| `BrainDamage` | Variable |  | 1 |
| `BrainDead` | Variable |  | 1 |
| `Brave` | Variable |  | 1 |
| [`bunker`](./Enums.md#enum-bunker) | Enum | `AREA_NAME_BUNKER`, `mapflag_BunkerUnlocked` | 1 |
| `burned` | Variable |  | 1 |
| [`caves`](./Enums.md#enum-caves) | Enum | `AREA_NAME_CAVES`, `mapflag_CavesUnlocked` | 1 |
| [`chapter`](./Enums.md#enum-chapter) | Enum | `alley` | 1 |
| `chapter_rare` | Number | Examples: `1` | 1 |
| `CharmedTarBaby` | Variable |  | 1 |
| `clone_self_to_party` | Integer | Examples: `1` | 1 |
| `copy_items_to_party` | Integer | Examples: `1` | 1 |
| `copy_party_items` | Integer | Examples: `1` | 1 |
| [`core`](./Enums.md#enum-core) | Enum | `AREA_NAME_CORE`, `mapflag_CoreUnlocked`, `mapflag_IceAgeUnlocked` | 1 |
| [`crater`](./Enums.md#enum-crater) | Enum | `AREA_NAME_CRATER`, `mapflag_CraterUnlocked` | 1 |
| `CryogenicTimeChamber_Empty` | Variable |  | 1 |
| `Cunch` | Variable |  | 1 |
| `cursed` | Boolean | `true` | 1 |
| `CursedStickman` | Variable |  | 1 |
| `DeathsScythe` | Variable |  | 1 |
| [`desert`](./Enums.md#enum-desert) | Enum | `AREA_NAME_DESERT`, `mapflag_DesertUnlocked` | 1 |
| `dex` | Number | `aux` | 1 |
| [`dimensionx`](./Enums.md#enum-dimensionx) | Enum | `AREA_NAME_DIMENSIONX`, `mapflag_DimensionXUnlocked`, `mapflag_IceAgeUnlocked` | 1 |
| `dimensionx.gon` | Variable |  | 1 |
| `EnchantingPoop` | Variable |  | 1 |
| `EVENT_USETHETOILET_AGAIN` | Variable |  | 1 |
| `FecalHood_Cursed` | Variable |  | 1 |
| `FecalMask_Cursed` | Variable |  | 1 |
| `Feebis` | Variable |  | 1 |
| [`future`](./Enums.md#enum-future) | Enum | `AREA_NAME_FUTURE`, `mapflag_FutureUnlocked` | 1 |
| [`gain_clone_familiar`](#gain_clone_familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 1 |
| [`general_common`](./Enums.md#enum-general_common) | Enum | `auto` | 1 |
| [`general_rare`](./Enums.md#enum-general_rare) | Enum | `auto` | 1 |
| `GeomagneticStorm` | Variable |  | 1 |
| [`get_full_item_set_from_pool`](./Enums.md#enum-get_full_item_set_from_pool) | Enum | Examples: `common` | 1 |
| `Gigachad` | Variable |  | 1 |
| `godly_items` | Variable |  | 1 |
| `grass_items` | Variable |  | 1 |
| `GuillotinasHead` | Variable |  | 1 |
| `hide_items` | Variable |  | 1 |
| `Host` | Variable |  | 1 |
| [`iceage`](./Enums.md#enum-iceage) | Enum | `AREA_NAME_ICEAGE`, `mapflag_IceAgeUnlocked` | 1 |
| `iceage.gon` | Variable |  | 1 |
| `JarOfChaos` | Variable |  | 1 |
| `JarOfRadiation` | Variable |  | 1 |
| [`junkyard`](./Enums.md#enum-junkyard) | Enum | `AREA_NAME_JUNKYARD`, `mapflag_JunkyardUnlocked` | 1 |
| `junkyard_items` | Variable |  | 1 |
| [`jurassic`](./Enums.md#enum-jurassic) | Enum | `AREA_NAME_JURASSIC`, `endoftime`, `mapflag_JurassicUnlocked` | 1 |
| [`lab`](./Enums.md#enum-lab) | Enum | `AREA_NAME_LAB`, `mapflag_LabUnlocked` | 1 |
| `legacy_event_unlock_momsknife` | Variable |  | 1 |
| [`lose_all_equipped_items`](./Enums.md#enum-lose_all_equipped_items) | Enum | Examples: `cat` | 1 |
| `map_unlock_iceage` | Variable |  | 1 |
| `mapflag_ChaosAntennaAttached` | Variable |  | 1 |
| `mapflag_OrbAntennaAttached` | Variable |  | 1 |
| `mapflag_ThrobbingArteryDone` | Variable |  | 1 |
| `mapflag_VolcanoAntennaAttached` | Variable |  | 1 |
| `mapflag_WallOfFleshDone` | Variable |  | 1 |
| `meat_world_open` | Variable |  | 1 |
| [`meatworld`](./Enums.md#enum-meatworld) | Enum | `AREA_NAME_MEATWORLD`, `mapflag_MeatWorldUnlockedFull` | 1 |
| `MeatWorldQuest_Gristle` | Variable |  | 1 |
| `MeatWorldQuest_Leech` | Variable |  | 1 |
| `MeteorShowerUnlocked` | Variable |  | 1 |
| `MomsKnife` | Variable |  | 1 |
| `monkey_paw_1finger` | Variable |  | 1 |
| `monkey_paw_2fingers` | Variable |  | 1 |
| `monkey_paw_3fingers` | Variable |  | 1 |
| `monkey_paw_4fingers` | Variable |  | 1 |
| [`moon`](./Enums.md#enum-moon) | Enum | `AREA_NAME_MOON`, `mapflag_IceAgeUnlocked`, `mapflag_MoonUnlocked` | 1 |
| `MysteriousTomb1` | Variable |  | 1 |
| `MysteriousTomb2` | Variable |  | 1 |
| `parasite` | Boolean | `true` | 1 |
| [`party_injury`](./Enums.md#enum-party_injury) | Enum | Examples: `random` | 1 |
| [`play_result_animation`](./Enums.md#enum-play_result_animation) | Enum | Examples: `resultVeryGood` | 1 |
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
| `QEVENT_GLOWINGORB_QUES` | Variable |  | 1 |
| `QEVENT_GLOWINGORB_QUES2` | Variable |  | 1 |
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
| `QEVENT_VOLCANO_QUES` | Variable |  | 1 |
| `QEVENT_VOLCANO_QUES2` | Variable |  | 1 |
| `QEVENT_VOLCANO_REW4` | Variable |  | 1 |
| `QEVENT_VOLCANO_REW5` | Variable |  | 1 |
| `QEVENT_VOLCANO_REW7` | Variable |  | 1 |
| `QEVENT_WALLOFFLESH2_QUES` | Variable |  | 1 |
| `QEVENT_WALLOFFLESH2_REW_IGNORE` | Variable |  | 1 |
| `QEVENT_WALLOFFLESH_QUES1` | Variable |  | 1 |
| `QEVENT_WALLOFFLESH_QUES2` | Variable |  | 1 |
| `QEVENT_WALLOFFLESH_REW1` | Variable |  | 1 |
| `QEVENT_WALLOFFLESH_REW10` | Variable |  | 1 |
| `QEVENT_WALLOFFLESH_REW2` | Variable |  | 1 |
| `QEVENT_WALLOFFLESH_REW3` | Variable |  | 1 |
| `QEVENT_WALLOFFLESH_REW4` | Variable |  | 1 |
| `QEVENT_WALLOFFLESH_REW5` | Variable |  | 1 |
| `QEVENT_WALLOFFLESH_REW7` | Variable |  | 1 |
| `QEVENT_WALLOFFLESH_REW8` | Variable |  | 1 |
| `QEVENT_WALLOFFLESH_REW9` | Variable |  | 1 |
| `QEVENT_WALLOFFLESH_REW_IGNORE` | Variable |  | 1 |
| [`random_chance`](#random_chance) | Object | Event Logic: Executes the nested outcome based on a percentage roll. | 1 |
| `raptor_nest_eggs` | Variable |  | 1 |
| [`RaptorEgg`](./Enums.md#enum-raptoregg) | Enum | Examples: `.1` | 1 |
| [`requires_flag`](./Enums.md#enum-requires_flag) | Enum | Prerequisite: Must meet this condition. | 1 |
| `resultConfused` | Variable |  | 1 |
| `resultVeryBad` | Variable |  | 1 |
| `rock_items` | Variable |  | 1 |
| [`scramble_basic_attack`](./Enums.md#enum-scramble_basic_attack) | Enum | Examples: `all` | 1 |
| [`scramble_passives`](./Enums.md#enum-scramble_passives) | Enum | Examples: `all` | 1 |
| [`select_item_from_pool_for_cutscene_only`](./Enums.md#enum-select_item_from_pool_for_cutscene_only) | Enum | Examples: `glitched_items` | 1 |
| `self_heal` | Integer | Examples: `10` | 1 |
| [`sewers`](./Enums.md#enum-sewers) | Enum | `AREA_NAME_SEWERS`, `mapflag_SewersUnlocked` | 1 |
| `SludgeHat` | Variable |  | 1 |
| `SludgeMask` | Variable |  | 1 |
| `Soulless` | Variable |  | 1 |
| `Steven_disorders` | Variable |  | 1 |
| `StrangeEggs` | Variable |  | 1 |
| `tech_items` | Variable |  | 1 |
| [`theend`](./Enums.md#enum-theend) | Enum | `AREA_NAME_THEEND`, `endoftime`, `mapflag_TheEndUnlocked` | 1 |
| `TheRift_UsedPyrophina` | Variable |  | 1 |
| `TheRift_UsedZaratana` | Variable |  | 1 |
| `TheShimmer` | Variable |  | 1 |
| `time_machine_quest_finalstep` | Variable |  | 1 |
| `time_machine_quest_trigger` | Variable |  | 1 |
| `Touched` | Variable |  | 1 |
| `trigger_butterfly_effect` | Integer | Examples: `1` | 1 |
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
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 0 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 0 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 0 |

| `bad` | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| `common` | Object | Event Node: Story branch or dialog option representing the 'Common' action. | 0 |
| `cutscene` | String | Event Node: Triggers a narrative cutscene. | 0 |
| `damage` | Number | Event Node: Story branch or dialog option representing the 'Damage' action. | 0 |
| `gain_familiar` | Enum | Event Action: Adds a specific familiar to the party. | 0 |
| `good` | Object | Event Node: Story branch or dialog option representing the 'Good' action. | 0 |
| `mutation` | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `options` | Object | Event Block: Lists the available clickable dialog choices for the current story node. | 0 |
| `outcome` | Object | Event Block: Logic and text executed after selecting a specific dialog option. | 0 |
| `rare` | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| `reward` | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| `setup` | Object | Event Block: Pre-initialization logic executed before the event UI is drawn. | 0 |
| `spawn_reflection_next_fight` | Number | Event Penalty: Spawns dark clones/reflections of the party in the next combat encounter. | 0 |
| `StatusDamagers` | Object | Event Trigger: Applies nested statuses to damagers. | 0 |
| `StatusEachTurnBegin` | Object | Event Trigger: Applies nested statuses to each turn begin. | 0 |
</details>

### Valid Nested Objects

The following objects all behave as `{Event Keys}` containers. Each has its own unique parameters listed below its entry.

---

#### `bad`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 343

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Properties for configuring event outcomes (rewards, penalties, dialog options, status applications). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 249 |
| [`prompt`](./Enums.md#enum-prompt) | String | Examples: `"woah", "EVENT_TRASHBIN_REW3", "EVENT_ABEGGAR_REW2"` | 38 |
| `set_frame` | Integer | Examples: `4, 2, 5` | 36 |
| [`permanent_stats`](#permanent_stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 7 |
| [`play_animation`](./Arrays.md#array-play_animation) | Array | Examples: `resultVeryGood, resultBad` | 5 |
| [`reward`](#reward) | Object | Event Object: Story branch or dialog option representing the 'Reward' action. | 5 |
| [`kill`](./Enums.md#enum-kill) | Enum | Examples: `cat` | 4 |
| [`event_now`](./Enums.md#enum-event_now) | Enum | Examples: `MeatGolem` | 3 |
| [`event_now_same_cat`](./Enums.md#enum-event_now_same_cat) | Enum | Examples: `BigToe, SpookieApparation, CatHole` | 3 |
| [`battle`](./Math_Equations.md) | Equation | Examples: `{ ... }` | 2 |
| [`get_parasite_from_pool`](./Enums.md#enum-get_parasite_from_pool) | Enum | Examples: `cursed_items, parasites` | 2 |
| [`conditional_reward`](#conditional_reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 1 |
| [`cutscene`](#cutscene) | Object | Event Object: Triggers a narrative cutscene. | 1 |
| [`gain_disorder_from_pool`](./Enums.md#enum-gain_disorder_from_pool) | Enum | Examples: `Crazy_disorders` | 1 |
| [`gain_immortal_familiar`](./Enums.md#enum-gain_immortal_familiar) | Enum | Examples: `CharmedFleaSpecial` | 1 |
| [`get_parasite`](./Enums.md#enum-get_parasite) | Enum | Examples: `FaceShards, BigToeCursed, MetalRod` | 1 |
| [`injury`](./Enums.md#enum-injury) | Enum | Examples: `random` | 1 |
| [`lose_item`](./Enums.md#enum-lose_item) | Enum | Examples: `equipped, inventory` | 1 |
| `next_event_bonus` | Integer | Examples: `2` | 1 |
| [`party_random_mutation_from_set`](#party_random_mutation_from_set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 1 |
| [`select_item_from_pool_for_cutscene_only`](./Enums.md#enum-select_item_from_pool_for_cutscene_only) | Enum | Examples: `glitched_items` | 1 |
| [`self_status_next_fight`](#self_status_next_fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 1 |
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum | Examples: `WorldEventLegacyToken_CryptOpened` | 1 |

</details>

---

#### `common`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1197

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Properties for configuring event outcomes (rewards, penalties, dialog options, status applications). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 658 |
| [`prompt`](./Enums.md#enum-prompt) | String | Examples: `"woah", "EVENT_TRASHBIN_REW3", "EVENT_ABEGGAR_REW2"` | 38 |
| `set_frame` | Integer | Examples: `4, 2, 5` | 36 |
| [`clear_adventure_token`](./Enums.md#enum-clear_adventure_token) | Enum | Examples: `AdventureToken_BlueNeedle, AdventureToken_HasTakenNeedle, AdventureToken_RedN...` | 24 |
| [`event_now_same_cat`](./Enums.md#enum-event_now_same_cat) | Enum | Examples: `BigToe, SpookieApparation, CatHole` | 21 |
| [`spawn_unit_next_fight`](#spawn_unit_next_fight) | Object | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. | 18 |
| [`get_item`](./Enums.md#enum-get_item) | Enum | Examples: `BrokenWindow` | 14 |
| [`play_animation`](./Arrays.md#array-play_animation) | Array | Examples: `resultVeryGood, resultBad` | 13 |
| [`gain_disorder`](./Enums.md#enum-gain_disorder) | Enum | Examples: `BorrowedTime, Brave, Dyslexia` | 12 |
| [`get_item_from_pool`](./Enums.md#enum-get_item_from_pool) | Enum | Event Action: Rewards the player with an item drawn from a specific loot pool. | 11 |
| `override_end_option_prompt` | String | Examples: `"EVENT_MYSTERIOUSSTRANGER_END_AGAIN2", "EVENT_LOCKEDDOOR_PROMPT2", "EVENT_MYS...` | 11 |
| [`party_status_next_fight`](#party_status_next_fight) | Object | Event Penalty/Reward: Applies a status effect to the entire party at the start of the next combat encounter. | 11 |
| `full_heal` | Integer | Examples: `1` | 10 |
| `ambush_next_basic_fights` | Integer | Examples: `1` | 9 |
| [`party_damage`](./Arrays.md#array-party_damage) | Array | Examples: `[ 5 10 ]` | 9 |
| [`set_adventure_token`](./Enums.md#enum-set_adventure_token) | Enum | Examples: `AdventureToken_Mirage2, AdventureToken_StevenTryAgain3, HasPlayedMysteriousSt...` | 9 |
| [`random_mutation_from_set`](#random_mutation_from_set) | Object | Event Reward: Applies a random mutation to a character from a specific pool. | 8 |
| [`get_parasite`](./Enums.md#enum-get_parasite) | Enum | Examples: `FaceShards, BigToeCursed, MetalRod` | 7 |
| [`permanent_stats`](#permanent_stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 7 |
| [`gain_coins`](./Arrays.md#array-gain_coins) | Array | Examples: `[ 4 15 ], 5` | 6 |
| [`global_effect_next_fight`](#global_effect_next_fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 6 |
| [`increment_legacy_counter`](./Enums.md#enum-increment_legacy_counter) | Enum | Examples: `WorldEventLegacyToken_StartDigging, WorldEventLegacyCounter_CrackInTheWall, W...` | 6 |
| [`add_weather`](./Enums.md#enum-add_weather) | Enum | Examples: `TheShimmer, SolarFlare, GeomagneticStorm` | 5 |
| [`kill`](./Enums.md#enum-kill) | Enum | Examples: `cat` | 5 |
| [`lose_item`](./Enums.md#enum-lose_item) | Enum | Examples: `equipped, inventory` | 5 |
| [`shop_now`](./Enums.md#enum-shop_now) | Enum | Examples: `TreasureHard, Event_SmallShop, Event_RareShop` | 5 |
| [`spin`](./Enums.md#enum-spin) | Enum | Examples: `again` | 4 |
| [`gain_familiar`](./Enums.md#enum-gain_familiar) | Enum | Event Action: Adds a specific familiar to the party. | 3 |
| [`gain_food`](./Arrays.md#array-gain_food) | Array | Examples: `[ 5 10 ]` | 3 |
| [`event_now`](./Enums.md#enum-event_now) | Enum | Examples: `MeatGolem` | 2 |
| [`get_parasite_from_pool`](./Enums.md#enum-get_parasite_from_pool) | Enum | Examples: `cursed_items, parasites` | 2 |
| [`lose_specific_item`](./Enums.md#enum-lose_specific_item) | Enum | Examples: `SlagTight` | 2 |
| [`next_event_from_set`](./Enums.md#enum-next_event_from_set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 2 |
| `party_heal_disorder` | Integer | Examples: `2` | 2 |
| [`party_permanent_stats_exclude_self`](#party_permanent_stats_exclude_self) | Object | Event Reward: Permanently modifies stats for all party members except the one who initiated the action. | 2 |
| `ally_ambush_next_fights` | Integer | Examples: `1` | 1 |
| `clear_result_animation` | Integer | Examples: `1` | 1 |
| [`conditional_reward`](#conditional_reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 1 |
| [`decrement_legacy_counter`](./Enums.md#enum-decrement_legacy_counter) | Enum | Examples: `WorldEventLegacyToken_StartDigging, WorldEventLegacyCounter_CrackInTheWall` | 1 |
| [`gain_disorder_from_pool`](./Enums.md#enum-gain_disorder_from_pool) | Enum | Examples: `Crazy_disorders` | 1 |
| [`get_and_equip_item`](./Enums.md#enum-get_and_equip_item) | Enum | Examples: `FlyLarva` | 1 |
| `heal_disorder` | Integer | Examples: `2` | 1 |
| `heal_injury` | Integer | Examples: `1` | 1 |
| [`injury`](./Enums.md#enum-injury) | Enum | Examples: `random` | 1 |
| [`learn_ability_from_pool`](./Enums.md#enum-learn_ability_from_pool) | Enum | Examples: `Necromancer` | 1 |
| [`mutation`](#mutation) | Object | Event Object: Story branch or dialog option representing the 'Mutation' action. | 1 |
| `next_event_bonus` | Integer | Examples: `2` | 1 |
| `party_heal` | Integer | Examples: `10` | 1 |
| `random_mutation` | Integer | Event Reward: Applies a completely random mutation to a character. | 1 |
| `self_heal` | Integer | Examples: `10` | 1 |
| [`self_status_next_fight`](#self_status_next_fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 1 |
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum | Examples: `WorldEventLegacyToken_CryptOpened` | 1 |
| [`upgrade_ability`](./Enums.md#enum-upgrade_ability) | Enum | Examples: `random` | 1 |
| [`random_pool`](./Arrays.md#array-random_pool) | Array | Examples: `[ { weight 90 prompt "EVENT_ABEGGAR_REW1" set_frame 3 ran..., [ { weight 85 p...` | 0 |

</details>

---

#### `good`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 572

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`rare`](./Enums.md#enum-rare) | Object | Event Object: Story branch or dialog option representing the 'Rare' action. | 673 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Properties for configuring event outcomes (rewards, penalties, dialog options, status applications). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 464 |
| [`increment_legacy_counter`](./Enums.md#enum-increment_legacy_counter) | Enum | Examples: `WorldEventLegacyToken_StartDigging, WorldEventLegacyCounter_CrackInTheWall, W...` | 52 |
| [`prompt`](./Enums.md#enum-prompt) | String | Examples: `"woah", "EVENT_TRASHBIN_REW3", "EVENT_ABEGGAR_REW2"` | 38 |
| `set_frame` | Integer | Examples: `4, 2, 5` | 36 |
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum | Examples: `WorldEventLegacyToken_CryptOpened` | 26 |
| [`play_animation`](./Enums.md#enum-play_animation) | Enum | Examples: `resultVeryGood, resultBad` | 20 |
| [`complete_item_quest`](./Enums.md#enum-complete_item_quest) | Enum | Examples: `BlackShard, JarOfRadiation, ScaldingOrb` | 18 |
| [`begin_chapter`](./Enums.md#enum-begin_chapter) | Enum | Examples: `iceage.gon, dimensionx.gon, future.gon` | 12 |
| [`set_adventure_token`](./Enums.md#enum-set_adventure_token) | Enum | Examples: `AdventureToken_Mirage2, AdventureToken_StevenTryAgain3, HasPlayedMysteriousSt...` | 12 |
| [`get_item_from_pool`](./Enums.md#enum-get_item_from_pool) | Enum | Event Action: Rewards the player with an item drawn from a specific loot pool. | 11 |
| [`event_now`](./Enums.md#enum-event_now) | Enum | Examples: `MeatGolem` | 9 |
| [`event_now_same_cat`](./Enums.md#enum-event_now_same_cat) | Enum | Examples: `BigToe, SpookieApparation, CatHole` | 9 |
| [`gain_disorder`](./Enums.md#enum-gain_disorder) | Enum | Examples: `BorrowedTime, Brave, Dyslexia` | 8 |
| [`lose_specific_item`](./Enums.md#enum-lose_specific_item) | Enum | Examples: `SlagTight` | 8 |
| [`trigger_adventure_unlock`](./Enums.md#enum-trigger_adventure_unlock) | Enum | Examples: `end_of_time_unlock, meat_world_unlock` | 7 |
| [`add_weather`](./Enums.md#enum-add_weather) | Enum | Examples: `TheShimmer, SolarFlare, GeomagneticStorm` | 5 |
| [`get_item`](./Enums.md#enum-get_item) | Enum | Examples: `BrokenWindow` | 5 |
| `heal_disorder` | Integer | Examples: `2` | 5 |
| [`reward`](#reward) | Object | Event Object: Story branch or dialog option representing the 'Reward' action. | 5 |
| [`get_parasite`](./Enums.md#enum-get_parasite) | Enum | Examples: `FaceShards, BigToeCursed, MetalRod` | 3 |
| `heal_injury` | Integer | Examples: `1` | 3 |
| [`kill`](./Enums.md#enum-kill) | Enum | Examples: `cat` | 3 |
| [`unlock_item_quest`](./Enums.md#enum-unlock_item_quest) | Enum | Examples: `CryogenicTimeChamber_Full, JarOfChaos, JarOfRadiatedBlood` | 3 |
| [`clear_surviving_kaiju`](./Enums.md#enum-clear_surviving_kaiju) | Enum | Examples: `pyrophina, zaratana` | 2 |
| [`cutscene_on_exit`](./Enums.md#enum-cutscene_on_exit) | Enum | Examples: `infinite_intro` | 2 |
| `full_heal` | Integer | Examples: `1` | 2 |
| [`level_up`](./Enums.md#enum-level_up) | Enum | Examples: `all, self` | 2 |
| `override_end_option_prompt` | String | Examples: `"EVENT_MYSTERIOUSSTRANGER_END_AGAIN2", "EVENT_LOCKEDDOOR_PROMPT2", "EVENT_MYS...` | 2 |
| `ally_ambush_next_fights` | Integer | Examples: `1` | 1 |
| `clone_self_to_party` | Integer | Examples: `1` | 1 |
| [`conditional_reward`](#conditional_reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 1 |
| `copy_items_to_party` | Integer | Examples: `1` | 1 |
| `copy_party_items` | Integer | Examples: `1` | 1 |
| `cutscene` | String | Event Object: Triggers a narrative cutscene. | 1 |
| [`gain_clone_familiar`](#gain_clone_familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 1 |
| [`gain_disorder_from_pool`](./Enums.md#enum-gain_disorder_from_pool) | Enum | Examples: `Crazy_disorders` | 1 |
| [`get_full_item_set_from_pool`](./Enums.md#enum-get_full_item_set_from_pool) | Enum | Examples: `common` | 1 |
| [`global_effect_next_fight`](#global_effect_next_fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 1 |
| [`injury`](./Enums.md#enum-injury) | Enum | Examples: `random` | 1 |
| [`learn_ability_from_pool`](./Arrays.md#array-learn_ability_from_pool) | Array | Examples: `Necromancer` | 1 |
| [`learn_passive_from_pool`](./Arrays.md#array-learn_passive_from_pool) | Array | Examples: `AnyUnlocked` | 1 |
| [`lose_item`](./Enums.md#enum-lose_item) | Enum | Examples: `equipped, inventory` | 1 |
| [`mutation`](#mutation) | Object | Event Object: Story branch or dialog option representing the 'Mutation' action. | 1 |
| `next_event_bonus` | Integer | Examples: `2` | 1 |
| [`next_event_from_set`](./Enums.md#enum-next_event_from_set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 1 |
| `random_mutation` | Integer | Event Reward: Applies a completely random mutation to a character. | 1 |
| [`scramble_abilities`](./Enums.md#enum-scramble_abilities) | Enum | Examples: `all` | 1 |
| [`scramble_passives`](./Enums.md#enum-scramble_passives) | Enum | Examples: `all` | 1 |
| [`shop_now`](./Enums.md#enum-shop_now) | Enum | Examples: `TreasureHard, Event_SmallShop, Event_RareShop` | 1 |
| `trigger_butterfly_effect` | Integer | Examples: `1` | 1 |
| [`upgrade_ability`](./Enums.md#enum-upgrade_ability) | Enum | Examples: `random` | 1 |
| [`upgrade_passive`](./Enums.md#enum-upgrade_passive) | Enum | Examples: `random` | 1 |
| [`gain_food`](./Arrays.md#array-gain_food) | Array | Examples: `[ 5 10 ]` | 0 |
| [`party_gain_disorder_from_pool`](./Arrays.md#array-party_gain_disorder_from_pool) | Array | Examples: `[ Dwarfism ], [ Gigantism ]` | 0 |
| [`random_pool`](./Arrays.md#array-random_pool) | Array | Examples: `[ { weight 90 prompt "EVENT_ABEGGAR_REW1" set_frame 3 ran..., [ { weight 85 p...` | 0 |
| [`random_pool_consider_luck`](./Arrays.md#array-random_pool_consider_luck) | Array | Examples: `[ { prompt "EVENT_TRACY_REW11" weight 1 get_item_from_poo..., [ { prompt "EVE...` | 0 |
| [`transform_item`](./Arrays.md#array-transform_item) | Array | Examples: `[ CryogenicTimeChamber_Empty CryogenicTimeChamber_Full ], [ JarOfRadiation Ja...` | 0 |

</details>

---

#### `main`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 215

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`rare`](./Enums.md#enum-rare) | Object | Event Object: Story branch or dialog option representing the 'Rare' action. | 673 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Properties for configuring event outcomes (rewards, penalties, dialog options, status applications). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 220 |
| [`options`](./Arrays.md#array-options) | Object | Event Object: Lists the available clickable dialog choices for the current story node. | 210 |
| [`prompt`](./Enums.md#enum-prompt) | String | Examples: `"woah", "EVENT_TRASHBIN_REW3", "EVENT_ABEGGAR_REW2"` | 38 |
| `set_frame` | Integer | Examples: `4, 2, 5` | 36 |
| [`setup`](#setup) | Object | Event Object: Pre-initialization logic executed before the event UI is drawn. | 23 |
| [`bad`](#bad) | Object | Event Object: Story branch or dialog option representing the 'Bad' action. | 10 |
| [`weight`](./Enums.md#enum-weight) | Float | Probability weight for this outcome. | 10 |
| [`add_weather`](./Enums.md#enum-add_weather) | Enum | Examples: `TheShimmer, SolarFlare, GeomagneticStorm` | 5 |
| [`requires_flag`](./Enums.md#enum-requires_flag) | Enum | Prerequisite: Must meet this condition. | 5 |
| [`goto`](./Enums.md#enum-goto) | Enum | Examples: `end` | 4 |
| [`outcome`](#outcome) | Object | Event Object: Logic and text executed after selecting a specific dialog option. | 4 |
| [`gain_familiar`](./Enums.md#enum-gain_familiar) | Enum | Event Action: Adds a specific familiar to the party. | 3 |
| `max_options` | Integer | Examples: `3, 2` | 3 |
| `shuffle_options` | Boolean | Examples: `true` | 3 |
| [`next_event_from_set`](./Enums.md#enum-next_event_from_set) | Enum | Event Action: Chains immediately into a randomly selected subsequent story event. | 1 |
| `party_heal` | Integer | Examples: `10` | 1 |
| [`party_permanent_stats`](#party_permanent_stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of all party members. | 1 |
| [`play_animation`](./Arrays.md#array-play_animation) | Array | Examples: `resultVeryGood, resultBad` | 1 |
| [`self_status_next_fight`](#self_status_next_fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 1 |
| [`shop_now`](./Enums.md#enum-shop_now) | Enum | Examples: `TreasureHard, Event_SmallShop, Event_RareShop` | 1 |

</details>

---

#### `rare`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 996

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Properties for configuring event outcomes (rewards, penalties, dialog options, status applications). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 705 |
| [`gain_disorder`](./Enums.md#enum-gain_disorder) | Enum | Examples: `BorrowedTime, Brave, Dyslexia` | 65 |
| [`get_item`](./Enums.md#enum-get_item) | Enum | Examples: `BrokenWindow` | 41 |
| [`prompt`](./Enums.md#enum-prompt) | String | Examples: `"woah", "EVENT_TRASHBIN_REW3", "EVENT_ABEGGAR_REW2"` | 38 |
| `set_frame` | Integer | Examples: `4, 2, 5` | 36 |
| [`event_now_same_cat`](./Enums.md#enum-event_now_same_cat) | Enum | Examples: `BigToe, SpookieApparation, CatHole` | 30 |
| [`get_parasite`](./Enums.md#enum-get_parasite) | Enum | Examples: `FaceShards, BigToeCursed, MetalRod` | 30 |
| [`set_adventure_token`](./Enums.md#enum-set_adventure_token) | Enum | Examples: `AdventureToken_Mirage2, AdventureToken_StevenTryAgain3, HasPlayedMysteriousSt...` | 22 |
| [`spawn_unit_next_fight`](#spawn_unit_next_fight) | Object | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. | 20 |
| [`random_mutation_from_set`](#random_mutation_from_set) | Object | Event Reward: Applies a random mutation to a character from a specific pool. | 13 |
| [`party_status_next_fight`](#party_status_next_fight) | Object | Event Penalty/Reward: Applies a status effect to the entire party at the start of the next combat encounter. | 12 |
| [`get_item_from_pool`](./Enums.md#enum-get_item_from_pool) | Enum | Event Action: Rewards the player with an item drawn from a specific loot pool. | 11 |
| [`learn_passive`](./Enums.md#enum-learn_passive) | Enum | Examples: `CobraStyle, PoisonTips, DeathProof` | 10 |
| [`play_animation`](./Arrays.md#array-play_animation) | Array | Examples: `resultVeryGood, resultBad` | 10 |
| [`increment_legacy_counter`](./Enums.md#enum-increment_legacy_counter) | Enum | Examples: `WorldEventLegacyToken_StartDigging, WorldEventLegacyCounter_CrackInTheWall, W...` | 9 |
| `override_end_option_prompt` | String | Examples: `"EVENT_MYSTERIOUSSTRANGER_END_AGAIN2", "EVENT_LOCKEDDOOR_PROMPT2", "EVENT_MYS...` | 8 |
| [`party_damage`](./Arrays.md#array-party_damage) | Integer | Examples: `[ 5 10 ]` | 8 |
| `party_random_mutation` | Integer | Examples: `1` | 8 |
| `ambush_next_basic_fights` | Integer | Examples: `1` | 7 |
| [`leave_party_temporarily`](#leave_party_temporarily) | Object | Event Action: Removes a character from the active team until the next hub area. | 7 |
| [`lose_item`](./Enums.md#enum-lose_item) | Enum | Examples: `equipped, inventory` | 7 |
| [`permanent_stats`](#permanent_stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 7 |
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum | Examples: `WorldEventLegacyToken_CryptOpened` | 7 |
| [`gain_coins`](./Arrays.md#array-gain_coins) | Array | Examples: `[ 4 15 ], 5` | 6 |
| `hide_appearance_changes` | Integer | Examples: `1` | 6 |
| [`shop_now`](./Enums.md#enum-shop_now) | Enum | Examples: `TreasureHard, Event_SmallShop, Event_RareShop` | 6 |
| [`add_weather`](./Enums.md#enum-add_weather) | Enum | Examples: `TheShimmer, SolarFlare, GeomagneticStorm` | 5 |
| [`decrement_legacy_counter`](./Enums.md#enum-decrement_legacy_counter) | Enum | Examples: `WorldEventLegacyToken_StartDigging, WorldEventLegacyCounter_CrackInTheWall` | 5 |
| `full_heal` | Integer | Examples: `1` | 4 |
| [`learn_ability`](./Enums.md#enum-learn_ability) | Enum | Examples: `BarfBall, FutureSight` | 4 |
| [`gain_familiar`](./Enums.md#enum-gain_familiar) | Enum | Event Action: Adds a specific familiar to the party. | 3 |
| [`global_effect_next_fight`](#global_effect_next_fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 3 |
| [`kill`](./Enums.md#enum-kill) | Enum | Examples: `cat` | 3 |
| [`lose_item_from_inventory`](./Enums.md#enum-lose_item_from_inventory) | Enum | Examples: `cat` | 3 |
| [`make_old`](./Enums.md#enum-make_old) | Enum | Examples: `self` | 3 |
| [`next_event_from_set`](./Enums.md#enum-next_event_from_set) | Enum | Event Action: Chains immediately into a randomly selected subsequent story event. | 3 |
| `spawn_reflection_next_fight` | Integer | Event Penalty: Spawns dark clones/reflections of the party in the next combat encounter. | 3 |
| [`battle`](./Math_Equations.md) | Equation | Examples: `{ ... }` | 2 |
| [`event_now`](./Enums.md#enum-event_now) | Enum | Examples: `MeatGolem` | 2 |
| [`gain_food`](./Arrays.md#array-gain_food) | Array | Examples: `[ 5 10 ]` | 2 |
| [`get_parasite_from_pool`](./Enums.md#enum-get_parasite_from_pool) | Enum | Examples: `cursed_items, parasites` | 2 |
| [`level_up`](./Enums.md#enum-level_up) | Enum | Examples: `all, self` | 2 |
| [`lose_specific_item`](./Enums.md#enum-lose_specific_item) | Enum | Examples: `SlagTight` | 2 |
| `party_heal_disorder` | Integer | Examples: `2` | 2 |
| `party_heal_injury` | Integer | Examples: `99` | 2 |
| [`party_permanent_stats_exclude_self`](#party_permanent_stats_exclude_self) | Object | Event Reward: Permanently modifies stats for all party members except the one who initiated the action. | 2 |
| `set_age` | Integer | Examples: `1` | 2 |
| [`upgrade_ability`](./Enums.md#enum-upgrade_ability) | Enum | Examples: `random` | 2 |
| [`upgrade_passive`](./Enums.md#enum-upgrade_passive) | Enum | Examples: `random` | 2 |
| `ally_ambush_next_fights` | Integer | Examples: `1` | 1 |
| [`ambush`](./Math_Equations.md) | Equation | Examples: `"events/chupacabra.lvl"` | 1 |
| `clear_result_animation` | Integer | Examples: `1` | 1 |
| [`conditional_reward`](#conditional_reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 1 |
| `gain_cat_familiar` | Integer | Examples: `1` | 1 |
| [`gain_disorder_from_pool`](./Enums.md#enum-gain_disorder_from_pool) | Enum | Examples: `Crazy_disorders` | 1 |
| [`gain_immortal_familiar`](./Enums.md#enum-gain_immortal_familiar) | Enum | Examples: `CharmedFleaSpecial` | 1 |
| [`get_and_equip_item`](./Enums.md#enum-get_and_equip_item) | Enum | Examples: `FlyLarva` | 1 |
| `heal_disorder` | Integer | Examples: `2` | 1 |
| [`injury`](./Enums.md#enum-injury) | Enum | Examples: `random` | 1 |
| [`learn_ability_from_pool`](./Enums.md#enum-learn_ability_from_pool) | Enum | Examples: `Necromancer` | 1 |
| [`learn_passive_from_pool`](./Enums.md#enum-learn_passive_from_pool) | Enum | Examples: `AnyUnlocked` | 1 |
| [`lose_all_equipped_items`](./Enums.md#enum-lose_all_equipped_items) | Enum | Examples: `cat` | 1 |
| [`mutation`](#mutation) | Object | Event Object: Story branch or dialog option representing the 'Mutation' action. | 1 |
| `next_event_bonus` | Integer | Examples: `2` | 1 |
| `party_heal` | Integer | Examples: `10` | 1 |
| [`party_injury`](./Enums.md#enum-party_injury) | Enum | Examples: `random` | 1 |
| [`party_permanent_stats`](#party_permanent_stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of all party members. | 1 |
| [`party_random_mutation_from_set`](#party_random_mutation_from_set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 1 |
| [`play_result_animation`](./Enums.md#enum-play_result_animation) | Enum | Examples: `resultVeryGood` | 1 |
| `random_mutation` | Integer | Event Reward: Applies a completely random mutation to a character. | 1 |
| [`scramble_abilities`](./Enums.md#enum-scramble_abilities) | Enum | Examples: `all` | 1 |
| [`scramble_basic_attack`](./Enums.md#enum-scramble_basic_attack) | Enum | Examples: `all` | 1 |
| [`self_status_next_fight`](#self_status_next_fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 1 |
| [`trigger_adventure_unlock`](./Enums.md#enum-trigger_adventure_unlock) | Enum | Examples: `end_of_time_unlock, meat_world_unlock` | 1 |
| [`random_pool`](./Arrays.md#array-random_pool) | Array | Examples: `[ { weight 90 prompt "EVENT_ABEGGAR_REW1" set_frame 3 ran..., [ { weight 85 p...` | 0 |

</details>

---

#### `reward`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 760

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Properties for configuring event outcomes (rewards, penalties, dialog options, status applications). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 1364 |
| [`common`](./Enums.md#enum-common) | Object | Event Object: Story branch or dialog option representing the 'Common' action. | 1067 |
| [`rare`](./Enums.md#enum-rare) | Object | Event Object: Story branch or dialog option representing the 'Rare' action. | 673 |
| [`prompt`](./Enums.md#enum-prompt) | String | Examples: `"woah", "EVENT_TRASHBIN_REW3", "EVENT_ABEGGAR_REW2"` | 38 |
| `set_frame` | Integer | Examples: `4, 2, 5` | 36 |
| [`clear_adventure_token`](./Enums.md#enum-clear_adventure_token) | Enum | Examples: `AdventureToken_BlueNeedle, AdventureToken_HasTakenNeedle, AdventureToken_RedN...` | 24 |
| [`get_item_from_pool`](./Enums.md#enum-get_item_from_pool) | Enum | Event Action: Rewards the player with an item drawn from a specific loot pool. | 11 |
| [`set_subject`](./Enums.md#enum-set_subject) | Enum | Examples: `subject_frame, wall_of_flesh_noartery, throbbing_artery_noflesh` | 10 |
| [`weight`](./Enums.md#enum-weight) | Float | Probability weight for this outcome. | 10 |
| [`set_adventure_token`](./Enums.md#enum-set_adventure_token) | Enum | Examples: `AdventureToken_Mirage2, AdventureToken_StevenTryAgain3, HasPlayedMysteriousSt...` | 9 |
| [`trigger_adventure_unlock`](./Enums.md#enum-trigger_adventure_unlock) | Enum | Examples: `end_of_time_unlock, meat_world_unlock` | 5 |
| [`play_animation`](./Arrays.md#array-play_animation) | Array | Examples: `resultVeryGood, resultBad` | 4 |
| [`cutscene_on_exit`](./Enums.md#enum-cutscene_on_exit) | Enum | Examples: `infinite_intro` | 3 |
| [`get_parasite_from_pool`](./Enums.md#enum-get_parasite_from_pool) | Enum | Examples: `cursed_items, parasites` | 2 |
| [`level_up`](./Enums.md#enum-level_up) | Enum | Examples: `all, self` | 2 |
| [`spawn_unit_next_fight`](#spawn_unit_next_fight) | Object | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. | 2 |
| `ambush_next_basic_fights` | Integer | Examples: `1` | 1 |
| [`event_now`](./Enums.md#enum-event_now) | Enum | Examples: `MeatGolem` | 1 |
| [`gain_coins`](./Arrays.md#array-gain_coins) | Array | Examples: `[ 4 15 ], 5` | 1 |
| [`gain_disorder_from_pool`](./Enums.md#enum-gain_disorder_from_pool) | Enum | Examples: `Crazy_disorders` | 1 |
| [`get_item`](./Enums.md#enum-get_item) | Enum | Examples: `BrokenWindow` | 1 |
| [`injury`](./Enums.md#enum-injury) | Enum | Examples: `random` | 1 |
| `next_event_bonus` | Integer | Examples: `2` | 1 |
| [`random_chance`](#random_chance) | Object | Event Logic: Executes the nested outcome based on a percentage roll. | 1 |
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum | Examples: `WorldEventLegacyToken_CryptOpened` | 1 |
| [`party_damage`](./Arrays.md#array-party_damage) | Array | Examples: `[ 5 10 ]` | 0 |
| [`random_pool`](./Arrays.md#array-random_pool) | Array | Examples: `[ { weight 90 prompt "EVENT_ABEGGAR_REW1" set_frame 3 ran..., [ { weight 85 p...` | 0 |

</details>

