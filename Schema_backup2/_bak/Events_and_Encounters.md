# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Math_Equations.md).

## Events & Encounters

> **Associated Files:** `data/events/`


### Context: `ROOT` (214 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`intro`](./Events_and_Encounters.md#context-intro) | Block | Event Node: The initial text block when a story event first loads. | 214 |
| [`main`](./Events_and_Encounters.md#context-main) | Block | Event Node: The central hub or recurring menu of a story event. | 214 |
| [`label`](./Strings.md#string-label) | String |  | 15 |
| [`stat`](./Math_Equations.md) | Equation |  | 15 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 12 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 10 |
| [`prompt`](./Strings.md#string-prompt) | String |  | 9 |
| `set_frame` | Number |  | 9 |
| [`copy_results`](./Enums.md#enum-copy_results) | Enum |  | 8 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 7 |
| [`get_item_from_pool`](./Enums.md#enum-get_item_from_pool) | Enum | Event Action: Rewards the player with an item drawn from a specific loot pool. | 5 |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 4 |
| [`reward`](./Events_and_Encounters.md#context-reward) | Block | Event Node: Story branch or dialog option representing the 'Reward' action. | 4 |
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum |  | 3 |
| `stat_max` | Number |  | 3 |
| `stat_min` | Number |  | 3 |
| `weight` | Number | Probability weight for this outcome. | 3 |
| `cha` | Number |  | 2 |
| `con` | Number |  | 2 |
| [`ignore`](./Events_and_Encounters.md#context-ignore) | Block | Event Node: Story branch or dialog option representing the 'Ignore' action. | 2 |
| `int` | Number |  | 2 |
| `lck` | Number |  | 2 |
| `spd` | Number |  | 2 |
| `str` | Number |  | 2 |
| [`10coins`](./Events_and_Encounters.md#context-10coins) | Block | Event Action: Grants or consumes 10 coins. | 1 |
| [`add_weather`](./Enums.md#enum-add_weather) | Enum |  | 1 |
| [`destroy`](./Events_and_Encounters.md#context-destroy) | Block | Event Node: Story branch or dialog option representing the 'Destroy' action. | 1 |
| `dex` | Number |  | 1 |
| [`gain_familiar`](./Enums.md#enum-gain_familiar) | Enum | Event Action: Adds a specific familiar to the party. | 1 |
| `next_event_bonus` | Number |  | 1 |
| [`requires_flag`](./Enums.md#enum-requires_flag) | Enum | Prerequisite: Must meet this condition. | 1 |
| [`self_status_next_fight`](./Events_and_Encounters.md#context-self_status_next_fight) | Block | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 1 |

</details>

---

### Context: `reward` (757 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`bad`](./Events_and_Encounters.md#context-bad), [`conditional_reward`](./Events_and_Encounters.md#context-conditional_reward), [`good`](./Events_and_Encounters.md#context-good)

> **Engine Schema:** This block is a `[event_node]` container. [View all confirmed values in Engine_Events.md](./Engine_Events.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[event_node]`](./Engine_Events.md#all-confirmed-event-node-values) | Block | An event outcome node. See Engine_Events.md for the full schema. |
| [`common`](./Events_and_Encounters.md#context-common) | Block | Event Node: Story branch or dialog option representing the 'Common' action. | 633 |
| [`rare`](./Events_and_Encounters.md#context-rare) | Block | Event Node: Story branch or dialog option representing the 'Rare' action. | 623 |
| [`prompt`](./Strings.md#string-prompt) | String |  | 72 |
| `set_frame` | Number |  | 54 |
| [`clear_adventure_token`](./Enums.md#enum-clear_adventure_token) | Enum |  | 24 |
| [`get_item_from_pool`](./Enums.md#enum-get_item_from_pool) | Enum | Event Action: Rewards the player with an item drawn from a specific loot pool. | 14 |
| [`set_adventure_token`](./Enums.md#enum-set_adventure_token) | Enum |  | 9 |
| [`set_subject`](./Enums.md#enum-set_subject) | Enum |  | 9 |
| [`random_pool`](./Arrays.md#array-random_pool) | Array |  | 8 |
| `next_event_bonus` | Number |  | 5 |
| [`trigger_adventure_unlock`](./Enums.md#enum-trigger_adventure_unlock) | Enum |  | 5 |
| [`play_animation`](./Arrays.md#array-play_animation) | Array |  | 4 |
| [`cutscene_on_exit`](./Enums.md#enum-cutscene_on_exit) | Enum |  | 3 |
| [`gain_disorder_from_pool`](./Enums.md#enum-gain_disorder_from_pool) | Enum |  | 2 |
| [`injury`](./Math_Equations.md) | Equation |  | 2 |
| [`spawn_unit_next_fight`](./Events_and_Encounters.md#context-spawn_unit_next_fight) | Block | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. | 2 |
| [`event_now`](./Enums.md#enum-event_now) | Enum |  | 1 |
| [`gain_coins`](./Arrays.md#array-gain_coins) | Array |  | 1 |
| [`get_item`](./Enums.md#enum-get_item) | Enum |  | 1 |
| [`get_parasite_from_pool`](./Enums.md#enum-get_parasite_from_pool) | Enum |  | 1 |
| [`party_damage`](./Arrays.md#array-party_damage) | Array |  | 1 |
| [`random_chance`](./Events_and_Encounters.md#context-random_chance) | Block | Event Logic: Executes the nested outcome based on a percentage roll. | 1 |
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum |  | 1 |
| `weight` | Number | Probability weight for this outcome. | 1 |

</details>

---

### Context: `common` (633 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`reward`](./Events_and_Encounters.md#context-reward)

> **Engine Schema:** This block is a `[event_node]` container. [View all confirmed values in Engine_Events.md](./Engine_Events.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[event_node]`](./Engine_Events.md#all-confirmed-event-node-values) | Block | An event outcome node. See Engine_Events.md for the full schema. |
| [`prompt`](./Strings.md#string-prompt) | String |  | 608 |
| `set_frame` | Number |  | 150 |
| [`self_status_next_fight`](./Events_and_Encounters.md#context-self_status_next_fight) | Block | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 93 |
| [`get_item_from_pool`](./Enums.md#enum-get_item_from_pool) | Enum | Event Action: Rewards the player with an item drawn from a specific loot pool. | 71 |
| [`permanent_stats`](./Events_and_Encounters.md#context-permanent_stats) | Block | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 41 |
| [`random_pool`](./Arrays.md#array-random_pool) | Array |  | 36 |
| [`damage`](./Arrays.md#array-damage) | Array | Event Node: Story branch or dialog option representing the 'Damage' action. | 35 |
| [`gain_coins`](./Arrays.md#array-gain_coins) | Array |  | 28 |
| [`injury`](./Math_Equations.md) | Equation |  | 27 |
| `self_damage` | Number | Recoil or self-inflicted damage/effects applied to the caster. | 26 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 25 |
| [`clear_adventure_token`](./Enums.md#enum-clear_adventure_token) | Enum |  | 24 |
| [`gain_disorder_from_pool`](./Enums.md#enum-gain_disorder_from_pool) | Enum |  | 24 |
| [`play_animation`](./Enums.md#enum-play_animation) | Enum |  | 23 |
| [`event_now_same_cat`](./Enums.md#enum-event_now_same_cat) | Enum |  | 21 |
| [`gain_food`](./Arrays.md#array-gain_food) | Array |  | 21 |
| [`gain_familiar`](./Enums.md#enum-gain_familiar) | Enum | Event Action: Adds a specific familiar to the party. | 19 |
| [`spawn_unit_next_fight`](./Events_and_Encounters.md#context-spawn_unit_next_fight) | Block | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. | 18 |
| [`party_damage`](./Arrays.md#array-party_damage) | Array |  | 15 |
| `party_heal` | Number |  | 15 |
| [`get_item`](./Enums.md#enum-get_item) | Enum |  | 14 |
| `heal` | Number |  | 13 |
| [`gain_disorder`](./Enums.md#enum-gain_disorder) | Enum |  | 12 |
| [`get_parasite_from_pool`](./Arrays.md#array-get_parasite_from_pool) | Array |  | 11 |
| [`override_end_option_prompt`](./Strings.md#string-override_end_option_prompt) | String |  | 11 |
| [`party_status_next_fight`](./Events_and_Encounters.md#context-party_status_next_fight) | Block | Event Penalty/Reward: Applies a status effect to the entire party at the start of the next combat encounter. | 11 |
| `ally_ambush_next_fights` | Number |  | 10 |
| `full_heal` | Number |  | 10 |
| `ambush_next_basic_fights` | Number |  | 9 |
| [`conditional_reward`](./Events_and_Encounters.md#context-conditional_reward) | Block | Event Action: Provides a reward only if a specific condition is met. | 9 |
| [`set_adventure_token`](./Enums.md#enum-set_adventure_token) | Enum |  | 9 |
| [`random_mutation_from_set`](./Events_and_Encounters.md#context-random_mutation_from_set) | Block | Event Reward: Applies a random mutation to a character from a specific pool. | 8 |
| [`get_parasite`](./Enums.md#enum-get_parasite) | Enum |  | 7 |
| `next_event_bonus` | Number |  | 7 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#context-global_effect_next_fight) | Block | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 6 |
| [`increment_legacy_counter`](./Enums.md#enum-increment_legacy_counter) | Enum |  | 6 |
| [`kill`](./Enums.md#enum-kill) | Enum |  | 5 |
| [`lose_item`](./Enums.md#enum-lose_item) | Enum |  | 5 |
| [`shop_now`](./Enums.md#enum-shop_now) | Enum |  | 5 |
| [`add_weather`](./Enums.md#enum-add_weather) | Enum |  | 4 |
| [`event_now`](./Enums.md#enum-event_now) | Enum |  | 2 |
| [`lose_specific_item`](./Enums.md#enum-lose_specific_item) | Enum |  | 2 |
| [`next_event_from_set`](./Events_and_Encounters.md#context-next_event_from_set) | Block | Event Action: Chains immediately into a randomly selected subsequent story event. | 2 |
| `party_heal_disorder` | Number |  | 2 |
| [`party_permanent_stats_exclude_self`](./Events_and_Encounters.md#context-party_permanent_stats_exclude_self) | Block | Event Reward: Permanently modifies stats for all party members except the one who initiated the action. | 2 |
| [`spin`](./Enums.md#enum-spin) | Enum |  | 2 |
| `clear_result_animation` | Number |  | 1 |
| [`decrement_legacy_counter`](./Enums.md#enum-decrement_legacy_counter) | Enum |  | 1 |
| [`get_and_equip_item`](./Enums.md#enum-get_and_equip_item) | Enum |  | 1 |
| `heal_disorder` | Number |  | 1 |
| `heal_injury` | Number |  | 1 |
| [`learn_ability_from_pool`](./Enums.md#enum-learn_ability_from_pool) | Enum |  | 1 |
| [`mutation`](./Events_and_Encounters.md#context-mutation) | Block | Event Node: Story branch or dialog option representing the 'Mutation' action. | 1 |
| `self_heal` | Number |  | 1 |
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum |  | 1 |
| [`upgrade_ability`](./Enums.md#enum-upgrade_ability) | Enum |  | 1 |

</details>

---

### Context: `rare` (633 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`attack`](./Events_and_Encounters.md#context-attack), [`good`](./Events_and_Encounters.md#context-good), [`loot`](./Events_and_Encounters.md#context-loot), [`main`](./Events_and_Encounters.md#context-main), [`options`](./Events_and_Encounters.md#context-options), [`reward`](./Events_and_Encounters.md#context-reward)

> **Engine Schema:** This block is a `[event_node]` container. [View all confirmed values in Engine_Events.md](./Engine_Events.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[event_node]`](./Engine_Events.md#all-confirmed-event-node-values) | Block | An event outcome node. See Engine_Events.md for the full schema. |
| [`prompt`](./Strings.md#string-prompt) | String |  | 612 |
| `set_frame` | Number |  | 179 |
| [`get_item_from_pool`](./Enums.md#enum-get_item_from_pool) | Enum | Event Action: Rewards the player with an item drawn from a specific loot pool. | 124 |
| [`permanent_stats`](./Events_and_Encounters.md#context-permanent_stats) | Block | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 84 |
| [`gain_disorder`](./Enums.md#enum-gain_disorder) | Enum |  | 65 |
| [`gain_disorder_from_pool`](./Enums.md#enum-gain_disorder_from_pool) | Enum |  | 51 |
| [`injury`](./Math_Equations.md) | Equation |  | 51 |
| [`get_item`](./Enums.md#enum-get_item) | Enum |  | 41 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 40 |
| [`self_status_next_fight`](./Events_and_Encounters.md#context-self_status_next_fight) | Block | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 40 |
| [`event_now_same_cat`](./Enums.md#enum-event_now_same_cat) | Enum |  | 30 |
| [`get_parasite`](./Enums.md#enum-get_parasite) | Enum |  | 30 |
| [`gain_familiar`](./Enums.md#enum-gain_familiar) | Enum | Event Action: Adds a specific familiar to the party. | 29 |
| [`random_pool`](./Arrays.md#array-random_pool) | Array |  | 29 |
| [`get_parasite_from_pool`](./Enums.md#enum-get_parasite_from_pool) | Enum |  | 24 |
| [`conditional_reward`](./Events_and_Encounters.md#context-conditional_reward) | Block | Event Action: Provides a reward only if a specific condition is met. | 22 |
| [`set_adventure_token`](./Enums.md#enum-set_adventure_token) | Enum |  | 22 |
| [`spawn_unit_next_fight`](./Events_and_Encounters.md#context-spawn_unit_next_fight) | Block | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. | 20 |
| `damage` | Number | Event Node: Story branch or dialog option representing the 'Damage' action. | 18 |
| [`mutation`](./Events_and_Encounters.md#context-mutation) | Block | Event Node: Story branch or dialog option representing the 'Mutation' action. | 18 |
| [`gain_coins`](./Arrays.md#array-gain_coins) | Array |  | 17 |
| `next_event_bonus` | Number |  | 14 |
| [`random_mutation_from_set`](./Events_and_Encounters.md#context-random_mutation_from_set) | Block | Event Reward: Applies a random mutation to a character from a specific pool. | 13 |
| `self_damage` | Number | Recoil or self-inflicted damage/effects applied to the caster. | 13 |
| [`party_status_next_fight`](./Events_and_Encounters.md#context-party_status_next_fight) | Block | Event Penalty/Reward: Applies a status effect to the entire party at the start of the next combat encounter. | 12 |
| [`play_animation`](./Arrays.md#array-play_animation) | Array |  | 11 |
| [`learn_passive`](./Enums.md#enum-learn_passive) | Enum |  | 10 |
| `party_damage` | Number |  | 10 |
| `party_heal` | Number |  | 10 |
| [`battle`](./Math_Equations.md) | Equation |  | 9 |
| [`increment_legacy_counter`](./Enums.md#enum-increment_legacy_counter) | Enum |  | 9 |
| [`override_end_option_prompt`](./Strings.md#string-override_end_option_prompt) | String |  | 8 |
| `party_random_mutation` | Number |  | 8 |
| `ambush_next_basic_fights` | Number |  | 7 |
| [`leave_party_temporarily`](./Events_and_Encounters.md#context-leave_party_temporarily) | Block | Event Action: Removes a character from the active team until the next hub area. | 7 |
| [`lose_item`](./Enums.md#enum-lose_item) | Enum |  | 7 |
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum |  | 7 |
| [`gain_food`](./Arrays.md#array-gain_food) | Array |  | 6 |
| `hide_appearance_changes` | Number |  | 6 |
| [`shop_now`](./Enums.md#enum-shop_now) | Enum |  | 6 |
| `ally_ambush_next_fights` | Number |  | 5 |
| [`decrement_legacy_counter`](./Enums.md#enum-decrement_legacy_counter) | Enum |  | 5 |
| [`add_weather`](./Enums.md#enum-add_weather) | Enum |  | 4 |
| `full_heal` | Number |  | 4 |
| [`learn_ability`](./Enums.md#enum-learn_ability) | Enum |  | 4 |
| `gain_cat_familiar` | Number |  | 3 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#context-global_effect_next_fight) | Block | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 3 |
| [`kill`](./Enums.md#enum-kill) | Enum |  | 3 |
| [`level_up`](./Enums.md#enum-level_up) | Enum |  | 3 |
| [`lose_item_from_inventory`](./Enums.md#enum-lose_item_from_inventory) | Enum |  | 3 |
| [`make_old`](./Enums.md#enum-make_old) | Enum |  | 3 |
| [`next_event_from_set`](./Enums.md#enum-next_event_from_set) | Enum | Event Action: Chains immediately into a randomly selected subsequent story event. | 3 |
| `spawn_reflection_next_fight` | Number | Event Penalty: Spawns dark clones/reflections of the party in the next combat encounter. | 3 |
| [`event_now`](./Enums.md#enum-event_now) | Enum |  | 2 |
| [`lose_specific_item`](./Enums.md#enum-lose_specific_item) | Enum |  | 2 |
| `party_heal_disorder` | Number |  | 2 |
| `party_heal_injury` | Number |  | 2 |
| [`party_permanent_stats_exclude_self`](./Events_and_Encounters.md#context-party_permanent_stats_exclude_self) | Block | Event Reward: Permanently modifies stats for all party members except the one who initiated the action. | 2 |
| `set_age` | Number |  | 2 |
| [`upgrade_ability`](./Enums.md#enum-upgrade_ability) | Enum |  | 2 |
| [`upgrade_passive`](./Enums.md#enum-upgrade_passive) | Enum |  | 2 |
| [`ambush`](./Math_Equations.md) | Equation |  | 1 |
| `clear_result_animation` | Number |  | 1 |
| [`gain_immortal_familiar`](./Enums.md#enum-gain_immortal_familiar) | Enum |  | 1 |
| [`get_and_equip_item`](./Enums.md#enum-get_and_equip_item) | Enum |  | 1 |
| `heal_disorder` | Number |  | 1 |
| [`learn_ability_from_pool`](./Enums.md#enum-learn_ability_from_pool) | Enum |  | 1 |
| [`learn_passive_from_pool`](./Enums.md#enum-learn_passive_from_pool) | Enum |  | 1 |
| [`lose_all_equipped_items`](./Enums.md#enum-lose_all_equipped_items) | Enum |  | 1 |
| [`party_injury`](./Enums.md#enum-party_injury) | Enum |  | 1 |
| [`party_permanent_stats`](./Events_and_Encounters.md#context-party_permanent_stats) | Block | Event Reward: Permanently increases (or decreases) the core stats of all party members. | 1 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#context-party_random_mutation_from_set) | Block | Event Reward: Applies a random mutation to the entire party from a specific pool. | 1 |
| [`play_result_animation`](./Enums.md#enum-play_result_animation) | Enum |  | 1 |
| [`scramble_abilities`](./Enums.md#enum-scramble_abilities) | Enum |  | 1 |
| [`scramble_basic_attack`](./Enums.md#enum-scramble_basic_attack) | Enum |  | 1 |
| [`trigger_adventure_unlock`](./Enums.md#enum-trigger_adventure_unlock) | Enum |  | 1 |

</details>

---

### Context: `good` (550 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`10coins`](./Events_and_Encounters.md#context-10coins), [`5coins`](./Events_and_Encounters.md#context-5coins), [`ROOT`](./Events_and_Encounters.md#context-root), [`a`](./Events_and_Encounters.md#context-a), [`activate_p`](./Events_and_Encounters.md#context-activate_p), [`activate_z`](./Events_and_Encounters.md#context-activate_z), [`altar_sacrifice`](./Events_and_Encounters.md#context-altar_sacrifice), [`arm`](./Events_and_Encounters.md#context-arm), [`attach_amplifier`](./Events_and_Encounters.md#context-attach_amplifier), [`attach_antenna`](./Events_and_Encounters.md#context-attach_antenna), [`attach_leech`](./Events_and_Encounters.md#context-attach_leech), [`attack`](./Events_and_Encounters.md#context-attack), [`b`](./Events_and_Encounters.md#context-b), [`bash`](./Events_and_Encounters.md#context-bash), [`bash_past_alt`](./Events_and_Encounters.md#context-bash_past_alt), [`bite`](./Events_and_Encounters.md#context-bite), [`bite_it_off`](./Events_and_Encounters.md#context-bite_it_off), [`blue_needle`](./Events_and_Encounters.md#context-blue_needle), [`boogers`](./Events_and_Encounters.md#context-boogers), [`book`](./Events_and_Encounters.md#context-book), [`brace`](./Events_and_Encounters.md#context-brace), [`break_ice`](./Events_and_Encounters.md#context-break_ice), [`break_lock`](./Events_and_Encounters.md#context-break_lock), [`bribe`](./Events_and_Encounters.md#context-bribe), [`buy1`](./Events_and_Encounters.md#context-buy1), [`c`](./Events_and_Encounters.md#context-c), [`catch`](./Events_and_Encounters.md#context-catch), [`challenge_to_game`](./Events_and_Encounters.md#context-challenge_to_game), [`chaos_ending`](./Events_and_Encounters.md#context-chaos_ending), [`chapter_cutscene`](./Events_and_Encounters.md#context-chapter_cutscene), [`charm`](./Events_and_Encounters.md#context-charm), [`charm_past_alt`](./Events_and_Encounters.md#context-charm_past_alt), [`climb`](./Events_and_Encounters.md#context-climb), [`comfort`](./Events_and_Encounters.md#context-comfort), [`communicate`](./Events_and_Encounters.md#context-communicate), [`concheck`](./Events_and_Encounters.md#context-concheck), [`copy`](./Events_and_Encounters.md#context-copy), [`counter`](./Events_and_Encounters.md#context-counter), [`crack_open`](./Events_and_Encounters.md#context-crack_open), [`cross`](./Events_and_Encounters.md#context-cross), [`cut_wires`](./Events_and_Encounters.md#context-cut_wires), [`d`](./Events_and_Encounters.md#context-d), [`damage`](./Events_and_Encounters.md#context-damage), [`damage_1`](./Events_and_Encounters.md#context-damage_1), [`damage_full`](./Events_and_Encounters.md#context-damage_full), [`damage_half`](./Events_and_Encounters.md#context-damage_half), [`desert_cutscene`](./Events_and_Encounters.md#context-desert_cutscene), [`destroy`](./Events_and_Encounters.md#context-destroy), [`dexcheck`](./Events_and_Encounters.md#context-dexcheck), [`dig`](./Events_and_Encounters.md#context-dig), [`disarm`](./Events_and_Encounters.md#context-disarm), [`dive`](./Events_and_Encounters.md#context-dive), [`donate`](./Events_and_Encounters.md#context-donate), [`donate_10`](./Events_and_Encounters.md#context-donate_10), [`donate_15`](./Events_and_Encounters.md#context-donate_15), [`donate_20`](./Events_and_Encounters.md#context-donate_20), [`donate_5`](./Events_and_Encounters.md#context-donate_5), [`double`](./Events_and_Encounters.md#context-double), [`drink`](./Events_and_Encounters.md#context-drink), [`eat`](./Events_and_Encounters.md#context-eat), [`eat_meat`](./Events_and_Encounters.md#context-eat_meat), [`enter`](./Events_and_Encounters.md#context-enter), [`enter_crater`](./Events_and_Encounters.md#context-enter_crater), [`examine`](./Events_and_Encounters.md#context-examine), [`face`](./Events_and_Encounters.md#context-face), [`fiddle`](./Events_and_Encounters.md#context-fiddle), [`fight`](./Events_and_Encounters.md#context-fight), [`fill_jar`](./Events_and_Encounters.md#context-fill_jar), [`find`](./Events_and_Encounters.md#context-find), [`find_another_way`](./Events_and_Encounters.md#context-find_another_way), [`fire`](./Events_and_Encounters.md#context-fire), [`flush_yourself`](./Events_and_Encounters.md#context-flush_yourself), [`follow`](./Events_and_Encounters.md#context-follow), [`free`](./Events_and_Encounters.md#context-free), [`future`](./Events_and_Encounters.md#context-future), [`give_parasite`](./Events_and_Encounters.md#context-give_parasite), [`go_around`](./Events_and_Encounters.md#context-go_around), [`hack`](./Events_and_Encounters.md#context-hack), [`head`](./Events_and_Encounters.md#context-head), [`holy`](./Events_and_Encounters.md#context-holy), [`home`](./Events_and_Encounters.md#context-home), [`hp`](./Events_and_Encounters.md#context-hp), [`ice`](./Events_and_Encounters.md#context-ice), [`ignore`](./Events_and_Encounters.md#context-ignore), [`infinite`](./Events_and_Encounters.md#context-infinite), [`inspect`](./Events_and_Encounters.md#context-inspect), [`intcheck`](./Events_and_Encounters.md#context-intcheck), [`intimidation`](./Events_and_Encounters.md#context-intimidation), [`investigate`](./Events_and_Encounters.md#context-investigate), [`join`](./Events_and_Encounters.md#context-join), [`jump`](./Events_and_Encounters.md#context-jump), [`jump_over`](./Events_and_Encounters.md#context-jump_over), [`keep_going`](./Events_and_Encounters.md#context-keep_going), [`kiss`](./Events_and_Encounters.md#context-kiss), [`kiss_meat`](./Events_and_Encounters.md#context-kiss_meat), [`knife`](./Events_and_Encounters.md#context-knife), [`leave`](./Events_and_Encounters.md#context-leave), [`leave_it_in`](./Events_and_Encounters.md#context-leave_it_in), [`leg`](./Events_and_Encounters.md#context-leg), [`lever`](./Events_and_Encounters.md#context-lever), [`lick`](./Events_and_Encounters.md#context-lick), [`lick_alt`](./Events_and_Encounters.md#context-lick_alt), [`lightning`](./Events_and_Encounters.md#context-lightning), [`listen`](./Events_and_Encounters.md#context-listen), [`looks`](./Events_and_Encounters.md#context-looks), [`loot`](./Events_and_Encounters.md#context-loot), [`loot_heart`](./Events_and_Encounters.md#context-loot_heart), [`makeup`](./Events_and_Encounters.md#context-makeup), [`move_closer`](./Events_and_Encounters.md#context-move_closer), [`neck`](./Events_and_Encounters.md#context-neck), [`nothanks`](./Events_and_Encounters.md#context-nothanks), [`open`](./Events_and_Encounters.md#context-open), [`outsmart`](./Events_and_Encounters.md#context-outsmart), [`past`](./Events_and_Encounters.md#context-past), [`patch_up`](./Events_and_Encounters.md#context-patch_up), [`pick_lock`](./Events_and_Encounters.md#context-pick_lock), [`pilfer`](./Events_and_Encounters.md#context-pilfer), [`pirouette`](./Events_and_Encounters.md#context-pirouette), [`place_gristle`](./Events_and_Encounters.md#context-place_gristle), [`play`](./Events_and_Encounters.md#context-play), [`poop`](./Events_and_Encounters.md#context-poop), [`power`](./Events_and_Encounters.md#context-power), [`print`](./Events_and_Encounters.md#context-print), [`protection`](./Events_and_Encounters.md#context-protection), [`pull`](./Events_and_Encounters.md#context-pull), [`pull_it_out`](./Events_and_Encounters.md#context-pull_it_out), [`pull_lever`](./Events_and_Encounters.md#context-pull_lever), [`purify`](./Events_and_Encounters.md#context-purify), [`push_buttons`](./Events_and_Encounters.md#context-push_buttons), [`push_through`](./Events_and_Encounters.md#context-push_through), [`put_in_coins`](./Events_and_Encounters.md#context-put_in_coins), [`put_out_of_misery`](./Events_and_Encounters.md#context-put_out_of_misery), [`reach_inside`](./Events_and_Encounters.md#context-reach_inside), [`read`](./Events_and_Encounters.md#context-read), [`receive`](./Events_and_Encounters.md#context-receive), [`red`](./Events_and_Encounters.md#context-red), [`red_needle`](./Events_and_Encounters.md#context-red_needle), [`reflect`](./Events_and_Encounters.md#context-reflect), [`remove`](./Events_and_Encounters.md#context-remove), [`remove_the_nail`](./Events_and_Encounters.md#context-remove_the_nail), [`repair`](./Events_and_Encounters.md#context-repair), [`repair_quest`](./Events_and_Encounters.md#context-repair_quest), [`repell`](./Events_and_Encounters.md#context-repell), [`rest`](./Events_and_Encounters.md#context-rest), [`revive`](./Events_and_Encounters.md#context-revive), [`rub`](./Events_and_Encounters.md#context-rub), [`run`](./Events_and_Encounters.md#context-run), [`run_again`](./Events_and_Encounters.md#context-run_again), [`run_away`](./Events_and_Encounters.md#context-run_away), [`sacrifice`](./Events_and_Encounters.md#context-sacrifice), [`sacrifice_full_favor`](./Events_and_Encounters.md#context-sacrifice_full_favor), [`sacrifice_normal`](./Events_and_Encounters.md#context-sacrifice_normal), [`sacrifice_partial_favor`](./Events_and_Encounters.md#context-sacrifice_partial_favor), [`sacrifice_quest`](./Events_and_Encounters.md#context-sacrifice_quest), [`scale`](./Events_and_Encounters.md#context-scale), [`scream`](./Events_and_Encounters.md#context-scream), [`shake`](./Events_and_Encounters.md#context-shake), [`slip_through`](./Events_and_Encounters.md#context-slip_through), [`smash`](./Events_and_Encounters.md#context-smash), [`sneak`](./Events_and_Encounters.md#context-sneak), [`sneak_by`](./Events_and_Encounters.md#context-sneak_by), [`sneak_past_alt`](./Events_and_Encounters.md#context-sneak_past_alt), [`speed`](./Events_and_Encounters.md#context-speed), [`surprise`](./Events_and_Encounters.md#context-surprise), [`sweet_talk`](./Events_and_Encounters.md#context-sweet_talk), [`swim`](./Events_and_Encounters.md#context-swim), [`tail`](./Events_and_Encounters.md#context-tail), [`take`](./Events_and_Encounters.md#context-take), [`take_blood`](./Events_and_Encounters.md#context-take_blood), [`talk`](./Events_and_Encounters.md#context-talk), [`talk_to`](./Events_and_Encounters.md#context-talk_to), [`tappytoes`](./Events_and_Encounters.md#context-tappytoes), [`teleport`](./Events_and_Encounters.md#context-teleport), [`thorns`](./Events_and_Encounters.md#context-thorns), [`throw`](./Events_and_Encounters.md#context-throw), [`timemachine`](./Events_and_Encounters.md#context-timemachine), [`touch`](./Events_and_Encounters.md#context-touch), [`traverse`](./Events_and_Encounters.md#context-traverse), [`turnon`](./Events_and_Encounters.md#context-turnon), [`upgrade_yourself`](./Events_and_Encounters.md#context-upgrade_yourself), [`use_item`](./Events_and_Encounters.md#context-use_item), [`use_toilet_con`](./Events_and_Encounters.md#context-use_toilet_con), [`use_toilet_str`](./Events_and_Encounters.md#context-use_toilet_str), [`use_weapon`](./Events_and_Encounters.md#context-use_weapon), [`w1`](./Events_and_Encounters.md#context-w1), [`w2`](./Events_and_Encounters.md#context-w2), [`w3`](./Events_and_Encounters.md#context-w3), [`w4`](./Events_and_Encounters.md#context-w4), [`w5`](./Events_and_Encounters.md#context-w5), [`w6`](./Events_and_Encounters.md#context-w6), [`wealth`](./Events_and_Encounters.md#context-wealth), [`wish_genes`](./Events_and_Encounters.md#context-wish_genes), [`wish_items`](./Events_and_Encounters.md#context-wish_items), [`wish_levelups`](./Events_and_Encounters.md#context-wish_levelups), [`wish_strength`](./Events_and_Encounters.md#context-wish_strength), [`withstand`](./Events_and_Encounters.md#context-withstand), [`yank_it_out`](./Events_and_Encounters.md#context-yank_it_out), [`yellow_needle`](./Events_and_Encounters.md#context-yellow_needle)

> **Engine Schema:** This block is a `[event_node]` container. [View all confirmed values in Engine_Events.md](./Engine_Events.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[event_node]`](./Engine_Events.md#all-confirmed-event-node-values) | Block | An event outcome node. See Engine_Events.md for the full schema. |
| [`reward`](./Events_and_Encounters.md#context-reward) | Block | Event Node: Story branch or dialog option representing the 'Reward' action. | 326 |
| `set_frame` | Number |  | 285 |
| [`prompt`](./Strings.md#string-prompt) | String |  | 185 |
| [`play_animation`](./Enums.md#enum-play_animation) | Enum |  | 111 |
| [`increment_legacy_counter`](./Enums.md#enum-increment_legacy_counter) | Enum |  | 52 |
| [`conditional_reward`](./Events_and_Encounters.md#context-conditional_reward) | Block | Event Action: Provides a reward only if a specific condition is met. | 38 |
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum |  | 26 |
| [`cutscene`](./Strings.md#string-cutscene) | String | Event Node: Triggers a narrative cutscene. | 19 |
| [`begin_chapter`](./Enums.md#enum-begin_chapter) | Enum |  | 12 |
| [`complete_item_quest`](./Enums.md#enum-complete_item_quest) | Enum |  | 12 |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. | 12 |
| [`set_adventure_token`](./Enums.md#enum-set_adventure_token) | Enum |  | 12 |
| [`event_now`](./Enums.md#enum-event_now) | Enum |  | 9 |
| [`event_now_same_cat`](./Enums.md#enum-event_now_same_cat) | Enum |  | 9 |
| [`gain_disorder`](./Enums.md#enum-gain_disorder) | Enum |  | 8 |
| [`lose_specific_item`](./Enums.md#enum-lose_specific_item) | Enum |  | 8 |
| [`trigger_adventure_unlock`](./Enums.md#enum-trigger_adventure_unlock) | Enum |  | 7 |
| [`add_weather`](./Enums.md#enum-add_weather) | Enum |  | 6 |
| [`random_pool`](./Arrays.md#array-random_pool) | Array |  | 6 |
| [`get_item`](./Enums.md#enum-get_item) | Enum |  | 5 |
| [`get_item_from_pool`](./Enums.md#enum-get_item_from_pool) | Enum | Event Action: Rewards the player with an item drawn from a specific loot pool. | 5 |
| [`heal_disorder`](./Enums.md#enum-heal_disorder) | Enum |  | 5 |
| [`injury`](./Enums.md#enum-injury) | Enum |  | 4 |
| [`level_up`](./Enums.md#enum-level_up) | Enum |  | 4 |
| [`mutation`](./Events_and_Encounters.md#context-mutation) | Block | Event Node: Story branch or dialog option representing the 'Mutation' action. | 4 |
| [`random_pool_consider_luck`](./Arrays.md#array-random_pool_consider_luck) | Array |  | 4 |
| [`rare`](./Events_and_Encounters.md#context-rare) | Block | Event Node: Story branch or dialog option representing the 'Rare' action. | 4 |
| [`get_parasite`](./Enums.md#enum-get_parasite) | Enum |  | 3 |
| `heal_injury` | Number |  | 3 |
| [`kill`](./Enums.md#enum-kill) | Enum |  | 3 |
| [`transform_item`](./Arrays.md#array-transform_item) | Array |  | 3 |
| [`unlock_item_quest`](./Enums.md#enum-unlock_item_quest) | Enum |  | 3 |
| [`clear_surviving_kaiju`](./Enums.md#enum-clear_surviving_kaiju) | Enum |  | 2 |
| [`cutscene_on_exit`](./Enums.md#enum-cutscene_on_exit) | Enum |  | 2 |
| `full_heal` | Number |  | 2 |
| [`gain_disorder_from_pool`](./Enums.md#enum-gain_disorder_from_pool) | Enum |  | 2 |
| [`learn_ability_from_pool`](./Arrays.md#array-learn_ability_from_pool) | Array |  | 2 |
| [`learn_passive_from_pool`](./Enums.md#enum-learn_passive_from_pool) | Enum |  | 2 |
| [`override_end_option_prompt`](./Strings.md#string-override_end_option_prompt) | String |  | 2 |
| [`party_gain_disorder_from_pool`](./Arrays.md#array-party_gain_disorder_from_pool) | Array |  | 2 |
| `ally_ambush_next_fights` | Number |  | 1 |
| `clone_self_to_party` | Number |  | 1 |
| `copy_items_to_party` | Number |  | 1 |
| `copy_party_items` | Number |  | 1 |
| [`gain_clone_familiar`](./Events_and_Encounters.md#context-gain_clone_familiar) | Block | Event Action: Adds a clone of a character to the party as a familiar. | 1 |
| [`gain_food`](./Arrays.md#array-gain_food) | Array |  | 1 |
| [`get_full_item_set_from_pool`](./Enums.md#enum-get_full_item_set_from_pool) | Enum |  | 1 |
| [`global_effect_next_fight`](./Events_and_Encounters.md#context-global_effect_next_fight) | Block | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. | 1 |
| `heal` | Number |  | 1 |
| [`lose_item`](./Enums.md#enum-lose_item) | Enum |  | 1 |
| `next_event_bonus` | Number |  | 1 |
| [`next_event_from_set`](./Events_and_Encounters.md#context-next_event_from_set) | Block | Event Action: Chains immediately into a randomly selected subsequent story event. | 1 |
| [`scramble_abilities`](./Enums.md#enum-scramble_abilities) | Enum |  | 1 |
| [`scramble_passives`](./Enums.md#enum-scramble_passives) | Enum |  | 1 |
| [`shop_now`](./Enums.md#enum-shop_now) | Enum |  | 1 |
| `trigger_butterfly_effect` | Number |  | 1 |
| [`upgrade_ability`](./Enums.md#enum-upgrade_ability) | Enum |  | 1 |
| [`upgrade_passive`](./Enums.md#enum-upgrade_passive) | Enum |  | 1 |

</details>

---

### Context: `bad` (336 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`arm`](./Events_and_Encounters.md#context-arm), [`attack`](./Events_and_Encounters.md#context-attack), [`bash`](./Events_and_Encounters.md#context-bash), [`bash_past_alt`](./Events_and_Encounters.md#context-bash_past_alt), [`bite`](./Events_and_Encounters.md#context-bite), [`bite_it_off`](./Events_and_Encounters.md#context-bite_it_off), [`blue_needle`](./Events_and_Encounters.md#context-blue_needle), [`body`](./Events_and_Encounters.md#context-body), [`break_ice`](./Events_and_Encounters.md#context-break_ice), [`break_lock`](./Events_and_Encounters.md#context-break_lock), [`bribe`](./Events_and_Encounters.md#context-bribe), [`catch`](./Events_and_Encounters.md#context-catch), [`challenge_to_game`](./Events_and_Encounters.md#context-challenge_to_game), [`charm`](./Events_and_Encounters.md#context-charm), [`charm_past_alt`](./Events_and_Encounters.md#context-charm_past_alt), [`climb`](./Events_and_Encounters.md#context-climb), [`comfort`](./Events_and_Encounters.md#context-comfort), [`communicate`](./Events_and_Encounters.md#context-communicate), [`concheck`](./Events_and_Encounters.md#context-concheck), [`crack_open`](./Events_and_Encounters.md#context-crack_open), [`cross`](./Events_and_Encounters.md#context-cross), [`cut_wires`](./Events_and_Encounters.md#context-cut_wires), [`damage_1`](./Events_and_Encounters.md#context-damage_1), [`damage_full`](./Events_and_Encounters.md#context-damage_full), [`damage_half`](./Events_and_Encounters.md#context-damage_half), [`destroy`](./Events_and_Encounters.md#context-destroy), [`dexcheck`](./Events_and_Encounters.md#context-dexcheck), [`dig`](./Events_and_Encounters.md#context-dig), [`disarm`](./Events_and_Encounters.md#context-disarm), [`dive`](./Events_and_Encounters.md#context-dive), [`donate_10`](./Events_and_Encounters.md#context-donate_10), [`donate_15`](./Events_and_Encounters.md#context-donate_15), [`donate_20`](./Events_and_Encounters.md#context-donate_20), [`donate_5`](./Events_and_Encounters.md#context-donate_5), [`drink`](./Events_and_Encounters.md#context-drink), [`eat`](./Events_and_Encounters.md#context-eat), [`eat_meat`](./Events_and_Encounters.md#context-eat_meat), [`enter`](./Events_and_Encounters.md#context-enter), [`enter_crater`](./Events_and_Encounters.md#context-enter_crater), [`examine`](./Events_and_Encounters.md#context-examine), [`fight`](./Events_and_Encounters.md#context-fight), [`find_another_way`](./Events_and_Encounters.md#context-find_another_way), [`follow`](./Events_and_Encounters.md#context-follow), [`free`](./Events_and_Encounters.md#context-free), [`give_parasite`](./Events_and_Encounters.md#context-give_parasite), [`go_around`](./Events_and_Encounters.md#context-go_around), [`hack`](./Events_and_Encounters.md#context-hack), [`ignore`](./Events_and_Encounters.md#context-ignore), [`inspect`](./Events_and_Encounters.md#context-inspect), [`intcheck`](./Events_and_Encounters.md#context-intcheck), [`investigate`](./Events_and_Encounters.md#context-investigate), [`itchies`](./Events_and_Encounters.md#context-itchies), [`join`](./Events_and_Encounters.md#context-join), [`jump`](./Events_and_Encounters.md#context-jump), [`jump_over`](./Events_and_Encounters.md#context-jump_over), [`keep_going`](./Events_and_Encounters.md#context-keep_going), [`kiss`](./Events_and_Encounters.md#context-kiss), [`kiss_meat`](./Events_and_Encounters.md#context-kiss_meat), [`leave`](./Events_and_Encounters.md#context-leave), [`leave_it_in`](./Events_and_Encounters.md#context-leave_it_in), [`leg`](./Events_and_Encounters.md#context-leg), [`lever`](./Events_and_Encounters.md#context-lever), [`lick`](./Events_and_Encounters.md#context-lick), [`lick_alt`](./Events_and_Encounters.md#context-lick_alt), [`listen`](./Events_and_Encounters.md#context-listen), [`loot`](./Events_and_Encounters.md#context-loot), [`main`](./Events_and_Encounters.md#context-main), [`mind`](./Events_and_Encounters.md#context-mind), [`move_closer`](./Events_and_Encounters.md#context-move_closer), [`open`](./Events_and_Encounters.md#context-open), [`options`](./Events_and_Encounters.md#context-options), [`patch_up`](./Events_and_Encounters.md#context-patch_up), [`pick_lock`](./Events_and_Encounters.md#context-pick_lock), [`pilfer`](./Events_and_Encounters.md#context-pilfer), [`play`](./Events_and_Encounters.md#context-play), [`pull`](./Events_and_Encounters.md#context-pull), [`pull_it_out`](./Events_and_Encounters.md#context-pull_it_out), [`pull_lever`](./Events_and_Encounters.md#context-pull_lever), [`purify`](./Events_and_Encounters.md#context-purify), [`push_buttons`](./Events_and_Encounters.md#context-push_buttons), [`push_through`](./Events_and_Encounters.md#context-push_through), [`put_in_coins`](./Events_and_Encounters.md#context-put_in_coins), [`put_out_of_misery`](./Events_and_Encounters.md#context-put_out_of_misery), [`read`](./Events_and_Encounters.md#context-read), [`red`](./Events_and_Encounters.md#context-red), [`red_needle`](./Events_and_Encounters.md#context-red_needle), [`remove`](./Events_and_Encounters.md#context-remove), [`remove_the_nail`](./Events_and_Encounters.md#context-remove_the_nail), [`repair`](./Events_and_Encounters.md#context-repair), [`repell`](./Events_and_Encounters.md#context-repell), [`rest`](./Events_and_Encounters.md#context-rest), [`revive`](./Events_and_Encounters.md#context-revive), [`rub`](./Events_and_Encounters.md#context-rub), [`run`](./Events_and_Encounters.md#context-run), [`run_again`](./Events_and_Encounters.md#context-run_again), [`run_away`](./Events_and_Encounters.md#context-run_away), [`sacrifice`](./Events_and_Encounters.md#context-sacrifice), [`sacrifice_partial_favor`](./Events_and_Encounters.md#context-sacrifice_partial_favor), [`shake`](./Events_and_Encounters.md#context-shake), [`skip`](./Events_and_Encounters.md#context-skip), [`slip_through`](./Events_and_Encounters.md#context-slip_through), [`smash`](./Events_and_Encounters.md#context-smash), [`sneak`](./Events_and_Encounters.md#context-sneak), [`sneak_by`](./Events_and_Encounters.md#context-sneak_by), [`sneak_past_alt`](./Events_and_Encounters.md#context-sneak_past_alt), [`soul`](./Events_and_Encounters.md#context-soul), [`sweet_talk`](./Events_and_Encounters.md#context-sweet_talk), [`swim`](./Events_and_Encounters.md#context-swim), [`tail`](./Events_and_Encounters.md#context-tail), [`take`](./Events_and_Encounters.md#context-take), [`talk`](./Events_and_Encounters.md#context-talk), [`talk_to`](./Events_and_Encounters.md#context-talk_to), [`teleport`](./Events_and_Encounters.md#context-teleport), [`throw`](./Events_and_Encounters.md#context-throw), [`touch`](./Events_and_Encounters.md#context-touch), [`turnon`](./Events_and_Encounters.md#context-turnon), [`upgrade_yourself`](./Events_and_Encounters.md#context-upgrade_yourself), [`use_item`](./Events_and_Encounters.md#context-use_item), [`use_toilet_con`](./Events_and_Encounters.md#context-use_toilet_con), [`use_toilet_str`](./Events_and_Encounters.md#context-use_toilet_str), [`use_weapon`](./Events_and_Encounters.md#context-use_weapon), [`wheezies`](./Events_and_Encounters.md#context-wheezies), [`withstand`](./Events_and_Encounters.md#context-withstand), [`yank_it_out`](./Events_and_Encounters.md#context-yank_it_out), [`yellow_needle`](./Events_and_Encounters.md#context-yellow_needle)

> **Engine Schema:** This block is a `[event_node]` container. [View all confirmed values in Engine_Events.md](./Engine_Events.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[event_node]`](./Engine_Events.md#all-confirmed-event-node-values) | Block | An event outcome node. See Engine_Events.md for the full schema. |
| [`reward`](./Events_and_Encounters.md#context-reward) | Block | Event Node: Story branch or dialog option representing the 'Reward' action. | 303 |
| `set_frame` | Number |  | 219 |
| [`prompt`](./Strings.md#string-prompt) | String |  | 38 |
| [`play_animation`](./Enums.md#enum-play_animation) | Enum |  | 10 |
| [`conditional_reward`](./Events_and_Encounters.md#context-conditional_reward) | Block | Event Action: Provides a reward only if a specific condition is met. | 9 |
| [`injury`](./Math_Equations.md) | Equation |  | 8 |
| [`battle`](./Math_Equations.md) | Equation |  | 4 |
| [`gain_disorder_from_pool`](./Enums.md#enum-gain_disorder_from_pool) | Enum |  | 4 |
| [`kill`](./Enums.md#enum-kill) | Enum |  | 4 |
| [`self_status_next_fight`](./Events_and_Encounters.md#context-self_status_next_fight) | Block | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 4 |
| [`cutscene`](./Events_and_Encounters.md#context-cutscene) | Block | Event Node: Triggers a narrative cutscene. | 3 |
| [`event_now`](./Enums.md#enum-event_now) | Enum |  | 3 |
| [`event_now_same_cat`](./Enums.md#enum-event_now_same_cat) | Enum |  | 3 |
| [`get_parasite_from_pool`](./Enums.md#enum-get_parasite_from_pool) | Enum |  | 3 |
| `next_event_bonus` | Number |  | 2 |
| [`gain_immortal_familiar`](./Enums.md#enum-gain_immortal_familiar) | Enum |  | 1 |
| [`get_parasite`](./Enums.md#enum-get_parasite) | Enum |  | 1 |
| [`lose_item`](./Enums.md#enum-lose_item) | Enum |  | 1 |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#context-party_random_mutation_from_set) | Block | Event Reward: Applies a random mutation to the entire party from a specific pool. | 1 |
| [`permanent_stats`](./Events_and_Encounters.md#context-permanent_stats) | Block | Event Reward: Permanently increases (or decreases) the core stats of a single character. | 1 |
| [`select_item_from_pool_for_cutscene_only`](./Enums.md#enum-select_item_from_pool_for_cutscene_only) | Enum |  | 1 |
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum |  | 1 |

</details>

---

### Context: `intro` (214 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`cat_choice`](./Enums.md#enum-cat_choice) | Enum |  | 214 |
| [`event_clip`](./Enums.md#enum-event_clip) | Enum |  | 214 |
| [`subject_clip`](./Enums.md#enum-subject_clip) | Enum |  | 214 |
| [`subject_frame`](./Enums.md#enum-subject_frame) | Enum |  | 214 |
| [`title`](./Strings.md#string-title) | String |  | 214 |
| [`choose_cat_with_item`](./Enums.md#enum-choose_cat_with_item) | Enum |  | 17 |
| `different_from_last_x_cats` | Number |  | 3 |
| `subject_frame_inner` | Number |  | 3 |
| [`choose_cat_with_highest_stat`](./Math_Equations.md) | Equation |  | 1 |
| [`choose_cat_with_item_slot_equipped`](./Enums.md#enum-choose_cat_with_item_slot_equipped) | Enum |  | 1 |
| `choose_cat_with_min_health` | Number |  | 1 |
| `choose_cat_with_most_injuries` | Boolean |  | 1 |
| `choose_cat_with_parasite` | Boolean |  | 1 |
| `set_frame` | Number |  | 1 |

</details>

---

### Context: `main` (214 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root)

> **Engine Schema:** This block is a `[event_node]` container. [View all confirmed values in Engine_Events.md](./Engine_Events.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[event_node]`](./Engine_Events.md#all-confirmed-event-node-values) | Block | An event outcome node. See Engine_Events.md for the full schema. |
| [`options`](./Events_and_Encounters.md#context-options) | Block | Event Block: Lists the available clickable dialog choices for the current story node. | 210 |
| [`prompt`](./Strings.md#string-prompt) | String |  | 208 |
| [`setup`](./Events_and_Encounters.md#context-setup) | Block | Event Block: Pre-initialization logic executed before the event UI is drawn. | 23 |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 5 |
| [`goto`](./Enums.md#enum-goto) | Enum |  | 4 |
| [`outcome`](./Events_and_Encounters.md#context-outcome) | Block | Event Block: Logic and text executed after selecting a specific dialog option. | 4 |
| `max_options` | Number |  | 3 |
| `set_frame` | Number |  | 3 |
| `shuffle_options` | Boolean |  | 3 |
| [`weight`](./Enums.md#enum-weight) | Enum | Probability weight for this outcome. | 2 |
| [`add_weather`](./Enums.md#enum-add_weather) | Enum |  | 1 |
| [`gain_familiar`](./Enums.md#enum-gain_familiar) | Enum | Event Action: Adds a specific familiar to the party. | 1 |
| [`leave`](./Events_and_Encounters.md#context-leave) | Block | Event Node: Story branch or dialog option representing the 'Leave' action. | 1 |
| [`next_event_from_set`](./Enums.md#enum-next_event_from_set) | Enum | Event Action: Chains immediately into a randomly selected subsequent story event. | 1 |
| `party_heal` | Number |  | 1 |
| [`party_permanent_stats`](./Events_and_Encounters.md#context-party_permanent_stats) | Block | Event Reward: Permanently increases (or decreases) the core stats of all party members. | 1 |
| [`play_animation`](./Arrays.md#array-play_animation) | Array |  | 1 |
| [`rare`](./Events_and_Encounters.md#context-rare) | Block | Event Node: Story branch or dialog option representing the 'Rare' action. | 1 |
| [`requires_flag`](./Enums.md#enum-requires_flag) | Enum | Prerequisite: Must meet this condition. | 1 |
| [`self_damage`](./Arrays.md#array-self_damage) | Array | Recoil or self-inflicted damage/effects applied to the caster. | 1 |
| [`self_status_next_fight`](./Events_and_Encounters.md#context-self_status_next_fight) | Block | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 1 |
| [`shop_now`](./Enums.md#enum-shop_now) | Enum |  | 1 |

</details>

---

### Context: `options` (210 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`main`](./Events_and_Encounters.md#context-main)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ignore`](./Events_and_Encounters.md#context-ignore) | Block | Event Node: Story branch or dialog option representing the 'Ignore' action. | 55 |
| [`examine`](./Events_and_Encounters.md#context-examine) | Block | Event Node: Story branch or dialog option representing the 'Examine' action. | 43 |
| [`leave`](./Events_and_Encounters.md#context-leave) | Block | Event Node: Story branch or dialog option representing the 'Leave' action. | 29 |
| [`loot`](./Events_and_Encounters.md#context-loot) | Block | Event Node: Story branch or dialog option representing the 'Loot' action. | 25 |
| [`eat`](./Events_and_Encounters.md#context-eat) | Block | Event Node: Story branch or dialog option representing the 'Eat' action. | 23 |
| [`smash`](./Events_and_Encounters.md#context-smash) | Block | Event Node: Story branch or dialog option representing the 'Smash' action. | 15 |
| [`destroy`](./Events_and_Encounters.md#context-destroy) | Block | Event Node: Story branch or dialog option representing the 'Destroy' action. | 13 |
| [`bash`](./Events_and_Encounters.md#context-bash) | Block | Event Node: Story branch or dialog option representing the 'Bash' action. | 12 |
| [`sneak`](./Events_and_Encounters.md#context-sneak) | Block | Event Node: Story branch or dialog option representing the 'Sneak' action. | 11 |
| [`open`](./Events_and_Encounters.md#context-open) | Block | Event Node: Story branch or dialog option representing the 'Open' action. | 8 |
| [`take`](./Events_and_Encounters.md#context-take) | Block | Event Node: Story branch or dialog option representing the 'Take' action. | 8 |
| [`a`](./Events_and_Encounters.md#context-a) | Block | Event Node: Story branch or dialog option representing the 'A' action. | 7 |
| [`attack`](./Events_and_Encounters.md#context-attack) | Block | Event Node: Story branch or dialog option representing the 'Attack' action. | 7 |
| [`b`](./Events_and_Encounters.md#context-b) | Block | Event Node: Story branch or dialog option representing the 'B' action. | 7 |
| [`c`](./Events_and_Encounters.md#context-c) | Block | Event Node: Story branch or dialog option representing the 'C' action. | 7 |
| [`charm`](./Events_and_Encounters.md#context-charm) | Block | Event Node: Story branch or dialog option representing the 'Charm' action. | 7 |
| [`fight`](./Events_and_Encounters.md#context-fight) | Block | Event Node: Story branch or dialog option representing the 'Fight' action. | 7 |
| [`touch`](./Events_and_Encounters.md#context-touch) | Block | Event Node: Story branch or dialog option representing the 'Touch' action. | 7 |
| [`activate_p`](./Events_and_Encounters.md#context-activate_p) | Block | Event Node: Story branch or dialog option representing the 'Activate P' action. | 6 |
| [`activate_z`](./Events_and_Encounters.md#context-activate_z) | Block | Event Node: Story branch or dialog option representing the 'Activate Z' action. | 6 |
| [`d`](./Events_and_Encounters.md#context-d) | Block | Event Node: Story branch or dialog option representing the 'D' action. | 6 |
| [`enter`](./Events_and_Encounters.md#context-enter) | Block | Event Node: Story branch or dialog option representing the 'Enter' action. | 6 |
| [`inspect`](./Events_and_Encounters.md#context-inspect) | Block | Event Node: Story branch or dialog option representing the 'Inspect' action. | 6 |
| [`lick`](./Events_and_Encounters.md#context-lick) | Block | Event Node: Story branch or dialog option representing the 'Lick' action. | 6 |
| [`drink`](./Events_and_Encounters.md#context-drink) | Block | Event Node: Story branch or dialog option representing the 'Drink' action. | 5 |
| [`kiss`](./Events_and_Encounters.md#context-kiss) | Block | Event Node: Story branch or dialog option representing the 'Kiss' action. | 5 |
| [`run`](./Events_and_Encounters.md#context-run) | Block | Event Node: Story branch or dialog option representing the 'Run' action. | 5 |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 4 |
| [`bite`](./Events_and_Encounters.md#context-bite) | Block | Event Node: Story branch or dialog option representing the 'Bite' action. | 4 |
| [`damage`](./Events_and_Encounters.md#context-damage) | Block | Event Node: Story branch or dialog option representing the 'Damage' action. | 4 |
| [`go_around`](./Events_and_Encounters.md#context-go_around) | Block | Event Node: Story branch or dialog option representing the 'Go Around' action. | 4 |
| [`home`](./Events_and_Encounters.md#context-home) | Block | Event Node: Story branch or dialog option representing the 'Home' action. | 4 |
| [`past`](./Events_and_Encounters.md#context-past) | Block | Event Node: Story branch or dialog option representing the 'Past' action. | 4 |
| [`skip`](./Events_and_Encounters.md#context-skip) | Block | Event Node: Story branch or dialog option representing the 'Skip' action. | 4 |
| [`investigate`](./Events_and_Encounters.md#context-investigate) | Block | Event Node: Story branch or dialog option representing the 'Investigate' action. | 3 |
| [`rare`](./Events_and_Encounters.md#context-rare) | Block | Event Node: Story branch or dialog option representing the 'Rare' action. | 3 |
| [`repell`](./Events_and_Encounters.md#context-repell) | Block | Event Node: Story branch or dialog option representing the 'Repell' action. | 3 |
| [`attach_antenna`](./Events_and_Encounters.md#context-attach_antenna) | Block | Event Node: Story branch or dialog option representing the 'Attach Antenna' action. | 2 |
| [`boogers`](./Events_and_Encounters.md#context-boogers) | Block | Event Node: Story branch or dialog option representing the 'Boogers' action. | 2 |
| [`copy`](./Events_and_Encounters.md#context-copy) | Block | Event Node: Story branch or dialog option representing the 'Copy' action. | 2 |
| [`find_another_way`](./Events_and_Encounters.md#context-find_another_way) | Block | Event Node: Story branch or dialog option representing the 'Find Another Way' action. | 2 |
| [`get_item_from_pool`](./Enums.md#enum-get_item_from_pool) | Enum | Event Action: Rewards the player with an item drawn from a specific loot pool. | 2 |
| [`move_closer`](./Events_and_Encounters.md#context-move_closer) | Block | Event Node: Story branch or dialog option representing the 'Move Closer' action. | 2 |
| [`play`](./Events_and_Encounters.md#context-play) | Block | Event Node: Story branch or dialog option representing the 'Play' action. | 2 |
| [`poop`](./Events_and_Encounters.md#context-poop) | Block | Event Node: Story branch or dialog option representing the 'Poop' action. | 2 |
| [`print`](./Events_and_Encounters.md#context-print) | Block | Event Node: Story branch or dialog option representing the 'Print' action. | 2 |
| [`prompt`](./Strings.md#string-prompt) | String |  | 2 |
| [`protection`](./Events_and_Encounters.md#context-protection) | Block | Event Node: Story branch or dialog option representing the 'Protection' action. | 2 |
| [`repair`](./Events_and_Encounters.md#context-repair) | Block | Event Node: Story branch or dialog option representing the 'Repair' action. | 2 |
| [`sacrifice`](./Events_and_Encounters.md#context-sacrifice) | Block | Event Node: Story branch or dialog option representing the 'Sacrifice' action. | 2 |
| [`scale`](./Events_and_Encounters.md#context-scale) | Block | Event Node: Story branch or dialog option representing the 'Scale' action. | 2 |
| [`turnon`](./Events_and_Encounters.md#context-turnon) | Block | Event Node: Story branch or dialog option representing the 'Turnon' action. | 2 |
| [`5coins`](./Events_and_Encounters.md#context-5coins) | Block | Event Action: Grants or consumes 5 coins. | 1 |
| [`altar_sacrifice`](./Events_and_Encounters.md#context-altar_sacrifice) | Block | Event Action: Triggers the altar sacrifice progression logic. | 1 |
| [`arm`](./Events_and_Encounters.md#context-arm) | Block | Event Node: Story branch or dialog option representing the 'Arm' action. | 1 |
| [`attach_amplifier`](./Events_and_Encounters.md#context-attach_amplifier) | Block | Event Node: Story branch or dialog option representing the 'Attach Amplifier' action. | 1 |
| [`attach_leech`](./Events_and_Encounters.md#context-attach_leech) | Block | Event Node: Story branch or dialog option representing the 'Attach Leech' action. | 1 |
| [`bash_past_alt`](./Events_and_Encounters.md#context-bash_past_alt) | Block | Event Node: Story branch or dialog option representing the 'Bash Past Alt' action. | 1 |
| [`bite_it_off`](./Events_and_Encounters.md#context-bite_it_off) | Block | Event Node: Story branch or dialog option representing the 'Bite It Off' action. | 1 |
| [`blue`](./Events_and_Encounters.md#context-blue) | Block | Event Node: Story branch or dialog option representing the 'Blue' action. | 1 |
| [`blue_needle`](./Events_and_Encounters.md#context-blue_needle) | Block | Event Node: Story branch or dialog option representing the 'Blue Needle' action. | 1 |
| [`body`](./Events_and_Encounters.md#context-body) | Block | Event Node: Story branch or dialog option representing the 'Body' action. | 1 |
| [`book`](./Events_and_Encounters.md#context-book) | Block | Event Node: Story branch or dialog option representing the 'Book' action. | 1 |
| [`brace`](./Events_and_Encounters.md#context-brace) | Block | Event Node: Story branch or dialog option representing the 'Brace' action. | 1 |
| [`break_ice`](./Events_and_Encounters.md#context-break_ice) | Block | Event Node: Story branch or dialog option representing the 'Break Ice' action. | 1 |
| [`break_lock`](./Events_and_Encounters.md#context-break_lock) | Block | Event Node: Story branch or dialog option representing the 'Break Lock' action. | 1 |
| [`bribe`](./Events_and_Encounters.md#context-bribe) | Block | Event Node: Story branch or dialog option representing the 'Bribe' action. | 1 |
| [`button`](./Events_and_Encounters.md#context-button) | Block | Event Node: Story branch or dialog option representing the 'Button' action. | 1 |
| [`buy1`](./Events_and_Encounters.md#context-buy1) | Block | Event Node: Story branch or dialog option representing the 'Buy1' action. | 1 |
| [`catch`](./Events_and_Encounters.md#context-catch) | Block | Event Node: Story branch or dialog option representing the 'Catch' action. | 1 |
| [`challenge_to_game`](./Events_and_Encounters.md#context-challenge_to_game) | Block | Event Node: Story branch or dialog option representing the 'Challenge To Game' action. | 1 |
| [`chaos_ending`](./Events_and_Encounters.md#context-chaos_ending) | Block | Event Node: Triggers the Chaos Boss victory sequence. | 1 |
| [`chapter_cutscene`](./Events_and_Encounters.md#context-chapter_cutscene) | Block | Event Node: Triggers an intermission cutscene. | 1 |
| [`charm_past_alt`](./Events_and_Encounters.md#context-charm_past_alt) | Block | Event Node: Story branch or dialog option representing the 'Charm Past Alt' action. | 1 |
| [`climb`](./Events_and_Encounters.md#context-climb) | Block | Event Node: Story branch or dialog option representing the 'Climb' action. | 1 |
| [`comfort`](./Events_and_Encounters.md#context-comfort) | Block | Event Node: Story branch or dialog option representing the 'Comfort' action. | 1 |
| [`communicate`](./Events_and_Encounters.md#context-communicate) | Block | Event Node: Story branch or dialog option representing the 'Communicate' action. | 1 |
| [`concheck`](./Events_and_Encounters.md#context-concheck) | Block | Event Node: Stat check branch evaluating the 'con' attribute. | 1 |
| [`counter`](./Events_and_Encounters.md#context-counter) | Block | Event Node: Story branch or dialog option representing the 'Counter' action. | 1 |
| [`crack_open`](./Events_and_Encounters.md#context-crack_open) | Block | Event Node: Story branch or dialog option representing the 'Crack Open' action. | 1 |
| [`cross`](./Events_and_Encounters.md#context-cross) | Block | Event Node: Story branch or dialog option representing the 'Cross' action. | 1 |
| [`cut_wires`](./Events_and_Encounters.md#context-cut_wires) | Block | Event Node: Story branch or dialog option representing the 'Cut Wires' action. | 1 |
| [`damage_1`](./Events_and_Encounters.md#context-damage_1) | Block | Event Node: Story branch or dialog option representing the 'Damage 1' action. | 1 |
| [`damage_full`](./Events_and_Encounters.md#context-damage_full) | Block | Event Node: Story branch or dialog option representing the 'Damage Full' action. | 1 |
| [`damage_half`](./Events_and_Encounters.md#context-damage_half) | Block | Event Node: Story branch or dialog option representing the 'Damage Half' action. | 1 |
| [`desert_cutscene`](./Events_and_Encounters.md#context-desert_cutscene) | Block | Event Node: Triggers the desert transition cutscene. | 1 |
| [`dexcheck`](./Events_and_Encounters.md#context-dexcheck) | Block | Event Node: Stat check branch evaluating the 'dex' attribute. | 1 |
| [`dig`](./Events_and_Encounters.md#context-dig) | Block | Event Node: Story branch or dialog option representing the 'Dig' action. | 1 |
| [`disarm`](./Events_and_Encounters.md#context-disarm) | Block | Event Node: Story branch or dialog option representing the 'Disarm' action. | 1 |
| [`dive`](./Events_and_Encounters.md#context-dive) | Block | Event Node: Story branch or dialog option representing the 'Dive' action. | 1 |
| [`donate`](./Events_and_Encounters.md#context-donate) | Block | Event Node: Story branch or dialog option representing the 'Donate' action. | 1 |
| [`donate_10`](./Events_and_Encounters.md#context-donate_10) | Block | Event Node: Story branch or dialog option representing the 'Donate 10' action. | 1 |
| [`donate_15`](./Events_and_Encounters.md#context-donate_15) | Block | Event Node: Story branch or dialog option representing the 'Donate 15' action. | 1 |
| [`donate_20`](./Events_and_Encounters.md#context-donate_20) | Block | Event Node: Story branch or dialog option representing the 'Donate 20' action. | 1 |
| [`donate_5`](./Events_and_Encounters.md#context-donate_5) | Block | Event Node: Story branch or dialog option representing the 'Donate 5' action. | 1 |
| [`double`](./Events_and_Encounters.md#context-double) | Block | Event Node: Story branch or dialog option representing the 'Double' action. | 1 |
| [`eat_meat`](./Events_and_Encounters.md#context-eat_meat) | Block | Event Node: Story branch or dialog option representing the 'Eat Meat' action. | 1 |
| [`enter_crater`](./Events_and_Encounters.md#context-enter_crater) | Block | Event Node: Story branch or dialog option representing the 'Enter Crater' action. | 1 |
| [`face`](./Events_and_Encounters.md#context-face) | Block | Event Node: Story branch or dialog option representing the 'Face' action. | 1 |
| [`fiddle`](./Events_and_Encounters.md#context-fiddle) | Block | Event Node: Story branch or dialog option representing the 'Fiddle' action. | 1 |
| [`fill_jar`](./Events_and_Encounters.md#context-fill_jar) | Block | Event Node: Story branch or dialog option representing the 'Fill Jar' action. | 1 |
| [`find`](./Events_and_Encounters.md#context-find) | Block | Event Node: Story branch or dialog option representing the 'Find' action. | 1 |
| [`fire`](./Events_and_Encounters.md#context-fire) | Block | Event Node: Story branch or dialog option representing the 'Fire' action. | 1 |
| [`flush_yourself`](./Events_and_Encounters.md#context-flush_yourself) | Block | Event Node: Story branch or dialog option representing the 'Flush Yourself' action. | 1 |
| [`follow`](./Events_and_Encounters.md#context-follow) | Block | Event Node: Story branch or dialog option representing the 'Follow' action. | 1 |
| [`free`](./Events_and_Encounters.md#context-free) | Block | Event Node: Story branch or dialog option representing the 'Free' action. | 1 |
| [`future`](./Events_and_Encounters.md#context-future) | Block | Event Node: Story branch or dialog option representing the 'Future' action. | 1 |
| [`gain_familiar`](./Enums.md#enum-gain_familiar) | Enum | Event Action: Adds a specific familiar to the party. | 1 |
| [`give_parasite`](./Events_and_Encounters.md#context-give_parasite) | Block | Event Action: Equips a parasite item to a character. | 1 |
| [`hack`](./Events_and_Encounters.md#context-hack) | Block | Event Node: Story branch or dialog option representing the 'Hack' action. | 1 |
| [`head`](./Events_and_Encounters.md#context-head) | Block | Event Node: Story branch or dialog option representing the 'Head' action. | 1 |
| [`holy`](./Events_and_Encounters.md#context-holy) | Block | Event Node: Story branch or dialog option representing the 'Holy' action. | 1 |
| [`hp`](./Events_and_Encounters.md#context-hp) | Block | Event Node: Story branch or dialog option representing the 'Hp' action. | 1 |
| [`ice`](./Events_and_Encounters.md#context-ice) | Block | Event Node: Story branch or dialog option representing the 'Ice' action. | 1 |
| [`infinite`](./Events_and_Encounters.md#context-infinite) | Block | Event Node: A looping or endlessly repeating story branch. | 1 |
| [`intcheck`](./Events_and_Encounters.md#context-intcheck) | Block | Event Node: Stat check branch evaluating the 'int' attribute. | 1 |
| [`intimidation`](./Events_and_Encounters.md#context-intimidation) | Block | Event Node: Story branch or dialog option representing the 'Intimidation' action. | 1 |
| [`itchies`](./Events_and_Encounters.md#context-itchies) | Block | Event Node: Story branch or dialog option representing the 'Itchies' action. | 1 |
| [`join`](./Events_and_Encounters.md#context-join) | Block | Event Node: Story branch or dialog option representing the 'Join' action. | 1 |
| [`jump`](./Events_and_Encounters.md#context-jump) | Block | Event Node: Story branch or dialog option representing the 'Jump' action. | 1 |
| [`jump_over`](./Events_and_Encounters.md#context-jump_over) | Block | Event Node: Story branch or dialog option representing the 'Jump Over' action. | 1 |
| [`keep_going`](./Events_and_Encounters.md#context-keep_going) | Block | Event Node: Story branch or dialog option representing the 'Keep Going' action. | 1 |
| [`kiss_meat`](./Events_and_Encounters.md#context-kiss_meat) | Block | Event Node: Story branch or dialog option representing the 'Kiss Meat' action. | 1 |
| [`knife`](./Events_and_Encounters.md#context-knife) | Block | Event Node: Story branch or dialog option representing the 'Knife' action. | 1 |
| [`leave_it_in`](./Events_and_Encounters.md#context-leave_it_in) | Block | Event Node: Story branch or dialog option representing the 'Leave It In' action. | 1 |
| [`leg`](./Events_and_Encounters.md#context-leg) | Block | Event Node: Story branch or dialog option representing the 'Leg' action. | 1 |
| [`lever`](./Events_and_Encounters.md#context-lever) | Block | Event Node: Story branch or dialog option representing the 'Lever' action. | 1 |
| [`lick_alt`](./Events_and_Encounters.md#context-lick_alt) | Block | Event Node: Story branch or dialog option representing the 'Lick Alt' action. | 1 |
| [`lightning`](./Events_and_Encounters.md#context-lightning) | Block | Event Node: Story branch or dialog option representing the 'Lightning' action. | 1 |
| [`listen`](./Events_and_Encounters.md#context-listen) | Block | Event Node: Story branch or dialog option representing the 'Listen' action. | 1 |
| [`looks`](./Events_and_Encounters.md#context-looks) | Block | Event Node: Story branch or dialog option representing the 'Looks' action. | 1 |
| [`loot_heart`](./Events_and_Encounters.md#context-loot_heart) | Block | Event Node: Story branch or dialog option representing the 'Loot Heart' action. | 1 |
| [`makeup`](./Events_and_Encounters.md#context-makeup) | Block | Event Node: Story branch or dialog option representing the 'Makeup' action. | 1 |
| [`mind`](./Events_and_Encounters.md#context-mind) | Block | Event Node: Story branch or dialog option representing the 'Mind' action. | 1 |
| [`neck`](./Events_and_Encounters.md#context-neck) | Block | Event Node: Story branch or dialog option representing the 'Neck' action. | 1 |
| [`nothanks`](./Events_and_Encounters.md#context-nothanks) | Block | Event Node: Story branch or dialog option representing the 'Nothanks' action. | 1 |
| [`outsmart`](./Events_and_Encounters.md#context-outsmart) | Block | Event Node: Story branch or dialog option representing the 'Outsmart' action. | 1 |
| [`patch_up`](./Events_and_Encounters.md#context-patch_up) | Block | Event Node: Story branch or dialog option representing the 'Patch Up' action. | 1 |
| [`pick_lock`](./Events_and_Encounters.md#context-pick_lock) | Block | Event Node: Story branch or dialog option representing the 'Pick Lock' action. | 1 |
| [`pilfer`](./Events_and_Encounters.md#context-pilfer) | Block | Event Node: Story branch or dialog option representing the 'Pilfer' action. | 1 |
| [`pirouette`](./Events_and_Encounters.md#context-pirouette) | Block | Event Node: Story branch or dialog option representing the 'Pirouette' action. | 1 |
| [`place_gristle`](./Events_and_Encounters.md#context-place_gristle) | Block | Event Node: Story branch or dialog option representing the 'Place Gristle' action. | 1 |
| [`play_animation`](./Enums.md#enum-play_animation) | Enum |  | 1 |
| [`power`](./Events_and_Encounters.md#context-power) | Block | Event Node: Story branch or dialog option representing the 'Power' action. | 1 |
| [`pull`](./Events_and_Encounters.md#context-pull) | Block | Event Node: Story branch or dialog option representing the 'Pull' action. | 1 |
| [`pull_it_out`](./Events_and_Encounters.md#context-pull_it_out) | Block | Event Node: Story branch or dialog option representing the 'Pull It Out' action. | 1 |
| [`pull_lever`](./Events_and_Encounters.md#context-pull_lever) | Block | Event Node: Story branch or dialog option representing the 'Pull Lever' action. | 1 |
| [`purify`](./Events_and_Encounters.md#context-purify) | Block | Event Node: Story branch or dialog option representing the 'Purify' action. | 1 |
| [`push_buttons`](./Events_and_Encounters.md#context-push_buttons) | Block | Event Node: Story branch or dialog option representing the 'Push Buttons' action. | 1 |
| [`push_through`](./Events_and_Encounters.md#context-push_through) | Block | Event Node: Story branch or dialog option representing the 'Push Through' action. | 1 |
| [`put_in_coins`](./Events_and_Encounters.md#context-put_in_coins) | Block | Event Node: Story branch or dialog option representing the 'Put In Coins' action. | 1 |
| [`put_out_of_misery`](./Events_and_Encounters.md#context-put_out_of_misery) | Block | Event Node: Story branch or dialog option representing the 'Put Out Of Misery' action. | 1 |
| [`reach_inside`](./Events_and_Encounters.md#context-reach_inside) | Block | Event Node: Story branch or dialog option representing the 'Reach Inside' action. | 1 |
| [`read`](./Events_and_Encounters.md#context-read) | Block | Event Node: Story branch or dialog option representing the 'Read' action. | 1 |
| [`receive`](./Events_and_Encounters.md#context-receive) | Block | Event Node: Story branch or dialog option representing the 'Receive' action. | 1 |
| [`red`](./Events_and_Encounters.md#context-red) | Block | Event Node: Story branch or dialog option representing the 'Red' action. | 1 |
| [`red_needle`](./Events_and_Encounters.md#context-red_needle) | Block | Event Node: Story branch or dialog option representing the 'Red Needle' action. | 1 |
| [`reflect`](./Events_and_Encounters.md#context-reflect) | Block | Event Node: Story branch or dialog option representing the 'Reflect' action. | 1 |
| [`remove`](./Events_and_Encounters.md#context-remove) | Block | Event Node: Story branch or dialog option representing the 'Remove' action. | 1 |
| [`remove_the_nail`](./Events_and_Encounters.md#context-remove_the_nail) | Block | Event Node: Story branch or dialog option representing the 'Remove The Nail' action. | 1 |
| [`repair_quest`](./Events_and_Encounters.md#context-repair_quest) | Block | Event Node: Story branch or dialog option representing the 'Repair Quest' action. | 1 |
| [`rest`](./Events_and_Encounters.md#context-rest) | Block | Event Node: Story branch or dialog option representing the 'Rest' action. | 1 |
| [`revive`](./Events_and_Encounters.md#context-revive) | Block | Event Node: Story branch or dialog option representing the 'Revive' action. | 1 |
| [`rub`](./Events_and_Encounters.md#context-rub) | Block | Event Node: Story branch or dialog option representing the 'Rub' action. | 1 |
| [`run_again`](./Events_and_Encounters.md#context-run_again) | Block | Event Node: Story branch or dialog option representing the 'Run Again' action. | 1 |
| [`run_away`](./Events_and_Encounters.md#context-run_away) | Block | Event Node: Story branch or dialog option representing the 'Run Away' action. | 1 |
| [`sacrifice_full_favor`](./Events_and_Encounters.md#context-sacrifice_full_favor) | Block | Event Node: Story branch or dialog option representing the 'Sacrifice Full Favor' action. | 1 |
| [`sacrifice_normal`](./Events_and_Encounters.md#context-sacrifice_normal) | Block | Event Node: Story branch or dialog option representing the 'Sacrifice Normal' action. | 1 |
| [`sacrifice_partial_favor`](./Events_and_Encounters.md#context-sacrifice_partial_favor) | Block | Event Node: Story branch or dialog option representing the 'Sacrifice Partial Favor' action. | 1 |
| [`sacrifice_quest`](./Events_and_Encounters.md#context-sacrifice_quest) | Block | Event Node: Story branch or dialog option representing the 'Sacrifice Quest' action. | 1 |
| [`scream`](./Events_and_Encounters.md#context-scream) | Block | Event Node: Story branch or dialog option representing the 'Scream' action. | 1 |
| [`shake`](./Events_and_Encounters.md#context-shake) | Block | Event Node: Story branch or dialog option representing the 'Shake' action. | 1 |
| [`slip_through`](./Events_and_Encounters.md#context-slip_through) | Block | Event Node: Story branch or dialog option representing the 'Slip Through' action. | 1 |
| [`sneak_by`](./Events_and_Encounters.md#context-sneak_by) | Block | Event Node: Story branch or dialog option representing the 'Sneak By' action. | 1 |
| [`sneak_past_alt`](./Events_and_Encounters.md#context-sneak_past_alt) | Block | Event Node: Story branch or dialog option representing the 'Sneak Past Alt' action. | 1 |
| [`soul`](./Events_and_Encounters.md#context-soul) | Block | Event Node: Story branch or dialog option representing the 'Soul' action. | 1 |
| [`speed`](./Events_and_Encounters.md#context-speed) | Block | Event Node: Story branch or dialog option representing the 'Speed' action. | 1 |
| [`surprise`](./Events_and_Encounters.md#context-surprise) | Block | Event Node: Story branch or dialog option representing the 'Surprise' action. | 1 |
| [`sweet_talk`](./Events_and_Encounters.md#context-sweet_talk) | Block | Event Node: Story branch or dialog option representing the 'Sweet Talk' action. | 1 |
| [`swim`](./Events_and_Encounters.md#context-swim) | Block | Event Node: Story branch or dialog option representing the 'Swim' action. | 1 |
| [`tail`](./Events_and_Encounters.md#context-tail) | Block | Event Node: Story branch or dialog option representing the 'Tail' action. | 1 |
| [`take_blood`](./Events_and_Encounters.md#context-take_blood) | Block | Event Node: Story branch or dialog option representing the 'Take Blood' action. | 1 |
| [`talk`](./Events_and_Encounters.md#context-talk) | Block | Event Node: Story branch or dialog option representing the 'Talk' action. | 1 |
| [`talk_to`](./Events_and_Encounters.md#context-talk_to) | Block | Event Node: Story branch or dialog option representing the 'Talk To' action. | 1 |
| [`tappytoes`](./Events_and_Encounters.md#context-tappytoes) | Block | Event Node: Story branch or dialog option representing the 'Tappytoes' action. | 1 |
| [`teleport`](./Events_and_Encounters.md#context-teleport) | Block | Event Node: Story branch or dialog option representing the 'Teleport' action. | 1 |
| [`thorns`](./Events_and_Encounters.md#context-thorns) | Block | Event Node: Story branch or dialog option representing the 'Thorns' action. | 1 |
| [`throw`](./Events_and_Encounters.md#context-throw) | Block | Event Node: Story branch or dialog option representing the 'Throw' action. | 1 |
| [`timemachine`](./Events_and_Encounters.md#context-timemachine) | Block | Event Node: Story branch or dialog option representing the 'Timemachine' action. | 1 |
| [`traverse`](./Events_and_Encounters.md#context-traverse) | Block | Event Node: Story branch or dialog option representing the 'Traverse' action. | 1 |
| [`upgrade_yourself`](./Events_and_Encounters.md#context-upgrade_yourself) | Block | Event Reward: Upgrades an existing ability or item. | 1 |
| [`use_item`](./Events_and_Encounters.md#context-use_item) | Block | Event Requirement: Requires the player to consume a specific item to proceed. | 1 |
| [`use_toilet_con`](./Events_and_Encounters.md#context-use_toilet_con) | Block | Event Node: Story branch or dialog option representing the 'Use Toilet Con' action. | 1 |
| [`use_toilet_str`](./Events_and_Encounters.md#context-use_toilet_str) | Block | Event Node: Story branch or dialog option representing the 'Use Toilet Str' action. | 1 |
| [`use_weapon`](./Events_and_Encounters.md#context-use_weapon) | Block | Event Requirement: Uses the properties of the equipped weapon to resolve an outcome. | 1 |
| [`w1`](./Events_and_Encounters.md#context-w1) | Block | Event Node: Story branch or dialog option representing the 'W1' action. | 1 |
| [`w2`](./Events_and_Encounters.md#context-w2) | Block | Event Node: Story branch or dialog option representing the 'W2' action. | 1 |
| [`w3`](./Events_and_Encounters.md#context-w3) | Block | Event Node: Story branch or dialog option representing the 'W3' action. | 1 |
| [`w4`](./Events_and_Encounters.md#context-w4) | Block | Event Node: Story branch or dialog option representing the 'W4' action. | 1 |
| [`w5`](./Events_and_Encounters.md#context-w5) | Block | Event Node: Story branch or dialog option representing the 'W5' action. | 1 |
| [`w6`](./Events_and_Encounters.md#context-w6) | Block | Event Node: Story branch or dialog option representing the 'W6' action. | 1 |
| [`wealth`](./Events_and_Encounters.md#context-wealth) | Block | Event Node: Story branch or dialog option representing the 'Wealth' action. | 1 |
| [`weight`](./Enums.md#enum-weight) | Enum | Probability weight for this outcome. | 1 |
| [`wheezies`](./Events_and_Encounters.md#context-wheezies) | Block | Event Node: Story branch or dialog option representing the 'Wheezies' action. | 1 |
| [`wish_genes`](./Events_and_Encounters.md#context-wish_genes) | Block | Event Node: Story branch or dialog option representing the 'Wish Genes' action. | 1 |
| [`wish_items`](./Events_and_Encounters.md#context-wish_items) | Block | Event Node: Story branch or dialog option representing the 'Wish Items' action. | 1 |
| [`wish_levelups`](./Events_and_Encounters.md#context-wish_levelups) | Block | Event Node: Story branch or dialog option representing the 'Wish Levelups' action. | 1 |
| [`wish_strength`](./Events_and_Encounters.md#context-wish_strength) | Block | Event Node: Story branch or dialog option representing the 'Wish Strength' action. | 1 |
| [`withstand`](./Events_and_Encounters.md#context-withstand) | Block | Event Node: Story branch or dialog option representing the 'Withstand' action. | 1 |
| [`yank_it_out`](./Events_and_Encounters.md#context-yank_it_out) | Block | Event Node: Story branch or dialog option representing the 'Yank It Out' action. | 1 |
| [`yellow_needle`](./Events_and_Encounters.md#context-yellow_needle) | Block | Event Node: Story branch or dialog option representing the 'Yellow Needle' action. | 1 |

</details>

---

### Context: `requirements` (203 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`activate_p`](./Events_and_Encounters.md#context-activate_p), [`activate_z`](./Events_and_Encounters.md#context-activate_z), [`attach_amplifier`](./Events_and_Encounters.md#context-attach_amplifier), [`attach_antenna`](./Events_and_Encounters.md#context-attach_antenna), [`attach_leech`](./Events_and_Encounters.md#context-attach_leech), [`bash`](./Events_and_Encounters.md#context-bash), [`bash_past_alt`](./Events_and_Encounters.md#context-bash_past_alt), [`blue_needle`](./Events_and_Encounters.md#context-blue_needle), [`charm`](./Events_and_Encounters.md#context-charm), [`charm_past_alt`](./Events_and_Encounters.md#context-charm_past_alt), [`conditional_reward`](./Events_and_Encounters.md#context-conditional_reward), [`dig`](./Events_and_Encounters.md#context-dig), [`donate_10`](./Events_and_Encounters.md#context-donate_10), [`donate_15`](./Events_and_Encounters.md#context-donate_15), [`donate_20`](./Events_and_Encounters.md#context-donate_20), [`donate_5`](./Events_and_Encounters.md#context-donate_5), [`fiddle`](./Events_and_Encounters.md#context-fiddle), [`fight`](./Events_and_Encounters.md#context-fight), [`fill_jar`](./Events_and_Encounters.md#context-fill_jar), [`flush_yourself`](./Events_and_Encounters.md#context-flush_yourself), [`future`](./Events_and_Encounters.md#context-future), [`give_parasite`](./Events_and_Encounters.md#context-give_parasite), [`ignore`](./Events_and_Encounters.md#context-ignore), [`infinite`](./Events_and_Encounters.md#context-infinite), [`lick`](./Events_and_Encounters.md#context-lick), [`lick_alt`](./Events_and_Encounters.md#context-lick_alt), [`loot`](./Events_and_Encounters.md#context-loot), [`loot_heart`](./Events_and_Encounters.md#context-loot_heart), [`past`](./Events_and_Encounters.md#context-past), [`place_gristle`](./Events_and_Encounters.md#context-place_gristle), [`receive`](./Events_and_Encounters.md#context-receive), [`red_needle`](./Events_and_Encounters.md#context-red_needle), [`repair`](./Events_and_Encounters.md#context-repair), [`repair_quest`](./Events_and_Encounters.md#context-repair_quest), [`run`](./Events_and_Encounters.md#context-run), [`run_again`](./Events_and_Encounters.md#context-run_again), [`sacrifice`](./Events_and_Encounters.md#context-sacrifice), [`sacrifice_full_favor`](./Events_and_Encounters.md#context-sacrifice_full_favor), [`sacrifice_normal`](./Events_and_Encounters.md#context-sacrifice_normal), [`sacrifice_partial_favor`](./Events_and_Encounters.md#context-sacrifice_partial_favor), [`sacrifice_quest`](./Events_and_Encounters.md#context-sacrifice_quest), [`sneak`](./Events_and_Encounters.md#context-sneak), [`sneak_past_alt`](./Events_and_Encounters.md#context-sneak_past_alt), [`take_blood`](./Events_and_Encounters.md#context-take_blood), [`use_weapon`](./Events_and_Encounters.md#context-use_weapon), [`wish_genes`](./Events_and_Encounters.md#context-wish_genes), [`wish_items`](./Events_and_Encounters.md#context-wish_items), [`wish_levelups`](./Events_and_Encounters.md#context-wish_levelups), [`wish_strength`](./Events_and_Encounters.md#context-wish_strength), [`yellow_needle`](./Events_and_Encounters.md#context-yellow_needle)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`has_token`](./Enums.md#enum-has_token) | Enum |  | 80 |
| [`counter_range`](./Arrays.md#array-counter_range) | Array |  | 37 |
| [`not_has_token`](./Enums.md#enum-not_has_token) | Enum |  | 30 |
| [`counter_minimum`](./Arrays.md#array-counter_minimum) | Array |  | 25 |
| [`cat_has_item_equipped`](./Enums.md#enum-cat_has_item_equipped) | Enum |  | 22 |
| [`counter_maximum`](./Arrays.md#array-counter_maximum) | Array |  | 18 |
| [`is_not_chapter`](./Arrays.md#array-is_not_chapter) | Array |  | 16 |
| [`is_chapter`](./Arrays.md#array-is_chapter) | Array |  | 8 |
| `minimum_party_size` | Number |  | 2 |
| [`not_cat_has_item_equipped`](./Enums.md#enum-not_cat_has_item_equipped) | Enum |  | 2 |
| `not_on_quest` | Number |  | 2 |
| `cat_has_injury_count_min` | Number |  | 1 |
| [`cat_has_item_slot_equipped`](./Enums.md#enum-cat_has_item_slot_equipped) | Enum |  | 1 |
| `cat_has_parasite` | Boolean |  | 1 |

</details>

---

### Context: `self_status_next_fight` (141 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`bad`](./Events_and_Encounters.md#context-bad), [`buy1`](./Events_and_Encounters.md#context-buy1), [`common`](./Events_and_Encounters.md#context-common), [`else`](./Events_and_Encounters.md#context-else), [`main`](./Events_and_Encounters.md#context-main), [`rare`](./Events_and_Encounters.md#context-rare)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `permanent_stats` (126 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bad`](./Events_and_Encounters.md#context-bad), [`common`](./Events_and_Encounters.md#context-common), [`rare`](./Events_and_Encounters.md#context-rare)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 35 |
| `random` | Number |  | 25 |
| `int` | Number |  | 21 |
| `lck` | Number |  | 18 |
| `spd` | Number |  | 18 |
| `str` | Number |  | 16 |
| `cha` | Number |  | 14 |
| `dex` | Number |  | 9 |

</details>

---

### Context: `conditional_reward` (124 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bad`](./Events_and_Encounters.md#context-bad), [`common`](./Events_and_Encounters.md#context-common), [`else`](./Events_and_Encounters.md#context-else), [`good`](./Events_and_Encounters.md#context-good), [`rare`](./Events_and_Encounters.md#context-rare), [`setup`](./Events_and_Encounters.md#context-setup)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 124 |
| [`reward`](./Events_and_Encounters.md#context-reward) | Block | Event Node: Story branch or dialog option representing the 'Reward' action. | 124 |
| [`else`](./Events_and_Encounters.md#context-else) | Block | Event Node: Story branch or dialog option representing the 'Else' action. | 37 |
| [`prompt`](./Strings.md#string-prompt) | String |  | 2 |

</details>

---

### Context: `ignore` (57 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 57 |
| [`label`](./Strings.md#string-label) | String |  | 57 |
| [`stat`](./Math_Equations.md) | Equation |  | 56 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 55 |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 4 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 3 |
| [`hint_chapter_exit`](./Enums.md#enum-hint_chapter_exit) | Enum |  | 2 |

</details>

---

### Context: `examine` (43 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`label`](./Strings.md#string-label) | String |  | 43 |
| [`stat`](./Math_Equations.md) | Equation |  | 43 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 41 |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 32 |
| [`copy_results`](./Enums.md#enum-copy_results) | Enum |  | 2 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`gain_coins`](./Arrays.md#array-gain_coins) | Array |  | 1 |

</details>

---

### Context: `get_item_from_pool` (40 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Enum |  | 40 |
| [`restrict`](./Arrays.md#array-restrict) | Array |  | 30 |
| [`prompt`](./Strings.md#string-prompt) | String |  | 1 |

</details>

---

### Context: `spawn_unit_next_fight` (40 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`rare`](./Events_and_Encounters.md#context-rare), [`reward`](./Events_and_Encounters.md#context-reward)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array |  | 40 |
| `count` | Number | Quantity. | 34 |
| [`spawn_side`](./Enums.md#enum-spawn_side) | Enum |  | 31 |
| [`side`](./Enums.md#enum-side) | Enum |  | 3 |

</details>

---

### Context: `else` (37 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`conditional_reward`](./Events_and_Encounters.md#context-conditional_reward)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prompt`](./Strings.md#string-prompt) | String |  | 19 |
| [`event_now_same_cat`](./Enums.md#enum-event_now_same_cat) | Enum |  | 6 |
| [`set_adventure_token`](./Enums.md#enum-set_adventure_token) | Enum |  | 6 |
| `party_damage` | Number |  | 5 |
| `set_frame` | Number |  | 5 |
| [`conditional_reward`](./Events_and_Encounters.md#context-conditional_reward) | Block | Event Action: Provides a reward only if a specific condition is met. | 4 |
| [`event_now`](./Enums.md#enum-event_now) | Enum |  | 4 |
| [`random_pool`](./Arrays.md#array-random_pool) | Array |  | 3 |
| [`gain_disorder`](./Enums.md#enum-gain_disorder) | Enum |  | 2 |
| [`get_item_from_pool`](./Arrays.md#array-get_item_from_pool) | Array | Event Action: Rewards the player with an item drawn from a specific loot pool. | 2 |
| `damage` | Number | Event Node: Story branch or dialog option representing the 'Damage' action. | 1 |
| `next_event_bonus` | Number |  | 1 |
| [`random_mutation`](./Events_and_Encounters.md#context-random_mutation) | Block | Event Reward: Applies a completely random mutation to a character. | 1 |
| [`self_status_next_fight`](./Events_and_Encounters.md#context-self_status_next_fight) | Block | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 1 |
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum |  | 1 |

</details>

---

### Context: `leave` (30 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`main`](./Events_and_Encounters.md#context-main), [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 30 |
| [`label`](./Strings.md#string-label) | String |  | 30 |
| [`stat`](./Math_Equations.md) | Equation |  | 30 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 28 |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 3 |

</details>

---

### Context: `loot` (25 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 25 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 25 |
| [`label`](./Strings.md#string-label) | String |  | 25 |
| [`stat`](./Math_Equations.md) | Equation |  | 25 |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 23 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 2 |
| [`rare`](./Events_and_Encounters.md#context-rare) | Block | Event Node: Story branch or dialog option representing the 'Rare' action. | 1 |

</details>

---

### Context: `mutation` (24 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`good`](./Events_and_Encounters.md#context-good), [`rare`](./Events_and_Encounters.md#context-rare), [`spawn_reflection_next_fight`](./Events_and_Encounters.md#context-spawn_reflection_next_fight)

| Property Key | Type | Definition | Count |
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

### Context: `eat` (23 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 23 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 23 |
| [`label`](./Enums.md#enum-label) | Enum |  | 23 |
| [`stat`](./Math_Equations.md) | Equation |  | 23 |

</details>

---

### Context: `party_status_next_fight` (23 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`rare`](./Events_and_Encounters.md#context-rare)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `setup` (23 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`main`](./Events_and_Encounters.md#context-main)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`conditional_reward`](./Events_and_Encounters.md#context-conditional_reward) | Block | Event Action: Provides a reward only if a specific condition is met. | 42 |
| `set_frame` | Number |  | 3 |

</details>

---

### Context: `random_mutation_from_set` (21 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`rare`](./Events_and_Encounters.md#context-rare)

| Property Key | Type | Definition | Count |
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

### Context: `smash` (15 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`label`](./Strings.md#string-label) | String |  | 15 |
| [`stat`](./Math_Equations.md) | Equation |  | 15 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 14 |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 12 |
| [`copy_results`](./Enums.md#enum-copy_results) | Enum |  | 1 |

</details>

---

### Context: `destroy` (14 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 14 |
| [`label`](./Strings.md#string-label) | String |  | 14 |
| [`stat`](./Math_Equations.md) | Equation |  | 14 |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 13 |

</details>

---

### Context: `bash` (12 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 12 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 12 |
| [`label`](./Strings.md#string-label) | String |  | 12 |
| [`stat`](./Math_Equations.md) | Equation |  | 12 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |

</details>

---

### Context: `sneak` (11 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 11 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 11 |
| [`label`](./Strings.md#string-label) | String |  | 11 |
| [`stat`](./Math_Equations.md) | Equation |  | 11 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |

</details>

---

### Context: `global_effect_next_fight` (10 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`good`](./Events_and_Encounters.md#context-good), [`rare`](./Events_and_Encounters.md#context-rare)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Fights` | Number | Applies or references the 'Fights' effect/state. | 6 |
| [`CharacterTypeGainsStatusAtBattleStart`](./Events_and_Encounters.md#context-charactertypegainsstatusatbattlestart) | Block | Encounter Modifier: Applies a status effect to all characters of a specific type (e.g., Cats, Bosses) at the start of battle. | 5 |
| [`StatusRandomEnemiesOnBattleStart`](./Events_and_Encounters.md#context-statusrandomenemiesonbattlestart) | Block | Encounter Modifier: Applies a status effect to a random number of enemies at the start of battle. | 3 |
| [`KillEnemyOfTypeAtBattleStart`](./Events_and_Encounters.md#context-killenemyoftypeatbattlestart) | Block | Encounter Modifier: Instantly kills one enemy of the specified type at the start of battle. | 2 |

</details>

---

### Context: `open` (8 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`label`](./Strings.md#string-label) | String |  | 8 |
| [`stat`](./Math_Equations.md) | Equation |  | 8 |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 7 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 7 |
| [`copy_results`](./Enums.md#enum-copy_results) | Enum |  | 1 |

</details>

---

### Context: `take` (8 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 8 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 8 |
| [`label`](./Strings.md#string-label) | String |  | 8 |
| [`stat`](./Math_Equations.md) | Equation |  | 8 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |

</details>

---

### Context: `a` (7 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 7 |
| [`label`](./Strings.md#string-label) | String |  | 7 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 7 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 5 |

</details>

---

### Context: `attack` (7 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`label`](./Strings.md#string-label) | String |  | 7 |
| [`stat`](./Math_Equations.md) | Equation |  | 7 |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 6 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 6 |
| [`rare`](./Events_and_Encounters.md#context-rare) | Block | Event Node: Story branch or dialog option representing the 'Rare' action. | 1 |

</details>

---

### Context: `b` (7 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 7 |
| [`label`](./Strings.md#string-label) | String |  | 7 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 7 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 5 |

</details>

---

### Context: `c` (7 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 7 |
| [`label`](./Strings.md#string-label) | String |  | 7 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 7 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 5 |

</details>

---

### Context: `charm` (7 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 7 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 7 |
| [`label`](./Strings.md#string-label) | String |  | 7 |
| [`stat`](./Math_Equations.md) | Equation |  | 7 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |

</details>

---

### Context: `fight` (7 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 7 |
| [`label`](./Strings.md#string-label) | String |  | 7 |
| [`stat`](./Math_Equations.md) | Equation |  | 7 |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 6 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |

</details>

---

### Context: `leave_party_temporarily` (7 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`rare`](./Events_and_Encounters.md#context-rare)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `fights_skipped` | Number |  | 7 |
| [`return_as`](./Enums.md#enum-return_as) | Enum |  | 3 |
| [`return_during`](./Enums.md#enum-return_during) | Enum |  | 3 |

</details>

---

### Context: `touch` (7 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 7 |
| [`label`](./Strings.md#string-label) | String |  | 7 |
| [`stat`](./Math_Equations.md) | Equation |  | 7 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 6 |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 6 |

</details>

---

### Context: `activate_p` (6 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 6 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 6 |
| [`label`](./Enums.md#enum-label) | Enum |  | 6 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 6 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 6 |

</details>

---

### Context: `activate_z` (6 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 6 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 6 |
| [`label`](./Enums.md#enum-label) | Enum |  | 6 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 6 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 6 |

</details>

---

### Context: `d` (6 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 6 |
| [`label`](./Strings.md#string-label) | String |  | 6 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 6 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 5 |

</details>

---

### Context: `enter` (6 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 6 |
| [`label`](./Strings.md#string-label) | String |  | 6 |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 5 |
| [`stat`](./Math_Equations.md) | Equation |  | 5 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`hint_chapter_exit`](./Enums.md#enum-hint_chapter_exit) | Enum |  | 1 |

</details>

---

### Context: `inspect` (6 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 6 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 6 |
| [`label`](./Strings.md#string-label) | String |  | 6 |
| [`stat`](./Math_Equations.md) | Equation |  | 6 |

</details>

---

### Context: `lick` (6 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 6 |
| [`label`](./Strings.md#string-label) | String |  | 6 |
| [`stat`](./Math_Equations.md) | Equation |  | 6 |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 5 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |

</details>

---

### Context: `CharacterTypeGainsStatusAtBattleStart` (5 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`global_effect_next_fight`](./Events_and_Encounters.md#context-global_effect_next_fight)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |
| [`tag`](./Enums.md#enum-tag) | Enum | Specific entity tag required. | 5 |

</details>

---

### Context: `drink` (5 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 5 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 5 |
| [`label`](./Enums.md#enum-label) | Enum |  | 5 |
| [`stat`](./Math_Equations.md) | Equation |  | 5 |

</details>

---

### Context: `kiss` (5 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 5 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 5 |
| [`label`](./Strings.md#string-label) | String |  | 5 |
| [`stat`](./Math_Equations.md) | Equation |  | 5 |

</details>

---

### Context: `run` (5 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 5 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 5 |
| [`label`](./Strings.md#string-label) | String |  | 5 |
| [`stat`](./Math_Equations.md) | Equation |  | 5 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 2 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |

</details>

---

### Context: `bite` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 4 |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 4 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 4 |
| [`label`](./Enums.md#enum-label) | Enum |  | 4 |
| [`stat`](./Math_Equations.md) | Equation |  | 4 |

</details>

---

### Context: `damage` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 4 |
| [`label`](./Strings.md#string-label) | String |  | 4 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 3 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 3 |

</details>

---

### Context: `go_around` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 4 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 4 |
| [`label`](./Strings.md#string-label) | String |  | 4 |
| [`stat`](./Math_Equations.md) | Equation |  | 3 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 2 |

</details>

---

### Context: `home` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 4 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 4 |
| [`hint_chapter_exit`](./Enums.md#enum-hint_chapter_exit) | Enum |  | 4 |
| [`label`](./Enums.md#enum-label) | Enum |  | 4 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 4 |

</details>

---

### Context: `outcome` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`main`](./Events_and_Encounters.md#context-main)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`play_animation`](./Arrays.md#array-play_animation) | Array |  | 4 |
| [`random_pool`](./Arrays.md#array-random_pool) | Array |  | 3 |
| [`add_weather`](./Enums.md#enum-add_weather) | Enum |  | 1 |
| [`weather_roll`](./Arrays.md#array-weather_roll) | Array |  | 1 |

</details>

---

### Context: `party_permanent_stats_exclude_self` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`rare`](./Events_and_Encounters.md#context-rare)

| Property Key | Type | Definition | Count |
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

### Context: `past` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 4 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 4 |
| [`hint_chapter_exit`](./Enums.md#enum-hint_chapter_exit) | Enum |  | 4 |
| [`label`](./Enums.md#enum-label) | Enum |  | 4 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 4 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 4 |

</details>

---

### Context: `skip` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 4 |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 4 |
| [`label`](./Strings.md#string-label) | String |  | 4 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 4 |

</details>

---

### Context: `StatusRandomEnemiesOnBattleStart` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`global_effect_next_fight`](./Events_and_Encounters.md#context-global_effect_next_fight)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |
| `count` | Number | Quantity. | 3 |

</details>

---

### Context: `cutscene` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bad`](./Events_and_Encounters.md#context-bad)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`cutscene`](./Strings.md#string-cutscene) | String | Event Node: Triggers a narrative cutscene. | 21 |
| `skip_result_screen` | Boolean |  | 21 |

</details>

---

### Context: `investigate` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 3 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 3 |
| [`label`](./Strings.md#string-label) | String |  | 3 |
| [`stat`](./Math_Equations.md) | Equation |  | 3 |

</details>

---

### Context: `next_event_from_set` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`good`](./Events_and_Encounters.md#context-good)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`event`](./Enums.md#enum-event) | Enum |  | 5 |
| `same_cat` | Boolean |  | 5 |
| `count` | Number | Quantity. | 4 |

</details>

---

### Context: `repell` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 3 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 3 |
| [`label`](./Strings.md#string-label) | String |  | 3 |
| [`stat`](./Math_Equations.md) | Equation |  | 3 |

</details>

---

### Context: `KillEnemyOfTypeAtBattleStart` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`global_effect_next_fight`](./Events_and_Encounters.md#context-global_effect_next_fight)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`enemy_type`](./Enums.md#enum-enemy_type) | Enum |  | 2 |
| [`fallback_spawn`](./Arrays.md#array-fallback_spawn) | Array |  | 1 |

</details>

---

### Context: `attach_antenna` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 2 |
| [`label`](./Enums.md#enum-label) | Enum |  | 2 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 2 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 2 |

</details>

---

### Context: `boogers` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 2 |
| [`label`](./Strings.md#string-label) | String |  | 2 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 2 |

</details>

---

### Context: `copy` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 2 |
| [`label`](./Strings.md#string-label) | String |  | 2 |

</details>

---

### Context: `find_another_way` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 2 |
| [`label`](./Strings.md#string-label) | String |  | 2 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `move_closer` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 2 |
| [`label`](./Strings.md#string-label) | String |  | 2 |
| [`stat`](./Math_Equations.md) | Equation |  | 2 |

</details>

---

### Context: `party_permanent_stats` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`main`](./Events_and_Encounters.md#context-main), [`rare`](./Events_and_Encounters.md#context-rare)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 2 |

</details>

---

### Context: `party_random_mutation_from_set` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bad`](./Events_and_Encounters.md#context-bad), [`rare`](./Events_and_Encounters.md#context-rare)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `count` | Number | Quantity. | 2 |
| `ears` | Number |  | 2 |
| `eyebrows` | Number |  | 2 |
| `eyes` | Number |  | 2 |
| `mouth` | Number |  | 2 |

</details>

---

### Context: `play` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 2 |
| [`label`](./Strings.md#string-label) | String |  | 2 |
| [`stat`](./Math_Equations.md) | Equation |  | 2 |

</details>

---

### Context: `poop` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 2 |
| [`label`](./Strings.md#string-label) | String |  | 2 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 2 |

</details>

---

### Context: `print` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 2 |
| [`label`](./Strings.md#string-label) | String |  | 2 |

</details>

---

### Context: `protection` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 2 |
| [`label`](./Strings.md#string-label) | String |  | 2 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 2 |

</details>

---

### Context: `repair` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 2 |
| [`label`](./Strings.md#string-label) | String |  | 2 |
| [`stat`](./Math_Equations.md) | Equation |  | 2 |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |

</details>

---

### Context: `sacrifice` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 2 |
| [`label`](./Strings.md#string-label) | String |  | 2 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `scale` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 2 |
| [`label`](./Strings.md#string-label) | String |  | 2 |

</details>

---

### Context: `turnon` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 2 |
| [`label`](./Strings.md#string-label) | String |  | 2 |
| [`stat`](./Math_Equations.md) | Equation |  | 2 |

</details>

---

### Context: `10coins` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum |  | 1 |
| [`get_item_from_pool`](./Enums.md#enum-get_item_from_pool) | Enum | Event Action: Rewards the player with an item drawn from a specific loot pool. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`prompt`](./Strings.md#string-prompt) | String |  | 1 |
| `set_frame` | Number |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| `stat_max` | Number |  | 1 |
| `stat_min` | Number |  | 1 |
| `weight` | Number | Probability weight for this outcome. | 1 |

</details>

---

### Context: `5coins` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum |  | 1 |
| [`get_item_from_pool`](./Enums.md#enum-get_item_from_pool) | Enum | Event Action: Rewards the player with an item drawn from a specific loot pool. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`prompt`](./Strings.md#string-prompt) | String |  | 1 |
| `set_frame` | Number |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| `stat_max` | Number |  | 1 |
| `stat_min` | Number |  | 1 |
| `weight` | Number | Probability weight for this outcome. | 1 |

</details>

---

### Context: `altar_sacrifice` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `arm` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `attach_amplifier` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `attach_leech` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `bash_past_alt` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `bite_it_off` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `blue` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`copy_results`](./Enums.md#enum-copy_results) | Enum |  | 1 |
| `fixed_chance` | Number |  | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `blue_needle` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `body` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `book` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `brace` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `break_ice` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |

</details>

---

### Context: `break_lock` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `bribe` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `button` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`copy_results`](./Enums.md#enum-copy_results) | Enum |  | 1 |
| `fixed_chance` | Number |  | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `buy1` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`prompt`](./Strings.md#string-prompt) | String |  | 1 |
| [`self_status_next_fight`](./Events_and_Encounters.md#context-self_status_next_fight) | Block | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| `stat_max` | Number |  | 1 |
| `stat_min` | Number |  | 1 |
| `weight` | Number | Probability weight for this outcome. | 1 |

</details>

---

### Context: `catch` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `challenge_to_game` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `chaos_ending` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `chapter_cutscene` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `charm_past_alt` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `climb` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `comfort` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `communicate` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `concheck` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `counter` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `crack_open` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `cross` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |

</details>

---

### Context: `cut_wires` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `damage_1` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `damage_full` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `damage_half` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `desert_cutscene` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `dexcheck` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `dig` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `disarm` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `dive` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `donate` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `donate_10` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum |  | 1 |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| `stat_max` | Number |  | 1 |
| `stat_min` | Number |  | 1 |

</details>

---

### Context: `donate_15` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum |  | 1 |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| `stat_max` | Number |  | 1 |
| `stat_min` | Number |  | 1 |

</details>

---

### Context: `donate_20` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum |  | 1 |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| `stat_max` | Number |  | 1 |
| `stat_min` | Number |  | 1 |

</details>

---

### Context: `donate_5` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum |  | 1 |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| `stat_max` | Number |  | 1 |
| `stat_min` | Number |  | 1 |

</details>

---

### Context: `double` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `eat_meat` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `enter_crater` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `face` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |

</details>

---

### Context: `fiddle` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `fill_jar` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `find` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `fire` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `flush_yourself` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |

</details>

---

### Context: `follow` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `free` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `future` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`hint_chapter_exit`](./Enums.md#enum-hint_chapter_exit) | Enum |  | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `gain_clone_familiar` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`good`](./Events_and_Encounters.md#context-good)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 1 |

</details>

---

### Context: `gain_familiar` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `initial_health` | Number |  | 1 |
| [`object`](./Enums.md#enum-object) | Enum |  | 1 |

</details>

---

### Context: `give_parasite` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |

</details>

---

### Context: `hack` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `head` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |

</details>

---

### Context: `holy` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `hp` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `ice` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `infinite` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`hint_chapter_exit`](./Enums.md#enum-hint_chapter_exit) | Enum |  | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `intcheck` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `intimidation` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `itchies` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `join` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `jump` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `jump_over` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `keep_going` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |

</details>

---

### Context: `kiss_meat` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `knife` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `leave_it_in` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `leg` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `lever` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| `fixed_chance` | Number |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `lick_alt` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `lightning` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `listen` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `looks` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `loot_heart` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `makeup` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `mind` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `neck` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |

</details>

---

### Context: `nothanks` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `outsmart` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `patch_up` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `pick_lock` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `pilfer` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `pirouette` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `place_gristle` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `power` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `pull` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `pull_it_out` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `pull_lever` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |

</details>

---

### Context: `purify` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `push_buttons` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |

</details>

---

### Context: `push_through` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `put_in_coins` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum |  | 1 |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| `stat_max` | Number |  | 1 |
| `stat_min` | Number |  | 1 |

</details>

---

### Context: `put_out_of_misery` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `random_chance` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`reward`](./Events_and_Encounters.md#context-reward)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number | Probability weight for this outcome. | 1 |
| [`get_item_from_pool`](./Enums.md#enum-get_item_from_pool) | Enum | Event Action: Rewards the player with an item drawn from a specific loot pool. | 1 |

</details>

---

### Context: `random_mutation` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`else`](./Events_and_Encounters.md#context-else)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `count` | Number | Quantity. | 15 |
| [`tag`](./Enums.md#enum-tag) | Enum | Specific entity tag required. | 12 |
| `asymmetric` | Boolean |  | 8 |

</details>

---

### Context: `reach_inside` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `read` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `receive` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `red` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| `fixed_chance` | Number |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `red_needle` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `reflect` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `remove` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `remove_the_nail` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `repair_quest` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `rest` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `revive` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `rub` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `run_again` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `run_away` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `sacrifice_full_favor` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `sacrifice_normal` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `sacrifice_partial_favor` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `sacrifice_quest` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `scream` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `shake` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `slip_through` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `sneak_by` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `sneak_past_alt` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `soul` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `spawn_reflection_next_fight` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`mutation`](./Events_and_Encounters.md#context-mutation) | Block | Event Node: Story branch or dialog option representing the 'Mutation' action. | 1 |

</details>

---

### Context: `speed` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `surprise` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `sweet_talk` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `swim` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `tail` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `take_blood` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `talk` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `talk_to` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `tappytoes` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `teleport` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `thorns` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `throw` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `timemachine` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `traverse` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`play_animation`](./Enums.md#enum-play_animation) | Enum |  | 1 |
| [`prompt`](./Strings.md#string-prompt) | String |  | 1 |
| [`shop_now`](./Enums.md#enum-shop_now) | Enum |  | 1 |

</details>

---

### Context: `upgrade_yourself` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `use_item` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `use_toilet_con` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `use_toilet_str` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `use_weapon` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |

</details>

---

### Context: `w1` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `w2` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `w3` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `w4` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `w5` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `w6` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `wealth` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `wheezies` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `wish_genes` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `wish_items` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `wish_levelups` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `wish_strength` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `withstand` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `yank_it_out` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `yellow_needle` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bad`](./Events_and_Encounters.md#context-bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

