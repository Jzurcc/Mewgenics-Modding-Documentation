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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 664 |  |
| [`intro`](#object-intro) | Object | An object defining the introductory cutscene for the event, including title, cat selection, and visuals. | 239 ||
| [`main`](#object-main) | Object | An object containing the primary prompt and options for an event. | 227 ||
| [`self_damage`](Abilities_and_Spells.md#object-self_damage) | Boolean / Integer / Object | Defines damage or effects applied to the caster when using the ability. | 218 ||
| `cha` | Enum / Integer | The Charisma stat value or modifier. | 89 |  |
| `con` | Enum / Integer | The Constitution stat value or modifier. | 79 ||
| `spd` | Enum / Integer | The Speed stat value or modifier. | 78 ||
| `int` | Enum / Integer || 66 ||
| `lck` | Enum / Integer || 53 ||
| `str` | Enum / Integer || 45 ||
| [`rare`](./Events_and_Encounters.md#object-rare) | Enum | Defines the rare reward block for a boss encounter. | 34 |  |
| `dex` | Enum / Integer || 30 ||
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String || 25 ||
| `normal` | Array || 23 | `[common boneyard_events.gon]` (Array), `[common core_events.gon]` (Array) |
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 13 ||
| [`common`](./Events_and_Encounters.md#object-common) | Enum | Defines the common reward block for a boss encounter. | 11 |  |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | String || 9 ||
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String || 4 ||
| `set_frame` | `Number` || 4 ||
| [`label`](./Strings.md#string-label) | String || 3 ||
| [`stat`](./Enums.md#enum-stat) | Variable || 3 ||
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 3 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 3 ||
| [`reward`](#object-reward) | Object | An object containing sub-objects defining the rewards for different rarity tiers (e.g., common, rare), each with their own set of actions and items. | 3 ||
| [`pick`](#object-pick) | Object | An object defining the player action to pick or collect an object, including its stat check and outcomes. | 2 ||
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | String | Grants an item from the specified pool or a specific item name. | 1 ||
| `weight` | `Number` | A multiplier or priority value for random selection or effect magnitude. | 1 ||
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum || 1 ||
| `stat_max` | Number || 1 ||
| `stat_min` | Number || 1 ||
| [`open`](Characters_and_Bosses.md#object-open) | Object | An object defining the player action to open a container, including its stat check and outcomes. | 1 ||
| [`smash`](#object-smash) | Object | An object defining the player action to smash an object, including its stat check and outcomes. | 1 ||
| [`conditional_reward`](#object-conditional_reward) | Object | An object defining a reward that is granted only if specified conditions are met. | 1 ||
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Specifies the name of a cutscene to play. | 1 ||
| [`destroy`](#object-destroy) | Object | An object defining the player action to destroy an object, including its stat check and outcomes. | 1 ||
| [`mutation`](#object-mutation) | Object | An object defining specific body part mutations applied to the unit. | 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 759 ||
| [`common`](./Events_and_Encounters.md#object-common) | Enum | Defines the common reward block for a boss encounter. | 633 ||
| [`rare`](./Events_and_Encounters.md#object-rare) | Enum | Defines the rare reward block for a boss encounter. | 623 ||
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String || 70 ||
| `set_frame` | `Number` || 53 ||
| [`set_subject`](./Engine_EventKeys.md#valid-property-keys) | `String` || 10 ||
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | String | Grants an item from the specified pool or a specific item name. | 9 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 634 ||
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | `String` || 606 ||
| `set_frame` | `Number` || 151 ||
| [`self_status_next_fight`](#object-self_status_next_fight) | Object | An object defining status effects applied to the unit at the start of the next fight. | 92 ||
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | `String` | Grants an item from the specified pool or a specific item name. | 66 ||
| [`permanent_stats`](#object-permanent_stats) | Object | Defines permanent stat changes to apply to the unit (e.g., con, cha). | 39 ||
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Specifies the amount of damage dealt, can be a number or expression. | 35 ||
| [`random_pool`](./Enums.md) | Array || 35 | [event_now] |
| [`gain_coins`](./Engine_EventKeys.md#valid-property-keys) | `Array` || 28 ||
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | `String` || 26 ||
| `self_damage` | `Number` | Defines damage or effects applied to the caster when using the ability. | 26 ||
| `random_mutation` | `Number` | The number of random mutations applied to the unit. | 25 ||
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | `String` || 24 ||
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | `String` || 23 ||
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | `String` || 21 ||
| `gain_food` | `Number` || 21 ||
| [`spawn_unit_next_fight`](#object-spawn_unit_next_fight) | Object | An object defining a unit to spawn during the next fight, including its object, count, and spawn side. | 18 ||
| [`gain_familiar`](./Events_and_Encounters.md#object-gain-familiar) | `String` | Specifies which familiar type (by its class name) the unit gains. | 15 ||
| `party_heal` | `Number` || 15 ||
| `party_damage` | `Number` || 15 ||
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | `String` || 14 ||
| `heal` | `Number` | An equation string that determines the amount of health restored by this damage instance. | 13 ||
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | `String` || 12 ||
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | `String` || 11 ||
| [`party_status_next_fight`](#object-party_status_next_fight) | Object | An object defining status effects to apply to the party at the start of the next fight. | 11 ||
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | `String` || 11 ||
| `ally_ambush_next_fights` | `Number` || 10 ||
| `full_heal` | `Number` || 10 ||
| `ambush_next_basic_fights` | `Number` || 9 ||
| [`conditional_reward`](#object-conditional_reward) | Object | An object defining a reward that is granted only if specified conditions are met. | 9 ||
| [`random_mutation_from_set`](#object-random_mutation_from_set) | Object | Defines a set of mutation categories and their specific IDs to apply a random mutation from. | 8 ||
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | `String` || 7 ||
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | `String` || 7 ||
| `next_event_bonus` | `Number` || 7 ||
| [`clear_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | `String` || 6 ||
| [`global_effect_next_fight`](#object-global_effect_next_fight) | Object | Defines a global status effect or modifier to apply in the next fight. | 6 ||
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | `String` || 6 ||
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | `String` || 5 ||
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | `String` || 5 ||
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | `String` || 5 ||
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | `String` || 4 ||
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | `String` || 2 ||
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | `String` || 2 ||
| [`next_event_from_set`](#object-next_event_from_set) | Object | Specifies the next event to trigger, or defines a set of events with count and category constraints. | 2 ||
| `party_heal_disorder` | `Number` || 2 ||
| [`party_permanent_stats_exclude_self`](#object-party_permanent_stats_exclude_self) | Object | An object specifying permanent stat bonuses (str, dex, con, int, spd) applied to all party members except the triggering unit. | 2 ||
| [`spin`](./Engine_EventKeys.md#valid-property-keys) | `String` || 2 ||
| `clear_result_animation` | `Number` || 1 ||
| [`decrement_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 ||
| [`get_and_equip_item`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 ||
| `heal_disorder` | `Number` || 1 ||
| `heal_injury` | `Number` || 1 ||
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 ||
| [`mutation`](#object-mutation) | Object | An object defining specific body part mutations applied to the unit. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 634 ||
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | `String` || 611 ||
| `set_frame` | `Number` || 180 ||
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | `String` | Grants an item from the specified pool or a specific item name. | 84 ||
| [`permanent_stats`](#object-permanent_stats) | Object | Defines permanent stat changes to apply to the unit (e.g., con, cha). | 84 ||
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | `String` || 65 ||
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | `String` || 46 ||
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | `String` || 45 ||
| [`self_status_next_fight`](#object-self_status_next_fight) | Object | An object defining status effects applied to the unit at the start of the next fight. | 40 ||
| `random_mutation` | `Number` | The number of random mutations applied to the unit. | 38 ||
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | `String` || 35 ||
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | `String` || 30 ||
| [`random_pool`](./Enums.md) | Array || 28 | [event_now] |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | `String` || 26 ||
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | `String` || 21 ||
| [`spawn_unit_next_fight`](#object-spawn_unit_next_fight) | Object | An object defining a unit to spawn during the next fight, including its object, count, and spawn side. | 20 ||
| [`conditional_reward`](#object-conditional_reward) | Object | An object defining a reward that is granted only if specified conditions are met. | 18 ||
| [`mutation`](#object-mutation) | Object | An object defining specific body part mutations applied to the unit. | 18 ||
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Specifies the amount of damage dealt, can be a number or expression. | 18 ||
| [`gain_coins`](./Engine_EventKeys.md#valid-property-keys) | `Array` || 17 ||
| [`gain_familiar`](./Events_and_Encounters.md#object-gain-familiar) | `String` | Specifies which familiar type (by its class name) the unit gains. | 15 ||
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | `String` || 14 ||
| `next_event_bonus` | `Number` || 14 ||
| `self_damage` | `Number` | Defines damage or effects applied to the caster when using the ability. | 13 ||
| [`party_status_next_fight`](#object-party_status_next_fight) | Object | An object defining status effects to apply to the party at the start of the next fight. | 12 ||
| [`random_mutation_from_set`](#object-random_mutation_from_set) | Object | Defines a set of mutation categories and their specific IDs to apply a random mutation from. | 11 ||
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | `Array` || 11 ||
| [`learn_passive`](./Engine_EventKeys.md#valid-property-keys) | `String` || 10 ||
| `party_heal` | `Number` || 10 ||
| `party_damage` | `Number` || 10 ||
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | `String` || 9 ||
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | `String` || 8 ||
| `party_random_mutation` | `Number` || 8 ||
| `ambush_next_basic_fights` | `Number` || 7 ||
| [`leave_party_temporarily`](#object-leave_party_temporarily) | Object | Defines parameters for a unit leaving the party temporarily, such as skipped fights and return conditions. | 7 ||
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
| [`global_effect_next_fight`](#object-global_effect_next_fight) | Object | Defines a global status effect or modifier to apply in the next fight. | 3 ||
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | `String` || 3 ||
| [`make_old`](./Engine_EventKeys.md#valid-property-keys) | `String` || 3 ||
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | `String` | Specifies the next event to trigger, or defines a set of events with count and category constraints. | 3 ||
| `spawn_reflection_next_fight` | `Number` | The number of reflections to spawn in the next battle, optionally with a mutation. | 3 ||
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | `String` || 2 ||
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | `String` || 2 ||
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | `String` || 2 ||
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | `String` || 2 ||
| `party_heal_disorder` | `Number` || 2 ||
| `party_heal_injury` | `Number` || 2 ||
| [`party_permanent_stats_exclude_self`](#object-party_permanent_stats_exclude_self) | Object | An object specifying permanent stat bonuses (str, dex, con, int, spd) applied to all party members except the triggering unit. | 2 ||
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
| [`party_permanent_stats`](#object-party_permanent_stats) | Object | An object defining permanent stat increases applied to the party. | 1 ||
| [`party_random_mutation_from_set`](#object-party_random_mutation_from_set) | Object | An object specifying the count and mutation parts to randomly apply to the party. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 545 ||
| [`reward`](#object-reward) | Object | An object containing sub-objects defining the rewards for different rarity tiers (e.g., common, rare), each with their own set of actions and items. | 326 ||
| `set_frame` | `Number` || 285 ||
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String || 184 ||
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | String || 111 ||
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | `String` || 21 ||
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | `String` | Specifies the name of a cutscene to play. | 19 ||
| [`conditional_reward`](#object-conditional_reward) | Object | An object defining a reward that is granted only if specified conditions are met. | 14 ||
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | `String` || 12 ||
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | `String` || 12 ||
| `random_mutation` | Number | The number of random mutations applied to the unit. | 12 ||
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | `String` || 12 ||
| [`rare`](./Events_and_Encounters.md#object-rare) | Enum | Defines the rare reward block for a boss encounter. | 10 ||
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | String || 9 ||
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | String || 9 ||
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | String || 8 ||
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | String || 7 ||
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | `String` || 7 ||
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | String || 6 ||
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | String || 6 ||
| [`random_pool`](./Enums.md) | Array || 5 | [event_now] |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | String || 4 ||
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | String | Grants an item from the specified pool or a specific item name. | 4 ||
| [`mutation`](#object-mutation) | Object | An object defining specific body part mutations applied to the unit. | 4 ||
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
| [`gain_clone_familiar`](#object-gain_clone_familiar) | Object | An object that triggers the gaining of a clone familiar, with a specified object name. | 1 ||
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 ||
| [`global_effect_next_fight`](#object-global_effect_next_fight) | Object | Defines a global status effect or modifier to apply in the next fight. | 1 ||
| `heal` | `Number` | An equation string that determines the amount of health restored by this damage instance. | 1 ||
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | String || 1 ||
| `next_event_bonus` | Number || 1 ||
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | String | Specifies the next event to trigger, or defines a set of events with count and category constraints. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 339 ||
| [`reward`](#object-reward) | Object | An object containing sub-objects defining the rewards for different rarity tiers (e.g., common, rare), each with their own set of actions and items. | 305 ||
| `set_frame` | `Number` || 222 ||
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String || 38 ||
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | String || 10 ||
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | `String` || 4 ||
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | String || 4 ||
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | `String` || 4 ||
| [`self_status_next_fight`](#object-self_status_next_fight) | Object | An object defining status effects applied to the unit at the start of the next fight. | 4 ||
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Specifies the name of a cutscene to play. | 3 ||
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | String || 3 ||
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | `String` || 3 ||
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | String || 3 ||
| [`conditional_reward`](#object-conditional_reward) | Object | An object defining a reward that is granted only if specified conditions are met. | 2 ||
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | String || 2 ||
| `next_event_bonus` | Number || 2 ||
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 ||
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 ||
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | `String` || 1 ||
| [`party_random_mutation_from_set`](#object-party_random_mutation_from_set) | Object | An object specifying the count and mutation parts to randomly apply to the party. | 1 ||
| [`permanent_stats`](#object-permanent_stats) | Object | Defines permanent stat changes to apply to the unit (e.g., con, cha). | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 214 ||
| [`options`](./Events_and_Encounters.md#object-options) | Array | An array of named option objects within an event, each defining a possible action the player can take. | 210 ||
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String || 203 ||
| [`setup`](#object-setup) | Object | Defines actions or checks to run before the main event logic, often setting up conditions or tokens. | 23 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 4 ||
| [`goto`](./Engine_EventKeys.md#valid-property-keys) | `String` || 4 ||
| [`outcome`](#object-outcome) | Object | An object defining the possible outcomes of an event, typically containing a random pool or weighted lists of rewards and animations. | 4 ||
| `max_options` | `Number` || 3 ||
| `shuffle_options` | `Boolean` || 3 ||
| [`leave`](Engine_LogicKeys.md#object-leave) | Object | An object defining the player action to leave or ignore the event, including its stat check and outcomes. | 3 ||
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
| [`ignore`](#object-ignore) | Object | An object defining the player action to ignore the event, including its stat check and outcomes. | 55 ||
| [`examine`](#object-examine) | Object | An object defining the player action to examine an object, including its stat check and outcomes. | 43 ||
| [`leave`](Engine_LogicKeys.md#object-leave) | Object | An object defining the player action to leave or ignore the event, including its stat check and outcomes. | 29 ||
| [`loot`](#object-loot) | Object | An object defining the player action to loot a container or corpse, including its stat check and outcomes. | 25 ||
| [`eat`](#object-eat) | Object | An object defining the player action to consume something, including its stat check and outcomes. | 23 ||
| [`smash`](#object-smash) | Object | An object defining the player action to smash an object, including its stat check and outcomes. | 15 ||
| [`destroy`](#object-destroy) | Object | An object defining the player action to destroy an object, including its stat check and outcomes. | 13 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 12 ||
| [`bash`](#object-bash) | Object | An object defining the player action to bash open a container, including its stat check and outcomes. | 12 ||
| [`sneak`](#object-sneak) | Object | An object defining the player action to sneak past a threat, including its stat check and outcomes. | 11 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 10 ||
| [`open`](Characters_and_Bosses.md#object-open) | Object | An object defining the player action to open a container, including its stat check and outcomes. | 8 ||
| [`take`](#object-take) | Object | An object defining the player action to take an item, including its stat check and outcomes. | 8 ||
| [`a`](#object-a) | Object | An object defining the first custom option in a test or debug event. | 7 ||
| [`attack`](./Events_and_Encounters.md#context-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 7 ||
| [`b`](#object-b) | Object | An object defining the second custom option in a test or debug event. | 7 ||
| [`c`](#object-c) | Object | An object defining the third custom option in a test or debug event. | 7 ||
| [`charm`](#object-charm) | Object | Specifies the player character's attempt to charm or persuade the encounter. | 7 ||
| [`fight`](#object-fight) | Object | Specifies the player character's attempt to fight or force their way through the encounter. | 7 ||
| [`touch`](#object-touch) | Object | Specifies the player character's attempt to physically touch or interact with the encounter. | 7 ||
| [`activate_p`](#object-activate_p) | Object | Specifies the player character's attempt to activate the object (press a button/lever). | 6 ||
| [`activate_z`](#object-activate_z) | Object | Specifies the player character's attempt to activate the object (pull a lever/switch). | 6 ||
| [`d`](#object-d) | Object | Specifies a debug or test option for game development purposes. | 6 ||
| [`enter`](#object-enter) | Object | Specifies the player character's attempt to enter or go inside the encounter location. | 6 ||
| [`inspect`](#object-inspect) | Object | Specifies the player character's attempt to inspect or examine the encounter. | 6 ||
| [`lick`](#object-lick) | Object | Specifies the player character's attempt to lick the encounter. | 6 ||
| [`drink`](#object-drink) | Object | Specifies the player character's attempt to drink from or consume the encounter. | 5 ||
| [`kiss`](#object-kiss) | Object | Specifies the player character's attempt to kiss the encounter. | 5 ||
| [`run`](#object-run) | Object | Specifies the player character's attempt to run away or flee from the encounter. | 5 ||
| [`bite`](#object-bite) | Object | Specifies the player character's attempt to bite the encounter. | 4 ||
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Specifies the amount of damage dealt, can be a number or expression. | 4 ||
| [`go_around`](#object-go_around) | Object | Specifies the player character's attempt to go around or bypass the encounter. | 4 ||
| [`home`](#object-home) | Object | Specifies the option to go home (exit to the main hub). | 4 ||
| [`past`](#object-past) | Object | Specifies the option to travel to a past era (Ice Age, Jurassic, etc.). | 4 ||
| [`skip`](#object-skip) | Object | Specifies the option to skip or decline the current encounter. | 4 ||
| [`investigate`](#object-investigate) | Object | Specifies the player character's attempt to investigate the encounter. | 3 ||
| [`repell`](#object-repell) | Object | Specifies the player character's attempt to rappel down or climb into the encounter. | 3 ||
| [`attach_antenna`](#object-attach_antenna) | Object | Specifies the player character's attempt to attach a device or antenna to the encounter. | 2 ||
| [`boogers`](#object-boogers) | Object | Specifies the player character's attempt to pick or examine boogers. | 2 ||
| [`copy`](#object-copy) | Object | Specifies the player character's attempt to copy or replicate something from the encounter. | 2 ||
| [`find_another_way`](#object-find_another_way) | Object | Specifies the player character's attempt to find an alternative path around the encounter. | 2 ||
| [`move_closer`](#object-move_closer) | Object | Specifies the player character's attempt to move closer to the encounter. | 2 ||
| [`play`](#object-play) | Object | Specifies the player character's attempt to play or interact playfully with the encounter. | 2 ||
| [`poop`](#object-poop) | Object | Defines a poop event or interaction, often part of a random encounter or response in dialogue. | 2 ||
| [`print`](#object-print) | Object | Specifies the player character's attempt to print or output something from the encounter. | 2 ||
| [`protection`](#object-protection) | Object | Specifies the player character's attempt to offer or ask for protection. | 2 ||
| [`repair`](#object-repair) | Object | Specifies the player character's attempt to repair the encounter object. | 2 ||
| [`sacrifice`](#object-sacrifice) | Object | Specifies the player character's attempt to make a sacrifice at the encounter. | 2 ||
| [`scale`](./Events_and_Encounters.md#context-scale) | Number | The scale multiplier applied to the unit's visual size. | 2 ||
| [`turnon`](#object-turnon) | Object | Specifies the player character's attempt to turn on or activate the encounter. | 2 ||
| [`altar_sacrifice`](#object-altar_sacrifice) | Object | Specifies the player character's attempt to sacrifice a cat at the altar. | 1 ||
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum || 1 ||
| [`arm`](#object-arm) | Object | Specifies the player character's attempt to put their arm inside the encounter. | 1 ||
| [`attach_amplifier`](#object-attach_amplifier) | Object | Specifies the player character's attempt to attach an amplifier to the encounter. | 1 ||
| [`attach_leech`](#object-attach_leech) | Object | Specifies the player character's attempt to attach a leech to the encounter. | 1 ||
| [`bash_past_alt`](#object-bash_past_alt) | Object | Specifies the player character's attempt to bash through the encounter (alternate version for specific chapters). | 1 ||
| [`bite_it_off`](#object-bite_it_off) | Object | Specifies the player character's attempt to bite off part of the encounter. | 1 ||
| [`blue`](#object-blue) | Object | Specifies the player character's attempt to choose the blue option. | 1 ||
| [`blue_needle`](#object-blue_needle) | Object | Specifies the player character's attempt to take the blue needle. | 1 ||
| [`body`](./Events_and_Encounters.md#context-body) | Number | The catalog ID for the cat's body part. | 1 ||
| [`book`](#object-book) | Object | Specifies the player character's attempt to read or take the book. | 1 ||
| [`brace`](#object-brace) | Object | Specifies the player character's attempt to brace themselves for the encounter. | 1 ||
| [`break_ice`](#object-break_ice) | Object | Specifies the player character's attempt to break the ice covering the encounter. | 1 ||
| [`break_lock`](#object-break_lock) | Object | Specifies the player character's attempt to break the lock on the encounter. | 1 ||
| [`bribe`](#object-bribe) | Object | Specifies the player character's attempt to bribe the encounter. | 1 ||
| [`button`](#object-button) | Object | Specifies the player character's attempt to push the button. | 1 ||
| [`buy1`](#object-buy1) | Object | Specifies the player character's attempt to buy one of the offered items. | 1 ||
| [`catch`](#object-catch) | Object | An object defining a response option for catching an entity, including stat checks and rewards. | 1 ||
| [`challenge_to_game`](#object-challenge_to_game) | Object | Specifies the player character's attempt to challenge the encounter to a game. | 1 ||
| [`chaos_ending`](#object-chaos_ending) | Object | Specifies the option to trigger the chaos ending cutscene. | 1 ||
| [`chapter_cutscene`](#object-chapter_cutscene) | Object | Specifies the option to trigger a chapter intro cutscene. | 1 ||
| [`charm_past_alt`](#object-charm_past_alt) | Object | Specifies the player character's attempt to charm the encounter (alternate version for specific chapters). | 1 ||
| [`climb`](#object-climb) | Object | Specifies the player character's attempt to climb over the encounter. | 1 ||
| [`comfort`](Engine_LogicKeys.md#object-comfort) | Object | A charisma-based event response that soothes the encounter subject. | 1 ||
| [`communicate`](#object-communicate) | Object | A charisma-based event response to establish communication. | 1 ||
| [`concheck`](#object-concheck) | Object | A constitution-based event response to test endurance. | 1 ||
| [`counter`](#object-counter) | Object | An event response that uses a countering action, with no stat requirement. | 1 ||
| [`crack_open`](#object-crack_open) | Object | A strength-based event response to break something open. | 1 ||
| [`cross`](#object-cross) | Object | An event response to traverse an obstacle, with no stat requirement. | 1 ||
| [`cut_wires`](#object-cut_wires) | Object | An intelligence-based event response to disable wires. | 1 ||
| [`damage_1`](#object-damage_1) | Object | A constitution-based event response that deals minor damage. | 1 ||
| [`damage_full`](#object-damage_full) | Object | A constitution-based event response that deals full damage. | 1 ||
| [`damage_half`](#object-damage_half) | Object | A constitution-based event response that deals halved damage. | 1 ||
| [`desert_cutscene`](#object-desert_cutscene) | Object | An event response that triggers a desert-themed cutscene, with no stat requirement. | 1 ||
| [`dexcheck`](#object-dexcheck) | Object | A dexterity-based event response to test agility. | 1 ||
| [`dig`](#object-dig) | Object | A strength-based event response to excavate, limited by a token counter maximum. | 1 ||
| [`disarm`](#object-disarm) | Object | A dexterity-based event response to remove a trap. | 1 ||
| [`dive`](#object-dive) | Object | A dexterity-based event response to plunge into water. | 1 ||
| [`donate`](#object-donate) | Object | An event response to give a donation, with no stat requirement but a coin cost. | 1 ||
| [`donate_10`](#object-donate_10) | Object | An event response to donate 10 coins. | 1 ||
| [`donate_15`](#object-donate_15) | Object | An event response to donate 15 coins. | 1 ||
| [`donate_20`](#object-donate_20) | Object | An event response to donate 20 coins. | 1 ||
| [`donate_5`](#object-donate_5) | Object | An event response to donate 5 coins. | 1 ||
| [`double`](#object-double) | Object | An event response that doubles something, with no stat requirement. | 1 ||
| [`eat_meat`](#object-eat_meat) | Object | A constitution-based event response to consume meat. | 1 ||
| [`enter_crater`](#object-enter_crater) | Object | A luck-based event response to enter a crater. | 1 ||
| [`face`](./Events_and_Encounters.md#context-face) | Enum | The face equipment item assigned to the unit. | 1 ||
| [`fiddle`](#object-fiddle) | Object | A quest-based event response to tamper, requiring no specific quest token. | 1 ||
| [`fill_jar`](#object-fill_jar) | Object | A quest-based event response to fill a jar, with no stat requirement. | 1 ||
| [`find`](#object-find) | Object | An event response to search, with no stat requirement. | 1 ||
| [`fire`](Characters_and_Bosses.md#object-fire) | Object | An event response that uses fire, with no stat requirement. | 1 ||
| [`flush_yourself`](#object-flush_yourself) | Object | An event response to flush oneself, requiring a minimum counter value. | 1 ||
| [`follow`](#object-follow) | Object | A speed-based event response to pursue. | 1 ||
| [`free`](#object-free) | Object | If true, this option requires no cost to activate. | 1 ||
| [`future`](#object-future) | Object | Specifies the name, map flag, or connection for the Future area. | 1 ||
| [`give_parasite`](#object-give_parasite) | Object | An event response to give a parasite, requiring the cat to have a parasite. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`hack`](#object-hack) | Object | An intelligence-based event response to hack a system. | 1 ||
| [`head`](./Events_and_Encounters.md#context-head) | Enum / Number | The catalog ID for the cat's head part. | 1 ||
| [`holy`](Characters_and_Bosses.md#object-holy) | Object | An event response that uses holy power, with no stat requirement. | 1 ||
| [`hp`](#object-hp) | Object | An event response that trades health, with no stat requirement. | 1 ||
| [`ice`](Engine_LogicKeys.md#object-ice) | Object | An event response that uses ice, with no stat requirement. | 1 ||
| [`infinite`](#object-infinite) | Object | An event response to choose infinite, with a chapter exit hint and no stat requirement. | 1 ||
| [`intcheck`](#object-intcheck) | Object | An intelligence-based event response to test intellect. | 1 ||
| [`intimidation`](#object-intimidation) | Object | An event response that intimidates, with no stat requirement. | 1 ||
| [`itchies`](#object-itchies) | Object | An event response that causes itches, with no stat requirement. | 1 ||
| [`join`](#object-join) | Object | A charisma-based event response to join in. | 1 ||
| [`jump`](#object-jump) | Object | A speed-based event response to leap. | 1 ||
| [`jump_over`](#object-jump_over) | Object | A dexterity-based event response to vault over. | 1 ||
| [`keep_going`](#object-keep_going) | Object | An event response to persevere, with no stat requirement. | 1 ||
| [`kiss_meat`](#object-kiss_meat) | Object | A charisma-based event response to kiss meat. | 1 ||
| [`knife`](#object-knife) | Object | An event response to obtain a knife, with no stat requirement. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`leave_it_in`](#object-leave_it_in) | Object | An event response to leave an object in place, with no stat requirement. | 1 ||
| [`leg`](#object-leg) | Object | A luck-based event response to use a leg. | 1 ||
| [`lever`](#object-lever) | Object | An event response to pull a lever, with a fixed chance and no stat requirement. | 1 ||
| [`lick_alt`](#object-lick_alt) | Object | A constitution-based event response to lick, restricted to specific chapters. | 1 ||
| [`lightning`](#object-lightning) | Object | An event response using lightning, with no stat requirement. | 1 ||
| [`listen`](#object-listen) | Object | An intelligence-based event response to listen. | 1 ||
| [`looks`](#object-looks) | Object | The dialogue option for the Genie good event that selects the looks reward. | 1 ||
| [`loot_heart`](#object-loot_heart) | Object | The dialogue option to take the heart from the Dead King as a quest action. | 1 ||
| [`makeup`](#object-makeup) | Object | The dialogue option for the makeup event, associated with the Tink2 encounter. | 1 ||
| [`mind`](#object-mind) | Object | The dialogue option for the Genie bad event that selects the curse mind reward. | 1 ||
| [`neck`](./Events_and_Encounters.md#context-neck) | Enum | The neck equipment item assigned to the unit. | 1 ||
| [`nothanks`](#object-nothanks) | Object | The generic decline dialogue option that triggers a leave animation. | 1 ||
| [`outsmart`](#object-outsmart) | Object | The dialogue option that uses the int stat to outsmart the tutorial encounter. | 1 ||
| [`patch_up`](#object-patch_up) | Object | The dialogue option that uses the int stat to patch up the dying fetus. | 1 ||
| [`pick_lock`](#object-pick_lock) | Object | The dialogue option that uses the dex stat to pick a lock on a crate. | 1 ||
| [`pilfer`](#object-pilfer) | Object | The dialogue option that uses the lck stat to pilfer from a pile of skulls. | 1 ||
| [`pirouette`](#object-pirouette) | Object | The dialogue option for the Tink1 encounter that performs a pirouette. | 1 ||
| [`place_gristle`](#object-place_gristle) | Object | The dialogue option to place gristle on the Wall of Flesh as a quest action. | 1 ||
| [`power`](#object-power) | Object | The dialogue option for the Genie good event that selects the power reward. | 1 ||
| [`pull`](#object-pull) | Object | The dialogue option that uses the str stat to pull a knife from a wall. | 1 ||
| [`pull_it_out`](#object-pull_it_out) | Object | The dialogue option to pull out a stalactite from the Jagged Pathway. | 1 ||
| [`pull_lever`](#object-pull_lever) | Object | The dialogue option to pull the lever on the Odd Device. | 1 ||
| [`purify`](#object-purify) | Object | The dialogue option that uses the lck stat to purify the Mysterious Chamber. | 1 ||
| [`push_buttons`](#object-push_buttons) | Object | The dialogue option to push buttons on the Odd Device. | 1 ||
| [`push_through`](#object-push_through) | Object | The dialogue option that uses the str stat to push through the Jagged Pathway. | 1 ||
| [`put_in_coins`](#object-put_in_coins) | Object | The dialogue option to put coins into the Vending Machine, requiring a minimum of 10 coins. | 1 ||
| [`put_out_of_misery`](#object-put_out_of_misery) | Object | The dialogue option that uses the str stat to put the dying fetus out of its misery. | 1 ||
| [`reach_inside`](#object-reach_inside) | Object | The dialogue option that uses the spd stat to reach inside a Small Black Hole. | 1 ||
| [`read`](#object-read) | Object | The dialogue option that uses the int stat to read the Mysterious Manual. | 1 ||
| [`receive`](#object-receive) | Object | The dialogue option to receive an item from a legacy event. | 1 ||
| [`red`](#object-red) | Object | Configuration for one of the dialog options (label 'EVENT_RED_ANSW'), with a fixed chance and associated animation, in a choice event. | 1 ||
| [`red_needle`](#object-red_needle) | Object | The dialogue option that uses the lck stat to select the red needle, requiring not having the RedNeedle token. | 1 ||
| [`reflect`](Engine_StatusAndPassiveKeys.md#object-reflect) | Object | The dialogue option for the StacyMutant4 encounter that chooses to reflect. | 1 ||
| [`remove`](#object-remove) | Object | The dialogue option that uses the str stat to remove a stuck corpse. | 1 ||
| [`remove_the_nail`](#object-remove_the_nail) | Object | The dialogue option that uses the dex stat to remove the nail from a big toe. | 1 ||
| [`repair_quest`](#object-repair_quest) | Object | The dialogue option to repair the broken time machine as a quest action. | 1 ||
| [`rest`](#object-rest) | Object | The dialogue option that uses the lck stat to rest on a cat bed. | 1 ||
| [`revive`](Engine_StatusAndPassiveKeys.md#object-revive) | Object | The dialogue option that uses the lck stat to revive the Dead Mammoth. | 1 ||
| [`rub`](#object-rub) | Object | The dialogue option that uses the lck stat to rub the Genie Lamp. | 1 ||
| [`run_again`](#object-run_again) | Object | The dialogue option that uses the spd stat to run away from Death again, requiring he hasn't chased you yet. | 1 ||
| [`run_away`](#object-run_away) | Object | The dialogue option that uses the spd stat to run away from a Giant Sleeping Shark. | 1 ||
| [`sacrifice_full_favor`](#object-sacrifice_full_favor) | Object | The dialogue option to sacrifice a cat at the Volcano with full favor as a quest action. | 1 ||
| [`sacrifice_normal`](#object-sacrifice_normal) | Object | The dialogue option to perform a normal sacrifice at the Meat Altar, requiring the GuillotinasHead not equipped. | 1 ||
| [`sacrifice_partial_favor`](#object-sacrifice_partial_favor) | Object | The dialogue option to sacrifice a cat at the Volcano with partial favor as a quest action. | 1 ||
| [`sacrifice_quest`](#object-sacrifice_quest) | Object | The dialogue option to perform a quest sacrifice at the Meat Altar, requiring the GuillotinasHead equipped. | 1 ||
| [`scream`](#object-scream) | Object | The dialogue option to scream at the Meat Golem with no stat requirement. | 1 ||
| [`shake`](#object-shake) | Object | The dialogue option that uses the str stat to shake the Vending Machine. | 1 ||
| [`slip_through`](#object-slip_through) | Object | The dialogue option that uses the dex stat to slip through a Barbed Wire Fence. | 1 ||
| [`sneak_by`](#object-sneak_by) | Object | The dialogue option that uses the dex stat to sneak by a Giant Sleeping Shark. | 1 ||
| [`sneak_past_alt`](#object-sneak_past_alt) | Object | The dialogue option using dex to sneak past a stray cat, available only in the Ice Age or Jurassic chapters. | 1 ||
| [`soul`](#object-soul) | Object | The dialogue option for the Genie bad event that selects the curse soul reward. | 1 ||
| [`speed`](./Events_and_Encounters.md#context-speed) | Array / Number | The speed of the projectile or move, can be a value or a range. | 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||
| `stat_max` | Number || 1 ||
| `stat_min` | Number || 1 ||
| [`surprise`](#object-surprise) | Object | The dialogue option for the Butch2 encounter that surprises the target. | 1 ||
| [`sweet_talk`](#object-sweet_talk) | Object | The dialogue option that uses the cha stat to sweet-talk Death. | 1 ||
| [`swim`](#object-swim) | Object | The dialogue option that uses the str stat to swim through a Strong Current. | 1 ||
| [`tail`](./Events_and_Encounters.md#context-tail) | Integer | The catalog ID for the cat's tail part. | 1 ||
| [`take_blood`](#object-take_blood) | Object | The dialogue option to drain blood from the Dead King as a quest action. | 1 ||
| [`talk`](#object-talk) | Object | The dialogue option that uses the cha stat to talk to a Spookie Apparation. | 1 ||
| [`talk_to`](#object-talk_to) | Object | The dialogue option that uses the cha stat to talk to someone during a Dust Storm. | 1 ||
| [`tappytoes`](#object-tappytoes) | Object | The dialogue option for the Tink1 encounter that performs a tappytoes action. | 1 ||
| [`teleport`](#object-teleport) | Object | Defines a dialogue option that transports the unit to an alternative location in the event. | 1 ||
| [`thorns`](#object-thorns) | Object | Defines a dialogue option that applies a thorns effect to the unit. | 1 ||
| [`throw`](#object-throw) | Object | Defines a dialogue option that allows the unit to throw an object. | 1 ||
| [`timemachine`](#object-timemachine) | Object | Defines a dialogue option that triggers a time travel sequence. | 1 ||
| [`traverse`](#object-traverse) | Object | Defines a dialogue option that moves the unit through a traversal area. | 1 ||
| [`upgrade_yourself`](#object-upgrade_yourself) | Object | Defines a dialogue option that upgrades the unit's attributes or abilities. | 1 ||
| [`use_item`](#object-use_item) | Object | Defines a dialogue option that prompts the unit to use an item from their inventory. | 1 ||
| [`use_toilet_con`](#object-use_toilet_con) | Object | Defines a dialogue option that interacts with a toilet using the Constitution stat. | 1 ||
| [`use_toilet_str`](#object-use_toilet_str) | Object | Defines a dialogue option that interacts with a toilet using the Strength stat. | 1 ||
| [`use_weapon`](#object-use_weapon) | Object | Defines a dialogue option that prompts the unit to use their equipped weapon. | 1 ||
| [`w1`](#object-w1) | Object | Defines a dialogue option for the first weather choice in the Crater Weather event. | 1 ||
| [`w2`](#object-w2) | Object | Defines a dialogue option for the second weather choice in the Crater Weather event. | 1 ||
| [`w3`](#object-w3) | Object | Defines a dialogue option for the third weather choice in the Crater Weather event. | 1 ||
| [`w4`](#object-w4) | Object | Defines a dialogue option for the fourth weather choice in the Crater Weather event. | 1 ||
| [`w5`](#object-w5) | Object | Defines a dialogue option for the fifth weather choice in the Crater Weather event. | 1 ||
| [`w6`](#object-w6) | Object | Defines a dialogue option for the sixth weather choice in the Crater Weather event. | 1 ||
| [`wealth`](#object-wealth) | Object | Defines a dialogue option that grants the unit money or valuable items. | 1 ||
| [`wheezies`](#object-wheezies) | Object | Defines a dialogue option that triggers a wheezing effect or condition. | 1 ||
| [`wish_genes`](#object-wish_genes) | Object | Defines a dialogue option in the Monkey Paw event that modifies the unit's genetics. | 1 ||
| [`wish_items`](#object-wish_items) | Object | Defines a dialogue option in the Monkey Paw event that grants items. | 1 ||
| [`wish_levelups`](#object-wish_levelups) | Object | Defines a dialogue option in the Monkey Paw event that grants level-ups. | 1 ||
| [`wish_strength`](#object-wish_strength) | Object | Defines a dialogue option in the Monkey Paw event that increases Strength. | 1 ||
| [`withstand`](#object-withstand) | Object | Defines a dialogue option that allows the unit to withstand a hazard using Constitution. | 1 ||
| [`yank_it_out`](#object-yank_it_out) | Object | Defines a dialogue option that yanks out an object using Strength. | 1 ||
| [`yellow_needle`](#object-yellow_needle) | Object | Defines a dialogue option to interact with a yellow needle. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 131 ||
| [`Fear`](./Enums.md) | Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 29 | 2 |
| [`Poison`](./Enums.md) | Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 28 | 4 |
| [`Bleed`](./Enums.md) | Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 20 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 13 |
| [`AllStatsUp`](./Enums.md) | Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 7 | 1 |
| [`SpeedUp`](./Enums.md) | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 5 | -2 |
| [`StrengthUp`](./Enums.md) | Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 5 | 2 |
| [`AbilityOnBattleStart_Immediate`](./Enums.md) | Enum || 4 | Flush |
| [`ConstitutionUp`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 4 | -1 |
| [`AddStartingMana`](./Enums.md) | Integer | The amount of bonus mana the unit starts each battle with. | 3 | 5 |
| [`Burn`](./Enums.md) | Integer | The amount of Burn applied, either as a fixed number or a formula string. | 3 | 5 |
| [`CharismaUp`](./Enums.md) | Integer | The amount of charisma change, or a keyword like 'item_aux'. | 3 | -2 |
| [`Confusion`](./Enums.md) | Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 3 | 2 |
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 3 | 2 |
| [`Webbed`](./Enums.md) | Integer | The amount of webbed stacks applied, or an [stacks, probability] array. | 3 | 2 |
| [`Blind`](./Enums.md) | Integer | The amount of blind stacks applied, or an [stacks, probability] array. | 2 | 6 |
| [`Bruise`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 2 | 1 |
| [`DexterityUp`](./Enums.md) | Integer | The amount of dexterity change, or a keyword like 'item_aux'. | 2 | 2 |
| [`IntelligenceUp`](./Enums.md) | Integer | The amount of Intelligence added as a flat bonus. | 2 | 3 |
| [`NoHealthRegen`](./Enums.md) | Integer | Prevents the unit from regenerating health normally. | 2 | 1 |
| [`Sleep`](./Enums.md) | Integer | The amount of sleep stacks applied, or an [stacks, probability] array. | 2 | 2 |
| [`Stun`](./Enums.md) | Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 2 | 1 |
| [`AbilityOnBattleStart`](./Enums.md) | Enum || 1 | Flush |
| [`AddInitiative`](./Enums.md) | Integer | The amount of bonus or penalty to the unit's turn order initiative value. | 1 | -99 |
| [`AlphaTurns`](./Enums.md) | Integer | The number of turns the unit acts first in battle; negative values may indicate last. | 1 | 1 |
| [`ChangeTileUnderCharacterAtStart`](./Enums.md) | Enum || 1 | GlassTile |
| [`DivineShield`](./Enums.md) | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | 2 |
| [`Fights`](./Enums.md) | Integer || 1 | 3 |
| [`LuckUp`](./Enums.md) | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 1 | 1 |
| [`Madness`](./Enums.md) | Integer | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 1 | 1 |
| [`MissChance`](./Enums.md) | Integer | The flat percentage chance that the unit's attacks will miss. | 1 | 10 |
| [`NoManaRegen`](./Enums.md) | Integer | The unit does not naturally regenerate mana per turn. Value indicates the stage or flag enabling this restriction. | 1 | 1 |
| [`PermanentConfusion`](./Enums.md) | Integer | If set to 1, the unit is permanently confused and cannot be cured. | 1 | 1 |
| [`ProbeCharmed`](./Enums.md) | Integer | The number of charm stacks applied by a probe. | 1 | 1 |
| [`RandomStatUp`](./Enums.md) | Integer | The amount of random stat increase applied, either as a fixed number or a formula string. | 1 | 1 |
| [`Rot`](./Enums.md) | Integer | Integer, or an array [stacks, probability] specifying the amount of Rot stacks applied with the given probability. | 1 | 2 |
| [`Slow`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 1 | 3 |
| [`SpiderInfested`](./Enums.md) | Integer | The number of spider infestation stacks applied. | 1 | 1 |
| [`Tarred`](./Enums.md) | Integer | The amount of tarred stacks applied, or an [stacks, probability] array. | 1 | 1 |
| [`TempStrengthUp`](./Enums.md) | Integer | The number of stacks of temporary Strength Up applied to the unit. | 1 | 1 |

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
| `con` | Enum / Integer | The Constitution stat value or modifier. | 37 ||
| `random` | Number || 25 ||
| `int` | Enum / Integer || 23 ||
| `lck` | Enum / Integer || 20 ||
| `spd` | Enum / Integer | The Speed stat value or modifier. | 20 ||
| `str` | Enum / Integer || 18 ||
| [`cha`](./Engine_EventKeys.md#valid-property-keys) | Variable | The Charisma stat value or modifier. | 16 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 125 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 125 ||
| [`reward`](#object-reward) | Object | An object containing sub-objects defining the rewards for different rarity tiers (e.g., common, rare), each with their own set of actions and items. | 125 ||
| [`else`](Abilities_and_Spells.md#object-else) | Object | Specifies the fallback outcome when the primary condition in a conditional reward is not met. | 37 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 57 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 57 ||
| [`label`](./Strings.md#string-label) | Variable || 57 ||
| [`stat`](./Enums.md#enum-stat) | Variable || 56 ||
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 55 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 4 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 3 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 41 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 41 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 32 ||
| [`copy_results`](./Enums.md#enum-copy_results) | Enum || 3 ||
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||

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
| [`object`](./Arrays.md#array-object) | Array / Enum | Specifies the object or unit to be spawned. | 40 ||
| [`count`](./Arrays.md#array-count) | Array / Integer | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 34 ||
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
| [`pool`](./Enums.md#enum-pool) | Array / Enum | Specifies the name of the pool from which an ability is learned or an item is crafted. | 39 ||
| [`restrict`](./Arrays.md#array-restrict) | Array || 30 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 38 ||
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | `String` || 20 ||
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | `String` || 6 ||
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | `String` || 6 ||
| `party_damage` | `Number` || 6 ||
| `set_frame` | `Number` || 5 ||
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | `String` || 4 ||
| [`conditional_reward`](#object-conditional_reward) | Object || 4 ||
| [`random_pool`](./Enums.md) | Array || 3 | [event_now] |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | `Array` | Grants an item from the specified pool or a specific item name. | 2 ||
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | `String` || 2 ||
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Specifies the amount of damage dealt, can be a number or expression. | 1 ||
| `next_event_bonus` | `Number` || 1 ||
| [`random_mutation`](#object-random_mutation) | Object | The number of random mutations applied to the unit. | 1 ||
| [`self_status_next_fight`](#object-self_status_next_fight) | Object | An object defining status effects applied to the unit at the start of the next fight. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 32 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 32 ||
| [`label`](./Strings.md#string-label) | String || 32 ||
| [`stat`](./Enums.md#enum-stat) | Variable || 32 ||
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 30 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 3 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 25 ||
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 25 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 25 ||
| [`label`](./Strings.md#string-label) | Variable || 25 ||
| [`stat`](./Math_Equations.md) | Equation || 25 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 23 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 2 ||

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
| `mouth` | Number | The catalog ID for the cat's mouth part. | 11 ||
| `ears` | Number || 10 ||
| `eyebrows` | Number || 8 ||
| `head` | Enum / Number | The catalog ID for the cat's head part. | 7 ||
| `legs` | Number || 7 ||
| `arms` | Number || 6 ||
| `body` | Number | The catalog ID for the cat's body part. | 6 ||
| `tail` | Integer | The catalog ID for the cat's tail part. | 6 ||
| `eye1` | Integer | The catalog ID for the cat's first eye part. | 3 ||
| `arm1` | Number | The catalog ID for the cat's first arm part. | 2 ||
| `ear1` | Integer || 2 ||
| `eyebrow1` | Integer | The catalog ID for the cat's first eyebrow part. | 2 ||
| `leg1` | Integer | The catalog ID for the cat's first leg part. | 2 ||
| `eye2` | Integer | The catalog ID for the cat's second eye part. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 22 ||
| [`Fear`](./Enums.md) | Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 6 | 2 |
| [`Poison`](./Enums.md) | Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 5 | 4 |
| [`AbilityOnBattleStart_Immediate`](./Enums.md) | Enum || 3 | Flush |
| [`NoHealthRegen`](./Enums.md) | Integer | Prevents the unit from regenerating health normally. | 3 | 1 |
| [`Bleed`](./Enums.md) | Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 1 | 2 |
| [`DivineShield`](./Enums.md) | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | 2 |
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 1 | 2 |
| [`Immobile`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 1 | 1 |
| [`Tangled`](./Enums.md) | Integer | The number of stacks of the Tangled status effect applied, or an object defining its properties such as `stacks` and `alt_art`. | 1 | 2 |
| [`Tarred`](./Enums.md) | Integer | The amount of tarred stacks applied, or an [stacks, probability] array. | 1 | 1 |
| [`Webbed`](./Enums.md) | Integer | The amount of webbed stacks applied, or an [stacks, probability] array. | 1 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 |

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 23 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 23 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 23 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 23 ||
| [`conditional_reward`](#object-conditional_reward) | Object | An object defining a reward that is granted only if specified conditions are met. | 20 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 21 ||
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | `String` | Specifies the name of a cutscene to play. | 21 ||
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
| `mouth` | Number | The catalog ID for the cat's mouth part. | 9 ||
| `count` | Array / Integer | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 8 ||
| `tail` | Integer | The catalog ID for the cat's tail part. | 6 ||
| `ears` | Number || 5 ||
| `eyes` | Number || 5 ||
| `legs` | Number || 5 ||
| `body` | Number | The catalog ID for the cat's body part. | 3 ||
| `eyebrows` | Number || 3 ||
| `head` | Enum / Number | The catalog ID for the cat's head part. | 3 ||
| `arm1` | Number | The catalog ID for the cat's first arm part. | 2 ||
| `arm2` | Number | The catalog ID for the cat's second arm part. | 2 ||
| `leg1` | Integer | The catalog ID for the cat's first leg part. | 1 ||
| `leg2` | Integer | The catalog ID for the cat's second leg part. | 1 ||
| `texture` | Integer | The catalog ID for the cat's texture. | 1 ||

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
| `count` | Array / Integer | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 15 ||
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specifies the tag(s) to check on the target, used in conditional effects. | 12 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 14 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 14 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 12 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 14 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 14 ||
| [`label`](./Strings.md#string-label) | String || 14 ||
| [`stat`](./Math_Equations.md) | Equation || 14 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 13 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 12 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 12 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 12 ||
| [`label`](./Strings.md#string-label) | String || 12 ||
| [`stat`](./Math_Equations.md) | Equation || 12 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 8 ||
| [`Fights`](./Enums.md) | Integer || 6 | 3 |
| [`CharacterTypeGainsStatusAtBattleStart`](Engine_LogicKeys.md#object-charactertypegainsstatusatbattlestart) | Object || 5 ||
| [`StatusRandomEnemiesOnBattleStart`](#object-statusrandomenemiesonbattlestart) | Object || 3 ||
| [`KillEnemyOfTypeAtBattleStart`](Engine_StatusAndPassiveKeys.md#object-killenemyoftypeatbattlestart) | Object | Specifies that a specific enemy type is killed at the start of the next battle. | 2 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 |

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 7 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 7 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 7 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 11 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 11 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 11 ||
| [`label`](./Strings.md#string-label) | Variable || 11 ||
| [`stat`](./Math_Equations.md) | Equation || 11 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 8 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 8 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 8 ||
| [`label`](./Strings.md#string-label) | String || 8 ||
| [`stat`](./Math_Equations.md) | Equation || 8 ||
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 7 ||
| [`label`](./Strings.md#string-label) | String || 7 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 7 ||
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 5 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 7 ||
| [`label`](./Strings.md#string-label) | String || 7 ||
| [`stat`](./Math_Equations.md) | Equation || 7 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 6 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 6 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 7 ||
| [`label`](./Strings.md#string-label) | String || 7 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 7 ||
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 5 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 7 ||
| [`label`](./Strings.md#string-label) | String || 7 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 7 ||
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 5 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 7 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 7 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 7 ||
| [`label`](./Strings.md#string-label) | Variable || 7 ||
| [`stat`](./Math_Equations.md) | Equation || 7 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 7 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 7 ||
| [`label`](./Strings.md#string-label) | Variable || 7 ||
| [`stat`](./Math_Equations.md) | Equation || 7 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 6 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 7 ||
| [`label`](./Strings.md#string-label) | Variable || 7 ||
| [`stat`](./Enums.md#enum-stat) | Variable || 7 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 7 ||
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 6 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 6 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 6 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 6 ||
| [`label`](./Enums.md#enum-label) | Enum || 6 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 6 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 6 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 6 ||
| [`label`](./Enums.md#enum-label) | Enum || 6 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 6 ||
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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 6 ||
| [`label`](./Strings.md#string-label) | String || 6 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 6 ||
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 5 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 6 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 6 ||
| [`label`](./Strings.md#string-label) | Variable || 6 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 5 ||
| [`stat`](./Enums.md#enum-stat) | Variable || 5 ||
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
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
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 6 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 6 ||
| [`label`](./Strings.md#string-label) | String || 6 ||
| [`stat`](./Math_Equations.md) | Equation || 6 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 6 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 6 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 6 ||
| [`label`](./Strings.md#string-label) | Variable || 6 ||
| [`stat`](./Enums.md#enum-stat) | Variable || 6 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 5 ||
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||

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
| `count` | Array / Integer | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 4 ||

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
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specifies the tag(s) to check on the target, used in conditional effects. | 8 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 8 ||
| [`Fear`](./Enums.md) | Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 3 | 2 |
| [`Stun`](./Enums.md) | Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 2 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 |
| [`AllStatsUp`](./Enums.md) | Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | 1 |

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 5 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 5 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 5 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 5 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 5 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 5 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 5 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 5 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 5 ||
| [`label`](./Strings.md#string-label) | String || 5 ||
| [`stat`](./Math_Equations.md) | Equation || 5 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 2 ||
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 4 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 4 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 4 ||
| [`label`](./Enums.md#enum-label) | Enum || 4 ||
| [`stat`](./Math_Equations.md) | Equation || 4 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 4 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 4 ||
| [`label`](./Strings.md#string-label) | String || 4 ||
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 3 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 4 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 4 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 4 ||
| [`label`](./Strings.md#string-label) | String || 4 ||
| [`stat`](./Enums.md#enum-stat) | Variable || 3 ||
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 2 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 4 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 4 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 4 ||
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
| `cha` | Enum / Integer | The Charisma stat value or modifier. | 4 ||
| `con` | Enum / Integer | The Constitution stat value or modifier. | 4 ||
| `dex` | Enum / Integer || 4 ||
| `int` | Enum / Integer || 4 ||
| `lck` | Enum / Integer || 4 ||
| `spd` | Enum / Integer | The Speed stat value or modifier. | 4 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 4 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 4 ||
| [`hint_chapter_exit`](./Enums.md#enum-hint_chapter_exit) | Enum || 4 ||
| [`label`](./Enums.md#enum-label) | Enum || 4 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 4 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 4 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 4 ||
| [`label`](./Strings.md#string-label) | String || 4 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 4 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 4 ||

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
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 3 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 3 ||
| [`label`](./Strings.md#string-label) | String || 3 ||
| [`stat`](./Math_Equations.md) | Equation || 3 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 3 ||

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
| `con` | Enum / Integer | The Constitution stat value or modifier. | 2 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 3 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 3 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 3 ||
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
| `count` | Array / Integer | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 7 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 7 ||
| [`Fear`](./Enums.md) | Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 3 | 2 |
| [`Bleed`](./Enums.md) | Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 1 | 2 |

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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 2 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 ||
| [`label`](./Enums.md#enum-label) | Enum || 2 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 2 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 2 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 ||
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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 ||
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
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 2 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 ||
| [`label`](./Strings.md#string-label) | String || 2 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 2 ||
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
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
| `initial_health` | Integer | The starting health of the unit when spawned. | 1 ||
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the object or unit to be spawned. | 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 2 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 2 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 ||
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
| `count` | Array / Integer | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 2 ||
| `ears` | Number || 2 ||
| `eyebrows` | Number || 2 ||
| `eyes` | Number || 2 ||
| `mouth` | Number | The catalog ID for the cat's mouth part. | 2 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 2 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 2 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 2 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 ||
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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 2 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 1 ||
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | `String` | Grants an item from the specified pool or a specific item name. | 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 ||
| [`label`](./Strings.md#string-label) | Variable || 2 ||
| [`stat`](./Enums.md#enum-stat) | Variable || 2 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 2 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 ||
| [`label`](./Strings.md#string-label) | String || 2 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 2 ||
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||
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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 ||
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
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 2 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 ||
| [`label`](./Strings.md#string-label) | String || 2 ||
| [`stat`](./Math_Equations.md) | Equation || 2 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 2 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Enums.md#enum-label) | Enum || 1 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Enums.md#enum-label) | Enum || 1 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||
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
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`label`](./Enums.md#enum-label) | Enum || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||

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
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||

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
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum || 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum || 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum || 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum || 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Enums.md#enum-label) | Enum || 1 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Enums.md#enum-label) | Enum || 1 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||
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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`hint_chapter_exit`](./Enums.md#enum-hint_chapter_exit) | Enum || 1 ||
| [`label`](./Enums.md#enum-label) | Enum || 1 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||
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
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the object or unit to be spawned. | 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`hint_chapter_exit`](./Enums.md#enum-hint_chapter_exit) | Enum || 1 ||
| [`label`](./Enums.md#enum-label) | Enum || 1 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||
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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| `fixed_chance` | Number || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Enums.md#enum-label) | Enum || 1 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Enums.md#enum-label) | Enum || 1 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||
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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum || 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||
| `stat_max` | Number || 1 ||
| `stat_min` | Number || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||

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
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| `fixed_chance` | Number || 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Enums.md#enum-label) | Enum || 1 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||
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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||
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
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Enums.md#enum-label) | Enum || 1 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Enums.md#enum-label) | Enum || 1 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||
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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Enums.md#enum-label) | Enum || 1 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Math_Equations.md) | Equation || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`stat`](./Enums.md#enum-stat) | Enum || 1 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||

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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||
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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||
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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||
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
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 1 ||
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](./Events_and_Encounters.md#context-good) | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| [`label`](./Strings.md#string-label) | String || 1 ||
| [`requirements`](#object-requirements) | Object | An object defining the conditions that must be met for a reward or event branch to be available. | 1 ||
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
| `animation` | String | Specifies the animation played when the ability is used. | 1 | `choice_coins_ten` |
| `animation_fail` | String | Specifies the animation to play when an action fails. | 1 | `choice_no_coins` |
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](#object-good) | Object | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| `label` | String | Specifies the localization key or display string for an event option. | 1 | `"EVENT_BUY_ANSW"` |
| `stat` | String | Specifies the stat used for a success check in an event option. | 1 | `coins` |
| `stat_max` | Number | The maximum stat value required for an event option to succeed. | 1 | `10` |
| `stat_min` | Number | The minimum stat value required for an event option to succeed. | 1 | `10` |

</details>

### Object: `buy3`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation` | String | Specifies the animation played when the ability is used. | 1 | `choice_coins_twentyfive` |
| `animation_fail` | String | Specifies the animation to play when an action fails. | 1 | `choice_no_coins` |
| [`bad`](#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 ||
| [`good`](#object-good) | Object | If true, indicates the positive outcome branch for events or spawning contexts. | 1 ||
| `label` | String | Specifies the localization key or display string for an event option. | 1 | `"EVENT_BUY_ANSW"` |
| `stat` | String | Specifies the stat used for a success check in an event option. | 1 | `coins` |
| `stat_max` | Number | The maximum stat value required for an event option to succeed. | 1 | `25` |
| `stat_min` | Number | The minimum stat value required for an event option to succeed. | 1 | `25` |

</details>

### Object: `pick`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation` | String | Specifies the animation played when the ability is used. | 3 | `choice_dex_alt` |
| `copy_results` | String | Specifies the identifier of another option whose outcomes are replicated. | 3 | `examine` |
| `label` | String | Specifies the localization key or display string for an event option. | 3 | `"EVENT_PICK_ANSW"` |
| `stat` | String | Specifies the stat used for a success check in an event option. | 3 | `dex` |

</details>
