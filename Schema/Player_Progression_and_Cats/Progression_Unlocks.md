---
title: "Progression Unlocks Schema"
description: "Conditions and flags for unlocking content."
---

# Progression Unlocks Schema


<details open>
<summary><strong>Quick Navigation</strong></summary>

<table>
  <tr>
    <td width="22%"><strong>Core Entities & Combat</strong></td>
    <td><a href="../Core_Entities_and_Combat/Abilities_and_Spells.md">Abilities & Spells</a> • <a href="../Core_Entities_and_Combat/Characters_and_Bosses.md">Characters & Bosses</a> • <a href="../Core_Entities_and_Combat/Items_and_Equipment.md">Items & Equipment</a> • <a href="../Core_Entities_and_Combat/Passives_and_Statuses.md">Passives & Statuses</a> • <a href="../Core_Entities_and_Combat/Elite_Buffs.md">Elite Buffs</a> • <a href="../Core_Entities_and_Combat/Enemy_AI.md">Enemy AI</a> • <a href="../Core_Entities_and_Combat/Status_Effect_Keywords.md">Status Keywords</a></td>
  </tr>
  <tr>
    <td><strong>Engine Scripts & Logic</strong></td>
    <td><a href="../Engine_Scripts_and_Logic/Engine_LogicKeys.md">Logic Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_EventKeys.md">Event Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_DamagingKeys.md">Damaging Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md">Status & Passive Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_GlobalModifierKeys.md">Global Modifiers</a> • <a href="../Engine_Scripts_and_Logic/Math_Equations.md">Math Equations</a></td>
  </tr>
  <tr>
    <td><strong>Player Progression & Cats</strong></td>
    <td><a href="../Player_Progression_and_Cats/Cat_Classes.md">Cat Classes</a> • <a href="../Player_Progression_and_Cats/Cat_Mutations.md">Cat Mutations</a> • <a href="../Player_Progression_and_Cats/Custom_Cats.md">Custom Cats</a> • <a href="../Player_Progression_and_Cats/Injuries.md">Injuries</a> • <a href="../Player_Progression_and_Cats/Progression_Unlocks.md">Progression Unlocks</a> • <a href="../Player_Progression_and_Cats/Combat_Rewards.md">Combat Rewards</a></td>
  </tr>
  <tr>
    <td><strong>World, Maps & Events</strong></td>
    <td><a href="../World_Maps_and_Events/Events_and_Encounters.md">Events & Encounters</a> • <a href="../World_Maps_and_Events/House_and_Environment.md">House & Environment</a> • <a href="../World_Maps_and_Events/Map_Generation_and_Routing.md">Map Gen & Routing</a> • <a href="../World_Maps_and_Events/Furniture_and_Metaprogression.md">Furniture & Meta</a> • <a href="../World_Maps_and_Events/Shops.md">Shops</a> • <a href="../World_Maps_and_Events/Spawns_and_Enemy_Pools.md">Spawns & Enemy Pools</a> • <a href="../World_Maps_and_Events/Boss_Cutscene_Info.md">Boss Cutscenes</a> • <a href="../World_Maps_and_Events/NPC_Scripts.md">NPC Scripts</a></td>
  </tr>
  <tr>
    <td><strong>Assets & Localization</strong></td>
    <td><a href="../Assets_and_Localization/Audio_SFX_Dictionary.md">Audio SFX</a> • <a href="../Assets_and_Localization/Particles_and_VFX_Dictionary.md">Particles & VFX</a> • <a href="../Assets_and_Localization/Damage_Text_Styles.md">Damage Text</a> • <a href="../Assets_and_Localization/Localization_Guide.md">Localization Guide</a> • <a href="../Assets_and_Localization/Text_Formatting_and_Effects.md">Text Formatting</a> • <a href="../Assets_and_Localization/Strings.md">Strings</a></td>
  </tr>
  <tr>
    <td><strong>Reference & Meta</strong></td>
    <td><a href="../Reference_and_Meta/Enums.md">Enums</a> • <a href="../Reference_and_Meta/Arrays.md">Arrays</a> • <a href="../Reference_and_Meta/Item_Pools.md">Item Pools</a> • <a href="../Reference_and_Meta/Difficulties.md">Difficulties</a> • <a href="../Reference_and_Meta/Engine_Hidden_Passives_and_Statuses.md">Hidden Passives</a> • <a href="../Reference_and_Meta/Passive_Identifiers_Audit.md">Passive Audit</a> • <a href="../Reference_and_Meta/Engine_Uncategorized_Resources.md">Uncategorized Keys</a> • <a href="../Reference_and_Meta/Miscellaneous.md">Miscellaneous</a></td>
  </tr>
</table>

</details>

## Overview
> [!NOTE]
> This schema manages the meta-progression flags. It tracks what the player has accomplished to unlock new items, cats, and house upgrades.

## Usage Example
Here is a real example of this object being defined in the game's data:
```gon
class_unlock_medic {
	complete_chapter alley
	trigger_npc_sequence class_unlock_medic
}
```

## Associated Directory Files
To see extracted instances of this schema in the base game, refer to:
- [`Progression_Unlocks.md`](../../Directory/System_and_Engine/Progression_Unlocks.md)

---



This document is an exhaustive, auto-generated dictionary of `.gon` properties relevant to this subsystem. While the overview above provides high-level context, you may still need to infer exact engine execution rules through testing or context clues.

## Progression Unlocks

> **Associated Files:** `data/adventure_progression_unlocks.gon, data/npc_favor_unlocks.gon`


### Object: `ROOT`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 266

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`popup`](./Progression_Unlocks.md#object-popup) | Object | An object defining a popup notification with prompt and optional unlock. | 266 | `{ . . . }` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 206 | `common`<br>`rare`<br>`cha` |
| [`complete_chapter_with_class`](../Reference_and_Meta/Arrays.md#array-complete_chapter_with_class) | Array | An array specifying [chapter, class] that must be completed to unlock this reward. | 129 | `[boneyard Butcher]`<br>`[boneyard Colorless]`<br>`[boneyard Druid]` |
| [`unlock_item_immediate`](../Reference_and_Meta/Enums.md#enum-unlock_item_immediate) | Enum | Specifies which item is unlocked immediately when this unlock condition is met. | 127 | `AnointingOil`<br>`BagOfBags`<br>`BagOfSeeds` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 70 | `{ . . . }` |
| [`trigger_npc_sequence`](../Reference_and_Meta/Enums.md#enum-trigger_npc_sequence) | Enum | The name of an NPC dialogue sequence to trigger. | 55 | `beanies_begin_accepting_cats`<br>`beanies_bombquest_2`<br>`beanies_bombquest_3` |
| [`beat_house_boss`](../Reference_and_Meta/Enums.md#enum-beat_house_boss) | Enum | Specifies which house boss (or 'any') must be defeated to fulfill this unlock condition. | 48 | `any`<br>`guillotina_1`<br>`guillotina_2` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 38 | Default<br>FormChange<br>Druid |
| [`complete_chapter`](../Reference_and_Meta/Enums.md#enum-complete_chapter) | Enum | Specifies which chapter to mark as completed when this event triggers. | 36 | `alley`<br>`boneyard`<br>`bunker` |
| `required_difficulty` | Integer | The minimum difficulty level required to access this content (0 = easy, 1 = normal, etc.). | 36 | `0`<br>`1`<br>`2` |
| `repeat` | Integer | Determines how many times an event, song, or unlock can be triggered. Accepts a positive integer or the string "infinite". | 32 | `1`<br>`2`<br>`20` |
| [`beat_chapter_boss`](../Reference_and_Meta/Enums.md#enum-beat_chapter_boss) | Enum | Specifies the chapter boss that must be defeated to trigger the unlock. | 31 | `alley`<br>`boneyard`<br>`bunker` |
| [`unlock_ability`](../Reference_and_Meta/Enums.md#enum-unlock_ability) | Enum | Specifies the ability that is unlocked. | 31 | `BallOfSpiders`<br>`Bump`<br>`Ethereal` |
| [`unlock_song`](../Reference_and_Meta/Enums.md#enum-unlock_song) | Enum | Specifies the song that is unlocked. | 29 | `alone_in_the_dark`<br>`angel_wings`<br>`bolt_of_lightning` |
| [`unlock_passive`](../Reference_and_Meta/Enums.md#enum-unlock_passive) | Enum | Specifies the passive ability that is unlocked. | 29 | `AlphaStrike`<br>`ArmorSpecialist`<br>`Bouncer` |
| [`set_mapgen_flag`](../Reference_and_Meta/Enums.md#enum-set_mapgen_flag) | Enum | The name of a map generation flag to set when this event triggers. | 23 | `BoneyardUnlocked`<br>`BothObelisksUnlocked`<br>`BunkerUnlocked` |
| [`complete_checklist_with_class`](../Reference_and_Meta/Enums.md#enum-complete_checklist_with_class) | Enum | Specifies the class required to complete the checklist for this unlock. | 14 | `Butcher`<br>`Colorless`<br>`Druid` |
| [`unlock_quest_item`](../Reference_and_Meta/Enums.md#enum-unlock_quest_item) | Enum | Specifies the quest item that is unlocked. | 13 | `BlackShard`<br>`CryogenicTimeChamber_Empty`<br>`GuillotinasHead` |
| `repeatable` | Boolean | If true, this unlock or event can be triggered multiple times. | 10 | `true` |
| [`trigger_house_boss`](../Reference_and_Meta/Enums.md#enum-trigger_house_boss) | Enum | Specifies the house boss encounter that is triggered. | 10 | `guillotina_1`<br>`guillotina_2`<br>`guillotina_3` |
| [`complete_act_difficulty`](../Reference_and_Meta/Arrays.md#array-complete_act_difficulty) | Array | An array containing the act number and difficulty level that must be completed. | 9 | `[1 0]`<br>`[1 1]`<br>`[1 2]` |
| [`unlock_act_difficulty`](../Reference_and_Meta/Arrays.md#array-unlock_act_difficulty) | Array | An array containing the act number and difficulty level to unlock. | 9 | `[1 1]`<br>`[1 2]`<br>`[1 3]` |
| [`queue_cutscene_immediate`](../Reference_and_Meta/Enums.md#enum-queue_cutscene_immediate) | Enum | Determines which cutscene to play immediately upon queueing. | 8 | `caves_intro`<br>`core_intro`<br>`desert_intro` |
| [`reset_npc_sequence`](../Reference_and_Meta/Enums.md#enum-reset_npc_sequence) | Enum | Specifies the NPC sequence to reset for re-triggering. | 8 | `beanies_bombquest_2`<br>`beanies_bombquest_3`<br>`beanies_bombquest_begin` |
| `set_savefile_flag` | String | Determines which save file flag to set. | 6 | `AlienInvasionUnlocked`<br>`HauntedNightUnlocked`<br>`PlotFlag_Beanies_Homeless` |
| [`unlock_boss`](../Reference_and_Meta/Enums.md#enum-unlock_boss) | Enum | Determines which boss encounter to unlock. | 6 | `bumblefoot`<br>`gambit`<br>`infestedduo` |
| [`preempt_npc_sequence`](../Reference_and_Meta/Enums.md#enum-preempt_npc_sequence) | Enum | Specifies the NPC sequence to run before the current one. | 6 | `beanies_bombquest_2`<br>`beanies_bombquest_3`<br>`beanies_bombquest_amnesia` |
| [`fail_item_quest`](../Reference_and_Meta/Enums.md#enum-fail_item_quest) | Enum | Determines which item quest is marked as failed. | 4 | `JarOfChaos`<br>`JarOfRadiatedBlood`<br>`JarOfRadiation` |
| `fully_complete_difficulty` | Integer | The difficulty level required to be fully completed. | 4 | `0`<br>`1`<br>`2` |
| [`post_combat_cutscene`](../Reference_and_Meta/Enums.md#enum-post_combat_cutscene) | Enum | Determines which cutscene to play after a combat encounter. | 4 | `obelisk1_core`<br>`obelisk1_moon`<br>`obelisk2_core` |
| [`unlock_npc_tomorrow`](../Reference_and_Meta/Enums.md#enum-unlock_npc_tomorrow) | Enum | Specifies the NPC that will become available to interact with the next in-game day. | 4 | `beanies`<br>`jack`<br>`organgrinder` |
| [`visit_chapter`](../Reference_and_Meta/Enums.md#enum-visit_chapter) | Enum | Specifies the chapter area that the player must visit to trigger an event. | 4 | `dimensionx`<br>`future`<br>`iceage` |
| [`trigger_npc_sequence_tomorrow`](../Reference_and_Meta/Enums.md#enum-trigger_npc_sequence_tomorrow) | Enum | Determines which NPC sequence to schedule for the next day. | 4 | `butch_boneyard_intro`<br>`frank_caves_intro`<br>`jack_desert_intro` |
| `requires_monoclass_run` | Boolean | If true, this unlock requires the player to have completed a monoclass run. | 3 | `true` |
| [`requires_unlocked_npc`](../Reference_and_Meta/Enums.md#enum-requires_unlocked_npc) | Enum | Specifies the NPC that must be unlocked before this event or unlock can occur. | 3 | `frank`<br>`jack`<br>`tracy` |
| [`complete_chapters`](../Reference_and_Meta/Arrays.md#array-complete_chapters) | Array | An array of chapter names that must be completed to unlock this entity. | 3 | `[caves boneyard]`<br>`[core moon]` |
| [`complete_adventure`](../Reference_and_Meta/Enums.md#enum-complete_adventure) | Enum | Specifies the location requirement (e.g., 'anywhere') for completing an adventure. | 2 | `anywhere` |
| [`require_beat_house_boss`](../Reference_and_Meta/Enums.md#enum-require_beat_house_boss) | Enum | Specifies the name of the house boss that must be defeated to unlock this content. | 2 | `pyrophina`<br>`zaratana` |
| [`require_mapgen_flag`](../Reference_and_Meta/Enums.md#enum-require_mapgen_flag) | Enum | Specifies the map generation flag that must be present to unlock this content. | 2 | `CoreObeliskUnlocked`<br>`MoonObeliskUnlocked` |
| [`surviving_kaiju`](../Reference_and_Meta/Enums.md#enum-surviving_kaiju) | Enum | Specifies which kaiju entity survives a given quest event. | 2 | `pyrophina`<br>`zaratana` |
| [`unlock_levelgroup`](../Reference_and_Meta/Enums.md#enum-unlock_levelgroup) | Enum | Specifies the level group to unlock when a given condition is met. | 2 | `bigsharklevels` |
| [`intro`](../Reference_and_Meta/Arrays.md#array-intro) | Array | An object defining the introductory cutscene for the event, including title, cat selection, and visuals. | 1 | `[PersuasionDevice]` |
| [`beanies_quests_intro`](./Progression_Unlocks.md#object-beanies_quests_intro) | Object | Defines the initial dialog or quest-generation sequence for Dr. Beanies' quests. | 1 | `{ . . . }` |
| [`beanies_quests_repeat`](./Progression_Unlocks.md#object-beanies_quests_repeat) | Object | Defines the repeatable quest dialog or generator for Dr. Beanies. | 1 | `{ . . . }` |
| [`frank_max_intro`](./Progression_Unlocks.md#object-frank_max_intro) | Object | Defines the dialog sequence and rewards for reaching max favor with Frank. | 1 | `{ . . . }` |
| [`frank_max_repeating`](./Progression_Unlocks.md#object-frank_max_repeating) | Object | Defines the repeatable dialog sequence and rewards for Frank at max favor. | 1 | `{ . . . }` |
| [`house_upgrade_4throom`](./Progression_Unlocks.md#object-house_upgrade_4throom) | Object | Defines the dialog and house upgrade for unlocking the 4th room. | 1 | `{ . . . }` |
| [`house_upgrade_attic`](./Progression_Unlocks.md#object-house_upgrade_attic) | Object | Defines the dialog and house upgrade for the attic. | 1 | `{ . . . }` |
| [`house_upgrade_largehouse`](./Progression_Unlocks.md#object-house_upgrade_largehouse) | Object | Defines the dialog and house upgrade for the large house. | 1 | `{ . . . }` |
| [`house_upgrade_mediumhouse`](./Progression_Unlocks.md#object-house_upgrade_mediumhouse) | Object | Defines the dialog and house upgrade for the medium house. | 1 | `{ . . . }` |
| [`jack_max_intro`](./Progression_Unlocks.md#object-jack_max_intro) | Object | Defines the dialog sequence and rewards for reaching max favor with Jack. | 1 | `{ . . . }` |
| [`jack_max_repeating`](./Progression_Unlocks.md#object-jack_max_repeating) | Object | Defines the repeatable dialog sequence and rewards for Jack at max favor. | 1 | `{ . . . }` |
| [`jack_shopupgrade1`](./Progression_Unlocks.md#object-jack_shopupgrade1) | Object | Defines the dialog and shop level up for Jack's first shop upgrade. | 1 | `{ . . . }` |
| [`jack_shopupgrade2`](./Progression_Unlocks.md#object-jack_shopupgrade2) | Object | Defines the dialog and shop level up for Jack's second shop upgrade. | 1 | `{ . . . }` |
| [`jack_shopupgrade3`](./Progression_Unlocks.md#object-jack_shopupgrade3) | Object | Defines the dialog and shop level up for Jack's third shop upgrade. | 1 | `{ . . . }` |
| [`jack_shopupgrade4`](./Progression_Unlocks.md#object-jack_shopupgrade4) | Object | Defines the dialog and shop level up for Jack's fourth shop upgrade. | 1 | `{ . . . }` |
| [`organ_max_intro`](./Progression_Unlocks.md#object-organ_max_intro) | Object | Defines the dialog sequence and rewards for reaching max favor with Organ Grinder. | 1 | `{ . . . }` |
| [`organ_max_repeating`](./Progression_Unlocks.md#object-organ_max_repeating) | Object | Defines the repeatable dialog sequence and rewards for Organ Grinder at max favor. | 1 | `{ . . . }` |
| [`organ_unlock`](./Progression_Unlocks.md#object-organ_unlock) | Object | Defines the dialog and shop level up for unlocking Organ Grinder. | 1 | `{ . . . }` |
| [`organ_upgrade1`](./Progression_Unlocks.md#object-organ_upgrade1) | Object | Defines the dialog and shop level up for Organ Grinder's first upgrade. | 1 | `{ . . . }` |
| [`organ_upgrade2`](./Progression_Unlocks.md#object-organ_upgrade2) | Object | Defines the dialog and shop level up for Organ Grinder's second upgrade. | 1 | `{ . . . }` |
| [`organ_upgrade3`](./Progression_Unlocks.md#object-organ_upgrade3) | Object | Defines the dialog and shop level up for Organ Grinder's third upgrade. | 1 | `{ . . . }` |
| [`organ_upgrade4`](./Progression_Unlocks.md#object-organ_upgrade4) | Object | Defines the dialog and shop level up for Organ Grinder's fourth upgrade. | 1 | `{ . . . }` |
| [`organ_upgrade5`](./Progression_Unlocks.md#object-organ_upgrade5) | Object | Defines the dialog and shop level up for Organ Grinder's fifth upgrade. | 1 | `{ . . . }` |
| [`organ_upgrade6`](./Progression_Unlocks.md#object-organ_upgrade6) | Object | Defines the dialog and shop level up for Organ Grinder's sixth upgrade. | 1 | `{ . . . }` |
| [`steven_milliontrashed`](./Progression_Unlocks.md#object-steven_milliontrashed) | Object | A dialogue sequence or favor reward configuration for the NPC Steven, triggered when the player has accumulated 1,000,000 favor. | 1 | `{ . . . }` |
| [`tink_aggression`](./Progression_Unlocks.md#object-tink_aggression) | Object | A dialogue sequence or favor reward that unlocks the cat info panel for viewing a cat's aggression stat. | 1 | `{ . . . }` |
| [`tink_basestats`](./Progression_Unlocks.md#object-tink_basestats) | Object | A dialogue sequence or favor reward that unlocks the cat info panel for viewing a cat's base stats and stat modifications. | 1 | `{ . . . }` |
| [`tink_inbreeding`](./Progression_Unlocks.md#object-tink_inbreeding) | Object | A dialogue sequence or favor reward that unlocks the cat info panel for viewing a cat's inbreeding level and family tree. | 1 | `{ . . . }` |
| [`tink_max_intro`](./Progression_Unlocks.md#object-tink_max_intro) | Object | The first dialogue sequence and favor reward that plays when Tink reaches maximum favor. | 1 | `{ . . . }` |
| [`tink_max_repeating`](./Progression_Unlocks.md#object-tink_max_repeating) | Object | A repeating dialogue sequence and favor reward that plays when Tink is at maximum favor, cycling through random sub-sequences. | 1 | `{ . . . }` |
| [`tink_prettybow`](./Progression_Unlocks.md#object-tink_prettybow) | Object | A dialogue sequence and favor reward that grants the gift item TinksBow. | 1 | `{ . . . }` |
| [`tink_relationships`](./Progression_Unlocks.md#object-tink_relationships) | Object | A dialogue sequence or favor reward that unlocks the cat info panel for viewing a cat's relationships (loves and hates). | 1 | `{ . . . }` |
| [`tink_sexuality`](./Progression_Unlocks.md#object-tink_sexuality) | Object | A dialogue sequence or favor reward that unlocks the cat info panel for viewing a cat's libido and sexual orientation flags. | 1 | `{ . . . }` |
| [`tink_tags`](./Progression_Unlocks.md#object-tink_tags) | Object | A dialogue sequence or favor reward that unlocks the ability to manually add symbols to a cat's name. | 1 | `{ . . . }` |
| [`tracy_blankcollar1`](./Progression_Unlocks.md#object-tracy_blankcollar1) | Object | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 1 | `{ . . . }` |
| [`tracy_blankcollar2`](./Progression_Unlocks.md#object-tracy_blankcollar2) | Object | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 1 | `{ . . . }` |
| [`tracy_blankcollar3`](./Progression_Unlocks.md#object-tracy_blankcollar3) | Object | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 1 | `{ . . . }` |
| [`tracy_foodstorage1`](./Progression_Unlocks.md#object-tracy_foodstorage1) | Object | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 1 | `{ . . . }` |
| [`tracy_foodstorage10`](./Progression_Unlocks.md#object-tracy_foodstorage10) | Object | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 1 | `{ . . . }` |
| [`tracy_foodstorage2`](./Progression_Unlocks.md#object-tracy_foodstorage2) | Object | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 1 | `{ . . . }` |
| [`tracy_foodstorage3`](./Progression_Unlocks.md#object-tracy_foodstorage3) | Object | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 1 | `{ . . . }` |
| [`tracy_foodstorage4`](./Progression_Unlocks.md#object-tracy_foodstorage4) | Object | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 1 | `{ . . . }` |
| [`tracy_foodstorage5`](./Progression_Unlocks.md#object-tracy_foodstorage5) | Object | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 1 | `{ . . . }` |
| [`tracy_foodstorage6`](./Progression_Unlocks.md#object-tracy_foodstorage6) | Object | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 1 | `{ . . . }` |
| [`tracy_foodstorage7`](./Progression_Unlocks.md#object-tracy_foodstorage7) | Object | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 1 | `{ . . . }` |
| [`tracy_foodstorage8`](./Progression_Unlocks.md#object-tracy_foodstorage8) | Object | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 1 | `{ . . . }` |
| [`tracy_foodstorage9`](./Progression_Unlocks.md#object-tracy_foodstorage9) | Object | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 1 | `{ . . . }` |
| [`tracy_idol1`](./Progression_Unlocks.md#object-tracy_idol1) | Object | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 1 | `{ . . . }` |
| [`tracy_idol2`](./Progression_Unlocks.md#object-tracy_idol2) | Object | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 1 | `{ . . . }` |
| [`tracy_idol3`](./Progression_Unlocks.md#object-tracy_idol3) | Object | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 1 | `{ . . . }` |
| [`tracy_idol4`](./Progression_Unlocks.md#object-tracy_idol4) | Object | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 1 | `{ . . . }` |
| [`tracy_idol5`](./Progression_Unlocks.md#object-tracy_idol5) | Object | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 1 | `{ . . . }` |
| [`tracy_idol6`](./Progression_Unlocks.md#object-tracy_idol6) | Object | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 1 | `{ . . . }` |
| [`tracy_idol7`](./Progression_Unlocks.md#object-tracy_idol7) | Object | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 1 | `{ . . . }` |
| [`tracy_max_intro`](./Progression_Unlocks.md#object-tracy_max_intro) | Object | The first dialogue sequence and bonus rare item reward that plays when Tracy reaches maximum favor. | 1 | `{ . . . }` |
| [`tracy_max_repeating`](./Progression_Unlocks.md#object-tracy_max_repeating) | Object | A repeating dialogue sequence and favor reward that plays when Tracy is at maximum favor, cycling through random sub-sequences. | 1 | `{ . . . }` |
| [`upgrade_storage_1`](./Progression_Unlocks.md#object-upgrade_storage_1) | Object | A dialogue sequence and storage expansion reward for Butch, requiring act 0 and chapter 0. | 1 | `{ . . . }` |
| [`upgrade_storage_2`](./Progression_Unlocks.md#object-upgrade_storage_2) | Object | A dialogue sequence and storage expansion reward for Butch, requiring act 1 and chapter 2. | 1 | `{ . . . }` |
| [`upgrade_storage_3`](./Progression_Unlocks.md#object-upgrade_storage_3) | Object | A dialogue sequence and storage expansion reward for Butch, requiring act 1 and chapter 3. | 1 | `{ . . . }` |
| [`upgrade_storage_4`](./Progression_Unlocks.md#object-upgrade_storage_4) | Object | A dialogue sequence and storage expansion reward for Butch, requiring act 2 and chapter 2. | 1 | `{ . . . }` |
| [`upgrade_storage_5`](./Progression_Unlocks.md#object-upgrade_storage_5) | Object | A dialogue sequence and storage expansion reward for Butch, requiring act 2 and chapter 3. | 1 | `{ . . . }` |
| [`upgrade_storage_6`](./Progression_Unlocks.md#object-upgrade_storage_6) | Object | A dialogue sequence and storage expansion reward for Butch, requiring act 3 and chapter 2. | 1 | `{ . . . }` |
| [`upgrade_storage_7`](./Progression_Unlocks.md#object-upgrade_storage_7) | Object | A dialogue sequence and storage expansion reward for Butch, requiring act 3 and chapter 3. | 1 | `{ . . . }` |
| [`upgrade_storage_repeating_crazy`](./Progression_Unlocks.md#object-upgrade_storage_repeating_crazy) | Object | A repeating dialogue sequence for Butch's storage upgrade at crazy difficulty, granting one storage expansion. | 1 | `{ . . . }` |
| [`upgrade_storage_repeating_hard`](./Progression_Unlocks.md#object-upgrade_storage_repeating_hard) | Object | A repeating dialogue sequence for Butch's storage upgrade at hard difficulty, granting one storage expansion. | 1 | `{ . . . }` |
| [`upgrade_storage_repeating_impossible`](./Progression_Unlocks.md#object-upgrade_storage_repeating_impossible) | Object | A repeating dialogue sequence for Butch's storage upgrade at impossible difficulty, granting one storage expansion. | 1 | `{ . . . }` |
| [`upgrade_storage_repeating_intro`](./Progression_Unlocks.md#object-upgrade_storage_repeating_intro) | Object | The introductory dialogue sequence and reward when Butch maxes out storage capacity. | 1 | `{ . . . }` |
| [`upgrade_storage_repeating_normal`](./Progression_Unlocks.md#object-upgrade_storage_repeating_normal) | Object | A repeating dialogue sequence for Butch's storage upgrade at normal difficulty, granting one storage expansion. | 1 | `{ . . . }` |
| [`main_pool`](../Reference_and_Meta/Arrays.md#array-main_pool) | Array | A list of quest IDs or objects that form the primary quest pool for a beanies quest node. | 1 | `[` |
| [`destinations`](./Progression_Unlocks.md#object-destinations) | Object | Specifies the list of areas and their associated coin rewards for Beanie's quest destinations. | 1 | `{ . . . }` |
| [`fail_adventure`](../Reference_and_Meta/Enums.md#enum-fail_adventure) | Enum | Specifies a trigger that causes the current adventure to fail, with a location parameter (e.g., 'anywhere'). | 1 | `anywhere` |
| [`finish_quest`](../Reference_and_Meta/Enums.md#enum-finish_quest) | Enum | Specifies the name of the quest to mark as finished. | 1 | `JarOfChaos` |
| `increment_savefile_counter` | String | Specifies the GameStat counter to increment when this sequence completes. | 1 | `GameStat_CountNukeQuestCompletions` |
| [`prereqs`](./Progression_Unlocks.md#object-prereqs) | Object | Object mapping quest or unlock names to their prerequisite mapflags or conditions. | 1 | `{ . . . }` |
| `requires_hard_path` | Boolean | If true, this unlock requires the player to be on the hard path. | 1 | `true` |
| [`reset_unlock`](../Reference_and_Meta/Enums.md#enum-reset_unlock) | Enum | Specifies the unlock key to reset upon completing this unlock chain. | 1 | `nuke_quest_begin` |
| [`unlock_item`](../Reference_and_Meta/Enums.md#enum-unlock_item) | Enum | The name of the item unlocked by this event. | 1 | `MomsKnife` |

</details>


---


### Object: `popup`


**Definition:** An object defining a popup notification with prompt and optional unlock.  
**Total Count:** 266

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

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

> **Referenced by:** [`tracy_blankcollar1`](./Progression_Unlocks.md#object-tracy_blankcollar1), [`tracy_blankcollar2`](./Progression_Unlocks.md#object-tracy_blankcollar2), [`tracy_blankcollar3`](./Progression_Unlocks.md#object-tracy_blankcollar3), [`tracy_foodstorage1`](./Progression_Unlocks.md#object-tracy_foodstorage1), [`tracy_foodstorage10`](./Progression_Unlocks.md#object-tracy_foodstorage10), [`tracy_foodstorage2`](./Progression_Unlocks.md#object-tracy_foodstorage2), [`tracy_foodstorage3`](./Progression_Unlocks.md#object-tracy_foodstorage3), [`tracy_foodstorage4`](./Progression_Unlocks.md#object-tracy_foodstorage4), [`tracy_foodstorage5`](./Progression_Unlocks.md#object-tracy_foodstorage5), [`tracy_foodstorage6`](./Progression_Unlocks.md#object-tracy_foodstorage6), [`tracy_foodstorage7`](./Progression_Unlocks.md#object-tracy_foodstorage7), [`tracy_foodstorage8`](./Progression_Unlocks.md#object-tracy_foodstorage8), [`tracy_foodstorage9`](./Progression_Unlocks.md#object-tracy_foodstorage9), [`tracy_idol1`](./Progression_Unlocks.md#object-tracy_idol1), [`tracy_idol2`](./Progression_Unlocks.md#object-tracy_idol2), [`tracy_idol3`](./Progression_Unlocks.md#object-tracy_idol3), [`tracy_idol4`](./Progression_Unlocks.md#object-tracy_idol4), [`tracy_idol5`](./Progression_Unlocks.md#object-tracy_idol5), [`tracy_idol6`](./Progression_Unlocks.md#object-tracy_idol6), [`tracy_idol7`](./Progression_Unlocks.md#object-tracy_idol7), [`tracy_max_intro`](./Progression_Unlocks.md#object-tracy_max_intro), [`tracy_max_repeating`](./Progression_Unlocks.md#object-tracy_max_repeating)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 22 | `{ . . . }` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 22 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `upgrade_storage_repeating_normal`


**Definition:** A repeating dialogue sequence for Butch's storage upgrade at normal difficulty, granting one storage expansion.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `repeat` | Integer | Determines how many times an event, song, or unlock can be triggered. Accepts a positive integer or the string "infinite". | 1 | `1`<br>`2`<br>`20` |
| `required_difficulty` | Integer | The minimum difficulty level required to access this content (0 = easy, 1 = normal, etc.). | 1 | `0`<br>`1`<br>`2` |
| [`level_display`](../Reference_and_Meta/Enums.md#enum-level_display) | Enum | Specifies how to display the current level of a repeating upgrade (e.g., 'max'). | 1 | `max` |
| `required_act` | Integer | The act number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`1`<br>`2` |
| `required_chapter` | Integer | The chapter number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`2`<br>`3` |
| `rep_reward_count` | Integer | The number of reputation rewards granted. | 1 | `1` |

</details>


---


### Object: `upgrade_storage_repeating_intro`


**Definition:** The introductory dialogue sequence and reward when Butch maxes out storage capacity.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `required_difficulty` | Integer | The minimum difficulty level required to access this content (0 = easy, 1 = normal, etc.). | 1 | `0`<br>`1`<br>`2` |
| [`level_display`](../Reference_and_Meta/Enums.md#enum-level_display) | Enum | Specifies how to display the current level of a repeating upgrade (e.g., 'max'). | 1 | `max` |
| `required_act` | Integer | The act number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`1`<br>`2` |
| `required_chapter` | Integer | The chapter number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`2`<br>`3` |
| `rep_reward_count` | Integer | The number of reputation rewards granted. | 1 | `1` |

</details>


---


### Object: `upgrade_storage_repeating_impossible`


**Definition:** A repeating dialogue sequence for Butch's storage upgrade at impossible difficulty, granting one storage expansion.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| [`repeat`](../Reference_and_Meta/Enums.md#enum-repeat) | Enum | Determines how many times an event, song, or unlock can be triggered. Accepts a positive integer or the string "infinite". | 1 | `1`<br>`2`<br>`20` |
| `required_difficulty` | Integer | The minimum difficulty level required to access this content (0 = easy, 1 = normal, etc.). | 1 | `0`<br>`1`<br>`2` |
| [`level_display`](../Reference_and_Meta/Enums.md#enum-level_display) | Enum | Specifies how to display the current level of a repeating upgrade (e.g., 'max'). | 1 | `max` |
| `required_act` | Integer | The act number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`1`<br>`2` |
| `required_chapter` | Integer | The chapter number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`2`<br>`3` |
| `rep_reward_count` | Integer | The number of reputation rewards granted. | 1 | `1` |

</details>


---


### Object: `upgrade_storage_repeating_hard`


**Definition:** A repeating dialogue sequence for Butch's storage upgrade at hard difficulty, granting one storage expansion.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `repeat` | Integer | Determines how many times an event, song, or unlock can be triggered. Accepts a positive integer or the string "infinite". | 1 | `1`<br>`2`<br>`20` |
| `required_difficulty` | Integer | The minimum difficulty level required to access this content (0 = easy, 1 = normal, etc.). | 1 | `0`<br>`1`<br>`2` |
| [`level_display`](../Reference_and_Meta/Enums.md#enum-level_display) | Enum | Specifies how to display the current level of a repeating upgrade (e.g., 'max'). | 1 | `max` |
| `required_act` | Integer | The act number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`1`<br>`2` |
| `required_chapter` | Integer | The chapter number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`2`<br>`3` |
| `rep_reward_count` | Integer | The number of reputation rewards granted. | 1 | `1` |

</details>


---


### Object: `upgrade_storage_repeating_crazy`


**Definition:** A repeating dialogue sequence for Butch's storage upgrade at crazy difficulty, granting one storage expansion.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `repeat` | Integer | Determines how many times an event, song, or unlock can be triggered. Accepts a positive integer or the string "infinite". | 1 | `1`<br>`2`<br>`20` |
| `required_difficulty` | Integer | The minimum difficulty level required to access this content (0 = easy, 1 = normal, etc.). | 1 | `0`<br>`1`<br>`2` |
| [`level_display`](../Reference_and_Meta/Enums.md#enum-level_display) | Enum | Specifies how to display the current level of a repeating upgrade (e.g., 'max'). | 1 | `max` |
| `required_act` | Integer | The act number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`1`<br>`2` |
| `required_chapter` | Integer | The chapter number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`2`<br>`3` |
| `rep_reward_count` | Integer | The number of reputation rewards granted. | 1 | `1` |

</details>


---


### Object: `upgrade_storage_7`


**Definition:** A dialogue sequence and storage expansion reward for Butch, requiring act 3 and chapter 3.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `required_act` | Integer | The act number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`1`<br>`2` |
| `required_chapter` | Integer | The chapter number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`2`<br>`3` |
| `storage_expansion` | Integer | The number of additional storage slots granted by this upgrade. | 1 | `1` |

</details>


---


### Object: `upgrade_storage_6`


**Definition:** A dialogue sequence and storage expansion reward for Butch, requiring act 3 and chapter 2.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `required_act` | Integer | The act number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`1`<br>`2` |
| `required_chapter` | Integer | The chapter number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`2`<br>`3` |
| `storage_expansion` | Integer | The number of additional storage slots granted by this upgrade. | 1 | `1` |

</details>


---


### Object: `upgrade_storage_5`


**Definition:** A dialogue sequence and storage expansion reward for Butch, requiring act 2 and chapter 3.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `required_act` | Integer | The act number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`1`<br>`2` |
| `required_chapter` | Integer | The chapter number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`2`<br>`3` |
| `storage_expansion` | Integer | The number of additional storage slots granted by this upgrade. | 1 | `1` |

</details>


---


### Object: `upgrade_storage_4`


**Definition:** A dialogue sequence and storage expansion reward for Butch, requiring act 2 and chapter 2.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `required_act` | Integer | The act number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`1`<br>`2` |
| `required_chapter` | Integer | The chapter number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`2`<br>`3` |
| `storage_expansion` | Integer | The number of additional storage slots granted by this upgrade. | 1 | `1` |

</details>


---


### Object: `upgrade_storage_3`


**Definition:** A dialogue sequence and storage expansion reward for Butch, requiring act 1 and chapter 3.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `required_act` | Integer | The act number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`1`<br>`2` |
| `required_chapter` | Integer | The chapter number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`2`<br>`3` |
| `storage_expansion` | Integer | The number of additional storage slots granted by this upgrade. | 1 | `1` |

</details>


---


### Object: `upgrade_storage_2`


**Definition:** A dialogue sequence and storage expansion reward for Butch, requiring act 1 and chapter 2.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `required_act` | Integer | The act number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`1`<br>`2` |
| `required_chapter` | Integer | The chapter number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`2`<br>`3` |
| `storage_expansion` | Integer | The number of additional storage slots granted by this upgrade. | 1 | `1` |

</details>


---


### Object: `upgrade_storage_1`


**Definition:** A dialogue sequence and storage expansion reward for Butch, requiring act 0 and chapter 0.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `required_act` | Integer | The act number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`1`<br>`2` |
| `required_chapter` | Integer | The chapter number that must be reached before this upgrade or interaction becomes available. | 1 | `0`<br>`2`<br>`3` |
| `storage_expansion` | Integer | The number of additional storage slots granted by this upgrade. | 1 | `1` |

</details>


---


### Object: `tracy_max_repeating`


**Definition:** A repeating dialogue sequence and favor reward that plays when Tracy is at maximum favor, cycling through random sub-sequences.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| [`repeat`](../Reference_and_Meta/Enums.md#enum-repeat) | Enum | Determines how many times an event, song, or unlock can be triggered. Accepts a positive integer or the string "infinite". | 1 | `1`<br>`2`<br>`20` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |
| [`level_display`](../Reference_and_Meta/Enums.md#enum-level_display) | Enum | Specifies how to display the current level of a repeating upgrade (e.g., 'max'). | 1 | `max` |

</details>


---


### Object: `tracy_max_intro`


**Definition:** The first dialogue sequence and bonus rare item reward that plays when Tracy reaches maximum favor.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |
| [`level_display`](../Reference_and_Meta/Enums.md#enum-level_display) | Enum | Specifies how to display the current level of a repeating upgrade (e.g., 'max'). | 1 | `max` |

</details>


---


### Object: `tracy_idol7`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `tracy_idol6`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `tracy_idol5`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `tracy_idol4`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `tracy_idol3`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `tracy_idol2`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `tracy_idol1`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `tracy_foodstorage9`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `tracy_foodstorage8`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `tracy_foodstorage7`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `tracy_foodstorage6`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `tracy_foodstorage5`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `tracy_foodstorage4`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `tracy_foodstorage3`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `tracy_foodstorage2`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `tracy_foodstorage10`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `tracy_foodstorage1`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `tracy_blankcollar3`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `tracy_blankcollar2`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `tracy_blankcollar1`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |
| `required_age` | Integer | The minimum age the player character must be to access this interaction or upgrade. | 1 | `5` |
| [`tracy_special_item`](./Progression_Unlocks.md#object-tracy_special_item) | Object | An object defining a special item offered by Tracy, including its type, cost, and associated reward text. | 1 | `{ . . . }` |

</details>


---


### Object: `tink_tags`


**Definition:** A dialogue sequence or favor reward that unlocks the ability to manually add symbols to a cat's name.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

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

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `set_savefile_flag` | String | Determines which save file flag to set. | 1 | `AlienInvasionUnlocked`<br>`HauntedNightUnlocked`<br>`PlotFlag_Beanies_Homeless` |

</details>


---


### Object: `tink_relationships`


**Definition:** A dialogue sequence or favor reward that unlocks the cat info panel for viewing a cat's relationships (loves and hates).  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `set_savefile_flag` | String | Determines which save file flag to set. | 1 | `AlienInvasionUnlocked`<br>`HauntedNightUnlocked`<br>`PlotFlag_Beanies_Homeless` |

</details>


---


### Object: `tink_prettybow`


**Definition:** A dialogue sequence and favor reward that grants the gift item TinksBow.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| [`gift_item`](../Reference_and_Meta/Enums.md#enum-gift_item) | Enum | The identifier of the item to gift to the player. | 1 | `TinksBow`<br>`disorder_needle` |

</details>


---


### Object: `tink_max_repeating`


**Definition:** A repeating dialogue sequence and favor reward that plays when Tink is at maximum favor, cycling through random sub-sequences.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `coins` | Integer | The amount of coins required to use this ability or obtained from this source. | 1 | `1`<br>`2`<br>`25` |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| [`repeat`](../Reference_and_Meta/Enums.md#enum-repeat) | Enum | Determines how many times an event, song, or unlock can be triggered. Accepts a positive integer or the string "infinite". | 1 | `1`<br>`2`<br>`20` |
| [`level_display`](../Reference_and_Meta/Enums.md#enum-level_display) | Enum | Specifies how to display the current level of a repeating upgrade (e.g., 'max'). | 1 | `max` |

</details>


---


### Object: `tink_max_intro`


**Definition:** The first dialogue sequence and favor reward that plays when Tink reaches maximum favor.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `coins` | Integer | The amount of coins required to use this ability or obtained from this source. | 1 | `1`<br>`2`<br>`25` |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| [`level_display`](../Reference_and_Meta/Enums.md#enum-level_display) | Enum | Specifies how to display the current level of a repeating upgrade (e.g., 'max'). | 1 | `max` |

</details>


---


### Object: `tink_inbreeding`


**Definition:** A dialogue sequence or favor reward that unlocks the cat info panel for viewing a cat's inbreeding level and family tree.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

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

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `set_savefile_flag` | String | Determines which save file flag to set. | 1 | `AlienInvasionUnlocked`<br>`HauntedNightUnlocked`<br>`PlotFlag_Beanies_Homeless` |

</details>


---


### Object: `tink_aggression`


**Definition:** A dialogue sequence or favor reward that unlocks the cat info panel for viewing a cat's aggression stat.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `set_savefile_flag` | String | Determines which save file flag to set. | 1 | `AlienInvasionUnlocked`<br>`HauntedNightUnlocked`<br>`PlotFlag_Beanies_Homeless` |

</details>


---


### Object: `steven_milliontrashed`


**Definition:** A dialogue sequence or favor reward configuration for the NPC Steven, triggered when the player has accumulated 1,000,000 favor.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`repeat`](../Reference_and_Meta/Enums.md#enum-repeat) | Enum | Determines how many times an event, song, or unlock can be triggered. Accepts a positive integer or the string "infinite". | 1 | `1`<br>`2`<br>`20` |
| [`level_display`](../Reference_and_Meta/Enums.md#enum-level_display) | Enum | Specifies how to display the current level of a repeating upgrade (e.g., 'max'). | 1 | `max` |

</details>


---


### Object: `organ_upgrade6`


**Definition:** Defines the dialog and shop level up for Organ Grinder's sixth upgrade.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

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

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

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

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

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

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

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

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

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

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |

</details>


---


### Object: `organ_unlock`


**Definition:** Defines the dialog and shop level up for unlocking Organ Grinder.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |

</details>


---


### Object: `organ_max_repeating`


**Definition:** Defines the repeatable dialog sequence and rewards for Organ Grinder at max favor.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| [`repeat`](../Reference_and_Meta/Enums.md#enum-repeat) | Enum | Determines how many times an event, song, or unlock can be triggered. Accepts a positive integer or the string "infinite". | 1 | `1`<br>`2`<br>`20` |
| [`level_display`](../Reference_and_Meta/Enums.md#enum-level_display) | Enum | Specifies how to display the current level of a repeating upgrade (e.g., 'max'). | 1 | `max` |
| [`gift_item`](../Reference_and_Meta/Enums.md#enum-gift_item) | Enum | The identifier of the item to gift to the player. | 1 | `TinksBow`<br>`disorder_needle` |

</details>


---


### Object: `organ_max_intro`


**Definition:** Defines the dialog sequence and rewards for reaching max favor with Organ Grinder.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| [`level_display`](../Reference_and_Meta/Enums.md#enum-level_display) | Enum | Specifies how to display the current level of a repeating upgrade (e.g., 'max'). | 1 | `max` |
| [`gift_item`](../Reference_and_Meta/Enums.md#enum-gift_item) | Enum | The identifier of the item to gift to the player. | 1 | `TinksBow`<br>`disorder_needle` |

</details>


---


### Object: `jack_shopupgrade4`


**Definition:** Defines the dialog and shop level up for Jack's fourth shop upgrade.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

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

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

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

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |

</details>


---


### Object: `jack_shopupgrade1`


**Definition:** Defines the dialog and shop level up for Jack's first shop upgrade.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| `shop_level_up` | Integer | The level of the shop upgrade granted. | 1 | `1` |

</details>


---


### Object: `jack_max_repeating`


**Definition:** Defines the repeatable dialog sequence and rewards for Jack at max favor.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| [`repeat`](../Reference_and_Meta/Enums.md#enum-repeat) | Enum | Determines how many times an event, song, or unlock can be triggered. Accepts a positive integer or the string "infinite". | 1 | `1`<br>`2`<br>`20` |
| [`level_display`](../Reference_and_Meta/Enums.md#enum-level_display) | Enum | Specifies how to display the current level of a repeating upgrade (e.g., 'max'). | 1 | `max` |
| `rep_reward_count` | Integer | The number of reputation rewards granted. | 1 | `1` |

</details>


---


### Object: `jack_max_intro`


**Definition:** Defines the dialog sequence and rewards for reaching max favor with Jack.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| [`level_display`](../Reference_and_Meta/Enums.md#enum-level_display) | Enum | Specifies how to display the current level of a repeating upgrade (e.g., 'max'). | 1 | `max` |
| `rep_reward_count` | Integer | The number of reputation rewards granted. | 1 | `1` |

</details>


---


### Object: `house_upgrade_mediumhouse`


**Definition:** Defines the dialog and house upgrade for the medium house.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`house_upgrade`](../Reference_and_Meta/Enums.md#enum-house_upgrade) | Enum | Specifies the name of the house upgrade to apply. | 2 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `house_upgrade_largehouse`


**Definition:** Defines the dialog and house upgrade for the large house.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`house_upgrade`](../Reference_and_Meta/Enums.md#enum-house_upgrade) | Enum | Specifies the name of the house upgrade to apply. | 2 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |

</details>


---


### Object: `house_upgrade_attic`


**Definition:** Defines the dialog and house upgrade for the attic.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| [`house_upgrade`](../Reference_and_Meta/Enums.md#enum-house_upgrade) | Enum | Specifies the name of the house upgrade to apply. | 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |

</details>


---


### Object: `house_upgrade_4throom`


**Definition:** Defines the dialog and house upgrade for unlocking the 4th room.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| [`house_upgrade`](../Reference_and_Meta/Enums.md#enum-house_upgrade) | Enum | Specifies the name of the house upgrade to apply. | 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |

</details>


---


### Object: `frank_max_repeating`


**Definition:** Defines the repeatable dialog sequence and rewards for Frank at max favor.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| [`repeat`](../Reference_and_Meta/Enums.md#enum-repeat) | Enum | Determines how many times an event, song, or unlock can be triggered. Accepts a positive integer or the string "infinite". | 1 | `1`<br>`2`<br>`20` |
| [`level_display`](../Reference_and_Meta/Enums.md#enum-level_display) | Enum | Specifies how to display the current level of a repeating upgrade (e.g., 'max'). | 1 | `max` |
| [`gift_item_from_pool`](../Reference_and_Meta/Enums.md#enum-gift_item_from_pool) | Enum | Specifies the item pool from which to gift an item. | 1 | `parasites` |

</details>


---


### Object: `frank_max_intro`


**Definition:** Defines the dialog sequence and rewards for reaching max favor with Frank.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| [`level_display`](../Reference_and_Meta/Enums.md#enum-level_display) | Enum | Specifies how to display the current level of a repeating upgrade (e.g., 'max'). | 1 | `max` |
| [`gift_item_from_pool`](../Reference_and_Meta/Enums.md#enum-gift_item_from_pool) | Enum | Specifies the item pool from which to gift an item. | 1 | `parasites` |

</details>


---


### Object: `beanies_quests_repeat`


**Definition:** Defines the repeatable quest dialog or generator for Dr. Beanies.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| [`repeat`](../Reference_and_Meta/Enums.md#enum-repeat) | Enum | Determines how many times an event, song, or unlock can be triggered. Accepts a positive integer or the string "infinite". | 1 | `1`<br>`2`<br>`20` |
| [`level_display`](../Reference_and_Meta/Enums.md#enum-level_display) | Enum | Specifies how to display the current level of a repeating upgrade (e.g., 'max'). | 1 | `max` |
| [`generate_beanies_quest`](../Reference_and_Meta/Enums.md#enum-generate_beanies_quest) | Enum | Specifies which quest pool (e.g., 'main_pool', 'intro') to generate a quest from. | 1 | `intro`<br>`main_pool` |

</details>


---


### Object: `beanies_quests_intro`


**Definition:** Defines the initial dialog or quest-generation sequence for Dr. Beanies' quests.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer | The amount of favor points awarded or spent. | 1 | `1`<br>`10`<br>`100` |
| [`reward_text`](../Assets_and_Localization/Strings.md#string-reward_text) | String | A localization key for the text describing the reward. | 1 | `"FAVOR_BEANIES_INTRO"`<br>`"FAVOR_BEANIES_REPEAT"`<br>`"FAVOR_BUTCH_UPGRADE"` |
| [`generate_beanies_quest`](../Reference_and_Meta/Enums.md#enum-generate_beanies_quest) | Enum | Specifies which quest pool (e.g., 'main_pool', 'intro') to generate a quest from. | 1 | `intro`<br>`main_pool` |

</details>


---


### Object: `prereqs`


**Definition:** Object mapping quest or unlock names to their prerequisite mapflags or conditions.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`endoftime`](../Reference_and_Meta/Enums.md#enum-endoftime) | Enum | Configures various attributes of the End of Time area, depending on context. | 4 | `500`<br>`AREA_NAME_ENDOFTIME`<br>`[jurassic theend iceage future lab]` |
| [`jurassic`](../Reference_and_Meta/Enums.md#enum-jurassic) | Enum | Specifies the name, map flag, or connection for the Jurassic area. | 1 | `400`<br>`AREA_NAME_JURASSIC`<br>`[iceage lab]` |
| [`theend`](../Reference_and_Meta/Enums.md#enum-theend) | Enum | Specifies the name, map flag, or connection for The End area. | 1 | `400`<br>`AREA_NAME_THEEND`<br>`[future lab]` |
| [`core`](../Reference_and_Meta/Enums.md#enum-core) | Enum | Specifies the name, map flag, or connection for the Core area. | 1 | `300`<br>`AREA_NAME_CORE`<br>`[bunker desert]` |
| [`dimensionx`](../Reference_and_Meta/Enums.md#enum-dimensionx) | Enum | An enum specifying the Dimension X chapter area, or an object with its specific properties. | 1 | `400`<br>`AREA_NAME_DIMENSIONX`<br>`[moon core bunker crater desert]` |
| [`moon`](../Reference_and_Meta/Enums.md#enum-moon) | Enum | Specifies the name, map flag, or connection for the Moon area. | 1 | `300`<br>`AREA_NAME_MOON`<br>`[crater desert]` |

</details>


---
### Object: `destinations`


**Definition:** Specifies the list of areas and their associated coin rewards for Beanie's quest destinations.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `jurassic` | Integer | Specifies the name, map flag, or connection for the Jurassic area. | 1 | `400`<br>`AREA_NAME_JURASSIC`<br>`[iceage lab]` |
| `theend` | Integer | Specifies the name, map flag, or connection for The End area. | 1 | `400`<br>`AREA_NAME_THEEND`<br>`[future lab]` |
| `boneyard` | Integer | Specifies the name, map flag, or connection for the Boneyard area. | 1 | `200`<br>`AREA_NAME_BONEYARD`<br>`[junkyard alley]` |
| `core` | Integer | Specifies the name, map flag, or connection for the Core area. | 1 | `300`<br>`AREA_NAME_CORE`<br>`[bunker desert]` |
| `dimensionx` | Integer | An enum specifying the Dimension X chapter area, or an object with its specific properties. | 1 | `400`<br>`AREA_NAME_DIMENSIONX`<br>`[moon core bunker crater desert]` |
| `endoftime` | Integer | Configures various attributes of the End of Time area, depending on context. | 1 | `500`<br>`AREA_NAME_ENDOFTIME`<br>`[jurassic theend iceage future lab]` |
| `meatworld` | Integer | An enum specifying the Meatworld chapter area, or an object with its specific properties. | 1 | `300`<br>`AREA_NAME_MEATWORLD`<br>`[caves boneyard junkyard sewers alley]` |
| `moon` | Integer | Specifies the name, map flag, or connection for the Moon area. | 1 | `300`<br>`AREA_NAME_MOON`<br>`[crater desert]` |
| `caves` | Integer | Specifies the name, map flag, or connection for the Caves area. | 1 | `200`<br>`AREA_NAME_CAVES`<br>`[sewers alley]` |

</details>


---

