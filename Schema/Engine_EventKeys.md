# Mewgenics Mod Developer Documentation: Engine: Event Keys

## Engine: Event Keys

This document defines the schema shared by all Event Node blocks (`good`, `bad`, `main`, `reward`, `common`, `rare`). Each key in these blocks defines what happens as part of that event outcome.

> **Referenced by:** [`reward` (Events_and_Encounters)](./Events_and_Encounters.md#context-reward), [`common` (Events_and_Encounters)](./Events_and_Encounters.md#context-common), [`rare` (Events_and_Encounters)](./Events_and_Encounters.md#context-rare), [`good` (Events_and_Encounters)](./Events_and_Encounters.md#context-good), [`bad` (Events_and_Encounters)](./Events_and_Encounters.md#context-bad), [`main` (Events_and_Encounters)](./Events_and_Encounters.md#context-main), [`reward` (Miscellaneous)](./Miscellaneous.md#context-reward), [`common` (Miscellaneous)](./Miscellaneous.md#context-common), [`rare` (Miscellaneous)](./Miscellaneous.md#context-rare)

### Valid Property Keys

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`add_weather`](./Enums.md#enum-add_weather) | Enum |  |
| `ally_ambush_next_fights` | Integer |  |
| [`ambush`](./Math_Equations.md) | Equation |  |
| `ambush_next_basic_fights` | Integer |  |
| [`bad`](#bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. |
| [`battle`](./Math_Equations.md) | Equation |  |
| [`begin_chapter`](./Enums.md#enum-begin_chapter) | Enum |  |
| [`clear_adventure_token`](./Enums.md#enum-clear_adventure_token) | Enum |  |
| `clear_result_animation` | Integer |  |
| [`clear_surviving_kaiju`](./Enums.md#enum-clear_surviving_kaiju) | Enum |  |
| `clone_self_to_party` | Integer |  |
| [`common`](#common) | Block | Event Node: Story branch or dialog option representing the 'Common' action. |
| [`complete_item_quest`](./Enums.md#enum-complete_item_quest) | Enum |  |
| [`conditional_reward`](#conditional_reward) | Block | Event Action: Provides a reward only if a specific condition is met. |
| `copy_items_to_party` | Integer |  |
| `copy_party_items` | Integer |  |
| `cutscene` | String | Event Node: Triggers a narrative cutscene. |
| [`cutscene_on_exit`](./Enums.md#enum-cutscene_on_exit) | Enum |  |
| `damage` | Integer | Event Node: Story branch or dialog option representing the 'Damage' action. |
| [`decrement_legacy_counter`](./Enums.md#enum-decrement_legacy_counter) | Enum |  |
| [`event_now`](./Enums.md#enum-event_now) | Enum |  |
| [`event_now_same_cat`](./Enums.md#enum-event_now_same_cat) | Enum |  |
| `full_heal` | Integer |  |
| `gain_cat_familiar` | Integer |  |
| [`gain_clone_familiar`](#gain_clone_familiar) | Block | Event Action: Adds a clone of a character to the party as a familiar. |
| [`gain_coins`](./Arrays.md#array-gain_coins) | Array |  |
| [`gain_disorder`](./Enums.md#enum-gain_disorder) | Enum |  |
| [`gain_disorder_from_pool`](./Enums.md#enum-gain_disorder_from_pool) | Enum |  |
| [`gain_familiar`](./Enums.md#enum-gain_familiar) | Enum | Event Action: Adds a specific familiar to the party. |
| [`gain_food`](./Arrays.md#array-gain_food) | Array |  |
| [`gain_immortal_familiar`](./Enums.md#enum-gain_immortal_familiar) | Enum |  |
| [`get_and_equip_item`](./Enums.md#enum-get_and_equip_item) | Enum |  |
| [`get_full_item_set_from_pool`](./Enums.md#enum-get_full_item_set_from_pool) | Enum |  |
| [`get_item`](./Enums.md#enum-get_item) | Enum |  |
| [`get_item_from_pool`](./Enums.md#enum-get_item_from_pool) | Enum | Event Action: Rewards the player with an item drawn from a specific loot pool. |
| [`get_parasite`](./Enums.md#enum-get_parasite) | Enum |  |
| [`get_parasite_from_pool`](./Enums.md#enum-get_parasite_from_pool) | Enum |  |
| [`global_effect_next_fight`](#global_effect_next_fight) | Block | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. |
| [`goto`](./Enums.md#enum-goto) | Enum |  |
| `heal` | Integer |  |
| `heal_disorder` | Integer |  |
| `heal_injury` | Integer |  |
| `hide_appearance_changes` | Integer |  |
| [`increment_legacy_counter`](./Enums.md#enum-increment_legacy_counter) | Enum |  |
| [`injury`](./Enums.md#enum-injury) | Enum |  |
| [`kill`](./Enums.md#enum-kill) | Enum |  |
| [`learn_ability`](./Enums.md#enum-learn_ability) | Enum |  |
| [`learn_ability_from_pool`](./Arrays.md#array-learn_ability_from_pool) | Array |  |
| [`learn_passive`](./Enums.md#enum-learn_passive) | Enum |  |
| [`learn_passive_from_pool`](./Arrays.md#array-learn_passive_from_pool) | Array |  |
| [`leave`](#leave) | Block | Event Node: Story branch or dialog option representing the 'Leave' action. |
| [`leave_party_temporarily`](#leave_party_temporarily) | Block | Event Action: Removes a character from the active team until the next hub area. |
| [`level_up`](./Enums.md#enum-level_up) | Enum |  |
| [`lose_all_equipped_items`](./Enums.md#enum-lose_all_equipped_items) | Enum |  |
| [`lose_item`](./Enums.md#enum-lose_item) | Enum |  |
| [`lose_item_from_inventory`](./Enums.md#enum-lose_item_from_inventory) | Enum |  |
| [`lose_specific_item`](./Enums.md#enum-lose_specific_item) | Enum |  |
| [`make_old`](./Enums.md#enum-make_old) | Enum |  |
| `max_options` | Integer |  |
| [`mutation`](#mutation) | Block | Event Node: Story branch or dialog option representing the 'Mutation' action. |
| `next_event_bonus` | Integer |  |
| [`next_event_from_set`](./Enums.md#enum-next_event_from_set) | Enum | Event Action: Chains immediately into a randomly selected subsequent story event. |
| [`options`](#options) | Block | Event Block: Lists the available clickable dialog choices for the current story node. |
| [`outcome`](#outcome) | Block | Event Block: Logic and text executed after selecting a specific dialog option. |
| `override_end_option_prompt` | String |  |
| [`party_damage`](./Arrays.md#array-party_damage) | Array |  |
| [`party_gain_disorder_from_pool`](./Arrays.md#array-party_gain_disorder_from_pool) | Array |  |
| `party_heal` | Integer |  |
| `party_heal_disorder` | Integer |  |
| `party_heal_injury` | Integer |  |
| [`party_injury`](./Enums.md#enum-party_injury) | Enum |  |
| [`party_permanent_stats`](#party_permanent_stats) | Block | Event Reward: Permanently increases (or decreases) the core stats of all party members. |
| [`party_permanent_stats_exclude_self`](#party_permanent_stats_exclude_self) | Block | Event Reward: Permanently modifies stats for all party members except the one who initiated the action. |
| `party_random_mutation` | Integer |  |
| [`party_random_mutation_from_set`](#party_random_mutation_from_set) | Block | Event Reward: Applies a random mutation to the entire party from a specific pool. |
| [`party_status_next_fight`](#party_status_next_fight) | Block | Event Penalty/Reward: Applies a status effect to the entire party at the start of the next combat encounter. |
| [`permanent_stats`](#permanent_stats) | Block | Event Reward: Permanently increases (or decreases) the core stats of a single character. |
| [`play_animation`](./Enums.md#enum-play_animation) | Enum |  |
| [`play_result_animation`](./Enums.md#enum-play_result_animation) | Enum |  |
| `prompt` | String |  |
| [`random_chance`](#random_chance) | Block | Event Logic: Executes the nested outcome based on a percentage roll. |
| `random_mutation` | Integer | Event Reward: Applies a completely random mutation to a character. |
| [`random_mutation_from_set`](#random_mutation_from_set) | Block | Event Reward: Applies a random mutation to a character from a specific pool. |
| [`random_pool`](./Arrays.md#array-random_pool) | Array |  |
| [`random_pool_consider_luck`](./Arrays.md#array-random_pool_consider_luck) | Array |  |
| [`rare`](#rare) | Block | Event Node: Story branch or dialog option representing the 'Rare' action. |
| [`requires_flag`](./Enums.md#enum-requires_flag) | Enum | Prerequisite: Must meet this condition. |
| [`reward`](#reward) | Block | Event Node: Story branch or dialog option representing the 'Reward' action. |
| [`scramble_abilities`](./Enums.md#enum-scramble_abilities) | Enum |  |
| [`scramble_basic_attack`](./Enums.md#enum-scramble_basic_attack) | Enum |  |
| [`scramble_passives`](./Enums.md#enum-scramble_passives) | Enum |  |
| [`select_item_from_pool_for_cutscene_only`](./Enums.md#enum-select_item_from_pool_for_cutscene_only) | Enum |  |
| `self_damage` | Integer | Recoil or self-inflicted damage/effects applied to the caster. |
| `self_heal` | Integer |  |
| [`self_status_next_fight`](#self_status_next_fight) | Block | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. |
| [`set_adventure_token`](./Enums.md#enum-set_adventure_token) | Enum |  |
| `set_age` | Integer |  |
| `set_frame` | Integer |  |
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum |  |
| [`set_subject`](./Enums.md#enum-set_subject) | Enum |  |
| [`setup`](#setup) | Block | Event Block: Pre-initialization logic executed before the event UI is drawn. |
| [`shop_now`](./Enums.md#enum-shop_now) | Enum |  |
| `shuffle_options` | Boolean |  |
| `spawn_reflection_next_fight` | Integer | Event Penalty: Spawns dark clones/reflections of the party in the next combat encounter. |
| [`spawn_unit_next_fight`](#spawn_unit_next_fight) | Block | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. |
| [`spin`](./Enums.md#enum-spin) | Enum |  |
| [`transform_item`](./Arrays.md#array-transform_item) | Array |  |
| [`trigger_adventure_unlock`](./Enums.md#enum-trigger_adventure_unlock) | Enum |  |
| `trigger_butterfly_effect` | Integer |  |
| [`unlock_item_quest`](./Enums.md#enum-unlock_item_quest) | Enum |  |
| [`upgrade_ability`](./Enums.md#enum-upgrade_ability) | Enum |  |
| [`upgrade_passive`](./Enums.md#enum-upgrade_passive) | Enum |  |
| `weight` | Float | Probability weight for this outcome. |

</details>

### Valid Nested Blocks

The following blocks all behave as `{Event Keys}` containers. Each has its own unique parameters listed below its entry.

---

#### `bad`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |
| [`battle`](./Math_Equations.md) | Equation |  |
| [`conditional_reward`](#conditional_reward) | Block | Event Action: Provides a reward only if a specific condition is met. |
| [`cutscene`](#cutscene) | Block | Event Node: Triggers a narrative cutscene. |
| [`event_now`](./Enums.md#enum-event_now) | Enum |  |
| [`event_now_same_cat`](./Enums.md#enum-event_now_same_cat) | Enum |  |
| [`gain_disorder_from_pool`](./Enums.md#enum-gain_disorder_from_pool) | Enum |  |
| [`gain_immortal_familiar`](./Enums.md#enum-gain_immortal_familiar) | Enum |  |
| [`get_parasite`](./Enums.md#enum-get_parasite) | Enum |  |
| [`get_parasite_from_pool`](./Enums.md#enum-get_parasite_from_pool) | Enum |  |
| [`injury`](./Enums.md#enum-injury) | Enum |  |
| [`kill`](./Enums.md#enum-kill) | Enum |  |
| [`lose_item`](./Enums.md#enum-lose_item) | Enum |  |
| `next_event_bonus` | Integer |  |
| [`party_random_mutation_from_set`](#party_random_mutation_from_set) | Block | Event Reward: Applies a random mutation to the entire party from a specific pool. |
| [`permanent_stats`](#permanent_stats) | Block | Event Reward: Permanently increases (or decreases) the core stats of a single character. |
| [`play_animation`](./Arrays.md#array-play_animation) | Array |  |
| `prompt` | String |  |
| [`reward`](#reward) | Block | Event Node: Story branch or dialog option representing the 'Reward' action. |
| [`select_item_from_pool_for_cutscene_only`](./Enums.md#enum-select_item_from_pool_for_cutscene_only) | Enum |  |
| [`self_status_next_fight`](#self_status_next_fight) | Block | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. |
| `set_frame` | Integer |  |
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum |  |

</details>

---

#### `common`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |
| [`add_weather`](./Enums.md#enum-add_weather) | Enum |  |
| `ally_ambush_next_fights` | Integer |  |
| `ambush_next_basic_fights` | Integer |  |
| [`clear_adventure_token`](./Enums.md#enum-clear_adventure_token) | Enum |  |
| `clear_result_animation` | Integer |  |
| [`conditional_reward`](#conditional_reward) | Block | Event Action: Provides a reward only if a specific condition is met. |
| `damage` | Integer | Event Node: Story branch or dialog option representing the 'Damage' action. |
| [`decrement_legacy_counter`](./Enums.md#enum-decrement_legacy_counter) | Enum |  |
| [`event_now`](./Enums.md#enum-event_now) | Enum |  |
| [`event_now_same_cat`](./Enums.md#enum-event_now_same_cat) | Enum |  |
| `full_heal` | Integer |  |
| [`gain_coins`](./Arrays.md#array-gain_coins) | Array |  |
| [`gain_disorder`](./Enums.md#enum-gain_disorder) | Enum |  |
| [`gain_disorder_from_pool`](./Enums.md#enum-gain_disorder_from_pool) | Enum |  |
| [`gain_familiar`](./Enums.md#enum-gain_familiar) | Enum | Event Action: Adds a specific familiar to the party. |
| [`gain_food`](./Arrays.md#array-gain_food) | Array |  |
| [`get_and_equip_item`](./Enums.md#enum-get_and_equip_item) | Enum |  |
| [`get_item`](./Enums.md#enum-get_item) | Enum |  |
| [`get_item_from_pool`](./Enums.md#enum-get_item_from_pool) | Enum | Event Action: Rewards the player with an item drawn from a specific loot pool. |
| [`get_parasite`](./Enums.md#enum-get_parasite) | Enum |  |
| [`get_parasite_from_pool`](./Enums.md#enum-get_parasite_from_pool) | Enum |  |
| [`global_effect_next_fight`](#global_effect_next_fight) | Block | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. |
| `heal` | Integer |  |
| `heal_disorder` | Integer |  |
| `heal_injury` | Integer |  |
| [`increment_legacy_counter`](./Enums.md#enum-increment_legacy_counter) | Enum |  |
| [`injury`](./Enums.md#enum-injury) | Enum |  |
| [`kill`](./Enums.md#enum-kill) | Enum |  |
| [`learn_ability_from_pool`](./Enums.md#enum-learn_ability_from_pool) | Enum |  |
| [`lose_item`](./Enums.md#enum-lose_item) | Enum |  |
| [`lose_specific_item`](./Enums.md#enum-lose_specific_item) | Enum |  |
| [`mutation`](#mutation) | Block | Event Node: Story branch or dialog option representing the 'Mutation' action. |
| `next_event_bonus` | Integer |  |
| [`next_event_from_set`](#next_event_from_set) | Block | Event Action: Chains immediately into a randomly selected subsequent story event. |
| `override_end_option_prompt` | String |  |
| [`party_damage`](./Arrays.md#array-party_damage) | Array |  |
| `party_heal` | Integer |  |
| `party_heal_disorder` | Integer |  |
| [`party_permanent_stats_exclude_self`](#party_permanent_stats_exclude_self) | Block | Event Reward: Permanently modifies stats for all party members except the one who initiated the action. |
| [`party_status_next_fight`](#party_status_next_fight) | Block | Event Penalty/Reward: Applies a status effect to the entire party at the start of the next combat encounter. |
| [`permanent_stats`](#permanent_stats) | Block | Event Reward: Permanently increases (or decreases) the core stats of a single character. |
| [`play_animation`](./Arrays.md#array-play_animation) | Array |  |
| `prompt` | String |  |
| `random_mutation` | Integer | Event Reward: Applies a completely random mutation to a character. |
| [`random_mutation_from_set`](#random_mutation_from_set) | Block | Event Reward: Applies a random mutation to a character from a specific pool. |
| [`random_pool`](./Arrays.md#array-random_pool) | Array |  |
| `self_damage` | Integer | Recoil or self-inflicted damage/effects applied to the caster. |
| `self_heal` | Integer |  |
| [`self_status_next_fight`](#self_status_next_fight) | Block | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. |
| [`set_adventure_token`](./Enums.md#enum-set_adventure_token) | Enum |  |
| `set_frame` | Integer |  |
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum |  |
| [`shop_now`](./Enums.md#enum-shop_now) | Enum |  |
| [`spawn_unit_next_fight`](#spawn_unit_next_fight) | Block | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. |
| [`spin`](./Enums.md#enum-spin) | Enum |  |
| [`upgrade_ability`](./Enums.md#enum-upgrade_ability) | Enum |  |

</details>

---

#### `good`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |
| [`add_weather`](./Enums.md#enum-add_weather) | Enum |  |
| `ally_ambush_next_fights` | Integer |  |
| [`begin_chapter`](./Enums.md#enum-begin_chapter) | Enum |  |
| [`clear_surviving_kaiju`](./Enums.md#enum-clear_surviving_kaiju) | Enum |  |
| `clone_self_to_party` | Integer |  |
| [`complete_item_quest`](./Enums.md#enum-complete_item_quest) | Enum |  |
| [`conditional_reward`](#conditional_reward) | Block | Event Action: Provides a reward only if a specific condition is met. |
| `copy_items_to_party` | Integer |  |
| `copy_party_items` | Integer |  |
| `cutscene` | String | Event Node: Triggers a narrative cutscene. |
| [`cutscene_on_exit`](./Enums.md#enum-cutscene_on_exit) | Enum |  |
| [`event_now`](./Enums.md#enum-event_now) | Enum |  |
| [`event_now_same_cat`](./Enums.md#enum-event_now_same_cat) | Enum |  |
| `full_heal` | Integer |  |
| [`gain_clone_familiar`](#gain_clone_familiar) | Block | Event Action: Adds a clone of a character to the party as a familiar. |
| [`gain_disorder`](./Enums.md#enum-gain_disorder) | Enum |  |
| [`gain_disorder_from_pool`](./Enums.md#enum-gain_disorder_from_pool) | Enum |  |
| [`gain_food`](./Arrays.md#array-gain_food) | Array |  |
| [`get_full_item_set_from_pool`](./Enums.md#enum-get_full_item_set_from_pool) | Enum |  |
| [`get_item`](./Enums.md#enum-get_item) | Enum |  |
| [`get_item_from_pool`](./Enums.md#enum-get_item_from_pool) | Enum | Event Action: Rewards the player with an item drawn from a specific loot pool. |
| [`get_parasite`](./Enums.md#enum-get_parasite) | Enum |  |
| [`global_effect_next_fight`](#global_effect_next_fight) | Block | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. |
| `heal` | Integer |  |
| `heal_disorder` | Integer |  |
| `heal_injury` | Integer |  |
| [`increment_legacy_counter`](./Enums.md#enum-increment_legacy_counter) | Enum |  |
| [`injury`](./Enums.md#enum-injury) | Enum |  |
| [`kill`](./Enums.md#enum-kill) | Enum |  |
| [`learn_ability_from_pool`](./Arrays.md#array-learn_ability_from_pool) | Array |  |
| [`learn_passive_from_pool`](./Arrays.md#array-learn_passive_from_pool) | Array |  |
| [`level_up`](./Enums.md#enum-level_up) | Enum |  |
| [`lose_item`](./Enums.md#enum-lose_item) | Enum |  |
| [`lose_specific_item`](./Enums.md#enum-lose_specific_item) | Enum |  |
| [`mutation`](#mutation) | Block | Event Node: Story branch or dialog option representing the 'Mutation' action. |
| `next_event_bonus` | Integer |  |
| [`next_event_from_set`](#next_event_from_set) | Block | Event Action: Chains immediately into a randomly selected subsequent story event. |
| `override_end_option_prompt` | String |  |
| [`party_gain_disorder_from_pool`](./Arrays.md#array-party_gain_disorder_from_pool) | Array |  |
| [`play_animation`](./Enums.md#enum-play_animation) | Enum |  |
| `prompt` | String |  |
| `random_mutation` | Integer | Event Reward: Applies a completely random mutation to a character. |
| [`random_pool`](./Arrays.md#array-random_pool) | Array |  |
| [`random_pool_consider_luck`](./Arrays.md#array-random_pool_consider_luck) | Array |  |
| [`rare`](#rare) | Block | Event Node: Story branch or dialog option representing the 'Rare' action. |
| [`reward`](#reward) | Block | Event Node: Story branch or dialog option representing the 'Reward' action. |
| [`scramble_abilities`](./Enums.md#enum-scramble_abilities) | Enum |  |
| [`scramble_passives`](./Enums.md#enum-scramble_passives) | Enum |  |
| [`set_adventure_token`](./Enums.md#enum-set_adventure_token) | Enum |  |
| `set_frame` | Integer |  |
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum |  |
| [`shop_now`](./Enums.md#enum-shop_now) | Enum |  |
| [`transform_item`](./Arrays.md#array-transform_item) | Array |  |
| [`trigger_adventure_unlock`](./Enums.md#enum-trigger_adventure_unlock) | Enum |  |
| `trigger_butterfly_effect` | Integer |  |
| [`unlock_item_quest`](./Enums.md#enum-unlock_item_quest) | Enum |  |
| [`upgrade_ability`](./Enums.md#enum-upgrade_ability) | Enum |  |
| [`upgrade_passive`](./Enums.md#enum-upgrade_passive) | Enum |  |

</details>

---

#### `main`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |
| [`add_weather`](./Enums.md#enum-add_weather) | Enum |  |
| [`bad`](#bad) | Block | Event Node: Story branch or dialog option representing the 'Bad' action. |
| [`gain_familiar`](./Enums.md#enum-gain_familiar) | Enum | Event Action: Adds a specific familiar to the party. |
| [`goto`](./Enums.md#enum-goto) | Enum |  |
| [`leave`](#leave) | Block | Event Node: Story branch or dialog option representing the 'Leave' action. |
| `max_options` | Integer |  |
| [`next_event_from_set`](./Enums.md#enum-next_event_from_set) | Enum | Event Action: Chains immediately into a randomly selected subsequent story event. |
| [`options`](#options) | Block | Event Block: Lists the available clickable dialog choices for the current story node. |
| [`outcome`](#outcome) | Block | Event Block: Logic and text executed after selecting a specific dialog option. |
| `party_heal` | Integer |  |
| [`party_permanent_stats`](#party_permanent_stats) | Block | Event Reward: Permanently increases (or decreases) the core stats of all party members. |
| [`play_animation`](./Arrays.md#array-play_animation) | Array |  |
| `prompt` | String |  |
| [`rare`](#rare) | Block | Event Node: Story branch or dialog option representing the 'Rare' action. |
| [`requires_flag`](./Enums.md#enum-requires_flag) | Enum | Prerequisite: Must meet this condition. |
| [`self_damage`](./Arrays.md#array-self_damage) | Array | Recoil or self-inflicted damage/effects applied to the caster. |
| [`self_status_next_fight`](#self_status_next_fight) | Block | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. |
| `set_frame` | Integer |  |
| [`setup`](#setup) | Block | Event Block: Pre-initialization logic executed before the event UI is drawn. |
| [`shop_now`](./Enums.md#enum-shop_now) | Enum |  |
| `shuffle_options` | Boolean |  |
| `weight` | Float | Probability weight for this outcome. |

</details>

---

#### `rare`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |
| [`add_weather`](./Enums.md#enum-add_weather) | Enum |  |
| `ally_ambush_next_fights` | Integer |  |
| [`ambush`](./Math_Equations.md) | Equation |  |
| `ambush_next_basic_fights` | Integer |  |
| [`battle`](./Math_Equations.md) | Equation |  |
| `clear_result_animation` | Integer |  |
| [`conditional_reward`](#conditional_reward) | Block | Event Action: Provides a reward only if a specific condition is met. |
| `damage` | Integer | Event Node: Story branch or dialog option representing the 'Damage' action. |
| [`decrement_legacy_counter`](./Enums.md#enum-decrement_legacy_counter) | Enum |  |
| [`event_now`](./Enums.md#enum-event_now) | Enum |  |
| [`event_now_same_cat`](./Enums.md#enum-event_now_same_cat) | Enum |  |
| `full_heal` | Integer |  |
| `gain_cat_familiar` | Integer |  |
| [`gain_coins`](./Arrays.md#array-gain_coins) | Array |  |
| [`gain_disorder`](./Enums.md#enum-gain_disorder) | Enum |  |
| [`gain_disorder_from_pool`](./Enums.md#enum-gain_disorder_from_pool) | Enum |  |
| [`gain_familiar`](./Enums.md#enum-gain_familiar) | Enum | Event Action: Adds a specific familiar to the party. |
| [`gain_food`](./Arrays.md#array-gain_food) | Array |  |
| [`gain_immortal_familiar`](./Enums.md#enum-gain_immortal_familiar) | Enum |  |
| [`get_and_equip_item`](./Enums.md#enum-get_and_equip_item) | Enum |  |
| [`get_item`](./Enums.md#enum-get_item) | Enum |  |
| [`get_item_from_pool`](./Enums.md#enum-get_item_from_pool) | Enum | Event Action: Rewards the player with an item drawn from a specific loot pool. |
| [`get_parasite`](./Enums.md#enum-get_parasite) | Enum |  |
| [`get_parasite_from_pool`](./Enums.md#enum-get_parasite_from_pool) | Enum |  |
| [`global_effect_next_fight`](#global_effect_next_fight) | Block | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. |
| `heal_disorder` | Integer |  |
| `hide_appearance_changes` | Integer |  |
| [`increment_legacy_counter`](./Enums.md#enum-increment_legacy_counter) | Enum |  |
| [`injury`](./Enums.md#enum-injury) | Enum |  |
| [`kill`](./Enums.md#enum-kill) | Enum |  |
| [`learn_ability`](./Enums.md#enum-learn_ability) | Enum |  |
| [`learn_ability_from_pool`](./Enums.md#enum-learn_ability_from_pool) | Enum |  |
| [`learn_passive`](./Enums.md#enum-learn_passive) | Enum |  |
| [`learn_passive_from_pool`](./Enums.md#enum-learn_passive_from_pool) | Enum |  |
| [`leave_party_temporarily`](#leave_party_temporarily) | Block | Event Action: Removes a character from the active team until the next hub area. |
| [`level_up`](./Enums.md#enum-level_up) | Enum |  |
| [`lose_all_equipped_items`](./Enums.md#enum-lose_all_equipped_items) | Enum |  |
| [`lose_item`](./Enums.md#enum-lose_item) | Enum |  |
| [`lose_item_from_inventory`](./Enums.md#enum-lose_item_from_inventory) | Enum |  |
| [`lose_specific_item`](./Enums.md#enum-lose_specific_item) | Enum |  |
| [`make_old`](./Enums.md#enum-make_old) | Enum |  |
| [`mutation`](#mutation) | Block | Event Node: Story branch or dialog option representing the 'Mutation' action. |
| `next_event_bonus` | Integer |  |
| [`next_event_from_set`](./Enums.md#enum-next_event_from_set) | Enum | Event Action: Chains immediately into a randomly selected subsequent story event. |
| `override_end_option_prompt` | String |  |
| `party_damage` | Integer |  |
| `party_heal` | Integer |  |
| `party_heal_disorder` | Integer |  |
| `party_heal_injury` | Integer |  |
| [`party_injury`](./Enums.md#enum-party_injury) | Enum |  |
| [`party_permanent_stats`](#party_permanent_stats) | Block | Event Reward: Permanently increases (or decreases) the core stats of all party members. |
| [`party_permanent_stats_exclude_self`](#party_permanent_stats_exclude_self) | Block | Event Reward: Permanently modifies stats for all party members except the one who initiated the action. |
| `party_random_mutation` | Integer |  |
| [`party_random_mutation_from_set`](#party_random_mutation_from_set) | Block | Event Reward: Applies a random mutation to the entire party from a specific pool. |
| [`party_status_next_fight`](#party_status_next_fight) | Block | Event Penalty/Reward: Applies a status effect to the entire party at the start of the next combat encounter. |
| [`permanent_stats`](#permanent_stats) | Block | Event Reward: Permanently increases (or decreases) the core stats of a single character. |
| [`play_animation`](./Arrays.md#array-play_animation) | Array |  |
| [`play_result_animation`](./Enums.md#enum-play_result_animation) | Enum |  |
| `prompt` | String |  |
| `random_mutation` | Integer | Event Reward: Applies a completely random mutation to a character. |
| [`random_mutation_from_set`](#random_mutation_from_set) | Block | Event Reward: Applies a random mutation to a character from a specific pool. |
| [`random_pool`](./Arrays.md#array-random_pool) | Array |  |
| [`scramble_abilities`](./Enums.md#enum-scramble_abilities) | Enum |  |
| [`scramble_basic_attack`](./Enums.md#enum-scramble_basic_attack) | Enum |  |
| `self_damage` | Integer | Recoil or self-inflicted damage/effects applied to the caster. |
| [`self_status_next_fight`](#self_status_next_fight) | Block | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. |
| [`set_adventure_token`](./Enums.md#enum-set_adventure_token) | Enum |  |
| `set_age` | Integer |  |
| `set_frame` | Integer |  |
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum |  |
| [`shop_now`](./Enums.md#enum-shop_now) | Enum |  |
| `spawn_reflection_next_fight` | Integer | Event Penalty: Spawns dark clones/reflections of the party in the next combat encounter. |
| [`spawn_unit_next_fight`](#spawn_unit_next_fight) | Block | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. |
| [`trigger_adventure_unlock`](./Enums.md#enum-trigger_adventure_unlock) | Enum |  |
| [`upgrade_ability`](./Enums.md#enum-upgrade_ability) | Enum |  |
| [`upgrade_passive`](./Enums.md#enum-upgrade_passive) | Enum |  |

</details>

---

#### `reward`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |
| `ambush_next_basic_fights` | Integer |  |
| [`clear_adventure_token`](./Enums.md#enum-clear_adventure_token) | Enum |  |
| [`common`](#common) | Block | Event Node: Story branch or dialog option representing the 'Common' action. |
| [`cutscene_on_exit`](./Enums.md#enum-cutscene_on_exit) | Enum |  |
| [`event_now`](./Enums.md#enum-event_now) | Enum |  |
| [`gain_coins`](./Arrays.md#array-gain_coins) | Array |  |
| [`gain_disorder_from_pool`](./Enums.md#enum-gain_disorder_from_pool) | Enum |  |
| [`get_item`](./Enums.md#enum-get_item) | Enum |  |
| [`get_item_from_pool`](./Enums.md#enum-get_item_from_pool) | Enum | Event Action: Rewards the player with an item drawn from a specific loot pool. |
| [`get_parasite_from_pool`](./Enums.md#enum-get_parasite_from_pool) | Enum |  |
| [`injury`](./Enums.md#enum-injury) | Enum |  |
| [`level_up`](./Enums.md#enum-level_up) | Enum |  |
| `next_event_bonus` | Integer |  |
| [`party_damage`](./Arrays.md#array-party_damage) | Array |  |
| [`play_animation`](./Arrays.md#array-play_animation) | Array |  |
| `prompt` | String |  |
| [`random_chance`](#random_chance) | Block | Event Logic: Executes the nested outcome based on a percentage roll. |
| [`random_pool`](./Arrays.md#array-random_pool) | Array |  |
| [`rare`](#rare) | Block | Event Node: Story branch or dialog option representing the 'Rare' action. |
| [`set_adventure_token`](./Enums.md#enum-set_adventure_token) | Enum |  |
| `set_frame` | Integer |  |
| [`set_legacy_token`](./Enums.md#enum-set_legacy_token) | Enum |  |
| [`set_subject`](./Enums.md#enum-set_subject) | Enum |  |
| [`spawn_unit_next_fight`](#spawn_unit_next_fight) | Block | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. |
| [`trigger_adventure_unlock`](./Enums.md#enum-trigger_adventure_unlock) | Enum |  |
| `weight` | Float | Probability weight for this outcome. |

</details>

