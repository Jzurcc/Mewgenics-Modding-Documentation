# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Events & Encounters

> **Associated Files:** `data/events/`


### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 214

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 229 |
| [`intro`](./Events_and_Encounters.md#context-intro) | Object | Event Node: The initial text block when a story event first loads. | 214 |
| [`main`](./Events_and_Encounters.md#context-main) | Object | Event Node: The central hub or recurring menu of a story event. | 214 |
| [`label`](./Strings.md#string-label) | String |  | 16 |
| [`stat`](./Enums.md#enum-stat) | Mixed |  | 16 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 12 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 11 |
| [`copy_results`](./Enums.md#enum-copy_results) | Enum |  | 8 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the 'Good' action. | 8 |
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum |  | 4 |
| `stat_max` | Number |  | 4 |
| `stat_min` | Number |  | 4 |
| [`open`](./Events_and_Encounters.md#context-open) | Object | Examples: `{ ... }` | 3 |
| `pick` | Object | Examples: `{ ... }` | 3 |
| `cha` | Number |  | 2 |
| `con` | Number |  | 2 |
| [`ignore`](./Events_and_Encounters.md#context-ignore) | Object | Event Node: Story branch or dialog option representing the \'Ignore\' action. | 2 |
| `int` | Number |  | 2 |
| `lck` | Number |  | 2 |
| `spd` | Number |  | 2 |
| `str` | Number |  | 2 |
| `buy2` | Object | Examples: `{ ... }` | 1 |
| `buy3` | Object | Examples: `{ ... }` | 1 |
| [`destroy`](./Events_and_Encounters.md#context-destroy) | Object | Event Node: Story branch or dialog option representing the \'Destroy\' action. | 1 |
| `dex` | Number |  | 1 |
| [`examine`](./Events_and_Encounters.md#context-examine) | Object | Examples: `{ ... }` | 1 |
| [`smash`](./Events_and_Encounters.md#context-smash) | Object | Examples: `{ ... }` | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`common`](./Events_and_Encounters.md#object-common) | Object | Event Node: Story branch or dialog option representing the 'Common' action. | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_coins`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_familiar`](./Events_and_Encounters.md#object-gain-familiar) | Enum/String | Event Action: Adds a specific familiar to the party. | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| [`goto`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`leave`](./Events_and_Encounters.md#object-leave) | Object | Event Node: Story branch or dialog option representing the 'Leave' action. | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `max_options` | Number |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Enum/String | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`options`](./Events_and_Encounters.md#object-options) | Object | Event Block: Lists the available clickable dialog choices for the current story node. | 0 |
| [`outcome`](./Events_and_Encounters.md#object-outcome) | Object | Event Block: Logic and text executed after selecting a specific dialog option. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_damage`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| `party_heal` | Number |  | 0 |
| [`party_permanent_stats`](./Events_and_Encounters.md#object-party-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of all party members. | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`random_chance`](./Events_and_Encounters.md#object-random-chance) | Object | Event Logic: Executes the nested outcome based on a percentage roll. | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`requires_flag`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` | Prerequisite: Must meet this condition. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_damage`](./Engine_DamagingKeys.md#valid-property-keys) | Array | Recoil or self-inflicted damage/effects applied to the caster. | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | `Number` |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`set_subject`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`setup`](./Events_and_Encounters.md#object-setup) | Object | Event Block: Pre-initialization logic executed before the event UI is drawn. | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `shuffle_options` | Boolean |  | 0 |
| [`spawn_unit_next_fight`](./Events_and_Encounters.md#object-spawn-unit-next-fight) | Object | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `weight` | `Number` | Probability weight for this outcome. | 0 |

</details>

---

### Object: `reward`



<details>
<summary><b>Expand</b></summary>

> **Total Count:** 757

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`bad`](./Events_and_Encounters.md#context-bad), [`conditional_reward`](./Events_and_Encounters.md#context-conditional_reward), [`good`](./Events_and_Encounters.md#context-good)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1364 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`ambush`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `ambush_next_basic_fights` | Number |  | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`clear_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clear_result_animation` | Number |  | 0 |
| [`common`](./Events_and_Encounters.md#object-common) | Object | Event Node: Story branch or dialog option representing the 'Common' action. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| `damage` | Number | Event Node: Story branch or dialog option representing the 'Damage' action. | 0 |
| [`decrement_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| `gain_cat_familiar` | Number |  | 0 |
| [`gain_coins`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_familiar`](./Events_and_Encounters.md#object-gain-familiar) | Enum/String | Event Action: Adds a specific familiar to the party. | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_and_equip_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| `hide_appearance_changes` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`leave_party_temporarily`](./Events_and_Encounters.md#object-leave-party-temporarily) | Object | Event Action: Removes a character from the active team until the next hub area. | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_all_equipped_items`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item_from_inventory`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`make_old`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Enum/String | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `party_damage` | Number |  | 0 |
| `party_heal` | Number |  | 0 |
| `party_heal_disorder` | Number |  | 0 |
| `party_heal_injury` | Number |  | 0 |
| [`party_injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`party_permanent_stats`](./Events_and_Encounters.md#object-party-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of all party members. | 0 |
| [`party_permanent_stats_exclude_self`](./Events_and_Encounters.md#object-party-permanent-stats-exclude-self) | Object | Event Reward: Permanently modifies stats for all party members except the one who initiated the action. | 0 |
| `party_random_mutation` | Number |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`party_status_next_fight`](./Events_and_Encounters.md#object-party-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect to the entire party at the start of the next combat encounter. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`play_result_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`random_chance`](./Events_and_Encounters.md#object-random-chance) | Object | Event Logic: Executes the nested outcome based on a percentage roll. | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_mutation_from_set`](./Events_and_Encounters.md#object-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to a character from a specific pool. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_basic_attack`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `self_damage` | Number | Recoil or self-inflicted damage/effects applied to the caster. | 0 |
| `self_heal` | Number |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| `set_age` | Number |  | 0 |
| `set_frame` | `Number` |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`set_subject`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `spawn_reflection_next_fight` | Number | Event Penalty: Spawns dark clones/reflections of the party in the next combat encounter. | 0 |
| [`spawn_unit_next_fight`](./Events_and_Encounters.md#object-spawn-unit-next-fight) | Object | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. | 0 |
| [`spin`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `weight` | `Number` | Probability weight for this outcome. | 0 |

</details>

---

### Object: `common`



<details>
<summary><b>Expand</b></summary>

> **Total Count:** 633

> **Referenced by:** [`reward`](./Events_and_Encounters.md#context-reward)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 658 |
| [`damage`](./Arrays.md#array-damage) | Array | Event Node: Story branch or dialog option representing the 'Damage' action. | 35 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| `ally_ambush_next_fights` | `Number` |  | 0 |
| `ambush_next_basic_fights` | `Number` |  | 0 |
| [`cha`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| `clear_result_animation` | `Number` |  | 0 |
| `con` | Number |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| [`decrement_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| `dex` | Number |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| `full_heal` | `Number` |  | 0 |
| [`gain_coins`](./Engine_EventKeys.md#valid-property-keys) | `Array` |  | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`gain_familiar`](./Events_and_Encounters.md#object-gain-familiar) | `Enum/String` | Event Action: Adds a specific familiar to the party. | 0 |
| `gain_food` | `Number` |  | 0 |
| [`get_and_equip_item`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | `Enum/String` | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | `Number` |  | 0 |
| `heal_disorder` | `Number` |  | 0 |
| `heal_injury` | `Number` |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | `Number` |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | `String` |  | 0 |
| `party_damage` | `Number` |  | 0 |
| `party_heal` | `Number` |  | 0 |
| `party_heal_disorder` | `Number` |  | 0 |
| [`party_permanent_stats_exclude_self`](./Events_and_Encounters.md#object-party-permanent-stats-exclude-self) | Object | Event Reward: Permanently modifies stats for all party members except the one who initiated the action. | 0 |
| [`party_status_next_fight`](./Events_and_Encounters.md#object-party-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect to the entire party at the start of the next combat encounter. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | `String` |  | 0 |
| `random` | Number |  | 0 |
| `random_mutation` | `Number` | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_mutation_from_set`](./Events_and_Encounters.md#object-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to a character from a specific pool. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | `Array` |  | 0 |
| `self_damage` | `Number` | Recoil or self-inflicted damage/effects applied to the caster. | 0 |
| `self_heal` | `Number` |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| `set_frame` | `Number` |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`spawn_unit_next_fight`](./Events_and_Encounters.md#object-spawn-unit-next-fight) | Object | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. | 0 |
| `spd` | Number |  | 0 |
| [`spin`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |

</details>

---

### Object: `rare`



<details>
<summary><b>Expand</b></summary>

> **Total Count:** 633

> **Referenced by:** [`attack`](./Events_and_Encounters.md#context-attack), [`good`](./Events_and_Encounters.md#context-good), [`loot`](./Events_and_Encounters.md#context-loot), [`main`](./Events_and_Encounters.md#context-main), [`options`](./Events_and_Encounters.md#context-options), [`reward`](./Events_and_Encounters.md#context-reward)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 705 |
| `damage` | Number | Event Node: Story branch or dialog option representing the 'Damage' action. | 18 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| `ally_ambush_next_fights` | `Number` |  | 0 |
| [`ambush`](./Engine_EventKeys.md#valid-property-keys) | `String` |  | 0 |
| `ambush_next_basic_fights` | `Number` |  | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | `String` |  | 0 |
| [`cha`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clear_result_animation` | `Number` |  | 0 |
| `con` | Number |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| [`decrement_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| `dex` | Number |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| `full_heal` | `Number` |  | 0 |
| `gain_cat_familiar` | `Number` |  | 0 |
| [`gain_coins`](./Engine_EventKeys.md#valid-property-keys) | `Array` |  | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`gain_familiar`](./Events_and_Encounters.md#object-gain-familiar) | `Enum/String` | Event Action: Adds a specific familiar to the party. | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | `Array` |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`get_and_equip_item`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | `Enum/String` | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal_disorder` | `Number` |  | 0 |
| `hide_appearance_changes` | `Number` |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`learn_ability`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`learn_passive`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`leave_party_temporarily`](./Events_and_Encounters.md#object-leave-party-temporarily) | Object | Event Action: Removes a character from the active team until the next hub area. | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`lose_all_equipped_items`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`lose_item_from_inventory`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`make_old`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | `Number` |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | `Enum/String` | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | `String` |  | 0 |
| `party_damage` | `Number` |  | 0 |
| `party_heal` | `Number` |  | 0 |
| `party_heal_disorder` | `Number` |  | 0 |
| `party_heal_injury` | `Number` |  | 0 |
| [`party_injury`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`party_permanent_stats`](./Events_and_Encounters.md#object-party-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of all party members. | 0 |
| [`party_permanent_stats_exclude_self`](./Events_and_Encounters.md#object-party-permanent-stats-exclude-self) | Object | Event Reward: Permanently modifies stats for all party members except the one who initiated the action. | 0 |
| `party_random_mutation` | `Number` |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`party_status_next_fight`](./Events_and_Encounters.md#object-party-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect to the entire party at the start of the next combat encounter. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | `Array` |  | 0 |
| [`play_result_animation`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | `String` |  | 0 |
| `random` | Number |  | 0 |
| `random_mutation` | `Number` | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_mutation_from_set`](./Events_and_Encounters.md#object-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to a character from a specific pool. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | `Array` |  | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`scramble_basic_attack`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| `self_damage` | `Number` | Recoil or self-inflicted damage/effects applied to the caster. | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| `set_age` | `Number` |  | 0 |
| `set_frame` | `Number` |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| `spawn_reflection_next_fight` | `Number` | Event Penalty: Spawns dark clones/reflections of the party in the next combat encounter. | 0 |
| [`spawn_unit_next_fight`](./Events_and_Encounters.md#object-spawn-unit-next-fight) | Object | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. | 0 |
| `spd` | Number |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |

</details>

---

### Object: `good`



<details>
<summary><b>Expand</b></summary>

> **Total Count:** 550

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`a`](./Events_and_Encounters.md#context-a), [`activate_p`](./Events_and_Encounters.md#context-activate_p), [`activate_z`](./Events_and_Encounters.md#context-activate_z), [`altar_sacrifice`](./Events_and_Encounters.md#context-altar_sacrifice), [`arm`](./Events_and_Encounters.md#context-arm), [`attach_amplifier`](./Events_and_Encounters.md#context-attach_amplifier), [`attach_antenna`](./Events_and_Encounters.md#context-attach_antenna), [`attach_leech`](./Events_and_Encounters.md#context-attach_leech), [`attack`](./Events_and_Encounters.md#context-attack), [`b`](./Events_and_Encounters.md#context-b), [`bash`](./Events_and_Encounters.md#context-bash), [`bash_past_alt`](./Events_and_Encounters.md#context-bash_past_alt), [`bite`](./Events_and_Encounters.md#context-bite), [`bite_it_off`](./Events_and_Encounters.md#context-bite_it_off), [`blue_needle`](./Events_and_Encounters.md#context-blue_needle), [`boogers`](./Events_and_Encounters.md#context-boogers), [`book`](./Events_and_Encounters.md#context-book), [`brace`](./Events_and_Encounters.md#context-brace), [`break_ice`](./Events_and_Encounters.md#context-break_ice), and 177 more...

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 464 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`ambush`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `ambush_next_basic_fights` | Number |  | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`clear_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clear_result_animation` | Number |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| `clone_self_to_party` | `Number` |  | 0 |
| [`common`](./Events_and_Encounters.md#object-common) | Object | Event Node: Story branch or dialog option representing the 'Common' action. | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | `Number` |  | 0 |
| `copy_party_items` | `Number` |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | `String` | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `damage` | Number | Event Node: Story branch or dialog option representing the 'Damage' action. | 0 |
| [`decrement_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| `gain_cat_familiar` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_coins`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_familiar`](./Events_and_Encounters.md#object-gain-familiar) | Enum/String | Event Action: Adds a specific familiar to the party. | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_and_equip_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | `Number` |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | `Number` |  | 0 |
| `hide_appearance_changes` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`leave_party_temporarily`](./Events_and_Encounters.md#object-leave-party-temporarily) | Object | Event Action: Removes a character from the active team until the next hub area. | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_all_equipped_items`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item_from_inventory`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`make_old`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Enum/String | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_damage`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | `Array` |  | 0 |
| `party_heal` | Number |  | 0 |
| `party_heal_disorder` | Number |  | 0 |
| `party_heal_injury` | Number |  | 0 |
| [`party_injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`party_permanent_stats`](./Events_and_Encounters.md#object-party-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of all party members. | 0 |
| [`party_permanent_stats_exclude_self`](./Events_and_Encounters.md#object-party-permanent-stats-exclude-self) | Object | Event Reward: Permanently modifies stats for all party members except the one who initiated the action. | 0 |
| `party_random_mutation` | Number |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`party_status_next_fight`](./Events_and_Encounters.md#object-party-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect to the entire party at the start of the next combat encounter. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`play_result_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`random_chance`](./Events_and_Encounters.md#object-random-chance) | Object | Event Logic: Executes the nested outcome based on a percentage roll. | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_mutation_from_set`](./Events_and_Encounters.md#object-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to a character from a specific pool. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | `Array` |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`scramble_basic_attack`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| `self_damage` | Number | Recoil or self-inflicted damage/effects applied to the caster. | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| `set_age` | Number |  | 0 |
| `set_frame` | `Number` |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`set_subject`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| `spawn_reflection_next_fight` | Number | Event Penalty: Spawns dark clones/reflections of the party in the next combat encounter. | 0 |
| [`spawn_unit_next_fight`](./Events_and_Encounters.md#object-spawn-unit-next-fight) | Object | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | `Array` |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| `trigger_butterfly_effect` | `Number` |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| `weight` | Number | Probability weight for this outcome. | 0 |

</details>

---

### Object: `bad`



<details>
<summary><b>Expand</b></summary>

> **Total Count:** 341

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`arm`](./Events_and_Encounters.md#context-arm), [`attack`](./Events_and_Encounters.md#context-attack), [`bash`](./Events_and_Encounters.md#context-bash), [`bash_past_alt`](./Events_and_Encounters.md#context-bash_past_alt), [`bite`](./Events_and_Encounters.md#context-bite), [`bite_it_off`](./Events_and_Encounters.md#context-bite_it_off), [`blue_needle`](./Events_and_Encounters.md#context-blue_needle), [`body`](./Events_and_Encounters.md#context-body), [`break_ice`](./Events_and_Encounters.md#context-break_ice), [`break_lock`](./Events_and_Encounters.md#context-break_lock), [`bribe`](./Events_and_Encounters.md#context-bribe), [`catch`](./Events_and_Encounters.md#context-catch), [`challenge_to_game`](./Events_and_Encounters.md#context-challenge_to_game), [`charm`](./Events_and_Encounters.md#context-charm), [`charm_past_alt`](./Events_and_Encounters.md#context-charm_past_alt), [`climb`](./Events_and_Encounters.md#context-climb), [`comfort`](./Events_and_Encounters.md#context-comfort), [`communicate`](./Events_and_Encounters.md#context-communicate), [`concheck`](./Events_and_Encounters.md#context-concheck), and 106 more...

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 249 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | `String` |  | 0 |
| [`cha`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`common`](./Events_and_Encounters.md#object-common) | Object | Event Node: Story branch or dialog option representing the 'Common' action. | 0 |
| `con` | Number |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `dex` | Number |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`gain_coins`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`party_damage`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random` | Number |  | 0 |
| [`random_chance`](./Events_and_Encounters.md#object-random-chance) | Object | Event Logic: Executes the nested outcome based on a percentage roll. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | `Number` |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`set_subject`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`spawn_unit_next_fight`](./Events_and_Encounters.md#object-spawn-unit-next-fight) | Object | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. | 0 |
| `spd` | Number |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `weight` | Number | Probability weight for this outcome. | 0 |

</details>

---

### Object: `intro`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 214

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`cat_choice`](./Enums.md#enum-cat_choice) | Enum |  | 214 |
| [`event_clip`](./Enums.md#enum-event_clip) | Enum |  | 214 |
| [`subject_clip`](./Enums.md#enum-subject_clip) | Enum |  | 214 |
| [`subject_frame`](./Enums.md#enum-subject_frame) | Enum |  | 214 |
| [`title`](./Strings.md#string-title) | String |  | 214 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 214 |
| [`choose_cat_with_item`](./Enums.md#enum-choose_cat_with_item) | Enum |  | 17 |
| `different_from_last_x_cats` | Number |  | 3 |
| `subject_frame_inner` | Number |  | 3 |
| [`choose_cat_with_highest_stat`](./Math_Equations.md) | Equation |  | 1 |
| [`choose_cat_with_item_slot_equipped`](./Enums.md#enum-choose_cat_with_item_slot_equipped) | Enum |  | 1 |
| `choose_cat_with_min_health` | Number |  | 1 |
| `choose_cat_with_most_injuries` | Boolean |  | 1 |
| `choose_cat_with_parasite` | Boolean |  | 1 |
| `set_frame` | `Number` |  | 0 |

</details>

---

### Object: `main`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 214

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 220 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`ambush`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `ambush_next_basic_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `clear_result_animation` | Number |  | 0 |
| `con` | Number |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | Object | Event Node: Triggers a narrative cutscene. | 0 |
| `damage` | Number | Event Node: Story branch or dialog option representing the 'Damage' action. | 0 |
| [`decrement_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`future`](./Events_and_Encounters.md#object-future) | Object | Event Node: Story branch or dialog option representing the 'Future' action. | 0 |
| `gain_cat_familiar` | Number |  | 0 |
| [`gain_coins`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_familiar`](./Events_and_Encounters.md#object-gain-familiar) | Enum/String | Event Action: Adds a specific familiar to the party. | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_and_equip_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| [`good`](./Events_and_Encounters.md#object-good) | Object | Event Node: Story branch or dialog option representing the 'Good' action. | 0 |
| [`goto`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `hide_appearance_changes` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`leave`](./Events_and_Encounters.md#object-leave) | Object | Event Node: Story branch or dialog option representing the 'Leave' action. | 0 |
| [`leave_party_temporarily`](./Events_and_Encounters.md#object-leave-party-temporarily) | Object | Event Action: Removes a character from the active team until the next hub area. | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_all_equipped_items`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item_from_inventory`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`make_old`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `max_options` | `Number` |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Enum/String | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`options`](./Events_and_Encounters.md#object-options) | Object | Event Object: Lists the available clickable dialog choices for the current story node. | 0 |
| [`outcome`](./Events_and_Encounters.md#object-outcome) | Object | Event Object: Logic and text executed after selecting a specific dialog option. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `party_damage` | Number |  | 0 |
| `party_heal` | Number |  | 0 |
| `party_heal_disorder` | Number |  | 0 |
| `party_heal_injury` | Number |  | 0 |
| [`party_injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`party_permanent_stats`](./Events_and_Encounters.md#object-party-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of all party members. | 0 |
| [`party_permanent_stats_exclude_self`](./Events_and_Encounters.md#object-party-permanent-stats-exclude-self) | Object | Event Reward: Permanently modifies stats for all party members except the one who initiated the action. | 0 |
| `party_random_mutation` | Number |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`party_status_next_fight`](./Events_and_Encounters.md#object-party-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect to the entire party at the start of the next combat encounter. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`play_result_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_mutation_from_set`](./Events_and_Encounters.md#object-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to a character from a specific pool. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`requires_flag`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` | Prerequisite: Must meet this condition. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_basic_attack`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_damage`](./Engine_DamagingKeys.md#valid-property-keys) | `Array` | Recoil or self-inflicted damage/effects applied to the caster. | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_age` | Number |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`setup`](./Events_and_Encounters.md#object-setup) | Object | Event Object: Pre-initialization logic executed before the event UI is drawn. | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| `shuffle_options` | `Boolean` |  | 0 |
| `spawn_reflection_next_fight` | Number | Event Penalty: Spawns dark clones/reflections of the party in the next combat encounter. | 0 |
| [`spawn_unit_next_fight`](./Events_and_Encounters.md#object-spawn-unit-next-fight) | Object | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`weight`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` | Probability weight for this outcome. | 0 |

</details>

---

### Object: `options`



<details>
<summary><b>Expand</b></summary>

> **Total Count:** 210

> **Referenced by:** [`main`](./Events_and_Encounters.md#context-main)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`ignore`](./Events_and_Encounters.md#context-ignore) | Object | Event Node: Story branch or dialog option representing the \'Ignore\' action. | 55 |
| [`examine`](./Events_and_Encounters.md#context-examine) | Object | Event Node: Story branch or dialog option representing the \'Examine\' action. | 43 |
| [`loot`](./Events_and_Encounters.md#context-loot) | Object | Event Node: Story branch or dialog option representing the \'Loot\' action. | 25 |
| [`eat`](./Events_and_Encounters.md#context-eat) | Object | Event Node: Story branch or dialog option representing the \'Eat\' action. | 23 |
| [`smash`](./Events_and_Encounters.md#context-smash) | Object | Event Node: Story branch or dialog option representing the \'Smash\' action. | 15 |
| [`destroy`](./Events_and_Encounters.md#context-destroy) | Object | Event Node: Story branch or dialog option representing the \'Destroy\' action. | 13 |
| [`bash`](./Events_and_Encounters.md#context-bash) | Object | Event Node: Story branch or dialog option representing the \'Bash\' action. | 12 |
| [`sneak`](./Events_and_Encounters.md#context-sneak) | Object | Event Node: Story branch or dialog option representing the \'Sneak\' action. | 11 |
| [`open`](./Events_and_Encounters.md#context-open) | Object | Event Node: Story branch or dialog option representing the \'Open\' action. | 8 |
| [`take`](./Events_and_Encounters.md#context-take) | Object | Event Node: Story branch or dialog option representing the \'Take\' action. | 8 |
| [`a`](./Events_and_Encounters.md#context-a) | Object | Event Node: Story branch or dialog option representing the \'A\' action. | 7 |
| [`attack`](./Events_and_Encounters.md#context-attack) | Object | Event Node: Story branch or dialog option representing the \'Attack\' action. | 7 |
| [`b`](./Events_and_Encounters.md#context-b) | Object | Event Node: Story branch or dialog option representing the \'B\' action. | 7 |
| [`c`](./Events_and_Encounters.md#context-c) | Object | Event Node: Story branch or dialog option representing the \'C\' action. | 7 |
| [`charm`](./Events_and_Encounters.md#context-charm) | Object | Event Node: Story branch or dialog option representing the \'Charm\' action. | 7 |
| [`fight`](./Events_and_Encounters.md#context-fight) | Object | Event Node: Story branch or dialog option representing the \'Fight\' action. | 7 |
| [`touch`](./Events_and_Encounters.md#context-touch) | Object | Event Node: Story branch or dialog option representing the \'Touch\' action. | 7 |
| [`activate_p`](./Events_and_Encounters.md#context-activate_p) | Object | Event Node: Story branch or dialog option representing the 'Activate P' action. | 6 |
| [`activate_z`](./Events_and_Encounters.md#context-activate_z) | Object | Event Node: Story branch or dialog option representing the 'Activate Z' action. | 6 |
| [`d`](./Events_and_Encounters.md#context-d) | Object | Event Node: Story branch or dialog option representing the \'D\' action. | 6 |
| [`enter`](./Events_and_Encounters.md#context-enter) | Object | Event Node: Story branch or dialog option representing the \'Enter\' action. | 6 |
| [`inspect`](./Events_and_Encounters.md#context-inspect) | Object | Event Node: Story branch or dialog option representing the \'Inspect\' action. | 6 |
| [`lick`](./Events_and_Encounters.md#context-lick) | Object | Event Node: Story branch or dialog option representing the \'Lick\' action. | 6 |
| [`drink`](./Events_and_Encounters.md#context-drink) | Object | Event Node: Story branch or dialog option representing the \'Drink\' action. | 5 |
| [`kiss`](./Events_and_Encounters.md#context-kiss) | Object | Event Node: Story branch or dialog option representing the \'Kiss\' action. | 5 |
| [`run`](./Events_and_Encounters.md#context-run) | Object | Event Node: Story branch or dialog option representing the \'Run\' action. | 5 |
| [`bite`](./Events_and_Encounters.md#context-bite) | Object | Event Node: Story branch or dialog option representing the 'Bite' action. | 4 |
| [`damage`](./Events_and_Encounters.md#context-damage) | Object | Event Node: Story branch or dialog option representing the 'Damage' action. | 4 |
| [`go_around`](./Events_and_Encounters.md#context-go_around) | Object | Event Node: Story branch or dialog option representing the \'Go Around\' action. | 4 |
| [`home`](./Events_and_Encounters.md#context-home) | Object | Event Node: Story branch or dialog option representing the 'Home' action. | 4 |
| [`past`](./Events_and_Encounters.md#context-past) | Object | Event Node: Story branch or dialog option representing the 'Past' action. | 4 |
| [`skip`](./Events_and_Encounters.md#context-skip) | Object | Event Node: Story branch or dialog option representing the \'Skip\' action. | 4 |
| [`investigate`](./Events_and_Encounters.md#context-investigate) | Object | Event Node: Story branch or dialog option representing the \'Investigate\' action. | 3 |
| [`repell`](./Events_and_Encounters.md#context-repell) | Object | Event Node: Story branch or dialog option representing the \'Repell\' action. | 3 |
| [`attach_antenna`](./Events_and_Encounters.md#context-attach_antenna) | Object | Event Node: Story branch or dialog option representing the 'Attach Antenna' action. | 2 |
| [`boogers`](./Events_and_Encounters.md#context-boogers) | Object | Event Node: Story branch or dialog option representing the \'Boogers\' action. | 2 |
| [`copy`](./Events_and_Encounters.md#context-copy) | Object | Event Node: Story branch or dialog option representing the \'Copy\' action. | 2 |
| [`find_another_way`](./Events_and_Encounters.md#context-find_another_way) | Object | Event Node: Story branch or dialog option representing the \'Find Another Way\' action. | 2 |
| [`move_closer`](./Events_and_Encounters.md#context-move_closer) | Object | Event Node: Story branch or dialog option representing the \'Move Closer\' action. | 2 |
| [`play`](./Events_and_Encounters.md#context-play) | Object | Event Node: Story branch or dialog option representing the \'Play\' action. | 2 |
| [`poop`](./Events_and_Encounters.md#context-poop) | Object | Event Node: Story branch or dialog option representing the \'Poop\' action. | 2 |
| [`print`](./Events_and_Encounters.md#context-print) | Object | Event Node: Story branch or dialog option representing the \'Print\' action. | 2 |
| [`protection`](./Events_and_Encounters.md#context-protection) | Object | Event Node: Story branch or dialog option representing the \'Protection\' action. | 2 |
| [`repair`](./Events_and_Encounters.md#context-repair) | Object | Event Node: Story branch or dialog option representing the \'Repair\' action. | 2 |
| [`sacrifice`](./Events_and_Encounters.md#context-sacrifice) | Object | Event Node: Story branch or dialog option representing the \'Sacrifice\' action. | 2 |
| [`scale`](./Events_and_Encounters.md#context-scale) | Object | Event Node: Story branch or dialog option representing the \'Scale\' action. | 2 |
| [`turnon`](./Events_and_Encounters.md#context-turnon) | Object | Event Node: Story branch or dialog option representing the \'Turnon\' action. | 2 |
| [`altar_sacrifice`](./Events_and_Encounters.md#context-altar_sacrifice) | Object | Event Action: Triggers the altar sacrifice progression logic. | 1 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum |  | 1 |
| [`arm`](./Events_and_Encounters.md#context-arm) | Object | Event Node: Story branch or dialog option representing the \'Arm\' action. | 1 |
| [`attach_amplifier`](./Events_and_Encounters.md#context-attach_amplifier) | Object | Event Node: Story branch or dialog option representing the 'Attach Amplifier' action. | 1 |
| [`attach_leech`](./Events_and_Encounters.md#context-attach_leech) | Object | Event Node: Story branch or dialog option representing the 'Attach Leech' action. | 1 |
| [`bash_past_alt`](./Events_and_Encounters.md#context-bash_past_alt) | Object | Event Node: Story branch or dialog option representing the \'Bash Past Alt\' action. | 1 |
| [`bite_it_off`](./Events_and_Encounters.md#context-bite_it_off) | Object | Event Node: Story branch or dialog option representing the \'Bite It Off\' action. | 1 |
| [`blue`](./Events_and_Encounters.md#context-blue) | Object | Event Node: Story branch or dialog option representing the \'Blue\' action. | 1 |
| [`blue_needle`](./Events_and_Encounters.md#context-blue_needle) | Object | Event Node: Story branch or dialog option representing the \'Blue Needle\' action. | 1 |
| [`body`](./Events_and_Encounters.md#context-body) | Object | Event Node: Story branch or dialog option representing the 'Body' action. | 1 |
| [`book`](./Events_and_Encounters.md#context-book) | Object | Event Node: Story branch or dialog option representing the \'Book\' action. | 1 |
| [`brace`](./Events_and_Encounters.md#context-brace) | Object | Event Node: Story branch or dialog option representing the \'Brace\' action. | 1 |
| [`break_ice`](./Events_and_Encounters.md#context-break_ice) | Object | Event Node: Story branch or dialog option representing the \'Break Ice\' action. | 1 |
| [`break_lock`](./Events_and_Encounters.md#context-break_lock) | Object | Event Node: Story branch or dialog option representing the \'Break Lock\' action. | 1 |
| [`bribe`](./Events_and_Encounters.md#context-bribe) | Object | Event Node: Story branch or dialog option representing the 'Bribe' action. | 1 |
| [`button`](./Events_and_Encounters.md#context-button) | Object | Event Node: Story branch or dialog option representing the \'Button\' action. | 1 |
| [`buy1`](./Events_and_Encounters.md#context-buy1) | Object | Event Node: Story branch or dialog option representing the \'Buy1\' action. | 1 |
| [`catch`](./Events_and_Encounters.md#context-catch) | Object | Event Node: Story branch or dialog option representing the \'Catch\' action. | 1 |
| [`challenge_to_game`](./Events_and_Encounters.md#context-challenge_to_game) | Object | Event Node: Story branch or dialog option representing the \'Challenge To Game\' action. | 1 |
| [`chaos_ending`](./Events_and_Encounters.md#context-chaos_ending) | Object | Event Node: Triggers the Chaos Boss victory sequence. | 1 |
| [`chapter_cutscene`](./Events_and_Encounters.md#context-chapter_cutscene) | Object | Event Node: Triggers an intermission cutscene. | 1 |
| [`charm_past_alt`](./Events_and_Encounters.md#context-charm_past_alt) | Object | Event Node: Story branch or dialog option representing the \'Charm Past Alt\' action. | 1 |
| [`climb`](./Events_and_Encounters.md#context-climb) | Object | Event Node: Story branch or dialog option representing the \'Climb\' action. | 1 |
| [`comfort`](./Events_and_Encounters.md#context-comfort) | Object | Event Node: Story branch or dialog option representing the \'Comfort\' action. | 1 |
| [`communicate`](./Events_and_Encounters.md#context-communicate) | Object | Event Node: Story branch or dialog option representing the \'Communicate\' action. | 1 |
| [`concheck`](./Events_and_Encounters.md#context-concheck) | Object | Event Node: Stat check branch evaluating the \'con\' attribute. | 1 |
| [`counter`](./Events_and_Encounters.md#context-counter) | Object | Event Node: Story branch or dialog option representing the \'Counter\' action. | 1 |
| [`crack_open`](./Events_and_Encounters.md#context-crack_open) | Object | Event Node: Story branch or dialog option representing the \'Crack Open\' action. | 1 |
| [`cross`](./Events_and_Encounters.md#context-cross) | Object | Event Node: Story branch or dialog option representing the \'Cross\' action. | 1 |
| [`cut_wires`](./Events_and_Encounters.md#context-cut_wires) | Object | Event Node: Story branch or dialog option representing the \'Cut Wires\' action. | 1 |
| [`damage_1`](./Events_and_Encounters.md#context-damage_1) | Object | Event Node: Story branch or dialog option representing the \'Damage 1\' action. | 1 |
| [`damage_full`](./Events_and_Encounters.md#context-damage_full) | Object | Event Node: Story branch or dialog option representing the \'Damage Full\' action. | 1 |
| [`damage_half`](./Events_and_Encounters.md#context-damage_half) | Object | Event Node: Story branch or dialog option representing the \'Damage Half\' action. | 1 |
| [`desert_cutscene`](./Events_and_Encounters.md#context-desert_cutscene) | Object | Event Node: Triggers the desert transition cutscene. | 1 |
| [`dexcheck`](./Events_and_Encounters.md#context-dexcheck) | Object | Event Node: Stat check branch evaluating the \'dex\' attribute. | 1 |
| [`dig`](./Events_and_Encounters.md#context-dig) | Object | Event Node: Story branch or dialog option representing the \'Dig\' action. | 1 |
| [`disarm`](./Events_and_Encounters.md#context-disarm) | Object | Event Node: Story branch or dialog option representing the \'Disarm\' action. | 1 |
| [`dive`](./Events_and_Encounters.md#context-dive) | Object | Event Node: Story branch or dialog option representing the \'Dive\' action. | 1 |
| [`donate`](./Events_and_Encounters.md#context-donate) | Object | Event Node: Story branch or dialog option representing the \'Donate\' action. | 1 |
| [`donate_10`](./Events_and_Encounters.md#context-donate_10) | Object | Event Node: Story branch or dialog option representing the \'Donate 10\' action. | 1 |
| [`donate_15`](./Events_and_Encounters.md#context-donate_15) | Object | Event Node: Story branch or dialog option representing the \'Donate 15\' action. | 1 |
| [`donate_20`](./Events_and_Encounters.md#context-donate_20) | Object | Event Node: Story branch or dialog option representing the \'Donate 20\' action. | 1 |
| [`donate_5`](./Events_and_Encounters.md#context-donate_5) | Object | Event Node: Story branch or dialog option representing the \'Donate 5\' action. | 1 |
| [`double`](./Events_and_Encounters.md#context-double) | Object | Event Node: Story branch or dialog option representing the \'Double\' action. | 1 |
| [`eat_meat`](./Events_and_Encounters.md#context-eat_meat) | Object | Event Node: Story branch or dialog option representing the \'Eat Meat\' action. | 1 |
| [`enter_crater`](./Events_and_Encounters.md#context-enter_crater) | Object | Event Node: Story branch or dialog option representing the \'Enter Crater\' action. | 1 |
| [`face`](./Events_and_Encounters.md#context-face) | Object | Event Node: Story branch or dialog option representing the \'Face\' action. | 1 |
| [`fiddle`](./Events_and_Encounters.md#context-fiddle) | Object | Event Node: Story branch or dialog option representing the 'Fiddle' action. | 1 |
| [`fill_jar`](./Events_and_Encounters.md#context-fill_jar) | Object | Event Node: Story branch or dialog option representing the 'Fill Jar' action. | 1 |
| [`find`](./Events_and_Encounters.md#context-find) | Object | Event Node: Story branch or dialog option representing the \'Find\' action. | 1 |
| [`fire`](./Events_and_Encounters.md#context-fire) | Object | Event Node: Story branch or dialog option representing the \'Fire\' action. | 1 |
| [`flush_yourself`](./Events_and_Encounters.md#context-flush_yourself) | Object | Event Node: Story branch or dialog option representing the \'Flush Yourself\' action. | 1 |
| [`follow`](./Events_and_Encounters.md#context-follow) | Object | Event Node: Story branch or dialog option representing the \'Follow\' action. | 1 |
| [`free`](./Events_and_Encounters.md#context-free) | Object | Event Node: Story branch or dialog option representing the \'Free\' action. | 1 |
| [`future`](./Events_and_Encounters.md#context-future) | Object | Event Node: Story branch or dialog option representing the 'Future' action. | 1 |
| [`give_parasite`](./Events_and_Encounters.md#context-give_parasite) | Object | Event Action: Equips a parasite item to a character. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`hack`](./Events_and_Encounters.md#context-hack) | Object | Event Node: Story branch or dialog option representing the \'Hack\' action. | 1 |
| [`head`](./Events_and_Encounters.md#context-head) | Object | Event Node: Story branch or dialog option representing the \'Head\' action. | 1 |
| [`holy`](./Events_and_Encounters.md#context-holy) | Object | Event Node: Story branch or dialog option representing the \'Holy\' action. | 1 |
| [`hp`](./Events_and_Encounters.md#context-hp) | Object | Event Node: Story branch or dialog option representing the \'Hp\' action. | 1 |
| [`ice`](./Events_and_Encounters.md#context-ice) | Object | Event Node: Story branch or dialog option representing the \'Ice\' action. | 1 |
| [`infinite`](./Events_and_Encounters.md#context-infinite) | Object | Event Node: A looping or endlessly repeating story branch. | 1 |
| [`intcheck`](./Events_and_Encounters.md#context-intcheck) | Object | Event Node: Stat check branch evaluating the \'int\' attribute. | 1 |
| [`intimidation`](./Events_and_Encounters.md#context-intimidation) | Object | Event Node: Story branch or dialog option representing the \'Intimidation\' action. | 1 |
| [`itchies`](./Events_and_Encounters.md#context-itchies) | Object | Event Node: Story branch or dialog option representing the \'Itchies\' action. | 1 |
| [`join`](./Events_and_Encounters.md#context-join) | Object | Event Node: Story branch or dialog option representing the \'Join\' action. | 1 |
| [`jump`](./Events_and_Encounters.md#context-jump) | Object | Event Node: Story branch or dialog option representing the \'Jump\' action. | 1 |
| [`jump_over`](./Events_and_Encounters.md#context-jump_over) | Object | Event Node: Story branch or dialog option representing the \'Jump Over\' action. | 1 |
| [`keep_going`](./Events_and_Encounters.md#context-keep_going) | Object | Event Node: Story branch or dialog option representing the \'Keep Going\' action. | 1 |
| [`kiss_meat`](./Events_and_Encounters.md#context-kiss_meat) | Object | Event Node: Story branch or dialog option representing the \'Kiss Meat\' action. | 1 |
| [`knife`](./Events_and_Encounters.md#context-knife) | Object | Event Node: Story branch or dialog option representing the \'Knife\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`leave_it_in`](./Events_and_Encounters.md#context-leave_it_in) | Object | Event Node: Story branch or dialog option representing the \'Leave It In\' action. | 1 |
| [`leg`](./Events_and_Encounters.md#context-leg) | Object | Event Node: Story branch or dialog option representing the \'Leg\' action. | 1 |
| [`lever`](./Events_and_Encounters.md#context-lever) | Object | Event Node: Story branch or dialog option representing the \'Lever\' action. | 1 |
| [`lick_alt`](./Events_and_Encounters.md#context-lick_alt) | Object | Event Node: Story branch or dialog option representing the \'Lick Alt\' action. | 1 |
| [`lightning`](./Events_and_Encounters.md#context-lightning) | Object | Event Node: Story branch or dialog option representing the \'Lightning\' action. | 1 |
| [`listen`](./Events_and_Encounters.md#context-listen) | Object | Event Node: Story branch or dialog option representing the \'Listen\' action. | 1 |
| [`looks`](./Events_and_Encounters.md#context-looks) | Object | Event Node: Story branch or dialog option representing the 'Looks' action. | 1 |
| [`loot_heart`](./Events_and_Encounters.md#context-loot_heart) | Object | Event Node: Story branch or dialog option representing the 'Loot Heart' action. | 1 |
| [`makeup`](./Events_and_Encounters.md#context-makeup) | Object | Event Node: Story branch or dialog option representing the \'Makeup\' action. | 1 |
| [`mind`](./Events_and_Encounters.md#context-mind) | Object | Event Node: Story branch or dialog option representing the 'Mind' action. | 1 |
| [`neck`](./Events_and_Encounters.md#context-neck) | Object | Event Node: Story branch or dialog option representing the \'Neck\' action. | 1 |
| [`nothanks`](./Events_and_Encounters.md#context-nothanks) | Object | Event Node: Story branch or dialog option representing the \'Nothanks\' action. | 1 |
| [`outsmart`](./Events_and_Encounters.md#context-outsmart) | Object | Event Node: Story branch or dialog option representing the \'Outsmart\' action. | 1 |
| [`patch_up`](./Events_and_Encounters.md#context-patch_up) | Object | Event Node: Story branch or dialog option representing the \'Patch Up\' action. | 1 |
| [`pick_lock`](./Events_and_Encounters.md#context-pick_lock) | Object | Event Node: Story branch or dialog option representing the \'Pick Lock\' action. | 1 |
| [`pilfer`](./Events_and_Encounters.md#context-pilfer) | Object | Event Node: Story branch or dialog option representing the \'Pilfer\' action. | 1 |
| [`pirouette`](./Events_and_Encounters.md#context-pirouette) | Object | Event Node: Story branch or dialog option representing the \'Pirouette\' action. | 1 |
| [`place_gristle`](./Events_and_Encounters.md#context-place_gristle) | Object | Event Node: Story branch or dialog option representing the 'Place Gristle' action. | 1 |
| [`power`](./Events_and_Encounters.md#context-power) | Object | Event Node: Story branch or dialog option representing the 'Power' action. | 1 |
| [`pull`](./Events_and_Encounters.md#context-pull) | Object | Event Node: Story branch or dialog option representing the \'Pull\' action. | 1 |
| [`pull_it_out`](./Events_and_Encounters.md#context-pull_it_out) | Object | Event Node: Story branch or dialog option representing the \'Pull It Out\' action. | 1 |
| [`pull_lever`](./Events_and_Encounters.md#context-pull_lever) | Object | Event Node: Story branch or dialog option representing the \'Pull Lever\' action. | 1 |
| [`purify`](./Events_and_Encounters.md#context-purify) | Object | Event Node: Story branch or dialog option representing the \'Purify\' action. | 1 |
| [`push_buttons`](./Events_and_Encounters.md#context-push_buttons) | Object | Event Node: Story branch or dialog option representing the \'Push Buttons\' action. | 1 |
| [`push_through`](./Events_and_Encounters.md#context-push_through) | Object | Event Node: Story branch or dialog option representing the \'Push Through\' action. | 1 |
| [`put_in_coins`](./Events_and_Encounters.md#context-put_in_coins) | Object | Event Node: Story branch or dialog option representing the \'Put In Coins\' action. | 1 |
| [`put_out_of_misery`](./Events_and_Encounters.md#context-put_out_of_misery) | Object | Event Node: Story branch or dialog option representing the \'Put Out Of Misery\' action. | 1 |
| [`reach_inside`](./Events_and_Encounters.md#context-reach_inside) | Object | Event Node: Story branch or dialog option representing the \'Reach Inside\' action. | 1 |
| [`read`](./Events_and_Encounters.md#context-read) | Object | Event Node: Story branch or dialog option representing the \'Read\' action. | 1 |
| [`receive`](./Events_and_Encounters.md#context-receive) | Object | Event Node: Story branch or dialog option representing the \'Receive\' action. | 1 |
| [`red`](./Events_and_Encounters.md#context-red) | Object | Event Node: Story branch or dialog option representing the \'Red\' action. | 1 |
| [`red_needle`](./Events_and_Encounters.md#context-red_needle) | Object | Event Node: Story branch or dialog option representing the \'Red Needle\' action. | 1 |
| [`reflect`](./Events_and_Encounters.md#context-reflect) | Object | Event Node: Story branch or dialog option representing the \'Reflect\' action. | 1 |
| [`remove`](./Events_and_Encounters.md#context-remove) | Object | Event Node: Story branch or dialog option representing the \'Remove\' action. | 1 |
| [`remove_the_nail`](./Events_and_Encounters.md#context-remove_the_nail) | Object | Event Node: Story branch or dialog option representing the \'Remove The Nail\' action. | 1 |
| [`repair_quest`](./Events_and_Encounters.md#context-repair_quest) | Object | Event Node: Story branch or dialog option representing the 'Repair Quest' action. | 1 |
| [`rest`](./Events_and_Encounters.md#context-rest) | Object | Event Node: Story branch or dialog option representing the \'Rest\' action. | 1 |
| [`revive`](./Events_and_Encounters.md#context-revive) | Object | Event Node: Story branch or dialog option representing the \'Revive\' action. | 1 |
| [`rub`](./Events_and_Encounters.md#context-rub) | Object | Event Node: Story branch or dialog option representing the \'Rub\' action. | 1 |
| [`run_again`](./Events_and_Encounters.md#context-run_again) | Object | Event Node: Story branch or dialog option representing the \'Run Again\' action. | 1 |
| [`run_away`](./Events_and_Encounters.md#context-run_away) | Object | Event Node: Story branch or dialog option representing the \'Run Away\' action. | 1 |
| [`sacrifice_full_favor`](./Events_and_Encounters.md#context-sacrifice_full_favor) | Object | Event Node: Story branch or dialog option representing the \'Sacrifice Full Favor\' action. | 1 |
| [`sacrifice_normal`](./Events_and_Encounters.md#context-sacrifice_normal) | Object | Event Node: Story branch or dialog option representing the 'Sacrifice Normal' action. | 1 |
| [`sacrifice_partial_favor`](./Events_and_Encounters.md#context-sacrifice_partial_favor) | Object | Event Node: Story branch or dialog option representing the \'Sacrifice Partial Favor\' action. | 1 |
| [`sacrifice_quest`](./Events_and_Encounters.md#context-sacrifice_quest) | Object | Event Node: Story branch or dialog option representing the 'Sacrifice Quest' action. | 1 |
| [`scream`](./Events_and_Encounters.md#context-scream) | Object | Event Node: Story branch or dialog option representing the \'Scream\' action. | 1 |
| [`shake`](./Events_and_Encounters.md#context-shake) | Object | Event Node: Story branch or dialog option representing the \'Shake\' action. | 1 |
| [`slip_through`](./Events_and_Encounters.md#context-slip_through) | Object | Event Node: Story branch or dialog option representing the \'Slip Through\' action. | 1 |
| [`sneak_by`](./Events_and_Encounters.md#context-sneak_by) | Object | Event Node: Story branch or dialog option representing the \'Sneak By\' action. | 1 |
| [`sneak_past_alt`](./Events_and_Encounters.md#context-sneak_past_alt) | Object | Event Node: Story branch or dialog option representing the \'Sneak Past Alt\' action. | 1 |
| [`soul`](./Events_and_Encounters.md#context-soul) | Object | Event Node: Story branch or dialog option representing the 'Soul' action. | 1 |
| [`speed`](./Events_and_Encounters.md#context-speed) | Object | Event Node: Story branch or dialog option representing the \'Speed\' action. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| `stat_max` | Number |  | 1 |
| `stat_min` | Number |  | 1 |
| [`surprise`](./Events_and_Encounters.md#context-surprise) | Object | Event Node: Story branch or dialog option representing the \'Surprise\' action. | 1 |
| [`sweet_talk`](./Events_and_Encounters.md#context-sweet_talk) | Object | Event Node: Story branch or dialog option representing the \'Sweet Talk\' action. | 1 |
| [`swim`](./Events_and_Encounters.md#context-swim) | Object | Event Node: Story branch or dialog option representing the \'Swim\' action. | 1 |
| [`tail`](./Events_and_Encounters.md#context-tail) | Object | Event Node: Story branch or dialog option representing the \'Tail\' action. | 1 |
| [`take_blood`](./Events_and_Encounters.md#context-take_blood) | Object | Event Node: Story branch or dialog option representing the 'Take Blood' action. | 1 |
| [`talk`](./Events_and_Encounters.md#context-talk) | Object | Event Node: Story branch or dialog option representing the 'Talk' action. | 1 |
| [`talk_to`](./Events_and_Encounters.md#context-talk_to) | Object | Event Node: Story branch or dialog option representing the \'Talk To\' action. | 1 |
| [`tappytoes`](./Events_and_Encounters.md#context-tappytoes) | Object | Event Node: Story branch or dialog option representing the \'Tappytoes\' action. | 1 |
| [`teleport`](./Events_and_Encounters.md#context-teleport) | Object | Event Node: Story branch or dialog option representing the \'Teleport\' action. | 1 |
| [`thorns`](./Events_and_Encounters.md#context-thorns) | Object | Event Node: Story branch or dialog option representing the \'Thorns\' action. | 1 |
| [`throw`](./Events_and_Encounters.md#context-throw) | Object | Event Node: Story branch or dialog option representing the \'Throw\' action. | 1 |
| [`timemachine`](./Events_and_Encounters.md#context-timemachine) | Object | Event Node: Story branch or dialog option representing the \'Timemachine\' action. | 1 |
| [`traverse`](./Events_and_Encounters.md#context-traverse) | Object | Event Node: Story branch or dialog option representing the \'Traverse\' action. | 1 |
| [`upgrade_yourself`](./Events_and_Encounters.md#context-upgrade_yourself) | Object | Event Reward: Upgrades an existing ability or item. | 1 |
| [`use_item`](./Events_and_Encounters.md#context-use_item) | Object | Event Requirement: Requires the player to consume a specific item to proceed. | 1 |
| [`use_toilet_con`](./Events_and_Encounters.md#context-use_toilet_con) | Object | Event Node: Story branch or dialog option representing the \'Use Toilet Con\' action. | 1 |
| [`use_toilet_str`](./Events_and_Encounters.md#context-use_toilet_str) | Object | Event Node: Story branch or dialog option representing the \'Use Toilet Str\' action. | 1 |
| [`use_weapon`](./Events_and_Encounters.md#context-use_weapon) | Object | Event Requirement: Uses the properties of the equipped weapon to resolve an outcome. | 1 |
| [`w1`](./Events_and_Encounters.md#context-w1) | Object | Event Node: Story branch or dialog option representing the \'W1\' action. | 1 |
| [`w2`](./Events_and_Encounters.md#context-w2) | Object | Event Node: Story branch or dialog option representing the \'W2\' action. | 1 |
| [`w3`](./Events_and_Encounters.md#context-w3) | Object | Event Node: Story branch or dialog option representing the \'W3\' action. | 1 |
| [`w4`](./Events_and_Encounters.md#context-w4) | Object | Event Node: Story branch or dialog option representing the \'W4\' action. | 1 |
| [`w5`](./Events_and_Encounters.md#context-w5) | Object | Event Node: Story branch or dialog option representing the \'W5\' action. | 1 |
| [`w6`](./Events_and_Encounters.md#context-w6) | Object | Event Node: Story branch or dialog option representing the \'W6\' action. | 1 |
| [`wealth`](./Events_and_Encounters.md#context-wealth) | Object | Event Node: Story branch or dialog option representing the 'Wealth' action. | 1 |
| [`wheezies`](./Events_and_Encounters.md#context-wheezies) | Object | Event Node: Story branch or dialog option representing the \'Wheezies\' action. | 1 |
| [`wish_genes`](./Events_and_Encounters.md#context-wish_genes) | Object | Event Node: Story branch or dialog option representing the \'Wish Genes\' action. | 1 |
| [`wish_items`](./Events_and_Encounters.md#context-wish_items) | Object | Event Node: Story branch or dialog option representing the \'Wish Items\' action. | 1 |
| [`wish_levelups`](./Events_and_Encounters.md#context-wish_levelups) | Object | Event Node: Story branch or dialog option representing the \'Wish Levelups\' action. | 1 |
| [`wish_strength`](./Events_and_Encounters.md#context-wish_strength) | Object | Event Node: Story branch or dialog option representing the \'Wish Strength\' action. | 1 |
| [`withstand`](./Events_and_Encounters.md#context-withstand) | Object | Event Node: Story branch or dialog option representing the \'Withstand\' action. | 1 |
| [`yank_it_out`](./Events_and_Encounters.md#context-yank_it_out) | Object | Event Node: Story branch or dialog option representing the \'Yank It Out\' action. | 1 |
| [`yellow_needle`](./Events_and_Encounters.md#context-yellow_needle) | Object | Event Node: Story branch or dialog option representing the \'Yellow Needle\' action. | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`ambush`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `ambush_next_basic_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `clear_result_animation` | Number |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | Object | Event Node: Triggers a narrative cutscene. | 0 |
| [`decrement_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| `gain_cat_familiar` | Number |  | 0 |
| [`gain_coins`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_familiar`](./Events_and_Encounters.md#object-gain-familiar) | Enum/String | Event Action: Adds a specific familiar to the party. | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_and_equip_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal_disorder` | Number |  | 0 |
| `hide_appearance_changes` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`leave`](./Events_and_Encounters.md#object-leave) | Object | Event Node: Story branch or dialog option representing the 'Leave' action. | 0 |
| [`leave_party_temporarily`](./Events_and_Encounters.md#object-leave-party-temporarily) | Object | Event Action: Removes a character from the active team until the next hub area. | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_all_equipped_items`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item_from_inventory`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`make_old`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Enum/String | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `party_damage` | Number |  | 0 |
| `party_heal` | Number |  | 0 |
| `party_heal_disorder` | Number |  | 0 |
| `party_heal_injury` | Number |  | 0 |
| [`party_injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`party_permanent_stats`](./Events_and_Encounters.md#object-party-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of all party members. | 0 |
| [`party_permanent_stats_exclude_self`](./Events_and_Encounters.md#object-party-permanent-stats-exclude-self) | Object | Event Reward: Permanently modifies stats for all party members except the one who initiated the action. | 0 |
| `party_random_mutation` | Number |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`party_status_next_fight`](./Events_and_Encounters.md#object-party-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect to the entire party at the start of the next combat encounter. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`play_result_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_mutation_from_set`](./Events_and_Encounters.md#object-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to a character from a specific pool. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_basic_attack`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `self_damage` | Number | Recoil or self-inflicted damage/effects applied to the caster. | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_age` | Number |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `spawn_reflection_next_fight` | Number | Event Penalty: Spawns dark clones/reflections of the party in the next combat encounter. | 0 |
| [`spawn_unit_next_fight`](./Events_and_Encounters.md#object-spawn-unit-next-fight) | Object | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`weight`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` | Probability weight for this outcome. | 0 |

</details>

---

### Object: `get_item_from_pool`


**Definition:** Event Action: Rewards the player with an item drawn from a specific loot pool.  
**Total Count:** 40

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 209

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`rare`](./Events_and_Encounters.md#context-rare), [`reward`](./Events_and_Encounters.md#context-reward)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Enum |  | 40 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 32 |
| [`restrict`](./Arrays.md#array-restrict) | Array |  | 30 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | `String` |  | 0 |

</details>

---

### Object: `requirements`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 203

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`activate_p`](./Events_and_Encounters.md#context-activate_p), [`activate_z`](./Events_and_Encounters.md#context-activate_z), [`attach_amplifier`](./Events_and_Encounters.md#context-attach_amplifier), [`attach_antenna`](./Events_and_Encounters.md#context-attach_antenna), [`attach_leech`](./Events_and_Encounters.md#context-attach_leech), [`bash`](./Events_and_Encounters.md#context-bash), [`bash_past_alt`](./Events_and_Encounters.md#context-bash_past_alt), [`blue_needle`](./Events_and_Encounters.md#context-blue_needle), [`charm`](./Events_and_Encounters.md#context-charm), [`charm_past_alt`](./Events_and_Encounters.md#context-charm_past_alt), [`conditional_reward`](./Events_and_Encounters.md#context-conditional_reward), [`dig`](./Events_and_Encounters.md#context-dig), [`donate_10`](./Events_and_Encounters.md#context-donate_10), [`donate_15`](./Events_and_Encounters.md#context-donate_15), [`donate_20`](./Events_and_Encounters.md#context-donate_20), [`donate_5`](./Events_and_Encounters.md#context-donate_5), [`fiddle`](./Events_and_Encounters.md#context-fiddle), [`fight`](./Events_and_Encounters.md#context-fight), [`fill_jar`](./Events_and_Encounters.md#context-fill_jar), and 31 more...

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`has_token`](./Enums.md#enum-has_token) | Enum |  | 80 |
| [`counter_range`](./Arrays.md#array-counter_range) | Array |  | 37 |
| [`not_has_token`](./Enums.md#enum-not_has_token) | Enum |  | 30 |
| [`counter_minimum`](./Arrays.md#array-counter_minimum) | Array |  | 25 |
| [`cat_has_item_equipped`](./Enums.md#enum-cat_has_item_equipped) | Enum |  | 22 |
| [`counter_maximum`](./Arrays.md#array-counter_maximum) | Array |  | 18 |
| [`is_not_chapter`](./Arrays.md#array-is_not_chapter) | Array |  | 16 |
| [`is_chapter`](./Arrays.md#array-is_chapter) | Array |  | 8 |
| [`not_cat_has_item_equipped`](./Enums.md#enum-not_cat_has_item_equipped) | Enum |  | 2 |
| `minimum_party_size` | Number |  | 2 |
| `not_on_quest` | Number |  | 2 |
| [`cat_has_item_slot_equipped`](./Enums.md#enum-cat_has_item_slot_equipped) | Enum |  | 1 |
| `cat_has_injury_count_min` | Number |  | 1 |
| `cat_has_parasite` | Boolean |  | 1 |

</details>

---

### Object: `self_status_next_fight`


**Definition:** Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter.  
**Total Count:** 143

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 141

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`bad`](./Events_and_Encounters.md#context-bad), [`buy1`](./Events_and_Encounters.md#context-buy1), [`common`](./Events_and_Encounters.md#context-common), [`else`](./Events_and_Encounters.md#context-else), [`main`](./Events_and_Encounters.md#context-main), [`rare`](./Events_and_Encounters.md#context-rare)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 103 |

</details>

---

### Object: `permanent_stats`


**Definition:** Event Reward: Permanently increases (or decreases) the core stats of a single character.  
**Total Count:** 134

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 133

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`bad`](./Events_and_Encounters.md#context-bad), [`common`](./Events_and_Encounters.md#context-common), [`rare`](./Events_and_Encounters.md#context-rare)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 35 |
| `random` | Number |  | 25 |
| `int` | Number |  | 21 |
| `lck` | Number |  | 18 |
| `spd` | Number |  | 18 |
| `str` | Number |  | 16 |
| [`cha`](./Engine_EventKeys.md#valid-property-keys) | Mixed |  | 14 |
| `dex` | Number |  | 9 |

</details>

---

### Object: `conditional_reward`


**Definition:** Event Action: Provides a reward only if a specific condition is met.  
**Total Count:** 126

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 124

> **Referenced by:** [`bad`](./Events_and_Encounters.md#context-bad), [`common`](./Events_and_Encounters.md#context-common), [`else`](./Events_and_Encounters.md#context-else), [`good`](./Events_and_Encounters.md#context-good), [`rare`](./Events_and_Encounters.md#context-rare), [`setup`](./Events_and_Encounters.md#context-setup)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 175 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 124 |
| [`else`](./Events_and_Encounters.md#context-else) | Object | Event Node: Story branch or dialog option representing the \'Else\' action. | 37 |
| [`clear_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `damage` | Number | Event Node: Story branch or dialog option representing the 'Damage' action. | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_coins`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`party_damage`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`random_chance`](./Events_and_Encounters.md#object-random-chance) | Object | Event Logic: Executes the nested outcome based on a percentage roll. | 0 |
| [`random_mutation`](./Events_and_Encounters.md#object-random-mutation) | Object | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`set_subject`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`spawn_unit_next_fight`](./Events_and_Encounters.md#object-spawn-unit-next-fight) | Object | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `weight` | Number | Probability weight for this outcome. | 0 |

</details>

---

### Object: `random_mutation`


**Definition:** Event Reward: Applies a completely random mutation to a character.  
**Total Count:** 19

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 66

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`else`](./Events_and_Encounters.md#context-else), [`rare`](./Events_and_Encounters.md#context-rare)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `count` | Number | Quantity. | 15 |
| [`tag`](./Enums.md#enum-tag) | Enum | Specific entity tag required. | 12 |
| `asymmetric` | Boolean |  | 8 |

</details>

---

### Object: `ignore`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 57

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 57 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 57 |
| [`label`](./Strings.md#string-label) | Mixed |  | 57 |
| [`stat`](./Enums.md#enum-stat) | Mixed |  | 56 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 55 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 3 |
| [`hint_chapter_exit`](./Enums.md#enum-hint_chapter_exit) | Enum |  | 2 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `examine`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 44

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 41 |
| [`label`](./Strings.md#string-label) | Mixed |  | 43 |
| [`stat`](./Math_Equations.md) | Equation |  | 43 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 41 |
| [`copy_results`](./Enums.md#enum-copy_results) | Enum |  | 2 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_coins`](./Engine_EventKeys.md#valid-property-keys) | `Array` |  | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `spawn_unit_next_fight`


**Definition:** Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter.  
**Total Count:** 41

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 40

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`rare`](./Events_and_Encounters.md#context-rare), [`reward`](./Events_and_Encounters.md#context-reward)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array |  | 40 |
| [`count`](./Arrays.md#array-count) | Array | Quantity. | 34 |
| [`spawn_side`](./Enums.md#enum-spawn_side) | Enum |  | 31 |
| [`side`](./Enums.md#enum-side) | Enum |  | 3 |

</details>

---

### Object: `else`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 37

> **Referenced by:** [`conditional_reward`](./Events_and_Encounters.md#context-conditional_reward)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 32 |
| `damage` | Number | Event Node: Story branch or dialog option representing the 'Damage' action. | 1 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | `Array` | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| `next_event_bonus` | `Number` |  | 0 |
| `party_damage` | `Number` |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | `String` |  | 0 |
| [`random_mutation`](./Events_and_Encounters.md#object-random-mutation) | Object | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | `Array` |  | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| `set_frame` | `Number` |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |

</details>

---

### Object: `leave`



<details>
<summary><b>Expand</b></summary>

> **Total Count:** 32

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`main`](./Events_and_Encounters.md#context-main), [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 30 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 30 |
| [`label`](./Strings.md#string-label) | String |  | 30 |
| [`stat`](./Enums.md#enum-stat) | Mixed |  | 30 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 28 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `loot`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 25

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 25 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 25 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 25 |
| [`label`](./Strings.md#string-label) | Mixed |  | 25 |
| [`stat`](./Math_Equations.md) | Equation |  | 25 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 2 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`ambush`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `ambush_next_basic_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clear_result_animation` | Number |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `damage` | Number | Event Node: Story branch or dialog option representing the 'Damage' action. | 0 |
| [`decrement_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| `gain_cat_familiar` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_coins`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_familiar`](./Events_and_Encounters.md#object-gain-familiar) | Enum/String | Event Action: Adds a specific familiar to the party. | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_and_equip_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| `hide_appearance_changes` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`leave_party_temporarily`](./Events_and_Encounters.md#object-leave-party-temporarily) | Object | Event Action: Removes a character from the active team until the next hub area. | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_all_equipped_items`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item_from_inventory`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`make_old`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Enum/String | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `party_damage` | Number |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| `party_heal` | Number |  | 0 |
| `party_heal_disorder` | Number |  | 0 |
| `party_heal_injury` | Number |  | 0 |
| [`party_injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`party_permanent_stats`](./Events_and_Encounters.md#object-party-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of all party members. | 0 |
| [`party_permanent_stats_exclude_self`](./Events_and_Encounters.md#object-party-permanent-stats-exclude-self) | Object | Event Reward: Permanently modifies stats for all party members except the one who initiated the action. | 0 |
| `party_random_mutation` | Number |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`party_status_next_fight`](./Events_and_Encounters.md#object-party-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect to the entire party at the start of the next combat encounter. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`play_result_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_mutation_from_set`](./Events_and_Encounters.md#object-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to a character from a specific pool. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_basic_attack`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `self_damage` | Number | Recoil or self-inflicted damage/effects applied to the caster. | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_age` | Number |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `spawn_reflection_next_fight` | Number | Event Penalty: Spawns dark clones/reflections of the party in the next combat encounter. | 0 |
| [`spawn_unit_next_fight`](./Events_and_Encounters.md#object-spawn-unit-next-fight) | Object | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `mutation`



<details>
<summary><b>Expand</b></summary>

> **Total Count:** 24

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`good`](./Events_and_Encounters.md#context-good), [`rare`](./Events_and_Encounters.md#context-rare), [`spawn_reflection_next_fight`](./Events_and_Encounters.md#context-spawn_reflection_next_fight)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `eyes` | Number |  | 12 |
| `mouth` | Number |  | 11 |
| `ears` | Number |  | 10 |
| `eyebrows` | Number |  | 8 |
| `head` | Number | Event Node: Story branch or dialog option representing the 'Head' action. | 7 |
| `legs` | Number |  | 7 |
| `arms` | Number |  | 6 |
| `body` | Number | Event Node: Story branch or dialog option representing the 'Body' action. | 6 |
| `tail` | Number | Event Node: Story branch or dialog option representing the 'Tail' action. | 6 |
| `eye1` | Number |  | 3 |
| `arm1` | Number |  | 2 |
| `ear1` | Number |  | 2 |
| `eyebrow1` | Number |  | 2 |
| `leg1` | Number |  | 2 |
| `eye2` | Number |  | 1 |

</details>

---

### Object: `eat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 23

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 23 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 23 |
| [`stat`](./Math_Equations.md) | Equation |  | 23 |
| [`label`](./Strings.md#string-label) | Mixed |  | 23 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `party_status_next_fight`


**Definition:** Event Penalty/Reward: Applies a status effect to the entire party at the start of the next combat encounter.  
**Total Count:** 24

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 23

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`rare`](./Events_and_Encounters.md#context-rare)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 22 |

</details>

---

### Object: `setup`



<details>
<summary><b>Expand</b></summary>

> **Total Count:** 23

> **Referenced by:** [`main`](./Events_and_Encounters.md#context-main)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| `set_frame` | `Number` |  | 0 |

</details>

---

### Object: `cutscene`



<details>
<summary><b>Expand</b></summary>

> **Total Count:** 22

> **Referenced by:** [`bad`](./Events_and_Encounters.md#context-bad), [`good`](./Events_and_Encounters.md#context-good)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 22 |
| `skip_result_screen` | Boolean |  | 21 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | `String` | Event Node: Triggers a narrative cutscene. | 0 |

</details>

---

### Object: `random_mutation_from_set`


**Definition:** Event Reward: Applies a random mutation to a character from a specific pool.  
**Total Count:** 22

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 21

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`rare`](./Events_and_Encounters.md#context-rare)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `mouth` | Number |  | 9 |
| `count` | Number | Quantity. | 8 |
| `tail` | Number | Event Node: Story branch or dialog option representing the 'Tail' action. | 7 |
| `ears` | Number |  | 5 |
| `eyes` | Number |  | 5 |
| `legs` | Number |  | 5 |
| `body` | Number | Event Node: Story branch or dialog option representing the 'Body' action. | 4 |
| `eyebrows` | Number |  | 3 |
| `head` | Number | Event Node: Story branch or dialog option representing the 'Head' action. | 3 |
| `arm1` | Number |  | 2 |
| `arm2` | Number |  | 2 |
| `leg1` | Number |  | 1 |
| `leg2` | Number |  | 1 |
| `texture` | Number |  | 1 |

</details>

---

### Object: `smash`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 14 |
| [`label`](./Strings.md#string-label) | String |  | 15 |
| [`stat`](./Enums.md#enum-stat) | Mixed |  | 15 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 14 |
| [`copy_results`](./Enums.md#enum-copy_results) | Enum |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `destroy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 14 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 14 |
| [`label`](./Strings.md#string-label) | String |  | 14 |
| [`stat`](./Math_Equations.md) | Equation |  | 14 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `bash`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 12 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 12 |
| [`label`](./Strings.md#string-label) | String |  | 12 |
| [`stat`](./Math_Equations.md) | Equation |  | 12 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `open`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 |
| [`label`](./Strings.md#string-label) | String |  | 8 |
| [`stat`](./Math_Equations.md) | Equation |  | 8 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 7 |
| [`copy_results`](./Enums.md#enum-copy_results) | Enum |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `sneak`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 11 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 11 |
| [`stat`](./Math_Equations.md) | Equation |  | 11 |
| [`label`](./Strings.md#string-label) | Mixed |  | 11 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `global_effect_next_fight`


**Definition:** Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter.  
**Total Count:** 11

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`good`](./Events_and_Encounters.md#context-good), [`rare`](./Events_and_Encounters.md#context-rare)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 16 |
| [`KillEnemyOfTypeAtBattleStart`](./Events_and_Encounters.md#context-killenemyoftypeatbattlestart) | Object | Encounter Modifier: Instantly kills one enemy of the specified type at the start of battle. | 2 |
  | `Fights` | Number | Applies or references the 'Fights' effect/state. | 0 |
  | [`StatusRandomEnemiesOnBattleStart`](#statusrandomenemiesonbattlestart) | Object | Applies or references the 'StatusRandomEnemiesOnBattleStart' effect/state. | 0 |
  | [`CharacterTypeGainsStatusAtBattleStart`](#charactertypegainsstatusatbattlestart) | Object | Encounter Modifier: Applies a status effect to all characters of a specific type (e.g., Cats, Bosses) at the start of battle. | 0 |

</details>

---

### Object: `take`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 8 |
| [`label`](./Strings.md#string-label) | String |  | 8 |
| [`stat`](./Math_Equations.md) | Equation |  | 8 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `a`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 7 |
| [`label`](./Strings.md#string-label) | String |  | 7 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 7 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 5 |

</details>

---

### Object: `attack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |
| [`label`](./Strings.md#string-label) | String |  | 7 |
| [`stat`](./Math_Equations.md) | Equation |  | 7 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 6 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`ambush`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `ambush_next_basic_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clear_result_animation` | Number |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `damage` | Number | Event Node: Story branch or dialog option representing the 'Damage' action. | 0 |
| [`decrement_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| `gain_cat_familiar` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_coins`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_familiar`](./Events_and_Encounters.md#object-gain-familiar) | Enum/String | Event Action: Adds a specific familiar to the party. | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_and_equip_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| `hide_appearance_changes` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`leave_party_temporarily`](./Events_and_Encounters.md#object-leave-party-temporarily) | Object | Event Action: Removes a character from the active team until the next hub area. | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_all_equipped_items`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item_from_inventory`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`make_old`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Enum/String | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `party_damage` | Number |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| `party_heal` | Number |  | 0 |
| `party_heal_disorder` | Number |  | 0 |
| `party_heal_injury` | Number |  | 0 |
| [`party_injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`party_permanent_stats`](./Events_and_Encounters.md#object-party-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of all party members. | 0 |
| [`party_permanent_stats_exclude_self`](./Events_and_Encounters.md#object-party-permanent-stats-exclude-self) | Object | Event Reward: Permanently modifies stats for all party members except the one who initiated the action. | 0 |
| `party_random_mutation` | Number |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`party_status_next_fight`](./Events_and_Encounters.md#object-party-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect to the entire party at the start of the next combat encounter. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`play_result_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_mutation_from_set`](./Events_and_Encounters.md#object-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to a character from a specific pool. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_basic_attack`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `self_damage` | Number | Recoil or self-inflicted damage/effects applied to the caster. | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_age` | Number |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `spawn_reflection_next_fight` | Number | Event Penalty: Spawns dark clones/reflections of the party in the next combat encounter. | 0 |
| [`spawn_unit_next_fight`](./Events_and_Encounters.md#object-spawn-unit-next-fight) | Object | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `b`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 7 |
| [`label`](./Strings.md#string-label) | String |  | 7 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 7 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 5 |

</details>

---

### Object: `c`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 7 |
| [`label`](./Strings.md#string-label) | String |  | 7 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 7 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 5 |

</details>

---

### Object: `charm`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 7 |
| [`stat`](./Math_Equations.md) | Equation |  | 7 |
| [`label`](./Strings.md#string-label) | Mixed |  | 7 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `fight`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 7 |
| [`stat`](./Math_Equations.md) | Equation |  | 7 |
| [`label`](./Strings.md#string-label) | Mixed |  | 7 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `leave_party_temporarily`


**Definition:** Event Action: Removes a character from the active team until the next hub area.  
**Total Count:** 9

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`rare`](./Events_and_Encounters.md#context-rare)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `fights_skipped` | Number |  | 7 |
| [`return_as`](./Enums.md#enum-return_as) | Enum |  | 3 |
| [`return_during`](./Enums.md#enum-return_during) | Enum |  | 3 |

</details>

---

### Object: `touch`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 7 |
| [`label`](./Strings.md#string-label) | Mixed |  | 7 |
| [`stat`](./Enums.md#enum-stat) | Mixed |  | 7 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 6 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `activate_p`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 6 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 6 |
| [`label`](./Enums.md#enum-label) | Enum |  | 6 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 6 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 6 |

</details>

---

### Object: `activate_z`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 6 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 6 |
| [`label`](./Enums.md#enum-label) | Enum |  | 6 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 6 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 6 |

</details>

---

### Object: `d`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 6 |
| [`label`](./Strings.md#string-label) | String |  | 6 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 6 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 5 |

</details>

---

### Object: `enter`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 6 |
| [`label`](./Strings.md#string-label) | Mixed |  | 6 |
| [`stat`](./Enums.md#enum-stat) | Mixed |  | 5 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`hint_chapter_exit`](./Enums.md#enum-hint_chapter_exit) | Enum |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `inspect`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 6 |
| [`label`](./Strings.md#string-label) | String |  | 6 |
| [`stat`](./Math_Equations.md) | Equation |  | 6 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `lick`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 6 |
| [`label`](./Strings.md#string-label) | Mixed |  | 6 |
| [`stat`](./Enums.md#enum-stat) | Mixed |  | 6 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `next_event_from_set`


**Definition:** Event Action: Chains immediately into a randomly selected subsequent story event.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`good`](./Events_and_Encounters.md#context-good), [`rare`](./Events_and_Encounters.md#context-rare)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`event`](./Enums.md#enum-event) | Enum |  | 5 |
| `same_cat` | Boolean |  | 5 |
| `count` | Number | Quantity. | 4 |

</details>

---

### Object: `CharacterTypeGainsStatusAtBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`global_effect_next_fight`](./Events_and_Encounters.md#context-global_effect_next_fight)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 |
| [`tag`](./Enums.md#enum-tag) | Enum | Specific entity tag required. | 5 |

</details>

---

### Object: `drink`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 5 |
| [`stat`](./Math_Equations.md) | Equation |  | 5 |
| [`label`](./Strings.md#string-label) | Mixed |  | 5 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `kiss`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 5 |
| [`label`](./Strings.md#string-label) | String |  | 5 |
| [`stat`](./Math_Equations.md) | Equation |  | 5 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `run`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 5 |
| [`label`](./Strings.md#string-label) | String |  | 5 |
| [`stat`](./Math_Equations.md) | Equation |  | 5 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 2 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `bite`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 4 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 4 |
| [`label`](./Enums.md#enum-label) | Enum |  | 4 |
| [`stat`](./Math_Equations.md) | Equation |  | 4 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `damage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 4 |
| [`label`](./Strings.md#string-label) | String |  | 4 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 3 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 3 |

</details>

---

### Object: `go_around`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 4 |
| [`label`](./Strings.md#string-label) | String |  | 4 |
| [`stat`](./Enums.md#enum-stat) | Mixed |  | 3 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 2 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `home`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 4 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 4 |
| [`hint_chapter_exit`](./Enums.md#enum-hint_chapter_exit) | Enum |  | 4 |
| [`label`](./Enums.md#enum-label) | Enum |  | 4 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 4 |

</details>

---

### Object: `outcome`



<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`main`](./Events_and_Encounters.md#context-main)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`weather_roll`](./Arrays.md#array-weather_roll) | Array |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | `Array` |  | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | `Array` |  | 0 |

</details>

---

### Object: `party_permanent_stats_exclude_self`


**Definition:** Event Reward: Permanently modifies stats for all party members except the one who initiated the action.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`rare`](./Events_and_Encounters.md#context-rare)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 4 |
| `con` | Number |  | 4 |
| `dex` | Number |  | 4 |
| `int` | Number |  | 4 |
| `lck` | Number |  | 4 |
| `spd` | Number |  | 4 |
| `str` | Number |  | 4 |

</details>

---

### Object: `past`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 4 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 4 |
| [`hint_chapter_exit`](./Enums.md#enum-hint_chapter_exit) | Enum |  | 4 |
| [`label`](./Enums.md#enum-label) | Enum |  | 4 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 4 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 4 |

</details>

---

### Object: `skip`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 4 |
| [`label`](./Strings.md#string-label) | String |  | 4 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 4 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | Object | Event Node: Triggers a narrative cutscene. | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `StatusRandomEnemiesOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`global_effect_next_fight`](./Events_and_Encounters.md#context-global_effect_next_fight)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |
| `count` | Number | Quantity. | 3 |

</details>

---

### Object: `investigate`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 3 |
| [`label`](./Strings.md#string-label) | String |  | 3 |
| [`stat`](./Math_Equations.md) | Equation |  | 3 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `repell`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 3 |
| [`label`](./Strings.md#string-label) | String |  | 3 |
| [`stat`](./Math_Equations.md) | Equation |  | 3 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `spawn_reflection_next_fight`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`rare`](./Events_and_Encounters.md#context-rare)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
  | [`mutation`](#mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
  | [`gain_familiar`](./Enums.md#enum-gain_familiar) | Enum | Event Action: Adds a specific familiar to the party. | 0 |

</details>

---

### Object: `KillEnemyOfTypeAtBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`global_effect_next_fight`](./Events_and_Encounters.md#context-global_effect_next_fight)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`enemy_type`](./Enums.md#enum-enemy_type) | Enum |  | 2 |
| [`fallback_spawn`](./Arrays.md#array-fallback_spawn) | Array |  | 1 |

</details>

---

### Object: `attach_antenna`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 2 |
| [`label`](./Enums.md#enum-label) | Enum |  | 2 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 2 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 2 |

</details>

---

### Object: `boogers`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 2 |
| [`label`](./Strings.md#string-label) | String |  | 2 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 2 |

</details>

---

### Object: `copy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 2 |
| [`label`](./Strings.md#string-label) | String |  | 2 |

</details>

---

### Object: `find_another_way`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 2 |
| [`label`](./Strings.md#string-label) | String |  | 2 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `move_closer`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 2 |
| [`label`](./Strings.md#string-label) | String |  | 2 |
| [`stat`](./Math_Equations.md) | Equation |  | 2 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `party_permanent_stats`


**Definition:** Event Reward: Permanently increases (or decreases) the core stats of all party members.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`main`](./Events_and_Encounters.md#context-main), [`rare`](./Events_and_Encounters.md#context-rare)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 2 |

</details>

---

### Object: `party_random_mutation_from_set`


**Definition:** Event Reward: Applies a random mutation to the entire party from a specific pool.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`bad`](./Events_and_Encounters.md#context-bad), [`rare`](./Events_and_Encounters.md#context-rare)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `count` | Number | Quantity. | 2 |
| `ears` | Number |  | 2 |
| `eyebrows` | Number |  | 2 |
| `eyes` | Number |  | 2 |
| `mouth` | Number |  | 2 |

</details>

---

### Object: `play`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 2 |
| [`label`](./Strings.md#string-label) | String |  | 2 |
| [`stat`](./Math_Equations.md) | Equation |  | 2 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `poop`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 2 |
| [`label`](./Strings.md#string-label) | String |  | 2 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 2 |

</details>

---

### Object: `print`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 2 |
| [`label`](./Strings.md#string-label) | String |  | 2 |

</details>

---

### Object: `protection`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 2 |
| [`label`](./Strings.md#string-label) | String |  | 2 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 2 |

</details>

---

### Object: `repair`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 2 |
| [`label`](./Strings.md#string-label) | Mixed |  | 2 |
| [`stat`](./Enums.md#enum-stat) | Mixed |  | 2 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `sacrifice`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 2 |
| [`label`](./Strings.md#string-label) | String |  | 2 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `scale`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 2 |
| [`label`](./Strings.md#string-label) | String |  | 2 |

</details>

---

### Object: `turnon`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 2 |
| [`label`](./Strings.md#string-label) | String |  | 2 |
| [`stat`](./Math_Equations.md) | Equation |  | 2 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `altar_sacrifice`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `arm`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `attach_amplifier`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `attach_leech`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `bash_past_alt`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `bite_it_off`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `blue`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`copy_results`](./Enums.md#enum-copy_results) | Enum |  | 1 |
| `fixed_chance` | Number |  | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `blue_needle`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `body`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | Object | Event Node: Triggers a narrative cutscene. | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `book`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `brace`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `break_ice`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
  | [`bad`](#bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |

</details>

---

### Object: `break_lock`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `bribe`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `button`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`copy_results`](./Enums.md#enum-copy_results) | Enum |  | 1 |
| `fixed_chance` | Number |  | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `buy1`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| `stat_max` | Number |  | 1 |
| `stat_min` | Number |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | `String` |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `weight` | `Number` | Probability weight for this outcome. | 0 |

</details>

---

### Object: `catch`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `challenge_to_game`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `chaos_ending`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `chapter_cutscene`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `charm_past_alt`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `climb`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `comfort`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `communicate`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `concheck`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `counter`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `crack_open`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `cross`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `cut_wires`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `damage_1`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `damage_full`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `damage_half`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `desert_cutscene`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `dexcheck`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `dig`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `disarm`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `dive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `donate`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `donate_10`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| `stat_max` | Number |  | 1 |
| `stat_min` | Number |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `donate_15`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| `stat_max` | Number |  | 1 |
| `stat_min` | Number |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `donate_20`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| `stat_max` | Number |  | 1 |
| `stat_min` | Number |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `donate_5`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| `stat_max` | Number |  | 1 |
| `stat_min` | Number |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `double`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `eat_meat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `enter_crater`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Object: `face`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |

</details>

---

### Object: `fiddle`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `fill_jar`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `find`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `fire`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `flush_yourself`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |

</details>

---

### Object: `follow`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `free`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `future`



<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`hint_chapter_exit`](./Enums.md#enum-hint_chapter_exit) | Enum |  | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `gain_clone_familiar`


**Definition:** Event Action: Adds a clone of a character to the party as a familiar.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`good`](./Events_and_Encounters.md#context-good)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 1 |

</details>

---

### Object: `gain_familiar`


**Definition:** Event Action: Adds a specific familiar to the party.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 1 |
| `initial_health` | Number |  | 1 |

</details>

---

### Object: `give_parasite`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `hack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
  | [`bad`](#bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |

</details>

---

### Object: `head`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |

</details>

---

### Object: `holy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `hp`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `ice`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `infinite`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`hint_chapter_exit`](./Enums.md#enum-hint_chapter_exit) | Enum |  | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `intcheck`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
  | [`bad`](#bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |

</details>

---

### Object: `intimidation`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `itchies`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | Object | Event Node: Triggers a narrative cutscene. | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `join`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `jump`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `jump_over`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `keep_going`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `kiss_meat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `knife`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `leave_it_in`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `leg`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `lever`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| `fixed_chance` | Number |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `lick_alt`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `lightning`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `listen`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
  | [`bad`](#bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |

</details>

---

### Object: `looks`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `loot_heart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `makeup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `mind`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
  | [`bad`](#bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |

</details>

---

### Object: `neck`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |

</details>

---

### Object: `nothanks`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `outsmart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Object: `patch_up`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `pick_lock`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `pilfer`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `pirouette`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `place_gristle`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `power`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `pull`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `pull_it_out`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `pull_lever`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `purify`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `push_buttons`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `push_through`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `put_in_coins`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| `stat_max` | Number |  | 1 |
| `stat_min` | Number |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `put_out_of_misery`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `random_chance`


**Definition:** Event Logic: Executes the nested outcome based on a percentage roll.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`reward`](./Events_and_Encounters.md#context-reward)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| `chance` | Number | Probability weight for this outcome. | 1 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | `Enum/String` | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |

</details>

---

### Object: `reach_inside`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Object: `read`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `receive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `red`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| `fixed_chance` | Number |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `red_needle`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `reflect`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `remove`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `remove_the_nail`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `repair_quest`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `rest`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
  | [`bad`](#bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |

</details>

---

### Object: `revive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
  | [`bad`](#bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |

</details>

---

### Object: `rub`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Object: `run_again`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `run_away`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `sacrifice_full_favor`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `sacrifice_normal`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Object: `sacrifice_partial_favor`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `sacrifice_quest`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `scream`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `shake`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
  | [`bad`](#bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
  | `ignore` | Any | Explicit empirical property. | 0 |

</details>

---

### Object: `slip_through`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `sneak_by`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `sneak_past_alt`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `soul`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
  | [`bad`](#bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |

</details>

---

### Object: `speed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `surprise`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `sweet_talk`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `swim`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `tail`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `take_blood`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `talk`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `talk_to`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `tappytoes`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `teleport`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `thorns`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `throw`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
  | `ignore` | Any | Explicit empirical property. | 0 |

</details>

---

### Object: `timemachine`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `traverse`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | `String` |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `upgrade_yourself`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `use_item`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `use_toilet_con`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `use_toilet_str`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `use_weapon`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
  | [`sfx`](./Enums.md#enum-sfx) | Enum | `BeaniesEnding_Banging`, `FireExtinguish`, `Intro_LabDisposal`, `PickupCoin`, `UISFX_BeaniesAppear` | 0 |
  | `unlock_controls` | Any | Explicit empirical property. | 0 |
  | `get_token` | Any | Explicit empirical property. | 0 |
  | `dialog_and_autopass` | Any | Explicit empirical property. | 0 |
  | `dialog` | Any | Explicit empirical property. | 0 |
  | `set_state` | Any | Explicit empirical property. | 0 |
  | `wait_for` | Any | Explicit empirical property. | 0 |

</details>

---

### Object: `w1`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `w2`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `w3`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `w4`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `w5`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `w6`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `wealth`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `wheezies`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | Object | Event Node: Triggers a narrative cutscene. | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `wish_genes`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `wish_items`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `wish_levelups`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `wish_strength`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Object: `withstand`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `yank_it_out`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

### Object: `yellow_needle`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Object | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Object | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`add_weather`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `ally_ambush_next_fights` | Number |  | 0 |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Event Node: Story branch or dialog option representing the 'Bad' action. | 0 |
| [`battle`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`begin_chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`clear_surviving_kaiju`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `clone_self_to_party` | Number |  | 0 |
| [`complete_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional-reward) | Object | Event Action: Provides a reward only if a specific condition is met. | 0 |
| `copy_items_to_party` | Number |  | 0 |
| `copy_party_items` | Number |  | 0 |
| [`cutscene`](./Events_and_Encounters.md#object-cutscene) | String | Event Node: Triggers a narrative cutscene. | 0 |
| [`cutscene_on_exit`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`event_now_same_cat`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `full_heal` | Number |  | 0 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain-clone-familiar) | Object | Event Action: Adds a clone of a character to the party as a familiar. | 0 |
| [`gain_disorder`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`gain_food`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`gain_immortal_familiar`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_full_item_set_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_item_from_pool`](./Events_and_Encounters.md#object-get-item-from-pool) | Enum/String | Event Action: Rewards the player with an item drawn from a specific loot pool. | 0 |
| [`get_parasite`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`get_parasite_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global-effect-next-fight) | Object | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 0 |
| `heal` | Number |  | 0 |
| `heal_disorder` | Number |  | 0 |
| `heal_injury` | Number |  | 0 |
| [`increment_legacy_counter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`kill`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_ability_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`learn_passive_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`level_up`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`lose_specific_item`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object | Event Node: Story branch or dialog option representing the 'Mutation' action. | 0 |
| `next_event_bonus` | Number |  | 0 |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next-event-from-set) | Object | Event Action: Chains immediately into a randomly selected subsequent story event. | 0 |
| [`override_end_option_prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| [`party_gain_disorder_from_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party-random-mutation-from-set) | Object | Event Reward: Applies a random mutation to the entire party from a specific pool. | 0 |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent-stats) | Object | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 0 |
| [`play_animation`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`prompt`](./Engine_EventKeys.md#valid-property-keys) | String |  | 0 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 0 |
| [`random_pool`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`random_pool_consider_luck`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`rare`](./Events_and_Encounters.md#object-rare) | Object | Event Node: Story branch or dialog option representing the 'Rare' action. | 0 |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object | Event Node: Story branch or dialog option representing the 'Reward' action. | 0 |
| [`scramble_abilities`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`scramble_passives`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`select_item_from_pool_for_cutscene_only`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self-status-next-fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 0 |
| [`set_adventure_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `set_frame` | Number |  | 0 |
| [`set_legacy_token`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`shop_now`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`transform_item`](./Engine_EventKeys.md#valid-property-keys) | Array |  | 0 |
| [`trigger_adventure_unlock`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| `trigger_butterfly_effect` | Number |  | 0 |
| [`unlock_item_quest`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_ability`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |
| [`upgrade_passive`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 0 |

</details>

---

