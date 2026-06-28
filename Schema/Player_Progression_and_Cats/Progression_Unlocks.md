# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see AUDIT_GAPS.md. For enum values, see [Enums.md](../Reference_and_Meta/Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Progression Unlocks

> **Associated Files:** `data/adventure_progression_unlocks.gon, data/npc_favor_unlocks.gon`


### Object: `ROOT`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 266

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 883 | `common`<br>`rare`<br>`cha` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 155 | Default<br>FormChange<br>Druid |
| [`popup`](./Progression_Unlocks.md#object-popup) | Object | An object defining a popup notification with prompt and optional unlock. | 266 | `{ . . . }` |
| [`intro`](../Reference_and_Meta/Arrays.md#array-intro) | Array | An object defining the introductory cutscene for the event, including title, cat selection, and visuals. | 239 | `[PersuasionDevice]` |
| [`complete_chapter_with_class`](../Reference_and_Meta/Arrays.md#array-complete_chapter_with_class) | Array | An array specifying [chapter, class] that must be completed to unlock this reward. | 129 | `[boneyard Butcher]`<br>`[boneyard Colorless]`<br>`[boneyard Druid]` |
| [`unlock_item_immediate`](../Reference_and_Meta/Enums.md#enum-unlock_item_immediate) | Enum | Specifies which item is unlocked immediately when this unlock condition is met. | 127 | `AnointingOil`<br>`BagOfBags`<br>`BagOfSeeds` |
| [`trigger_npc_sequence`](../Reference_and_Meta/Enums.md#enum-trigger_npc_sequence) | Enum | The name of an NPC dialogue sequence to trigger. | 53 | `beanies_begin_accepting_cats`<br>`beanies_bombquest_2`<br>`beanies_bombquest_3` |
| [`beat_house_boss`](../Reference_and_Meta/Enums.md#enum-beat_house_boss) | Enum | Specifies which house boss (or 'any') must be defeated to fulfill this unlock condition. | 48 | `any`<br>`guillotina_1`<br>`guillotina_2` |
| [`complete_chapter`](../Reference_and_Meta/Enums.md#enum-complete_chapter) | Enum | Specifies which chapter to mark as completed when this event triggers. | 37 | `alley`<br>`boneyard`<br>`bunker` |
| `required_difficulty` | Integer | The minimum difficulty level required to access this content (0 = easy, 1 = normal, etc.). | 36 | `0`<br>`1`<br>`2` |
| `repeat` | Integer | Determines how many times an event, song, or unlock can be triggered. Accepts a positive integer or the string "infinite". | 33 | `1`<br>`2`<br>`20` |
| [`beat_chapter_boss`](../Reference_and_Meta/Enums.md#enum-beat_chapter_boss) | Enum | Specifies the chapter boss that must be defeated to trigger the unlock. | 31 | `alley`<br>`boneyard`<br>`bunker` |
| [`unlock_song`](../Reference_and_Meta/Enums.md#enum-unlock_song) | Enum | Specifies the song that is unlocked. | 29 | `alone_in_the_dark`<br>`angel_wings`<br>`bolt_of_lightning` |
| [`unlock_ability`](../Reference_and_Meta/Enums.md#enum-unlock_ability) | Enum | Specifies the ability that is unlocked. | 28 | `BallOfSpiders`<br>`Bump`<br>`Ethereal` |
| [`unlock_passive`](../Reference_and_Meta/Enums.md#enum-unlock_passive) | Enum | Specifies the passive ability that is unlocked. | 28 | `AlphaStrike`<br>`ArmorSpecialist`<br>`Bouncer` |
| [`set_mapgen_flag`](../Reference_and_Meta/Enums.md#enum-set_mapgen_flag) | Enum | The name of a map generation flag to set when this event triggers. | 23 | `BoneyardUnlocked`<br>`BothObelisksUnlocked`<br>`BunkerUnlocked` |
| [`complete_checklist_with_class`](../Reference_and_Meta/Enums.md#enum-complete_checklist_with_class) | Enum | Specifies the class required to complete the checklist for this unlock. | 14 | `Butcher`<br>`Colorless`<br>`Druid` |
| [`unlock_quest_item`](../Reference_and_Meta/Enums.md#enum-unlock_quest_item) | Enum | Specifies the quest item that is unlocked. | 13 | `BlackShard`<br>`CryogenicTimeChamber_Empty`<br>`GuillotinasHead` |
| `repeatable` | Boolean | If true, this unlock or event can be triggered multiple times. | 10 | `true` |
| [`trigger_house_boss`](../Reference_and_Meta/Enums.md#enum-trigger_house_boss) | Enum | Specifies the house boss encounter that is triggered. | 10 | `guillotina_1`<br>`guillotina_2`<br>`guillotina_3` |
| [`complete_act_difficulty`](../Reference_and_Meta/Arrays.md#array-complete_act_difficulty) | Array | An array containing the act number and difficulty level that must be completed. | 9 | `[1 0]`<br>`[1 1]`<br>`[1 2]` |
| [`unlock_act_difficulty`](../Reference_and_Meta/Arrays.md#array-unlock_act_difficulty) | Array | An array containing the act number and difficulty level to unlock. | 9 | `[1 1]`<br>`[1 2]`<br>`[1 3]` |
| [`queue_cutscene_immediate`](../Reference_and_Meta/Enums.md#enum-queue_cutscene_immediate) | Enum | Determines which cutscene to play immediately upon queueing. | 8 | `caves_intro`<br>`core_intro`<br>`desert_intro` |
| `set_savefile_flag` | String | Determines which save file flag to set. | 6 | `AlienInvasionUnlocked`<br>`HauntedNightUnlocked`<br>`PlotFlag_Beanies_Homeless` |
| [`unlock_boss`](../Reference_and_Meta/Enums.md#enum-unlock_boss) | Enum | Determines which boss encounter to unlock. | 6 | `bumblefoot`<br>`gambit`<br>`infestedduo` |
| [`preempt_npc_sequence`](../Reference_and_Meta/Enums.md#enum-preempt_npc_sequence) | Enum | Specifies the NPC sequence to run before the current one. | 4 | `beanies_bombquest_2`<br>`beanies_bombquest_3`<br>`beanies_bombquest_amnesia` |
| [`fail_item_quest`](../Reference_and_Meta/Enums.md#enum-fail_item_quest) | Enum | Determines which item quest is marked as failed. | 4 | `JarOfChaos`<br>`JarOfRadiatedBlood`<br>`JarOfRadiation` |
| `fully_complete_difficulty` | Integer | The difficulty level required to be fully completed. | 4 | `0`<br>`1`<br>`2` |
| [`post_combat_cutscene`](../Reference_and_Meta/Enums.md#enum-post_combat_cutscene) | Enum | Determines which cutscene to play after a combat encounter. | 4 | `obelisk1_core`<br>`obelisk1_moon`<br>`obelisk2_core` |
| [`unlock_npc_tomorrow`](../Reference_and_Meta/Enums.md#enum-unlock_npc_tomorrow) | Enum | Specifies the NPC that will become available to interact with the next in-game day. | 4 | `beanies`<br>`jack`<br>`organgrinder` |
| [`visit_chapter`](../Reference_and_Meta/Enums.md#enum-visit_chapter) | Enum | Specifies the chapter area that the player must visit to trigger an event. | 4 | `dimensionx`<br>`future`<br>`iceage` |
| [`trigger_npc_sequence_tomorrow`](../Reference_and_Meta/Enums.md#enum-trigger_npc_sequence_tomorrow) | Enum | Determines which NPC sequence to schedule for the next day. | 3 | `butch_boneyard_intro`<br>`frank_caves_intro`<br>`jack_desert_intro` |
| `requires_monoclass_run` | Boolean | If true, this unlock requires the player to have completed a monoclass run. | 3 | `true` |
| [`requires_unlocked_npc`](../Reference_and_Meta/Enums.md#enum-requires_unlocked_npc) | Enum | Specifies the NPC that must be unlocked before this event or unlock can occur. | 3 | `frank`<br>`jack`<br>`tracy` |
| [`complete_chapters`](../Reference_and_Meta/Arrays.md#array-complete_chapters) | Array | An array of chapter names that must be completed to unlock this entity. | 3 | `[caves boneyard]`<br>`[core moon]` |
| [`reset_npc_sequence`](../Reference_and_Meta/Enums.md#enum-reset_npc_sequence) | Enum | Specifies the NPC sequence to reset for re-triggering. | 2 | `beanies_bombquest_2`<br>`beanies_bombquest_3`<br>`beanies_bombquest_begin` |
| [`beanies_quests_intro`](./Progression_Unlocks.md#object-beanies_quests_intro) | Object | Defines the initial dialog or quest-generation sequence for Dr. Beanies' quests. | 2 | `{ . . . }` |
| [`beanies_quests_repeat`](./Progression_Unlocks.md#object-beanies_quests_repeat) | Object | Defines the repeatable quest dialog or generator for Dr. Beanies. | 2 | `{ . . . }` |
| [`complete_adventure`](../Reference_and_Meta/Enums.md#enum-complete_adventure) | Enum | Specifies the location requirement (e.g., 'anywhere') for completing an adventure. | 2 | `anywhere` |
| [`frank_max_intro`](./Progression_Unlocks.md#object-frank_max_intro) | Object | Defines the dialog sequence and rewards for reaching max favor with Frank. | 2 | `{ . . . }` |
| [`frank_max_repeating`](./Progression_Unlocks.md#object-frank_max_repeating) | Object | Defines the repeatable dialog sequence and rewards for Frank at max favor. | 2 | `{ . . . }` |
| [`house_upgrade_4throom`](./Progression_Unlocks.md#object-house_upgrade_4throom) | Object | Defines the dialog and house upgrade for unlocking the 4th room. | 2 | `{ . . . }` |
| [`house_upgrade_attic`](./Progression_Unlocks.md#object-house_upgrade_attic) | Object | Defines the dialog and house upgrade for the attic. | 2 | `{ . . . }` |
| [`house_upgrade_largehouse`](./Progression_Unlocks.md#object-house_upgrade_largehouse) | Object | Defines the dialog and house upgrade for the large house. | 2 | `{ . . . }` |
| [`house_upgrade_mediumhouse`](./Progression_Unlocks.md#object-house_upgrade_mediumhouse) | Object | Defines the dialog and house upgrade for the medium house. | 2 | `{ . . . }` |
| [`jack_max_intro`](./Progression_Unlocks.md#object-jack_max_intro) | Object | Defines the dialog sequence and rewards for reaching max favor with Jack. | 2 | `{ . . . }` |
| [`jack_max_repeating`](./Progression_Unlocks.md#object-jack_max_repeating) | Object | Defines the repeatable dialog sequence and rewards for Jack at max favor. | 2 | `{ . . . }` |
| [`jack_shopupgrade1`](./Progression_Unlocks.md#object-jack_shopupgrade1) | Object | Defines the dialog and shop level up for Jack's first shop upgrade. | 2 | `{ . . . }` |
| [`jack_shopupgrade2`](./Progression_Unlocks.md#object-jack_shopupgrade2) | Object | Defines the dialog and shop level up for Jack's second shop upgrade. | 2 | `{ . . . }` |
| [`jack_shopupgrade3`](./Progression_Unlocks.md#object-jack_shopupgrade3) | Object | Defines the dialog and shop level up for Jack's third shop upgrade. | 2 | `{ . . . }` |
| [`jack_shopupgrade4`](./Progression_Unlocks.md#object-jack_shopupgrade4) | Object | Defines the dialog and shop level up for Jack's fourth shop upgrade. | 2 | `{ . . . }` |
| [`organ_max_intro`](./Progression_Unlocks.md#object-organ_max_intro) | Object | Defines the dialog sequence and rewards for reaching max favor with Organ Grinder. | 2 | `{ . . . }` |
| [`organ_max_repeating`](./Progression_Unlocks.md#object-organ_max_repeating) | Object | Defines the repeatable dialog sequence and rewards for Organ Grinder at max favor. | 2 | `{ . . . }` |
| [`organ_unlock`](./Progression_Unlocks.md#object-organ_unlock) | Object | Defines the dialog and shop level up for unlocking Organ Grinder. | 2 | `{ . . . }` |
| [`organ_upgrade1`](./Progression_Unlocks.md#object-organ_upgrade1) | Object | Defines the dialog and shop level up for Organ Grinder's first upgrade. | 2 | `{ . . . }` |
| [`organ_upgrade2`](./Progression_Unlocks.md#object-organ_upgrade2) | Object | Defines the dialog and shop level up for Organ Grinder's second upgrade. | 2 | `{ . . . }` |
| [`organ_upgrade3`](./Progression_Unlocks.md#object-organ_upgrade3) | Object | Defines the dialog and shop level up for Organ Grinder's third upgrade. | 2 | `{ . . . }` |
| [`organ_upgrade4`](./Progression_Unlocks.md#object-organ_upgrade4) | Object | Defines the dialog and shop level up for Organ Grinder's fourth upgrade. | 2 | `{ . . . }` |
| [`organ_upgrade5`](./Progression_Unlocks.md#object-organ_upgrade5) | Object | Defines the dialog and shop level up for Organ Grinder's fifth upgrade. | 2 | `{ . . . }` |
| [`organ_upgrade6`](./Progression_Unlocks.md#object-organ_upgrade6) | Object | Defines the dialog and shop level up for Organ Grinder's sixth upgrade. | 2 | `{ . . . }` |
| [`require_beat_house_boss`](../Reference_and_Meta/Enums.md#enum-require_beat_house_boss) | Enum | Specifies the name of the house boss that must be defeated to unlock this content. | 2 | `pyrophina`<br>`zaratana` |
| [`require_mapgen_flag`](../Reference_and_Meta/Enums.md#enum-require_mapgen_flag) | Enum | Specifies the map generation flag that must be present to unlock this content. | 2 | `CoreObeliskUnlocked`<br>`MoonObeliskUnlocked` |
| [`steven_milliontrashed`](./Progression_Unlocks.md#object-steven_milliontrashed) | Object | A dialogue sequence or favor reward configuration for the NPC Steven, triggered when the player has accumulated 1,000,000 favor. | 2 | `{ . . . }` |
| [`surviving_kaiju`](../Reference_and_Meta/Enums.md#enum-surviving_kaiju) | Enum | Specifies which kaiju entity survives a given quest event. | 2 | `pyrophina`<br>`zaratana` |
| [`tink_aggression`](./Progression_Unlocks.md#object-tink_aggression) | Object | A dialogue sequence or favor reward that unlocks the cat info panel for viewing a cat's aggression stat. | 2 | `{ . . . }` |
| [`tink_basestats`](./Progression_Unlocks.md#object-tink_basestats) | Object | A dialogue sequence or favor reward that unlocks the cat info panel for viewing a cat's base stats and stat modifications. | 2 | `{ . . . }` |
| [`tink_inbreeding`](./Progression_Unlocks.md#object-tink_inbreeding) | Object | A dialogue sequence or favor reward that unlocks the cat info panel for viewing a cat's inbreeding level and family tree. | 2 | `{ . . . }` |
| [`tink_max_intro`](./Progression_Unlocks.md#object-tink_max_intro) | Object | The first dialogue sequence and favor reward that plays when Tink reaches maximum favor. | 2 | `{ . . . }` |
| [`tink_max_repeating`](./Progression_Unlocks.md#object-tink_max_repeating) | Object | A repeating dialogue sequence and favor reward that plays when Tink is at maximum favor, cycling through random sub-sequences. | 2 | `{ . . . }` |
| [`tink_prettybow`](./Progression_Unlocks.md#object-tink_prettybow) | Object | A dialogue sequence and favor reward that grants the gift item TinksBow. | 2 | `{ . . . }` |
| [`tink_relationships`](./Progression_Unlocks.md#object-tink_relationships) | Object | A dialogue sequence or favor reward that unlocks the cat info panel for viewing a cat's relationships (loves and hates). | 2 | `{ . . . }` |
| [`tink_sexuality`](./Progression_Unlocks.md#object-tink_sexuality) | Object | A dialogue sequence or favor reward that unlocks the cat info panel for viewing a cat's libido and sexual orientation flags. | 2 | `{ . . . }` |
| [`tink_tags`](./Progression_Unlocks.md#object-tink_tags) | Object | A dialogue sequence or favor reward that unlocks the ability to manually add symbols to a cat's name. | 2 | `{ . . . }` |
| [`tracy_blankcollar1`](./Progression_Unlocks.md#object-tracy_blankcollar1) | Object | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 2 | `{ . . . }` |
| [`tracy_blankcollar2`](./Progression_Unlocks.md#object-tracy_blankcollar2) | Object | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 2 | `{ . . . }` |
| [`tracy_blankcollar3`](./Progression_Unlocks.md#object-tracy_blankcollar3) | Object | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 2 | `{ . . . }` |
| [`tracy_foodstorage1`](./Progression_Unlocks.md#object-tracy_foodstorage1) | Object | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 2 | `{ . . . }` |
| [`tracy_foodstorage10`](./Progression_Unlocks.md#object-tracy_foodstorage10) | Object | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 2 | `{ . . . }` |
| [`tracy_foodstorage2`](./Progression_Unlocks.md#object-tracy_foodstorage2) | Object | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 2 | `{ . . . }` |
| [`tracy_foodstorage3`](./Progression_Unlocks.md#object-tracy_foodstorage3) | Object | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 2 | `{ . . . }` |
| [`tracy_foodstorage4`](./Progression_Unlocks.md#object-tracy_foodstorage4) | Object | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 2 | `{ . . . }` |
| [`tracy_foodstorage5`](./Progression_Unlocks.md#object-tracy_foodstorage5) | Object | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 2 | `{ . . . }` |
| [`tracy_foodstorage6`](./Progression_Unlocks.md#object-tracy_foodstorage6) | Object | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 2 | `{ . . . }` |
| [`tracy_foodstorage7`](./Progression_Unlocks.md#object-tracy_foodstorage7) | Object | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 2 | `{ . . . }` |
| [`tracy_foodstorage8`](./Progression_Unlocks.md#object-tracy_foodstorage8) | Object | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 2 | `{ . . . }` |
| [`tracy_foodstorage9`](./Progression_Unlocks.md#object-tracy_foodstorage9) | Object | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 2 | `{ . . . }` |
| [`tracy_idol1`](./Progression_Unlocks.md#object-tracy_idol1) | Object | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 2 | `{ . . . }` |
| [`tracy_idol2`](./Progression_Unlocks.md#object-tracy_idol2) | Object | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 2 | `{ . . . }` |
| [`tracy_idol3`](./Progression_Unlocks.md#object-tracy_idol3) | Object | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 2 | `{ . . . }` |
| [`tracy_idol4`](./Progression_Unlocks.md#object-tracy_idol4) | Object | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 2 | `{ . . . }` |
| [`tracy_idol5`](./Progression_Unlocks.md#object-tracy_idol5) | Object | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 2 | `{ . . . }` |
| [`tracy_idol6`](./Progression_Unlocks.md#object-tracy_idol6) | Object | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 2 | `{ . . . }` |
| [`tracy_idol7`](./Progression_Unlocks.md#object-tracy_idol7) | Object | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 2 | `{ . . . }` |
| [`tracy_max_intro`](./Progression_Unlocks.md#object-tracy_max_intro) | Object | The first dialogue sequence and bonus rare item reward that plays when Tracy reaches maximum favor. | 2 | `{ . . . }` |
| [`tracy_max_repeating`](./Progression_Unlocks.md#object-tracy_max_repeating) | Object | A repeating dialogue sequence and favor reward that plays when Tracy is at maximum favor, cycling through random sub-sequences. | 2 | `{ . . . }` |
| [`unlock_levelgroup`](../Reference_and_Meta/Enums.md#enum-unlock_levelgroup) | Enum | Specifies the level group to unlock when a given condition is met. | 2 | `bigsharklevels` |
| [`upgrade_storage_1`](./Progression_Unlocks.md#object-upgrade_storage_1) | Object | A dialogue sequence and storage expansion reward for Butch, requiring act 0 and chapter 0. | 2 | `{ . . . }` |
| [`upgrade_storage_2`](./Progression_Unlocks.md#object-upgrade_storage_2) | Object | A dialogue sequence and storage expansion reward for Butch, requiring act 1 and chapter 2. | 2 | `{ . . . }` |
| [`upgrade_storage_3`](./Progression_Unlocks.md#object-upgrade_storage_3) | Object | A dialogue sequence and storage expansion reward for Butch, requiring act 1 and chapter 3. | 2 | `{ . . . }` |
| [`upgrade_storage_4`](./Progression_Unlocks.md#object-upgrade_storage_4) | Object | A dialogue sequence and storage expansion reward for Butch, requiring act 2 and chapter 2. | 2 | `{ . . . }` |
| [`upgrade_storage_5`](./Progression_Unlocks.md#object-upgrade_storage_5) | Object | A dialogue sequence and storage expansion reward for Butch, requiring act 2 and chapter 3. | 2 | `{ . . . }` |
| [`upgrade_storage_6`](./Progression_Unlocks.md#object-upgrade_storage_6) | Object | A dialogue sequence and storage expansion reward for Butch, requiring act 3 and chapter 2. | 2 | `{ . . . }` |
| [`upgrade_storage_7`](./Progression_Unlocks.md#object-upgrade_storage_7) | Object | A dialogue sequence and storage expansion reward for Butch, requiring act 3 and chapter 3. | 2 | `{ . . . }` |
| [`upgrade_storage_repeating_crazy`](./Progression_Unlocks.md#object-upgrade_storage_repeating_crazy) | Object | A repeating dialogue sequence for Butch's storage upgrade at crazy difficulty, granting one storage expansion. | 2 | `{ . . . }` |
| [`upgrade_storage_repeating_hard`](./Progression_Unlocks.md#object-upgrade_storage_repeating_hard) | Object | A repeating dialogue sequence for Butch's storage upgrade at hard difficulty, granting one storage expansion. | 2 | `{ . . . }` |
| [`upgrade_storage_repeating_impossible`](./Progression_Unlocks.md#object-upgrade_storage_repeating_impossible) | Object | A repeating dialogue sequence for Butch's storage upgrade at impossible difficulty, granting one storage expansion. | 2 | `{ . . . }` |
| [`upgrade_storage_repeating_intro`](./Progression_Unlocks.md#object-upgrade_storage_repeating_intro) | Object | The introductory dialogue sequence and reward when Butch maxes out storage capacity. | 2 | `{ . . . }` |
| [`upgrade_storage_repeating_normal`](./Progression_Unlocks.md#object-upgrade_storage_repeating_normal) | Object | A repeating dialogue sequence for Butch's storage upgrade at normal difficulty, granting one storage expansion. | 2 | `{ . . . }` |
| [`destinations`](./Progression_Unlocks.md#object-destinations) | Object | Specifies the list of areas and their associated coin rewards for Beanie's quest destinations. | 1 | `{ . . . }` |
| [`fail_adventure`](../Reference_and_Meta/Enums.md#enum-fail_adventure) | Enum | Specifies a trigger that causes the current adventure to fail, with a location parameter (e.g., 'anywhere'). | 1 | `anywhere` |
| [`finish_quest`](../Reference_and_Meta/Enums.md#enum-finish_quest) | Enum | Specifies the name of the quest to mark as finished. | 1 | `JarOfChaos` |
| `increment_savefile_counter` | String | Specifies the GameStat counter to increment when this sequence completes. | 1 | `GameStat_CountNukeQuestCompletions` |
| [`prereqs`](./Progression_Unlocks.md#object-prereqs) | Object | Object mapping quest or unlock names to their prerequisite mapflags or conditions. | 1 | `{ . . . }` |
| `requires_hard_path` | Boolean | If true, this unlock requires the player to be on the hard path. | 1 | `true` |
| [`reset_unlock`](../Reference_and_Meta/Enums.md#enum-reset_unlock) | Enum | Specifies the unlock key to reset upon completing this unlock chain. | 1 | `nuke_quest_begin` |
| [`unlock_item`](../Reference_and_Meta/Enums.md#enum-unlock_item) | Enum | The name of the item unlocked by this event. | 1 | `MomsKnife` |
| [`main_pool`](../Reference_and_Meta/Arrays.md#array-main_pool) | Array | A list of quest IDs or objects that form the primary quest pool for a beanies quest node. | 1 | `[` |

</details>


---


### Object: `popup`


**Definition:** An object defining a popup notification with prompt and optional unlock.
**Total Count:** 266

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 266 | `common`<br>`rare`<br>`cha` |
| `immediate` | Boolean | If true, the action (e.g., attack) occurs instantly without waiting for the unit's turn in the initiative order. | 221 | `false`<br>`true` |
| `frame` | Integer | The sprite frame index to display. | 159 | `1`<br>`10`<br>`100` |

</details>


---


### Object: `tracy_special_item`


**Definition:** An object defining a special item offered by Tracy, including its type, cost, and associated reward text.
**Total Count:** 22

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`tracy_blankcollar1`](#object-tracy_blankcollar1), [`tracy_blankcollar2`](#object-tracy_blankcollar2), [`tracy_blankcollar3`](#object-tracy_blankcollar3), [`tracy_foodstorage1`](#object-tracy_foodstorage1), [`tracy_foodstorage10`](#object-tracy_foodstorage10), [`tracy_foodstorage2`](#object-tracy_foodstorage2), [`tracy_foodstorage3`](#object-tracy_foodstorage3), [`tracy_foodstorage4`](#object-tracy_foodstorage4), [`tracy_foodstorage5`](#object-tracy_foodstorage5), [`tracy_foodstorage6`](#object-tracy_foodstorage6), [`tracy_foodstorage7`](#object-tracy_foodstorage7), [`tracy_foodstorage8`](#object-tracy_foodstorage8), [`tracy_foodstorage9`](#object-tracy_foodstorage9), [`tracy_idol1`](#object-tracy_idol1), [`tracy_idol2`](#object-tracy_idol2), [`tracy_idol3`](#object-tracy_idol3), [`tracy_idol4`](#object-tracy_idol4), [`tracy_idol5`](#object-tracy_idol5), [`tracy_idol6`](#object-tracy_idol6), [`tracy_idol7`](#object-tracy_idol7), [`tracy_max_intro`](#object-tracy_max_intro), [`tracy_max_repeating`](#object-tracy_max_repeating)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 22 | `{ . . . }` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 22 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `beanies_quests_intro`


**Definition:** Defines the initial dialog or quest-generation sequence for Dr. Beanies' quests.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`generate_beanies_quest`](../Reference_and_Meta/Enums.md#enum-generate_beanies_quest) | Enum | Specifies which quest pool (e.g., 'main_pool', 'intro') to generate a quest from. | 1 | `intro`<br>`main_pool` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `beanies_quests_repeat`


**Definition:** Defines the repeatable quest dialog or generator for Dr. Beanies.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`generate_beanies_quest`](../Reference_and_Meta/Enums.md#enum-generate_beanies_quest) | Enum | Specifies which quest pool (e.g., 'main_pool', 'intro') to generate a quest from. | 1 | `intro`<br>`main_pool` |
| [`level_display`](../Reference_and_Meta/Enums.md#enum-level_display) | Enum | Specifies how to display the current level of a repeating upgrade (e.g., 'max'). | 1 | `max` |
| [`repeat`](../Reference_and_Meta/Enums.md#enum-repeat) | Enum | Determines how many times an event, song, or unlock can be triggered. Accepts a positive integer or the string "infinite". | 1 | `1`<br>`2`<br>`20` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `frank_max_intro`


**Definition:** Defines the dialog sequence and rewards for reaching max favor with Frank.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`gift_item_from_pool`](../Reference_and_Meta/Enums.md#enum-gift_item_from_pool) | Enum | Specifies the item pool from which to gift an item. | 1 | `parasites` |
| [`level_display`](../Reference_and_Meta/Enums.md#enum-level_display) | Enum | Specifies how to display the current level of a repeating upgrade (e.g., 'max'). | 1 | `max` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `frank_max_repeating`


**Definition:** Defines the repeatable dialog sequence and rewards for Frank at max favor.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`gift_item_from_pool`](../Reference_and_Meta/Enums.md#enum-gift_item_from_pool) | Enum | Specifies the item pool from which to gift an item. | 1 | `parasites` |
| [`level_display`](../Reference_and_Meta/Enums.md#enum-level_display) | Enum | Specifies how to display the current level of a repeating upgrade (e.g., 'max'). | 1 | `max` |
| [`repeat`](../Reference_and_Meta/Enums.md#enum-repeat) | Enum | Determines how many times an event, song, or unlock can be triggered. Accepts a positive integer or the string "infinite". | 1 | `1`<br>`2`<br>`20` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `house_upgrade_4throom`


**Definition:** Defines the dialog and house upgrade for unlocking the 4th room.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`house_upgrade`](../Reference_and_Meta/Enums.md#enum-house_upgrade) | Enum | Specifies the name of the house upgrade to apply. | 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `house_upgrade_attic`


**Definition:** Defines the dialog and house upgrade for the attic.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`house_upgrade`](../Reference_and_Meta/Enums.md#enum-house_upgrade) | Enum | Specifies the name of the house upgrade to apply. | 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `house_upgrade_largehouse`


**Definition:** Defines the dialog and house upgrade for the large house.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`house_upgrade`](../Reference_and_Meta/Enums.md#enum-house_upgrade) | Enum | Specifies the name of the house upgrade to apply. | 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `house_upgrade_mediumhouse`


**Definition:** Defines the dialog and house upgrade for the medium house.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`house_upgrade`](../Reference_and_Meta/Enums.md#enum-house_upgrade) | Enum | Specifies the name of the house upgrade to apply. | 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `jack_max_intro`


**Definition:** Defines the dialog sequence and rewards for reaching max favor with Jack.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`level_display`](../Reference_and_Meta/Enums.md#enum-level_display) | Enum | Specifies how to display the current level of a repeating upgrade (e.g., 'max'). | 1 | `max` |
| `rep_reward_count` | Integer | The number of reputation rewards granted. | 1 | `1` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `jack_max_repeating`


**Definition:** Defines the repeatable dialog sequence and rewards for Jack at max favor.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`level_display`](../Reference_and_Meta/Enums.md#enum-level_display) | Enum | Specifies how to display the current level of a repeating upgrade (e.g., 'max'). | 1 | `max` |
| `rep_reward_count` | Integer | The number of reputation rewards granted. | 1 | `1` |
| [`repeat`](../Reference_and_Meta/Enums.md#enum-repeat) | Enum | Determines how many times an event, song, or unlock can be triggered. Accepts a positive integer or the string "infinite". | 1 | `1`<br>`2`<br>`20` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `jack_shopupgrade1`


**Definition:** Defines the dialog and shop level up for Jack's first shop upgrade.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |

</details>


---


### Object: `jack_shopupgrade2`


**Definition:** Defines the dialog and shop level up for Jack's second shop upgrade.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |

</details>


---


### Object: `jack_shopupgrade3`


**Definition:** Defines the dialog and shop level up for Jack's third shop upgrade.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |

</details>


---


### Object: `jack_shopupgrade4`


**Definition:** Defines the dialog and shop level up for Jack's fourth shop upgrade.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |

</details>


---


### Object: `organ_max_intro`


**Definition:** Defines the dialog sequence and rewards for reaching max favor with Organ Grinder.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`gift_item`](../Reference_and_Meta/Enums.md#enum-gift_item) | Enum | The identifier of the item to gift to the player. | 1 | `TinksBow`<br>`disorder_needle` |
| [`level_display`](../Reference_and_Meta/Enums.md#enum-level_display) | Enum | Specifies how to display the current level of a repeating upgrade (e.g., 'max'). | 1 | `max` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `organ_max_repeating`


**Definition:** Defines the repeatable dialog sequence and rewards for Organ Grinder at max favor.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`gift_item`](../Reference_and_Meta/Enums.md#enum-gift_item) | Enum | The identifier of the item to gift to the player. | 1 | `TinksBow`<br>`disorder_needle` |
| [`level_display`](../Reference_and_Meta/Enums.md#enum-level_display) | Enum | Specifies how to display the current level of a repeating upgrade (e.g., 'max'). | 1 | `max` |
| [`repeat`](../Reference_and_Meta/Enums.md#enum-repeat) | Enum | Determines how many times an event, song, or unlock can be triggered. Accepts a positive integer or the string "infinite". | 1 | `1`<br>`2`<br>`20` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `organ_unlock`


**Definition:** Defines the dialog and shop level up for unlocking Organ Grinder.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |

</details>


---


### Object: `organ_upgrade1`


**Definition:** Defines the dialog and shop level up for Organ Grinder's first upgrade.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |

</details>


---


### Object: `organ_upgrade2`


**Definition:** Defines the dialog and shop level up for Organ Grinder's second upgrade.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |

</details>


---


### Object: `organ_upgrade3`


**Definition:** Defines the dialog and shop level up for Organ Grinder's third upgrade.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |

</details>


---


### Object: `organ_upgrade4`


**Definition:** Defines the dialog and shop level up for Organ Grinder's fourth upgrade.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |

</details>


---


### Object: `organ_upgrade5`


**Definition:** Defines the dialog and shop level up for Organ Grinder's fifth upgrade.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |

</details>


---


### Object: `organ_upgrade6`


**Definition:** Defines the dialog and shop level up for Organ Grinder's sixth upgrade.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |

</details>


---


### Object: `steven_milliontrashed`


**Definition:** A dialogue sequence or favor reward configuration for the NPC Steven, triggered when the player has accumulated 1,000,000 favor.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`level_display`](../Reference_and_Meta/Enums.md#enum-level_display) | Enum | Specifies how to display the current level of a repeating upgrade (e.g., 'max'). | 1 | `max` |
| [`repeat`](../Reference_and_Meta/Enums.md#enum-repeat) | Enum | Determines how many times an event, song, or unlock can be triggered. Accepts a positive integer or the string "infinite". | 1 | `1`<br>`2`<br>`20` |

</details>


---


### Object: `tink_aggression`


**Definition:** A dialogue sequence or favor reward that unlocks the cat info panel for viewing a cat's aggression stat.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `set_savefile_flag` | String | Determines which save file flag to set. | 1 | `AlienInvasionUnlocked`<br>`HauntedNightUnlocked`<br>`PlotFlag_Beanies_Homeless` |

</details>


---


### Object: `tink_basestats`


**Definition:** A dialogue sequence or favor reward that unlocks the cat info panel for viewing a cat's base stats and stat modifications.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `set_savefile_flag` | String | Determines which save file flag to set. | 1 | `AlienInvasionUnlocked`<br>`HauntedNightUnlocked`<br>`PlotFlag_Beanies_Homeless` |

</details>


---


### Object: `tink_inbreeding`


**Definition:** A dialogue sequence or favor reward that unlocks the cat info panel for viewing a cat's inbreeding level and family tree.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `set_savefile_flag` | String | Determines which save file flag to set. | 1 | `AlienInvasionUnlocked`<br>`HauntedNightUnlocked`<br>`PlotFlag_Beanies_Homeless` |

</details>


---


### Object: `tink_max_intro`


**Definition:** The first dialogue sequence and favor reward that plays when Tink reaches maximum favor.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `coins` | Integer | The amount of coins required to use this ability or obtained from this source. | 1 | `1`<br>`2`<br>`25` |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`level_display`](../Reference_and_Meta/Enums.md#enum-level_display) | Enum | Specifies how to display the current level of a repeating upgrade (e.g., 'max'). | 1 | `max` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `tink_max_repeating`


**Definition:** A repeating dialogue sequence and favor reward that plays when Tink is at maximum favor, cycling through random sub-sequences.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `coins` | Integer | The amount of coins required to use this ability or obtained from this source. | 1 | `1`<br>`2`<br>`25` |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`level_display`](../Reference_and_Meta/Enums.md#enum-level_display) | Enum | Specifies how to display the current level of a repeating upgrade (e.g., 'max'). | 1 | `max` |
| [`repeat`](../Reference_and_Meta/Enums.md#enum-repeat) | Enum | Determines how many times an event, song, or unlock can be triggered. Accepts a positive integer or the string "infinite". | 1 | `1`<br>`2`<br>`20` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `tink_prettybow`


**Definition:** A dialogue sequence and favor reward that grants the gift item TinksBow.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`gift_item`](../Reference_and_Meta/Enums.md#enum-gift_item) | Enum | The identifier of the item to gift to the player. | 1 | `TinksBow`<br>`disorder_needle` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `tink_relationships`


**Definition:** A dialogue sequence or favor reward that unlocks the cat info panel for viewing a cat's relationships (loves and hates).
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `set_savefile_flag` | String | Determines which save file flag to set. | 1 | `AlienInvasionUnlocked`<br>`HauntedNightUnlocked`<br>`PlotFlag_Beanies_Homeless` |

</details>


---


### Object: `tink_sexuality`


**Definition:** A dialogue sequence or favor reward that unlocks the cat info panel for viewing a cat's libido and sexual orientation flags.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `set_savefile_flag` | String | Determines which save file flag to set. | 1 | `AlienInvasionUnlocked`<br>`HauntedNightUnlocked`<br>`PlotFlag_Beanies_Homeless` |

</details>


---


### Object: `tink_tags`


**Definition:** A dialogue sequence or favor reward that unlocks the ability to manually add symbols to a cat's name.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `set_savefile_flag` | String | Determines which save file flag to set. | 1 | `AlienInvasionUnlocked`<br>`HauntedNightUnlocked`<br>`PlotFlag_Beanies_Homeless` |

</details>


---


### Object: `tracy_blankcollar1`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `tracy_blankcollar2`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `tracy_blankcollar3`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `tracy_foodstorage1`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `tracy_foodstorage10`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `tracy_foodstorage2`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `tracy_foodstorage3`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `tracy_foodstorage4`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `tracy_foodstorage5`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `tracy_foodstorage6`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `tracy_foodstorage7`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `tracy_foodstorage8`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `tracy_foodstorage9`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `tracy_idol1`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `tracy_idol2`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `tracy_idol3`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `tracy_idol4`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `tracy_idol5`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `tracy_idol6`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `tracy_idol7`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `tracy_max_intro`


**Definition:** The first dialogue sequence and bonus rare item reward that plays when Tracy reaches maximum favor.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`level_display`](../Reference_and_Meta/Enums.md#enum-level_display) | Enum | Specifies how to display the current level of a repeating upgrade (e.g., 'max'). | 1 | `max` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `tracy_max_repeating`


**Definition:** A repeating dialogue sequence and favor reward that plays when Tracy is at maximum favor, cycling through random sub-sequences.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`level_display`](../Reference_and_Meta/Enums.md#enum-level_display) | Enum | Specifies how to display the current level of a repeating upgrade (e.g., 'max'). | 1 | `max` |
| [`repeat`](../Reference_and_Meta/Enums.md#enum-repeat) | Enum | Determines how many times an event, song, or unlock can be triggered. Accepts a positive integer or the string "infinite". | 1 | `1`<br>`2`<br>`20` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `upgrade_storage_1`


**Definition:** A dialogue sequence and storage expansion reward for Butch, requiring act 0 and chapter 0.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| `required_act` | Integer | The act number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`1`<br>`2` |
| `required_chapter` | Integer | The chapter number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`2`<br>`3` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `storage_expansion` | Integer | The number of additional storage slots granted by this upgrade. | 1 | `1` |

</details>


---


### Object: `upgrade_storage_2`


**Definition:** A dialogue sequence and storage expansion reward for Butch, requiring act 1 and chapter 2.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| `required_act` | Integer | The act number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`1`<br>`2` |
| `required_chapter` | Integer | The chapter number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`2`<br>`3` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `storage_expansion` | Integer | The number of additional storage slots granted by this upgrade. | 1 | `1` |

</details>


---


### Object: `upgrade_storage_3`


**Definition:** A dialogue sequence and storage expansion reward for Butch, requiring act 1 and chapter 3.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| `required_act` | Integer | The act number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`1`<br>`2` |
| `required_chapter` | Integer | The chapter number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`2`<br>`3` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `storage_expansion` | Integer | The number of additional storage slots granted by this upgrade. | 1 | `1` |

</details>


---


### Object: `upgrade_storage_4`


**Definition:** A dialogue sequence and storage expansion reward for Butch, requiring act 2 and chapter 2.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| `required_act` | Integer | The act number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`1`<br>`2` |
| `required_chapter` | Integer | The chapter number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`2`<br>`3` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `storage_expansion` | Integer | The number of additional storage slots granted by this upgrade. | 1 | `1` |

</details>


---


### Object: `upgrade_storage_5`


**Definition:** A dialogue sequence and storage expansion reward for Butch, requiring act 2 and chapter 3.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| `required_act` | Integer | The act number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`1`<br>`2` |
| `required_chapter` | Integer | The chapter number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`2`<br>`3` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `storage_expansion` | Integer | The number of additional storage slots granted by this upgrade. | 1 | `1` |

</details>


---


### Object: `upgrade_storage_6`


**Definition:** A dialogue sequence and storage expansion reward for Butch, requiring act 3 and chapter 2.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| `required_act` | Integer | The act number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`1`<br>`2` |
| `required_chapter` | Integer | The chapter number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`2`<br>`3` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `storage_expansion` | Integer | The number of additional storage slots granted by this upgrade. | 1 | `1` |

</details>


---


### Object: `upgrade_storage_7`


**Definition:** A dialogue sequence and storage expansion reward for Butch, requiring act 3 and chapter 3.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| `required_act` | Integer | The act number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`1`<br>`2` |
| `required_chapter` | Integer | The chapter number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`2`<br>`3` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `storage_expansion` | Integer | The number of additional storage slots granted by this upgrade. | 1 | `1` |

</details>


---


### Object: `upgrade_storage_repeating_crazy`


**Definition:** A repeating dialogue sequence for Butch's storage upgrade at crazy difficulty, granting one storage expansion.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`level_display`](../Reference_and_Meta/Enums.md#enum-level_display) | Enum | Specifies how to display the current level of a repeating upgrade (e.g., 'max'). | 1 | `max` |
| `rep_reward_count` | Integer | The number of reputation rewards granted. | 1 | `1` |
| `repeat` | Integer | Determines how many times an event, song, or unlock can be triggered. Accepts a positive integer or the string "infinite". | 1 | `1`<br>`2`<br>`20` |
| `required_act` | Integer | The act number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`1`<br>`2` |
| `required_chapter` | Integer | The chapter number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`2`<br>`3` |
| `required_difficulty` | Integer | The minimum difficulty level required to access this content (0 = easy, 1 = normal, etc.). | 1 | `0`<br>`1`<br>`2` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `upgrade_storage_repeating_hard`


**Definition:** A repeating dialogue sequence for Butch's storage upgrade at hard difficulty, granting one storage expansion.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`level_display`](../Reference_and_Meta/Enums.md#enum-level_display) | Enum | Specifies how to display the current level of a repeating upgrade (e.g., 'max'). | 1 | `max` |
| `rep_reward_count` | Integer | The number of reputation rewards granted. | 1 | `1` |
| `repeat` | Integer | Determines how many times an event, song, or unlock can be triggered. Accepts a positive integer or the string "infinite". | 1 | `1`<br>`2`<br>`20` |
| `required_act` | Integer | The act number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`1`<br>`2` |
| `required_chapter` | Integer | The chapter number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`2`<br>`3` |
| `required_difficulty` | Integer | The minimum difficulty level required to access this content (0 = easy, 1 = normal, etc.). | 1 | `0`<br>`1`<br>`2` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `upgrade_storage_repeating_impossible`


**Definition:** A repeating dialogue sequence for Butch's storage upgrade at impossible difficulty, granting one storage expansion.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`level_display`](../Reference_and_Meta/Enums.md#enum-level_display) | Enum | Specifies how to display the current level of a repeating upgrade (e.g., 'max'). | 1 | `max` |
| `rep_reward_count` | Integer | The number of reputation rewards granted. | 1 | `1` |
| [`repeat`](../Reference_and_Meta/Enums.md#enum-repeat) | Enum | Determines how many times an event, song, or unlock can be triggered. Accepts a positive integer or the string "infinite". | 1 | `1`<br>`2`<br>`20` |
| `required_act` | Integer | The act number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`1`<br>`2` |
| `required_chapter` | Integer | The chapter number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`2`<br>`3` |
| `required_difficulty` | Integer | The minimum difficulty level required to access this content (0 = easy, 1 = normal, etc.). | 1 | `0`<br>`1`<br>`2` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `upgrade_storage_repeating_intro`


**Definition:** The introductory dialogue sequence and reward when Butch maxes out storage capacity.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`level_display`](../Reference_and_Meta/Enums.md#enum-level_display) | Enum | Specifies how to display the current level of a repeating upgrade (e.g., 'max'). | 1 | `max` |
| `rep_reward_count` | Integer | The number of reputation rewards granted. | 1 | `1` |
| `required_act` | Integer | The act number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`1`<br>`2` |
| `required_chapter` | Integer | The chapter number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`2`<br>`3` |
| `required_difficulty` | Integer | The minimum difficulty level required to access this content (0 = easy, 1 = normal, etc.). | 1 | `0`<br>`1`<br>`2` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `upgrade_storage_repeating_normal`


**Definition:** A repeating dialogue sequence for Butch's storage upgrade at normal difficulty, granting one storage expansion.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`level_display`](../Reference_and_Meta/Enums.md#enum-level_display) | Enum | Specifies how to display the current level of a repeating upgrade (e.g., 'max'). | 1 | `max` |
| `rep_reward_count` | Integer | The number of reputation rewards granted. | 1 | `1` |
| `repeat` | Integer | Determines how many times an event, song, or unlock can be triggered. Accepts a positive integer or the string "infinite". | 1 | `1`<br>`2`<br>`20` |
| `required_act` | Integer | The act number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`1`<br>`2` |
| `required_chapter` | Integer | The chapter number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`2`<br>`3` |
| `required_difficulty` | Integer | The minimum difficulty level required to access this content (0 = easy, 1 = normal, etc.). | 1 | `0`<br>`1`<br>`2` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `destinations`


**Definition:** Specifies the list of areas and their associated coin rewards for Beanie's quest destinations.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `boneyard` | Integer | Specifies the name, map flag, or connection for the Boneyard area. | 1 | `200`<br>`AREA_NAME_BONEYARD`<br>`[junkyard alley]` |
| `caves` | Integer | Specifies the name, map flag, or connection for the Caves area. | 1 | `200`<br>`AREA_NAME_CAVES`<br>`[sewers alley]` |
| `core` | Integer | Specifies the name, map flag, or connection for the Core area. | 1 | `300`<br>`AREA_NAME_CORE`<br>`[bunker desert]` |
| `dimensionx` | Integer | An enum specifying the Dimension X chapter area, or an object with its specific properties. | 1 | `400`<br>`AREA_NAME_DIMENSIONX`<br>`[moon core bunker crater desert]` |
| `endoftime` | Integer | Configures various attributes of the End of Time area, depending on context. | 1 | `500`<br>`AREA_NAME_ENDOFTIME`<br>`[jurassic theend iceage future lab]` |
| `jurassic` | Integer | Specifies the name, map flag, or connection for the Jurassic area. | 1 | `400`<br>`AREA_NAME_JURASSIC`<br>`[iceage lab]` |
| `meatworld` | Integer | An enum specifying the Meatworld chapter area, or an object with its specific properties. | 1 | `300`<br>`AREA_NAME_MEATWORLD`<br>`[caves boneyard junkyard sewers alley]` |
| `moon` | Integer | Specifies the name, map flag, or connection for the Moon area. | 1 | `300`<br>`AREA_NAME_MOON`<br>`[crater desert]` |
| `theend` | Integer | Specifies the name, map flag, or connection for The End area. | 1 | `400`<br>`AREA_NAME_THEEND`<br>`[future lab]` |

</details>


---


### Object: `prereqs`


**Definition:** Object mapping quest or unlock names to their prerequisite mapflags or conditions.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`endoftime`](../Reference_and_Meta/Enums.md#enum-endoftime) | Enum | Configures various attributes of the End of Time area, depending on context. | 1 | `500`<br>`AREA_NAME_ENDOFTIME`<br>`[jurassic theend iceage future lab]` |
| [`core`](../Reference_and_Meta/Enums.md#enum-core) | Enum | Specifies the name, map flag, or connection for the Core area. | 1 | `300`<br>`AREA_NAME_CORE`<br>`[bunker desert]` |
| [`dimensionx`](../Reference_and_Meta/Enums.md#enum-dimensionx) | Enum | An enum specifying the Dimension X chapter area, or an object with its specific properties. | 1 | `400`<br>`AREA_NAME_DIMENSIONX`<br>`[moon core bunker crater desert]` |
| [`jurassic`](../Reference_and_Meta/Enums.md#enum-jurassic) | Enum | Specifies the name, map flag, or connection for the Jurassic area. | 1 | `400`<br>`AREA_NAME_JURASSIC`<br>`[iceage lab]` |
| [`moon`](../Reference_and_Meta/Enums.md#enum-moon) | Enum | Specifies the name, map flag, or connection for the Moon area. | 1 | `300`<br>`AREA_NAME_MOON`<br>`[crater desert]` |
| [`theend`](../Reference_and_Meta/Enums.md#enum-theend) | Enum | Specifies the name, map flag, or connection for The End area. | 1 | `400`<br>`AREA_NAME_THEEND`<br>`[future lab]` |

</details>


---