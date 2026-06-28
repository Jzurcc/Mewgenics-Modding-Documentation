---
title: "NPC Scripts Schema"
description: "Behavior logic for non-combat interactive NPCs."
---

# NPC Scripts Schema

## Overview
This schema hooks scripts to town NPCs to control their dialogue, quest-giving behavior, and idle animations.

## Usage Example
Here is a real example of this object being defined in the game's data:
```gon
Blacksmith {
    npc "Blacksmith"
    idle_anim "hammering"
    on_talk {
        script "open_upgrade_menu"
    }
}
```

## Associated Directory Files
To see extracted instances of this schema in the base game, refer to:
- [`NPC_Scripts.md`](../../Directory/World_and_Events/NPC_Scripts.md)

---



This document is an exhaustive, auto-generated dictionary of `.gon` properties relevant to this subsystem. While the overview above provides high-level context, you may still need to infer exact engine execution rules through testing or context clues.

## NPC Scripts


### Object: `ROOT`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`intro`](./NPC_Scripts.md#object-intro) | Object  | An object defining the introductory cutscene for the event, including title, cat selection, and visuals. | 239 | `{ . . . }` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 161 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`states`](./NPC_Scripts.md#object-states) | Object  | Defines named animation states and their associated animation clips. | 12 | `{ . . . }` |
| [`transitions`](./NPC_Scripts.md#object-transitions) | Object  | Defines named transitions between animation states. | 12 | `{ . . . }` |
| [`unprompted`](./NPC_Scripts.md#object-unprompted) | Object  | Defines sequences of unprompted dialog events. | 8 | `{ . . . }` |
| [`also`](./NPC_Scripts.md#object-also) | Object  | Defines an additional dialog sequence that plays alongside the main one. | 8 | `{ . . . }` |
| [`unknown`](./NPC_Scripts.md#object-unknown) | Object  | A generic object container for dialog and rewards, often used for unprompted sequences. | 8 | `{ . . . }` |
| [`hide_text`](./NPC_Scripts.md#object-hide_text) | Object  | Defines a sequence that hides text dialogs and autopasses to the next step. | 4 | `{ . . . }` |
| [`purchase_item`](./NPC_Scripts.md#object-purchase_item) | Object  | Defines the dialog sequence for purchasing an item from an NPC. | 4 | `{ . . . }` |
| [`unprompted_a`](./NPC_Scripts.md#object-unprompted_a) | Object  | Defines a dialog sequence that plays when the player approaches the NPC without a prompt, labeled as the first variant. | 4 | `{ . . . }` |
| [`unprompted_b`](./NPC_Scripts.md#object-unprompted_b) | Object  | Defines a dialog sequence that plays when the player approaches the NPC without a prompt, labeled as the second variant. | 4 | `{ . . . }` |
| [`unprompted_c`](./NPC_Scripts.md#object-unprompted_c) | Object  | Defines a dialog sequence that plays when the player approaches the NPC without a prompt, labeled as the third variant. | 4 | `{ . . . }` |
| [`unprompted_d`](./NPC_Scripts.md#object-unprompted_d) | Object  | Defines a dialog sequence that plays when the player approaches the NPC without a prompt, labeled as the fourth variant. | 4 | `{ . . . }` |
| [`unprompted_e`](./NPC_Scripts.md#object-unprompted_e) | Object  | Defines a dialog sequence that plays when the player approaches the NPC without a prompt, labeled as the fifth variant. | 4 | `{ . . . }` |
| [`unprompted_f`](./NPC_Scripts.md#object-unprompted_f) | Object  | Defines a dialog sequence that plays when the player approaches the NPC without a prompt, labeled as the sixth variant. | 4 | `{ . . . }` |
| [`unprompted_g`](./NPC_Scripts.md#object-unprompted_g) | Object  | Defines a dialog sequence that plays when the player approaches the NPC without a prompt, labeled as the seventh variant. | 4 | `{ . . . }` |
| [`unprompted_h`](./NPC_Scripts.md#object-unprompted_h) | Object  | Defines a dialog sequence that plays when the player approaches the NPC without a prompt, labeled as the eighth variant. | 4 | `{ . . . }` |
| [`unprompted_i`](./NPC_Scripts.md#object-unprompted_i) | Object  | Defines a dialog sequence that plays when the player approaches the NPC without a prompt, labeled as the ninth variant. | 4 | `{ . . . }` |
| [`cant_afford`](./NPC_Scripts.md#object-cant_afford) | Object  | Defines the dialog sequence that plays when the player attempts to purchase an item they cannot afford. | 3 | `{ . . . }` |
| [`forward_to_tips`](./NPC_Scripts.md#object-forward_to_tips) | Object  | Defines a dialog sequence that forwards the player to a random tip dialog for the current NPC. | 3 | `{ . . . }` |
| [`out_of_stock`](./NPC_Scripts.md#object-out_of_stock) | Object  | Defines the dialog sequence that plays when a shop item is out of stock. | 3 | `{ . . . }` |
| [`beanies_quests_intro`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-beanies_quests_intro) | Object  | Defines the initial dialog or quest-generation sequence for Dr. Beanies' quests. | 2 | `{ . . . }` |
| [`beanies_quests_repeat`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-beanies_quests_repeat) | Object  | Defines the repeatable quest dialog or generator for Dr. Beanies. | 2 | `{ . . . }` |
| [`frank_max_intro`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-frank_max_intro) | Object  | Defines the dialog sequence and rewards for reaching max favor with Frank. | 2 | `{ . . . }` |
| [`frank_max_repeating`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-frank_max_repeating) | Object  | Defines the repeatable dialog sequence and rewards for Frank at max favor. | 2 | `{ . . . }` |
| [`house_upgrade_4throom`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-house_upgrade_4throom) | Object  | Defines the dialog and house upgrade for unlocking the 4th room. | 2 | `{ . . . }` |
| [`house_upgrade_attic`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-house_upgrade_attic) | Object  | Defines the dialog and house upgrade for the attic. | 2 | `{ . . . }` |
| [`house_upgrade_largehouse`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-house_upgrade_largehouse) | Object  | Defines the dialog and house upgrade for the large house. | 2 | `{ . . . }` |
| [`house_upgrade_mediumhouse`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-house_upgrade_mediumhouse) | Object  | Defines the dialog and house upgrade for the medium house. | 2 | `{ . . . }` |
| [`jack_max_intro`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-jack_max_intro) | Object  | Defines the dialog sequence and rewards for reaching max favor with Jack. | 2 | `{ . . . }` |
| [`jack_max_repeating`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-jack_max_repeating) | Object  | Defines the repeatable dialog sequence and rewards for Jack at max favor. | 2 | `{ . . . }` |
| [`jack_shopupgrade1`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-jack_shopupgrade1) | Object  | Defines the dialog and shop level up for Jack's first shop upgrade. | 2 | `{ . . . }` |
| [`jack_shopupgrade2`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-jack_shopupgrade2) | Object  | Defines the dialog and shop level up for Jack's second shop upgrade. | 2 | `{ . . . }` |
| [`jack_shopupgrade3`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-jack_shopupgrade3) | Object  | Defines the dialog and shop level up for Jack's third shop upgrade. | 2 | `{ . . . }` |
| [`jack_shopupgrade4`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-jack_shopupgrade4) | Object  | Defines the dialog and shop level up for Jack's fourth shop upgrade. | 2 | `{ . . . }` |
| [`organ_max_intro`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-organ_max_intro) | Object  | Defines the dialog sequence and rewards for reaching max favor with Organ Grinder. | 2 | `{ . . . }` |
| [`organ_max_repeating`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-organ_max_repeating) | Object  | Defines the repeatable dialog sequence and rewards for Organ Grinder at max favor. | 2 | `{ . . . }` |
| [`organ_unlock`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-organ_unlock) | Object  | Defines the dialog and shop level up for unlocking Organ Grinder. | 2 | `{ . . . }` |
| [`organ_upgrade1`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-organ_upgrade1) | Object  | Defines the dialog and shop level up for Organ Grinder's first upgrade. | 2 | `{ . . . }` |
| [`organ_upgrade2`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-organ_upgrade2) | Object  | Defines the dialog and shop level up for Organ Grinder's second upgrade. | 2 | `{ . . . }` |
| [`organ_upgrade3`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-organ_upgrade3) | Object  | Defines the dialog and shop level up for Organ Grinder's third upgrade. | 2 | `{ . . . }` |
| [`organ_upgrade4`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-organ_upgrade4) | Object  | Defines the dialog and shop level up for Organ Grinder's fourth upgrade. | 2 | `{ . . . }` |
| [`organ_upgrade5`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-organ_upgrade5) | Object  | Defines the dialog and shop level up for Organ Grinder's fifth upgrade. | 2 | `{ . . . }` |
| [`organ_upgrade6`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-organ_upgrade6) | Object  | Defines the dialog and shop level up for Organ Grinder's sixth upgrade. | 2 | `{ . . . }` |
| [`steven_milliontrashed`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-steven_milliontrashed) | Object  | A dialogue sequence or favor reward configuration for the NPC Steven, triggered when the player has accumulated 1,000,000 favor. | 2 | `{ . . . }` |
| [`tink_aggression`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tink_aggression) | Object  | A dialogue sequence or favor reward that unlocks the cat info panel for viewing a cat's aggression stat. | 2 | `{ . . . }` |
| [`tink_basestats`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tink_basestats) | Object  | A dialogue sequence or favor reward that unlocks the cat info panel for viewing a cat's base stats and stat modifications. | 2 | `{ . . . }` |
| [`tink_inbreeding`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tink_inbreeding) | Object  | A dialogue sequence or favor reward that unlocks the cat info panel for viewing a cat's inbreeding level and family tree. | 2 | `{ . . . }` |
| [`tink_max_intro`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tink_max_intro) | Object  | The first dialogue sequence and favor reward that plays when Tink reaches maximum favor. | 2 | `{ . . . }` |
| [`tink_max_repeating`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tink_max_repeating) | Object  | A repeating dialogue sequence and favor reward that plays when Tink is at maximum favor, cycling through random sub-sequences. | 2 | `{ . . . }` |
| [`tink_prettybow`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tink_prettybow) | Object  | A dialogue sequence and favor reward that grants the gift item TinksBow. | 2 | `{ . . . }` |
| [`tink_relationships`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tink_relationships) | Object  | A dialogue sequence or favor reward that unlocks the cat info panel for viewing a cat's relationships (loves and hates). | 2 | `{ . . . }` |
| [`tink_sexuality`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tink_sexuality) | Object  | A dialogue sequence or favor reward that unlocks the cat info panel for viewing a cat's libido and sexual orientation flags. | 2 | `{ . . . }` |
| [`tink_tags`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tink_tags) | Object  | A dialogue sequence or favor reward that unlocks the ability to manually add symbols to a cat's name. | 2 | `{ . . . }` |
| [`tracy_blankcollar1`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tracy_blankcollar1) | Object  | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 2 | `{ . . . }` |
| [`tracy_blankcollar2`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tracy_blankcollar2) | Object  | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 2 | `{ . . . }` |
| [`tracy_blankcollar3`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tracy_blankcollar3) | Object  | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 2 | `{ . . . }` |
| [`tracy_foodstorage1`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tracy_foodstorage1) | Object  | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 2 | `{ . . . }` |
| [`tracy_foodstorage10`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tracy_foodstorage10) | Object  | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 2 | `{ . . . }` |
| [`tracy_foodstorage2`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tracy_foodstorage2) | Object  | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 2 | `{ . . . }` |
| [`tracy_foodstorage3`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tracy_foodstorage3) | Object  | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 2 | `{ . . . }` |
| [`tracy_foodstorage4`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tracy_foodstorage4) | Object  | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 2 | `{ . . . }` |
| [`tracy_foodstorage5`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tracy_foodstorage5) | Object  | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 2 | `{ . . . }` |
| [`tracy_foodstorage6`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tracy_foodstorage6) | Object  | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 2 | `{ . . . }` |
| [`tracy_foodstorage7`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tracy_foodstorage7) | Object  | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 2 | `{ . . . }` |
| [`tracy_foodstorage8`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tracy_foodstorage8) | Object  | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 2 | `{ . . . }` |
| [`tracy_foodstorage9`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tracy_foodstorage9) | Object  | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 2 | `{ . . . }` |
| [`tracy_idol1`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tracy_idol1) | Object  | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 2 | `{ . . . }` |
| [`tracy_idol2`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tracy_idol2) | Object  | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 2 | `{ . . . }` |
| [`tracy_idol3`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tracy_idol3) | Object  | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 2 | `{ . . . }` |
| [`tracy_idol4`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tracy_idol4) | Object  | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 2 | `{ . . . }` |
| [`tracy_idol5`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tracy_idol5) | Object  | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 2 | `{ . . . }` |
| [`tracy_idol6`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tracy_idol6) | Object  | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 2 | `{ . . . }` |
| [`tracy_idol7`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tracy_idol7) | Object  | A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level. | 2 | `{ . . . }` |
| [`tracy_max_intro`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tracy_max_intro) | Object  | The first dialogue sequence and bonus rare item reward that plays when Tracy reaches maximum favor. | 2 | `{ . . . }` |
| [`tracy_max_repeating`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tracy_max_repeating) | Object  | A repeating dialogue sequence and favor reward that plays when Tracy is at maximum favor, cycling through random sub-sequences. | 2 | `{ . . . }` |
| [`upgrade_storage_1`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-upgrade_storage_1) | Object  | A dialogue sequence and storage expansion reward for Butch, requiring act 0 and chapter 0. | 2 | `{ . . . }` |
| [`upgrade_storage_2`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-upgrade_storage_2) | Object  | A dialogue sequence and storage expansion reward for Butch, requiring act 1 and chapter 2. | 2 | `{ . . . }` |
| [`upgrade_storage_3`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-upgrade_storage_3) | Object  | A dialogue sequence and storage expansion reward for Butch, requiring act 1 and chapter 3. | 2 | `{ . . . }` |
| [`upgrade_storage_4`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-upgrade_storage_4) | Object  | A dialogue sequence and storage expansion reward for Butch, requiring act 2 and chapter 2. | 2 | `{ . . . }` |
| [`upgrade_storage_5`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-upgrade_storage_5) | Object  | A dialogue sequence and storage expansion reward for Butch, requiring act 2 and chapter 3. | 2 | `{ . . . }` |
| [`upgrade_storage_6`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-upgrade_storage_6) | Object  | A dialogue sequence and storage expansion reward for Butch, requiring act 3 and chapter 2. | 2 | `{ . . . }` |
| [`upgrade_storage_7`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-upgrade_storage_7) | Object  | A dialogue sequence and storage expansion reward for Butch, requiring act 3 and chapter 3. | 2 | `{ . . . }` |
| [`upgrade_storage_repeating_crazy`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-upgrade_storage_repeating_crazy) | Object  | A repeating dialogue sequence for Butch's storage upgrade at crazy difficulty, granting one storage expansion. | 2 | `{ . . . }` |
| [`upgrade_storage_repeating_hard`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-upgrade_storage_repeating_hard) | Object  | A repeating dialogue sequence for Butch's storage upgrade at hard difficulty, granting one storage expansion. | 2 | `{ . . . }` |
| [`upgrade_storage_repeating_impossible`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-upgrade_storage_repeating_impossible) | Object  | A repeating dialogue sequence for Butch's storage upgrade at impossible difficulty, granting one storage expansion. | 2 | `{ . . . }` |
| [`upgrade_storage_repeating_intro`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-upgrade_storage_repeating_intro) | Object  | The introductory dialogue sequence and reward when Butch maxes out storage capacity. | 2 | `{ . . . }` |
| [`upgrade_storage_repeating_normal`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-upgrade_storage_repeating_normal) | Object  | A repeating dialogue sequence for Butch's storage upgrade at normal difficulty, granting one storage expansion. | 2 | `{ . . . }` |
| [`beanies_bombquest_2`](./NPC_Scripts.md#object-beanies_bombquest_2) | Object  | Defines the dialog sequence for Beanies' bomb quest step 2. | 1 | `{ . . . }` |
| [`beanies_bombquest_3`](./NPC_Scripts.md#object-beanies_bombquest_3) | Object  | Defines the dialog sequence for the third stage of Beanies' bomb quest. | 1 | `{ . . . }` |
| [`beanies_bombquest_fail_jarofblood`](./NPC_Scripts.md#object-beanies_bombquest_fail_jarofblood) | Object  | Defines the dialog sequence for failing the bomb quest by losing or misusing the jar of blood. | 1 | `{ . . . }` |
| [`beanies_bombquest_fail_jarofchaos`](./NPC_Scripts.md#object-beanies_bombquest_fail_jarofchaos) | Object  | Defines the dialog sequence for failing the bomb quest by losing or misusing the jar of chaos. | 1 | `{ . . . }` |
| [`beanies_bombquest_amnesia`](./NPC_Scripts.md#object-beanies_bombquest_amnesia) | Object  | Defines the dialog sequence for Dr. Beanies' amnesia after a successful nuke quest. | 1 | `{ . . . }` |
| [`beanies_bombquest_begin`](./NPC_Scripts.md#object-beanies_bombquest_begin) | Object  | Defines the dialog sequence for Dr. Beanies beginning the final bomb quest. | 1 | `{ . . . }` |
| [`beanies_bombquest_fail_jarofradiation`](./NPC_Scripts.md#object-beanies_bombquest_fail_jarofradiation) | Object  | Defines the dialog sequence for failing the bomb quest during the Act 1 jar-of-radiation stage. | 1 | `{ . . . }` |
| [`beanies_bombquest_fail_nuke`](./NPC_Scripts.md#object-beanies_bombquest_fail_nuke) | Object  | Defines the dialog sequence for failing the bomb quest during the Act 3 nuke stage. | 1 | `{ . . . }` |
| [`beanies_future_intro`](./NPC_Scripts.md#object-beanies_future_intro) | Object  | Defines the dialog sequence where Dr. Beanies sends the player to the future. | 1 | `{ . . . }` |
| [`beanies_jurassic_intro`](./NPC_Scripts.md#object-beanies_jurassic_intro) | Object  | Defines the dialog sequence for Dr. Beanies' introduction to the Jurassic area. | 1 | `{ . . . }` |
| [`beanies_lab_intro`](./NPC_Scripts.md#object-beanies_lab_intro) | Object  | Defines the dialog sequence where Dr. Beanies is homeless and credits roll. | 1 | `{ . . . }` |
| [`beanies_theend_intro`](./NPC_Scripts.md#object-beanies_theend_intro) | Object  | Defines the dialog sequence where Dr. Beanies responds to you killing Hitler. | 1 | `{ . . . }` |
| [`butch_boneyard_intro`](./NPC_Scripts.md#object-butch_boneyard_intro) | Object  | Defines the dialog sequence for Butch's introduction in the boneyard. | 1 | `{ . . . }` |
| [`class_unlock_jester`](./NPC_Scripts.md#object-class_unlock_jester) | Object  | Defines the dialog sequence for unlocking the Jester class. | 1 | `{ . . . }` |
| [`frank_caves_intro`](./NPC_Scripts.md#object-frank_caves_intro) | Object  | Defines the dialog sequence for Frank's introduction in the caves. | 1 | `{ . . . }` |
| [`frank_ending`](./NPC_Scripts.md#object-frank_ending) | Object  | Defines the dialog sequence for Frank's new intro after the nuke ending. | 1 | `{ . . . }` |
| [`jack_desert_intro`](./NPC_Scripts.md#object-jack_desert_intro) | Object  | Defines the dialog sequence for Jack's introduction in the desert. | 1 | `{ . . . }` |
| [`organ_boneyard_intro`](./NPC_Scripts.md#object-organ_boneyard_intro) | Object  | Defines the dialog sequence for Organ Grinder's introduction in the boneyard. | 1 | `{ . . . }` |
| [`organ_throbbingdomain_intro`](./NPC_Scripts.md#object-organ_throbbingdomain_intro) | Object  | Defines the dialog sequence for Organ Grinder's introduction in the throbbing domain. | 1 | `{ . . . }` |
| [`steven_postendgame`](./NPC_Scripts.md#object-steven_postendgame) | Object  | A dialogue sequence for Steven that plays after the player has beaten the game and seen the final ending. | 1 | `{ . . . }` |
| [`beanies_begin_accepting_cats`](./NPC_Scripts.md#object-beanies_begin_accepting_cats) | Object  | A cutscene sequence where Beanies begins accepting cats, playing dialogue and adjusting camera states. | 1 | `{ . . . }` |
| [`beanies_hitler3`](./NPC_Scripts.md#object-beanies_hitler3) | Object  | A cutscene sequence where Beanies reveals that Hitler has been sending robots back in time, introducing Hitler as the final boss. | 1 | `{ . . . }` |
| [`beanies_hitler3_defeat`](./NPC_Scripts.md#object-beanies_hitler3_defeat) | Object  | A cutscene sequence where Beanies provides the final piece of tech to unlock the infinite after defeating Hitler. | 1 | `{ . . . }` |
| [`beanies_iloveyou`](./NPC_Scripts.md#object-beanies_iloveyou) | Object  | A cutscene sequence where Beanies expresses love to the player through dialogue. | 1 | `{ . . . }` |
| [`beanies_infinite_intro`](./NPC_Scripts.md#object-beanies_infinite_intro) | Object  | A cutscene sequence where Beanies unlocks the infinite and urges the player to challenge the creator. | 1 | `{ . . . }` |
| [`beanies_quest_complete`](./NPC_Scripts.md#object-beanies_quest_complete) | Object  | A cutscene sequence that triggers upon successfully completing Beanies' side quest. | 1 | `{ . . . }` |
| [`beanies_quest_fail`](./NPC_Scripts.md#object-beanies_quest_fail) | Object  | A cutscene sequence that triggers upon failing Beanies' side quest. | 1 | `{ . . . }` |
| [`beanies_rift_intro`](./NPC_Scripts.md#object-beanies_rift_intro) | Object  | A cutscene sequence where Beanies comments on the chaos realm. | 1 | `{ . . . }` |
| [`beanies_screenshake_test`](./NPC_Scripts.md#object-beanies_screenshake_test) | Object  | A cutscene sequence with a dialog followed by a screen shake effect. | 1 | `{ . . . }` |
| [`beanies_seefuture`](./NPC_Scripts.md#object-beanies_seefuture) | Object  | A cutscene sequence where Beanies reacts to the player seeing the future. | 1 | `{ . . . }` |
| [`beanies_seetheend`](./NPC_Scripts.md#object-beanies_seetheend) | Object  | A cutscene sequence where Beanies responds to the player seeing the far future. | 1 | `{ . . . }` |
| [`beanies_terminator1_defeat`](./NPC_Scripts.md#object-beanies_terminator1_defeat) | Object  | A cutscene sequence that plays when the first terminator is killed. | 1 | `{ . . . }` |
| [`beanies_terminator2_defeat`](./NPC_Scripts.md#object-beanies_terminator2_defeat) | Object  | A cutscene sequence where Beanies invents more time-bending tech after the second terminator is defeated. | 1 | `{ . . . }` |
| [`beanies_timemachine_2`](./NPC_Scripts.md#object-beanies_timemachine_2) | Object  | A cutscene sequence where a frustrated Beanies sends the player into the future to gather information. | 1 | `{ . . . }` |
| [`beanies_timemachine_intro`](./NPC_Scripts.md#object-beanies_timemachine_intro) | Object  | A cutscene sequence where Beanies explains how the time machine works and the butterfly effect. | 1 | `{ . . . }` |
| [`beanies_vscreator1`](./NPC_Scripts.md#object-beanies_vscreator1) | Object  | A cutscene sequence where Beanies tells the player to detonate the nuke against the creator. | 1 | `{ . . . }` |
| [`beanies_vscreator2`](./NPC_Scripts.md#object-beanies_vscreator2) | Object  | A cutscene sequence where Beanies attempts to convince the player to detonate the nuke if they refuse. | 1 | `{ . . . }` |
| [`beanies_vscreator3`](./NPC_Scripts.md#object-beanies_vscreator3) | Object  | A cutscene sequence where an angry Beanies continues to try to convince the player to end it. | 1 | `{ . . . }` |
| [`beanies_vscreator4`](./NPC_Scripts.md#object-beanies_vscreator4) | Object  | A cutscene sequence where Beanies sets off the nuke himself after the player's refusal. | 1 | `{ . . . }` |
| [`beanies_vscreatorintro`](./NPC_Scripts.md#object-beanies_vscreatorintro) | Object  | A cutscene sequence where Beanies explains how to end everything. | 1 | `{ . . . }` |
| [`beaniesquest_complete_AI`](./NPC_Scripts.md#object-beaniesquest_complete_ai) | Object  | A cutscene sequence that plays upon completing the AI-related portion of Beanies' quest. | 1 | `{ . . . }` |
| [`beaniesquest_complete_AirHorn`](./NPC_Scripts.md#object-beaniesquest_complete_airhorn) | Object  | A cutscene sequence that plays upon completing the AirHorn-related portion of Beanies' quest. | 1 | `{ . . . }` |
| [`beaniesquest_complete_AngryFace`](./NPC_Scripts.md#object-beaniesquest_complete_angryface) | Object  | The completion dialogue sequence for the AngryFace sidequest, triggered when the quest is fulfilled. | 1 | `{ . . . }` |
| [`beaniesquest_complete_AnimalHands`](./NPC_Scripts.md#object-beaniesquest_complete_animalhands) | Object  | The completion dialogue sequence for the AnimalHands sidequest, triggered when the quest is fulfilled. | 1 | `{ . . . }` |
| [`beaniesquest_complete_BubbleBoy`](./NPC_Scripts.md#object-beaniesquest_complete_bubbleboy) | Object  | The completion dialogue sequence for the BubbleBoy sidequest, triggered when the quest is fulfilled. | 1 | `{ . . . }` |
| [`beaniesquest_complete_ChadImplant`](./NPC_Scripts.md#object-beaniesquest_complete_chadimplant) | Object  | The completion dialogue sequence for the ChadImplant sidequest, triggered when the quest is fulfilled. | 1 | `{ . . . }` |
| [`beaniesquest_complete_ChaosDevice`](./NPC_Scripts.md#object-beaniesquest_complete_chaosdevice) | Object  | The completion dialogue sequence for the ChaosDevice sidequest, triggered when the quest is fulfilled. | 1 | `{ . . . }` |
| [`beaniesquest_complete_DimensionalDivider`](./NPC_Scripts.md#object-beaniesquest_complete_dimensionaldivider) | Object  | The completion dialogue sequence for the DimensionalDivider sidequest, triggered when the quest is fulfilled. | 1 | `{ . . . }` |
| [`beaniesquest_complete_DiseaseJar`](./NPC_Scripts.md#object-beaniesquest_complete_diseasejar) | Object  | The completion dialogue sequence for the DiseaseJar sidequest, triggered when the quest is fulfilled. | 1 | `{ . . . }` |
| [`beaniesquest_complete_ExperimentalTreatment`](./NPC_Scripts.md#object-beaniesquest_complete_experimentaltreatment) | Object  | The completion dialogue sequence for the ExperimentalTreatment sidequest, triggered when the quest is fulfilled. | 1 | `{ . . . }` |
| [`beaniesquest_complete_FartFace`](./NPC_Scripts.md#object-beaniesquest_complete_fartface) | Object  | The completion dialogue sequence for the FartFace sidequest, triggered when the quest is fulfilled. | 1 | `{ . . . }` |
| [`beaniesquest_complete_FigLeaf`](./NPC_Scripts.md#object-beaniesquest_complete_figleaf) | Object  | The completion dialogue sequence for the FigLeaf sidequest, triggered when the quest is fulfilled. | 1 | `{ . . . }` |
| [`beaniesquest_complete_Generic`](./NPC_Scripts.md#object-beaniesquest_complete_generic) | Object  | The completion dialogue sequence for a generic sidequest, triggered when the quest is fulfilled. | 1 | `{ . . . }` |
| [`beaniesquest_complete_GlassCannon`](./NPC_Scripts.md#object-beaniesquest_complete_glasscannon) | Object  | The completion dialogue sequence for the GlassCannon sidequest, triggered when the quest is fulfilled. | 1 | `{ . . . }` |
| [`beaniesquest_complete_HardPill`](./NPC_Scripts.md#object-beaniesquest_complete_hardpill) | Object  | The completion dialogue sequence for the HardPill sidequest, triggered when the quest is fulfilled. | 1 | `{ . . . }` |
| [`beaniesquest_complete_HiveMind`](./NPC_Scripts.md#object-beaniesquest_complete_hivemind) | Object  | The completion dialogue sequence for the HiveMind sidequest, triggered when the quest is fulfilled. | 1 | `{ . . . }` |
| [`beaniesquest_complete_MagicMirror`](./NPC_Scripts.md#object-beaniesquest_complete_magicmirror) | Object  | The completion dialogue sequence for the MagicMirror sidequest, triggered when the quest is fulfilled. | 1 | `{ . . . }` |
| [`beaniesquest_complete_MeStone`](./NPC_Scripts.md#object-beaniesquest_complete_mestone) | Object  | The completion dialogue sequence for the MeStone sidequest, triggered when the quest is fulfilled. | 1 | `{ . . . }` |
| [`beaniesquest_complete_MultilinkCable`](./NPC_Scripts.md#object-beaniesquest_complete_multilinkcable) | Object  | The completion dialogue sequence for the MultilinkCable sidequest, triggered when the quest is fulfilled. | 1 | `{ . . . }` |
| [`beaniesquest_complete_MysteriousDice`](./NPC_Scripts.md#object-beaniesquest_complete_mysteriousdice) | Object  | The completion dialogue sequence for the MysteriousDice sidequest, triggered when the quest is fulfilled. | 1 | `{ . . . }` |
| [`beaniesquest_complete_MysteriousGlasses`](./NPC_Scripts.md#object-beaniesquest_complete_mysteriousglasses) | Object  | The completion dialogue sequence for the MysteriousGlasses sidequest, triggered when the quest is fulfilled. | 1 | `{ . . . }` |
| [`beaniesquest_complete_NDEDevice`](./NPC_Scripts.md#object-beaniesquest_complete_ndedevice) | Object  | The completion dialogue sequence for the NDEDevice sidequest, triggered when the quest is fulfilled. | 1 | `{ . . . }` |
| [`beaniesquest_complete_NuclearKnife`](./NPC_Scripts.md#object-beaniesquest_complete_nuclearknife) | Object  | The completion dialogue sequence for the NuclearKnife sidequest, triggered when the quest is fulfilled. | 1 | `{ . . . }` |
| [`beaniesquest_complete_PartialLobotomy`](./NPC_Scripts.md#object-beaniesquest_complete_partiallobotomy) | Object  | The completion dialogue sequence for the PartialLobotomy sidequest, triggered when the quest is fulfilled. | 1 | `{ . . . }` |
| [`beaniesquest_complete_PartyDetonator`](./NPC_Scripts.md#object-beaniesquest_complete_partydetonator) | Object  | The completion dialogue sequence for the PartyDetonator sidequest, triggered when the quest is fulfilled. | 1 | `{ . . . }` |
| [`beaniesquest_complete_PersonalHeater`](./NPC_Scripts.md#object-beaniesquest_complete_personalheater) | Object  | The completion dialogue sequence for the PersonalHeater sidequest, triggered when the quest is fulfilled. | 1 | `{ . . . }` |
| [`beaniesquest_complete_PersuasionDevice`](./NPC_Scripts.md#object-beaniesquest_complete_persuasiondevice) | Object  | The completion dialogue sequence for the PersuasionDevice sidequest, triggered when the quest is fulfilled. | 1 | `{ . . . }` |
| [`beaniesquest_complete_PrincessHat`](./NPC_Scripts.md#object-beaniesquest_complete_princesshat) | Object  | The completion dialogue sequence for the PrincessHat sidequest, triggered when the quest is fulfilled. | 1 | `{ . . . }` |
| [`beaniesquest_complete_RealityScrambler`](./NPC_Scripts.md#object-beaniesquest_complete_realityscrambler) | Object  | The completion dialogue sequence for the RealityScrambler sidequest, triggered when the quest is fulfilled. | 1 | `{ . . . }` |
| [`beaniesquest_complete_Redacted`](./NPC_Scripts.md#object-beaniesquest_complete_redacted) | Object  | The completion dialogue sequence for the Redacted sidequest, triggered when the quest is fulfilled. | 1 | `{ . . . }` |
| [`beaniesquest_complete_SpiderInjector`](./NPC_Scripts.md#object-beaniesquest_complete_spiderinjector) | Object  | The completion dialogue sequence for the SpiderInjector sidequest, triggered when the quest is fulfilled. | 1 | `{ . . . }` |
| [`beaniesquest_complete_Stopwatch`](./NPC_Scripts.md#object-beaniesquest_complete_stopwatch) | Object  | The completion dialogue sequence for the Stopwatch sidequest, triggered when the quest is fulfilled. | 1 | `{ . . . }` |
| [`beaniesquest_complete_StorageLocker`](./NPC_Scripts.md#object-beaniesquest_complete_storagelocker) | Object  | The completion dialogue sequence for the StorageLocker sidequest, triggered when the quest is fulfilled. | 1 | `{ . . . }` |
| [`beaniesquest_complete_TheIOU`](./NPC_Scripts.md#object-beaniesquest_complete_theiou) | Object  | The completion dialogue sequence for the TheIOU sidequest, triggered when the quest is fulfilled. | 1 | `{ . . . }` |
| [`beaniesquest_complete_TheLoner`](./NPC_Scripts.md#object-beaniesquest_complete_theloner) | Object  | The completion dialogue sequence for the TheLoner sidequest, triggered when the quest is fulfilled. | 1 | `{ . . . }` |
| [`beaniesquest_complete_Trapfest99`](./NPC_Scripts.md#object-beaniesquest_complete_trapfest99) | Object  | The completion dialogue sequence for the Trapfest99 sidequest, triggered when the quest is fulfilled. | 1 | `{ . . . }` |
| [`beaniesquest_complete_UltraVision3000`](./NPC_Scripts.md#object-beaniesquest_complete_ultravision3000) | Object  | The completion dialogue sequence for the UltraVision3000 sidequest, triggered when the quest is fulfilled. | 1 | `{ . . . }` |
| [`beaniesquest_fail_AI`](./NPC_Scripts.md#object-beaniesquest_fail_ai) | Object  | The failure dialogue sequence for the AI sidequest, triggered when the quest fails. | 1 | `{ . . . }` |
| [`beaniesquest_fail_AirHorn`](./NPC_Scripts.md#object-beaniesquest_fail_airhorn) | Object  | The failure dialogue sequence for the AirHorn sidequest, triggered when the quest fails. | 1 | `{ . . . }` |
| [`beaniesquest_fail_AngryFace`](./NPC_Scripts.md#object-beaniesquest_fail_angryface) | Object  | The failure dialogue sequence for the AngryFace sidequest, triggered when the quest fails. | 1 | `{ . . . }` |
| [`beaniesquest_fail_AnimalHands`](./NPC_Scripts.md#object-beaniesquest_fail_animalhands) | Object  | The failure dialogue sequence for the AnimalHands sidequest, triggered when the quest fails. | 1 | `{ . . . }` |
| [`beaniesquest_fail_BubbleBoy`](./NPC_Scripts.md#object-beaniesquest_fail_bubbleboy) | Object  | The failure dialogue sequence for the BubbleBoy sidequest, triggered when the quest fails. | 1 | `{ . . . }` |
| [`beaniesquest_fail_ChadImplant`](./NPC_Scripts.md#object-beaniesquest_fail_chadimplant) | Object  | The failure dialogue sequence for the ChadImplant sidequest, triggered when the quest fails. | 1 | `{ . . . }` |
| [`beaniesquest_fail_ChaosDevice`](./NPC_Scripts.md#object-beaniesquest_fail_chaosdevice) | Object  | The failure dialogue sequence for the ChaosDevice sidequest, triggered when the quest fails. | 1 | `{ . . . }` |
| [`beaniesquest_fail_DimensionalDivider`](./NPC_Scripts.md#object-beaniesquest_fail_dimensionaldivider) | Object  | The failure dialogue sequence for the DimensionalDivider sidequest, triggered when the quest fails. | 1 | `{ . . . }` |
| [`beaniesquest_fail_DiseaseJar`](./NPC_Scripts.md#object-beaniesquest_fail_diseasejar) | Object  | The failure dialogue sequence for the DiseaseJar sidequest, triggered when the quest fails. | 1 | `{ . . . }` |
| [`beaniesquest_fail_ExperimentalTreatment`](./NPC_Scripts.md#object-beaniesquest_fail_experimentaltreatment) | Object  | The failure dialogue sequence for the ExperimentalTreatment sidequest, triggered when the quest fails. | 1 | `{ . . . }` |
| [`beaniesquest_fail_FartFace`](./NPC_Scripts.md#object-beaniesquest_fail_fartface) | Object  | The failure dialogue sequence for the FartFace sidequest, triggered when the quest fails. | 1 | `{ . . . }` |
| [`beaniesquest_fail_FigLeaf`](./NPC_Scripts.md#object-beaniesquest_fail_figleaf) | Object  | The failure dialogue sequence for the FigLeaf sidequest, triggered when the quest fails. | 1 | `{ . . . }` |
| [`beaniesquest_fail_Generic`](./NPC_Scripts.md#object-beaniesquest_fail_generic) | Object  | The failure dialogue sequence for a generic sidequest, triggered when the quest fails. | 1 | `{ . . . }` |
| [`beaniesquest_fail_GlassCannon`](./NPC_Scripts.md#object-beaniesquest_fail_glasscannon) | Object  | The failure dialogue sequence for the GlassCannon sidequest, triggered when the quest fails. | 1 | `{ . . . }` |
| [`beaniesquest_fail_HardPill`](./NPC_Scripts.md#object-beaniesquest_fail_hardpill) | Object  | The failure dialogue sequence for the HardPill sidequest, triggered when the quest fails. | 1 | `{ . . . }` |
| [`beaniesquest_fail_HiveMind`](./NPC_Scripts.md#object-beaniesquest_fail_hivemind) | Object  | The dialogue and camera sequence played upon failure of the quest for this item. | 1 | `{ . . . }` |
| [`beaniesquest_fail_MagicMirror`](./NPC_Scripts.md#object-beaniesquest_fail_magicmirror) | Object  | The dialogue and camera sequence played upon failure of the quest for this item. | 1 | `{ . . . }` |
| [`beaniesquest_fail_MeStone`](./NPC_Scripts.md#object-beaniesquest_fail_mestone) | Object  | The dialogue and camera sequence played upon failure of the quest for this item. | 1 | `{ . . . }` |
| [`beaniesquest_fail_MultilinkCable`](./NPC_Scripts.md#object-beaniesquest_fail_multilinkcable) | Object  | The dialogue and camera sequence played upon failure of the quest for this item. | 1 | `{ . . . }` |
| [`beaniesquest_fail_MysteriousDice`](./NPC_Scripts.md#object-beaniesquest_fail_mysteriousdice) | Object  | The dialogue and camera sequence played upon failure of the quest for this item. | 1 | `{ . . . }` |
| [`beaniesquest_fail_MysteriousGlasses`](./NPC_Scripts.md#object-beaniesquest_fail_mysteriousglasses) | Object  | The dialogue and camera sequence played upon failure of the quest for this item. | 1 | `{ . . . }` |
| [`beaniesquest_fail_NDEDevice`](./NPC_Scripts.md#object-beaniesquest_fail_ndedevice) | Object  | The dialogue and camera sequence played upon failure of the quest for this item. | 1 | `{ . . . }` |
| [`beaniesquest_fail_NuclearKnife`](./NPC_Scripts.md#object-beaniesquest_fail_nuclearknife) | Object  | The dialogue and camera sequence played upon failure of the quest for this item. | 1 | `{ . . . }` |
| [`beaniesquest_fail_PartialLobotomy`](./NPC_Scripts.md#object-beaniesquest_fail_partiallobotomy) | Object  | The dialogue and camera sequence played upon failure of the quest for this item. | 1 | `{ . . . }` |
| [`beaniesquest_fail_PartyDetonator`](./NPC_Scripts.md#object-beaniesquest_fail_partydetonator) | Object  | The dialogue and camera sequence played upon failure of the quest for this item. | 1 | `{ . . . }` |
| [`beaniesquest_fail_PersonalHeater`](./NPC_Scripts.md#object-beaniesquest_fail_personalheater) | Object  | The dialogue and camera sequence played upon failure of the quest for this item. | 1 | `{ . . . }` |
| [`beaniesquest_fail_PersuasionDevice`](./NPC_Scripts.md#object-beaniesquest_fail_persuasiondevice) | Object  | The dialogue and camera sequence played upon failure of the quest for this item. | 1 | `{ . . . }` |
| [`beaniesquest_fail_PrincessHat`](./NPC_Scripts.md#object-beaniesquest_fail_princesshat) | Object  | The dialogue and camera sequence played upon failure of the quest for this item. | 1 | `{ . . . }` |
| [`beaniesquest_fail_RealityScrambler`](./NPC_Scripts.md#object-beaniesquest_fail_realityscrambler) | Object  | The dialogue and camera sequence played upon failure of the quest for this item. | 1 | `{ . . . }` |
| [`beaniesquest_fail_Redacted`](./NPC_Scripts.md#object-beaniesquest_fail_redacted) | Object  | The dialogue and camera sequence played upon failure of the quest for this item. | 1 | `{ . . . }` |
| [`beaniesquest_fail_SpiderInjector`](./NPC_Scripts.md#object-beaniesquest_fail_spiderinjector) | Object  | The dialogue and camera sequence played upon failure of the quest for this item. | 1 | `{ . . . }` |
| [`beaniesquest_fail_Stopwatch`](./NPC_Scripts.md#object-beaniesquest_fail_stopwatch) | Object  | The dialogue and camera sequence played upon failure of the quest for this item. | 1 | `{ . . . }` |
| [`beaniesquest_fail_StorageLocker`](./NPC_Scripts.md#object-beaniesquest_fail_storagelocker) | Object  | The dialogue and camera sequence played upon failure of the quest for this item. | 1 | `{ . . . }` |
| [`beaniesquest_fail_TheIOU`](./NPC_Scripts.md#object-beaniesquest_fail_theiou) | Object  | The dialogue and camera sequence played upon failure of the quest for this item. | 1 | `{ . . . }` |
| [`beaniesquest_fail_TheLoner`](./NPC_Scripts.md#object-beaniesquest_fail_theloner) | Object  | The dialogue and camera sequence played upon failure of the quest for this item. | 1 | `{ . . . }` |
| [`beaniesquest_fail_Trapfest99`](./NPC_Scripts.md#object-beaniesquest_fail_trapfest99) | Object  | The dialogue and camera sequence played upon failure of the quest for this item. | 1 | `{ . . . }` |
| [`beaniesquest_fail_UltraVision3000`](./NPC_Scripts.md#object-beaniesquest_fail_ultravision3000) | Object  | The dialogue and camera sequence played upon failure of the quest for this item. | 1 | `{ . . . }` |
| [`beaniesquest_intro_AI`](./NPC_Scripts.md#object-beaniesquest_intro_ai) | Object  | The dialogue and camera sequence played during the introduction of this quest item. | 1 | `{ . . . }` |
| [`beaniesquest_intro_AirHorn`](./NPC_Scripts.md#object-beaniesquest_intro_airhorn) | Object  | The dialogue and camera sequence played during the introduction of this quest item. | 1 | `{ . . . }` |
| [`beaniesquest_intro_AngryFace`](./NPC_Scripts.md#object-beaniesquest_intro_angryface) | Object  | The dialogue and camera sequence played during the introduction of this quest item. | 1 | `{ . . . }` |
| [`beaniesquest_intro_AnimalHands`](./NPC_Scripts.md#object-beaniesquest_intro_animalhands) | Object  | The dialogue and camera sequence played during the introduction of this quest item. | 1 | `{ . . . }` |
| [`beaniesquest_intro_BubbleBoy`](./NPC_Scripts.md#object-beaniesquest_intro_bubbleboy) | Object  | The dialogue and camera sequence played during the introduction of this quest item. | 1 | `{ . . . }` |
| [`beaniesquest_intro_ChadImplant`](./NPC_Scripts.md#object-beaniesquest_intro_chadimplant) | Object  | The dialogue and camera sequence played during the introduction of this quest item. | 1 | `{ . . . }` |
| [`beaniesquest_intro_ChaosDevice`](./NPC_Scripts.md#object-beaniesquest_intro_chaosdevice) | Object  | The dialogue and camera sequence played during the introduction of this quest item. | 1 | `{ . . . }` |
| [`beaniesquest_intro_DimensionalDivider`](./NPC_Scripts.md#object-beaniesquest_intro_dimensionaldivider) | Object  | The dialogue and camera sequence played during the introduction of this quest item. | 1 | `{ . . . }` |
| [`beaniesquest_intro_DiseaseJar`](./NPC_Scripts.md#object-beaniesquest_intro_diseasejar) | Object  | The dialogue and camera sequence played during the introduction of this quest item. | 1 | `{ . . . }` |
| [`beaniesquest_intro_ExperimentalTreatment`](./NPC_Scripts.md#object-beaniesquest_intro_experimentaltreatment) | Object  | The dialogue and camera sequence played during the introduction of this quest item. | 1 | `{ . . . }` |
| [`beaniesquest_intro_FartFace`](./NPC_Scripts.md#object-beaniesquest_intro_fartface) | Object  | The dialogue and camera sequence played during the introduction of this quest item. | 1 | `{ . . . }` |
| [`beaniesquest_intro_FigLeaf`](./NPC_Scripts.md#object-beaniesquest_intro_figleaf) | Object  | The dialogue and camera sequence played during the introduction of this quest item. | 1 | `{ . . . }` |
| [`beaniesquest_intro_Generic`](./NPC_Scripts.md#object-beaniesquest_intro_generic) | Object  | The dialogue and camera sequence played during the introduction of this quest item. | 1 | `{ . . . }` |
| [`beaniesquest_intro_GlassCannon`](./NPC_Scripts.md#object-beaniesquest_intro_glasscannon) | Object  | The dialogue and camera sequence played during the introduction of this quest item. | 1 | `{ . . . }` |
| [`beaniesquest_intro_HardPill`](./NPC_Scripts.md#object-beaniesquest_intro_hardpill) | Object  | The dialogue and camera sequence played during the introduction of this quest item. | 1 | `{ . . . }` |
| [`beaniesquest_intro_HiveMind`](./NPC_Scripts.md#object-beaniesquest_intro_hivemind) | Object  | The dialogue and camera sequence played during the introduction of this quest item. | 1 | `{ . . . }` |
| [`beaniesquest_intro_MagicMirror`](./NPC_Scripts.md#object-beaniesquest_intro_magicmirror) | Object  | The dialogue and camera sequence played during the introduction of this quest item. | 1 | `{ . . . }` |
| [`beaniesquest_intro_MeStone`](./NPC_Scripts.md#object-beaniesquest_intro_mestone) | Object  | The dialogue and camera sequence played during the introduction of this quest item. | 1 | `{ . . . }` |
| [`beaniesquest_intro_MultilinkCable`](./NPC_Scripts.md#object-beaniesquest_intro_multilinkcable) | Object  | The dialogue and camera sequence played during the introduction of this quest item. | 1 | `{ . . . }` |
| [`beaniesquest_intro_MysteriousDice`](./NPC_Scripts.md#object-beaniesquest_intro_mysteriousdice) | Object  | The dialogue and camera sequence played during the introduction of this quest item. | 1 | `{ . . . }` |
| [`beaniesquest_intro_MysteriousGlasses`](./NPC_Scripts.md#object-beaniesquest_intro_mysteriousglasses) | Object  | The dialogue and camera sequence played during the introduction of this quest item. | 1 | `{ . . . }` |
| [`beaniesquest_intro_NDEDevice`](./NPC_Scripts.md#object-beaniesquest_intro_ndedevice) | Object  | The dialogue and camera sequence played during the introduction of this quest item. | 1 | `{ . . . }` |
| [`beaniesquest_intro_NuclearKnife`](./NPC_Scripts.md#object-beaniesquest_intro_nuclearknife) | Object  | The dialogue and camera sequence played during the introduction of this quest item. | 1 | `{ . . . }` |
| [`beaniesquest_intro_PartialLobotomy`](./NPC_Scripts.md#object-beaniesquest_intro_partiallobotomy) | Object  | The dialogue and camera sequence played during the introduction of this quest item. | 1 | `{ . . . }` |
| [`beaniesquest_intro_PartyDetonator`](./NPC_Scripts.md#object-beaniesquest_intro_partydetonator) | Object  | The dialogue and camera sequence played during the introduction of this quest item. | 1 | `{ . . . }` |
| [`beaniesquest_intro_PersonalHeater`](./NPC_Scripts.md#object-beaniesquest_intro_personalheater) | Object  | The dialogue and camera sequence played during the introduction of this quest item. | 1 | `{ . . . }` |
| [`beaniesquest_intro_PersuasionDevice`](./NPC_Scripts.md#object-beaniesquest_intro_persuasiondevice) | Object  | The dialogue and camera sequence played during the introduction of this quest item. | 1 | `{ . . . }` |
| [`beaniesquest_intro_PrincessHat`](./NPC_Scripts.md#object-beaniesquest_intro_princesshat) | Object  | The dialogue and camera sequence played during the introduction of this quest item. | 1 | `{ . . . }` |
| [`beaniesquest_intro_RealityScrambler`](./NPC_Scripts.md#object-beaniesquest_intro_realityscrambler) | Object  | A sequence of dialog and state changes for Beanie's quest intro involving the Reality Scrambler item. | 1 | `{ . . . }` |
| [`beaniesquest_intro_Redacted`](./NPC_Scripts.md#object-beaniesquest_intro_redacted) | Object  | A sequence of dialog and state changes for Beanie's quest intro involving the Redacted item. | 1 | `{ . . . }` |
| [`beaniesquest_intro_SpiderInjector`](./NPC_Scripts.md#object-beaniesquest_intro_spiderinjector) | Object  | A sequence of dialog and state changes for Beanie's quest intro involving the Spider Injector item. | 1 | `{ . . . }` |
| [`beaniesquest_intro_Stopwatch`](./NPC_Scripts.md#object-beaniesquest_intro_stopwatch) | Object  | A sequence of dialog and state changes for Beanie's quest intro involving the Stopwatch item. | 1 | `{ . . . }` |
| [`beaniesquest_intro_StorageLocker`](./NPC_Scripts.md#object-beaniesquest_intro_storagelocker) | Object  | A sequence of dialog and state changes for Beanie's quest intro involving the Storage Locker item. | 1 | `{ . . . }` |
| [`beaniesquest_intro_TheIOU`](./NPC_Scripts.md#object-beaniesquest_intro_theiou) | Object  | A sequence of dialog and state changes for Beanie's quest intro involving The IOU item. | 1 | `{ . . . }` |
| [`beaniesquest_intro_TheLoner`](./NPC_Scripts.md#object-beaniesquest_intro_theloner) | Object  | A sequence of dialog and state changes for Beanie's quest intro involving The Loner item. | 1 | `{ . . . }` |
| [`beaniesquest_intro_Trapfest99`](./NPC_Scripts.md#object-beaniesquest_intro_trapfest99) | Object  | A sequence of dialog and state changes for Beanie's quest intro involving the Trapfest99 item. | 1 | `{ . . . }` |
| [`beaniesquest_intro_UltraVision3000`](./NPC_Scripts.md#object-beaniesquest_intro_ultravision3000) | Object  | A sequence of dialog and state changes for Beanie's quest intro involving the UltraVision3000 item. | 1 | `{ . . . }` |
| [`boss_fight_intro`](./NPC_Scripts.md#object-boss_fight_intro) | Object  | A sequence of dialog and state changes for the boss fight introduction cutscene. | 1 | `{ . . . }` |
| [`boss_fight_round2`](./NPC_Scripts.md#object-boss_fight_round2) | Object  | A sequence of dialog and state changes for the boss fight round 2 cutscene. | 1 | `{ . . . }` |
| [`butch_begin_accepting_cats`](./NPC_Scripts.md#object-butch_begin_accepting_cats) | Object  | A sequence of dialog and state changes when Butch begins accepting cats into the shelter. | 1 | `{ . . . }` |
| [`butch_first_house_boss_beat`](./NPC_Scripts.md#object-butch_first_house_boss_beat) | Object  | A sequence of dialog and state changes after defeating the first house boss. | 1 | `{ . . . }` |
| [`butch_pyro`](./NPC_Scripts.md#object-butch_pyro) | Object  | A sequence of dialog and state changes discussing Butch's pyro character. | 1 | `{ . . . }` |
| [`butch_tina1`](./NPC_Scripts.md#object-butch_tina1) | Object  | A sequence of dialog and state changes related to Butch and Tina's first interaction. | 1 | `{ . . . }` |
| [`butch_tips_backstab`](./NPC_Scripts.md#object-butch_tips_backstab) | Object  | A tutorial tip sequence explaining the backstab mechanic. | 1 | `{ . . . }` |
| [`butch_tips_charisma`](./NPC_Scripts.md#object-butch_tips_charisma) | Object  | A tutorial tip sequence explaining the charisma stat. | 1 | `{ . . . }` |
| [`butch_tips_combat`](./NPC_Scripts.md#object-butch_tips_combat) | Object  | A tutorial tip sequence covering basic combat mechanics. | 1 | `{ . . . }` |
| [`butch_tips_disorders`](./NPC_Scripts.md#object-butch_tips_disorders) | Object  | A tutorial tip sequence explaining disorders in cats. | 1 | `{ . . . }` |
| [`butch_tips_drafting`](./NPC_Scripts.md#object-butch_tips_drafting) | Object  | A tutorial tip sequence explaining the drafting system. | 1 | `{ . . . }` |
| [`butch_tips_elements`](./NPC_Scripts.md#object-butch_tips_elements) | Object  | A tutorial tip sequence covering elemental damage types. | 1 | `{ . . . }` |
| [`butch_tips_hard`](./NPC_Scripts.md#object-butch_tips_hard) | Object  | A tutorial tip sequence about playing on hard difficulty. | 1 | `{ . . . }` |
| [`butch_tips_headhome`](./NPC_Scripts.md#object-butch_tips_headhome) | Object  | A tutorial tip sequence about returning to the home base. | 1 | `{ . . . }` |
| [`butch_tips_houseboss`](./NPC_Scripts.md#object-butch_tips_houseboss) | Object  | A tutorial tip sequence explaining house bosses. | 1 | `{ . . . }` |
| [`butch_tips_info`](./NPC_Scripts.md#object-butch_tips_info) | Object  | A tutorial tip sequence about viewing information on units. | 1 | `{ . . . }` |
| [`butch_tips_intelligence`](./NPC_Scripts.md#object-butch_tips_intelligence) | Object  | A tutorial tip sequence explaining the intelligence stat. | 1 | `{ . . . }` |
| [`butch_tips_intro`](./NPC_Scripts.md#object-butch_tips_intro) | Object  | The initial tutorial tip sequence that introduces Butch's tips. | 1 | `{ . . . }` |
| [`butch_tips_items`](./NPC_Scripts.md#object-butch_tips_items) | Object  | A tutorial tip sequence about using items in combat. | 1 | `{ . . . }` |
| [`butch_tips_lesscats`](./NPC_Scripts.md#object-butch_tips_lesscats) | Object  | A tutorial tip sequence about managing with fewer cats. | 1 | `{ . . . }` |
| [`butch_tips_magicdamage`](./NPC_Scripts.md#object-butch_tips_magicdamage) | Object  | A tutorial tip sequence explaining magic damage. | 1 | `{ . . . }` |
| [`butch_tips_passives`](./NPC_Scripts.md#object-butch_tips_passives) | Object  | A tutorial tip sequence covering passive abilities. | 1 | `{ . . . }` |
| [`butch_tips_reorient`](./NPC_Scripts.md#object-butch_tips_reorient) | Object  | A tutorial tip sequence explaining the reorient mechanic. | 1 | `{ . . . }` |
| [`butch_tips_rewards`](./NPC_Scripts.md#object-butch_tips_rewards) | Object  | A tutorial tip sequence about earning rewards. | 1 | `{ . . . }` |
| [`butch_tips_tacticalview`](./NPC_Scripts.md#object-butch_tips_tacticalview) | Object  | A tutorial tip sequence about using tactical view. | 1 | `{ . . . }` |
| [`butch_tips_turnorder`](./NPC_Scripts.md#object-butch_tips_turnorder) | Object  | A tutorial tip sequence explaining turn order. | 1 | `{ . . . }` |
| [`butch_tips_wellrounded`](./NPC_Scripts.md#object-butch_tips_wellrounded) | Object  | A tutorial tip sequence about building well-rounded teams. | 1 | `{ . . . }` |
| [`can_still_use_attack`](./NPC_Scripts.md#object-can_still_use_attack) | Object  | A sequence of dialog and state changes when a unit can still use an attack ability. | 1 | `{ . . . }` |
| [`can_still_use_attack_didntspell`](./NPC_Scripts.md#object-can_still_use_attack_didntspell) | Object  | A sequence of dialog and state changes when a unit didn't use a spell but can still attack. | 1 | `{ . . . }` |
| [`cant_afford_a`](./NPC_Scripts.md#object-cant_afford_a) | Object  | A sequence showing dialog when the player cannot afford item A. | 1 | `{ . . . }` |
| [`cant_afford_b`](./NPC_Scripts.md#object-cant_afford_b) | Object  | A sequence showing dialog when the player cannot afford item B. | 1 | `{ . . . }` |
| [`cant_afford_c`](./NPC_Scripts.md#object-cant_afford_c) | Object  | A sequence showing dialog when the player cannot afford item C. | 1 | `{ . . . }` |
| [`cant_afford_d`](./NPC_Scripts.md#object-cant_afford_d) | Object  | A sequence showing dialog when the player cannot afford item D. | 1 | `{ . . . }` |
| [`cant_afford_iceage`](./NPC_Scripts.md#object-cant_afford_iceage) | Object  | A sequence showing dialog when the player cannot afford the Ice Age item. Can also be a boolean flag. | 1 | `{ . . . }` |
| [`cant_afford_jurassic`](./NPC_Scripts.md#object-cant_afford_jurassic) | Object  | A sequence showing dialog when the player cannot afford the Jurassic item. Can also be a boolean flag. | 1 | `{ . . . }` |
| [`cant_afford_moon`](./NPC_Scripts.md#object-cant_afford_moon) | Object  | A sequence showing dialog when the player cannot afford the Moon item. Can also be a boolean flag. | 1 | `{ . . . }` |
| [`cant_afford_theend`](./NPC_Scripts.md#object-cant_afford_theend) | Object  | Defines the sequence for when the player cannot afford the End purchase, optionally cancelable with a dialog and autopass. | 1 | `{ . . . }` |
| [`class_unlock_butcher`](./NPC_Scripts.md#object-class_unlock_butcher) | Object  | Defines the sequence for unlocking the Butcher class, including dialogs and camera state changes. | 1 | `{ . . . }` |
| [`class_unlock_druid`](./NPC_Scripts.md#object-class_unlock_druid) | Object  | Defines the dialog sequence that plays when unlocking the Druid class. | 1 | `{ . . . }` |
| [`class_unlock_medic`](./NPC_Scripts.md#object-class_unlock_medic) | Object  | Defines the dialog sequence that plays when unlocking the Medic class. | 1 | `{ . . . }` |
| [`class_unlock_monk`](./NPC_Scripts.md#object-class_unlock_monk) | Object  | Defines the dialog sequence that plays when unlocking the Monk class. | 1 | `{ . . . }` |
| [`class_unlock_necromancer`](./NPC_Scripts.md#object-class_unlock_necromancer) | Object  | Defines the dialog sequence that plays when unlocking the Necromancer class. | 1 | `{ . . . }` |
| [`class_unlock_psychic`](./NPC_Scripts.md#object-class_unlock_psychic) | Object  | Defines the dialog sequence that plays when unlocking the Psychic class. | 1 | `{ . . . }` |
| [`class_unlock_thief`](./NPC_Scripts.md#object-class_unlock_thief) | Object  | Defines the dialog sequence that plays when unlocking the Thief class. | 1 | `{ . . . }` |
| [`class_unlock_tinkerer`](./NPC_Scripts.md#object-class_unlock_tinkerer) | Object  | Defines the dialog sequence that plays when unlocking the Tinkerer class. | 1 | `{ . . . }` |
| [`collected_new_items`](./NPC_Scripts.md#object-collected_new_items) | Object  | Defines the dialog sequence that plays when the player has collected new items after an adventure. | 1 | `{ . . . }` |
| [`collected_nothing`](./NPC_Scripts.md#object-collected_nothing) | Object  | Defines the dialog sequence that plays when the player collected nothing (e.g., died in first combat). | 1 | `{ . . . }` |
| [`do_not_end_turn`](./NPC_Scripts.md#object-do_not_end_turn) | Object  | Defines a dialog sequence warning the player not to end their turn. | 1 | `{ . . . }` |
| [`done_spitting_fail_ally`](./NPC_Scripts.md#object-done_spitting_fail_ally) | Object  | Defines a dialog sequence that plays when a spitting action fails on an ally. | 1 | `{ . . . }` |
| [`done_spitting_fail_miss`](./NPC_Scripts.md#object-done_spitting_fail_miss) | Object  | Defines a dialog sequence that plays when a spitting action misses. | 1 | `{ . . . }` |
| [`done_spitting_fail_rat`](./NPC_Scripts.md#object-done_spitting_fail_rat) | Object  | Defines a dialog sequence that plays when a spitting action fails on a rat. | 1 | `{ . . . }` |
| [`done_spitting_success`](./NPC_Scripts.md#object-done_spitting_success) | Object  | Defines a dialog sequence that plays when a spitting action succeeds. | 1 | `{ . . . }` |
| [`ending`](./NPC_Scripts.md#object-ending) | Object  | Defines the ending dialog sequence with Dr. Beanies after saving the player in the time machine. | 1 | `{ . . . }` |
| [`finish_adventure`](./NPC_Scripts.md#object-finish_adventure) | Object  | Defines a dialog sequence that plays when the player finishes an adventure. | 1 | `{ . . . }` |
| [`first_fight_intro`](./NPC_Scripts.md#object-first_fight_intro) | Object  | Defines the intro dialog sequence for the first fight. | 1 | `{ . . . }` |
| [`first_house_boss_tomorrow`](./NPC_Scripts.md#object-first_house_boss_tomorrow) | Object  | Defines a dialog sequence about a boss arriving tomorrow in the first house. | 1 | `{ . . . }` |
| [`first_house_hint_retired`](./NPC_Scripts.md#object-first_house_hint_retired) | Object  | Defines a dialog sequence giving a hint about a retired cat in the first house. | 1 | `{ . . . }` |
| [`frank_max1`](./NPC_Scripts.md#object-frank_max1) | Object  | Defines a dialog sequence for Frank at maximum affinity level 1. | 1 | `{ . . . }` |
| [`frank_max2`](./NPC_Scripts.md#object-frank_max2) | Object  | Defines a dialog sequence for Frank at maximum affinity level 2. | 1 | `{ . . . }` |
| [`frank_max3`](./NPC_Scripts.md#object-frank_max3) | Object  | Defines a dialog sequence for Frank at maximum affinity level 3. | 1 | `{ . . . }` |
| [`frank_max4`](./NPC_Scripts.md#object-frank_max4) | Object  | Defines a dialog sequence for Frank at maximum affinity level 4. | 1 | `{ . . . }` |
| [`frank_max5`](./NPC_Scripts.md#object-frank_max5) | Object  | Defines a dialog sequence for Frank at maximum affinity level 5. | 1 | `{ . . . }` |
| [`frank_terminator2`](./NPC_Scripts.md#object-frank_terminator2) | Object  | Defines a dialog sequence for Frank's 'terminator' event (likely a special encounter). | 1 | `{ . . . }` |
| [`frank_tips_1`](./NPC_Scripts.md#object-frank_tips_1) | Object  | Defines a tips dialog sequence from Frank (tip #1). | 1 | `{ . . . }` |
| [`frank_tips_10`](./NPC_Scripts.md#object-frank_tips_10) | Object  | Defines a tips dialog sequence from Frank (tip #10). | 1 | `{ . . . }` |
| [`frank_tips_2`](./NPC_Scripts.md#object-frank_tips_2) | Object  | Defines a tips dialog sequence from Frank (tip #2). | 1 | `{ . . . }` |
| [`frank_tips_3`](./NPC_Scripts.md#object-frank_tips_3) | Object  | Defines a tips dialog sequence from Frank (tip #3). | 1 | `{ . . . }` |
| [`frank_tips_4`](./NPC_Scripts.md#object-frank_tips_4) | Object  | Defines a tips dialog sequence from Frank (tip #4). | 1 | `{ . . . }` |
| [`frank_tips_5`](./NPC_Scripts.md#object-frank_tips_5) | Object  | Defines a tips dialog sequence from Frank (tip #5). | 1 | `{ . . . }` |
| [`frank_tips_6`](./NPC_Scripts.md#object-frank_tips_6) | Object  | Defines a tips dialog sequence from Frank (tip #6). | 1 | `{ . . . }` |
| [`frank_tips_7`](./NPC_Scripts.md#object-frank_tips_7) | Object  | Defines a tips dialog sequence from Frank (tip #7). | 1 | `{ . . . }` |
| [`frank_tips_8`](./NPC_Scripts.md#object-frank_tips_8) | Object  | Defines a tips dialog sequence from Frank (tip #8). | 1 | `{ . . . }` |
| [`frank_tips_9`](./NPC_Scripts.md#object-frank_tips_9) | Object  | Defines a tips dialog sequence from Frank (tip #9). | 1 | `{ . . . }` |
| [`gone`](./NPC_Scripts.md#object-gone) | Object  | Sets the NPC state to 'gone', making them disappear from the scene. | 1 | `{ . . . }` |
| [`house_intro`](./NPC_Scripts.md#object-house_intro) | Object  | Defines the intro dialog sequence that plays when entering a house. | 1 | `{ . . . }` |
| [`house_kitten_box`](./NPC_Scripts.md#object-house_kitten_box) | Object  | Defines a dialog sequence about a kitten box in the house. | 1 | `{ . . . }` |
| [`house_pass_day`](./NPC_Scripts.md#object-house_pass_day) | Object  | A sequence that plays dialog and animations when a day passes in the house. | 1 | `{ . . . }` |
| [`house_pass_day2`](./NPC_Scripts.md#object-house_pass_day2) | Object  | A sequence that plays extended dialog and animations when a day passes in the house. | 1 | `{ . . . }` |
| [`house_pipe`](./NPC_Scripts.md#object-house_pipe) | Object  | A sequence that plays dialog and animations related to the house pipe. | 1 | `{ . . . }` |
| [`house_retired_cat_box`](./NPC_Scripts.md#object-house_retired_cat_box) | Object  | A sequence that plays dialog and animations for the retired cat box. | 1 | `{ . . . }` |
| [`house_starred_box`](./NPC_Scripts.md#object-house_starred_box) | Object  | A sequence that plays dialog and animations for the starred box. | 1 | `{ . . . }` |
| [`house_strays`](./NPC_Scripts.md#object-house_strays) | Object  | A sequence that plays dialog and animations for stray cats in the house. | 1 | `{ . . . }` |
| [`house_upgrade_basement`](./NPC_Scripts.md#object-house_upgrade_basement) | Object  | A sequence that triggers dialog and a reward for the first basement upgrade. | 1 | `{ . . . }` |
| [`house_upgrade_basement2`](./NPC_Scripts.md#object-house_upgrade_basement2) | Object  | A sequence that triggers the second basement upgrade and awards favor. | 1 | `{ . . . }` |
| [`house_upgrade_basement3`](./NPC_Scripts.md#object-house_upgrade_basement3) | Object  | A sequence that triggers the third basement upgrade and awards favor. | 1 | `{ . . . }` |
| [`house_upgrade_basement4`](./NPC_Scripts.md#object-house_upgrade_basement4) | Object  | A sequence that triggers the fourth basement upgrade and awards favor. | 1 | `{ . . . }` |
| [`house_upgrade_basement5`](./NPC_Scripts.md#object-house_upgrade_basement5) | Object  | A sequence that triggers the fifth basement upgrade and awards favor. | 1 | `{ . . . }` |
| [`introduce_hard_path`](./NPC_Scripts.md#object-introduce_hard_path) | Object  | A sequence that plays dialog and animations to introduce the hard path. | 1 | `{ . . . }` |
| [`jack_begin_accepting_cats`](./NPC_Scripts.md#object-jack_begin_accepting_cats) | Object  | A sequence that shows Jack's introductory dialog for accepting cats, locking player controls. | 1 | `{ . . . }` |
| [`Jack_Gainaltfurniture`](./NPC_Scripts.md#object-jack_gainaltfurniture) | Object  | A sequence that plays Jack's dialog explaining rare alt furniture and the Nona cat, locking controls. | 1 | `{ . . . }` |
| [`jack_introduction`](./NPC_Scripts.md#object-jack_introduction) | Object  | A sequence that plays Jack's initial introduction dialog and animation. | 1 | `{ . . . }` |
| [`jack_max1`](./NPC_Scripts.md#object-jack_max1) | Object  | A sequence that plays Jack's first max favor dialog sequence, locking controls. | 1 | `{ . . . }` |
| [`jack_max2`](./NPC_Scripts.md#object-jack_max2) | Object  | A sequence that plays Jack's second max favor dialog sequence, locking controls. | 1 | `{ . . . }` |
| [`jack_max3`](./NPC_Scripts.md#object-jack_max3) | Object  | A sequence that plays Jack's third max favor dialog sequence, locking controls. | 1 | `{ . . . }` |
| [`jack_max4`](./NPC_Scripts.md#object-jack_max4) | Object  | A sequence that plays Jack's fourth max favor dialog sequence, locking controls. | 1 | `{ . . . }` |
| [`jack_max5`](./NPC_Scripts.md#object-jack_max5) | Object  | A sequence that plays Jack's fifth max favor dialog sequence, locking controls. | 1 | `{ . . . }` |
| [`jack_zara`](./NPC_Scripts.md#object-jack_zara) | Object  | A sequence that plays Jack's dialog about Zara, locking controls. | 1 | `{ . . . }` |
| [`level_up_didnt_select_sunburn`](./NPC_Scripts.md#object-level_up_didnt_select_sunburn) | Object  | A sequence that plays dialog when the player did not select the Sunburn level-up option. | 1 | `{ . . . }` |
| [`level_up_intro`](./NPC_Scripts.md#object-level_up_intro) | Object  | A sequence that plays the introductory dialog and animation for the level-up UI. | 1 | `{ . . . }` |
| [`level_up_selected_sunburn`](./NPC_Scripts.md#object-level_up_selected_sunburn) | Object  | A sequence that plays dialog when the player selected the Sunburn level-up option. | 1 | `{ . . . }` |
| [`low_on_food`](./NPC_Scripts.md#object-low_on_food) | Object  | A sequence that plays a dialog and animation warning the player that they are low on food. | 1 | `{ . . . }` |
| [`map_click_node`](./NPC_Scripts.md#object-map_click_node) | Object  | A sequence that teaches the player to click a map node, then unlocks controls. | 1 | `{ . . . }` |
| [`map_equip_items`](./NPC_Scripts.md#object-map_equip_items) | Object  | A sequence that teaches the player to equip items on the map. | 1 | `{ . . . }` |
| [`map_equip_items2`](./NPC_Scripts.md#object-map_equip_items2) | Object  | A sequence that provides a secondary reminder to equip items, clearing its own token. | 1 | `{ . . . }` |
| [`melee_attack_rat`](./NPC_Scripts.md#object-melee_attack_rat) | Object  | A tutorial sequence that demonstrates how to perform a melee attack on a rat. | 1 | `{ . . . }` |
| [`melee_cat_spit`](./NPC_Scripts.md#object-melee_cat_spit) | Object  | A tutorial sequence that demonstrates how to use the cat spit ability. | 1 | `{ . . . }` |
| [`melee_cat_spit_fail_ally`](./NPC_Scripts.md#object-melee_cat_spit_fail_ally) | Object  | A tutorial sequence that plays when the cat spit fails due to targeting an ally. | 1 | `{ . . . }` |
| [`melee_cat_spit_fail_miss`](./NPC_Scripts.md#object-melee_cat_spit_fail_miss) | Object  | A tutorial sequence that plays when the cat spit fails due to a miss. | 1 | `{ . . . }` |
| [`melee_cat_spit_fail_rat`](./NPC_Scripts.md#object-melee_cat_spit_fail_rat) | Object  | A tutorial sequence that plays when the cat spit fails to hit a rat. | 1 | `{ . . . }` |
| [`melee_cat_spit_ignore`](./NPC_Scripts.md#object-melee_cat_spit_ignore) | Object  | A tutorial sequence that plays when the player ignores the cat spit prompt. | 1 | `{ . . . }` |
| [`melee_cat_spit_success`](./NPC_Scripts.md#object-melee_cat_spit_success) | Object  | A tutorial sequence that plays when the cat spit is successfully used. | 1 | `{ . . . }` |
| [`melee_killed_rat`](./NPC_Scripts.md#object-melee_killed_rat) | Object  | A tutorial sequence that plays after the player kills a rat with a melee attack. | 1 | `{ . . . }` |
| [`melee_move2`](./NPC_Scripts.md#object-melee_move2) | Object  | A tutorial sequence that teaches the player to use movement actions. | 1 | `{ . . . }` |
| [`melee_out_of_actions`](./NPC_Scripts.md#object-melee_out_of_actions) | Object  | A tutorial sequence that explains when the player is out of actions in melee. | 1 | `{ . . . }` |
| [`new_adventure`](./NPC_Scripts.md#object-new_adventure) | Object  | A sequence that plays dialog and animation when starting a new adventure. | 1 | `{ . . . }` |
| [`organ_intro`](./NPC_Scripts.md#object-organ_intro) | Object  | Sequence of events for the Organ Grinder's introductory dialogue. | 1 | `{ . . . }` |
| [`organ_max1`](./NPC_Scripts.md#object-organ_max1) | Object  | Sequence of events for the Organ Grinder's first max favor dialogue. | 1 | `{ . . . }` |
| [`organ_max2`](./NPC_Scripts.md#object-organ_max2) | Object  | Sequence of events for the Organ Grinder's second max favor dialogue. | 1 | `{ . . . }` |
| [`organ_max3`](./NPC_Scripts.md#object-organ_max3) | Object  | Sequence of events for the Organ Grinder's third max favor dialogue. | 1 | `{ . . . }` |
| [`organ_max4`](./NPC_Scripts.md#object-organ_max4) | Object  | Sequence of events for the Organ Grinder's fourth max favor dialogue. | 1 | `{ . . . }` |
| [`organ_max5`](./NPC_Scripts.md#object-organ_max5) | Object  | Sequence of events for the Organ Grinder's fifth max favor dialogue. | 1 | `{ . . . }` |
| [`organ_rename`](./NPC_Scripts.md#object-organ_rename) | Object  | Sequence of events for the Organ Grinder's rename dialogue. | 1 | `{ . . . }` |
| [`organ_tina3`](./NPC_Scripts.md#object-organ_tina3) | Object  | Sequence of events for the Organ Grinder's dialogue with Tina (stage 3). | 1 | `{ . . . }` |
| [`purchase_item_a`](./NPC_Scripts.md#object-purchase_item_a) | Object  | Sequence of events for purchasing shop item A from Tracy. | 1 | `{ . . . }` |
| [`purchase_item_b`](./NPC_Scripts.md#object-purchase_item_b) | Object  | Sequence of events for purchasing shop item B from Tracy. | 1 | `{ . . . }` |
| [`purchase_item_c`](./NPC_Scripts.md#object-purchase_item_c) | Object  | Sequence of events for purchasing shop item C from Tracy. | 1 | `{ . . . }` |
| [`purchase_item_d`](./NPC_Scripts.md#object-purchase_item_d) | Object  | Sequence of events for purchasing shop item D from Tracy. | 1 | `{ . . . }` |
| [`purchase_item_iceage`](./NPC_Scripts.md#object-purchase_item_iceage) | Object  | Sequence of events for purchasing the Ice Age shop item. When set to true, indicates the purchase has already occurred. | 1 | `{ . . . }` |
| [`purchase_item_jurassic`](./NPC_Scripts.md#object-purchase_item_jurassic) | Object  | Sequence of events for purchasing the Jurassic shop item. When set to true, indicates the purchase has already occurred. | 1 | `{ . . . }` |
| [`purchase_item_moon`](./NPC_Scripts.md#object-purchase_item_moon) | Object  | Sequence of events for purchasing the Moon shop item. When set to true, indicates the purchase has already occurred. | 1 | `{ . . . }` |
| [`purchase_item_theend`](./NPC_Scripts.md#object-purchase_item_theend) | Object  | Sequence of events for purchasing The End shop item. When set to true, indicates the purchase has already occurred. | 1 | `{ . . . }` |
| [`ranged_attack_tomtom`](./NPC_Scripts.md#object-ranged_attack_tomtom) | Object  | Sequence of events for TomTom's ranged attack. | 1 | `{ . . . }` |
| [`ranged_attack_tomtom_fail_ally`](./NPC_Scripts.md#object-ranged_attack_tomtom_fail_ally) | Object  | Sequence of events for when TomTom's ranged attack fails due to an ally in the way. | 1 | `{ . . . }` |
| [`ranged_attack_tomtom_fail_miss`](./NPC_Scripts.md#object-ranged_attack_tomtom_fail_miss) | Object  | Sequence of events for when TomTom's ranged attack misses. | 1 | `{ . . . }` |
| [`ranged_attack_tomtom_fail_rat`](./NPC_Scripts.md#object-ranged_attack_tomtom_fail_rat) | Object  | Sequence of events for when TomTom's ranged attack fails due to a rat. | 1 | `{ . . . }` |
| [`ranged_cat_attack`](./NPC_Scripts.md#object-ranged_cat_attack) | Object  | Sequence of events for the cat's ranged attack. | 1 | `{ . . . }` |
| [`ranged_cat_early_attack2_ally`](./NPC_Scripts.md#object-ranged_cat_early_attack2_ally) | Object  | Sequence of events for the cat's second early ranged attack failing due to an ally. | 1 | `{ . . . }` |
| [`ranged_cat_early_attack2_miss`](./NPC_Scripts.md#object-ranged_cat_early_attack2_miss) | Object  | Sequence of events for the cat's second early ranged attack missing. | 1 | `{ . . . }` |
| [`ranged_cat_early_attack2_rat`](./NPC_Scripts.md#object-ranged_cat_early_attack2_rat) | Object  | Sequence of events for the cat's second early ranged attack failing due to a rat. | 1 | `{ . . . }` |
| [`ranged_cat_early_attack_ally`](./NPC_Scripts.md#object-ranged_cat_early_attack_ally) | Object  | Sequence of events for the cat's first early ranged attack failing due to an ally. | 1 | `{ . . . }` |
| [`ranged_cat_early_attack_miss`](./NPC_Scripts.md#object-ranged_cat_early_attack_miss) | Object  | Sequence of events for the cat's first early ranged attack missing. | 1 | `{ . . . }` |
| [`ranged_cat_early_attack_rat`](./NPC_Scripts.md#object-ranged_cat_early_attack_rat) | Object  | Sequence of events for the cat's first early ranged attack failing due to a rat. | 1 | `{ . . . }` |
| [`ranged_cat_failmove`](./NPC_Scripts.md#object-ranged_cat_failmove) | Object  | Sequence of events for the cat's failed ranged attack move. | 1 | `{ . . . }` |
| [`ranged_cat_intro`](./NPC_Scripts.md#object-ranged_cat_intro) | Object  | Sequence of events for the cat's ranged attack introduction. | 1 | `{ . . . }` |
| [`ranged_cat_roll`](./NPC_Scripts.md#object-ranged_cat_roll) | Object  | Sequence of events for the cat's ranged attack roll animation. | 1 | `{ . . . }` |
| [`ranged_cat_rolled_first`](./NPC_Scripts.md#object-ranged_cat_rolled_first) | Object  | Sequence of events for when the cat rolls first. | 1 | `{ . . . }` |
| [`steven_100`](./NPC_Scripts.md#object-steven_100) | Object  | Sequence of events for Steven's 100% completion dialogue. | 1 | `{ . . . }` |
| [`steven_introduction`](./NPC_Scripts.md#object-steven_introduction) | Object  | Sequence of events for Steven's introduction dialogue. | 1 | `{ . . . }` |
| [`steven_resummon`](./NPC_Scripts.md#object-steven_resummon) | Object  | A sequence triggered after beating the final boss, unlocking the ability to resummon house bosses. | 1 | `{ . . . }` |
| [`steven_savescum_1`](./NPC_Scripts.md#object-steven_savescum_1) | Object  | A sequence that plays a random warning sequence for the first savescum event. | 1 | `{ . . . }` |
| [`steven_savescum_100`](./NPC_Scripts.md#object-steven_savescum_100) | Object  | A secret sequence for the 100th savescum event. | 1 | `{ . . . }` |
| [`steven_savescum_1alt1`](./NPC_Scripts.md#object-steven_savescum_1alt1) | Object  | One of the random alternative warning sequences for the first savescum event. | 1 | `{ . . . }` |
| [`steven_savescum_1alt2`](./NPC_Scripts.md#object-steven_savescum_1alt2) | Object  | One of the random alternative warning sequences for the first savescum event. | 1 | `{ . . . }` |
| [`steven_savescum_1alt3`](./NPC_Scripts.md#object-steven_savescum_1alt3) | Object  | One of the random alternative warning sequences for the first savescum event. | 1 | `{ . . . }` |
| [`steven_savescum_2`](./NPC_Scripts.md#object-steven_savescum_2) | Object  | A sequence that plays a random sequence for the second savescum event (1 cat deja vu 10%). | 1 | `{ . . . }` |
| [`steven_savescum_2alt1`](./NPC_Scripts.md#object-steven_savescum_2alt1) | Object  | One of the random alternative sequences for the second savescum event (1 cat deja vu 10%). | 1 | `{ . . . }` |
| [`steven_savescum_2alt2`](./NPC_Scripts.md#object-steven_savescum_2alt2) | Object  | One of the random alternative sequences for the second savescum event (1 cat deja vu 10%). | 1 | `{ . . . }` |
| [`steven_savescum_2alt3`](./NPC_Scripts.md#object-steven_savescum_2alt3) | Object  | One of the random alternative sequences for the second savescum event (1 cat deja vu 10%). | 1 | `{ . . . }` |
| [`steven_savescum_3`](./NPC_Scripts.md#object-steven_savescum_3) | Object  | A sequence that plays a random sequence for the third savescum event (all cats deja vu 10%). | 1 | `{ . . . }` |
| [`steven_savescum_3alt1`](./NPC_Scripts.md#object-steven_savescum_3alt1) | Object  | One of the random alternative sequences for the third savescum event (all cats deja vu 10%). | 1 | `{ . . . }` |
| [`steven_savescum_3alt2`](./NPC_Scripts.md#object-steven_savescum_3alt2) | Object  | One of the random alternative sequences for the third savescum event (all cats deja vu 10%). | 1 | `{ . . . }` |
| [`steven_savescum_3alt3`](./NPC_Scripts.md#object-steven_savescum_3alt3) | Object  | One of the random alternative sequences for the third savescum event (all cats deja vu 10%). | 1 | `{ . . . }` |
| [`steven_savescum_4`](./NPC_Scripts.md#object-steven_savescum_4) | Object  | A sequence that plays a random sequence for the fourth savescum event (deja vu level up 25%). | 1 | `{ . . . }` |
| [`steven_savescum_4alt1`](./NPC_Scripts.md#object-steven_savescum_4alt1) | Object  | One of the random alternative sequences for the fourth savescum event (deja vu level up 25%, steven takes over). | 1 | `{ . . . }` |
| [`steven_savescum_4alt2`](./NPC_Scripts.md#object-steven_savescum_4alt2) | Object  | One of the random alternative sequences for the fourth savescum event (deja vu level up 25%, steven takes over). | 1 | `{ . . . }` |
| [`steven_savescum_4alt3`](./NPC_Scripts.md#object-steven_savescum_4alt3) | Object  | One of the random alternative sequences for the fourth savescum event (deja vu level up 25%, steven takes over). | 1 | `{ . . . }` |
| [`steven_savescum_houseboss_1`](./NPC_Scripts.md#object-steven_savescum_houseboss_1) | Object  | A warning sequence for the first house boss savescum event. | 1 | `{ . . . }` |
| [`steven_savescum_houseboss_100`](./NPC_Scripts.md#object-steven_savescum_houseboss_100) | Object  | A secret sequence for the 100th house boss savescum event. | 1 | `{ . . . }` |
| [`steven_savescum_houseboss_2`](./NPC_Scripts.md#object-steven_savescum_houseboss_2) | Object  | A sequence for the second house boss savescum event (all cats 10% deja vu). | 1 | `{ . . . }` |
| [`steven_savescum_houseboss_3`](./NPC_Scripts.md#object-steven_savescum_houseboss_3) | Object  | A sequence for the third house boss savescum event (all cats deja vu 25% and onward). | 1 | `{ . . . }` |
| [`steven_savescum_intro`](./NPC_Scripts.md#object-steven_savescum_intro) | Object  | A sequence that replaces the first savescum event sequences if it is the first time savescumming. | 1 | `{ . . . }` |
| [`steven_savescum_intro_houseboss`](./NPC_Scripts.md#object-steven_savescum_intro_houseboss) | Object  | A sequence that replaces the first house boss savescum event sequences if it is the first time savescumming. | 1 | `{ . . . }` |
| [`steven_unlock_act1_crazy`](./NPC_Scripts.md#object-steven_unlock_act1_crazy) | Object  | A sequence triggered when beating Act 1 and its house bosses on Hard, unlocking Crazy difficulty. | 1 | `{ . . . }` |
| [`steven_unlock_act1_impossible`](./NPC_Scripts.md#object-steven_unlock_act1_impossible) | Object  | A sequence triggered when beating Act 1 house bosses on Crazy, unlocking Impossible difficulty. | 1 | `{ . . . }` |
| [`steven_unlock_act2_crazy`](./NPC_Scripts.md#object-steven_unlock_act2_crazy) | Object  | A sequence for unlocking Act 2 Crazy difficulty. | 1 | `{ . . . }` |
| [`steven_unlock_act2_hard`](./NPC_Scripts.md#object-steven_unlock_act2_hard) | Object  | A sequence triggered when beating Act 2 for the first time, unlocking Hard difficulty. | 1 | `{ . . . }` |
| [`steven_unlock_act2_impossible`](./NPC_Scripts.md#object-steven_unlock_act2_impossible) | Object  | A sequence for unlocking Act 2 Impossible difficulty. | 1 | `{ . . . }` |
| [`steven_unlock_act3_crazy`](./NPC_Scripts.md#object-steven_unlock_act3_crazy) | Object  | A sequence for unlocking Act 3 Crazy difficulty. | 1 | `{ . . . }` |
| [`steven_unlock_act3_hard`](./NPC_Scripts.md#object-steven_unlock_act3_hard) | Object  | A sequence triggered when beating Act 3 for the first time, unlocking Hard difficulty. | 1 | `{ . . . }` |
| [`steven_unlock_act3_impossible`](./NPC_Scripts.md#object-steven_unlock_act3_impossible) | Object  | A sequence for unlocking Act 3 Impossible difficulty. | 1 | `{ . . . }` |
| [`take_cats_inside`](./NPC_Scripts.md#object-take_cats_inside) | Object  | A sequence for taking cats inside the house. | 1 | `{ . . . }` |
| [`test_gamepad_prompts`](./NPC_Scripts.md#object-test_gamepad_prompts) | Object  | A sequence that shows gamepad binding prompts. | 1 | `{ . . . }` |
| [`tink_begin_accepting_cats`](./NPC_Scripts.md#object-tink_begin_accepting_cats) | Object  | A sequence for when Tink begins accepting cats. | 1 | `{ . . . }` |
| [`tink_max1`](./NPC_Scripts.md#object-tink_max1) | Object  | One of the sequences played when Tink is at max favor (1 of 10). | 1 | `{ . . . }` |
| [`tink_max10`](./NPC_Scripts.md#object-tink_max10) | Object  | One of the sequences played when Tink is at max favor (10 of 10). | 1 | `{ . . . }` |
| [`tink_max2`](./NPC_Scripts.md#object-tink_max2) | Object  | One of the sequences played when Tink is at max favor (2 of 10). | 1 | `{ . . . }` |
| [`tink_max3`](./NPC_Scripts.md#object-tink_max3) | Object  | One of the sequences played when Tink is at max favor (3 of 10). | 1 | `{ . . . }` |
| [`tink_max4`](./NPC_Scripts.md#object-tink_max4) | Object  | One of the sequences played when Tink is at max favor (4 of 10). | 1 | `{ . . . }` |
| [`tink_max5`](./NPC_Scripts.md#object-tink_max5) | Object  | One of the sequences played when Tink is at max favor (5 of 10). | 1 | `{ . . . }` |
| [`tink_max6`](./NPC_Scripts.md#object-tink_max6) | Object  | One of the sequences played when Tink is at max favor (6 of 10). | 1 | `{ . . . }` |
| [`tink_max7`](./NPC_Scripts.md#object-tink_max7) | Object  | One of the sequences played when Tink is at max favor (7 of 10). | 1 | `{ . . . }` |
| [`tink_max8`](./NPC_Scripts.md#object-tink_max8) | Object  | One of the sequences played when Tink is at max favor (8 of 10). | 1 | `{ . . . }` |
| [`tink_max9`](./NPC_Scripts.md#object-tink_max9) | Object  | One of the sequences played when Tink is at max favor (9 of 10). | 1 | `{ . . . }` |
| [`tink_terminator`](./NPC_Scripts.md#object-tink_terminator) | Object  | A sequence for Tink's terminator event. | 1 | `{ . . . }` |
| [`tink_tina2`](./NPC_Scripts.md#object-tink_tina2) | Object  | A sequence for Tink and Tina interaction 2. | 1 | `{ . . . }` |
| [`tink_tips_appeal`](./NPC_Scripts.md#object-tink_tips_appeal) | Object  | A sequence for Tink's tips on appeal. | 1 | `{ . . . }` |
| [`tink_tips_basestats`](./NPC_Scripts.md#object-tink_tips_basestats) | Object  | A sequence for Tink's tips on base stats. | 1 | `{ . . . }` |
| [`tink_tips_cleaning`](./NPC_Scripts.md#object-tink_tips_cleaning) | Object  | A sequence for Tink's tips on cleaning. | 1 | `{ . . . }` |
| [`tink_tips_comfort`](./NPC_Scripts.md#object-tink_tips_comfort) | Object  | A sequence of dialogs providing Tink's tips on cat comfort. | 1 | `{ . . . }` |
| [`tink_tips_health`](./NPC_Scripts.md#object-tink_tips_health) | Object  | A sequence of dialogs providing Tink's tips on cat health. | 1 | `{ . . . }` |
| [`tink_tips_inbreeding`](./NPC_Scripts.md#object-tink_tips_inbreeding) | Object  | A sequence of dialogs providing Tink's tips on inbreeding. | 1 | `{ . . . }` |
| [`tink_tips_intro`](./NPC_Scripts.md#object-tink_tips_intro) | Object  | A sequence of dialogs introducing Tink's tips, then playing the comfort tips sequence. | 1 | `{ . . . }` |
| [`tink_tips_multiclassing`](./NPC_Scripts.md#object-tink_tips_multiclassing) | Object  | A sequence of dialogs providing Tink's tips on multiclassing. | 1 | `{ . . . }` |
| [`tink_tips_mutation`](./NPC_Scripts.md#object-tink_tips_mutation) | Object  | A sequence of dialogs providing Tink's tips on mutations. | 1 | `{ . . . }` |
| [`tink_tips_stimulation`](./NPC_Scripts.md#object-tink_tips_stimulation) | Object  | A sequence of dialogs providing Tink's tips on stimulation. | 1 | `{ . . . }` |
| [`tracy_foodbonus1`](./NPC_Scripts.md#object-tracy_foodbonus1) | Object  | A sequence showing Tracy explaining a food bonus reward. | 1 | `{ . . . }` |
| [`tracy_introduction`](./NPC_Scripts.md#object-tracy_introduction) | Object  | A sequence introducing Tracy to the player. | 1 | `{ . . . }` |
| [`tracy_kaijufight`](./NPC_Scripts.md#object-tracy_kaijufight) | Object  | A sequence where Tracy discusses a kaiju fight. | 1 | `{ . . . }` |
| [`tracy_max1`](./NPC_Scripts.md#object-tracy_max1) | Object  | A sequence for Tracy at max favor (part 1). | 1 | `{ . . . }` |
| [`tracy_max2`](./NPC_Scripts.md#object-tracy_max2) | Object  | A sequence for Tracy at max favor (part 2). | 1 | `{ . . . }` |
| [`tracy_max3`](./NPC_Scripts.md#object-tracy_max3) | Object  | A sequence for Tracy at max favor (part 3). | 1 | `{ . . . }` |
| [`tracy_max4`](./NPC_Scripts.md#object-tracy_max4) | Object  | A sequence for Tracy at max favor (part 4). | 1 | `{ . . . }` |
| [`tracy_max5`](./NPC_Scripts.md#object-tracy_max5) | Object  | A sequence for Tracy at max favor (part 5). | 1 | `{ . . . }` |
| [`try_again_attack_rat`](./NPC_Scripts.md#object-try_again_attack_rat) | Object  | A tutorial sequence prompting the player to try attacking the rat again. | 1 | `{ . . . }` |
| [`try_again_melee_move`](./NPC_Scripts.md#object-try_again_melee_move) | Object  | A tutorial sequence prompting the player to try a melee move again. | 1 | `{ . . . }` |
| [`tutorial_cat_dies`](./NPC_Scripts.md#object-tutorial_cat_dies) | Object  | A tutorial sequence explaining what happens when a cat dies. | 1 | `{ . . . }` |
| [`unprompted1`](./NPC_Scripts.md#object-unprompted1) | Object  | An unprompted dialogue sequence from Beanies (part 1). | 1 | `{ . . . }` |
| [`unprompted2`](./NPC_Scripts.md#object-unprompted2) | Object  | An unprompted dialogue sequence from Beanies (part 2). | 1 | `{ . . . }` |
| [`unprompted3`](./NPC_Scripts.md#object-unprompted3) | Object  | An unprompted dialogue sequence from Beanies (part 3). | 1 | `{ . . . }` |
| [`unprompted4`](./NPC_Scripts.md#object-unprompted4) | Object  | An unprompted dialogue sequence from Beanies (part 4). | 1 | `{ . . . }` |
| [`unprompted5`](./NPC_Scripts.md#object-unprompted5) | Object  | An unprompted dialogue sequence from Beanies (part 5). | 1 | `{ . . . }` |
| [`unprompted6`](./NPC_Scripts.md#object-unprompted6) | Object  | An unprompted dialogue sequence from Beanies (part 6). | 1 | `{ . . . }` |
| [`upgrade_storage_max1`](./NPC_Scripts.md#object-upgrade_storage_max1) | Object  | A dialogue popup for the first storage space upgrade. | 1 | `{ . . . }` |
| [`upgrade_storage_max2`](./NPC_Scripts.md#object-upgrade_storage_max2) | Object  | A dialogue popup for the second storage space upgrade, including a reward. | 1 | `{ . . . }` |
| [`upgrade_storage_max3`](./NPC_Scripts.md#object-upgrade_storage_max3) | Object  | A dialogue popup for the third storage space upgrade. | 1 | `{ . . . }` |
| [`upgrade_storage_max4`](./NPC_Scripts.md#object-upgrade_storage_max4) | Object  | A dialogue popup for the fourth storage space upgrade. | 1 | `{ . . . }` |
| [`upgrade_storage_max5`](./NPC_Scripts.md#object-upgrade_storage_max5) | Object  | A dialogue popup for the fifth storage space upgrade. | 1 | `{ . . . }` |
| [`use_attack_after_used_weapon`](./NPC_Scripts.md#object-use_attack_after_used_weapon) | Object  | A tutorial sequence teaching the player to use an attack after using a weapon. | 1 | `{ . . . }` |
| [`use_weapon`](./NPC_Scripts.md#object-use_weapon) | Object  | Defines a dialogue option that prompts the unit to use their equipped weapon. | 1 | `{ . . . }` |
| [`welcome`](./NPC_Scripts.md#object-welcome) | Object  | A cancelable welcome sequence for Tracy's shop. | 1 | `{ . . . }` |
| [`welcome_boneyard`](./NPC_Scripts.md#object-welcome_boneyard) | Object  | A cancelable welcome sequence for the boneyard biome shop. | 1 | `{ . . . }` |
| [`welcome_bunker`](./NPC_Scripts.md#object-welcome_bunker) | Object  | A cancelable welcome sequence for the bunker biome shop. | 1 | `{ . . . }` |
| [`welcome_caves`](./NPC_Scripts.md#object-welcome_caves) | Object  | A cancelable welcome sequence for the caves biome shop. | 1 | `{ . . . }` |
| [`welcome_core`](./NPC_Scripts.md#object-welcome_core) | Object  | A cancelable welcome sequence for the core biome shop. | 1 | `{ . . . }` |
| [`welcome_crater`](./NPC_Scripts.md#object-welcome_crater) | Object  | A cancelable welcome sequence for the crater biome shop. | 1 | `{ . . . }` |
| [`welcome_desert`](./NPC_Scripts.md#object-welcome_desert) | Object  | A cancelable welcome sequence for the desert biome shop. | 1 | `{ . . . }` |
| [`welcome_future`](./NPC_Scripts.md#object-welcome_future) | Object  | A cancelable welcome sequence for the future biome shop. | 1 | `{ . . . }` |
| [`welcome_iceage`](./NPC_Scripts.md#object-welcome_iceage) | Object  | A cancelable welcome sequence for the ice age biome shop. | 1 | `{ . . . }` |
| [`welcome_junkyard`](./NPC_Scripts.md#object-welcome_junkyard) | Object  | A cancelable welcome sequence for the junkyard biome shop. | 1 | `{ . . . }` |
| [`welcome_jurassic`](./NPC_Scripts.md#object-welcome_jurassic) | Object  | A cancelable welcome sequence for the jurassic biome shop. | 1 | `{ . . . }` |
| [`welcome_lab`](./NPC_Scripts.md#object-welcome_lab) | Object  | A cancelable welcome sequence for the lab biome shop. | 1 | `{ . . . }` |
| [`welcome_moon`](./NPC_Scripts.md#object-welcome_moon) | Object  | A cancelable welcome sequence for the moon biome shop. | 1 | `{ . . . }` |
| [`welcome_sewers`](./NPC_Scripts.md#object-welcome_sewers) | Object  | A cancelable welcome sequence for the sewers biome shop. | 1 | `{ . . . }` |
| [`welcome_theend`](./NPC_Scripts.md#object-welcome_theend) | Object  | A cancelable welcome sequence for the theend biome shop, with Beanies' voice. | 1 | `{ . . . }` |
| [`welcome_water`](./NPC_Scripts.md#object-welcome_water) | Object  | Defines a cancelable sequence with a 0.5-second delay, auto-passing dialog NPC_TRACY_SHOP_WELCOME_WATER_1. | 1 | `{ . . . }` |
| [`welcome_water_cheap`](./NPC_Scripts.md#object-welcome_water_cheap) | Object  | Defines a cancelable sequence with a 0.5-second delay, auto-passing dialog NPC_TRACY_SHOP_WELCOME_WATER_CHEAP_1. | 1 | `{ . . . }` |

</details>


---


### Object: `states`


**Definition:** Defines named animation states and their associated animation clips.
**Total Count:** 12

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `idle` | Array | List of animation states used for the idle state. | 10 | `["idle" "blocking" "gone"]`<br>`["idle" "blocking"]`<br>`["idle"]` |
| `closeup` | Array | List of animation states used for the closeup camera view. | 3 | `["closeup"]` |
| `verycloseup` | Array | List of animation states used for the very closeup camera view. | 3 | `["verycloseup"]` |
| `zoomedout` | Array | List of animation states used for the zoomed out camera view. | 3 | `["zoomedout"]` |
| `beanies_intensestatic` | Array | List of animation states for Beanie's intense static effect. | 1 | `["beanies_intensestatic"]` |
| `beanies_right` | Array | List of animation states for Beanie's right-facing pose. | 1 | `["beanies_right"]` |
| `butch_left` | Array | List of animation states for Butch's left-facing pose and associated pointing gestures. | 1 ||
| `butch_right` | Array | List of animation states for Butch's right-facing pose and associated pointing gestures. | 1 ||
| `choosecats` | Array | List of animation states for the cat selection screen. | 1 | `["choosecats"]` |
| `closerup` | Array | List of animation states for an even closer camera view. | 1 | `["closerup"]` |
| `frank_right` | Array | List of animation states for Frank's right-facing pose and pipe point. | 1 | `["frank_right", "frank_point_pipe"]` |
| `jack_right` | Array | List of animation states for Jack's right-facing pose and furniture point. | 1 | `["jack_right", "jack_point_furniture"]` |
| `offscreen` | Array | List of animation states for when the character is off screen. | 1 | `["offscreen"]` |
| `steven_center` | Array | List of animation states for Steven's center position and cat animation. | 1 | `["steven_center", "steven_cat"]` |
| `tink_left` | Array | List of animation states for Tink's left-facing pose and associated pointing gestures. | 1 ||
| `tink_right` | Array | List of animation states for Tink's right-facing pose and stray point. | 1 | `["tink_right", "tink_point_strays"]` |

</details>


---


### Object: `transitions`


**Definition:** Defines named transitions between animation states.
**Total Count:** 12

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `beanies_intensestatic_to_offscreen` | Array | A transition array that moves Beanie from the intensestatic state to offscreen. | 1 | `[beanies_intensestatic offscreen]` |
| `beanies_offscreen_to_intensestatic` | Array | A transition array that moves Beanie from offscreen to the intensestatic state. | 1 | `[offscreen beanies_intensestatic]` |
| `beanies_offscreen_to_right` | Array | A transition array that moves Beanie from offscreen to the right position. | 1 | `[offscreen beanies_right]` |
| `beanies_right_to_offscreen` | Array | A transition array that moves Beanie from the right position to offscreen. | 1 | `[beanies_right offscreen]` |
| `butch_left_to_offscreen` | Array | A transition array that moves Butch from the left position to offscreen. | 1 | `[butch_left offscreen]` |
| `butch_left_to_right` | Array | A transition array that moves Butch from the left position to the right position. | 1 | `[butch_left butch_right]` |
| `butch_offscreen_to_left` | Array | A transition array that moves Butch from offscreen to the left position. | 1 | `[offscreen butch_left]` |
| `butch_offscreen_to_right` | Array | A transition array that moves Butch from offscreen to the right position. | 1 | `[offscreen butch_right]` |
| `butch_right_to_left` | Array | A transition array that moves Butch from the right position to the left position. | 1 | `[butch_right butch_left]` |
| `butch_right_to_offscreen` | Array | A transition array that moves Butch from the right position to offscreen. | 1 | `[butch_right offscreen]` |
| `frank_offscreen_to_right` | Array | A transition array that moves Frank from offscreen to the right position. | 1 | `[offscreen frank_right]` |
| `frank_right_to_offscreen` | Array | A transition array that moves Frank from the right position to offscreen. | 1 | `[frank_right offscreen]` |
| `jack_offscreen_to_right` | Array | A transition array that moves Jack from offscreen to the right position. | 1 | `[offscreen jack_right]` |
| `jack_right_to_offscreen` | Array | A transition array that moves Jack from the right position to offscreen. | 1 | `[jack_right offscreen]` |
| `steven_center_to_offscreen` | Array | A transition array that moves Steven from the center position to offscreen. | 1 | `[steven_center offscreen]` |
| `steven_offscreen_to_center` | Array | A transition array that moves Steven from offscreen to the center position. | 1 | `[offscreen steven_center]` |
| `tink_left_to_offscreen` | Array | A transition array that moves Tink from the left position to offscreen. | 1 | `[tink_left offscreen]` |
| `tink_left_to_right` | Array | A transition array that moves Tink from the left position to the right position. | 1 | `[tink_left tink_right]` |
| `tink_offscreen_to_left` | Array | A transition array that moves Tink from offscreen to the left position. | 1 | `[offscreen tink_left]` |
| `tink_offscreen_to_right` | Array | A transition array that moves Tink from offscreen to the right position. | 1 | `[offscreen tink_right]` |
| `tink_right_to_left` | Array | A transition array that moves Tink from the right position to the left position. | 1 | `[tink_right tink_left]` |
| `tink_right_to_offscreen` | Array | A transition array that moves Tink from the right position to offscreen. | 1 | `[tink_right offscreen]` |

</details>


---


### Object: `unprompted`


**Definition:** Defines sequences of unprompted dialog events.
**Total Count:** 9

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `do_random_sequence` | Array | An array of sequence names; one is chosen at random to execute. | 5 ||
| `cancelable` | Boolean | If true, the sequence can be cancelled by the player. | 3 | `true` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 3 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `wait_for_cancel` | Number | The number of frames to wait before the sequence is cancelled. | 3 | `1` |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 2 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `also`


**Definition:** Defines an additional dialog sequence that plays alongside the main one.
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 8 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `unknown`


**Definition:** A generic object container for dialog and rewards, often used for unprompted sequences.
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 8 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 8 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 3 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 3 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 3 | `1` |

</details>


---


### Object: `hide_text`


**Definition:** Defines a sequence that hides text dialogs and autopasses to the next step.
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | If true, the sequence can be cancelled by the player. | 4 | `true` |
| `dialog_and_autopass` | String | Specifies the dialog string to display, and automatically proceeds past it. | 4 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |

</details>


---


### Object: `purchase_item`


**Definition:** Defines the dialog sequence for purchasing an item from an NPC.
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | If true, the sequence can be cancelled by the player. | 3 | `true` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 3 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `wait_for_cancel` | Number | The number of frames to wait before the sequence is cancelled. | 3 | `1` |
| `do_random_sequence` | Array | An array of sequence names; one is chosen at random to execute. | 1 ||

</details>


---


### Object: `tooltip`


**Definition:** The localization string key used for the tooltip displayed on hover.
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | If true, the sequence can be cancelled by the player. | 4 | `true` |
| `tooltip_dialog` | Enum | Determines which tooltip dialog string to display, referenced by a unique NPC shop identifier. | 4 | `NPC_JACK_SHOP_TOOLTIP`<br>`NPC_ORGANGRINDER_SHOP_TOOLTIP`<br>`NPC_TRACY_SHOP_TOOLTIP` |
| `wait_for_cancel` | Number | The number of frames to wait before the sequence is cancelled. | 4 | `1` |

</details>


---


### Object: `unprompted_a`


**Definition:** Defines a dialog sequence that plays when the player approaches the NPC without a prompt, labeled as the first variant.
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 4 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `do_sequence` | Enum | Specifies the name of the sequence to execute. | 3 | `butch_tips_intelligence`<br>`forward_to_tips`<br>`tink_tips_comfort` |

</details>


---


### Object: `unprompted_b`


**Definition:** Defines a dialog sequence that plays when the player approaches the NPC without a prompt, labeled as the second variant.
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 4 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `do_sequence` | Enum | Specifies the name of the sequence to execute. | 3 | `butch_tips_intelligence`<br>`forward_to_tips`<br>`tink_tips_comfort` |

</details>


---


### Object: `unprompted_c`


**Definition:** Defines a dialog sequence that plays when the player approaches the NPC without a prompt, labeled as the third variant.
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 4 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `do_sequence` | Enum | Specifies the name of the sequence to execute. | 3 | `butch_tips_intelligence`<br>`forward_to_tips`<br>`tink_tips_comfort` |

</details>


---


### Object: `unprompted_d`


**Definition:** Defines a dialog sequence that plays when the player approaches the NPC without a prompt, labeled as the fourth variant.
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 4 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `do_sequence` | Enum | Specifies the name of the sequence to execute. | 3 | `butch_tips_intelligence`<br>`forward_to_tips`<br>`tink_tips_comfort` |

</details>


---


### Object: `unprompted_e`


**Definition:** Defines a dialog sequence that plays when the player approaches the NPC without a prompt, labeled as the fifth variant.
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 4 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `do_sequence` | Enum | Specifies the name of the sequence to execute. | 3 | `butch_tips_intelligence`<br>`forward_to_tips`<br>`tink_tips_comfort` |

</details>


---


### Object: `unprompted_f`


**Definition:** Defines a dialog sequence that plays when the player approaches the NPC without a prompt, labeled as the sixth variant.
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 4 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `do_sequence` | Enum | Specifies the name of the sequence to execute. | 3 | `butch_tips_intelligence`<br>`forward_to_tips`<br>`tink_tips_comfort` |

</details>


---


### Object: `unprompted_g`


**Definition:** Defines a dialog sequence that plays when the player approaches the NPC without a prompt, labeled as the seventh variant.
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 4 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `do_sequence` | Enum | Specifies the name of the sequence to execute. | 3 | `butch_tips_intelligence`<br>`forward_to_tips`<br>`tink_tips_comfort` |

</details>


---


### Object: `unprompted_h`


**Definition:** Defines a dialog sequence that plays when the player approaches the NPC without a prompt, labeled as the eighth variant.
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 4 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `do_sequence` | Enum | Specifies the name of the sequence to execute. | 3 | `butch_tips_intelligence`<br>`forward_to_tips`<br>`tink_tips_comfort` |

</details>


---


### Object: `unprompted_i`


**Definition:** Defines a dialog sequence that plays when the player approaches the NPC without a prompt, labeled as the ninth variant.
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 4 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `do_sequence` | Enum | Specifies the name of the sequence to execute. | 3 | `butch_tips_intelligence`<br>`forward_to_tips`<br>`tink_tips_comfort` |

</details>


---


### Object: `cant_afford`


**Definition:** Defines the dialog sequence that plays when the player attempts to purchase an item they cannot afford.
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | If true, the sequence can be cancelled by the player. | 2 | `true` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 2 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `wait_for_cancel` | Number | The number of frames to wait before the sequence is cancelled. | 2 | `1` |
| `do_random_sequence` | Array | An array of sequence names; one is chosen at random to execute. | 1 ||

</details>


---


### Object: `forward_to_tips`


**Definition:** Defines a dialog sequence that forwards the player to a random tip dialog for the current NPC.
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `do_random_sequence` | Array | An array of sequence names; one is chosen at random to execute. | 3 ||

</details>


---


### Object: `out_of_stock`


**Definition:** Defines the dialog sequence that plays when a shop item is out of stock.
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 3 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 3 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beanies_begin_accepting_cats`


**Definition:** A cutscene sequence where Beanies begins accepting cats, playing dialogue and adjusting camera states.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `begin_accepting_cats` | Enum | Specifies the character tag for the sequence that initiates accepting cats. | 1 | `beanies`<br>`butch`<br>`jack` |

</details>


---


### Object: `beanies_bombquest_2`


**Definition:** Defines the dialog sequence for Beanies' bomb quest step 2.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beanies_bombquest_3`


**Definition:** Defines the dialog sequence for the third stage of Beanies' bomb quest.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `trigger_unlock` | Enum | Specifies the quest or flag to unlock when this sequence completes. | 1 | `nuke_quest_get_nuke`<br>`nuke_quest_loop`<br>`quest_begin_amplifier2` |

</details>


---


### Object: `beanies_bombquest_amnesia`


**Definition:** Defines the dialog sequence for Dr. Beanies' amnesia after a successful nuke quest.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `trigger_unlock` | Enum | Specifies the quest or flag to unlock when this sequence completes. | 1 | `nuke_quest_get_nuke`<br>`nuke_quest_loop`<br>`quest_begin_amplifier2` |

</details>


---


### Object: `beanies_bombquest_begin`


**Definition:** Defines the dialog sequence for Dr. Beanies beginning the final bomb quest.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `trigger_unlock` | Enum | Specifies the quest or flag to unlock when this sequence completes. | 1 | `nuke_quest_get_nuke`<br>`nuke_quest_loop`<br>`quest_begin_amplifier2` |

</details>


---


### Object: `beanies_bombquest_fail_jarofblood`


**Definition:** Defines the dialog sequence for failing the bomb quest by losing or misusing the jar of blood.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `trigger_unlock` | Enum | Specifies the quest or flag to unlock when this sequence completes. | 1 | `nuke_quest_get_nuke`<br>`nuke_quest_loop`<br>`quest_begin_amplifier2` |

</details>


---


### Object: `beanies_bombquest_fail_jarofchaos`


**Definition:** Defines the dialog sequence for failing the bomb quest by losing or misusing the jar of chaos.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `trigger_unlock` | Enum | Specifies the quest or flag to unlock when this sequence completes. | 1 | `nuke_quest_get_nuke`<br>`nuke_quest_loop`<br>`quest_begin_amplifier2` |

</details>


---


### Object: `beanies_bombquest_fail_jarofradiation`


**Definition:** Defines the dialog sequence for failing the bomb quest during the Act 1 jar-of-radiation stage.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `trigger_unlock` | Enum | Specifies the quest or flag to unlock when this sequence completes. | 1 | `nuke_quest_get_nuke`<br>`nuke_quest_loop`<br>`quest_begin_amplifier2` |

</details>


---


### Object: `beanies_bombquest_fail_nuke`


**Definition:** Defines the dialog sequence for failing the bomb quest during the Act 3 nuke stage.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `trigger_unlock` | Enum | Specifies the quest or flag to unlock when this sequence completes. | 1 | `nuke_quest_get_nuke`<br>`nuke_quest_loop`<br>`quest_begin_amplifier2` |

</details>


---


### Object: `beanies_future_intro`


**Definition:** Defines the dialog sequence where Dr. Beanies sends the player to the future.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beanies_hitler3`


**Definition:** A cutscene sequence where Beanies reveals that Hitler has been sending robots back in time, introducing Hitler as the final boss.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beanies_hitler3_defeat`


**Definition:** A cutscene sequence where Beanies provides the final piece of tech to unlock the infinite after defeating Hitler.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `trigger_unlock` | Enum | Specifies the quest or flag to unlock when this sequence completes. | 1 | `nuke_quest_get_nuke`<br>`nuke_quest_loop`<br>`quest_begin_amplifier2` |

</details>


---


### Object: `beanies_iloveyou`


**Definition:** A cutscene sequence where Beanies expresses love to the player through dialogue.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `beanies_infinite_intro`


**Definition:** A cutscene sequence where Beanies unlocks the infinite and urges the player to challenge the creator.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |
| `delay` | Float | The delay in seconds before the ability's effect triggers. | 1 | `.05`<br>`.1`<br>`.25` |

</details>


---


### Object: `beanies_jurassic_intro`


**Definition:** Defines the dialog sequence for Dr. Beanies' introduction to the Jurassic area.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beanies_lab_intro`


**Definition:** Defines the dialog sequence where Dr. Beanies is homeless and credits roll.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `play_cutscene` | Enum | Specifies the name of the cutscene to play. | 1 | `credits_1` |
| `restart_npc_music` | Number | The number of times to restart the NPC's music track. | 1 | `1` |
| `trigger_unlock` | Enum | Specifies the quest or flag to unlock when this sequence completes. | 1 | `nuke_quest_get_nuke`<br>`nuke_quest_loop`<br>`quest_begin_amplifier2` |

</details>


---


### Object: `beanies_quest_complete`


**Definition:** A cutscene sequence that triggers upon successfully completing Beanies' side quest.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `do_sidequest_sequence` | Enum | Specifies the name of the sidequest sequence to run. | 1 | `beaniesquest_complete`<br>`beaniesquest_fail`<br>`beaniesquest_intro` |
| `gather_questitem_info` | Enum | Specifies the type of quest item information to gather (e.g., 'fail', 'success', 'newest'). | 1 | `fail`<br>`newest`<br>`success` |

</details>


---


### Object: `beanies_quest_fail`


**Definition:** A cutscene sequence that triggers upon failing Beanies' side quest.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `do_sidequest_sequence` | Enum | Specifies the name of the sidequest sequence to run. | 1 | `beaniesquest_complete`<br>`beaniesquest_fail`<br>`beaniesquest_intro` |
| `gather_questitem_info` | Enum | Specifies the type of quest item information to gather (e.g., 'fail', 'success', 'newest'). | 1 | `fail`<br>`newest`<br>`success` |

</details>


---


### Object: `beanies_quests_intro`


**Definition:** Defines the initial dialog or quest-generation sequence for Dr. Beanies' quests.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `do_sidequest_sequence` | Enum | Specifies the name of the sidequest sequence to run. | 1 | `beaniesquest_complete`<br>`beaniesquest_fail`<br>`beaniesquest_intro` |
| `gather_questitem_info` | Enum | Specifies the type of quest item information to gather (e.g., 'fail', 'success', 'newest'). | 1 | `fail`<br>`newest`<br>`success` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beanies_quests_repeat`


**Definition:** Defines the repeatable quest dialog or generator for Dr. Beanies.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `do_sidequest_sequence` | Enum | Specifies the name of the sidequest sequence to run. | 1 | `beaniesquest_complete`<br>`beaniesquest_fail`<br>`beaniesquest_intro` |
| `gather_questitem_info` | Enum | Specifies the type of quest item information to gather (e.g., 'fail', 'success', 'newest'). | 1 | `fail`<br>`newest`<br>`success` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beanies_rift_intro`


**Definition:** A cutscene sequence where Beanies comments on the chaos realm.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |
| `delay` | Float | The delay in seconds before the ability's effect triggers. | 1 | `.05`<br>`.1`<br>`.25` |

</details>


---


### Object: `beanies_screenshake_test`


**Definition:** A cutscene sequence with a dialog followed by a screen shake effect.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |
| `screenshake` | Array | [intensity, duration] in frames. Applies a screen shake effect. | 1 | `[.5, 10]`<br>`[1, 30]` |

</details>


---


### Object: `beanies_seefuture`


**Definition:** A cutscene sequence where Beanies reacts to the player seeing the future.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beanies_seetheend`


**Definition:** A cutscene sequence where Beanies responds to the player seeing the far future.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beanies_terminator1_defeat`


**Definition:** A cutscene sequence that plays when the first terminator is killed.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `trigger_unlock` | Enum | Specifies the quest or flag to unlock when this sequence completes. | 1 | `nuke_quest_get_nuke`<br>`nuke_quest_loop`<br>`quest_begin_amplifier2` |

</details>


---


### Object: `beanies_terminator2_defeat`


**Definition:** A cutscene sequence where Beanies invents more time-bending tech after the second terminator is defeated.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `trigger_unlock` | Enum | Specifies the quest or flag to unlock when this sequence completes. | 1 | `nuke_quest_get_nuke`<br>`nuke_quest_loop`<br>`quest_begin_amplifier2` |

</details>


---


### Object: `beanies_theend_intro`


**Definition:** Defines the dialog sequence where Dr. Beanies responds to you killing Hitler.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beanies_timemachine_2`


**Definition:** A cutscene sequence where a frustrated Beanies sends the player into the future to gather information.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beanies_timemachine_intro`


**Definition:** A cutscene sequence where Beanies explains how the time machine works and the butterfly effect.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `trigger_unlock` | Enum | Specifies the quest or flag to unlock when this sequence completes. | 1 | `nuke_quest_get_nuke`<br>`nuke_quest_loop`<br>`quest_begin_amplifier2` |

</details>


---


### Object: `beanies_vscreator1`


**Definition:** A cutscene sequence where Beanies tells the player to detonate the nuke against the creator.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |

</details>


---


### Object: `beanies_vscreator2`


**Definition:** A cutscene sequence where Beanies attempts to convince the player to detonate the nuke if they refuse.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |

</details>


---


### Object: `beanies_vscreator3`


**Definition:** A cutscene sequence where an angry Beanies continues to try to convince the player to end it.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |

</details>


---


### Object: `beanies_vscreator4`


**Definition:** A cutscene sequence where Beanies sets off the nuke himself after the player's refusal.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |
| `force_current_cat_use_ability` | Enum | Specifies the ability ID that the current cat is forced to use. | 1 | `neck_NukeBonus_remote` |

</details>


---


### Object: `beanies_vscreatorintro`


**Definition:** A cutscene sequence where Beanies explains how to end everything.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |

</details>


---


### Object: `beaniesquest_complete_AI`


**Definition:** A cutscene sequence that plays upon completing the AI-related portion of Beanies' quest.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_complete_AirHorn`


**Definition:** A cutscene sequence that plays upon completing the AirHorn-related portion of Beanies' quest.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_complete_AngryFace`


**Definition:** The completion dialogue sequence for the AngryFace sidequest, triggered when the quest is fulfilled.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_complete_AnimalHands`


**Definition:** The completion dialogue sequence for the AnimalHands sidequest, triggered when the quest is fulfilled.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_complete_BubbleBoy`


**Definition:** The completion dialogue sequence for the BubbleBoy sidequest, triggered when the quest is fulfilled.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_complete_ChadImplant`


**Definition:** The completion dialogue sequence for the ChadImplant sidequest, triggered when the quest is fulfilled.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_complete_ChaosDevice`


**Definition:** The completion dialogue sequence for the ChaosDevice sidequest, triggered when the quest is fulfilled.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_complete_DimensionalDivider`


**Definition:** The completion dialogue sequence for the DimensionalDivider sidequest, triggered when the quest is fulfilled.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_complete_DiseaseJar`


**Definition:** The completion dialogue sequence for the DiseaseJar sidequest, triggered when the quest is fulfilled.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_complete_ExperimentalTreatment`


**Definition:** The completion dialogue sequence for the ExperimentalTreatment sidequest, triggered when the quest is fulfilled.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_complete_FartFace`


**Definition:** The completion dialogue sequence for the FartFace sidequest, triggered when the quest is fulfilled.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_complete_FigLeaf`


**Definition:** The completion dialogue sequence for the FigLeaf sidequest, triggered when the quest is fulfilled.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_complete_Generic`


**Definition:** The completion dialogue sequence for a generic sidequest, triggered when the quest is fulfilled.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_complete_GlassCannon`


**Definition:** The completion dialogue sequence for the GlassCannon sidequest, triggered when the quest is fulfilled.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_complete_HardPill`


**Definition:** The completion dialogue sequence for the HardPill sidequest, triggered when the quest is fulfilled.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_complete_HiveMind`


**Definition:** The completion dialogue sequence for the HiveMind sidequest, triggered when the quest is fulfilled.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_complete_MagicMirror`


**Definition:** The completion dialogue sequence for the MagicMirror sidequest, triggered when the quest is fulfilled.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_complete_MeStone`


**Definition:** The completion dialogue sequence for the MeStone sidequest, triggered when the quest is fulfilled.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_complete_MultilinkCable`


**Definition:** The completion dialogue sequence for the MultilinkCable sidequest, triggered when the quest is fulfilled.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_complete_MysteriousDice`


**Definition:** The completion dialogue sequence for the MysteriousDice sidequest, triggered when the quest is fulfilled.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_complete_MysteriousGlasses`


**Definition:** The completion dialogue sequence for the MysteriousGlasses sidequest, triggered when the quest is fulfilled.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_complete_NDEDevice`


**Definition:** The completion dialogue sequence for the NDEDevice sidequest, triggered when the quest is fulfilled.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_complete_NuclearKnife`


**Definition:** The completion dialogue sequence for the NuclearKnife sidequest, triggered when the quest is fulfilled.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_complete_PartialLobotomy`


**Definition:** The completion dialogue sequence for the PartialLobotomy sidequest, triggered when the quest is fulfilled.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_complete_PartyDetonator`


**Definition:** The completion dialogue sequence for the PartyDetonator sidequest, triggered when the quest is fulfilled.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_complete_PersonalHeater`


**Definition:** The completion dialogue sequence for the PersonalHeater sidequest, triggered when the quest is fulfilled.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_complete_PersuasionDevice`


**Definition:** The completion dialogue sequence for the PersuasionDevice sidequest, triggered when the quest is fulfilled.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_complete_PrincessHat`


**Definition:** The completion dialogue sequence for the PrincessHat sidequest, triggered when the quest is fulfilled.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_complete_RealityScrambler`


**Definition:** The completion dialogue sequence for the RealityScrambler sidequest, triggered when the quest is fulfilled.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_complete_Redacted`


**Definition:** The completion dialogue sequence for the Redacted sidequest, triggered when the quest is fulfilled.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_complete_SpiderInjector`


**Definition:** The completion dialogue sequence for the SpiderInjector sidequest, triggered when the quest is fulfilled.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_complete_Stopwatch`


**Definition:** The completion dialogue sequence for the Stopwatch sidequest, triggered when the quest is fulfilled.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_complete_StorageLocker`


**Definition:** The completion dialogue sequence for the StorageLocker sidequest, triggered when the quest is fulfilled.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_complete_TheIOU`


**Definition:** The completion dialogue sequence for the TheIOU sidequest, triggered when the quest is fulfilled.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_complete_TheLoner`


**Definition:** The completion dialogue sequence for the TheLoner sidequest, triggered when the quest is fulfilled.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_complete_Trapfest99`


**Definition:** The completion dialogue sequence for the Trapfest99 sidequest, triggered when the quest is fulfilled.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_complete_UltraVision3000`


**Definition:** The completion dialogue sequence for the UltraVision3000 sidequest, triggered when the quest is fulfilled.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_fail_AI`


**Definition:** The failure dialogue sequence for the AI sidequest, triggered when the quest fails.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_fail_AirHorn`


**Definition:** The failure dialogue sequence for the AirHorn sidequest, triggered when the quest fails.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_fail_AngryFace`


**Definition:** The failure dialogue sequence for the AngryFace sidequest, triggered when the quest fails.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_fail_AnimalHands`


**Definition:** The failure dialogue sequence for the AnimalHands sidequest, triggered when the quest fails.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_fail_BubbleBoy`


**Definition:** The failure dialogue sequence for the BubbleBoy sidequest, triggered when the quest fails.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_fail_ChadImplant`


**Definition:** The failure dialogue sequence for the ChadImplant sidequest, triggered when the quest fails.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_fail_ChaosDevice`


**Definition:** The failure dialogue sequence for the ChaosDevice sidequest, triggered when the quest fails.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_fail_DimensionalDivider`


**Definition:** The failure dialogue sequence for the DimensionalDivider sidequest, triggered when the quest fails.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_fail_DiseaseJar`


**Definition:** The failure dialogue sequence for the DiseaseJar sidequest, triggered when the quest fails.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_fail_ExperimentalTreatment`


**Definition:** The failure dialogue sequence for the ExperimentalTreatment sidequest, triggered when the quest fails.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_fail_FartFace`


**Definition:** The failure dialogue sequence for the FartFace sidequest, triggered when the quest fails.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_fail_FigLeaf`


**Definition:** The failure dialogue sequence for the FigLeaf sidequest, triggered when the quest fails.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_fail_Generic`


**Definition:** The failure dialogue sequence for a generic sidequest, triggered when the quest fails.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_fail_GlassCannon`


**Definition:** The failure dialogue sequence for the GlassCannon sidequest, triggered when the quest fails.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_fail_HardPill`


**Definition:** The failure dialogue sequence for the HardPill sidequest, triggered when the quest fails.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_fail_HiveMind`


**Definition:** The dialogue and camera sequence played upon failure of the quest for this item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_fail_MagicMirror`


**Definition:** The dialogue and camera sequence played upon failure of the quest for this item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_fail_MeStone`


**Definition:** The dialogue and camera sequence played upon failure of the quest for this item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_fail_MultilinkCable`


**Definition:** The dialogue and camera sequence played upon failure of the quest for this item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_fail_MysteriousDice`


**Definition:** The dialogue and camera sequence played upon failure of the quest for this item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_fail_MysteriousGlasses`


**Definition:** The dialogue and camera sequence played upon failure of the quest for this item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_fail_NDEDevice`


**Definition:** The dialogue and camera sequence played upon failure of the quest for this item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_fail_NuclearKnife`


**Definition:** The dialogue and camera sequence played upon failure of the quest for this item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_fail_PartialLobotomy`


**Definition:** The dialogue and camera sequence played upon failure of the quest for this item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_fail_PartyDetonator`


**Definition:** The dialogue and camera sequence played upon failure of the quest for this item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_fail_PersonalHeater`


**Definition:** The dialogue and camera sequence played upon failure of the quest for this item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_fail_PersuasionDevice`


**Definition:** The dialogue and camera sequence played upon failure of the quest for this item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_fail_PrincessHat`


**Definition:** The dialogue and camera sequence played upon failure of the quest for this item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_fail_RealityScrambler`


**Definition:** The dialogue and camera sequence played upon failure of the quest for this item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_fail_Redacted`


**Definition:** The dialogue and camera sequence played upon failure of the quest for this item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_fail_SpiderInjector`


**Definition:** The dialogue and camera sequence played upon failure of the quest for this item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_fail_Stopwatch`


**Definition:** The dialogue and camera sequence played upon failure of the quest for this item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_fail_StorageLocker`


**Definition:** The dialogue and camera sequence played upon failure of the quest for this item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_fail_TheIOU`


**Definition:** The dialogue and camera sequence played upon failure of the quest for this item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_fail_TheLoner`


**Definition:** The dialogue and camera sequence played upon failure of the quest for this item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_fail_Trapfest99`


**Definition:** The dialogue and camera sequence played upon failure of the quest for this item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_fail_UltraVision3000`


**Definition:** The dialogue and camera sequence played upon failure of the quest for this item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `beaniesquest_intro_AI`


**Definition:** The dialogue and camera sequence played during the introduction of this quest item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_intro_AirHorn`


**Definition:** The dialogue and camera sequence played during the introduction of this quest item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_intro_AngryFace`


**Definition:** The dialogue and camera sequence played during the introduction of this quest item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_intro_AnimalHands`


**Definition:** The dialogue and camera sequence played during the introduction of this quest item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_intro_BubbleBoy`


**Definition:** The dialogue and camera sequence played during the introduction of this quest item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_intro_ChadImplant`


**Definition:** The dialogue and camera sequence played during the introduction of this quest item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_intro_ChaosDevice`


**Definition:** The dialogue and camera sequence played during the introduction of this quest item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_intro_DimensionalDivider`


**Definition:** The dialogue and camera sequence played during the introduction of this quest item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_intro_DiseaseJar`


**Definition:** The dialogue and camera sequence played during the introduction of this quest item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_intro_ExperimentalTreatment`


**Definition:** The dialogue and camera sequence played during the introduction of this quest item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_intro_FartFace`


**Definition:** The dialogue and camera sequence played during the introduction of this quest item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_intro_FigLeaf`


**Definition:** The dialogue and camera sequence played during the introduction of this quest item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_intro_Generic`


**Definition:** The dialogue and camera sequence played during the introduction of this quest item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `beaniesquest_intro_GlassCannon`


**Definition:** The dialogue and camera sequence played during the introduction of this quest item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_intro_HardPill`


**Definition:** The dialogue and camera sequence played during the introduction of this quest item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_intro_HiveMind`


**Definition:** The dialogue and camera sequence played during the introduction of this quest item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_intro_MagicMirror`


**Definition:** The dialogue and camera sequence played during the introduction of this quest item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_intro_MeStone`


**Definition:** The dialogue and camera sequence played during the introduction of this quest item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_intro_MultilinkCable`


**Definition:** The dialogue and camera sequence played during the introduction of this quest item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_intro_MysteriousDice`


**Definition:** The dialogue and camera sequence played during the introduction of this quest item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_intro_MysteriousGlasses`


**Definition:** The dialogue and camera sequence played during the introduction of this quest item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_intro_NDEDevice`


**Definition:** The dialogue and camera sequence played during the introduction of this quest item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_intro_NuclearKnife`


**Definition:** The dialogue and camera sequence played during the introduction of this quest item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_intro_PartialLobotomy`


**Definition:** The dialogue and camera sequence played during the introduction of this quest item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_intro_PartyDetonator`


**Definition:** The dialogue and camera sequence played during the introduction of this quest item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_intro_PersonalHeater`


**Definition:** The dialogue and camera sequence played during the introduction of this quest item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_intro_PersuasionDevice`


**Definition:** The dialogue and camera sequence played during the introduction of this quest item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_intro_PrincessHat`


**Definition:** The dialogue and camera sequence played during the introduction of this quest item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_intro_RealityScrambler`


**Definition:** A sequence of dialog and state changes for Beanie's quest intro involving the Reality Scrambler item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_intro_Redacted`


**Definition:** A sequence of dialog and state changes for Beanie's quest intro involving the Redacted item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_intro_SpiderInjector`


**Definition:** A sequence of dialog and state changes for Beanie's quest intro involving the Spider Injector item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_intro_Stopwatch`


**Definition:** A sequence of dialog and state changes for Beanie's quest intro involving the Stopwatch item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_intro_StorageLocker`


**Definition:** A sequence of dialog and state changes for Beanie's quest intro involving the Storage Locker item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_intro_TheIOU`


**Definition:** A sequence of dialog and state changes for Beanie's quest intro involving The IOU item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_intro_TheLoner`


**Definition:** A sequence of dialog and state changes for Beanie's quest intro involving The Loner item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `beaniesquest_intro_Trapfest99`


**Definition:** A sequence of dialog and state changes for Beanie's quest intro involving the Trapfest99 item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `beaniesquest_intro_UltraVision3000`


**Definition:** A sequence of dialog and state changes for Beanie's quest intro involving the UltraVision3000 item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `boss_fight_intro`


**Definition:** A sequence of dialog and state changes for the boss fight introduction cutscene.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |
| `delay` | Float | The delay in seconds before the ability's effect triggers. | 1 | `.05`<br>`.1`<br>`.25` |

</details>


---


### Object: `boss_fight_round2`


**Definition:** A sequence of dialog and state changes for the boss fight round 2 cutscene.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |

</details>


---


### Object: `butch_begin_accepting_cats`


**Definition:** A sequence of dialog and state changes when Butch begins accepting cats into the shelter.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `begin_accepting_cats` | Enum | Specifies the character tag for the sequence that initiates accepting cats. | 1 | `beanies`<br>`butch`<br>`jack` |

</details>


---


### Object: `butch_boneyard_intro`


**Definition:** Defines the dialog sequence for Butch's introduction in the boneyard.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `butch_first_house_boss_beat`


**Definition:** A sequence of dialog and state changes after defeating the first house boss.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `butch_pyro`


**Definition:** A sequence of dialog and state changes discussing Butch's pyro character.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `butch_tina1`


**Definition:** A sequence of dialog and state changes related to Butch and Tina's first interaction.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `butch_tips_backstab`


**Definition:** A tutorial tip sequence explaining the backstab mechanic.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `butch_tips_charisma`


**Definition:** A tutorial tip sequence explaining the charisma stat.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `butch_tips_combat`


**Definition:** A tutorial tip sequence covering basic combat mechanics.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `butch_tips_disorders`


**Definition:** A tutorial tip sequence explaining disorders in cats.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `butch_tips_drafting`


**Definition:** A tutorial tip sequence explaining the drafting system.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `butch_tips_elements`


**Definition:** A tutorial tip sequence covering elemental damage types.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `butch_tips_hard`


**Definition:** A tutorial tip sequence about playing on hard difficulty.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `butch_tips_headhome`


**Definition:** A tutorial tip sequence about returning to the home base.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `butch_tips_houseboss`


**Definition:** A tutorial tip sequence explaining house bosses.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `butch_tips_info`


**Definition:** A tutorial tip sequence about viewing information on units.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `butch_tips_intelligence`


**Definition:** A tutorial tip sequence explaining the intelligence stat.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `butch_tips_intro`


**Definition:** The initial tutorial tip sequence that introduces Butch's tips.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `do_sequence` | Enum | Specifies the name of the sequence to execute. | 1 | `butch_tips_intelligence`<br>`forward_to_tips`<br>`tink_tips_comfort` |

</details>


---


### Object: `butch_tips_items`


**Definition:** A tutorial tip sequence about using items in combat.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `butch_tips_lesscats`


**Definition:** A tutorial tip sequence about managing with fewer cats.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `butch_tips_magicdamage`


**Definition:** A tutorial tip sequence explaining magic damage.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `butch_tips_passives`


**Definition:** A tutorial tip sequence covering passive abilities.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `butch_tips_reorient`


**Definition:** A tutorial tip sequence explaining the reorient mechanic.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `butch_tips_rewards`


**Definition:** A tutorial tip sequence about earning rewards.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `butch_tips_tacticalview`


**Definition:** A tutorial tip sequence about using tactical view.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `butch_tips_turnorder`


**Definition:** A tutorial tip sequence explaining turn order.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `butch_tips_wellrounded`


**Definition:** A tutorial tip sequence about building well-rounded teams.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `can_still_use_attack`


**Definition:** A sequence of dialog and state changes when a unit can still use an attack ability.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `get_token` | Enum | Specifies the name of the token to retrieve from the sequence's current state. | 1 | `can_still_use_attack`<br>`can_still_use_attack_didntspell`<br>`ranged_cat_attack` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |
| `wait_for` | Enum | Specifies the game action or event to wait for before continuing the sequence. | 1 | `action_selected`<br>`cat_turn`<br>`choose_cat1` |

</details>


---


### Object: `can_still_use_attack_didntspell`


**Definition:** A sequence of dialog and state changes when a unit didn't use a spell but can still attack.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `get_token` | Enum | Specifies the name of the token to retrieve from the sequence's current state. | 1 | `can_still_use_attack`<br>`can_still_use_attack_didntspell`<br>`ranged_cat_attack` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |
| `wait_for` | Enum | Specifies the game action or event to wait for before continuing the sequence. | 1 | `action_selected`<br>`cat_turn`<br>`choose_cat1` |

</details>


---


### Object: `cant_afford_a`


**Definition:** A sequence showing dialog when the player cannot afford item A.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | If true, the sequence can be cancelled by the player. | 1 | `true` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `wait_for_cancel` | Number | The number of frames to wait before the sequence is cancelled. | 1 | `1` |

</details>


---


### Object: `cant_afford_b`


**Definition:** A sequence showing dialog when the player cannot afford item B.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | If true, the sequence can be cancelled by the player. | 1 | `true` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `wait_for_cancel` | Number | The number of frames to wait before the sequence is cancelled. | 1 | `1` |

</details>


---


### Object: `cant_afford_c`


**Definition:** A sequence showing dialog when the player cannot afford item C.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | If true, the sequence can be cancelled by the player. | 1 | `true` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `wait_for_cancel` | Number | The number of frames to wait before the sequence is cancelled. | 1 | `1` |

</details>


---


### Object: `cant_afford_d`


**Definition:** A sequence showing dialog when the player cannot afford item D.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | If true, the sequence can be cancelled by the player. | 1 | `true` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `wait_for_cancel` | Number | The number of frames to wait before the sequence is cancelled. | 1 | `1` |

</details>


---


### Object: `cant_afford_iceage`


**Definition:** A sequence showing dialog when the player cannot afford the Ice Age item. Can also be a boolean flag.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | If true, the sequence can be cancelled by the player. | 1 | `true` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `wait_for_cancel` | Number | The number of frames to wait before the sequence is cancelled. | 1 | `1` |

</details>


---


### Object: `cant_afford_jurassic`


**Definition:** A sequence showing dialog when the player cannot afford the Jurassic item. Can also be a boolean flag.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | If true, the sequence can be cancelled by the player. | 1 | `true` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `wait_for_cancel` | Number | The number of frames to wait before the sequence is cancelled. | 1 | `1` |

</details>


---


### Object: `cant_afford_moon`


**Definition:** A sequence showing dialog when the player cannot afford the Moon item. Can also be a boolean flag.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | If true, the sequence can be cancelled by the player. | 1 | `true` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `wait_for_cancel` | Number | The number of frames to wait before the sequence is cancelled. | 1 | `1` |

</details>


---


### Object: `cant_afford_theend`


**Definition:** Defines the sequence for when the player cannot afford the End purchase, optionally cancelable with a dialog and autopass.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | If true, the sequence can be cancelled by the player. | 1 | `true` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `wait_for_cancel` | Number | The number of frames to wait before the sequence is cancelled. | 1 | `1` |

</details>


---


### Object: `class_unlock_butcher`


**Definition:** Defines the sequence for unlocking the Butcher class, including dialogs and camera state changes.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `unlock_class` | Enum | Specifies the name of the cat class to unlock. | 1 | `Butcher`<br>`Druid`<br>`Jester` |

</details>


---


### Object: `class_unlock_druid`


**Definition:** Defines the dialog sequence that plays when unlocking the Druid class.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `unlock_class` | Enum | Specifies the name of the cat class to unlock. | 1 | `Butcher`<br>`Druid`<br>`Jester` |

</details>


---


### Object: `class_unlock_jester`


**Definition:** Defines the dialog sequence for unlocking the Jester class.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `unlock_class` | Enum | Specifies the name of the cat class to unlock. | 1 | `Butcher`<br>`Druid`<br>`Jester` |

</details>


---


### Object: `class_unlock_medic`


**Definition:** Defines the dialog sequence that plays when unlocking the Medic class.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `unlock_class` | Enum | Specifies the name of the cat class to unlock. | 1 | `Butcher`<br>`Druid`<br>`Jester` |

</details>


---


### Object: `class_unlock_monk`


**Definition:** Defines the dialog sequence that plays when unlocking the Monk class.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `unlock_class` | Enum | Specifies the name of the cat class to unlock. | 1 | `Butcher`<br>`Druid`<br>`Jester` |

</details>


---


### Object: `class_unlock_necromancer`


**Definition:** Defines the dialog sequence that plays when unlocking the Necromancer class.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `unlock_class` | Enum | Specifies the name of the cat class to unlock. | 1 | `Butcher`<br>`Druid`<br>`Jester` |

</details>


---


### Object: `class_unlock_psychic`


**Definition:** Defines the dialog sequence that plays when unlocking the Psychic class.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `unlock_class` | Enum | Specifies the name of the cat class to unlock. | 1 | `Butcher`<br>`Druid`<br>`Jester` |

</details>


---


### Object: `class_unlock_thief`


**Definition:** Defines the dialog sequence that plays when unlocking the Thief class.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `unlock_class` | Enum | Specifies the name of the cat class to unlock. | 1 | `Butcher`<br>`Druid`<br>`Jester` |

</details>


---


### Object: `class_unlock_tinkerer`


**Definition:** Defines the dialog sequence that plays when unlocking the Tinkerer class.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `unlock_class` | Enum | Specifies the name of the cat class to unlock. | 1 | `Butcher`<br>`Druid`<br>`Jester` |

</details>


---


### Object: `collected_new_items`


**Definition:** Defines the dialog sequence that plays when the player has collected new items after an adventure.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `collected_nothing`


**Definition:** Defines the dialog sequence that plays when the player collected nothing (e.g., died in first combat).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `do_not_end_turn`


**Definition:** Defines a dialog sequence warning the player not to end their turn.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |
| `clear_token` | Enum | Specifies the token name to clear from the sequence's state. | 1 | `do_not_end_turn`<br>`map_equip_items2`<br>`melee_cat_spit_ignore` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |

</details>


---


### Object: `done_spitting_fail_ally`


**Definition:** Defines a dialog sequence that plays when a spitting action fails on an ally.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |

</details>


---


### Object: `done_spitting_fail_miss`


**Definition:** Defines a dialog sequence that plays when a spitting action misses.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |

</details>


---


### Object: `done_spitting_fail_rat`


**Definition:** Defines a dialog sequence that plays when a spitting action fails on a rat.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |

</details>


---


### Object: `done_spitting_success`


**Definition:** Defines a dialog sequence that plays when a spitting action succeeds.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |

</details>


---


### Object: `ending`


**Definition:** Defines the ending dialog sequence with Dr. Beanies after saving the player in the time machine.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |
| `screenshake` | Array | [intensity, duration] in frames. Applies a screen shake effect. | 1 | `[.5, 10]`<br>`[1, 30]` |

</details>


---


### Object: `finish_adventure`


**Definition:** Defines a dialog sequence that plays when the player finishes an adventure.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |

</details>


---


### Object: `first_fight_intro`


**Definition:** Defines the intro dialog sequence for the first fight.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |
| `wait_for` | Enum | Specifies the game action or event to wait for before continuing the sequence. | 1 | `action_selected`<br>`cat_turn`<br>`choose_cat1` |
| `delay` | Float | The delay in seconds before the ability's effect triggers. | 1 | `.05`<br>`.1`<br>`.25` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `set_mood` | Enum | Specifies the mood state to set for the speaking NPC (e.g., 'pondering', 'sad', 'default', 'happy', 'veryhappy'). | 1 | `default`<br>`happy`<br>`pondering` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `first_house_boss_tomorrow`


**Definition:** Defines a dialog sequence about a boss arriving tomorrow in the first house.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |

</details>


---


### Object: `first_house_hint_retired`


**Definition:** Defines a dialog sequence giving a hint about a retired cat in the first house.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |

</details>


---


### Object: `frank_caves_intro`


**Definition:** Defines the dialog sequence for Frank's introduction in the caves.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `frank_ending`


**Definition:** Defines the dialog sequence for Frank's new intro after the nuke ending.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `frank_max1`


**Definition:** Defines a dialog sequence for Frank at maximum affinity level 1.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `frank_max2`


**Definition:** Defines a dialog sequence for Frank at maximum affinity level 2.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `frank_max3`


**Definition:** Defines a dialog sequence for Frank at maximum affinity level 3.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `frank_max4`


**Definition:** Defines a dialog sequence for Frank at maximum affinity level 4.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `frank_max5`


**Definition:** Defines a dialog sequence for Frank at maximum affinity level 5.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `frank_max_intro`


**Definition:** Defines the dialog sequence and rewards for reaching max favor with Frank.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `frank_max_repeating`


**Definition:** Defines the repeatable dialog sequence and rewards for Frank at max favor.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `do_random_sequence` | Array | An array of sequence names; one is chosen at random to execute. | 1 ||

</details>


---


### Object: `frank_terminator2`


**Definition:** Defines a dialog sequence for Frank's 'terminator' event (likely a special encounter).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `frank_tips_1`


**Definition:** Defines a tips dialog sequence from Frank (tip #1).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `frank_tips_10`


**Definition:** Defines a tips dialog sequence from Frank (tip #10).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `frank_tips_2`


**Definition:** Defines a tips dialog sequence from Frank (tip #2).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `frank_tips_3`


**Definition:** Defines a tips dialog sequence from Frank (tip #3).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `frank_tips_4`


**Definition:** Defines a tips dialog sequence from Frank (tip #4).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `frank_tips_5`


**Definition:** Defines a tips dialog sequence from Frank (tip #5).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `frank_tips_6`


**Definition:** Defines a tips dialog sequence from Frank (tip #6).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `frank_tips_7`


**Definition:** Defines a tips dialog sequence from Frank (tip #7).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `frank_tips_8`


**Definition:** Defines a tips dialog sequence from Frank (tip #8).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `frank_tips_9`


**Definition:** Defines a tips dialog sequence from Frank (tip #9).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `gone`


**Definition:** Sets the NPC state to 'gone', making them disappear from the scene.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `house_intro`


**Definition:** Defines the intro dialog sequence that plays when entering a house.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |
| `delay` | Float | The delay in seconds before the ability's effect triggers. | 1 | `.05`<br>`.1`<br>`.25` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |
| `wait_for` | Enum | Specifies the game action or event to wait for before continuing the sequence. | 1 | `action_selected`<br>`cat_turn`<br>`choose_cat1` |

</details>


---


### Object: `house_kitten_box`


**Definition:** Defines a dialog sequence about a kitten box in the house.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |

</details>


---


### Object: `house_pass_day`


**Definition:** A sequence that plays dialog and animations when a day passes in the house.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |

</details>


---


### Object: `house_pass_day2`


**Definition:** A sequence that plays extended dialog and animations when a day passes in the house.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |

</details>


---


### Object: `house_pipe`


**Definition:** A sequence that plays dialog and animations related to the house pipe.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |

</details>


---


### Object: `house_retired_cat_box`


**Definition:** A sequence that plays dialog and animations for the retired cat box.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `house_starred_box`


**Definition:** A sequence that plays dialog and animations for the starred box.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |

</details>


---


### Object: `house_strays`


**Definition:** A sequence that plays dialog and animations for stray cats in the house.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |
| `delay` | Float | The delay in seconds before the ability's effect triggers. | 1 | `.05`<br>`.1`<br>`.25` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `request_cat_info` | Enum | Specifies the type of cat information to request (e.g., 'stray'). | 1 | `stray` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |
| `wait_for` | Enum | Specifies the game action or event to wait for before continuing the sequence. | 1 | `action_selected`<br>`cat_turn`<br>`choose_cat1` |

</details>


---


### Object: `house_upgrade_4throom`


**Definition:** Defines the dialog and house upgrade for unlocking the 4th room.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `house_upgrade_attic`


**Definition:** Defines the dialog and house upgrade for the attic.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `house_upgrade_basement`


**Definition:** A sequence that triggers dialog and a reward for the first basement upgrade.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `house_upgrade_basement2`


**Definition:** A sequence that triggers the second basement upgrade and awards favor.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `house_upgrade_basement3`


**Definition:** A sequence that triggers the third basement upgrade and awards favor.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `house_upgrade_basement4`


**Definition:** A sequence that triggers the fourth basement upgrade and awards favor.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `house_upgrade_basement5`


**Definition:** A sequence that triggers the fifth basement upgrade and awards favor.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `house_upgrade_largehouse`


**Definition:** Defines the dialog and house upgrade for the large house.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `house_upgrade_mediumhouse`


**Definition:** Defines the dialog and house upgrade for the medium house.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `intro`


**Definition:** An object defining the introductory cutscene for the event, including title, cat selection, and visuals.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `set_mood` | Enum | Specifies the mood state to set for the speaking NPC (e.g., 'pondering', 'sad', 'default', 'happy', 'veryhappy'). | 1 | `default`<br>`happy`<br>`pondering` |
| `wait_for` | Enum | Specifies the game action or event to wait for before continuing the sequence. | 1 | `action_selected`<br>`cat_turn`<br>`choose_cat1` |
| `delay` | Float | The delay in seconds before the ability's effect triggers. | 1 | `.05`<br>`.1`<br>`.25` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `introduce_hard_path`


**Definition:** A sequence that plays dialog and animations to introduce the hard path.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |

</details>


---


### Object: `jack_begin_accepting_cats`


**Definition:** A sequence that shows Jack's introductory dialog for accepting cats, locking player controls.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `begin_accepting_cats` | Enum | Specifies the character tag for the sequence that initiates accepting cats. | 1 | `beanies`<br>`butch`<br>`jack` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `jack_desert_intro`


**Definition:** Defines the dialog sequence for Jack's introduction in the desert.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `Jack_Gainaltfurniture`


**Definition:** A sequence that plays Jack's dialog explaining rare alt furniture and the Nona cat, locking controls.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `jack_introduction`


**Definition:** A sequence that plays Jack's initial introduction dialog and animation.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |
| `wait_for` | Enum | Specifies the game action or event to wait for before continuing the sequence. | 1 | `action_selected`<br>`cat_turn`<br>`choose_cat1` |
| `get_random_furniture_piece` | Array | An array of furniture piece names; one is chosen at random to spawn. | 1 | `[small_trash_cans small_trash_can2]` |

</details>


---


### Object: `jack_max1`


**Definition:** A sequence that plays Jack's first max favor dialog sequence, locking controls.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `jack_max2`


**Definition:** A sequence that plays Jack's second max favor dialog sequence, locking controls.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `jack_max3`


**Definition:** A sequence that plays Jack's third max favor dialog sequence, locking controls.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `jack_max4`


**Definition:** A sequence that plays Jack's fourth max favor dialog sequence, locking controls.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `jack_max5`


**Definition:** A sequence that plays Jack's fifth max favor dialog sequence, locking controls.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `jack_max_intro`


**Definition:** Defines the dialog sequence and rewards for reaching max favor with Jack.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `jack_max_repeating`


**Definition:** Defines the repeatable dialog sequence and rewards for Jack at max favor.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `do_random_sequence` | Array | An array of sequence names; one is chosen at random to execute. | 1 ||

</details>


---


### Object: `jack_shopupgrade1`


**Definition:** Defines the dialog and shop level up for Jack's first shop upgrade.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `jack_shopupgrade2`


**Definition:** Defines the dialog and shop level up for Jack's second shop upgrade.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `jack_shopupgrade3`


**Definition:** Defines the dialog and shop level up for Jack's third shop upgrade.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `jack_shopupgrade4`


**Definition:** Defines the dialog and shop level up for Jack's fourth shop upgrade.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `jack_zara`


**Definition:** A sequence that plays Jack's dialog about Zara, locking controls.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `level_up_didnt_select_sunburn`


**Definition:** A sequence that plays dialog when the player did not select the Sunburn level-up option.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |

</details>


---


### Object: `level_up_intro`


**Definition:** A sequence that plays the introductory dialog and animation for the level-up UI.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |
| `wait_for` | Enum | Specifies the game action or event to wait for before continuing the sequence. | 1 | `action_selected`<br>`cat_turn`<br>`choose_cat1` |
| `delay` | Float | The delay in seconds before the ability's effect triggers. | 1 | `.05`<br>`.1`<br>`.25` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `lock_mouse` | Number | If non-zero, locks the mouse cursor in place. | 1 | `1` |
| `unlock_mouse` | Number | If non-zero, unlocks the mouse cursor. | 1 | `1` |

</details>


---


### Object: `level_up_selected_sunburn`


**Definition:** A sequence that plays dialog when the player selected the Sunburn level-up option.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |

</details>


---


### Object: `low_on_food`


**Definition:** A sequence that plays a dialog and animation warning the player that they are low on food.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `map_click_node`


**Definition:** A sequence that teaches the player to click a map node, then unlocks controls.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |
| `wait_for` | Enum | Specifies the game action or event to wait for before continuing the sequence. | 1 | `action_selected`<br>`cat_turn`<br>`choose_cat1` |

</details>


---


### Object: `map_equip_items`


**Definition:** A sequence that teaches the player to equip items on the map.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |
| `wait_for` | Enum | Specifies the game action or event to wait for before continuing the sequence. | 1 | `action_selected`<br>`cat_turn`<br>`choose_cat1` |

</details>


---


### Object: `map_equip_items2`


**Definition:** A sequence that provides a secondary reminder to equip items, clearing its own token.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |
| `clear_token` | Enum | Specifies the token name to clear from the sequence's state. | 1 | `do_not_end_turn`<br>`map_equip_items2`<br>`melee_cat_spit_ignore` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |
| `wait_for` | Enum | Specifies the game action or event to wait for before continuing the sequence. | 1 | `action_selected`<br>`cat_turn`<br>`choose_cat1` |

</details>


---


### Object: `melee_attack_rat`


**Definition:** A tutorial sequence that demonstrates how to perform a melee attack on a rat.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `get_token` | Enum | Specifies the name of the token to retrieve from the sequence's current state. | 1 | `can_still_use_attack`<br>`can_still_use_attack_didntspell`<br>`ranged_cat_attack` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |
| `wait_for` | Enum | Specifies the game action or event to wait for before continuing the sequence. | 1 | `action_selected`<br>`cat_turn`<br>`choose_cat1` |

</details>


---


### Object: `melee_cat_spit`


**Definition:** A tutorial sequence that demonstrates how to use the cat spit ability.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |
| `wait_for` | Enum | Specifies the game action or event to wait for before continuing the sequence. | 1 | `action_selected`<br>`cat_turn`<br>`choose_cat1` |

</details>


---


### Object: `melee_cat_spit_fail_ally`


**Definition:** A tutorial sequence that plays when the cat spit fails due to targeting an ally.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |
| `wait_for` | Enum | Specifies the game action or event to wait for before continuing the sequence. | 1 | `action_selected`<br>`cat_turn`<br>`choose_cat1` |

</details>


---


### Object: `melee_cat_spit_fail_miss`


**Definition:** A tutorial sequence that plays when the cat spit fails due to a miss.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |
| `wait_for` | Enum | Specifies the game action or event to wait for before continuing the sequence. | 1 | `action_selected`<br>`cat_turn`<br>`choose_cat1` |

</details>


---


### Object: `melee_cat_spit_fail_rat`


**Definition:** A tutorial sequence that plays when the cat spit fails to hit a rat.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |
| `wait_for` | Enum | Specifies the game action or event to wait for before continuing the sequence. | 1 | `action_selected`<br>`cat_turn`<br>`choose_cat1` |

</details>


---


### Object: `melee_cat_spit_ignore`


**Definition:** A tutorial sequence that plays when the player ignores the cat spit prompt.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |
| `clear_token` | Enum | Specifies the token name to clear from the sequence's state. | 1 | `do_not_end_turn`<br>`map_equip_items2`<br>`melee_cat_spit_ignore` |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |
| `wait_for` | Enum | Specifies the game action or event to wait for before continuing the sequence. | 1 | `action_selected`<br>`cat_turn`<br>`choose_cat1` |

</details>


---


### Object: `melee_cat_spit_success`


**Definition:** A tutorial sequence that plays when the cat spit is successfully used.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |
| `wait_for` | Enum | Specifies the game action or event to wait for before continuing the sequence. | 1 | `action_selected`<br>`cat_turn`<br>`choose_cat1` |

</details>


---


### Object: `melee_killed_rat`


**Definition:** A tutorial sequence that plays after the player kills a rat with a melee attack.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `wait_for` | Enum | Specifies the game action or event to wait for before continuing the sequence. | 1 | `action_selected`<br>`cat_turn`<br>`choose_cat1` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `unlock_mouse` | Number | If non-zero, unlocks the mouse cursor. | 1 | `1` |

</details>


---


### Object: `melee_move2`


**Definition:** A tutorial sequence that teaches the player to use movement actions.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |
| `clear_token` | Enum | Specifies the token name to clear from the sequence's state. | 1 | `do_not_end_turn`<br>`map_equip_items2`<br>`melee_cat_spit_ignore` |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |
| `wait_for` | Enum | Specifies the game action or event to wait for before continuing the sequence. | 1 | `action_selected`<br>`cat_turn`<br>`choose_cat1` |

</details>


---


### Object: `melee_out_of_actions`


**Definition:** A tutorial sequence that explains when the player is out of actions in melee.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |
| `wait_for` | Enum | Specifies the game action or event to wait for before continuing the sequence. | 1 | `action_selected`<br>`cat_turn`<br>`choose_cat1` |

</details>


---


### Object: `new_adventure`


**Definition:** A sequence that plays dialog and animation when starting a new adventure.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `organ_boneyard_intro`


**Definition:** Defines the dialog sequence for Organ Grinder's introduction in the boneyard.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `organ_intro`


**Definition:** Sequence of events for the Organ Grinder's introductory dialogue.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `begin_accepting_cats` | Enum | Specifies the character tag for the sequence that initiates accepting cats. | 1 | `beanies`<br>`butch`<br>`jack` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `set_organ_name` | String | The name to assign to the organ in this sequence. | 1 | `"Tyler"` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `organ_max1`


**Definition:** Sequence of events for the Organ Grinder's first max favor dialogue.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `organ_max2`


**Definition:** Sequence of events for the Organ Grinder's second max favor dialogue.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `organ_max3`


**Definition:** Sequence of events for the Organ Grinder's third max favor dialogue.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `organ_max4`


**Definition:** Sequence of events for the Organ Grinder's fourth max favor dialogue.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `organ_max5`


**Definition:** Sequence of events for the Organ Grinder's fifth max favor dialogue.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `organ_max_intro`


**Definition:** Defines the dialog sequence and rewards for reaching max favor with Organ Grinder.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `organ_max_repeating`


**Definition:** Defines the repeatable dialog sequence and rewards for Organ Grinder at max favor.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `do_random_sequence` | Array | An array of sequence names; one is chosen at random to execute. | 1 ||

</details>


---


### Object: `organ_rename`


**Definition:** Sequence of events for the Organ Grinder's rename dialogue.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `set_organ_name` | String | The name to assign to the organ in this sequence. | 1 | `"Tyler"` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `organ_throbbingdomain_intro`


**Definition:** Defines the dialog sequence for Organ Grinder's introduction in the throbbing domain.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `organ_tina3`


**Definition:** Sequence of events for the Organ Grinder's dialogue with Tina (stage 3).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `organ_unlock`


**Definition:** Defines the dialog and shop level up for unlocking Organ Grinder.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `organ_upgrade1`


**Definition:** Defines the dialog and shop level up for Organ Grinder's first upgrade.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `organ_upgrade2`


**Definition:** Defines the dialog and shop level up for Organ Grinder's second upgrade.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `organ_upgrade3`


**Definition:** Defines the dialog and shop level up for Organ Grinder's third upgrade.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `organ_upgrade4`


**Definition:** Defines the dialog and shop level up for Organ Grinder's fourth upgrade.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `organ_upgrade5`


**Definition:** Defines the dialog and shop level up for Organ Grinder's fifth upgrade.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `organ_upgrade6`


**Definition:** Defines the dialog and shop level up for Organ Grinder's sixth upgrade.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `purchase_item_a`


**Definition:** Sequence of events for purchasing shop item A from Tracy.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | If true, the sequence can be cancelled by the player. | 1 | `true` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `wait_for_cancel` | Number | The number of frames to wait before the sequence is cancelled. | 1 | `1` |

</details>


---


### Object: `purchase_item_b`


**Definition:** Sequence of events for purchasing shop item B from Tracy.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | If true, the sequence can be cancelled by the player. | 1 | `true` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `wait_for_cancel` | Number | The number of frames to wait before the sequence is cancelled. | 1 | `1` |

</details>


---


### Object: `purchase_item_c`


**Definition:** Sequence of events for purchasing shop item C from Tracy.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | If true, the sequence can be cancelled by the player. | 1 | `true` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `wait_for_cancel` | Number | The number of frames to wait before the sequence is cancelled. | 1 | `1` |

</details>


---


### Object: `purchase_item_d`


**Definition:** Sequence of events for purchasing shop item D from Tracy.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | If true, the sequence can be cancelled by the player. | 1 | `true` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `wait_for_cancel` | Number | The number of frames to wait before the sequence is cancelled. | 1 | `1` |

</details>


---


### Object: `purchase_item_iceage`


**Definition:** Sequence of events for purchasing the Ice Age shop item. When set to true, indicates the purchase has already occurred.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | If true, the sequence can be cancelled by the player. | 1 | `true` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `wait_for_cancel` | Number | The number of frames to wait before the sequence is cancelled. | 1 | `1` |

</details>


---


### Object: `purchase_item_jurassic`


**Definition:** Sequence of events for purchasing the Jurassic shop item. When set to true, indicates the purchase has already occurred.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | If true, the sequence can be cancelled by the player. | 1 | `true` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `wait_for_cancel` | Number | The number of frames to wait before the sequence is cancelled. | 1 | `1` |

</details>


---


### Object: `purchase_item_moon`


**Definition:** Sequence of events for purchasing the Moon shop item. When set to true, indicates the purchase has already occurred.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | If true, the sequence can be cancelled by the player. | 1 | `true` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `wait_for_cancel` | Number | The number of frames to wait before the sequence is cancelled. | 1 | `1` |

</details>


---


### Object: `purchase_item_theend`


**Definition:** Sequence of events for purchasing The End shop item. When set to true, indicates the purchase has already occurred.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | If true, the sequence can be cancelled by the player. | 1 | `true` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `wait_for_cancel` | Number | The number of frames to wait before the sequence is cancelled. | 1 | `1` |

</details>


---


### Object: `ranged_attack_tomtom`


**Definition:** Sequence of events for TomTom's ranged attack.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |

</details>


---


### Object: `ranged_attack_tomtom_fail_ally`


**Definition:** Sequence of events for when TomTom's ranged attack fails due to an ally in the way.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |

</details>


---


### Object: `ranged_attack_tomtom_fail_miss`


**Definition:** Sequence of events for when TomTom's ranged attack misses.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |

</details>


---


### Object: `ranged_attack_tomtom_fail_rat`


**Definition:** Sequence of events for when TomTom's ranged attack fails due to a rat.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |

</details>


---


### Object: `ranged_cat_attack`


**Definition:** Sequence of events for the cat's ranged attack.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |
| `wait_for` | Enum | Specifies the game action or event to wait for before continuing the sequence. | 1 | `action_selected`<br>`cat_turn`<br>`choose_cat1` |

</details>


---


### Object: `ranged_cat_early_attack2_ally`


**Definition:** Sequence of events for the cat's second early ranged attack failing due to an ally.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |

</details>


---


### Object: `ranged_cat_early_attack2_miss`


**Definition:** Sequence of events for the cat's second early ranged attack missing.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |

</details>


---


### Object: `ranged_cat_early_attack2_rat`


**Definition:** Sequence of events for the cat's second early ranged attack failing due to a rat.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |

</details>


---


### Object: `ranged_cat_early_attack_ally`


**Definition:** Sequence of events for the cat's first early ranged attack failing due to an ally.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |

</details>


---


### Object: `ranged_cat_early_attack_miss`


**Definition:** Sequence of events for the cat's first early ranged attack missing.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |

</details>


---


### Object: `ranged_cat_early_attack_rat`


**Definition:** Sequence of events for the cat's first early ranged attack failing due to a rat.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |

</details>


---


### Object: `ranged_cat_failmove`


**Definition:** Sequence of events for the cat's failed ranged attack move.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |

</details>


---


### Object: `ranged_cat_intro`


**Definition:** Sequence of events for the cat's ranged attack introduction.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |
| `wait_for` | Enum | Specifies the game action or event to wait for before continuing the sequence. | 1 | `action_selected`<br>`cat_turn`<br>`choose_cat1` |

</details>


---


### Object: `ranged_cat_roll`


**Definition:** Sequence of events for the cat's ranged attack roll animation.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |
| `wait_for` | Enum | Specifies the game action or event to wait for before continuing the sequence. | 1 | `action_selected`<br>`cat_turn`<br>`choose_cat1` |

</details>


---


### Object: `ranged_cat_rolled_first`


**Definition:** Sequence of events for when the cat rolls first.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |
| `wait_for` | Enum | Specifies the game action or event to wait for before continuing the sequence. | 1 | `action_selected`<br>`cat_turn`<br>`choose_cat1` |

</details>


---


### Object: `steven_100`


**Definition:** Sequence of events for Steven's 100% completion dialogue.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `steven_introduction`


**Definition:** Sequence of events for Steven's introduction dialogue.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `blocking` | Boolean | If true, the unit blocks movement and line-of-sight. | 1 | `false`<br>`idlenoani` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `steven_milliontrashed`


**Definition:** A dialogue sequence or favor reward configuration for the NPC Steven, triggered when the player has accumulated 1,000,000 favor.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `steven_postendgame`


**Definition:** A dialogue sequence for Steven that plays after the player has beaten the game and seen the final ending.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `steven_resummon`


**Definition:** A sequence triggered after beating the final boss, unlocking the ability to resummon house bosses.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `steven_savescum_1`


**Definition:** A sequence that plays a random warning sequence for the first savescum event.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `do_random_sequence` | Array | An array of sequence names; one is chosen at random to execute. | 1 ||

</details>


---


### Object: `steven_savescum_100`


**Definition:** A secret sequence for the 100th savescum event.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `autosave` | Enum | Specifies the point at which the game saves progress, such as before a house boss prep or during an adventure. | 1 | `adventure`<br>`housebossprep` |

</details>


---


### Object: `steven_savescum_1alt1`


**Definition:** One of the random alternative warning sequences for the first savescum event.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `autosave` | Enum | Specifies the point at which the game saves progress, such as before a house boss prep or during an adventure. | 1 | `adventure`<br>`housebossprep` |

</details>


---


### Object: `steven_savescum_1alt2`


**Definition:** One of the random alternative warning sequences for the first savescum event.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `autosave` | Enum | Specifies the point at which the game saves progress, such as before a house boss prep or during an adventure. | 1 | `adventure`<br>`housebossprep` |

</details>


---


### Object: `steven_savescum_1alt3`


**Definition:** One of the random alternative warning sequences for the first savescum event.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `autosave` | Enum | Specifies the point at which the game saves progress, such as before a house boss prep or during an adventure. | 1 | `adventure`<br>`housebossprep` |

</details>


---


### Object: `steven_savescum_2`


**Definition:** A sequence that plays a random sequence for the second savescum event (1 cat deja vu 10%).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `do_random_sequence` | Array | An array of sequence names; one is chosen at random to execute. | 1 ||

</details>


---


### Object: `steven_savescum_2alt1`


**Definition:** One of the random alternative sequences for the second savescum event (1 cat deja vu 10%).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `autosave` | Enum | Specifies the point at which the game saves progress, such as before a house boss prep or during an adventure. | 1 | `adventure`<br>`housebossprep` |

</details>


---


### Object: `steven_savescum_2alt2`


**Definition:** One of the random alternative sequences for the second savescum event (1 cat deja vu 10%).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `autosave` | Enum | Specifies the point at which the game saves progress, such as before a house boss prep or during an adventure. | 1 | `adventure`<br>`housebossprep` |

</details>


---


### Object: `steven_savescum_2alt3`


**Definition:** One of the random alternative sequences for the second savescum event (1 cat deja vu 10%).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `autosave` | Enum | Specifies the point at which the game saves progress, such as before a house boss prep or during an adventure. | 1 | `adventure`<br>`housebossprep` |

</details>


---


### Object: `steven_savescum_3`


**Definition:** A sequence that plays a random sequence for the third savescum event (all cats deja vu 10%).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `do_random_sequence` | Array | An array of sequence names; one is chosen at random to execute. | 1 ||

</details>


---


### Object: `steven_savescum_3alt1`


**Definition:** One of the random alternative sequences for the third savescum event (all cats deja vu 10%).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `autosave` | Enum | Specifies the point at which the game saves progress, such as before a house boss prep or during an adventure. | 1 | `adventure`<br>`housebossprep` |

</details>


---


### Object: `steven_savescum_3alt2`


**Definition:** One of the random alternative sequences for the third savescum event (all cats deja vu 10%).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `autosave` | Enum | Specifies the point at which the game saves progress, such as before a house boss prep or during an adventure. | 1 | `adventure`<br>`housebossprep` |

</details>


---


### Object: `steven_savescum_3alt3`


**Definition:** One of the random alternative sequences for the third savescum event (all cats deja vu 10%).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `autosave` | Enum | Specifies the point at which the game saves progress, such as before a house boss prep or during an adventure. | 1 | `adventure`<br>`housebossprep` |

</details>


---


### Object: `steven_savescum_4`


**Definition:** A sequence that plays a random sequence for the fourth savescum event (deja vu level up 25%).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `do_random_sequence` | Array | An array of sequence names; one is chosen at random to execute. | 1 ||

</details>


---


### Object: `steven_savescum_4alt1`


**Definition:** One of the random alternative sequences for the fourth savescum event (deja vu level up 25%, steven takes over).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `autosave` | Enum | Specifies the point at which the game saves progress, such as before a house boss prep or during an adventure. | 1 | `adventure`<br>`housebossprep` |

</details>


---


### Object: `steven_savescum_4alt2`


**Definition:** One of the random alternative sequences for the fourth savescum event (deja vu level up 25%, steven takes over).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `autosave` | Enum | Specifies the point at which the game saves progress, such as before a house boss prep or during an adventure. | 1 | `adventure`<br>`housebossprep` |

</details>


---


### Object: `steven_savescum_4alt3`


**Definition:** One of the random alternative sequences for the fourth savescum event (deja vu level up 25%, steven takes over).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `autosave` | Enum | Specifies the point at which the game saves progress, such as before a house boss prep or during an adventure. | 1 | `adventure`<br>`housebossprep` |

</details>


---


### Object: `steven_savescum_houseboss_1`


**Definition:** A warning sequence for the first house boss savescum event.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `autosave` | Enum | Specifies the point at which the game saves progress, such as before a house boss prep or during an adventure. | 1 | `adventure`<br>`housebossprep` |

</details>


---


### Object: `steven_savescum_houseboss_100`


**Definition:** A secret sequence for the 100th house boss savescum event.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `autosave` | Enum | Specifies the point at which the game saves progress, such as before a house boss prep or during an adventure. | 1 | `adventure`<br>`housebossprep` |

</details>


---


### Object: `steven_savescum_houseboss_2`


**Definition:** A sequence for the second house boss savescum event (all cats 10% deja vu).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `autosave` | Enum | Specifies the point at which the game saves progress, such as before a house boss prep or during an adventure. | 1 | `adventure`<br>`housebossprep` |

</details>


---


### Object: `steven_savescum_houseboss_3`


**Definition:** A sequence for the third house boss savescum event (all cats deja vu 25% and onward).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `autosave` | Enum | Specifies the point at which the game saves progress, such as before a house boss prep or during an adventure. | 1 | `adventure`<br>`housebossprep` |

</details>


---


### Object: `steven_savescum_intro`


**Definition:** A sequence that replaces the first savescum event sequences if it is the first time savescumming.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `autosave` | Enum | Specifies the point at which the game saves progress, such as before a house boss prep or during an adventure. | 1 | `adventure`<br>`housebossprep` |

</details>


---


### Object: `steven_savescum_intro_houseboss`


**Definition:** A sequence that replaces the first house boss savescum event sequences if it is the first time savescumming.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `autosave` | Enum | Specifies the point at which the game saves progress, such as before a house boss prep or during an adventure. | 1 | `adventure`<br>`housebossprep` |

</details>


---


### Object: `steven_unlock_act1_crazy`


**Definition:** A sequence triggered when beating Act 1 and its house bosses on Hard, unlocking Crazy difficulty.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `steven_unlock_act1_impossible`


**Definition:** A sequence triggered when beating Act 1 house bosses on Crazy, unlocking Impossible difficulty.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `steven_unlock_act2_crazy`


**Definition:** A sequence for unlocking Act 2 Crazy difficulty.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `steven_unlock_act2_hard`


**Definition:** A sequence triggered when beating Act 2 for the first time, unlocking Hard difficulty.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `steven_unlock_act2_impossible`


**Definition:** A sequence for unlocking Act 2 Impossible difficulty.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `steven_unlock_act3_crazy`


**Definition:** A sequence for unlocking Act 3 Crazy difficulty.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `steven_unlock_act3_hard`


**Definition:** A sequence triggered when beating Act 3 for the first time, unlocking Hard difficulty.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `steven_unlock_act3_impossible`


**Definition:** A sequence for unlocking Act 3 Impossible difficulty.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `take_cats_inside`


**Definition:** A sequence for taking cats inside the house.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |
| `clear_token` | Enum | Specifies the token name to clear from the sequence's state. | 1 | `do_not_end_turn`<br>`map_equip_items2`<br>`melee_cat_spit_ignore` |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `test_gamepad_prompts`


**Definition:** A sequence that shows gamepad binding prompts.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `tink_aggression`


**Definition:** A dialogue sequence or favor reward that unlocks the cat info panel for viewing a cat's aggression stat.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `tink_basestats`


**Definition:** A dialogue sequence or favor reward that unlocks the cat info panel for viewing a cat's base stats and stat modifications.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `tink_begin_accepting_cats`


**Definition:** A sequence for when Tink begins accepting cats.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `begin_accepting_cats` | Enum | Specifies the character tag for the sequence that initiates accepting cats. | 1 | `beanies`<br>`butch`<br>`jack` |

</details>


---


### Object: `tink_inbreeding`


**Definition:** A dialogue sequence or favor reward that unlocks the cat info panel for viewing a cat's inbreeding level and family tree.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `tink_max1`


**Definition:** One of the sequences played when Tink is at max favor (1 of 10).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `tink_max10`


**Definition:** One of the sequences played when Tink is at max favor (10 of 10).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `tink_max2`


**Definition:** One of the sequences played when Tink is at max favor (2 of 10).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `tink_max3`


**Definition:** One of the sequences played when Tink is at max favor (3 of 10).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `tink_max4`


**Definition:** One of the sequences played when Tink is at max favor (4 of 10).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `tink_max5`


**Definition:** One of the sequences played when Tink is at max favor (5 of 10).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `tink_max6`


**Definition:** One of the sequences played when Tink is at max favor (6 of 10).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `tink_max7`


**Definition:** One of the sequences played when Tink is at max favor (7 of 10).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `tink_max8`


**Definition:** One of the sequences played when Tink is at max favor (8 of 10).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `tink_max9`


**Definition:** One of the sequences played when Tink is at max favor (9 of 10).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `tink_max_intro`


**Definition:** The first dialogue sequence and favor reward that plays when Tink reaches maximum favor.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `tink_max_repeating`


**Definition:** A repeating dialogue sequence and favor reward that plays when Tink is at maximum favor, cycling through random sub-sequences.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `do_random_sequence` | Array | An array of sequence names; one is chosen at random to execute. | 1 ||

</details>


---


### Object: `tink_prettybow`


**Definition:** A dialogue sequence and favor reward that grants the gift item TinksBow.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `tink_relationships`


**Definition:** A dialogue sequence or favor reward that unlocks the cat info panel for viewing a cat's relationships (loves and hates).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `tink_sexuality`


**Definition:** A dialogue sequence or favor reward that unlocks the cat info panel for viewing a cat's libido and sexual orientation flags.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `tink_tags`


**Definition:** A dialogue sequence or favor reward that unlocks the ability to manually add symbols to a cat's name.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `tink_terminator`


**Definition:** A sequence for Tink's terminator event.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `tink_tina2`


**Definition:** A sequence for Tink and Tina interaction 2.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `tink_tips_appeal`


**Definition:** A sequence for Tink's tips on appeal.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `tink_tips_basestats`


**Definition:** A sequence for Tink's tips on base stats.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `tink_tips_cleaning`


**Definition:** A sequence for Tink's tips on cleaning.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `tink_tips_comfort`


**Definition:** A sequence of dialogs providing Tink's tips on cat comfort.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `tink_tips_health`


**Definition:** A sequence of dialogs providing Tink's tips on cat health.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `tink_tips_inbreeding`


**Definition:** A sequence of dialogs providing Tink's tips on inbreeding.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `tink_tips_intro`


**Definition:** A sequence of dialogs introducing Tink's tips, then playing the comfort tips sequence.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `do_sequence` | Enum | Specifies the name of the sequence to execute. | 1 | `butch_tips_intelligence`<br>`forward_to_tips`<br>`tink_tips_comfort` |

</details>


---


### Object: `tink_tips_multiclassing`


**Definition:** A sequence of dialogs providing Tink's tips on multiclassing.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `tink_tips_mutation`


**Definition:** A sequence of dialogs providing Tink's tips on mutations.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `tink_tips_stimulation`


**Definition:** A sequence of dialogs providing Tink's tips on stimulation.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `tracy_blankcollar1`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `tracy_blankcollar2`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `tracy_blankcollar3`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `tracy_foodbonus1`


**Definition:** A sequence showing Tracy explaining a food bonus reward.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `tracy_foodstorage1`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `tracy_foodstorage10`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `tracy_foodstorage2`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `tracy_foodstorage3`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `tracy_foodstorage4`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `tracy_foodstorage5`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `tracy_foodstorage6`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `tracy_foodstorage7`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `tracy_foodstorage8`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `tracy_foodstorage9`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `tracy_idol1`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `tracy_idol2`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `tracy_idol3`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `tracy_idol4`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `tracy_idol5`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `tracy_idol6`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `tracy_idol7`


**Definition:** A dialogue sequence and shop upgrade reward for Tracy, requiring age 5 and increasing shop level.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `tracy_introduction`


**Definition:** A sequence introducing Tracy to the player.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `begin_accepting_cats` | Enum | Specifies the character tag for the sequence that initiates accepting cats. | 1 | `beanies`<br>`butch`<br>`jack` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `tracy_kaijufight`


**Definition:** A sequence where Tracy discusses a kaiju fight.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `tracy_max1`


**Definition:** A sequence for Tracy at max favor (part 1).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `tracy_max2`


**Definition:** A sequence for Tracy at max favor (part 2).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `tracy_max3`


**Definition:** A sequence for Tracy at max favor (part 3).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `tracy_max4`


**Definition:** A sequence for Tracy at max favor (part 4).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `tracy_max5`


**Definition:** A sequence for Tracy at max favor (part 5).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `tracy_max_intro`


**Definition:** The first dialogue sequence and bonus rare item reward that plays when Tracy reaches maximum favor.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |

</details>


---


### Object: `tracy_max_repeating`


**Definition:** A repeating dialogue sequence and favor reward that plays when Tracy is at maximum favor, cycling through random sub-sequences.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `do_random_sequence` | Array | An array of sequence names; one is chosen at random to execute. | 1 ||

</details>


---


### Object: `try_again_attack_rat`


**Definition:** A tutorial sequence prompting the player to try attacking the rat again.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |
| `clear_token` | Enum | Specifies the token name to clear from the sequence's state. | 1 | `do_not_end_turn`<br>`map_equip_items2`<br>`melee_cat_spit_ignore` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `reset_turn` | Enum | Specifies whether to reset the current act's actions, both acts, or neither, upon a retry sequence. | 1 | `act`<br>`both` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |
| `wait_for` | Enum | Specifies the game action or event to wait for before continuing the sequence. | 1 | `action_selected`<br>`cat_turn`<br>`choose_cat1` |

</details>


---


### Object: `try_again_melee_move`


**Definition:** A tutorial sequence prompting the player to try a melee move again.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |
| `clear_token` | Enum | Specifies the token name to clear from the sequence's state. | 1 | `do_not_end_turn`<br>`map_equip_items2`<br>`melee_cat_spit_ignore` |
| `reset_turn` | Enum | Specifies whether to reset the current act's actions, both acts, or neither, upon a retry sequence. | 1 | `act`<br>`both` |

</details>


---


### Object: `tutorial_cat_dies`


**Definition:** A tutorial sequence explaining what happens when a cat dies.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |

</details>


---


### Object: `unprompted1`


**Definition:** An unprompted dialogue sequence from Beanies (part 1).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `unprompted2`


**Definition:** An unprompted dialogue sequence from Beanies (part 2).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `unprompted3`


**Definition:** An unprompted dialogue sequence from Beanies (part 3).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `unprompted4`


**Definition:** An unprompted dialogue sequence from Beanies (part 4).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `unprompted5`


**Definition:** An unprompted dialogue sequence from Beanies (part 5).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `unprompted6`


**Definition:** An unprompted dialogue sequence from Beanies (part 6).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |

</details>


---


### Object: `upgrade_storage_1`


**Definition:** A dialogue sequence and storage expansion reward for Butch, requiring act 0 and chapter 0.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `upgrade_storage_2`


**Definition:** A dialogue sequence and storage expansion reward for Butch, requiring act 1 and chapter 2.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `upgrade_storage_3`


**Definition:** A dialogue sequence and storage expansion reward for Butch, requiring act 1 and chapter 3.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `upgrade_storage_4`


**Definition:** A dialogue sequence and storage expansion reward for Butch, requiring act 2 and chapter 2.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `upgrade_storage_5`


**Definition:** A dialogue sequence and storage expansion reward for Butch, requiring act 2 and chapter 3.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `upgrade_storage_6`


**Definition:** A dialogue sequence and storage expansion reward for Butch, requiring act 3 and chapter 2.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `upgrade_storage_7`


**Definition:** A dialogue sequence and storage expansion reward for Butch, requiring act 3 and chapter 3.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `upgrade_storage_max1`


**Definition:** A dialogue popup for the first storage space upgrade.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |

</details>


---


### Object: `upgrade_storage_max2`


**Definition:** A dialogue popup for the second storage space upgrade, including a reward.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `upgrade_storage_max3`


**Definition:** A dialogue popup for the third storage space upgrade.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `upgrade_storage_max4`


**Definition:** A dialogue popup for the fourth storage space upgrade.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `upgrade_storage_max5`


**Definition:** A dialogue popup for the fifth storage space upgrade.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `upgrade_storage_repeating_crazy`


**Definition:** A repeating dialogue sequence for Butch's storage upgrade at crazy difficulty, granting one storage expansion.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `do_random_sequence` | Array | An array of sequence names; one is chosen at random to execute. | 1 ||

</details>


---


### Object: `upgrade_storage_repeating_hard`


**Definition:** A repeating dialogue sequence for Butch's storage upgrade at hard difficulty, granting one storage expansion.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `do_random_sequence` | Array | An array of sequence names; one is chosen at random to execute. | 1 ||

</details>


---


### Object: `upgrade_storage_repeating_impossible`


**Definition:** A repeating dialogue sequence for Butch's storage upgrade at impossible difficulty, granting one storage expansion.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `do_random_sequence` | Array | An array of sequence names; one is chosen at random to execute. | 1 ||

</details>


---


### Object: `upgrade_storage_repeating_intro`


**Definition:** The introductory dialogue sequence and reward when Butch maxes out storage capacity.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `get` | Enum | Specifies the type of result to retrieve from the sidequest (e.g., 'sidequest_fail', 'sidequest_reward', 'npc_reward'). | 1 | `npc_reward`<br>`sidequest_fail`<br>`sidequest_reward` |

</details>


---


### Object: `upgrade_storage_repeating_normal`


**Definition:** A repeating dialogue sequence for Butch's storage upgrade at normal difficulty, granting one storage expansion.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `do_random_sequence` | Array | An array of sequence names; one is chosen at random to execute. | 1 ||

</details>


---


### Object: `use_attack_after_used_weapon`


**Definition:** A tutorial sequence teaching the player to use an attack after using a weapon.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `get_token` | Enum | Specifies the name of the token to retrieve from the sequence's current state. | 1 | `can_still_use_attack`<br>`can_still_use_attack_didntspell`<br>`ranged_cat_attack` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |
| `wait_for` | Enum | Specifies the game action or event to wait for before continuing the sequence. | 1 | `action_selected`<br>`cat_turn`<br>`choose_cat1` |

</details>


---


### Object: `use_weapon`


**Definition:** Defines a dialogue option that prompts the unit to use their equipped weapon.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 1 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 1 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `get_token` | Enum | Specifies the name of the token to retrieve from the sequence's current state. | 1 | `can_still_use_attack`<br>`can_still_use_attack_didntspell`<br>`ranged_cat_attack` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |
| `wait_for` | Enum | Specifies the game action or event to wait for before continuing the sequence. | 1 | `action_selected`<br>`cat_turn`<br>`choose_cat1` |

</details>


---


### Object: `welcome`


**Definition:** A cancelable welcome sequence for Tracy's shop.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | If true, the sequence can be cancelled by the player. | 1 | `true` |
| `delay` | Float | The delay in seconds before the ability's effect triggers. | 1 | `.05`<br>`.1`<br>`.25` |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `wait_for_cancel` | Number | The number of frames to wait before the sequence is cancelled. | 1 | `1` |

</details>


---


### Object: `welcome_boneyard`


**Definition:** A cancelable welcome sequence for the boneyard biome shop.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | If true, the sequence can be cancelled by the player. | 1 | `true` |
| `delay` | Float | The delay in seconds before the ability's effect triggers. | 1 | `.05`<br>`.1`<br>`.25` |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `wait_for_cancel` | Number | The number of frames to wait before the sequence is cancelled. | 1 | `1` |

</details>


---


### Object: `welcome_bunker`


**Definition:** A cancelable welcome sequence for the bunker biome shop.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `cancelable` | Boolean | If true, the sequence can be cancelled by the player. | 1 | `true` |
| `delay` | Float | The delay in seconds before the ability's effect triggers. | 1 | `.05`<br>`.1`<br>`.25` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `wait_for_cancel` | Number | The number of frames to wait before the sequence is cancelled. | 1 | `1` |

</details>


---


### Object: `welcome_caves`


**Definition:** A cancelable welcome sequence for the caves biome shop.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | If true, the sequence can be cancelled by the player. | 1 | `true` |
| `delay` | Float | The delay in seconds before the ability's effect triggers. | 1 | `.05`<br>`.1`<br>`.25` |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `wait_for_cancel` | Number | The number of frames to wait before the sequence is cancelled. | 1 | `1` |

</details>


---


### Object: `welcome_core`


**Definition:** A cancelable welcome sequence for the core biome shop.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | If true, the sequence can be cancelled by the player. | 1 | `true` |
| `delay` | Float | The delay in seconds before the ability's effect triggers. | 1 | `.05`<br>`.1`<br>`.25` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `wait_for_cancel` | Number | The number of frames to wait before the sequence is cancelled. | 1 | `1` |

</details>


---


### Object: `welcome_crater`


**Definition:** A cancelable welcome sequence for the crater biome shop.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | If true, the sequence can be cancelled by the player. | 1 | `true` |
| `delay` | Float | The delay in seconds before the ability's effect triggers. | 1 | `.05`<br>`.1`<br>`.25` |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `wait_for_cancel` | Number | The number of frames to wait before the sequence is cancelled. | 1 | `1` |

</details>


---


### Object: `welcome_desert`


**Definition:** A cancelable welcome sequence for the desert biome shop.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | If true, the sequence can be cancelled by the player. | 1 | `true` |
| `delay` | Float | The delay in seconds before the ability's effect triggers. | 1 | `.05`<br>`.1`<br>`.25` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `wait_for_cancel` | Number | The number of frames to wait before the sequence is cancelled. | 1 | `1` |

</details>


---


### Object: `welcome_future`


**Definition:** A cancelable welcome sequence for the future biome shop.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | If true, the sequence can be cancelled by the player. | 1 | `true` |
| `delay` | Float | The delay in seconds before the ability's effect triggers. | 1 | `.05`<br>`.1`<br>`.25` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `wait_for_cancel` | Number | The number of frames to wait before the sequence is cancelled. | 1 | `1` |

</details>


---


### Object: `welcome_iceage`


**Definition:** A cancelable welcome sequence for the ice age biome shop.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | If true, the sequence can be cancelled by the player. | 1 | `true` |
| `delay` | Float | The delay in seconds before the ability's effect triggers. | 1 | `.05`<br>`.1`<br>`.25` |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `wait_for_cancel` | Number | The number of frames to wait before the sequence is cancelled. | 1 | `1` |

</details>


---


### Object: `welcome_junkyard`


**Definition:** A cancelable welcome sequence for the junkyard biome shop.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | If true, the sequence can be cancelled by the player. | 1 | `true` |
| `delay` | Float | The delay in seconds before the ability's effect triggers. | 1 | `.05`<br>`.1`<br>`.25` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `wait_for_cancel` | Number | The number of frames to wait before the sequence is cancelled. | 1 | `1` |

</details>


---


### Object: `welcome_jurassic`


**Definition:** A cancelable welcome sequence for the jurassic biome shop.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | If true, the sequence can be cancelled by the player. | 1 | `true` |
| `delay` | Float | The delay in seconds before the ability's effect triggers. | 1 | `.05`<br>`.1`<br>`.25` |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `wait_for_cancel` | Number | The number of frames to wait before the sequence is cancelled. | 1 | `1` |

</details>


---


### Object: `welcome_lab`


**Definition:** A cancelable welcome sequence for the lab biome shop.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | If true, the sequence can be cancelled by the player. | 1 | `true` |
| `delay` | Float | The delay in seconds before the ability's effect triggers. | 1 | `.05`<br>`.1`<br>`.25` |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `wait_for_cancel` | Number | The number of frames to wait before the sequence is cancelled. | 1 | `1` |

</details>


---


### Object: `welcome_moon`


**Definition:** A cancelable welcome sequence for the moon biome shop.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | If true, the sequence can be cancelled by the player. | 1 | `true` |
| `delay` | Float | The delay in seconds before the ability's effect triggers. | 1 | `.05`<br>`.1`<br>`.25` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `wait_for_cancel` | Number | The number of frames to wait before the sequence is cancelled. | 1 | `1` |

</details>


---


### Object: `welcome_sewers`


**Definition:** A cancelable welcome sequence for the sewers biome shop.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | If true, the sequence can be cancelled by the player. | 1 | `true` |
| `delay` | Float | The delay in seconds before the ability's effect triggers. | 1 | `.05`<br>`.1`<br>`.25` |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `wait_for_cancel` | Number | The number of frames to wait before the sequence is cancelled. | 1 | `1` |

</details>


---


### Object: `welcome_theend`


**Definition:** A cancelable welcome sequence for the theend biome shop, with Beanies' voice.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | If true, the sequence can be cancelled by the player. | 1 | `true` |
| `delay` | Float | The delay in seconds before the ability's effect triggers. | 1 | `.05`<br>`.1`<br>`.25` |
| `dialog` | Enum | Specifies a dialog entry or dialog tree to display. | 1 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `set_npc_voice` | Enum | Specifies which NPC's voice preset to apply for the current sequence's dialog. | 1 | `beanies` |
| `wait_for_cancel` | Number | The number of frames to wait before the sequence is cancelled. | 1 | `1` |

</details>


---


### Object: `welcome_water`


**Definition:** Defines a cancelable sequence with a 0.5-second delay, auto-passing dialog NPC_TRACY_SHOP_WELCOME_WATER_1.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | If true, the sequence can be cancelled by the player. | 1 | `true` |
| `delay` | Float | The delay in seconds before the ability's effect triggers. | 1 | `.05`<br>`.1`<br>`.25` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `wait_for_cancel` | Number | The number of frames to wait before the sequence is cancelled. | 1 | `1` |

</details>


---


### Object: `welcome_water_cheap`


**Definition:** Defines a cancelable sequence with a 0.5-second delay, auto-passing dialog NPC_TRACY_SHOP_WELCOME_WATER_CHEAP_1.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | If true, the sequence can be cancelled by the player. | 1 | `true` |
| `delay` | Float | The delay in seconds before the ability's effect triggers. | 1 | `.05`<br>`.1`<br>`.25` |
| `dialog_and_autopass` | Enum | Specifies the dialog string to display, and automatically proceeds past it. | 1 | `""`<br>`NPC_BEANIES_INTRO_15`<br>`NPC_JACK_CANT_AFFORD_1` |
| `wait_for_cancel` | Number | The number of frames to wait before the sequence is cancelled. | 1 | `1` |

</details>


---