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
| [`common`](./Enums.md#enum-common) | Enum | Event Object: Story branch or dialog option representing the 'Common' action. | 1067 |  |
| [`rare`](./Enums.md#enum-rare) | Enum | Event Object: Story branch or dialog option representing the 'Rare' action. | 673 ||
| `cha` | Enum / Integer | `+1`, `aux` | 468 ||
| `spd` | Enum / Integer | `aux` | 424 ||
| `con` | Enum / Integer | `aux` | 416 ||
| `dex` | Enum / Integer | `aux` | 301 ||
| [`main`](Events_and_Encounters.md#object-main) | Object | Event Object: The central hub or recurring menu of a story event. | 214 ||
| [`options`](./Arrays.md#array-options) | Array | Event Object: Lists the available clickable dialog choices for the current story node. | 210 ||
| [`play_animation`](./Enums.md#enum-play_animation) | Enum | Examples: `resultVeryGood, resultBad` | 160 ||
| `cursed` | Boolean | `true` | 154 ||
| `parasite` | Boolean | `true` | 102 ||
| [`complete_chapter`](./Enums.md#enum-complete_chapter) | Enum | `alley`, `boneyard`, `bunker`, `caves`, `core` | 90 ||
| [`gain_disorder`](./Enums.md#enum-gain_disorder) | Enum | Examples: `BorrowedTime, Brave, Dyslexia` | 85 ||
| `auto` | Variable | When true, the event triggers automatically. | 82 ||
| [`random_pool`](./Arrays.md#array-random_pool) | Array | Examples: `[ { weight 90 prompt "EVENT_ABEGGAR_REW1" set_frame 3 ran..., [ { weight 85 p...` | 79 ||
| [`increment_legacy_counter`](./Enums.md#enum-increment_legacy_counter) | Enum | Examples: `WorldEventLegacyToken_StartDigging, WorldEventLegacyCounter_CrackInTheWall, W...` | 67 ||
| [`event_now_same_cat`](./Enums.md#enum-event_now_same_cat) | Enum | Examples: `BigToe, SpookieApparation, CatHole` | 63 ||
| [`get_item`](./Enums.md#enum-get_item) | Enum | Examples: `BrokenWindow` | 61 ||
| [`set_adventure_token`](./Enums.md#enum-set_adventure_token) | Enum | Examples: `AdventureToken_Mirage2, AdventureToken_StevenTryAgain3, HasPlayedMysteriousSt...` | 52 ||
| `WorldEventLegacyCounter_Jack` | Variable | Tracks the number of times the Jack world event has occurred. | 50 ||
| [`clear_adventure_token`](./Enums.md#enum-clear_adventure_token) | Enum | Examples: `AdventureToken_BlueNeedle, AdventureToken_HasTakenNeedle, AdventureToken_RedN...` | 48 ||
| [`gain_coins`](./Arrays.md#array-gain_coins) | Array | Examples: `[ 4 15 ], 5` | 47 ||
| [`get_parasite`](./Enums.md#enum-get_parasite) | Enum | Examples: `FaceShards, BigToeCursed, MetalRod` | 41 ||
| [`spawn_unit_next_fight`](Events_and_Encounters.md#object-spawn_unit_next_fight) | Object | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. | 40 ||
| [`prompt`](./Enums.md#enum-prompt) | String | Examples: `"woah", "EVENT_TRASHBIN_REW3", "EVENT_ABEGGAR_REW2"` | 38 |  |
| `set_frame` | Integer | Examples: `4, 2, 5` | 36 |  |
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum | Examples: `WorldEventLegacyToken_CryptOpened` | 36 ||
| `resultHole` | Variable | Specifies the resulting hole from an event (e.g., digging). | 32 ||
| [`gain_food`](./Arrays.md#array-gain_food) | Array | Examples: `[ 5 10 ]` | 28 ||
| [`dimensionx`](./Enums.md#enum-dimensionx) | Enum | `AREA_NAME_DIMENSIONX`, `mapflag_DimensionXUnlocked`, `mapflag_IceAgeUnlocked` | 27 ||
| [`party_damage`](./Arrays.md#array-party_damage) | Array | Examples: `[ 5 10 ]` | 26 ||
| [`meatworld`](./Enums.md#enum-meatworld) | Enum | `AREA_NAME_MEATWORLD`, `mapflag_MeatWorldUnlockedFull` | 24 ||
| [`party_status_next_fight`](Events_and_Encounters.md#object-party_status_next_fight) | Object | Event Penalty/Reward: Applies a status effect to the entire party at the start of the next combat encounter. | 23 ||
| [`setup`](Events_and_Encounters.md#object-setup) | Object | Event Object: Pre-initialization logic executed before the event UI is drawn. | 23 ||
| `override_end_option_prompt` | String | Examples: `"EVENT_MYSTERIOUSSTRANGER_END_AGAIN2", "EVENT_LOCKEDDOOR_PROMPT2", "EVENT_MYS...` | 21 ||
| [`random_mutation_from_set`](Events_and_Encounters.md#object-random_mutation_from_set) | Object | Event Reward: Applies a random mutation to a character from a specific pool. | 21 ||
| [`boneyard`](./Enums.md#enum-boneyard) | Enum | `AREA_NAME_BONEYARD`, `mapflag_BoneyardUnlocked` | 21 ||
| [`bunker`](./Enums.md#enum-bunker) | Enum | `AREA_NAME_BUNKER`, `mapflag_BunkerUnlocked` | 20 ||
| [`core`](./Enums.md#enum-core) | Enum | `AREA_NAME_CORE`, `mapflag_CoreUnlocked`, `mapflag_IceAgeUnlocked` | 20 ||
| [`moon`](./Enums.md#enum-moon) | Enum | `AREA_NAME_MOON`, `mapflag_IceAgeUnlocked`, `mapflag_MoonUnlocked` | 20 ||
| `AdventureToken_HasTakenNeedle` | Variable | Indicates whether the unit has taken a needle from the adventure token. | 18 ||
| [`complete_item_quest`](./Enums.md#enum-complete_item_quest) | Enum | Examples: `BlackShard, JarOfRadiation, ScaldingOrb` | 18 ||
| [`alley`](./Enums.md#enum-alley) | Enum | `AREA_NAME_ALLEY`, `departed_first_real_adventure` | 18 ||
| `ambush_next_basic_fights` | Integer | Examples: `1` | 17 ||
| [`event_now`](./Enums.md#enum-event_now) | Enum | Examples: `MeatGolem` | 17 ||
| `full_heal` | Integer | Examples: `1` | 16 ||
| [`crater`](./Enums.md#enum-crater) | Enum | `AREA_NAME_CRATER`, `mapflag_CraterUnlocked` | 16 ||
| [`desert`](./Enums.md#enum-desert) | Enum | `AREA_NAME_DESERT`, `mapflag_DesertUnlocked` | 16 ||
| [`future`](./Enums.md#enum-future) | Enum | `AREA_NAME_FUTURE`, `mapflag_FutureUnlocked` | 16 ||
| [`sewers`](./Enums.md#enum-sewers) | Enum | `AREA_NAME_SEWERS`, `mapflag_SewersUnlocked` | 16 ||
| [`StatusEachTurnBegin`](Cat_Mutations.md#object-statuseachturnbegin) | Object | Event Trigger: Applies nested statuses to each turn begin. | 16 ||
| [`kill`](./Enums.md#enum-kill) | Enum | Examples: `cat` | 15 ||
| `AdventureToken_BlueNeedle` | Variable | Specifies the blue needle variant from the adventure token. | 14 ||
| `AdventureToken_RedNeedle` | Variable | Specifies the red needle variant from the adventure token. | 14 ||
| [`lose_item`](./Enums.md#enum-lose_item) | Enum | Examples: `equipped, inventory` | 14 ||
| [`iceage`](./Enums.md#enum-iceage) | Enum | `AREA_NAME_ICEAGE`, `mapflag_IceAgeUnlocked` | 14 ||
| [`jurassic`](./Enums.md#enum-jurassic) | Enum | `AREA_NAME_JURASSIC`, `endoftime`, `mapflag_JurassicUnlocked` | 14 ||
| [`lab`](./Enums.md#enum-lab) | Enum | `AREA_NAME_LAB`, `mapflag_LabUnlocked` | 14 ||
| [`theend`](./Enums.md#enum-theend) | Enum | `AREA_NAME_THEEND`, `endoftime`, `mapflag_TheEndUnlocked` | 14 ||
| [`shop_now`](./Enums.md#enum-shop_now) | Enum | Examples: `TreasureHard, Event_SmallShop, Event_RareShop` | 13 ||
| [`trigger_adventure_unlock`](./Enums.md#enum-trigger_adventure_unlock) | Enum | Examples: `end_of_time_unlock, meat_world_unlock` | 13 ||
| `all_disorders` | Variable | A list of all disorder IDs available. | 12 ||
| [`begin_chapter`](./Enums.md#enum-begin_chapter) | Enum | Examples: `iceage.gon, dimensionx.gon, future.gon` | 12 ||
| [`lose_specific_item`](./Enums.md#enum-lose_specific_item) | Enum | Examples: `SlagTight` | 12 ||
| `current_chapter_common` | Variable | `auto` | 12 ||
| `current_chapter_rare` | Variable | `auto` | 12 ||
| [`caves`](./Enums.md#enum-caves) | Enum | `AREA_NAME_CAVES`, `mapflag_CavesUnlocked` | 12 ||
| [`junkyard`](./Enums.md#enum-junkyard) | Enum | `AREA_NAME_JUNKYARD`, `mapflag_JunkyardUnlocked` | 12 ||
| [`get_item_from_pool`](./Enums.md#enum-get_item_from_pool) | Enum | Event Action: Rewards the player with an item drawn from a specific loot pool. | 11 ||
| [`CharmedMaggot`](#object-charmedmaggot) | Object | A variant of the Maggot familiar that is charmed (green tint). | 11 ||
| [`food`](./Arrays.md#array-food) | Array | Examples: `[ 4 8 ], [ 1 3 ], [ 4 7 ]` | 11 ||
| [`cat`](Characters_and_Bosses.md#object-cat) | Variable | References the cat unit type. | 10 ||
| [`global_effect_next_fight`](Events_and_Encounters.md#object-global_effect_next_fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 10 ||
| `HasPlayedMysteriousStranger` | Variable | Indicates whether the unit has interacted with the Mysterious Stranger. | 10 ||
| [`learn_passive`](./Enums.md#enum-learn_passive) | Enum | Examples: `CobraStyle, PoisonTips, DeathProof` | 10 ||
| [`set_subject`](./Enums.md#enum-set_subject) | Enum | Examples: `subject_frame, wall_of_flesh_noartery, throbbing_artery_noflesh` | 10 ||
| [`bad`](Events_and_Encounters.md#object-bad) | Object | Event Object: Story branch or dialog option representing the 'Bad' action. | 10 ||
| [`weight`](./Enums.md#enum-weight) | Float | Probability weight for this outcome. | 10 ||
| `chapter_rare` | Number | Examples: `1` | 10 ||
| [`good`](#good) | Boolean | `false`, `true` | 8 ||
| `parasites` | Variable | A list of parasites present. | 8 ||
| `party_random_mutation` | Integer | Examples: `1` | 8 ||
| [`permanent_stats`](Events_and_Encounters.md#object-permanent_stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 7 ||
| `heal_disorder` | Integer | Examples: `2` | 7 ||
| [`leave_party_temporarily`](Events_and_Encounters.md#object-leave_party_temporarily) | Object | Event Action: Removes a character from the active team until the next hub area. | 7 ||
| [`next_event_from_set`](./Enums.md#enum-next_event_from_set) | Enum | Event Action: Chains immediately into a randomly selected subsequent story event. | 7 ||
| `chapter_common` | Number | Examples: `1` | 7 ||
| `consumables` | Number | Examples: `60, 10` | 6 ||
| [`decrement_legacy_counter`](./Enums.md#enum-decrement_legacy_counter) | Enum | Examples: `WorldEventLegacyToken_StartDigging, WorldEventLegacyCounter_CrackInTheWall` | 6 ||
| `hide_appearance_changes` | Integer | Examples: `1` | 6 ||
| `QEVENT_OBELISK_IGNORE` | Variable | Flag to ignore the Obelisk quest event. | 6 ||
| `QEVENT_OBELISK_REW1` | Variable | Reward tier 1 for the Obelisk quest event. | 6 ||
| `QEVENT_OBELISK_REW2` | Variable | Reward tier 2 for the Obelisk quest event. | 6 ||
| `QEVENT_OBELISK_REW3` | Variable | Reward tier 3 for the Obelisk quest event. | 6 ||
| `QEVENT_OBELISK_REW4` | Variable | Reward tier 4 for the Obelisk quest event. | 6 ||
| [`Stinky`](#object-stinky) | Variable | The Stinky disorder that causes the unit to emit a stench. | 6 ||
| `WorldEventLegacyCounter_CrackInTheWall` | Variable | Tracks the number of times the Crack in the Wall event has occurred. | 6 ||
| `WorldEventLegacyToken_StartDigging` | Variable | Token flag to start the digging event. | 6 ||
| [`chapter`](./Enums.md#enum-chapter) | Enum | `alley` | 6 ||
| [`JarOfRadiation`](#object-jarofradiation) | Object | A jar containing radiation, used in events. | 6 ||
| [`reward`](Events_and_Encounters.md#object-reward) | Object | Event Object: Story branch or dialog option representing the 'Reward' action. | 5 ||
| [`add_weather`](./Enums.md#enum-add_weather) | Enum | Examples: `TheShimmer, SolarFlare, GeomagneticStorm` | 5 ||
| `blood_altar_items` | Variable | A list of items that can be sacrificed at the blood altar. | 5 ||
| [`cutscene_on_exit`](./Enums.md#enum-cutscene_on_exit) | Enum | Examples: `infinite_intro` | 5 ||
| `physical_disorders` | Variable | A list of physical disorder IDs. | 5 ||
| [`SlagTight`](#object-slagtight) | Object | A tight slag object, likely a resource. | 5 ||
| [`requires_flag`](./Enums.md#enum-requires_flag) | Enum | Prerequisite: Must meet this condition. | 5 ||
| `diseases` | Variable | A list of disease IDs. | 4 ||
| `fleshhead_items` | Variable | A list of items related to the Fleshhead enemy. | 4 ||
| [`goto`](./Enums.md#enum-goto) | Enum | Examples: `end` | 4 ||
| `heal_injury` | Integer | Examples: `1` | 4 ||
| `inventory` | Variable | The unit's inventory of items. | 4 ||
| [`learn_ability`](./Enums.md#enum-learn_ability) | Enum | Examples: `BarfBall, FutureSight` | 4 ||
| [`learn_ability_from_pool`](./Arrays.md#array-learn_ability_from_pool) | Array | Examples: `Necromancer` | 4 ||
| `MysteriousStranger_HasLostFinger` | Variable | Indicates whether the unit has lost a finger to the Mysterious Stranger. | 4 ||
| [`outcome`](Events_and_Encounters.md#object-outcome) | Object | Event Object: Logic and text executed after selecting a specific dialog option. | 4 ||
| `party_heal_disorder` | Integer | Examples: `2` | 4 ||
| [`party_permanent_stats_exclude_self`](Events_and_Encounters.md#object-party_permanent_stats_exclude_self) | Object | Event Reward: Permanently modifies stats for all party members except the one who initiated the action. | 4 ||
| `QEVENT_THROBBINGARTERY_REW3` | Variable | Reward tier 3 for the Throbbing Artery quest event. | 4 ||
| [`random_pool_consider_luck`](./Arrays.md#array-random_pool_consider_luck) | Array | Examples: `[ { prompt "EVENT_TRACY_REW11" weight 1 get_item_from_poo..., [ { prompt "EVE...` | 4 ||
| [`upgrade_ability`](./Enums.md#enum-upgrade_ability) | Enum | Examples: `random` | 4 ||
| `WorldEventLegacyCounter_ToiletFlushes` | Variable | Tracks the number of toilet flushes in the world. | 4 ||
| [`JarOfRadiatedBlood`](#object-jarofradiatedblood) | Object | A jar containing radiated blood. | 4 ||
| [`spin`](./Enums.md#enum-spin) | Enum | Examples: `again` | 4 ||
| [`JarOfChaos`](#object-jarofchaos) | Object | A jar containing chaos essence. | 4 ||
| [`gain_familiar`](./Enums.md#enum-gain_familiar) | Enum | Event Action: Adds a specific familiar to the party. | 3 ||
| `bone_armor` | Variable | Bone armor item or value. | 3 ||
| `bone_equipment` | Variable | Bone equipment item or value. | 3 ||
| [`chapter_specific_item`](#object-chapter_specific_item) | Variable | An item specific to the current chapter. | 3 ||
| [`CryogenicTimeChamber_Full`](#object-cryogenictimechamber_full) | Object | A full cryogenic time chamber, used for storage. | 3 ||
| [`end_of_time_unlock`](#object-end_of_time_unlock) | Variable | Unlocks the End of Time area. | 3 ||
| [`learn_passive_from_pool`](./Arrays.md#array-learn_passive_from_pool) | Array | Examples: `AnyUnlocked` | 3 ||
| [`lose_item_from_inventory`](./Enums.md#enum-lose_item_from_inventory) | Enum | Examples: `cat` | 3 ||
| [`make_old`](./Enums.md#enum-make_old) | Enum | Examples: `self` | 3 ||
| `max_options` | Integer | Examples: `3, 2` | 3 ||
| `mental_disorders` | Variable | Specifies the list of mental disorder statuses applied to a unit. | 3 ||
| `QEVENT_OBELISK_QUES2` | Variable | Determines if the second Obelisk quest event has been completed. | 3 ||
| `QEVENT_VOLCANO_REW2` | Variable | Determines if the second Volcano reward event has been triggered. | 3 ||
| `QEVENT_VOLCANO_REW3` | Variable | Determines if the third Volcano reward event has been triggered. | 3 ||
| [`radiated`](#object-radiated) | Variable | Determines if the unit has been affected by radiation and is now Radiated. | 3 ||
| [`RestlessDead`](#object-restlessdead) | Variable | Determines if the Restless Dead event is active or if the unit has the Restless Dead status. | 3 ||
| `resultVeryGood` | Variable | Determines if the event outcome was very good, affecting subsequent choices or rewards. | 3 ||
| [`Scatological`](#object-scatological) | Variable | Specifies the Scatological disorder, which causes a unit to produce fecal-related effects. | 3 ||
| `shuffle_options` | Boolean | Examples: `true` | 3 ||
| [`SlagMight`](#object-slagmight) | Object | Specifies the Slag Might item, a powerful trinket or consumable. | 3 ||
| `spawn_reflection_next_fight` | Integer | Event Penalty: Spawns dark clones/reflections of the party in the next combat encounter. | 3 ||
| [`transform_item`](./Arrays.md#array-transform_item) | Array | Examples: `[ CryogenicTimeChamber_Empty CryogenicTimeChamber_Full ], [ JarOfRadiation Ja...` | 3 ||
| [`unlock_item_quest`](./Enums.md#enum-unlock_item_quest) | Enum | Examples: `CryogenicTimeChamber_Full, JarOfChaos, JarOfRadiatedBlood` | 3 ||
| [`upgrade_passive`](./Enums.md#enum-upgrade_passive) | Enum | Examples: `random` | 3 ||
| [`get_parasite_from_pool`](./Enums.md#enum-get_parasite_from_pool) | Enum | Examples: `cursed_items, parasites` | 2 ||
| [`battle`](./Math_Equations.md) | Equation | Examples: `{ ... }` | 2 ||
| [`level_up`](./Enums.md#enum-level_up) | Enum | Examples: `all, self` | 2 ||
| [`Bottles`](#object-bottles) | Object | Specifies the Bottles item, a trinket or stackable resource. | 2 ||
| `pills` | Number | Examples: `7` | 2 ||
| `AdventureToken_YellowNeedle` | Variable | Determines if the Yellow Needle adventure token has been collected, tracking a quest step. | 2 ||
| `all` | Variable | Applies the referenced property or action to all valid targets or categories. | 2 ||
| [`Anxiety`](#object-anxiety) | Variable | Specifies the Anxiety disorder, which afflicts a unit with nervousness and potential stat penalties. | 2 ||
| [`Cancer`](#object-cancer) | Object | Specifies the Cancer disorder or trinket, which applies a degenerating or cursed effect to the unit. | 2 ||
| [`CharmedPinky`](#object-charmedpinky) | Object | Specifies the Charmed Pinky familiar, a friendly variant that fights for the player's faction. | 2 ||
| [`CharmedRaptorBaby`](#object-charmedraptorbaby) | Object | Specifies the Charmed Raptor Baby familiar, a friendly variant that fights for the player's faction. | 2 ||
| `clear_result_animation` | Integer | Examples: `1` | 2 ||
| [`clear_surviving_kaiju`](./Enums.md#enum-clear_surviving_kaiju) | Enum | Examples: `pyrophina, zaratana` | 2 ||
| [`Depression`](#object-depression) | Variable | Specifies the Depression disorder, which inflicts a unit with decreased morale or stats. | 2 ||
| `flesh_items` | Variable | The amount of flesh-based items in the inventory or loot pool. | 2 ||
| [`gain_immortal_familiar`](./Enums.md#enum-gain_immortal_familiar) | Enum | Examples: `CharmedFleaSpecial` | 2 ||
| [`get_and_equip_item`](./Enums.md#enum-get_and_equip_item) | Enum | Examples: `FlyLarva` | 2 ||
| `glitched_items` | Variable | The amount of glitched items in the inventory or loot pool. | 2 ||
| `HasHitPinata` | Variable | Determines if the unit or run has already hit the Pinata, preventing repeat rewards. | 2 ||
| [`HauntedNight`](#object-hauntednight) | Variable | Determines if the Haunted Night encounter or modifier is active. | 2 ||
| [`map_unlock_dimensionx`](#object-map_unlock_dimensionx) | Variable | Unlocks the Dimension X map region when set. | 2 ||
| [`party_gain_disorder_from_pool`](./Arrays.md#array-party_gain_disorder_from_pool) | Array | Examples: `[ Dwarfism ], [ Gigantism ]` | 2 ||
| `party_heal_injury` | Integer | Examples: `99` | 2 ||
| [`party_permanent_stats`](Events_and_Encounters.md#object-party_permanent_stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of all party members. | 2 ||
| [`party_random_mutation_from_set`](Events_and_Encounters.md#object-party_random_mutation_from_set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 2 ||
| [`PawShards`](#object-pawshards) | Object | Specifies the Paw Shards item, a crafting or quest material. | 2 ||
| `poop_items` | Variable | The amount of poop items in the inventory or loot pool. | 2 ||
| [`PutridLeech`](#object-putridleech) | Object | Specifies the Putrid Leech item, a trinket or consumable with healing or damaging effects. | 2 ||
| [`PyrophinasCollar`](#object-pyrophinascollar) | Object | Specifies Pyrophina's Collar, a trinket that enhances fire-related abilities. | 2 ||
| `QEVENT_OBELISK_QUES1` | Variable | Determines if the first Obelisk quest event has been completed. | 2 ||
| `QEVENT_THROBBINGARTERY_REW1` | Variable | Determines if the first Throbbing Artery reward event has been triggered. | 2 ||
| `QEVENT_THROBBINGARTERY_REW2` | Variable | Determines if the second Throbbing Artery reward event has been triggered. | 2 ||
| `QEVENT_VOLCANO_REW1` | Variable | Determines if the first Volcano reward event has been triggered. | 2 ||
| [`ReceiverAntenna`](#object-receiverantenna) | Object | Specifies the Receiver Antenna item, used for communication or quests. | 2 ||
| `resultBad` | Variable | Determines if the event outcome was bad, affecting subsequent choices or penalties. | 2 ||
| [`Rocks`](#object-rocks) | Object | Specifies the Rocks item, a common resource or trinket. | 2 ||
| [`scramble_abilities`](./Enums.md#enum-scramble_abilities) | Enum | Examples: `all` | 2 ||
| `set_age` | Integer | Examples: `1` | 2 ||
| [`SignalAmplifier`](#object-signalamplifier) | Object | Specifies the Signal Amplifier item, a trinket that boosts area or communication effects. | 2 ||
| [`Snake`](Engine_LogicKeys.md#object-snake) | Integer / Object | Applies or references the 'Snake' effect/state. | 2 ||
| [`ThrobbingGristle`](#object-throbbinggristle) | Object | Specifies the Throbbing Gristle item, a flesh-based trinket or resource. | 2 ||
| [`TransmitterAntenna`](#object-transmitterantenna) | Object | Specifies the Transmitter Antenna item, used for communication or quests. | 2 ||
| [`ZaratanasCollar`](#object-zaratanascollar) | Object | Specifies Zaratana's Collar, a trinket that enhances earth or defensive abilities. | 2 ||
| [`CryogenicTimeChamber_Empty`](#object-cryogenictimechamber_empty) | Object | Specifies the empty Cryogenic Time Chamber, a location or item used for revival or freezing. | 2 ||
| [`EnchantingPoop`](#object-enchantingpoop) | Object | Specifies the Enchanting Poop item, a fecal trinket with beneficial or enchanting properties. | 2 ||
| [`general_common`](./Enums.md#enum-general_common) | Enum | `auto` | 2 ||
| [`general_rare`](./Enums.md#enum-general_rare) | Enum | `auto` | 2 ||
| [`GuillotinasHead`](#object-guillotinashead) | Object | Specifies Guillotina's Head, a trinket that triggers execution or decapitation effects. | 2 ||
| [`MomsKnife`](#object-momsknife) | Object | Specifies Mom's Knife, a trinket that increases damage or enables ricochet attacks. | 2 ||
| [`RaptorEgg`](Engine_LogicKeys.md#object-raptoregg) | Object | Examples: `.1` | 2 ||
| [`StatusDamagers`](Miscellaneous.md#object-statusdamagers) | Object | Event Trigger: Applies nested statuses to damagers. | 2 ||
| [`self_status_next_fight`](Events_and_Encounters.md#object-self_status_next_fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 1 ||
| [`injury`](./Enums.md#enum-injury) | Enum | Examples: `random` | 1 ||
| [`gain_disorder_from_pool`](./Enums.md#enum-gain_disorder_from_pool) | Enum | Examples: `Crazy_disorders` | 1 ||
| [`conditional_reward`](Events_and_Encounters.md#object-conditional_reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 1 ||
| `random_mutation` | Integer | Event Reward: Applies a completely random mutation to a character. | 1 ||
| `next_event_bonus` | Integer | Examples: `2` | 1 ||
| `party_heal` | Integer | Examples: `10` | 1 ||
| [`mutation`](Events_and_Encounters.md#object-mutation) | Object | Event Object: Story branch or dialog option representing the 'Mutation' action. | 1 ||
| `cutscene` | String | Event Object: Triggers a narrative cutscene. | 1 ||
| `random` | Number | Examples: `4` | 1 ||
| `ally_ambush_next_fights` | Integer | Examples: `1` | 1 ||
| `gain_cat_familiar` | Integer | Examples: `1` | 1 ||
| `AdventureToken_HasRunFromDeath` | Variable | Determines if the unit has already run from death in the adventure. | 1 ||
| `AdventureToken_MysteriousCave_FamiliarVoice` | Variable | Determines if the unit has heard the familiar voice in the Mysterious Cave. | 1 ||
| `AdventureToken_MysteriousJarRepeat` | Variable | Determines if the Mysterious Jar encounter has been repeated. | 1 ||
| `AdventureToken_StevenTryAgain` | Variable | Determines if the Steven retry attempt has been made. | 1 ||
| `AdventureToken_StevenTryAgain2` | Variable | Determines if the second Steven retry attempt has been made. | 1 ||
| `AdventureToken_StevenTryAgain3` | Variable | Determines if the third Steven retry attempt has been made. | 1 ||
| `AdventureToken_TrippedOnBigToe` | Variable | Determines if the unit has tripped on their big toe in the adventure. | 1 ||
| `AdventureToken_UnmarkedGraveForced` | Variable | Determines if the unit was forced to discover the unmarked grave. | 1 ||
| [`Albinism`](#object-albinism) | Variable | Specifies the Albinism disorder, which causes a unit to have pale skin and sun-sensitivity effects. | 1 ||
| [`AlienOvergrowth`](#object-alienovergrowth) | Variable | A weather event that causes volcanic spawns on battle start. | 1 ||
| [`ambush`](./Math_Equations.md) | Equation | Examples: `"events/chupacabra.lvl"` | 1 ||
| `AntennaQuest_Orb` | Variable | A status flag indicating the Orb antenna quest is active. | 1 ||
| `AntennaQuest_Rift` | Variable | A status flag indicating the Rift antenna quest is active. | 1 ||
| `AntennaQuest_Volcano` | Variable | A status flag indicating the Volcano antenna quest is active. | 1 ||
| [`Beepis`](#object-beepis) | Object | An object definition for the Beepis item, entity, or character. | 1 ||
| [`bleeding`](#object-bleeding) | Variable | A status effect that deals damage over time to the affected unit. | 1 ||
| `bloody_items` | Variable | Determines which items are categorized as 'bloody' for interactions or drops. | 1 ||
| [`BrainDamage`](#object-braindamage) | Variable | A disorder or status that reduces the unit's intelligence or mental stats. | 1 ||
| [`BrainDead`](#object-braindead) | Variable | A disorder granted by a Monkey Paw wish that severely impairs the unit's mental faculties. | 1 ||
| [`Brave`](#object-brave) | Variable | A disorder that grants the unit passive benefits related to courage or resistance. | 1 ||
| [`burned`](#object-burned) | Variable | A status effect that deals fire damage over time to the affected unit. | 1 ||
| [`CharmedTarBaby`](#object-charmedtarbaby) | Object | An allied variant of TarBaby that fights for the player's faction. | 1 ||
| `clone_self_to_party` | Integer | Examples: `1` | 1 ||
| `copy_items_to_party` | Integer | Examples: `1` | 1 ||
| `copy_party_items` | Integer | Examples: `1` | 1 ||
| [`Cunch`](#object-cunch) | Object | An object definition for the Cunch item, entity, or character. | 1 ||
| [`CursedStickman`](#object-cursedstickman) | Object | A cursed trinket item variant of Stickman. | 1 ||
| [`DeathsScythe`](#object-deathsscythe) | Object | An object definition for the DeathsScythe item, entity, or character. | 1 ||
| `dimensionx.gon` | Variable | A variable referencing the Dimension X map or event file. | 1 ||
| `EVENT_USETHETOILET_AGAIN` | Variable | A variable flag that tracks whether the 'Use the Toilet' event has been triggered again. | 1 ||
| [`FecalHood_Cursed`](#object-fecalhood_cursed) | Object | A cursed variant of the FecalHood item. | 1 ||
| [`FecalMask_Cursed`](#object-fecalmask_cursed) | Object | A cursed variant of the FecalMask item. | 1 ||
| [`Feebis`](#object-feebis) | Object | An object definition for the Feebis item, entity, or character. | 1 ||
| [`gain_clone_familiar`](Events_and_Encounters.md#object-gain_clone_familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 1 ||
| [`GeomagneticStorm`](#object-geomagneticstorm) | Variable | A weather event that applies a status effect to all characters at round end. | 1 ||
| [`get_full_item_set_from_pool`](./Enums.md#enum-get_full_item_set_from_pool) | Enum | Examples: `common` | 1 ||
| [`Gigachad`](#object-gigachad) | Variable | A disorder that grants the unit significant stat boosts. | 1 ||
| `godly_items` | Variable | Determines which items are categorized as 'godly' for interactions or drops. | 1 ||
| `grass_items` | Variable | Determines which items are categorized as 'grass' for interactions or drops. | 1 ||
| `hide_items` | Variable | Determines which items are categorized as 'hide' for interactions or drops. | 1 ||
| [`Host`](#object-host) | Object | An object definition for the Host entity, likely a carrier for a parasite or symbiont. | 1 ||
| `iceage.gon` | Variable | A variable referencing the Ice Age map or event file. | 1 ||
| `junkyard_items` | Variable | Determines which items are categorized as 'junkyard' for interactions or drops. | 1 ||
| [`legacy_event_unlock_momsknife`](#object-legacy_event_unlock_momsknife) | Variable | A sequence that unlocks the MomsKnife item and displays an unlock popup. | 1 ||
| [`lose_all_equipped_items`](./Enums.md#enum-lose_all_equipped_items) | Enum | Examples: `cat` | 1 ||
| [`map_unlock_iceage`](#object-map_unlock_iceage) | Variable | A sequence that unlocks the Ice Age area and displays an unlock popup. | 1 ||
| `mapflag_ChaosAntennaAttached` | Variable | A flag indicating the Chaos antenna has been attached to the map. | 1 ||
| `mapflag_OrbAntennaAttached` | Variable | A flag indicating the Orb antenna has been attached to the map. | 1 ||
| `mapflag_ThrobbingArteryDone` | Variable | A flag indicating the Throbbing Artery event or encounter has been completed. | 1 ||
| `mapflag_VolcanoAntennaAttached` | Variable | A flag indicating the Volcano antenna has been attached to the map. | 1 ||
| `mapflag_WallOfFleshDone` | Variable | A flag indicating the Wall of Flesh event or encounter has been completed. | 1 ||
| [`meat_world_open`](#object-meat_world_open) | Variable | A sequence that sets the map generation flag for full Meat World unlock. | 1 ||
| `MeatWorldQuest_Gristle` | Variable | A variable representing the Gristle quest within the Meat World area. | 1 ||
| `MeatWorldQuest_Leech` | Variable | A variable representing the Leech quest within the Meat World area. | 1 ||
| `MeteorShowerUnlocked` | Variable | A flag indicating the Meteor Shower event or ability has been unlocked. | 1 ||
| `monkey_paw_1finger` | Variable | A variable tracking the state of the Monkey Paw with one finger remaining. | 1 ||
| `monkey_paw_2fingers` | Variable | A variable tracking the state of the Monkey Paw with two fingers remaining. | 1 ||
| `monkey_paw_3fingers` | Variable | A variable tracking the state of the Monkey Paw with three fingers remaining. | 1 ||
| `monkey_paw_4fingers` | Variable | A variable tracking the state of the Monkey Paw with four fingers remaining. | 1 ||
| [`MysteriousTomb1`](#object-mysterioustomb1) | Variable | A variable representing the first Mysterious Tomb event or location. | 1 ||
| [`MysteriousTomb2`](#object-mysterioustomb2) | Variable | A variable representing the second Mysterious Tomb event or location. | 1 ||
| [`party_injury`](./Enums.md#enum-party_injury) | Enum | Examples: `random` | 1 ||
| [`play_result_animation`](./Enums.md#enum-play_result_animation) | Enum | Examples: `resultVeryGood` | 1 ||
| [`PuncturedEye`](#object-puncturedeye) | Variable | A status effect or injury that impairs the unit's vision or accuracy. | 1 ||
| `QEVENT_BROKENTIMEMACHINE_QUES` | Variable | A quest flag for the Broken Time Machine quest chain. | 1 ||
| `QEVENT_BROKENTIMEMACHINE_REW2` | Variable | A reward flag for the second stage of the Broken Time Machine quest chain. | 1 ||
| `QEVENT_BROKENTIMEMACHINE_REW3` | Variable | A reward flag for the third stage of the Broken Time Machine quest chain. | 1 ||
| `QEVENT_BROKENTIMEMACHINE_REW4` | Variable | A reward flag for the fourth stage of the Broken Time Machine quest chain. | 1 ||
| `QEVENT_BROKENTIMEMACHINE_REW5` | Variable | A variable used to track the state or availability of the fifth reward for the broken time machine event. | 1 ||
| `QEVENT_DEADGOD_QUES` | Variable | A variable that controls the quest state for the dead god event. | 1 ||
| `QEVENT_DEADGOD_REW1` | Variable | A variable that controls the state or availability of the first reward for the dead god event. | 1 ||
| `QEVENT_DEADGOD_REW2` | Variable | A variable that controls the state or availability of the second reward for the dead god event. | 1 ||
| `QEVENT_DEADGOD_REW3` | Variable | A variable that controls the state or availability of the third reward for the dead god event. | 1 ||
| `QEVENT_DEADKING_QUES` | Variable | A variable that controls the quest state for the dead king event. | 1 ||
| `QEVENT_DEADKING_REW1` | Variable | A variable that controls the state or availability of the first reward for the dead king event. | 1 ||
| `QEVENT_DEADKING_REW2` | Variable | A variable that controls the state or availability of the second reward for the dead king event. | 1 ||
| `QEVENT_DEADKING_REW3` | Variable | A variable that controls the state or availability of the third reward for the dead king event. | 1 ||
| `QEVENT_DEADKING_REW4` | Variable | A variable that controls the state or availability of the fourth reward for the dead king event. | 1 ||
| `QEVENT_DEADKING_REW5` | Variable | A variable that controls the state or availability of the fifth reward for the dead king event. | 1 ||
| `QEVENT_DIMENSIONXPORTAL_ENTER_REW` | Variable | A variable that controls the reward state for entering the dimension X portal. | 1 ||
| `QEVENT_DIMENSIONXPORTAL_IGNORE_ANSW` | Variable | A variable that controls the state for ignoring the answer from the dimension X portal event. | 1 ||
| `QEVENT_DIMENSIONXPORTAL_QUES` | Variable | A variable that controls the quest state for the dimension X portal event. | 1 ||
| `QEVENT_GLOWINGORB_QUES` | Variable | A variable that controls the quest state for the glowing orb event. | 1 ||
| `QEVENT_GLOWINGORB_QUES2` | Variable | A variable that controls the secondary quest state for the glowing orb event. | 1 ||
| `QEVENT_GLOWINGORB_REW1` | Variable | A variable that controls the state or availability of the first reward for the glowing orb event. | 1 ||
| `QEVENT_GLOWINGORB_REW2` | Variable | A variable that controls the state or availability of the second reward for the glowing orb event. | 1 ||
| `QEVENT_GLOWINGORB_REW3` | Variable | A variable that controls the state or availability of the third reward for the glowing orb event. | 1 ||
| `QEVENT_GLOWINGORB_REW4` | Variable | A variable that controls the state or availability of the fourth reward for the glowing orb event. | 1 ||
| `QEVENT_GLOWINGORB_REW5` | Variable | A variable that controls the state or availability of the fifth reward for the glowing orb event. | 1 ||
| `QEVENT_GLOWINGORB_REW7` | Variable | A variable that controls the state or availability of the seventh reward for the glowing orb event. | 1 ||
| `QEVENT_MEATALTAR_QUES1` | Variable | A variable that controls the primary quest state for the meat altar event. | 1 ||
| `QEVENT_MEATALTAR_REW1` | Variable | A variable that controls the primary reward state for the meat altar event. | 1 ||
| `QEVENT_MEATALTAR_REW_IGNORE` | Variable | A variable that controls the reward state when the player ignores the meat altar event. | 1 ||
| `QEVENT_OBELISK_CORE_REW_ZARA3` | Variable | A variable controlling the third Zara reward state for the core obelisk event. | 1 ||
| `QEVENT_OBELISK_MOON_REW_PYRO3` | Variable | A variable controlling the third Pyro reward state for the moon obelisk event. | 1 ||
| `QEVENT_OBELISK_QUES3` | Variable | A variable that controls the tertiary quest state for the obelisk event. | 1 ||
| `QEVENT_THEHEAD_QUES` | Variable | A variable that controls the quest state for the head event. | 1 ||
| `QEVENT_THEHEAD_REW1` | Variable | A variable that controls the state or availability of the first reward for the head event. | 1 ||
| `QEVENT_THEHEAD_REW2` | Variable | A variable that controls the state or availability of the second reward for the head event. | 1 ||
| `QEVENT_THEHEAD_REW3` | Variable | A variable that controls the state or availability of the third reward for the head event. | 1 ||
| `QEVENT_THEHEAD_REW5` | Variable | A variable that controls the state or availability of the fifth reward for the head event. | 1 ||
| `QEVENT_THEHEAD_REW6` | Variable | A variable that controls the state or availability of the sixth reward for the head event. | 1 ||
| `QEVENT_THROBBINGARTERY2_QUES` | Variable | A variable that controls the quest state for the second throbbing artery event. | 1 ||
| `QEVENT_THROBBINGARTERY2_REW_IGNORE` | Variable | A variable that controls the reward state when the player ignores the second throbbing artery event. | 1 ||
| `QEVENT_THROBBINGARTERY_QUES1` | Variable | A variable that controls the primary quest state for the throbbing artery event. | 1 ||
| `QEVENT_THROBBINGARTERY_QUES2` | Variable | A variable that controls the secondary quest state for the throbbing artery event. | 1 ||
| `QEVENT_THROBBINGARTERY_REW5` | Variable | A variable that controls the state or availability of the fifth reward for the throbbing artery event. | 1 ||
| `QEVENT_THROBBINGARTERY_REW_IGNORE` | Variable | A variable that controls the reward state when the player ignores the throbbing artery event. | 1 ||
| `QEVENT_TIMEMACHINE_FUTURE_QUES` | Variable | A variable that controls the quest state for the time machine future event. | 1 ||
| `QEVENT_TIMEMACHINE_FUTURE_REW1` | Variable | A variable that controls the first reward state for the time machine future event. | 1 ||
| `QEVENT_TIMEMACHINE_FUTURE_REW2` | Variable | A variable that controls the second reward state for the time machine future event. | 1 ||
| `QEVENT_TIMEMACHINE_ICEAGE_QUES` | Variable | A variable that controls the quest state for the time machine ice age event. | 1 ||
| `QEVENT_TIMEMACHINE_ICEAGE_REW1` | Variable | A variable that controls the first reward state for the time machine ice age event. | 1 ||
| `QEVENT_TIMEMACHINE_ICEAGE_REW2` | Variable | A variable that controls the second reward state for the time machine ice age event. | 1 ||
| `QEVENT_TIMEMACHINE_JURASSIC_QUES` | Variable | A variable that controls the quest state for the time machine Jurassic event. | 1 ||
| `QEVENT_TIMEMACHINE_JURASSIC_REW1` | Variable | A variable that controls the first reward state for the time machine Jurassic event. | 1 ||
| `QEVENT_TIMEMACHINE_JURASSIC_REW2` | Variable | A variable that controls the second reward state for the time machine Jurassic event. | 1 ||
| `QEVENT_TIMEMACHINE_QUES` | Variable | A variable that controls the quest state for the time machine event. | 1 ||
| `QEVENT_TIMEMACHINE_REW1` | Variable | The first reward granted upon completing the time machine quest. | 1 ||
| `QEVENT_TIMEMACHINE_REW2` | Variable | The second reward granted upon completing the time machine quest. | 1 ||
| `QEVENT_TIMEMACHINE_REW3` | Variable | The third reward granted upon completing the time machine quest. | 1 ||
| `QEVENT_TIMEMACHINE_THEEND_QUES` | Variable | Quest objective related to the time machine "The End" variant. | 1 ||
| `QEVENT_TIMEMACHINE_THEEND_REW1` | Variable | The first reward for completing the time machine "The End" quest. | 1 ||
| `QEVENT_TIMEMACHINE_THEEND_REW2` | Variable | The second reward for completing the time machine "The End" quest. | 1 ||
| `QEVENT_VOLCANO_QUES` | Variable | Quest objective for the volcano event. | 1 ||
| `QEVENT_VOLCANO_QUES2` | Variable | Secondary quest objective for the volcano event. | 1 ||
| `QEVENT_VOLCANO_REW4` | Variable | The fourth reward for completing the volcano event quest. | 1 ||
| `QEVENT_VOLCANO_REW5` | Variable | The fifth reward for completing the volcano event quest. | 1 ||
| `QEVENT_VOLCANO_REW7` | Variable | The seventh reward for completing the volcano event quest. | 1 ||
| `QEVENT_WALLOFFLESH2_QUES` | Variable | Quest objective for the second wall of flesh event. | 1 ||
| `QEVENT_WALLOFFLESH2_REW_IGNORE` | Variable | A reward placeholder for the second wall of flesh event that is not awarded. | 1 ||
| `QEVENT_WALLOFFLESH_QUES1` | Variable | First quest objective for the wall of flesh event. | 1 ||
| `QEVENT_WALLOFFLESH_QUES2` | Variable | Second quest objective for the wall of flesh event. | 1 ||
| `QEVENT_WALLOFFLESH_REW1` | Variable | The first reward for completing the wall of flesh event quest. | 1 ||
| `QEVENT_WALLOFFLESH_REW10` | Variable | The tenth reward for completing the wall of flesh event quest. | 1 ||
| `QEVENT_WALLOFFLESH_REW2` | Variable | The second reward for completing the wall of flesh event quest. | 1 ||
| `QEVENT_WALLOFFLESH_REW3` | Variable | The third reward for completing the wall of flesh event quest. | 1 ||
| `QEVENT_WALLOFFLESH_REW4` | Variable | The fourth reward for completing the wall of flesh event quest. | 1 ||
| `QEVENT_WALLOFFLESH_REW5` | Variable | The fifth reward for completing the wall of flesh event quest. | 1 ||
| `QEVENT_WALLOFFLESH_REW7` | Variable | The seventh reward for completing the wall of flesh event quest. | 1 ||
| `QEVENT_WALLOFFLESH_REW8` | Variable | The eighth reward for completing the wall of flesh event quest. | 1 ||
| `QEVENT_WALLOFFLESH_REW9` | Variable | The ninth reward for completing the wall of flesh event quest. | 1 ||
| `QEVENT_WALLOFFLESH_REW_IGNORE` | Variable | A reward placeholder for the wall of flesh event that is not awarded. | 1 ||
| [`random_chance`](Events_and_Encounters.md#object-random_chance) | Object | Event Logic: Executes the nested outcome based on a percentage roll. | 1 ||
| `raptor_nest_eggs` | Variable | The number of eggs present in a raptor nest. | 1 ||
| `resultConfused` | Variable | Variable tracking a conflicting or inconclusive event outcome. | 1 ||
| `resultVeryBad` | Variable | Variable tracking a particularly negative event outcome. | 1 ||
| `rock_items` | Variable | A list of rock-type items (e.g., ores, gems) obtained from an event. | 1 ||
| [`scramble_basic_attack`](./Enums.md#enum-scramble_basic_attack) | Enum | Examples: `all` | 1 ||
| [`scramble_passives`](./Enums.md#enum-scramble_passives) | Enum | Examples: `all` | 1 ||
| [`select_item_from_pool_for_cutscene_only`](./Enums.md#enum-select_item_from_pool_for_cutscene_only) | Enum | Examples: `glitched_items` | 1 ||
| `self_heal` | Integer | Examples: `10` | 1 ||
| [`SludgeHat`](#object-sludgehat) | Object | A cosmetic hat item for a sludge-themed character. | 1 ||
| [`SludgeMask`](#object-sludgemask) | Object | A cosmetic mask item for a sludge-themed character. | 1 ||
| [`Soulless`](#object-soulless) | Variable | A disorder that removes or nullifies the unit's passive abilities. | 1 ||
| `Steven_disorders` | Variable | List of disorders associated with a character named Steven. | 1 ||
| [`StrangeEggs`](#object-strangeeggs) | Variable | A weather effect that spawns strange eggs on the battlefield at the start of combat. | 1 ||
| `tech_items` | Variable | A list of technology-themed items obtained from an event. | 1 ||
| `TheRift_UsedPyrophina` | Variable | Tracks whether the character Pyrophina was used in The Rift event. | 1 ||
| `TheRift_UsedZaratana` | Variable | Tracks whether the character Zaratana was used in The Rift event. | 1 ||
| [`TheShimmer`](#object-theshimmer) | Variable | A weather effect that applies a post-processing visual filter to the battlefield. | 1 ||
| [`time_machine_quest_finalstep`](#object-time_machine_quest_finalstep) | Variable | Triggers the NPC sequence for the final step of the time machine quest. | 1 ||
| [`time_machine_quest_trigger`](#object-time_machine_quest_trigger) | Variable | Triggers the initial NPC sequence to start the time machine quest. | 1 ||
| [`Touched`](#object-touched) | Variable | A disorder that modifies the unit's stats. | 1 ||
| `trigger_butterfly_effect` | Integer | Examples: `1` | 1 ||
| `WorldEventLegacyCounter_SealedCrypt` | Variable | Counter tracking the number of times the Sealed Crypt event has been triggered across legacies. | 1 ||
| `WorldEventLegacyToken_CryptOpened` | Variable | Legacy token indicating that the crypt has been opened in this run. | 1 ||
| `WorldEventLegacyToken_HasRunFromDeath` | Variable | Legacy token indicating that the unit has fled from death in this run. | 1 ||
| `WorldEventLegacyToken_MomsKnife` | Variable | Legacy token for obtaining Mom's Knife item in this run. | 1 ||
| `WorldEventLegacyToken_MonkeyPaw1` | Variable | First stage of the Monkey Paw legacy token tracking wishes used. | 1 ||
| `WorldEventLegacyToken_MonkeyPaw2` | Variable | Second stage of the Monkey Paw legacy token tracking wishes used. | 1 ||
| `WorldEventLegacyToken_MonkeyPaw3` | Variable | Third stage of the Monkey Paw legacy token tracking wishes used. | 1 ||
| `WorldEventLegacyToken_MonkeyPaw4` | Variable | Fourth stage of the Monkey Paw legacy token tracking wishes used. | 1 ||
| `WorldEventLegacyToken_MonkeyPawGenes` | Variable | Legacy token tracking the number of gene mutations gained from the Monkey Paw event. | 1 ||
| `WorldEventLegacyToken_MonkeyPawItems` | Variable | A reference to the legacy currency or token related to Monkey Paw items. | 1 ||
| `WorldEventLegacyToken_MonkeyPawKnowledge` | Variable | A reference to the legacy currency or token related to Monkey Paw knowledge. | 1 ||
| `WorldEventLegacyToken_MonkeyPawStrength` | Variable | A reference to the legacy currency or token related to Monkey Paw strength. | 1 ||
| `WorldEventLegacyToken_StacyMutant` | Variable | A reference to the legacy currency or token related to Stacy Mutant. | 1 ||
| `spawn_reflection_next_fight` | Number | Event Penalty: Spawns dark clones/reflections of the party in the next combat encounter. | 0 ||
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
| [`prompt`](./Enums.md#enum-prompt) | String | Examples: `"woah", "EVENT_TRASHBIN_REW3", "EVENT_ABEGGAR_REW2"` | 38 ||
| `set_frame` | Integer | Examples: `4, 2, 5` | 36 ||
| [`permanent_stats`](Events_and_Encounters.md#object-permanent_stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 7 ||
| [`play_animation`](./Arrays.md#array-play_animation) | Array / Enum | Examples: `resultVeryGood, resultBad` | 5 ||
| [`reward`](Events_and_Encounters.md#object-reward) | Object | Event Object: Story branch or dialog option representing the 'Reward' action. | 5 ||
| [`kill`](./Enums.md#enum-kill) | Enum | Examples: `cat` | 4 ||
| [`event_now`](./Enums.md#enum-event_now) | Enum | Examples: `MeatGolem` | 3 ||
| [`event_now_same_cat`](./Enums.md#enum-event_now_same_cat) | Enum | Examples: `BigToe, SpookieApparation, CatHole` | 3 ||
| [`battle`](./Math_Equations.md) | String | Examples: `{ ... }` | 2 ||
| [`get_parasite_from_pool`](./Enums.md#enum-get_parasite_from_pool) | Enum | Examples: `cursed_items, parasites` | 2 ||
| [`conditional_reward`](Events_and_Encounters.md#object-conditional_reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 1 ||
| [`cutscene`](Events_and_Encounters.md#object-cutscene) | Object | Event Object: Triggers a narrative cutscene. | 1 ||
| [`gain_disorder_from_pool`](./Enums.md#enum-gain_disorder_from_pool) | Enum | Examples: `Crazy_disorders` | 1 ||
| [`gain_immortal_familiar`](./Enums.md#enum-gain_immortal_familiar) | Enum | Examples: `CharmedFleaSpecial` | 1 ||
| [`get_parasite`](./Enums.md#enum-get_parasite) | Enum | Examples: `FaceShards, BigToeCursed, MetalRod` | 1 ||
| [`injury`](./Enums.md#enum-injury) | Enum | Examples: `random` | 1 ||
| [`lose_item`](./Enums.md#enum-lose_item) | Enum | Examples: `equipped, inventory` | 1 ||
| `next_event_bonus` | Integer | Examples: `2` | 1 ||
| [`party_random_mutation_from_set`](Events_and_Encounters.md#object-party_random_mutation_from_set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 1 ||
| [`select_item_from_pool_for_cutscene_only`](./Enums.md#enum-select_item_from_pool_for_cutscene_only) | Enum | Examples: `glitched_items` | 1 ||
| [`self_status_next_fight`](Events_and_Encounters.md#object-self_status_next_fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 1 ||
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum | Examples: `WorldEventLegacyToken_CryptOpened` | 1 ||

</details>

---

#### `common`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1197

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`self_damage`](Abilities_and_Spells.md#object-self_damage) | Boolean / Integer / Object | A damage instance object that applies damage and effects to the source unit itself. | 436 | `[4 8]` (Array), `[5 10]` (Array), `50` (Number), `8` (Number) |
| [`prompt`](./Enums.md#enum-prompt) | String | Examples: `"woah", "EVENT_TRASHBIN_REW3", "EVENT_ABEGGAR_REW2"` | 38 ||
| `set_frame` | Integer | Examples: `4, 2, 5` | 36 ||
| [`clear_adventure_token`](./Enums.md#enum-clear_adventure_token) | Enum | Examples: `AdventureToken_BlueNeedle, AdventureToken_HasTakenNeedle, AdventureToken_RedN...` | 24 ||
| [`event_now_same_cat`](./Enums.md#enum-event_now_same_cat) | Enum | Examples: `BigToe, SpookieApparation, CatHole` | 21 ||
| [`spawn_unit_next_fight`](Events_and_Encounters.md#object-spawn_unit_next_fight) | Object | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. | 18 ||
| [`get_item`](./Enums.md#enum-get_item) | Enum | Examples: `BrokenWindow` | 14 ||
| [`play_animation`](./Arrays.md#array-play_animation) | Array / Enum | Examples: `resultVeryGood, resultBad` | 13 ||
| [`gain_disorder`](./Enums.md#enum-gain_disorder) | Enum | Examples: `BorrowedTime, Brave, Dyslexia` | 12 ||
| [`get_item_from_pool`](Events_and_Encounters.md#object-get_item_from_pool) | Array / Enum / Object | Event Action: Rewards the player with an item drawn from a specific loot pool. | 11 ||
| `override_end_option_prompt` | String | Examples: `"EVENT_MYSTERIOUSSTRANGER_END_AGAIN2", "EVENT_LOCKEDDOOR_PROMPT2", "EVENT_MYS...` | 11 ||
| [`party_status_next_fight`](Events_and_Encounters.md#object-party_status_next_fight) | Object | Event Penalty/Reward: Applies a status effect to the entire party at the start of the next combat encounter. | 11 ||
| `full_heal` | Integer | Examples: `1` | 10 ||
| `ambush_next_basic_fights` | Integer | Examples: `1` | 9 ||
| [`party_damage`](./Arrays.md#array-party_damage) | Array / Number | Examples: `[ 5 10 ]` | 9 ||
| [`set_adventure_token`](./Enums.md#enum-set_adventure_token) | Enum | Examples: `AdventureToken_Mirage2, AdventureToken_StevenTryAgain3, HasPlayedMysteriousSt...` | 9 ||
| [`random_mutation_from_set`](Events_and_Encounters.md#object-random_mutation_from_set) | Number / Object | Event Reward: Applies a random mutation to a character from a specific pool. | 8 ||
| [`get_parasite`](./Enums.md#enum-get_parasite) | Enum | Examples: `FaceShards, BigToeCursed, MetalRod` | 7 ||
| [`permanent_stats`](Events_and_Encounters.md#object-permanent_stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 7 ||
| [`gain_coins`](./Arrays.md#array-gain_coins) | Array / Number | Examples: `[ 4 15 ], 5` | 6 ||
| [`global_effect_next_fight`](Events_and_Encounters.md#object-global_effect_next_fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 6 ||
| [`increment_legacy_counter`](./Enums.md#enum-increment_legacy_counter) | Enum | Examples: `WorldEventLegacyToken_StartDigging, WorldEventLegacyCounter_CrackInTheWall, W...` | 6 ||
| [`add_weather`](./Enums.md#enum-add_weather) | Enum | Examples: `TheShimmer, SolarFlare, GeomagneticStorm` | 5 ||
| [`kill`](./Enums.md#enum-kill) | Enum | Examples: `cat` | 5 ||
| [`lose_item`](./Enums.md#enum-lose_item) | Enum | Examples: `equipped, inventory` | 5 ||
| [`shop_now`](./Enums.md#enum-shop_now) | Enum | Examples: `TreasureHard, Event_SmallShop, Event_RareShop` | 5 ||
| [`spin`](./Enums.md#enum-spin) | Enum | Examples: `again` | 4 ||
| [`gain_familiar`](Events_and_Encounters.md#object-gain_familiar) | Enum / Object | Event Action: Adds a specific familiar to the party. | 3 ||
| [`gain_food`](./Arrays.md#array-gain_food) | Array / Number | Examples: `[ 5 10 ]` | 3 ||
| `damage` | Array / Equation | The damage dealt, which can be a numeric value, a formula string, or a defined damage object. | 2 | `[3 6]` (Array), `[5 10]` (Array), `8` (Equation), `5` (Equation) |
| [`event_now`](./Enums.md#enum-event_now) | Enum | Examples: `MeatGolem` | 2 ||
| [`get_parasite_from_pool`](./Enums.md#enum-get_parasite_from_pool) | Array / Enum | Examples: `cursed_items, parasites` | 2 ||
| [`lose_specific_item`](./Enums.md#enum-lose_specific_item) | Enum | Examples: `SlagTight` | 2 ||
| [`next_event_from_set`](Events_and_Encounters.md#object-next_event_from_set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 2 ||
| `party_heal_disorder` | Integer | Examples: `2` | 2 ||
| [`party_permanent_stats_exclude_self`](Events_and_Encounters.md#object-party_permanent_stats_exclude_self) | Object | Event Reward: Permanently modifies stats for all party members except the one who initiated the action. | 2 ||
| `ally_ambush_next_fights` | Integer | Examples: `1` | 1 ||
| `clear_result_animation` | Integer | Examples: `1` | 1 ||
| [`conditional_reward`](Events_and_Encounters.md#object-conditional_reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 1 ||
| [`decrement_legacy_counter`](./Enums.md#enum-decrement_legacy_counter) | Enum | Examples: `WorldEventLegacyToken_StartDigging, WorldEventLegacyCounter_CrackInTheWall` | 1 ||
| [`gain_disorder_from_pool`](./Enums.md#enum-gain_disorder_from_pool) | Array / Enum | Examples: `Crazy_disorders` | 1 ||
| [`get_and_equip_item`](./Enums.md#enum-get_and_equip_item) | Enum | Examples: `FlyLarva` | 1 ||
| `heal_disorder` | Integer | Examples: `2` | 1 ||
| `heal_injury` | Integer | Examples: `1` | 1 ||
| [`injury`](./Enums.md#enum-injury) | Enum | Examples: `random` | 1 ||
| [`learn_ability_from_pool`](./Enums.md#enum-learn_ability_from_pool) | Enum | Examples: `Necromancer` | 1 ||
| [`mutation`](Events_and_Encounters.md#object-mutation) | Object | Event Object: Story branch or dialog option representing the 'Mutation' action. | 1 ||
| `next_event_bonus` | Integer | Examples: `2` | 1 ||
| `party_heal` | Integer | Examples: `10` | 1 ||
| `random_mutation` | Integer | Event Reward: Applies a completely random mutation to a character. | 1 ||
| `self_heal` | Integer | Examples: `10` | 1 ||
| [`self_status_next_fight`](Events_and_Encounters.md#object-self_status_next_fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 1 ||
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum | Examples: `WorldEventLegacyToken_CryptOpened` | 1 ||
| [`upgrade_ability`](./Enums.md#enum-upgrade_ability) | Enum | Examples: `random` | 1 ||
| [`random_pool`](./Arrays.md#array-random_pool) | Array | Examples: `[ { weight 90 prompt "EVENT_ABEGGAR_REW1" set_frame 3 ran..., [ { weight 85 p...` | 0 ||

</details>

---

#### `good`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 572

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`rare`](./Enums.md#enum-rare) | Enum | Event Object: Story branch or dialog option representing the 'Rare' action. | 673 ||
| [`increment_legacy_counter`](./Enums.md#enum-increment_legacy_counter) | Enum | Examples: `WorldEventLegacyToken_StartDigging, WorldEventLegacyCounter_CrackInTheWall, W...` | 52 ||
| [`prompt`](./Enums.md#enum-prompt) | String | Examples: `"woah", "EVENT_TRASHBIN_REW3", "EVENT_ABEGGAR_REW2"` | 38 ||
| `set_frame` | Integer | Examples: `4, 2, 5` | 36 ||
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum | Examples: `WorldEventLegacyToken_CryptOpened` | 26 ||
| [`play_animation`](./Enums.md#enum-play_animation) | Array / Enum | Examples: `resultVeryGood, resultBad` | 20 ||
| [`complete_item_quest`](./Enums.md#enum-complete_item_quest) | Enum | Examples: `BlackShard, JarOfRadiation, ScaldingOrb` | 18 ||
| [`begin_chapter`](./Enums.md#enum-begin_chapter) | Enum | Examples: `iceage.gon, dimensionx.gon, future.gon` | 12 ||
| [`set_adventure_token`](./Enums.md#enum-set_adventure_token) | Enum | Examples: `AdventureToken_Mirage2, AdventureToken_StevenTryAgain3, HasPlayedMysteriousSt...` | 12 ||
| [`get_item_from_pool`](./Enums.md#enum-get_item_from_pool) | Enum | Event Action: Rewards the player with an item drawn from a specific loot pool. | 11 ||
| [`event_now`](./Enums.md#enum-event_now) | Enum | Examples: `MeatGolem` | 9 ||
| [`event_now_same_cat`](./Enums.md#enum-event_now_same_cat) | Enum | Examples: `BigToe, SpookieApparation, CatHole` | 9 ||
| [`gain_disorder`](./Enums.md#enum-gain_disorder) | Enum | Examples: `BorrowedTime, Brave, Dyslexia` | 8 ||
| [`lose_specific_item`](./Enums.md#enum-lose_specific_item) | Enum | Examples: `SlagTight` | 8 ||
| [`trigger_adventure_unlock`](./Enums.md#enum-trigger_adventure_unlock) | Enum | Examples: `end_of_time_unlock, meat_world_unlock` | 7 ||
| [`add_weather`](./Enums.md#enum-add_weather) | Enum | Examples: `TheShimmer, SolarFlare, GeomagneticStorm` | 5 ||
| [`get_item`](./Enums.md#enum-get_item) | Enum | Examples: `BrokenWindow` | 5 ||
| `heal_disorder` | Enum / Number | Examples: `2` | 5 ||
| [`reward`](Events_and_Encounters.md#object-reward) | Object | Event Object: Story branch or dialog option representing the 'Reward' action. | 5 ||
| [`get_parasite`](./Enums.md#enum-get_parasite) | Enum | Examples: `FaceShards, BigToeCursed, MetalRod` | 3 ||
| `heal_injury` | Integer | Examples: `1` | 3 ||
| [`kill`](./Enums.md#enum-kill) | Enum | Examples: `cat` | 3 ||
| [`unlock_item_quest`](./Enums.md#enum-unlock_item_quest) | Enum | Examples: `CryogenicTimeChamber_Full, JarOfChaos, JarOfRadiatedBlood` | 3 ||
| [`clear_surviving_kaiju`](./Enums.md#enum-clear_surviving_kaiju) | Enum | Examples: `pyrophina, zaratana` | 2 ||
| [`cutscene_on_exit`](./Enums.md#enum-cutscene_on_exit) | Enum / Object | Examples: `infinite_intro` | 2 ||
| `full_heal` | Integer | Examples: `1` | 2 ||
| [`level_up`](./Enums.md#enum-level_up) | Enum | Examples: `all, self` | 2 ||
| `override_end_option_prompt` | String | Examples: `"EVENT_MYSTERIOUSSTRANGER_END_AGAIN2", "EVENT_LOCKEDDOOR_PROMPT2", "EVENT_MYS...` | 2 ||
| `ally_ambush_next_fights` | Integer | Examples: `1` | 1 ||
| `clone_self_to_party` | Integer | Examples: `1` | 1 ||
| [`conditional_reward`](Events_and_Encounters.md#object-conditional_reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 1 ||
| `copy_items_to_party` | Integer | Examples: `1` | 1 ||
| `copy_party_items` | Integer | Examples: `1` | 1 ||
| `cutscene` | String | Event Object: Triggers a narrative cutscene. | 1 ||
| [`gain_clone_familiar`](Events_and_Encounters.md#object-gain_clone_familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 1 ||
| [`gain_disorder_from_pool`](./Enums.md#enum-gain_disorder_from_pool) | Enum | Examples: `Crazy_disorders` | 1 ||
| [`get_full_item_set_from_pool`](./Enums.md#enum-get_full_item_set_from_pool) | Enum | Examples: `common` | 1 ||
| [`global_effect_next_fight`](Events_and_Encounters.md#object-global_effect_next_fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 1 ||
| [`injury`](./Enums.md#enum-injury) | Enum | Examples: `random` | 1 ||
| [`learn_ability_from_pool`](./Arrays.md#array-learn_ability_from_pool) | Array / Enum | Examples: `Necromancer` | 1 ||
| [`learn_passive_from_pool`](./Arrays.md#array-learn_passive_from_pool) | Array / Enum | Examples: `AnyUnlocked` | 1 ||
| [`lose_item`](./Enums.md#enum-lose_item) | Enum | Examples: `equipped, inventory` | 1 ||
| [`mutation`](Events_and_Encounters.md#object-mutation) | Object | Event Object: Story branch or dialog option representing the 'Mutation' action. | 1 ||
| `next_event_bonus` | Integer | Examples: `2` | 1 ||
| [`next_event_from_set`](Events_and_Encounters.md#object-next_event_from_set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 1 ||
| [`random_mutation`](Events_and_Encounters.md#object-random_mutation) | Number / Object | Event Reward: Applies a completely random mutation to a character. | 1 ||
| [`scramble_abilities`](./Enums.md#enum-scramble_abilities) | Enum | Examples: `all` | 1 ||
| [`scramble_passives`](./Enums.md#enum-scramble_passives) | Enum | Examples: `all` | 1 ||
| [`shop_now`](./Enums.md#enum-shop_now) | Enum | Examples: `TreasureHard, Event_SmallShop, Event_RareShop` | 1 ||
| `trigger_butterfly_effect` | Integer | Examples: `1` | 1 ||
| [`upgrade_ability`](./Enums.md#enum-upgrade_ability) | Enum | Examples: `random` | 1 ||
| [`upgrade_passive`](./Enums.md#enum-upgrade_passive) | Enum | Examples: `random` | 1 ||
| [`gain_food`](./Arrays.md#array-gain_food) | Array | Examples: `[ 5 10 ]` | 0 ||
| [`party_gain_disorder_from_pool`](./Arrays.md#array-party_gain_disorder_from_pool) | Array | Examples: `[ Dwarfism ], [ Gigantism ]` | 0 ||
| [`random_pool`](./Arrays.md#array-random_pool) | Array | Examples: `[ { weight 90 prompt "EVENT_ABEGGAR_REW1" set_frame 3 ran..., [ { weight 85 p...` | 0 ||
| [`random_pool_consider_luck`](./Arrays.md#array-random_pool_consider_luck) | Array | Examples: `[ { prompt "EVENT_TRACY_REW11" weight 1 get_item_from_poo..., [ { prompt "EVE...` | 0 ||
| [`transform_item`](./Arrays.md#array-transform_item) | Array | Examples: `[ CryogenicTimeChamber_Empty CryogenicTimeChamber_Full ], [ JarOfRadiation Ja...` | 0 ||

</details>

---

#### `main`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 215

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`rare`](./Enums.md#enum-rare) | Enum | Event Object: Story branch or dialog option representing the 'Rare' action. | 673 ||
| [`options`](./Arrays.md#array-options) | Array | Event Object: Lists the available clickable dialog choices for the current story node. | 210 ||
| [`prompt`](./Enums.md#enum-prompt) | String | Examples: `"woah", "EVENT_TRASHBIN_REW3", "EVENT_ABEGGAR_REW2"` | 38 ||
| `set_frame` | Integer | Examples: `4, 2, 5` | 36 ||
| [`setup`](Events_and_Encounters.md#object-setup) | Object | Event Object: Pre-initialization logic executed before the event UI is drawn. | 23 ||
| [`bad`](Events_and_Encounters.md#object-bad) | Object | Event Object: Story branch or dialog option representing the 'Bad' action. | 10 ||
| [`weight`](./Enums.md#enum-weight) | Float | Probability weight for this outcome. | 10 ||
| [`add_weather`](./Enums.md#enum-add_weather) | Enum | Examples: `TheShimmer, SolarFlare, GeomagneticStorm` | 5 ||
| [`requires_flag`](./Enums.md#enum-requires_flag) | Enum | Prerequisite: Must meet this condition. | 5 ||
| [`goto`](./Enums.md#enum-goto) | Enum | Examples: `end` | 4 ||
| [`outcome`](Events_and_Encounters.md#object-outcome) | Object | Event Object: Logic and text executed after selecting a specific dialog option. | 4 ||
| [`gain_familiar`](./Enums.md#enum-gain_familiar) | Enum | Event Action: Adds a specific familiar to the party. | 3 ||
| `max_options` | Integer | Examples: `3, 2` | 3 ||
| `shuffle_options` | Boolean | Examples: `true` | 3 ||
| [`next_event_from_set`](./Enums.md#enum-next_event_from_set) | Enum | Event Action: Chains immediately into a randomly selected subsequent story event. | 1 ||
| `party_heal` | Integer | Examples: `10` | 1 ||
| [`party_permanent_stats`](Events_and_Encounters.md#object-party_permanent_stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of all party members. | 1 ||
| [`play_animation`](./Arrays.md#array-play_animation) | Array | Examples: `resultVeryGood, resultBad` | 1 ||
| [`self_status_next_fight`](Events_and_Encounters.md#object-self_status_next_fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 1 ||
| [`shop_now`](./Enums.md#enum-shop_now) | Enum | Examples: `TreasureHard, Event_SmallShop, Event_RareShop` | 1 ||

</details>

---

#### `rare`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 996

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`self_damage`](Abilities_and_Spells.md#object-self_damage) | Boolean / Integer / Object | A damage instance object that applies damage and effects to the source unit itself. | 436 | `[6 10]` (Array), `50` (Number), `10` (Number) |
| [`gain_disorder`](./Enums.md#enum-gain_disorder) | Enum | Examples: `BorrowedTime, Brave, Dyslexia` | 65 ||
| [`get_item`](./Enums.md#enum-get_item) | Enum | Examples: `BrokenWindow` | 41 ||
| [`prompt`](./Enums.md#enum-prompt) | String | Examples: `"woah", "EVENT_TRASHBIN_REW3", "EVENT_ABEGGAR_REW2"` | 38 ||
| `set_frame` | Integer | Examples: `4, 2, 5` | 36 ||
| [`event_now_same_cat`](./Enums.md#enum-event_now_same_cat) | Enum | Examples: `BigToe, SpookieApparation, CatHole` | 30 ||
| [`get_parasite`](./Enums.md#enum-get_parasite) | Enum | Examples: `FaceShards, BigToeCursed, MetalRod` | 30 ||
| [`set_adventure_token`](./Enums.md#enum-set_adventure_token) | Enum | Examples: `AdventureToken_Mirage2, AdventureToken_StevenTryAgain3, HasPlayedMysteriousSt...` | 22 ||
| [`spawn_unit_next_fight`](Events_and_Encounters.md#object-spawn_unit_next_fight) | Object | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. | 20 ||
| [`random_mutation_from_set`](Events_and_Encounters.md#object-random_mutation_from_set) | Number / Object | Event Reward: Applies a random mutation to a character from a specific pool. | 13 ||
| [`party_status_next_fight`](Events_and_Encounters.md#object-party_status_next_fight) | Object | Event Penalty/Reward: Applies a status effect to the entire party at the start of the next combat encounter. | 12 ||
| [`get_item_from_pool`](Events_and_Encounters.md#object-get_item_from_pool) | Array / Enum / Object | Event Action: Rewards the player with an item drawn from a specific loot pool. | 11 ||
| [`learn_passive`](./Enums.md#enum-learn_passive) | Enum | Examples: `CobraStyle, PoisonTips, DeathProof` | 10 ||
| [`play_animation`](./Arrays.md#array-play_animation) | Array / Enum | Examples: `resultVeryGood, resultBad` | 10 ||
| [`increment_legacy_counter`](./Enums.md#enum-increment_legacy_counter) | Enum | Examples: `WorldEventLegacyToken_StartDigging, WorldEventLegacyCounter_CrackInTheWall, W...` | 9 ||
| `override_end_option_prompt` | String | Examples: `"EVENT_MYSTERIOUSSTRANGER_END_AGAIN2", "EVENT_LOCKEDDOOR_PROMPT2", "EVENT_MYS...` | 8 ||
| [`party_damage`](./Arrays.md#array-party_damage) | Array / Number | Examples: `[ 5 10 ]` | 8 ||
| `party_random_mutation` | Integer | Examples: `1` | 8 ||
| `ambush_next_basic_fights` | String | Examples: `1` | 7 ||
| [`leave_party_temporarily`](Events_and_Encounters.md#object-leave_party_temporarily) | Object | Event Action: Removes a character from the active team until the next hub area. | 7 ||
| [`lose_item`](./Enums.md#enum-lose_item) | Enum | Examples: `equipped, inventory` | 7 ||
| [`permanent_stats`](Events_and_Encounters.md#object-permanent_stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 7 ||
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum | Examples: `WorldEventLegacyToken_CryptOpened` | 7 ||
| [`gain_coins`](./Arrays.md#array-gain_coins) | Array / Number | Examples: `[ 4 15 ], 5` | 6 ||
| `hide_appearance_changes` | Integer | Examples: `1` | 6 ||
| [`shop_now`](./Enums.md#enum-shop_now) | Enum | Examples: `TreasureHard, Event_SmallShop, Event_RareShop` | 6 ||
| [`add_weather`](./Enums.md#enum-add_weather) | Enum | Examples: `TheShimmer, SolarFlare, GeomagneticStorm` | 5 ||
| [`decrement_legacy_counter`](./Enums.md#enum-decrement_legacy_counter) | Enum | Examples: `WorldEventLegacyToken_StartDigging, WorldEventLegacyCounter_CrackInTheWall` | 5 ||
| `full_heal` | Integer | Examples: `1` | 4 ||
| [`learn_ability`](./Enums.md#enum-learn_ability) | Enum | Examples: `BarfBall, FutureSight` | 4 ||
| [`gain_familiar`](./Enums.md#enum-gain_familiar) | Enum | Event Action: Adds a specific familiar to the party. | 3 ||
| [`global_effect_next_fight`](Events_and_Encounters.md#object-global_effect_next_fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 3 ||
| [`kill`](./Enums.md#enum-kill) | Enum | Examples: `cat` | 3 ||
| [`lose_item_from_inventory`](./Enums.md#enum-lose_item_from_inventory) | Enum | Examples: `cat` | 3 ||
| [`make_old`](./Enums.md#enum-make_old) | Enum | Examples: `self` | 3 ||
| [`next_event_from_set`](Events_and_Encounters.md#object-next_event_from_set) | Enum / Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 3 ||
| [`spawn_reflection_next_fight`](Events_and_Encounters.md#object-spawn_reflection_next_fight) | Number / Object | Event Penalty: Spawns dark clones/reflections of the party in the next combat encounter. | 3 ||
| `damage` | Array / Equation | The damage dealt, which can be a numeric value, a formula string, or a defined damage object. | 2 | `[3 4]` (Array), `[2 5]` (Array), `5` (Equation), `7` (Equation) |
| [`battle`](./Math_Equations.md) | Enum / String | Examples: `{ ... }` | 2 ||
| [`event_now`](./Enums.md#enum-event_now) | Enum | Examples: `MeatGolem` | 2 ||
| [`gain_food`](./Arrays.md#array-gain_food) | Array / Number | Examples: `[ 5 10 ]` | 2 ||
| [`get_parasite_from_pool`](./Enums.md#enum-get_parasite_from_pool) | Array / Enum | Examples: `cursed_items, parasites` | 2 ||
| [`level_up`](./Enums.md#enum-level_up) | Enum | Examples: `all, self` | 2 ||
| [`lose_specific_item`](./Enums.md#enum-lose_specific_item) | Enum | Examples: `SlagTight` | 2 ||
| `party_heal_disorder` | Integer | Examples: `2` | 2 ||
| `party_heal_injury` | Integer | Examples: `99` | 2 ||
| [`party_permanent_stats_exclude_self`](Events_and_Encounters.md#object-party_permanent_stats_exclude_self) | Object | Event Reward: Permanently modifies stats for all party members except the one who initiated the action. | 2 ||
| `set_age` | Integer | Examples: `1` | 2 ||
| [`upgrade_ability`](./Enums.md#enum-upgrade_ability) | Enum | Examples: `random` | 2 ||
| [`upgrade_passive`](./Enums.md#enum-upgrade_passive) | Enum | Examples: `random` | 2 ||
| `ally_ambush_next_fights` | Integer | Examples: `1` | 1 ||
| [`ambush`](./Math_Equations.md) | Equation | Examples: `"events/chupacabra.lvl"` | 1 ||
| `clear_result_animation` | Integer | Examples: `1` | 1 ||
| [`conditional_reward`](Events_and_Encounters.md#object-conditional_reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 1 ||
| `gain_cat_familiar` | Integer | Examples: `1` | 1 ||
| [`gain_disorder_from_pool`](./Enums.md#enum-gain_disorder_from_pool) | Array / Enum | Examples: `Crazy_disorders` | 1 ||
| [`gain_immortal_familiar`](./Enums.md#enum-gain_immortal_familiar) | Enum | Examples: `CharmedFleaSpecial` | 1 ||
| [`get_and_equip_item`](./Enums.md#enum-get_and_equip_item) | Enum | Examples: `FlyLarva` | 1 ||
| `heal_disorder` | Integer | Examples: `2` | 1 ||
| [`injury`](./Enums.md#enum-injury) | Enum | Examples: `random` | 1 ||
| [`learn_ability_from_pool`](./Enums.md#enum-learn_ability_from_pool) | Enum | Examples: `Necromancer` | 1 ||
| [`learn_passive_from_pool`](./Enums.md#enum-learn_passive_from_pool) | Enum | Examples: `AnyUnlocked` | 1 ||
| [`lose_all_equipped_items`](./Enums.md#enum-lose_all_equipped_items) | Enum | Examples: `cat` | 1 ||
| [`mutation`](Events_and_Encounters.md#object-mutation) | Object | Event Object: Story branch or dialog option representing the 'Mutation' action. | 1 ||
| `next_event_bonus` | Integer | Examples: `2` | 1 ||
| `party_heal` | Integer | Examples: `10` | 1 ||
| [`party_injury`](./Enums.md#enum-party_injury) | Enum | Examples: `random` | 1 ||
| [`party_permanent_stats`](Events_and_Encounters.md#object-party_permanent_stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of all party members. | 1 ||
| [`party_random_mutation_from_set`](Events_and_Encounters.md#object-party_random_mutation_from_set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 1 ||
| [`play_result_animation`](./Enums.md#enum-play_result_animation) | Enum | Examples: `resultVeryGood` | 1 ||
| `random_mutation` | Integer | Event Reward: Applies a completely random mutation to a character. | 1 ||
| [`scramble_abilities`](./Enums.md#enum-scramble_abilities) | Enum | Examples: `all` | 1 ||
| [`scramble_basic_attack`](./Enums.md#enum-scramble_basic_attack) | Enum | Examples: `all` | 1 ||
| [`self_status_next_fight`](Events_and_Encounters.md#object-self_status_next_fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 1 ||
| [`trigger_adventure_unlock`](./Enums.md#enum-trigger_adventure_unlock) | Enum | Examples: `end_of_time_unlock, meat_world_unlock` | 1 ||
| [`random_pool`](./Arrays.md#array-random_pool) | Array | Examples: `[ { weight 90 prompt "EVENT_ABEGGAR_REW1" set_frame 3 ran..., [ { weight 85 p...` | 0 ||

</details>

---

#### `reward`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 760

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`common`](./Enums.md#enum-common) | Enum | Event Object: Story branch or dialog option representing the 'Common' action. | 1067 ||
| [`rare`](./Enums.md#enum-rare) | Enum | Event Object: Story branch or dialog option representing the 'Rare' action. | 673 ||
| [`prompt`](./Enums.md#enum-prompt) | String | Examples: `"woah", "EVENT_TRASHBIN_REW3", "EVENT_ABEGGAR_REW2"` | 38 ||
| `set_frame` | Integer | Examples: `4, 2, 5` | 36 ||
| [`clear_adventure_token`](./Enums.md#enum-clear_adventure_token) | Enum | Examples: `AdventureToken_BlueNeedle, AdventureToken_HasTakenNeedle, AdventureToken_RedN...` | 24 ||
| [`get_item_from_pool`](Events_and_Encounters.md#object-get_item_from_pool) | Enum / Object | Event Action: Rewards the player with an item drawn from a specific loot pool. | 11 ||
| [`set_subject`](./Enums.md#enum-set_subject) | Enum | Examples: `subject_frame, wall_of_flesh_noartery, throbbing_artery_noflesh` | 10 ||
| [`weight`](./Enums.md#enum-weight) | Float | Probability weight for this outcome. | 10 ||
| [`set_adventure_token`](./Enums.md#enum-set_adventure_token) | Enum | Examples: `AdventureToken_Mirage2, AdventureToken_StevenTryAgain3, HasPlayedMysteriousSt...` | 9 ||
| [`trigger_adventure_unlock`](./Enums.md#enum-trigger_adventure_unlock) | Enum | Examples: `end_of_time_unlock, meat_world_unlock` | 5 ||
| [`play_animation`](./Arrays.md#array-play_animation) | Enum | Examples: `resultVeryGood, resultBad` | 4 ||
| [`cutscene_on_exit`](./Enums.md#enum-cutscene_on_exit) | Enum | Examples: `infinite_intro` | 3 ||
| [`get_parasite_from_pool`](./Enums.md#enum-get_parasite_from_pool) | Enum | Examples: `cursed_items, parasites` | 2 ||
| [`level_up`](./Enums.md#enum-level_up) | Enum | Examples: `all, self` | 2 ||
| [`spawn_unit_next_fight`](Events_and_Encounters.md#object-spawn_unit_next_fight) | Object | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. | 2 ||
| `ambush_next_basic_fights` | Integer | Examples: `1` | 1 ||
| [`event_now`](./Enums.md#enum-event_now) | Enum | Examples: `MeatGolem` | 1 ||
| [`gain_coins`](./Arrays.md#array-gain_coins) | Array / Number | Examples: `[ 4 15 ], 5` | 1 ||
| [`gain_disorder_from_pool`](./Enums.md#enum-gain_disorder_from_pool) | Enum | Examples: `Crazy_disorders` | 1 ||
| [`get_item`](./Enums.md#enum-get_item) | Enum | Examples: `BrokenWindow` | 1 ||
| [`injury`](./Enums.md#enum-injury) | Enum | Examples: `random` | 1 ||
| `next_event_bonus` | Integer | Examples: `2` | 1 ||
| [`random_chance`](Events_and_Encounters.md#object-random_chance) | Object | Event Logic: Executes the nested outcome based on a percentage roll. | 1 ||
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum | Examples: `WorldEventLegacyToken_CryptOpened` | 1 ||
| [`party_damage`](./Arrays.md#array-party_damage) | Array | Examples: `[ 5 10 ]` | 0 ||
| [`random_pool`](./Arrays.md#array-random_pool) | Array | Examples: `[ { weight 90 prompt "EVENT_ABEGGAR_REW1" set_frame 3 ran..., [ { weight 85 p...` | 0 ||

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
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||

</details>

### Object: `AlienOvergrowth`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Undocumented. | 1 | `"WEATHER_ALIENOVERGROWTH_DESC"` |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Undocumented. | 1 ||
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
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||

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
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||

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
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||

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
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Undocumented. | 1 ||

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
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||

</details>

### Object: `Cancer`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Undocumented. | 2 | `"DISORDER_CANCER_DESC"`<br>`"ITEM_CANCER_DESC"` |
| `name` | String | Undocumented. | 2 | `"DISORDER_CANCER_NAME"`<br>`"ITEM_CANCER_NAME"` |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 2 ||
| `class` | String | Undocumented. | 1 | `Disorder` |
| `frame` | Number | Undocumented. | 1 | `152` |
| `kind` | String | Undocumented. | 1 | `trinket` |
| `rarity` | String | Undocumented. | 1 | `rare` |
| `set` | String | Undocumented. | 1 | `Mother` |

</details>

### Object: `CharmedMaggot`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
| `variant_of` | String | Undocumented. | 1 | `Maggot` |

</details>

### Object: `CharmedPinky`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
| `variant_of` | String | Undocumented. | 1 | `Pinky` |

</details>

### Object: `CharmedRaptorBaby`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
| `variant_of` | String | Undocumented. | 1 | `RaptorBaby` |

</details>

### Object: `CharmedTarBaby`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
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
| [`global_passives`](Items_and_Equipment.md#object-global_passives) | Object | Undocumented. | 1 ||
| `hint_destination` | String | Undocumented. | 1 | `meatworld` |
| `hint_prerequisite_flag` | String | Undocumented. | 1 | `mapflag_MeatWorldUnlockedFull` |
| `indestructible` | Boolean | Undocumented. | 1 | `true` |
| `kind` | String | Undocumented. | 1 | `trinket` |
| `legacy_quest` | Boolean | Undocumented. | 1 | `true` |
| `name` | String | Undocumented. | 1 | `"ITEM_CRYOGENICTIMECHAMBER_EMP` |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
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
| [`global_passives`](Items_and_Equipment.md#object-global_passives) | Object | Undocumented. | 1 ||
| `hint_destination` | String | Undocumented. | 1 | `lab` |
| `indestructible` | Boolean | Undocumented. | 1 | `true` |
| `kind` | String | Undocumented. | 1 | `trinket` |
| `legacy_quest` | Boolean | Undocumented. | 1 | `true` |
| `name` | String | Undocumented. | 1 | `"ITEM_CRYOGENICTIMECHAMBER_FUL` |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
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
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||

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
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
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
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Undocumented. | 1 ||

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
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
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
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||

</details>

### Object: `GeomagneticStorm`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Undocumented. | 1 | `"WEATHER_GEOMAGSTORM_DESC"` |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Undocumented. | 1 ||
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
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Undocumented. | 1 ||

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
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
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
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Undocumented. | 1 ||
| `name` | String | Undocumented. | 1 | `"WEATHER_HAUNTED_NAME"` |

</details>

### Object: `Host`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | Undocumented. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Undocumented. | 1 ||
| `class` | String | Undocumented. | 1 | `Hunter` |
| `desc` | String | Undocumented. | 1 | `"PASSIVE_HOST_DESC"` |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| `name` | String | Undocumented. | 1 | `"PASSIVE_HOST_NAME"` |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Undocumented. | 1 ||

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
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
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
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
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
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
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
| [`intro`](Events_and_Encounters.md#object-intro) | Object | Undocumented. | 1 ||
| [`main`](Events_and_Encounters.md#object-main) | Object | Undocumented. | 1 ||

</details>

### Object: `MysteriousTomb2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`intro`](Events_and_Encounters.md#object-intro) | Object | Undocumented. | 1 ||
| [`main`](Events_and_Encounters.md#object-main) | Object | Undocumented. | 1 ||

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
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||

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
| [`lock_item_slot`](Miscellaneous.md#object-lock_item_slot) | Object | Undocumented. | 1 ||
| `name` | String | Undocumented. | 1 | `"DISORDER_PUNCTUREDEYE_NAME"` |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||

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
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
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
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
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
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
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
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Undocumented. | 1 ||
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
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||

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
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
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
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
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
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||

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
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||

</details>

### Object: `StrangeEggs`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Undocumented. | 1 | `"WEATHER_STRANGEEGGS_DESC"` |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Undocumented. | 1 ||
| `name` | String | Undocumented. | 1 | `"WEATHER_STRANGEEGGS_NAME"` |

</details>

### Object: `TheShimmer`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Undocumented. | 1 | `"WEATHER_SHIMMER_DESC"` |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Undocumented. | 1 ||
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
| [`global_passives`](Items_and_Equipment.md#object-global_passives) | Object | Undocumented. | 1 ||
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
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Undocumented. | 1 ||

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
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
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
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
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
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Undocumented. | 1 ||
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
| [`scars`](Injuries.md#object-scars) | Object | Undocumented. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Undocumented. | 1 ||
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
| [`popup`](Miscellaneous.md#object-popup) | Object | Undocumented. | 1 ||
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
| [`popup`](Miscellaneous.md#object-popup) | Object | Undocumented. | 1 ||
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
| [`scars`](Injuries.md#object-scars) | Object | Undocumented. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Undocumented. | 1 ||
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
