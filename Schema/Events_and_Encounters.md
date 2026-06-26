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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 664 |  |
| [`intro`](#object-intro) | Object | Event Node: The initial text block when a story event first loads. | 239 ||
| [`main`](#object-main) | Object | Event Node: The central hub or recurring menu of a story event. | 227 ||
| [`self_damage`](Abilities_and_Spells.md#object-self_damage) | Boolean / Integer / Object | Recoil or self-inflicted damage/effects applied to the caster. | 218 ||
| `cha` | Enum / Integer |  | 89 |  |
| `con` | Enum / Integer || 79 ||
| `spd` | Enum / Integer || 78 ||
| `int` | Enum / Integer || 66 ||
| `lck` | Enum / Integer || 53 ||
| `str` | Enum / Integer || 45 ||
| [`rare`](./Events_and_Encounters.md#object-rare) | Enum | Event Node: Story branch or dialog option representing the 'Rare' action. | 34 |  |
| `dex` | Enum / Integer || 30 ||
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String || 25 ||
| `normal` | Array || 23 | `[common boneyard_events.gon]` (Array), `[common core_events.gon]` (Array) |
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 13 ||
| [`common`](./Events_and_Encounters.md#object-common) | Enum | Event Node: Story branch or dialog option representing the 'Common' action. | 11 |  |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | String || 9 ||
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String || 4 ||
| `set_frame` | `Number` || 4 ||
| [`label`](./Strings.md#string-label) | String || 3 ||
| [`stat`](./Enums.md#enum-stat) | Variable || 3 ||
| [`animation`](./Enums.md#enum-animation) | Enum || 3 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the 'Good' action. | 3 ||
| [`reward`](#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 3 ||
| [`pick`](#object-pick) | Object | Examples: `{ ... }` | 2 ||
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 1 ||
| `weight` | `Number` | Probability weight for this outcome. | 1 ||
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum || 1 ||
| `stat_max` | Number || 1 ||
| `stat_min` | Number || 1 ||
| [`open`](Characters_and_Bosses.md#object-open) | Object | Examples: `{ ... }` | 1 ||
| [`smash`](#object-smash) | Object | Examples: `{ ... }` | 1 ||
| [`conditional_reward`](#object-conditional_reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 1 ||
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 1 ||
| [`destroy`](#object-destroy) | Object | Event Node: Story branch or dialog option representing the \'Destroy\' action. | 1 ||
| [`mutation`](#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 759 ||
| [`common`](./Events_and_Encounters.md#object-common) | Enum | Event Node: Story branch or dialog option representing the 'Common' action. | 633 ||
| [`rare`](./Events_and_Encounters.md#object-rare) | Enum | Event Node: Story branch or dialog option representing the 'Rare' action. | 623 ||
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String || 70 ||
| `set_frame` | `Number` || 53 ||
| [`set_subject`](./Engine_EventKeys.md#valid-property-keys) | `String` || 10 ||
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 9 ||
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | `String` || 9 ||
| [`random_pool`](./Enums.md) | Array || 8 | [event_now] |
| [`clear_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | String || 6 ||
| `next_event_bonus` | Number || 5 ||
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | `String` || 5 ||
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Array || 4 ||
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | `String` || 3 ||
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | String || 2 ||
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | String || 2 ||
| [`gain_coins`](./Engine_EventKeys.md#valid-property-keys) | Array || 2 ||
| `ambush_next_basic_fights` | Number || 1 ||
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | String || 1 ||
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | String || 1 ||
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | String || 1 ||
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 ||
| [`party_damage`](./Enums.md) | Array / Integer || 1 | [15] |

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 634 ||
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | `String` || 606 ||
| `set_frame` | `Number` || 151 ||
| [`self_status_next_fight`](#object-self_status_next_fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 92 ||
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | `String` | Event Action: Rewards the player with an item drawn from a specific loot pool. | 66 ||
| [`permanent_stats`](#object-permanent_stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 39 ||
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Event Node: Story branch or dialog option representing the 'Damage' action. | 35 ||
| [`random_pool`](./Enums.md) | Array || 35 | [event_now] |
| [`gain_coins`](./Engine_EventKeys.md#valid-property-keys) | `Array` || 28 ||
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | `String` || 26 ||
| `self_damage` | `Number` | Recoil or self-inflicted damage/effects applied to the caster. | 26 ||
| `random_mutation` | `Number` | Event Reward: Applies a completely random mutation to a character. | 25 ||
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | `String` || 24 ||
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | `String` || 23 ||
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | `String` || 21 ||
| `gain_food` | `Number` || 21 ||
| [`spawn_unit_next_fight`](#object-spawn_unit_next_fight) | Object | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. | 18 ||
| [`gain_familiar`](./Events_and_Encounters.md#object-gain-familiar) | `String` | Event Action: Adds a specific familiar to the party. | 15 ||
| `party_heal` | `Number` || 15 ||
| `party_damage` | `Number` || 15 ||
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | `String` || 14 ||
| `heal` | `Number` || 13 ||
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | `String` || 12 ||
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | `String` || 11 ||
| [`party_status_next_fight`](#object-party_status_next_fight) | Object | Event Penalty/Reward: Applies a status effect to the entire party at the start of the next combat encounter. | 11 ||
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | `String` || 11 ||
| `ally_ambush_next_fights` | `Number` || 10 ||
| `full_heal` | `Number` || 10 ||
| `ambush_next_basic_fights` | `Number` || 9 ||
| [`conditional_reward`](#object-conditional_reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 9 ||
| [`random_mutation_from_set`](#object-random_mutation_from_set) | Object | Event Reward: Applies a random mutation to a character from a specific pool. | 8 ||
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | `String` || 7 ||
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | `String` || 7 ||
| `next_event_bonus` | `Number` || 7 ||
| [`clear_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | `String` || 6 ||
| [`global_effect_next_fight`](#object-global_effect_next_fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 6 ||
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | `String` || 6 ||
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | `String` || 5 ||
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | `String` || 5 ||
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | `String` || 5 ||
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | `String` || 4 ||
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | `String` || 2 ||
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | `String` || 2 ||
| [`next_event_from_set`](#object-next_event_from_set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 2 ||
| `party_heal_disorder` | `Number` || 2 ||
| [`party_permanent_stats_exclude_self`](#object-party_permanent_stats_exclude_self) | Object | Event Reward: Permanently modifies stats for all party members except the one who initiated the action. | 2 ||
| [`spin`](./Engine_EventKeys.md#valid-property-keys) | `String` || 2 ||
| `clear_result_animation` | `Number` || 1 ||
| [`decrement_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 ||
| [`get_and_equip_item`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 ||
| `heal_disorder` | `Number` || 1 ||
| `heal_injury` | `Number` || 1 ||
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 ||
| [`mutation`](#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 1 ||
| `self_heal` | `Number` || 1 ||
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 ||
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 634 ||
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | `String` || 611 ||
| `set_frame` | `Number` || 180 ||
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | `String` | Event Action: Rewards the player with an item drawn from a specific loot pool. | 84 ||
| [`permanent_stats`](#object-permanent_stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 84 ||
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | `String` || 65 ||
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | `String` || 46 ||
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | `String` || 45 ||
| [`self_status_next_fight`](#object-self_status_next_fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 40 ||
| `random_mutation` | `Number` | Event Reward: Applies a completely random mutation to a character. | 38 ||
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | `String` || 35 ||
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | `String` || 30 ||
| [`random_pool`](./Enums.md) | Array || 28 | [event_now] |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | `String` || 26 ||
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | `String` || 21 ||
| [`spawn_unit_next_fight`](#object-spawn_unit_next_fight) | Object | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. | 20 ||
| [`conditional_reward`](#object-conditional_reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 18 ||
| [`mutation`](#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 18 ||
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Event Node: Story branch or dialog option representing the 'Damage' action. | 18 ||
| [`gain_coins`](./Engine_EventKeys.md#valid-property-keys) | `Array` || 17 ||
| [`gain_familiar`](./Events_and_Encounters.md#object-gain-familiar) | `String` | Event Action: Adds a specific familiar to the party. | 15 ||
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | `String` || 14 ||
| `next_event_bonus` | `Number` || 14 ||
| `self_damage` | `Number` | Recoil or self-inflicted damage/effects applied to the caster. | 13 ||
| [`party_status_next_fight`](#object-party_status_next_fight) | Object | Event Penalty/Reward: Applies a status effect to the entire party at the start of the next combat encounter. | 12 ||
| [`random_mutation_from_set`](#object-random_mutation_from_set) | Object | Event Reward: Applies a random mutation to a character from a specific pool. | 11 ||
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | `Array` || 11 ||
| [`learn_passive`](./Engine_EventKeys.md#valid-property-keys) | `String` || 10 ||
| `party_heal` | `Number` || 10 ||
| `party_damage` | `Number` || 10 ||
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | `String` || 9 ||
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | `String` || 8 ||
| `party_random_mutation` | `Number` || 8 ||
| `ambush_next_basic_fights` | `Number` || 7 ||
| [`leave_party_temporarily`](#object-leave_party_temporarily) | Object | Event Action: Removes a character from the active team until the next hub area. | 7 ||
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | `String` || 7 ||
| `hide_appearance_changes` | `Number` || 6 ||
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | `String` || 6 ||
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | `Array` || 6 ||
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | `String` || 5 ||
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | `String` || 5 ||
| `ally_ambush_next_fights` | `Number` || 5 ||
| `full_heal` | `Number` || 4 ||
| [`learn_ability`](./Engine_EventKeys.md#valid-property-keys) | `String` || 4 ||
| [`decrement_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | `String` || 3 ||
| `gain_cat_familiar` | `Number` || 3 ||
| [`global_effect_next_fight`](#object-global_effect_next_fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 3 ||
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | `String` || 3 ||
| [`make_old`](./Engine_EventKeys.md#valid-property-keys) | `String` || 3 ||
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | `String` | Event Action: Chains immediately into a randomly selected subsequent story event. | 3 ||
| `spawn_reflection_next_fight` | `Number` | Event Penalty: Spawns dark clones/reflections of the party in the next combat encounter. | 3 ||
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | `String` || 2 ||
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | `String` || 2 ||
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | `String` || 2 ||
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | `String` || 2 ||
| `party_heal_disorder` | `Number` || 2 ||
| `party_heal_injury` | `Number` || 2 ||
| [`party_permanent_stats_exclude_self`](#object-party_permanent_stats_exclude_self) | Object | Event Reward: Permanently modifies stats for all party members except the one who initiated the action. | 2 ||
| `set_age` | `Number` || 2 ||
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | `String` || 2 ||
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | `String` || 2 ||
| [`lose_item_from_inventory`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 ||
| [`ambush`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 ||
| `clear_result_animation` | `Number` || 1 ||
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 ||
| [`get_and_equip_item`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 ||
| `heal_disorder` | `Number` || 1 ||
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 ||
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 ||
| [`lose_all_equipped_items`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 ||
| [`party_injury`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 ||
| [`party_permanent_stats`](#object-party_permanent_stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of all party members. | 1 ||
| [`party_random_mutation_from_set`](#object-party_random_mutation_from_set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 1 ||
| [`play_result_animation`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 ||
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 ||
| [`scramble_basic_attack`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 ||
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 545 ||
| [`reward`](#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 326 ||
| `set_frame` | `Number` || 285 ||
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String || 184 ||
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | String || 111 ||
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | `String` || 21 ||
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | `String` | Event Node: Triggers a narrative cutscene. | 19 ||
| [`conditional_reward`](#object-conditional_reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 14 ||
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | `String` || 12 ||
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | `String` || 12 ||
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 12 ||
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | `String` || 12 ||
| [`rare`](./Events_and_Encounters.md#object-rare) | Enum | Event Node: Story branch or dialog option representing the 'Rare' action. | 10 ||
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | String || 9 ||
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | String || 9 ||
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | String || 8 ||
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | String || 7 ||
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | `String` || 7 ||
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | String || 6 ||
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | String || 6 ||
| [`random_pool`](./Enums.md) | Array || 5 | [event_now] |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | String || 4 ||
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 4 ||
| [`mutation`](#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 4 ||
| [`random_pool_consider_luck`](./Enums.md) | Array || 4 | [Clover] |
| `heal_disorder` | Number || 3 ||
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | String || 3 ||
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | String || 3 ||
| `heal_injury` | `Number` || 3 ||
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | String || 3 ||
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | `String` || 3 ||
| [`transform_item`](./Enums.md) | Array || 3 | [JarOfRadiatedBlood] |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | String || 2 ||
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | `String` || 2 ||
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | String || 2 ||
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String || 2 ||
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | String || 2 ||
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | String || 2 ||
| [`party_gain_disorder_from_pool`](./Enums.md) | Array || 2 | [Gigantism] |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | String || 1 ||
| `ally_ambush_next_fights` | Number || 1 ||
| `clone_self_to_party` | `Number` || 1 ||
| `copy_items_to_party` | `Number` || 1 ||
| `copy_party_items` | `Number` || 1 ||
| [`gain_clone_familiar`](#object-gain_clone_familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 1 ||
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 ||
| [`global_effect_next_fight`](#object-global_effect_next_fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 1 ||
| `heal` | `Number` || 1 ||
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | String || 1 ||
| `next_event_bonus` | Number || 1 ||
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | String | Event Action: Chains immediately into a randomly selected subsequent story event. | 1 ||
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 ||
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 ||
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 ||
| `trigger_butterfly_effect` | `Number` || 1 ||
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 ||
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 339 ||
| [`reward`](#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 305 ||
| `set_frame` | `Number` || 222 ||
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String || 38 ||
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | String || 10 ||
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | `String` || 4 ||
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | String || 4 ||
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | `String` || 4 ||
| [`self_status_next_fight`](#object-self_status_next_fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 4 ||
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 3 ||
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | String || 3 ||
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | `String` || 3 ||
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | String || 3 ||
| [`conditional_reward`](#object-conditional_reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 2 ||
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | String || 2 ||
| `next_event_bonus` | Number || 2 ||
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 ||
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 ||
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 ||
| [`party_random_mutation_from_set`](#object-party_random_mutation_from_set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 1 ||
| [`permanent_stats`](#object-permanent_stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 1 ||
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 ||
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 ||

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
| [`cat_choice`](./Enums.md#enum-cat_choice) | Enum || 214 ||
| [`event_clip`](./Enums.md#enum-event_clip) | Enum || 214 ||
| [`subject_clip`](./Enums.md#enum-subject_clip) | Enum || 214 ||
| [`subject_frame`](./Enums.md#enum-subject_frame) | Enum || 214 ||
| [`title`](./Strings.md#string-title) | String || 214 ||
| [`choose_cat_with_item`](./Enums.md#enum-choose_cat_with_item) | Enum || 17 ||
| `different_from_last_x_cats` | Number || 3 ||
| `subject_frame_inner` | Number || 3 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`choose_cat_with_highest_stat`](./Math_Equations.md) | Equation || 1 ||
| [`choose_cat_with_item_slot_equipped`](./Enums.md#enum-choose_cat_with_item_slot_equipped) | Enum || 1 ||
| `choose_cat_with_min_health` | Number || 1 ||
| `choose_cat_with_most_injuries` | Boolean || 1 ||
| `choose_cat_with_parasite` | Boolean || 1 ||
| `set_frame` | `Number` || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 214 ||
| [`options`](./Events_and_Encounters.md#object-options) | Array | Event Object: Lists the available clickable dialog choices for the current story node. | 210 ||
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String || 203 ||
| [`setup`](#object-setup) | Object | Event Object: Pre-initialization logic executed before the event UI is drawn. | 23 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 4 ||
| [`goto`](./Engine_EventKeys.md#valid-property-keys) | `String` || 4 ||
| [`outcome`](#object-outcome) | Object | Event Object: Logic and text executed after selecting a specific dialog option. | 4 ||
| `max_options` | `Number` || 3 ||
| `shuffle_options` | `Boolean` || 3 ||
| [`leave`](Engine_LogicKeys.md#object-leave) | Object | Event Node: Story branch or dialog option representing the 'Leave' action. | 3 ||
| [`ignore`](#object-ignore) | Object || 2 ||
| [`open`](Characters_and_Bosses.md#object-open) | Object || 2 ||
| [`buy2`](#object-buy2) | Object || 1 ||
| [`buy3`](#object-buy3) | Object || 1 ||
| [`examine`](#object-examine) | Object || 1 ||
| [`pick`](#object-pick) | Object || 1 ||

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
| [`ignore`](#object-ignore) | Object | Event Node: Story branch or dialog option representing the \'Ignore\' action. | 55 ||
| [`examine`](#object-examine) | Object | Event Node: Story branch or dialog option representing the \'Examine\' action. | 43 ||
| [`leave`](Engine_LogicKeys.md#object-leave) | Object | Event Node: Story branch or dialog option representing the 'Leave' action. | 29 ||
| [`loot`](#object-loot) | Object | Event Node: Story branch or dialog option representing the \'Loot\' action. | 25 ||
| [`eat`](#object-eat) | Object | Event Node: Story branch or dialog option representing the \'Eat\' action. | 23 ||
| [`smash`](#object-smash) | Object | Event Node: Story branch or dialog option representing the \'Smash\' action. | 15 ||
| [`destroy`](#object-destroy) | Object | Event Node: Story branch or dialog option representing the \'Destroy\' action. | 13 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 12 ||
| [`bash`](#object-bash) | Object | Event Node: Story branch or dialog option representing the \'Bash\' action. | 12 ||
| [`sneak`](#object-sneak) | Object | Event Node: Story branch or dialog option representing the \'Sneak\' action. | 11 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 10 ||
| [`open`](Characters_and_Bosses.md#object-open) | Object | Event Node: Story branch or dialog option representing the \'Open\' action. | 8 ||
| [`take`](#object-take) | Object | Event Node: Story branch or dialog option representing the \'Take\' action. | 8 ||
| [`a`](#object-a) | Object | Event Node: Story branch or dialog option representing the \'A\' action. | 7 ||
| [`attack`](./Events_and_Encounters.md#context-attack) | Enum | Event Node: Story branch or dialog option representing the \'Attack\' action. | 7 ||
| [`b`](#object-b) | Object | Event Node: Story branch or dialog option representing the \'B\' action. | 7 ||
| [`c`](#object-c) | Object | Event Node: Story branch or dialog option representing the \'C\' action. | 7 ||
| [`charm`](#object-charm) | Object | Event Node: Story branch or dialog option representing the \'Charm\' action. | 7 ||
| [`fight`](#object-fight) | Object | Event Node: Story branch or dialog option representing the \'Fight\' action. | 7 ||
| [`touch`](#object-touch) | Object | Event Node: Story branch or dialog option representing the \'Touch\' action. | 7 ||
| [`activate_p`](#object-activate_p) | Object | Event Node: Story branch or dialog option representing the 'Activate P' action. | 6 ||
| [`activate_z`](#object-activate_z) | Object | Event Node: Story branch or dialog option representing the 'Activate Z' action. | 6 ||
| [`d`](#object-d) | Object | Event Node: Story branch or dialog option representing the \'D\' action. | 6 ||
| [`enter`](#object-enter) | Object | Event Node: Story branch or dialog option representing the \'Enter\' action. | 6 ||
| [`inspect`](#object-inspect) | Object | Event Node: Story branch or dialog option representing the \'Inspect\' action. | 6 ||
| [`lick`](#object-lick) | Object | Event Node: Story branch or dialog option representing the \'Lick\' action. | 6 ||
| [`drink`](#object-drink) | Object | Event Node: Story branch or dialog option representing the \'Drink\' action. | 5 ||
| [`kiss`](#object-kiss) | Object | Event Node: Story branch or dialog option representing the \'Kiss\' action. | 5 ||
| [`run`](#object-run) | Object | Event Node: Story branch or dialog option representing the \'Run\' action. | 5 ||
| [`bite`](#object-bite) | Object | Event Node: Story branch or dialog option representing the 'Bite' action. | 4 ||
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Event Node: Story branch or dialog option representing the 'Damage' action. | 4 ||
| [`go_around`](#object-go_around) | Object | Event Node: Story branch or dialog option representing the \'Go Around\' action. | 4 ||
| [`home`](#object-home) | Object | Event Node: Story branch or dialog option representing the 'Home' action. | 4 ||
| [`past`](#object-past) | Object | Event Node: Story branch or dialog option representing the 'Past' action. | 4 ||
| [`skip`](#object-skip) | Object | Event Node: Story branch or dialog option representing the \'Skip\' action. | 4 ||
| [`investigate`](#object-investigate) | Object | Event Node: Story branch or dialog option representing the \'Investigate\' action. | 3 ||
| [`repell`](#object-repell) | Object | Event Node: Story branch or dialog option representing the \'Repell\' action. | 3 ||
| [`attach_antenna`](#object-attach_antenna) | Object | Event Node: Story branch or dialog option representing the 'Attach Antenna' action. | 2 ||
| [`boogers`](#object-boogers) | Object | Event Node: Story branch or dialog option representing the \'Boogers\' action. | 2 ||
| [`copy`](#object-copy) | Object | Event Node: Story branch or dialog option representing the \'Copy\' action. | 2 ||
| [`find_another_way`](#object-find_another_way) | Object | Event Node: Story branch or dialog option representing the \'Find Another Way\' action. | 2 ||
| [`move_closer`](#object-move_closer) | Object | Event Node: Story branch or dialog option representing the \'Move Closer\' action. | 2 ||
| [`play`](#object-play) | Object | Event Node: Story branch or dialog option representing the \'Play\' action. | 2 ||
| [`poop`](#object-poop) | Object | Event Node: Story branch or dialog option representing the \'Poop\' action. | 2 ||
| [`print`](#object-print) | Object | Event Node: Story branch or dialog option representing the \'Print\' action. | 2 ||
| [`protection`](#object-protection) | Object | Event Node: Story branch or dialog option representing the \'Protection\' action. | 2 ||
| [`repair`](#object-repair) | Object | Event Node: Story branch or dialog option representing the \'Repair\' action. | 2 ||
| [`sacrifice`](#object-sacrifice) | Object | Event Node: Story branch or dialog option representing the \'Sacrifice\' action. | 2 ||
| [`scale`](./Events_and_Encounters.md#context-scale) | Number | Event Node: Story branch or dialog option representing the \'Scale\' action. | 2 ||
| [`turnon`](#object-turnon) | Object | Event Node: Story branch or dialog option representing the \'Turnon\' action. | 2 ||
| [`altar_sacrifice`](#object-altar_sacrifice) | Object | Event Action: Triggers the altar sacrifice progression logic. | 1 ||
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum || 1 ||
| [`arm`](#object-arm) | Object | Event Node: Story branch or dialog option representing the \'Arm\' action. | 1 ||
| [`attach_amplifier`](#object-attach_amplifier) | Object | Event Node: Story branch or dialog option representing the 'Attach Amplifier' action. | 1 ||
| [`attach_leech`](#object-attach_leech) | Object | Event Node: Story branch or dialog option representing the 'Attach Leech' action. | 1 ||
| [`bash_past_alt`](#object-bash_past_alt) | Object | Event Node: Story branch or dialog option representing the \'Bash Past Alt\' action. | 1 ||
| [`bite_it_off`](#object-bite_it_off) | Object | Event Node: Story branch or dialog option representing the \'Bite It Off\' action. | 1 ||
| [`blue`](#object-blue) | Object | Event Node: Story branch or dialog option representing the \'Blue\' action. | 1 ||
| [`blue_needle`](#object-blue_needle) | Object | Event Node: Story branch or dialog option representing the \'Blue Needle\' action. | 1 ||
| [`body`](./Events_and_Encounters.md#context-body) | Number | Event Node: Story branch or dialog option representing the 'Body' action. | 1 ||
| [`book`](#object-book) | Object | Event Node: Story branch or dialog option representing the \'Book\' action. | 1 ||
| [`brace`](#object-brace) | Object | Event Node: Story branch or dialog option representing the \'Brace\' action. | 1 ||
| [`break_ice`](#object-break_ice) | Object | Event Node: Story branch or dialog option representing the \'Break Ice\' action. | 1 ||
| [`break_lock`](#object-break_lock) | Object | Event Node: Story branch or dialog option representing the \'Break Lock\' action. | 1 ||
| [`bribe`](#object-bribe) | Object | Event Node: Story branch or dialog option representing the 'Bribe' action. | 1 ||
| [`button`](#object-button) | Object | Event Node: Story branch or dialog option representing the \'Button\' action. | 1 ||
| [`buy1`](#object-buy1) | Object | Event Node: Story branch or dialog option representing the \'Buy1\' action. | 1 ||
| [`catch`](#object-catch) | Object | Event Node: Story branch or dialog option representing the \'Catch\' action. | 1 ||
| [`challenge_to_game`](#object-challenge_to_game) | Object | Event Node: Story branch or dialog option representing the \'Challenge To Game\' action. | 1 ||
| [`chaos_ending`](#object-chaos_ending) | Object | Event Node: Triggers the Chaos Boss victory sequence. | 1 ||
| [`chapter_cutscene`](#object-chapter_cutscene) | Object | Event Node: Triggers an intermission cutscene. | 1 ||
| [`charm_past_alt`](#object-charm_past_alt) | Object | Event Node: Story branch or dialog option representing the \'Charm Past Alt\' action. | 1 ||
| [`climb`](#object-climb) | Object | Event Node: Story branch or dialog option representing the \'Climb\' action. | 1 ||
| [`comfort`](Engine_LogicKeys.md#object-comfort) | Object | Event Node: Story branch or dialog option representing the \'Comfort\' action. | 1 ||
| [`communicate`](#object-communicate) | Object | Event Node: Story branch or dialog option representing the \'Communicate\' action. | 1 ||
| [`concheck`](#object-concheck) | Object | Event Node: Stat check branch evaluating the \'con\' attribute. | 1 ||
| [`counter`](#object-counter) | Object | Event Node: Story branch or dialog option representing the \'Counter\' action. | 1 ||
| [`crack_open`](#object-crack_open) | Object | Event Node: Story branch or dialog option representing the \'Crack Open\' action. | 1 ||
| [`cross`](#object-cross) | Object | Event Node: Story branch or dialog option representing the \'Cross\' action. | 1 ||
| [`cut_wires`](#object-cut_wires) | Object | Event Node: Story branch or dialog option representing the \'Cut Wires\' action. | 1 ||
| [`damage_1`](#object-damage_1) | Object | Event Node: Story branch or dialog option representing the \'Damage 1\' action. | 1 ||
| [`damage_full`](#object-damage_full) | Object | Event Node: Story branch or dialog option representing the \'Damage Full\' action. | 1 ||
| [`damage_half`](#object-damage_half) | Object | Event Node: Story branch or dialog option representing the \'Damage Half\' action. | 1 ||
| [`desert_cutscene`](#object-desert_cutscene) | Object | Event Node: Triggers the desert transition cutscene. | 1 ||
| [`dexcheck`](#object-dexcheck) | Object | Event Node: Stat check branch evaluating the \'dex\' attribute. | 1 ||
| [`dig`](#object-dig) | Object | Event Node: Story branch or dialog option representing the \'Dig\' action. | 1 ||
| [`disarm`](#object-disarm) | Object | Event Node: Story branch or dialog option representing the \'Disarm\' action. | 1 ||
| [`dive`](#object-dive) | Object | Event Node: Story branch or dialog option representing the \'Dive\' action. | 1 ||
| [`donate`](#object-donate) | Object | Event Node: Story branch or dialog option representing the \'Donate\' action. | 1 ||
| [`donate_10`](#object-donate_10) | Object | Event Node: Story branch or dialog option representing the \'Donate 10\' action. | 1 ||
| [`donate_15`](#object-donate_15) | Object | Event Node: Story branch or dialog option representing the \'Donate 15\' action. | 1 ||
| [`donate_20`](#object-donate_20) | Object | Event Node: Story branch or dialog option representing the \'Donate 20\' action. | 1 ||
| [`donate_5`](#object-donate_5) | Object | Event Node: Story branch or dialog option representing the \'Donate 5\' action. | 1 ||
| [`double`](#object-double) | Object | Event Node: Story branch or dialog option representing the \'Double\' action. | 1 ||
| [`eat_meat`](#object-eat_meat) | Object | Event Node: Story branch or dialog option representing the \'Eat Meat\' action. | 1 ||
| [`enter_crater`](#object-enter_crater) | Object | Event Node: Story branch or dialog option representing the \'Enter Crater\' action. | 1 ||
| [`face`](./Events_and_Encounters.md#context-face) | Enum | Event Node: Story branch or dialog option representing the \'Face\' action. | 1 ||
| [`fiddle`](#object-fiddle) | Object | Event Node: Story branch or dialog option representing the 'Fiddle' action. | 1 ||
| [`fill_jar`](#object-fill_jar) | Object | Event Node: Story branch or dialog option representing the 'Fill Jar' action. | 1 ||
| [`find`](#object-find) | Object | Event Node: Story branch or dialog option representing the \'Find\' action. | 1 ||
| [`fire`](Characters_and_Bosses.md#object-fire) | Object | Event Node: Story branch or dialog option representing the \'Fire\' action. | 1 ||
| [`flush_yourself`](#object-flush_yourself) | Object | Event Node: Story branch or dialog option representing the \'Flush Yourself\' action. | 1 ||
| [`follow`](#object-follow) | Object | Event Node: Story branch or dialog option representing the \'Follow\' action. | 1 ||
| [`free`](#object-free) | Object | Event Node: Story branch or dialog option representing the \'Free\' action. | 1 ||
| [`future`](#object-future) | Object | Event Node: Story branch or dialog option representing the 'Future' action. | 1 ||
| [`give_parasite`](#object-give_parasite) | Object | Event Action: Equips a parasite item to a character. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the 'Good' action. | 1 ||
| [`hack`](#object-hack) | Object | Event Node: Story branch or dialog option representing the \'Hack\' action. | 1 ||
| [`head`](./Events_and_Encounters.md#context-head) | Enum / Number | Event Node: Story branch or dialog option representing the \'Head\' action. | 1 ||
| [`holy`](Characters_and_Bosses.md#object-holy) | Object | Event Node: Story branch or dialog option representing the \'Holy\' action. | 1 ||
| [`hp`](#object-hp) | Object | Event Node: Story branch or dialog option representing the \'Hp\' action. | 1 ||
| [`ice`](Engine_LogicKeys.md#object-ice) | Object | Event Node: Story branch or dialog option representing the \'Ice\' action. | 1 ||
| [`infinite`](#object-infinite) | Object | Event Node: A looping or endlessly repeating story branch. | 1 ||
| [`intcheck`](#object-intcheck) | Object | Event Node: Stat check branch evaluating the \'int\' attribute. | 1 ||
| [`intimidation`](#object-intimidation) | Object | Event Node: Story branch or dialog option representing the \'Intimidation\' action. | 1 ||
| [`itchies`](#object-itchies) | Object | Event Node: Story branch or dialog option representing the \'Itchies\' action. | 1 ||
| [`join`](#object-join) | Object | Event Node: Story branch or dialog option representing the \'Join\' action. | 1 ||
| [`jump`](#object-jump) | Object | Event Node: Story branch or dialog option representing the \'Jump\' action. | 1 ||
| [`jump_over`](#object-jump_over) | Object | Event Node: Story branch or dialog option representing the \'Jump Over\' action. | 1 ||
| [`keep_going`](#object-keep_going) | Object | Event Node: Story branch or dialog option representing the \'Keep Going\' action. | 1 ||
| [`kiss_meat`](#object-kiss_meat) | Object | Event Node: Story branch or dialog option representing the \'Kiss Meat\' action. | 1 ||
| [`knife`](#object-knife) | Object | Event Node: Story branch or dialog option representing the \'Knife\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`leave_it_in`](#object-leave_it_in) | Object | Event Node: Story branch or dialog option representing the \'Leave It In\' action. | 1 ||
| [`leg`](#object-leg) | Object | Event Node: Story branch or dialog option representing the \'Leg\' action. | 1 ||
| [`lever`](#object-lever) | Object | Event Node: Story branch or dialog option representing the \'Lever\' action. | 1 ||
| [`lick_alt`](#object-lick_alt) | Object | Event Node: Story branch or dialog option representing the \'Lick Alt\' action. | 1 ||
| [`lightning`](#object-lightning) | Object | Event Node: Story branch or dialog option representing the \'Lightning\' action. | 1 ||
| [`listen`](#object-listen) | Object | Event Node: Story branch or dialog option representing the \'Listen\' action. | 1 ||
| [`looks`](#object-looks) | Object | Event Node: Story branch or dialog option representing the 'Looks' action. | 1 ||
| [`loot_heart`](#object-loot_heart) | Object | Event Node: Story branch or dialog option representing the 'Loot Heart' action. | 1 ||
| [`makeup`](#object-makeup) | Object | Event Node: Story branch or dialog option representing the \'Makeup\' action. | 1 ||
| [`mind`](#object-mind) | Object | Event Node: Story branch or dialog option representing the 'Mind' action. | 1 ||
| [`neck`](./Events_and_Encounters.md#context-neck) | Enum | Event Node: Story branch or dialog option representing the \'Neck\' action. | 1 ||
| [`nothanks`](#object-nothanks) | Object | Event Node: Story branch or dialog option representing the \'Nothanks\' action. | 1 ||
| [`outsmart`](#object-outsmart) | Object | Event Node: Story branch or dialog option representing the \'Outsmart\' action. | 1 ||
| [`patch_up`](#object-patch_up) | Object | Event Node: Story branch or dialog option representing the \'Patch Up\' action. | 1 ||
| [`pick_lock`](#object-pick_lock) | Object | Event Node: Story branch or dialog option representing the \'Pick Lock\' action. | 1 ||
| [`pilfer`](#object-pilfer) | Object | Event Node: Story branch or dialog option representing the \'Pilfer\' action. | 1 ||
| [`pirouette`](#object-pirouette) | Object | Event Node: Story branch or dialog option representing the \'Pirouette\' action. | 1 ||
| [`place_gristle`](#object-place_gristle) | Object | Event Node: Story branch or dialog option representing the 'Place Gristle' action. | 1 ||
| [`power`](#object-power) | Object | Event Node: Story branch or dialog option representing the 'Power' action. | 1 ||
| [`pull`](#object-pull) | Object | Event Node: Story branch or dialog option representing the \'Pull\' action. | 1 ||
| [`pull_it_out`](#object-pull_it_out) | Object | Event Node: Story branch or dialog option representing the \'Pull It Out\' action. | 1 ||
| [`pull_lever`](#object-pull_lever) | Object | Event Node: Story branch or dialog option representing the \'Pull Lever\' action. | 1 ||
| [`purify`](#object-purify) | Object | Event Node: Story branch or dialog option representing the \'Purify\' action. | 1 ||
| [`push_buttons`](#object-push_buttons) | Object | Event Node: Story branch or dialog option representing the \'Push Buttons\' action. | 1 ||
| [`push_through`](#object-push_through) | Object | Event Node: Story branch or dialog option representing the \'Push Through\' action. | 1 ||
| [`put_in_coins`](#object-put_in_coins) | Object | Event Node: Story branch or dialog option representing the \'Put In Coins\' action. | 1 ||
| [`put_out_of_misery`](#object-put_out_of_misery) | Object | Event Node: Story branch or dialog option representing the \'Put Out Of Misery\' action. | 1 ||
| [`reach_inside`](#object-reach_inside) | Object | Event Node: Story branch or dialog option representing the \'Reach Inside\' action. | 1 ||
| [`read`](#object-read) | Object | Event Node: Story branch or dialog option representing the \'Read\' action. | 1 ||
| [`receive`](#object-receive) | Object | Event Node: Story branch or dialog option representing the \'Receive\' action. | 1 ||
| [`red`](#object-red) | Object | Event Node: Story branch or dialog option representing the \'Red\' action. | 1 ||
| [`red_needle`](#object-red_needle) | Object | Event Node: Story branch or dialog option representing the \'Red Needle\' action. | 1 ||
| [`reflect`](Engine_StatusAndPassiveKeys.md#object-reflect) | Object | Event Node: Story branch or dialog option representing the \'Reflect\' action. | 1 ||
| [`remove`](#object-remove) | Object | Event Node: Story branch or dialog option representing the \'Remove\' action. | 1 ||
| [`remove_the_nail`](#object-remove_the_nail) | Object | Event Node: Story branch or dialog option representing the \'Remove The Nail\' action. | 1 ||
| [`repair_quest`](#object-repair_quest) | Object | Event Node: Story branch or dialog option representing the 'Repair Quest' action. | 1 ||
| [`rest`](#object-rest) | Object | Event Node: Story branch or dialog option representing the \'Rest\' action. | 1 ||
| [`revive`](Engine_StatusAndPassiveKeys.md#object-revive) | Object | Event Node: Story branch or dialog option representing the \'Revive\' action. | 1 ||
| [`rub`](#object-rub) | Object | Event Node: Story branch or dialog option representing the \'Rub\' action. | 1 ||
| [`run_again`](#object-run_again) | Object | Event Node: Story branch or dialog option representing the \'Run Again\' action. | 1 ||
| [`run_away`](#object-run_away) | Object | Event Node: Story branch or dialog option representing the \'Run Away\' action. | 1 ||
| [`sacrifice_full_favor`](#object-sacrifice_full_favor) | Object | Event Node: Story branch or dialog option representing the \'Sacrifice Full Favor\' action. | 1 ||
| [`sacrifice_normal`](#object-sacrifice_normal) | Object | Event Node: Story branch or dialog option representing the 'Sacrifice Normal' action. | 1 ||
| [`sacrifice_partial_favor`](#object-sacrifice_partial_favor) | Object | Event Node: Story branch or dialog option representing the \'Sacrifice Partial Favor\' action. | 1 ||
| [`sacrifice_quest`](#object-sacrifice_quest) | Object | Event Node: Story branch or dialog option representing the 'Sacrifice Quest' action. | 1 ||
| [`scream`](#object-scream) | Object | Event Node: Story branch or dialog option representing the \'Scream\' action. | 1 ||
| [`shake`](#object-shake) | Object | Event Node: Story branch or dialog option representing the \'Shake\' action. | 1 ||
| [`slip_through`](#object-slip_through) | Object | Event Node: Story branch or dialog option representing the \'Slip Through\' action. | 1 ||
| [`sneak_by`](#object-sneak_by) | Object | Event Node: Story branch or dialog option representing the \'Sneak By\' action. | 1 ||
| [`sneak_past_alt`](#object-sneak_past_alt) | Object | Event Node: Story branch or dialog option representing the \'Sneak Past Alt\' action. | 1 ||
| [`soul`](#object-soul) | Object | Event Node: Story branch or dialog option representing the 'Soul' action. | 1 ||
| [`speed`](./Events_and_Encounters.md#context-speed) | Array / Number | Event Node: Story branch or dialog option representing the \'Speed\' action. | 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||
| `stat_max` | Number || 1 ||
| `stat_min` | Number || 1 ||
| [`surprise`](#object-surprise) | Object | Event Node: Story branch or dialog option representing the \'Surprise\' action. | 1 ||
| [`sweet_talk`](#object-sweet_talk) | Object | Event Node: Story branch or dialog option representing the \'Sweet Talk\' action. | 1 ||
| [`swim`](#object-swim) | Object | Event Node: Story branch or dialog option representing the \'Swim\' action. | 1 ||
| [`tail`](./Events_and_Encounters.md#context-tail) | Integer | Event Node: Story branch or dialog option representing the \'Tail\' action. | 1 ||
| [`take_blood`](#object-take_blood) | Object | Event Node: Story branch or dialog option representing the 'Take Blood' action. | 1 ||
| [`talk`](#object-talk) | Object | Event Node: Story branch or dialog option representing the 'Talk' action. | 1 ||
| [`talk_to`](#object-talk_to) | Object | Event Node: Story branch or dialog option representing the \'Talk To\' action. | 1 ||
| [`tappytoes`](#object-tappytoes) | Object | Event Node: Story branch or dialog option representing the \'Tappytoes\' action. | 1 ||
| [`teleport`](#object-teleport) | Object | Event Node: Story branch or dialog option representing the \'Teleport\' action. | 1 ||
| [`thorns`](#object-thorns) | Object | Event Node: Story branch or dialog option representing the \'Thorns\' action. | 1 ||
| [`throw`](#object-throw) | Object | Event Node: Story branch or dialog option representing the \'Throw\' action. | 1 ||
| [`timemachine`](#object-timemachine) | Object | Event Node: Story branch or dialog option representing the \'Timemachine\' action. | 1 ||
| [`traverse`](#object-traverse) | Object | Event Node: Story branch or dialog option representing the \'Traverse\' action. | 1 ||
| [`upgrade_yourself`](#object-upgrade_yourself) | Object | Event Reward: Upgrades an existing ability or item. | 1 ||
| [`use_item`](#object-use_item) | Object | Event Requirement: Requires the player to consume a specific item to proceed. | 1 ||
| [`use_toilet_con`](#object-use_toilet_con) | Object | Event Node: Story branch or dialog option representing the \'Use Toilet Con\' action. | 1 ||
| [`use_toilet_str`](#object-use_toilet_str) | Object | Event Node: Story branch or dialog option representing the \'Use Toilet Str\' action. | 1 ||
| [`use_weapon`](#object-use_weapon) | Object | Event Requirement: Uses the properties of the equipped weapon to resolve an outcome. | 1 ||
| [`w1`](#object-w1) | Object | Event Node: Story branch or dialog option representing the \'W1\' action. | 1 ||
| [`w2`](#object-w2) | Object | Event Node: Story branch or dialog option representing the \'W2\' action. | 1 ||
| [`w3`](#object-w3) | Object | Event Node: Story branch or dialog option representing the \'W3\' action. | 1 ||
| [`w4`](#object-w4) | Object | Event Node: Story branch or dialog option representing the \'W4\' action. | 1 ||
| [`w5`](#object-w5) | Object | Event Node: Story branch or dialog option representing the \'W5\' action. | 1 ||
| [`w6`](#object-w6) | Object | Event Node: Story branch or dialog option representing the \'W6\' action. | 1 ||
| [`wealth`](#object-wealth) | Object | Event Node: Story branch or dialog option representing the 'Wealth' action. | 1 ||
| [`wheezies`](#object-wheezies) | Object | Event Node: Story branch or dialog option representing the \'Wheezies\' action. | 1 ||
| [`wish_genes`](#object-wish_genes) | Object | Event Node: Story branch or dialog option representing the \'Wish Genes\' action. | 1 ||
| [`wish_items`](#object-wish_items) | Object | Event Node: Story branch or dialog option representing the \'Wish Items\' action. | 1 ||
| [`wish_levelups`](#object-wish_levelups) | Object | Event Node: Story branch or dialog option representing the \'Wish Levelups\' action. | 1 ||
| [`wish_strength`](#object-wish_strength) | Object | Event Node: Story branch or dialog option representing the \'Wish Strength\' action. | 1 ||
| [`withstand`](#object-withstand) | Object | Event Node: Story branch or dialog option representing the \'Withstand\' action. | 1 ||
| [`yank_it_out`](#object-yank_it_out) | Object | Event Node: Story branch or dialog option representing the \'Yank It Out\' action. | 1 ||
| [`yellow_needle`](#object-yellow_needle) | Object | Event Node: Story branch or dialog option representing the \'Yellow Needle\' action. | 1 ||

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
| [`has_token`](./Enums.md#enum-has_token) | Enum || 63 ||
| [`counter_range`](./Arrays.md#array-counter_range) | Array || 38 ||
| [`not_has_token`](./Enums.md#enum-not_has_token) | Enum || 30 ||
| [`counter_minimum`](./Arrays.md#array-counter_minimum) | Array || 26 ||
| [`cat_has_item_equipped`](./Enums.md#enum-cat_has_item_equipped) | Enum || 23 ||
| [`counter_maximum`](./Arrays.md#array-counter_maximum) | Array || 19 ||
| [`is_not_chapter`](./Arrays.md#array-is_not_chapter) | Array || 16 ||
| [`is_chapter`](./Arrays.md#array-is_chapter) | Array || 8 ||
| [`not_cat_has_item_equipped`](./Enums.md#enum-not_cat_has_item_equipped) | Enum || 3 ||
| `minimum_party_size` | Number || 2 ||
| `not_on_quest` | Number || 2 ||
| `cat_has_injury_count_min` | Number || 1 ||
| [`cat_has_item_slot_equipped`](./Enums.md#enum-cat_has_item_slot_equipped) | Enum || 1 ||
| `cat_has_parasite` | Boolean || 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 131 ||
| [`Fear`](./Enums.md) | Integer || 29 | 2 |
| [`Poison`](./Enums.md) | Integer || 28 | 4 |
| [`Bleed`](./Enums.md) | Integer || 20 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 13 |
| [`AllStatsUp`](./Enums.md) | Integer || 7 | 1 |
| [`SpeedUp`](./Enums.md) | Integer || 5 | -2 |
| [`StrengthUp`](./Enums.md) | Integer || 5 | 2 |
| [`AbilityOnBattleStart_Immediate`](./Enums.md) | Enum || 4 | Flush |
| [`ConstitutionUp`](./Enums.md) | Integer || 4 | -1 |
| [`AddStartingMana`](./Enums.md) | Integer || 3 | 5 |
| [`Burn`](./Enums.md) | Integer || 3 | 5 |
| [`CharismaUp`](./Enums.md) | Integer || 3 | -2 |
| [`Confusion`](./Enums.md) | Integer || 3 | 2 |
| [`HealthRegenUp`](./Enums.md) | Integer || 3 | 2 |
| [`Webbed`](./Enums.md) | Integer || 3 | 2 |
| [`Blind`](./Enums.md) | Integer || 2 | 6 |
| [`Bruise`](./Enums.md) | Integer || 2 | 1 |
| [`DexterityUp`](./Enums.md) | Integer || 2 | 2 |
| [`IntelligenceUp`](./Enums.md) | Integer || 2 | 3 |
| [`NoHealthRegen`](./Enums.md) | Integer || 2 | 1 |
| [`Sleep`](./Enums.md) | Integer || 2 | 2 |
| [`Stun`](./Enums.md) | Integer || 2 | 1 |
| [`AbilityOnBattleStart`](./Enums.md) | Enum || 1 | Flush |
| [`AddInitiative`](./Enums.md) | Integer || 1 | -99 |
| [`AlphaTurns`](./Enums.md) | Integer || 1 | 1 |
| [`ChangeTileUnderCharacterAtStart`](./Enums.md) | Enum || 1 | GlassTile |
| [`DivineShield`](./Enums.md) | Integer || 1 | 2 |
| [`Fights`](./Enums.md) | Integer || 1 | 3 |
| [`LuckUp`](./Enums.md) | Integer || 1 | 1 |
| [`Madness`](./Enums.md) | Integer || 1 | 1 |
| [`MissChance`](./Enums.md) | Integer || 1 | 10 |
| [`NoManaRegen`](./Enums.md) | Integer || 1 | 1 |
| [`PermanentConfusion`](./Enums.md) | Integer || 1 | 1 |
| [`ProbeCharmed`](./Enums.md) | Integer || 1 | 1 |
| [`RandomStatUp`](./Enums.md) | Integer || 1 | 1 |
| [`Rot`](./Enums.md) | Integer || 1 | 2 |
| [`Slow`](./Enums.md) | Integer || 1 | 3 |
| [`SpiderInfested`](./Enums.md) | Integer || 1 | 1 |
| [`Tarred`](./Enums.md) | Integer || 1 | 1 |
| [`TempStrengthUp`](./Enums.md) | Integer || 1 | 1 |

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
| `con` | Enum / Integer || 37 ||
| `random` | Number || 25 ||
| `int` | Enum / Integer || 23 ||
| `lck` | Enum / Integer || 20 ||
| `spd` | Enum / Integer || 20 ||
| `str` | Enum / Integer || 18 ||
| [`cha`](./Engine_EventKeys.md#valid-property-keys) | Variable || 16 ||
| `dex` | Enum / Integer || 10 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 125 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 125 ||
| [`reward`](#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 125 ||
| [`else`](Abilities_and_Spells.md#object-else) | Object | Event Node: Story branch or dialog option representing the \'Else\' action. | 37 ||
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String || 2 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 57 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 57 ||
| [`label`](./Strings.md#string-label) | Variable || 57 ||
| [`stat`](./Enums.md#enum-stat) | Variable || 56 ||
| [`animation`](./Enums.md#enum-animation) | Enum || 55 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 4 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 3 ||
| [`hint_chapter_exit`](./Enums.md#enum-hint_chapter_exit) | Enum || 2 ||

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
| [`label`](./Strings.md#string-label) | Variable || 44 ||
| [`stat`](./Math_Equations.md) | Equation || 44 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 41 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 41 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 32 ||
| [`copy_results`](./Enums.md#enum-copy_results) | Enum || 3 ||
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||

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
| [`object`](./Arrays.md#array-object) | Array / Enum || 40 ||
| [`count`](./Arrays.md#array-count) | Array / Integer | Quantity. | 34 ||
| [`spawn_side`](./Enums.md#enum-spawn_side) | Enum || 31 ||
| [`side`](./Enums.md#enum-side) | Enum || 3 ||

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
| [`pool`](./Enums.md#enum-pool) | Array / Enum || 39 ||
| [`restrict`](./Arrays.md#array-restrict) | Array || 30 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 38 ||
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | `String` || 20 ||
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | `String` || 6 ||
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | `String` || 6 ||
| `party_damage` | `Number` || 6 ||
| `set_frame` | `Number` || 5 ||
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | `String` || 4 ||
| [`conditional_reward`](#object-conditional_reward) | Object || 4 ||
| [`random_pool`](./Enums.md) | Array || 3 | [event_now] |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | `Array` | Event Action: Rewards the player with an item drawn from a specific loot pool. | 2 ||
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | `String` || 2 ||
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Event Node: Story branch or dialog option representing the 'Damage' action. | 1 ||
| `next_event_bonus` | `Number` || 1 ||
| [`random_mutation`](#object-random_mutation) | Object | Event Reward: Applies a completely random mutation to a character. | 1 ||
| [`self_status_next_fight`](#object-self_status_next_fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 1 ||
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 32 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 32 ||
| [`label`](./Strings.md#string-label) | String || 32 ||
| [`stat`](./Enums.md#enum-stat) | Variable || 32 ||
| [`animation`](./Enums.md#enum-animation) | Enum || 30 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 3 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 25 ||
| [`animation`](./Enums.md#enum-animation) | Enum || 25 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 25 ||
| [`label`](./Strings.md#string-label) | Variable || 25 ||
| [`stat`](./Math_Equations.md) | Equation || 25 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 23 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 2 ||

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
| `eyes` | Number || 13 ||
| `mouth` | Number || 11 ||
| `ears` | Number || 10 ||
| `eyebrows` | Number || 8 ||
| `head` | Enum / Number | Event Node: Story branch or dialog option representing the 'Head' action. | 7 ||
| `legs` | Number || 7 ||
| `arms` | Number || 6 ||
| `body` | Number | Event Node: Story branch or dialog option representing the 'Body' action. | 6 ||
| `tail` | Integer | Event Node: Story branch or dialog option representing the 'Tail' action. | 6 ||
| `eye1` | Integer || 3 ||
| `arm1` | Number || 2 ||
| `ear1` | Integer || 2 ||
| `eyebrow1` | Integer || 2 ||
| `leg1` | Integer || 2 ||
| `eye2` | Integer || 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 22 ||
| [`Fear`](./Enums.md) | Integer || 6 | 2 |
| [`Poison`](./Enums.md) | Integer || 5 | 4 |
| [`AbilityOnBattleStart_Immediate`](./Enums.md) | Enum || 3 | Flush |
| [`NoHealthRegen`](./Enums.md) | Integer || 3 | 1 |
| [`Bleed`](./Enums.md) | Integer || 1 | 2 |
| [`DivineShield`](./Enums.md) | Integer || 1 | 2 |
| [`HealthRegenUp`](./Enums.md) | Integer || 1 | 2 |
| [`Immobile`](./Enums.md) | Integer || 1 | 1 |
| [`Tangled`](./Enums.md) | Integer || 1 | 2 |
| [`Tarred`](./Enums.md) | Integer || 1 | 1 |
| [`Webbed`](./Enums.md) | Integer || 1 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 23 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 23 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 23 ||
| [`label`](./Strings.md#string-label) | Variable || 23 ||
| [`stat`](./Math_Equations.md) | Equation || 23 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 23 ||
| [`conditional_reward`](#object-conditional_reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 20 ||
| `set_frame` | `Number` || 3 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 21 ||
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | `String` | Event Node: Triggers a narrative cutscene. | 21 ||
| `skip_result_screen` | Boolean || 21 ||

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
| `mouth` | Number || 9 ||
| `count` | Array / Integer | Quantity. | 8 ||
| `tail` | Integer | Event Node: Story branch or dialog option representing the 'Tail' action. | 6 ||
| `ears` | Number || 5 ||
| `eyes` | Number || 5 ||
| `legs` | Number || 5 ||
| `body` | Number | Event Node: Story branch or dialog option representing the 'Body' action. | 3 ||
| `eyebrows` | Number || 3 ||
| `head` | Enum / Number | Event Node: Story branch or dialog option representing the 'Head' action. | 3 ||
| `arm1` | Number || 2 ||
| `arm2` | Number || 2 ||
| `leg1` | Integer || 1 ||
| `leg2` | Integer || 1 ||
| `texture` | Integer || 1 ||

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
| `count` | Array / Integer | Quantity. | 15 ||
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specific entity tag required. | 12 ||
| `asymmetric` | Boolean || 8 ||

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
| [`label`](./Strings.md#string-label) | String || 16 ||
| [`stat`](./Enums.md#enum-stat) | Variable || 16 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 14 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 14 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 12 ||
| [`copy_results`](./Enums.md#enum-copy_results) | Enum || 2 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 14 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 14 ||
| [`label`](./Strings.md#string-label) | String || 14 ||
| [`stat`](./Math_Equations.md) | Equation || 14 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 13 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 12 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 12 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 12 ||
| [`label`](./Strings.md#string-label) | String || 12 ||
| [`stat`](./Math_Equations.md) | Equation || 12 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 ||
| [`Fights`](./Enums.md) | Integer || 6 | 3 |
| [`CharacterTypeGainsStatusAtBattleStart`](Engine_LogicKeys.md#object-charactertypegainsstatusatbattlestart) | Object || 5 ||
| [`StatusRandomEnemiesOnBattleStart`](#object-statusrandomenemiesonbattlestart) | Object || 3 ||
| [`KillEnemyOfTypeAtBattleStart`](Engine_StatusAndPassiveKeys.md#object-killenemyoftypeatbattlestart) | Object | Encounter Modifier: Instantly kills one enemy of the specified type at the start of battle. | 2 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

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
| [`label`](./Strings.md#string-label) | String || 11 ||
| [`stat`](./Math_Equations.md) | Equation || 11 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 7 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 7 ||
| [`copy_results`](./Enums.md#enum-copy_results) | Enum || 4 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 11 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 11 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 11 ||
| [`label`](./Strings.md#string-label) | Variable || 11 ||
| [`stat`](./Math_Equations.md) | Equation || 11 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||

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
| `fights_skipped` | Number || 7 ||
| [`return_as`](./Enums.md#enum-return_as) | Enum || 3 ||
| [`return_during`](./Enums.md#enum-return_during) | Enum || 3 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 8 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 8 ||
| [`label`](./Strings.md#string-label) | String || 8 ||
| [`stat`](./Math_Equations.md) | Equation || 8 ||
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 7 ||
| [`label`](./Strings.md#string-label) | String || 7 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 7 ||
| [`animation`](./Enums.md#enum-animation) | Enum || 5 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 ||
| [`label`](./Strings.md#string-label) | String || 7 ||
| [`stat`](./Math_Equations.md) | Equation || 7 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 6 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 6 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 7 ||
| [`label`](./Strings.md#string-label) | String || 7 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 7 ||
| [`animation`](./Enums.md#enum-animation) | Enum || 5 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 7 ||
| [`label`](./Strings.md#string-label) | String || 7 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 7 ||
| [`animation`](./Enums.md#enum-animation) | Enum || 5 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 7 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 7 ||
| [`label`](./Strings.md#string-label) | Variable || 7 ||
| [`stat`](./Math_Equations.md) | Equation || 7 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 7 ||
| [`label`](./Strings.md#string-label) | Variable || 7 ||
| [`stat`](./Math_Equations.md) | Equation || 7 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 6 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 7 ||
| [`label`](./Strings.md#string-label) | Variable || 7 ||
| [`stat`](./Enums.md#enum-stat) | Variable || 7 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 ||
| [`animation`](./Enums.md#enum-animation) | Enum || 6 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 6 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 6 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 6 ||
| [`label`](./Enums.md#enum-label) | Enum || 6 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 6 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 6 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 6 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 6 ||
| [`label`](./Enums.md#enum-label) | Enum || 6 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 6 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 6 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 6 ||
| [`label`](./Strings.md#string-label) | String || 6 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 6 ||
| [`animation`](./Enums.md#enum-animation) | Enum || 5 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 6 ||
| [`label`](./Strings.md#string-label) | Variable || 6 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 5 ||
| [`stat`](./Enums.md#enum-stat) | Variable || 5 ||
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`hint_chapter_exit`](./Enums.md#enum-hint_chapter_exit) | Enum || 1 ||

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
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 6 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 6 ||
| [`label`](./Strings.md#string-label) | String || 6 ||
| [`stat`](./Math_Equations.md) | Equation || 6 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 6 ||
| [`label`](./Strings.md#string-label) | Variable || 6 ||
| [`stat`](./Enums.md#enum-stat) | Variable || 6 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 5 ||
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||

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
| [`event`](./Enums.md#enum-event) | Enum || 5 ||
| `same_cat` | Boolean || 5 ||
| `count` | Array / Integer | Quantity. | 4 ||

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
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specific entity tag required. | 8 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 ||
| [`Fear`](./Enums.md) | Integer || 3 | 2 |
| [`Stun`](./Enums.md) | Integer || 2 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`AllStatsUp`](./Enums.md) | Integer || 1 | 1 |

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 5 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 5 ||
| [`label`](./Strings.md#string-label) | Variable || 5 ||
| [`stat`](./Math_Equations.md) | Equation || 5 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 5 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 5 ||
| [`label`](./Strings.md#string-label) | String || 5 ||
| [`stat`](./Math_Equations.md) | Equation || 5 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 5 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 5 ||
| [`label`](./Strings.md#string-label) | String || 5 ||
| [`stat`](./Math_Equations.md) | Equation || 5 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 2 ||
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 4 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 4 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 4 ||
| [`label`](./Enums.md#enum-label) | Enum || 4 ||
| [`stat`](./Math_Equations.md) | Equation || 4 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 4 ||
| [`label`](./Strings.md#string-label) | String || 4 ||
| [`animation`](./Enums.md#enum-animation) | Enum || 3 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 3 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 4 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 4 ||
| [`label`](./Strings.md#string-label) | String || 4 ||
| [`stat`](./Enums.md#enum-stat) | Variable || 3 ||
| [`animation`](./Enums.md#enum-animation) | Enum || 2 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 4 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 4 ||
| [`hint_chapter_exit`](./Enums.md#enum-hint_chapter_exit) | Enum || 4 ||
| [`label`](./Enums.md#enum-label) | Enum || 4 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 4 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||
| [`play_animation`](./Enums.md) | Array / Enum || 4 | [0] |
| [`random_pool`](./Enums.md) | Array || 3 | [event_now] |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 ||
| [`weather_roll`](./Arrays.md#array-weather_roll) | Array || 1 ||

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
| `cha` | Enum / Integer || 4 ||
| `con` | Enum / Integer || 4 ||
| `dex` | Enum / Integer || 4 ||
| `int` | Enum / Integer || 4 ||
| `lck` | Enum / Integer || 4 ||
| `spd` | Enum / Integer || 4 ||
| `str` | Enum / Integer || 4 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 4 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 4 ||
| [`hint_chapter_exit`](./Enums.md#enum-hint_chapter_exit) | Enum || 4 ||
| [`label`](./Enums.md#enum-label) | Enum || 4 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 4 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 4 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 4 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 4 ||
| [`label`](./Strings.md#string-label) | String || 4 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 4 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||

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
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 3 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 3 ||
| [`label`](./Strings.md#string-label) | String || 3 ||
| [`stat`](./Math_Equations.md) | Equation || 3 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||

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
| `con` | Enum / Integer || 2 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 3 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 3 ||
| [`label`](./Strings.md#string-label) | String || 3 ||
| [`stat`](./Math_Equations.md) | Equation || 3 ||

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
| `count` | Array / Integer | Quantity. | 7 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 ||
| [`Fear`](./Enums.md) | Integer || 3 | 2 |
| [`Bleed`](./Enums.md) | Integer || 1 | 2 |

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
| [`animation`](./Enums.md#enum-animation) | Enum || 2 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 2 ||
| [`label`](./Enums.md#enum-label) | Enum || 2 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 2 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 2 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 2 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 2 ||
| [`label`](./Strings.md#string-label) | String || 2 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 2 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 2 ||
| [`label`](./Strings.md#string-label) | String || 2 ||

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
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 2 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 2 ||
| [`label`](./Strings.md#string-label) | String || 2 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

</details>

---

### Object: `gain_familiar`


**Definition:** Event Action: Adds a specific familiar to the party.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `initial_health` | Integer || 1 ||
| [`object`](./Enums.md#enum-object) | Array / Enum || 1 ||

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
| [`enemy_type`](./Enums.md#enum-enemy_type) | Enum || 2 ||
| [`fallback_spawn`](./Arrays.md#array-fallback_spawn) | Array || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 2 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 2 ||
| [`label`](./Strings.md#string-label) | String || 2 ||
| [`stat`](./Math_Equations.md) | Equation || 2 ||

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
| `count` | Array / Integer | Quantity. | 2 ||
| `ears` | Number || 2 ||
| `eyebrows` | Number || 2 ||
| `eyes` | Number || 2 ||
| `mouth` | Number || 2 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 2 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 2 ||
| [`label`](./Strings.md#string-label) | String || 2 ||
| [`stat`](./Math_Equations.md) | Equation || 2 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 2 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 2 ||
| [`label`](./Strings.md#string-label) | String || 2 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 2 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 2 ||
| [`label`](./Strings.md#string-label) | String || 2 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 2 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 2 ||
| [`label`](./Strings.md#string-label) | String || 2 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 2 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| `chance` | Number | Probability weight for this outcome. | 1 ||
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | `String` | Event Action: Rewards the player with an item drawn from a specific loot pool. | 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 2 ||
| [`label`](./Strings.md#string-label) | Variable || 2 ||
| [`stat`](./Enums.md#enum-stat) | Variable || 2 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 2 ||
| [`label`](./Strings.md#string-label) | String || 2 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 2 ||
| [`label`](./Strings.md#string-label) | String || 2 ||

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
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 2 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 2 ||
| [`label`](./Strings.md#string-label) | String || 2 ||
| [`stat`](./Math_Equations.md) | Equation || 2 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Enums.md#enum-label) | Enum || 1 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Enums.md#enum-label) | Enum || 1 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`copy_results`](./Enums.md#enum-copy_results) | Enum || 1 ||
| `fixed_chance` | Number || 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`label`](./Enums.md#enum-label) | Enum || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`bad`](#object-bad) | Object || 1 ||

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
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Enums.md#enum-label) | Enum || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`copy_results`](./Enums.md#enum-copy_results) | Enum || 1 ||
| `fixed_chance` | Number || 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||
| `stat_max` | Number || 1 ||
| `stat_min` | Number || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

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
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

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
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum || 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||
| `stat_max` | Number || 1 ||
| `stat_min` | Number || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum || 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||
| `stat_max` | Number || 1 ||
| `stat_min` | Number || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum || 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||
| `stat_max` | Number || 1 ||
| `stat_min` | Number || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum || 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||
| `stat_max` | Number || 1 ||
| `stat_min` | Number || 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`bad`](#object-bad) | Object || 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Enums.md#enum-label) | Enum || 1 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Enums.md#enum-label) | Enum || 1 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`hint_chapter_exit`](./Enums.md#enum-hint_chapter_exit) | Enum || 1 ||
| [`label`](./Enums.md#enum-label) | Enum || 1 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`object`](./Enums.md#enum-object) | Array / Enum || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`bad`](#object-bad) | Object || 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`hint_chapter_exit`](./Enums.md#enum-hint_chapter_exit) | Enum || 1 ||
| [`label`](./Enums.md#enum-label) | Enum || 1 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`bad`](#object-bad) | Object || 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| `fixed_chance` | Number || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`bad`](#object-bad) | Object || 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Enums.md#enum-label) | Enum || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Enums.md#enum-label) | Enum || 1 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`label`](./Enums.md#enum-label) | Enum || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||
| [`bad`](#object-bad) | Object || 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Enums.md#enum-label) | Enum || 1 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Enums.md#enum-label) | Enum || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||

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
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum || 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||
| `stat_max` | Number || 1 ||
| `stat_min` | Number || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

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
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| `fixed_chance` | Number || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Enums.md#enum-label) | Enum || 1 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`bad`](#object-bad) | Object || 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`bad`](#object-bad) | Object || 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`bad`](#object-bad) | Object || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Enums.md#enum-label) | Enum || 1 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Enums.md#enum-label) | Enum || 1 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`bad`](#object-bad) | Object || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`label`](./Enums.md#enum-label) | Enum || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||
| [`bad`](#object-bad) | Object || 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Enums.md#enum-label) | Enum || 1 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Enums.md#enum-label) | Enum || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`bad`](#object-bad) | Object || 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||
| [`bad`](#object-bad) | Object || 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Enums.md#enum-label) | Enum || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`bad`](#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||

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
| `animation` | String | Undocumented. | 1 | `choice_coins_ten` |
| `animation_fail` | String | Undocumented. | 1 | `choice_no_coins` |
| [`bad`](#object-bad) | Object | Undocumented. | 1 ||
| [`good`](#object-good) | Object | Undocumented. | 1 ||
| `label` | String | Undocumented. | 1 | `"EVENT_BUY_ANSW"` |
| `stat` | String | Undocumented. | 1 | `coins` |
| `stat_max` | Number | Undocumented. | 1 | `10` |
| `stat_min` | Number | Undocumented. | 1 | `10` |

</details>

### Object: `buy3`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation` | String | Undocumented. | 1 | `choice_coins_twentyfive` |
| `animation_fail` | String | Undocumented. | 1 | `choice_no_coins` |
| [`bad`](#object-bad) | Object | Undocumented. | 1 ||
| [`good`](#object-good) | Object | Undocumented. | 1 ||
| `label` | String | Undocumented. | 1 | `"EVENT_BUY_ANSW"` |
| `stat` | String | Undocumented. | 1 | `coins` |
| `stat_max` | Number | Undocumented. | 1 | `25` |
| `stat_min` | Number | Undocumented. | 1 | `25` |

</details>

### Object: `pick`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation` | String | Undocumented. | 3 | `choice_dex_alt` |
| `copy_results` | String | Undocumented. | 3 | `examine` |
| `label` | String | Undocumented. | 3 | `"EVENT_PICK_ANSW"` |
| `stat` | String | Undocumented. | 3 | `dex` |

</details>
