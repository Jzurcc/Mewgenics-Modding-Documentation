# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Progression Unlocks

> **Associated Files:** `data/adventure_progression_unlocks.gon, data/npc_favor_unlocks.gon`


### Object: `ROOT`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 266

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 883 | `common`<br>`rare`<br>`cha` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 155 | `Default`<br>`FormChange`<br>`Druid` |
| [`popup`](./Progression_Unlocks.md#object-popup) | Object  || 266 | `{ . . . }` |
| [`intro`](./Arrays.md#array-intro) | Array | An object defining the introductory cutscene for the event, including title, cat selection, and visuals. | 239 | `[PersuasionDevice]` |
| [`complete_chapter_with_class`](./Arrays.md#array-complete_chapter_with_class) | Array || 129 | `[boneyard Butcher]`<br>`[boneyard Colorless]`<br>`[boneyard Druid]` |
| [`unlock_item_immediate`](./Enums.md#enum-unlock_item_immediate) | Enum || 127 | `AnointingOil`<br>`BagOfBags`<br>`BagOfSeeds` |
| [`trigger_npc_sequence`](./Enums.md#enum-trigger_npc_sequence) | Enum || 53 | `beanies_begin_accepting_cats`<br>`beanies_bombquest_2`<br>`beanies_bombquest_3` |
| [`beat_house_boss`](./Enums.md#enum-beat_house_boss) | Enum || 48 | `any`<br>`guillotina_1`<br>`guillotina_2` |
| [`complete_chapter`](./Enums.md#enum-complete_chapter) | Enum || 37 | `alley`<br>`boneyard`<br>`bunker` |
| `required_difficulty` | Integer || 36 | `0`<br>`1`<br>`2` |
| `repeat` | Integer || 33 | `1`<br>`2`<br>`20` |
| [`beat_chapter_boss`](./Enums.md#enum-beat_chapter_boss) | Enum || 31 | `alley`<br>`boneyard`<br>`bunker` |
| [`unlock_song`](./Enums.md#enum-unlock_song) | Enum || 29 | `alone_in_the_dark`<br>`angel_wings`<br>`bolt_of_lightning` |
| [`unlock_ability`](./Enums.md#enum-unlock_ability) | Enum || 28 | `BallOfSpiders`<br>`Bump`<br>`Ethereal` |
| [`unlock_passive`](./Enums.md#enum-unlock_passive) | Enum || 28 | `AlphaStrike`<br>`ArmorSpecialist`<br>`Bouncer` |
| [`set_mapgen_flag`](./Enums.md#enum-set_mapgen_flag) | Enum || 23 | `BoneyardUnlocked`<br>`BothObelisksUnlocked`<br>`BunkerUnlocked` |
| [`complete_checklist_with_class`](./Enums.md#enum-complete_checklist_with_class) | Enum || 14 | `Butcher`<br>`Colorless`<br>`Druid` |
| [`unlock_quest_item`](./Enums.md#enum-unlock_quest_item) | Enum || 13 | `BlackShard`<br>`CryogenicTimeChamber_Empty`<br>`GuillotinasHead` |
| `repeatable` | Boolean || 10 | `true` |
| [`trigger_house_boss`](./Enums.md#enum-trigger_house_boss) | Enum || 10 | `guillotina_1`<br>`guillotina_2`<br>`guillotina_3` |
| [`complete_act_difficulty`](./Arrays.md#array-complete_act_difficulty) | Array || 9 | `[1 0]`<br>`[1 1]`<br>`[1 2]` |
| [`unlock_act_difficulty`](./Arrays.md#array-unlock_act_difficulty) | Array || 9 | `[1 1]`<br>`[1 2]`<br>`[1 3]` |
| [`queue_cutscene_immediate`](./Enums.md#enum-queue_cutscene_immediate) | Enum || 8 | `caves_intro`<br>`core_intro`<br>`desert_intro` |
| [`set_savefile_flag`](./Enums.md#enum-set_savefile_flag) | String || 6 | `AlienInvasionUnlocked`<br>`HauntedNightUnlocked`<br>`PlotFlag_Beanies_Homeless` |
| [`unlock_boss`](./Enums.md#enum-unlock_boss) | Enum || 6 | `bumblefoot`<br>`gambit`<br>`infestedduo` |
| [`preempt_npc_sequence`](./Enums.md#enum-preempt_npc_sequence) | Enum || 4 | `beanies_bombquest_2`<br>`beanies_bombquest_3`<br>`beanies_bombquest_amnesia` |
| [`fail_item_quest`](./Enums.md#enum-fail_item_quest) | Enum || 4 | `JarOfChaos`<br>`JarOfRadiatedBlood`<br>`JarOfRadiation` |
| `fully_complete_difficulty` | Integer || 4 | `0`<br>`1`<br>`2` |
| [`post_combat_cutscene`](./Enums.md#enum-post_combat_cutscene) | Enum || 4 | `obelisk1_core`<br>`obelisk1_moon`<br>`obelisk2_core` |
| [`unlock_npc_tomorrow`](./Enums.md#enum-unlock_npc_tomorrow) | Enum || 4 | `beanies`<br>`jack`<br>`organgrinder` |
| [`visit_chapter`](./Enums.md#enum-visit_chapter) | Enum || 4 | `dimensionx`<br>`future`<br>`iceage` |
| [`trigger_npc_sequence_tomorrow`](./Enums.md#enum-trigger_npc_sequence_tomorrow) | Enum || 3 | `butch_boneyard_intro`<br>`frank_caves_intro`<br>`jack_desert_intro` |
| `requires_monoclass_run` | Boolean || 3 | `true` |
| [`requires_unlocked_npc`](./Enums.md#enum-requires_unlocked_npc) | Enum || 3 | `frank`<br>`jack`<br>`tracy` |
| [`complete_chapters`](./Arrays.md#array-complete_chapters) | Array || 3 | `[caves boneyard]`<br>`[core moon]` |
| [`reset_npc_sequence`](./Enums.md#enum-reset_npc_sequence) | Enum || 2 | `beanies_bombquest_2`<br>`beanies_bombquest_3`<br>`beanies_bombquest_begin` |
| [`beanies_quests_intro`](./Progression_Unlocks.md#object-beanies_quests_intro) | Object  || 2 | `{ . . . }` |
| [`beanies_quests_repeat`](./Progression_Unlocks.md#object-beanies_quests_repeat) | Object  || 2 | `{ . . . }` |
| [`complete_adventure`](./Enums.md#enum-complete_adventure) | Enum || 2 | `anywhere` |
| [`frank_max_intro`](./Progression_Unlocks.md#object-frank_max_intro) | Object  || 2 | `{ . . . }` |
| [`frank_max_repeating`](./Progression_Unlocks.md#object-frank_max_repeating) | Object  || 2 | `{ . . . }` |
| [`house_upgrade_4throom`](./Progression_Unlocks.md#object-house_upgrade_4throom) | Object  || 2 | `{ . . . }` |
| [`house_upgrade_attic`](./Progression_Unlocks.md#object-house_upgrade_attic) | Object  || 2 | `{ . . . }` |
| [`house_upgrade_largehouse`](./Progression_Unlocks.md#object-house_upgrade_largehouse) | Object  || 2 | `{ . . . }` |
| [`house_upgrade_mediumhouse`](./Progression_Unlocks.md#object-house_upgrade_mediumhouse) | Object  || 2 | `{ . . . }` |
| [`jack_max_intro`](./Progression_Unlocks.md#object-jack_max_intro) | Object  || 2 | `{ . . . }` |
| [`jack_max_repeating`](./Progression_Unlocks.md#object-jack_max_repeating) | Object  || 2 | `{ . . . }` |
| [`jack_shopupgrade1`](./Progression_Unlocks.md#object-jack_shopupgrade1) | Object  || 2 | `{ . . . }` |
| [`jack_shopupgrade2`](./Progression_Unlocks.md#object-jack_shopupgrade2) | Object  || 2 | `{ . . . }` |
| [`jack_shopupgrade3`](./Progression_Unlocks.md#object-jack_shopupgrade3) | Object  || 2 | `{ . . . }` |
| [`jack_shopupgrade4`](./Progression_Unlocks.md#object-jack_shopupgrade4) | Object  || 2 | `{ . . . }` |
| [`organ_max_intro`](./Progression_Unlocks.md#object-organ_max_intro) | Object  || 2 | `{ . . . }` |
| [`organ_max_repeating`](./Progression_Unlocks.md#object-organ_max_repeating) | Object  || 2 | `{ . . . }` |
| [`organ_unlock`](./Progression_Unlocks.md#object-organ_unlock) | Object  || 2 | `{ . . . }` |
| [`organ_upgrade1`](./Progression_Unlocks.md#object-organ_upgrade1) | Object  || 2 | `{ . . . }` |
| [`organ_upgrade2`](./Progression_Unlocks.md#object-organ_upgrade2) | Object  || 2 | `{ . . . }` |
| [`organ_upgrade3`](./Progression_Unlocks.md#object-organ_upgrade3) | Object  || 2 | `{ . . . }` |
| [`organ_upgrade4`](./Progression_Unlocks.md#object-organ_upgrade4) | Object  || 2 | `{ . . . }` |
| [`organ_upgrade5`](./Progression_Unlocks.md#object-organ_upgrade5) | Object  || 2 | `{ . . . }` |
| [`organ_upgrade6`](./Progression_Unlocks.md#object-organ_upgrade6) | Object  || 2 | `{ . . . }` |
| [`require_beat_house_boss`](./Enums.md#enum-require_beat_house_boss) | Enum || 2 | `pyrophina`<br>`zaratana` |
| [`require_mapgen_flag`](./Enums.md#enum-require_mapgen_flag) | Enum || 2 | `CoreObeliskUnlocked`<br>`MoonObeliskUnlocked` |
| [`steven_milliontrashed`](./Progression_Unlocks.md#object-steven_milliontrashed) | Object  || 2 | `{ . . . }` |
| [`surviving_kaiju`](./Enums.md#enum-surviving_kaiju) | Enum || 2 | `pyrophina`<br>`zaratana` |
| [`tink_aggression`](./Progression_Unlocks.md#object-tink_aggression) | Object  || 2 | `{ . . . }` |
| [`tink_basestats`](./Progression_Unlocks.md#object-tink_basestats) | Object  || 2 | `{ . . . }` |
| [`tink_inbreeding`](./Progression_Unlocks.md#object-tink_inbreeding) | Object  || 2 | `{ . . . }` |
| [`tink_max_intro`](./Progression_Unlocks.md#object-tink_max_intro) | Object  || 2 | `{ . . . }` |
| [`tink_max_repeating`](./Progression_Unlocks.md#object-tink_max_repeating) | Object  || 2 | `{ . . . }` |
| [`tink_prettybow`](./Progression_Unlocks.md#object-tink_prettybow) | Object  || 2 | `{ . . . }` |
| [`tink_relationships`](./Progression_Unlocks.md#object-tink_relationships) | Object  || 2 | `{ . . . }` |
| [`tink_sexuality`](./Progression_Unlocks.md#object-tink_sexuality) | Object  || 2 | `{ . . . }` |
| [`tink_tags`](./Progression_Unlocks.md#object-tink_tags) | Object  || 2 | `{ . . . }` |
| [`tracy_blankcollar1`](./Progression_Unlocks.md#object-tracy_blankcollar1) | Object  || 2 | `{ . . . }` |
| [`tracy_blankcollar2`](./Progression_Unlocks.md#object-tracy_blankcollar2) | Object  || 2 | `{ . . . }` |
| [`tracy_blankcollar3`](./Progression_Unlocks.md#object-tracy_blankcollar3) | Object  || 2 | `{ . . . }` |
| [`tracy_foodstorage1`](./Progression_Unlocks.md#object-tracy_foodstorage1) | Object  || 2 | `{ . . . }` |
| [`tracy_foodstorage10`](./Progression_Unlocks.md#object-tracy_foodstorage10) | Object  || 2 | `{ . . . }` |
| [`tracy_foodstorage2`](./Progression_Unlocks.md#object-tracy_foodstorage2) | Object  || 2 | `{ . . . }` |
| [`tracy_foodstorage3`](./Progression_Unlocks.md#object-tracy_foodstorage3) | Object  || 2 | `{ . . . }` |
| [`tracy_foodstorage4`](./Progression_Unlocks.md#object-tracy_foodstorage4) | Object  || 2 | `{ . . . }` |
| [`tracy_foodstorage5`](./Progression_Unlocks.md#object-tracy_foodstorage5) | Object  || 2 | `{ . . . }` |
| [`tracy_foodstorage6`](./Progression_Unlocks.md#object-tracy_foodstorage6) | Object  || 2 | `{ . . . }` |
| [`tracy_foodstorage7`](./Progression_Unlocks.md#object-tracy_foodstorage7) | Object  || 2 | `{ . . . }` |
| [`tracy_foodstorage8`](./Progression_Unlocks.md#object-tracy_foodstorage8) | Object  || 2 | `{ . . . }` |
| [`tracy_foodstorage9`](./Progression_Unlocks.md#object-tracy_foodstorage9) | Object  || 2 | `{ . . . }` |
| [`tracy_idol1`](./Progression_Unlocks.md#object-tracy_idol1) | Object  || 2 | `{ . . . }` |
| [`tracy_idol2`](./Progression_Unlocks.md#object-tracy_idol2) | Object  || 2 | `{ . . . }` |
| [`tracy_idol3`](./Progression_Unlocks.md#object-tracy_idol3) | Object  || 2 | `{ . . . }` |
| [`tracy_idol4`](./Progression_Unlocks.md#object-tracy_idol4) | Object  || 2 | `{ . . . }` |
| [`tracy_idol5`](./Progression_Unlocks.md#object-tracy_idol5) | Object  || 2 | `{ . . . }` |
| [`tracy_idol6`](./Progression_Unlocks.md#object-tracy_idol6) | Object  || 2 | `{ . . . }` |
| [`tracy_idol7`](./Progression_Unlocks.md#object-tracy_idol7) | Object  || 2 | `{ . . . }` |
| [`tracy_max_intro`](./Progression_Unlocks.md#object-tracy_max_intro) | Object  || 2 | `{ . . . }` |
| [`tracy_max_repeating`](./Progression_Unlocks.md#object-tracy_max_repeating) | Object  || 2 | `{ . . . }` |
| [`unlock_levelgroup`](./Enums.md#enum-unlock_levelgroup) | Enum || 2 | `bigsharklevels` |
| [`upgrade_storage_1`](./Progression_Unlocks.md#object-upgrade_storage_1) | Object  || 2 | `{ . . . }` |
| [`upgrade_storage_2`](./Progression_Unlocks.md#object-upgrade_storage_2) | Object  || 2 | `{ . . . }` |
| [`upgrade_storage_3`](./Progression_Unlocks.md#object-upgrade_storage_3) | Object  || 2 | `{ . . . }` |
| [`upgrade_storage_4`](./Progression_Unlocks.md#object-upgrade_storage_4) | Object  || 2 | `{ . . . }` |
| [`upgrade_storage_5`](./Progression_Unlocks.md#object-upgrade_storage_5) | Object  || 2 | `{ . . . }` |
| [`upgrade_storage_6`](./Progression_Unlocks.md#object-upgrade_storage_6) | Object  || 2 | `{ . . . }` |
| [`upgrade_storage_7`](./Progression_Unlocks.md#object-upgrade_storage_7) | Object  || 2 | `{ . . . }` |
| [`upgrade_storage_repeating_crazy`](./Progression_Unlocks.md#object-upgrade_storage_repeating_crazy) | Object  || 2 | `{ . . . }` |
| [`upgrade_storage_repeating_hard`](./Progression_Unlocks.md#object-upgrade_storage_repeating_hard) | Object  || 2 | `{ . . . }` |
| [`upgrade_storage_repeating_impossible`](./Progression_Unlocks.md#object-upgrade_storage_repeating_impossible) | Object  || 2 | `{ . . . }` |
| [`upgrade_storage_repeating_intro`](./Progression_Unlocks.md#object-upgrade_storage_repeating_intro) | Object  || 2 | `{ . . . }` |
| [`upgrade_storage_repeating_normal`](./Progression_Unlocks.md#object-upgrade_storage_repeating_normal) | Object  || 2 | `{ . . . }` |
| [`destinations`](./Progression_Unlocks.md#object-destinations) | Object  || 1 | `{ . . . }` |
| [`fail_adventure`](./Enums.md#enum-fail_adventure) | Enum || 1 | `anywhere` |
| [`finish_quest`](./Enums.md#enum-finish_quest) | Enum || 1 | `JarOfChaos` |
| [`increment_savefile_counter`](./Enums.md#enum-increment_savefile_counter) | String || 1 | `GameStat_CountNukeQuestCompletions` |
| [`prereqs`](./Progression_Unlocks.md#object-prereqs) | Object  || 1 | `{ . . . }` |
| `requires_hard_path` | Boolean || 1 | `true` |
| [`reset_unlock`](./Enums.md#enum-reset_unlock) | Enum || 1 | `nuke_quest_begin` |
| [`unlock_item`](./Enums.md#enum-unlock_item) | Enum || 1 | `MomsKnife` |
| [`main_pool`](./Arrays.md#array-main_pool) | Array || 1 | `[` |

</details>


---


### Object: `popup`


**Definition:** No definition provided.  
**Total Count:** 266

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 266 | `common`<br>`rare`<br>`cha` |
| `immediate` | Boolean | If true, the action (e.g., attack) occurs instantly without waiting for the unit's turn in the initiative order. | 221 | `false`<br>`true` |
| [`frame`](./Enums.md#enum-frame) | Integer | The sprite frame index to display. | 159 | `1`<br>`10`<br>`100` |

</details>


---


### Object: `tracy_special_item`


**Definition:** No definition provided.  
**Total Count:** 22

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`tracy_blankcollar1`](#object-tracy_blankcollar1), [`tracy_blankcollar2`](#object-tracy_blankcollar2), [`tracy_blankcollar3`](#object-tracy_blankcollar3), [`tracy_foodstorage1`](#object-tracy_foodstorage1), [`tracy_foodstorage10`](#object-tracy_foodstorage10), [`tracy_foodstorage2`](#object-tracy_foodstorage2), [`tracy_foodstorage3`](#object-tracy_foodstorage3), [`tracy_foodstorage4`](#object-tracy_foodstorage4), [`tracy_foodstorage5`](#object-tracy_foodstorage5), [`tracy_foodstorage6`](#object-tracy_foodstorage6), [`tracy_foodstorage7`](#object-tracy_foodstorage7), [`tracy_foodstorage8`](#object-tracy_foodstorage8), [`tracy_foodstorage9`](#object-tracy_foodstorage9), [`tracy_idol1`](#object-tracy_idol1), [`tracy_idol2`](#object-tracy_idol2), [`tracy_idol3`](#object-tracy_idol3), [`tracy_idol4`](#object-tracy_idol4), [`tracy_idol5`](#object-tracy_idol5), [`tracy_idol6`](#object-tracy_idol6), [`tracy_idol7`](#object-tracy_idol7), [`tracy_max_intro`](#object-tracy_max_intro), [`tracy_max_repeating`](#object-tracy_max_repeating)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 22 | `{ . . . }` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 22 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `beanies_quests_intro`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| [`generate_beanies_quest`](./Enums.md#enum-generate_beanies_quest) | Enum || 1 | `intro`<br>`main_pool` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `beanies_quests_repeat`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| [`generate_beanies_quest`](./Enums.md#enum-generate_beanies_quest) | Enum || 1 | `intro`<br>`main_pool` |
| [`level_display`](./Enums.md#enum-level_display) | Enum || 1 | `max` |
| [`repeat`](./Enums.md#enum-repeat) | Enum || 1 | `1`<br>`2`<br>`20` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `frank_max_intro`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| [`gift_item_from_pool`](./Enums.md#enum-gift_item_from_pool) | Enum || 1 | `parasites` |
| [`level_display`](./Enums.md#enum-level_display) | Enum || 1 | `max` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `frank_max_repeating`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| [`gift_item_from_pool`](./Enums.md#enum-gift_item_from_pool) | Enum || 1 | `parasites` |
| [`level_display`](./Enums.md#enum-level_display) | Enum || 1 | `max` |
| [`repeat`](./Enums.md#enum-repeat) | Enum || 1 | `1`<br>`2`<br>`20` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `house_upgrade_4throom`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| [`house_upgrade`](./Enums.md#enum-house_upgrade) | Enum || 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `house_upgrade_attic`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| [`house_upgrade`](./Enums.md#enum-house_upgrade) | Enum || 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `house_upgrade_largehouse`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`house_upgrade`](./Enums.md#enum-house_upgrade) | Enum || 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `house_upgrade_mediumhouse`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`house_upgrade`](./Enums.md#enum-house_upgrade) | Enum || 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `jack_max_intro`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| [`level_display`](./Enums.md#enum-level_display) | Enum || 1 | `max` |
| `rep_reward_count` | Integer || 1 | `1` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `jack_max_repeating`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| [`level_display`](./Enums.md#enum-level_display) | Enum || 1 | `max` |
| `rep_reward_count` | Integer || 1 | `1` |
| [`repeat`](./Enums.md#enum-repeat) | Enum || 1 | `1`<br>`2`<br>`20` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `jack_shopupgrade1`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer || 1 | `1` |

</details>


---


### Object: `jack_shopupgrade2`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer || 1 | `1` |

</details>


---


### Object: `jack_shopupgrade3`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer || 1 | `1` |

</details>


---


### Object: `jack_shopupgrade4`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer || 1 | `1` |

</details>


---


### Object: `organ_max_intro`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| [`gift_item`](./Enums.md#enum-gift_item) | Enum || 1 | `TinksBow`<br>`disorder_needle` |
| [`level_display`](./Enums.md#enum-level_display) | Enum || 1 | `max` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `organ_max_repeating`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| [`gift_item`](./Enums.md#enum-gift_item) | Enum || 1 | `TinksBow`<br>`disorder_needle` |
| [`level_display`](./Enums.md#enum-level_display) | Enum || 1 | `max` |
| [`repeat`](./Enums.md#enum-repeat) | Enum || 1 | `1`<br>`2`<br>`20` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `organ_unlock`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer || 1 | `1` |

</details>


---


### Object: `organ_upgrade1`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer || 1 | `1` |

</details>


---


### Object: `organ_upgrade2`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer || 1 | `1` |

</details>


---


### Object: `organ_upgrade3`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer || 1 | `1` |

</details>


---


### Object: `organ_upgrade4`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer || 1 | `1` |

</details>


---


### Object: `organ_upgrade5`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer || 1 | `1` |

</details>


---


### Object: `organ_upgrade6`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer || 1 | `1` |

</details>


---


### Object: `steven_milliontrashed`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| [`level_display`](./Enums.md#enum-level_display) | Enum || 1 | `max` |
| [`repeat`](./Enums.md#enum-repeat) | Enum || 1 | `1`<br>`2`<br>`20` |

</details>


---


### Object: `tink_aggression`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| [`set_savefile_flag`](./Enums.md#enum-set_savefile_flag) | String || 1 | `AlienInvasionUnlocked`<br>`HauntedNightUnlocked`<br>`PlotFlag_Beanies_Homeless` |

</details>


---


### Object: `tink_basestats`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| [`set_savefile_flag`](./Enums.md#enum-set_savefile_flag) | String || 1 | `AlienInvasionUnlocked`<br>`HauntedNightUnlocked`<br>`PlotFlag_Beanies_Homeless` |

</details>


---


### Object: `tink_inbreeding`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| [`set_savefile_flag`](./Enums.md#enum-set_savefile_flag) | String || 1 | `AlienInvasionUnlocked`<br>`HauntedNightUnlocked`<br>`PlotFlag_Beanies_Homeless` |

</details>


---


### Object: `tink_max_intro`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `coins` | Integer | The amount of coins required to use this ability or obtained from this source. | 1 | `1`<br>`2`<br>`25` |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| [`level_display`](./Enums.md#enum-level_display) | Enum || 1 | `max` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `tink_max_repeating`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `coins` | Integer | The amount of coins required to use this ability or obtained from this source. | 1 | `1`<br>`2`<br>`25` |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| [`level_display`](./Enums.md#enum-level_display) | Enum || 1 | `max` |
| [`repeat`](./Enums.md#enum-repeat) | Enum || 1 | `1`<br>`2`<br>`20` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `tink_prettybow`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| [`gift_item`](./Enums.md#enum-gift_item) | Enum || 1 | `TinksBow`<br>`disorder_needle` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `tink_relationships`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| [`set_savefile_flag`](./Enums.md#enum-set_savefile_flag) | String || 1 | `AlienInvasionUnlocked`<br>`HauntedNightUnlocked`<br>`PlotFlag_Beanies_Homeless` |

</details>


---


### Object: `tink_sexuality`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| [`set_savefile_flag`](./Enums.md#enum-set_savefile_flag) | String || 1 | `AlienInvasionUnlocked`<br>`HauntedNightUnlocked`<br>`PlotFlag_Beanies_Homeless` |

</details>


---


### Object: `tink_tags`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| [`set_savefile_flag`](./Enums.md#enum-set_savefile_flag) | String || 1 | `AlienInvasionUnlocked`<br>`HauntedNightUnlocked`<br>`PlotFlag_Beanies_Homeless` |

</details>


---


### Object: `tracy_blankcollar1`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| `required_age` | Integer || 1 | `5` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer || 1 | `1` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `tracy_blankcollar2`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| `required_age` | Integer || 1 | `5` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer || 1 | `1` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `tracy_blankcollar3`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| `required_age` | Integer || 1 | `5` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer || 1 | `1` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `tracy_foodstorage1`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| `required_age` | Integer || 1 | `5` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer || 1 | `1` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `tracy_foodstorage10`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| `required_age` | Integer || 1 | `5` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer || 1 | `1` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `tracy_foodstorage2`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| `required_age` | Integer || 1 | `5` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer || 1 | `1` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `tracy_foodstorage3`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| `required_age` | Integer || 1 | `5` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer || 1 | `1` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `tracy_foodstorage4`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| `required_age` | Integer || 1 | `5` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer || 1 | `1` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `tracy_foodstorage5`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| `required_age` | Integer || 1 | `5` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer || 1 | `1` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `tracy_foodstorage6`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| `required_age` | Integer || 1 | `5` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer || 1 | `1` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `tracy_foodstorage7`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| `required_age` | Integer || 1 | `5` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer || 1 | `1` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `tracy_foodstorage8`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| `required_age` | Integer || 1 | `5` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer || 1 | `1` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `tracy_foodstorage9`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| `required_age` | Integer || 1 | `5` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer || 1 | `1` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `tracy_idol1`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| `required_age` | Integer || 1 | `5` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer || 1 | `1` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `tracy_idol2`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| `required_age` | Integer || 1 | `5` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer || 1 | `1` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `tracy_idol3`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| `required_age` | Integer || 1 | `5` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer || 1 | `1` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `tracy_idol4`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| `required_age` | Integer || 1 | `5` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer || 1 | `1` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `tracy_idol5`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| `required_age` | Integer || 1 | `5` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer || 1 | `1` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `tracy_idol6`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| `required_age` | Integer || 1 | `5` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer || 1 | `1` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `tracy_idol7`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| `required_age` | Integer || 1 | `5` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer || 1 | `1` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `tracy_max_intro`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| [`level_display`](./Enums.md#enum-level_display) | Enum || 1 | `max` |
| `required_age` | Integer || 1 | `5` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `tracy_max_repeating`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| [`level_display`](./Enums.md#enum-level_display) | Enum || 1 | `max` |
| [`repeat`](./Enums.md#enum-repeat) | Enum || 1 | `1`<br>`2`<br>`20` |
| `required_age` | Integer || 1 | `5` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `upgrade_storage_1`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| `required_act` | Integer || 1 | `0`<br>`1`<br>`2` |
| `required_chapter` | Integer || 1 | `0`<br>`2`<br>`3` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `storage_expansion` | Integer || 1 | `1` |

</details>


---


### Object: `upgrade_storage_2`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| `required_act` | Integer || 1 | `0`<br>`1`<br>`2` |
| `required_chapter` | Integer || 1 | `0`<br>`2`<br>`3` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `storage_expansion` | Integer || 1 | `1` |

</details>


---


### Object: `upgrade_storage_3`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| `required_act` | Integer || 1 | `0`<br>`1`<br>`2` |
| `required_chapter` | Integer || 1 | `0`<br>`2`<br>`3` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `storage_expansion` | Integer || 1 | `1` |

</details>


---


### Object: `upgrade_storage_4`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| `required_act` | Integer || 1 | `0`<br>`1`<br>`2` |
| `required_chapter` | Integer || 1 | `0`<br>`2`<br>`3` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `storage_expansion` | Integer || 1 | `1` |

</details>


---


### Object: `upgrade_storage_5`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| `required_act` | Integer || 1 | `0`<br>`1`<br>`2` |
| `required_chapter` | Integer || 1 | `0`<br>`2`<br>`3` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `storage_expansion` | Integer || 1 | `1` |

</details>


---


### Object: `upgrade_storage_6`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| `required_act` | Integer || 1 | `0`<br>`1`<br>`2` |
| `required_chapter` | Integer || 1 | `0`<br>`2`<br>`3` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `storage_expansion` | Integer || 1 | `1` |

</details>


---


### Object: `upgrade_storage_7`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| `required_act` | Integer || 1 | `0`<br>`1`<br>`2` |
| `required_chapter` | Integer || 1 | `0`<br>`2`<br>`3` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `storage_expansion` | Integer || 1 | `1` |

</details>


---


### Object: `upgrade_storage_repeating_crazy`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| [`level_display`](./Enums.md#enum-level_display) | Enum || 1 | `max` |
| `rep_reward_count` | Integer || 1 | `1` |
| `repeat` | Integer || 1 | `1`<br>`2`<br>`20` |
| `required_act` | Integer || 1 | `0`<br>`1`<br>`2` |
| `required_chapter` | Integer || 1 | `0`<br>`2`<br>`3` |
| `required_difficulty` | Integer || 1 | `0`<br>`1`<br>`2` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `upgrade_storage_repeating_hard`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| [`level_display`](./Enums.md#enum-level_display) | Enum || 1 | `max` |
| `rep_reward_count` | Integer || 1 | `1` |
| `repeat` | Integer || 1 | `1`<br>`2`<br>`20` |
| `required_act` | Integer || 1 | `0`<br>`1`<br>`2` |
| `required_chapter` | Integer || 1 | `0`<br>`2`<br>`3` |
| `required_difficulty` | Integer || 1 | `0`<br>`1`<br>`2` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `upgrade_storage_repeating_impossible`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| [`level_display`](./Enums.md#enum-level_display) | Enum || 1 | `max` |
| `rep_reward_count` | Integer || 1 | `1` |
| [`repeat`](./Enums.md#enum-repeat) | Enum || 1 | `1`<br>`2`<br>`20` |
| `required_act` | Integer || 1 | `0`<br>`1`<br>`2` |
| `required_chapter` | Integer || 1 | `0`<br>`2`<br>`3` |
| `required_difficulty` | Integer || 1 | `0`<br>`1`<br>`2` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `upgrade_storage_repeating_intro`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| [`level_display`](./Enums.md#enum-level_display) | Enum || 1 | `max` |
| `rep_reward_count` | Integer || 1 | `1` |
| `required_act` | Integer || 1 | `0`<br>`1`<br>`2` |
| `required_chapter` | Integer || 1 | `0`<br>`2`<br>`3` |
| `required_difficulty` | Integer || 1 | `0`<br>`1`<br>`2` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `upgrade_storage_repeating_normal`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer || 1 | `1`<br>`10`<br>`100` |
| [`level_display`](./Enums.md#enum-level_display) | Enum || 1 | `max` |
| `rep_reward_count` | Integer || 1 | `1` |
| `repeat` | Integer || 1 | `1`<br>`2`<br>`20` |
| `required_act` | Integer || 1 | `0`<br>`1`<br>`2` |
| `required_chapter` | Integer || 1 | `0`<br>`2`<br>`3` |
| `required_difficulty` | Integer || 1 | `0`<br>`1`<br>`2` |
| [`reward_text`](./Strings.md#string-reward_text) | String || 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `destinations`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `boneyard` | Integer || 1 | `200`<br>`AREA_NAME_BONEYARD`<br>`[junkyard alley]` |
| `caves` | Integer || 1 | `200`<br>`AREA_NAME_CAVES`<br>`[sewers alley]` |
| `core` | Integer || 1 | `300`<br>`AREA_NAME_CORE`<br>`[bunker desert]` |
| `dimensionx` | Integer || 1 | `400`<br>`AREA_NAME_DIMENSIONX`<br>`[moon core bunker crater desert]` |
| `endoftime` | Integer || 1 | `500`<br>`AREA_NAME_ENDOFTIME`<br>`[jurassic theend iceage future lab]` |
| `jurassic` | Integer || 1 | `400`<br>`AREA_NAME_JURASSIC`<br>`[iceage lab]` |
| `meatworld` | Integer || 1 | `300`<br>`AREA_NAME_MEATWORLD`<br>`[caves boneyard junkyard sewers alley]` |
| `moon` | Integer || 1 | `300`<br>`AREA_NAME_MOON`<br>`[crater desert]` |
| `theend` | Integer || 1 | `400`<br>`AREA_NAME_THEEND`<br>`[future lab]` |

</details>


---


### Object: `prereqs`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`endoftime`](./Enums.md#enum-endoftime) | Enum || 1 | `500`<br>`AREA_NAME_ENDOFTIME`<br>`[jurassic theend iceage future lab]` |
| [`core`](./Enums.md#enum-core) | Enum || 1 | `300`<br>`AREA_NAME_CORE`<br>`[bunker desert]` |
| [`dimensionx`](./Enums.md#enum-dimensionx) | Enum || 1 | `400`<br>`AREA_NAME_DIMENSIONX`<br>`[moon core bunker crater desert]` |
| [`jurassic`](./Enums.md#enum-jurassic) | Enum || 1 | `400`<br>`AREA_NAME_JURASSIC`<br>`[iceage lab]` |
| [`moon`](./Enums.md#enum-moon) | Enum || 1 | `300`<br>`AREA_NAME_MOON`<br>`[crater desert]` |
| [`theend`](./Enums.md#enum-theend) | Enum || 1 | `400`<br>`AREA_NAME_THEEND`<br>`[future lab]` |

</details>


---