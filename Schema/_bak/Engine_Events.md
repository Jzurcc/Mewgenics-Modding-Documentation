# Mewgenics Mod Developer Documentation: Engine: Event Nodes

> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Math_Equations.md).

## Engine: Event Nodes

This document defines the schema shared by all Event Node blocks (`good`, `bad`, `main`, `reward`, `common`, `rare`). Each key in these blocks defines what happens as part of that event outcome.

### Known Explicit Parameters

These are hardcoded configuration keys found within these blocks (not dynamic IDs).

<details>
<summary><b>Expand</b></summary>

| Parameter | Type | Notes |
| :--- | :--- | :--- |
| `add_weather` | Enum |  |
| `ally_ambush_next_fights` | Number |  |
| `ambush` | Equation |  |
| `ambush_next_basic_fights` | Number |  |
| `bad` | Block | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `battle` | Equation |  |
| `begin_chapter` | Enum |  |
| `clear_adventure_token` | Enum |  |
| `clear_result_animation` | Number |  |
| `clear_surviving_kaiju` | Enum |  |
| `clone_self_to_party` | Number |  |
| `common` | Block | Event Node: Story branch or dialog option representing the 'Common' action. |
| `complete_item_quest` | Enum |  |
| `conditional_reward` | Block | Event Action: Provides a reward only if a specific condition is met. |
| `copy_items_to_party` | Number |  |
| `copy_party_items` | Number |  |
| `cutscene` | String | Event Node: Triggers a narrative cutscene. |
| `cutscene_on_exit` | Enum |  |
| `damage` | Number | Event Node: Story branch or dialog option representing the 'Damage' action. |
| `decrement_legacy_counter` | Enum |  |
| `event_now` | Enum |  |
| `event_now_same_cat` | Enum |  |
| `full_heal` | Number |  |
| `gain_cat_familiar` | Number |  |
| `gain_clone_familiar` | Block | Event Action: Adds a clone of a character to the party as a familiar. |
| `gain_coins` | Array |  |
| `gain_disorder` | Enum |  |
| `gain_disorder_from_pool` | Enum |  |
| `gain_familiar` | Enum | Event Action: Adds a specific familiar to the party. |
| `gain_food` | Array |  |
| `gain_immortal_familiar` | Enum |  |
| `get_and_equip_item` | Enum |  |
| `get_full_item_set_from_pool` | Enum |  |
| `get_item` | Enum |  |
| `get_item_from_pool` | Enum | Event Action: Rewards the player with an item drawn from a specific loot pool. |
| `get_parasite` | Enum |  |
| `get_parasite_from_pool` | Enum |  |
| `global_effect_next_fight` | Block | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. |
| `goto` | Enum |  |
| `heal` | Number |  |
| `heal_disorder` | Number |  |
| `heal_injury` | Number |  |
| `hide_appearance_changes` | Number |  |
| `increment_legacy_counter` | Enum |  |
| `injury` | Enum |  |
| `kill` | Enum |  |
| `learn_ability` | Enum |  |
| `learn_ability_from_pool` | Array |  |
| `learn_passive` | Enum |  |
| `learn_passive_from_pool` | Array |  |
| `leave` | Block | Event Node: Story branch or dialog option representing the 'Leave' action. |
| `leave_party_temporarily` | Block | Event Action: Removes a character from the active team until the next hub area. |
| `level_up` | Enum |  |
| `lose_all_equipped_items` | Enum |  |
| `lose_item` | Enum |  |
| `lose_item_from_inventory` | Enum |  |
| `lose_specific_item` | Enum |  |
| `make_old` | Enum |  |
| `max_options` | Number |  |
| `mutation` | Block | Event Node: Story branch or dialog option representing the 'Mutation' action. |
| `next_event_bonus` | Number |  |
| `next_event_from_set` | Enum | Event Action: Chains immediately into a randomly selected subsequent story event. |
| `options` | Block | Event Block: Lists the available clickable dialog choices for the current story node. |
| `outcome` | Block | Event Block: Logic and text executed after selecting a specific dialog option. |
| `override_end_option_prompt` | String |  |
| `party_damage` | Array |  |
| `party_gain_disorder_from_pool` | Array |  |
| `party_heal` | Number |  |
| `party_heal_disorder` | Number |  |
| `party_heal_injury` | Number |  |
| `party_injury` | Enum |  |
| `party_permanent_stats` | Block | Event Reward: Permanently increases (or decreases) the core stats of all party members. |
| `party_permanent_stats_exclude_self` | Block | Event Reward: Permanently modifies stats for all party members except the one who initiated the action. |
| `party_random_mutation` | Number |  |
| `party_random_mutation_from_set` | Block | Event Reward: Applies a random mutation to the entire party from a specific pool. |
| `party_status_next_fight` | Block | Event Penalty/Reward: Applies a status effect to the entire party at the start of the next combat encounter. |
| `permanent_stats` | Block | Event Reward: Permanently increases (or decreases) the core stats of a single character. |
| `play_animation` | Enum |  |
| `play_result_animation` | Enum |  |
| `prompt` | String |  |
| `random_chance` | Block | Event Logic: Executes the nested outcome based on a percentage roll. |
| `random_mutation` | Number | Event Reward: Applies a completely random mutation to a character. |
| `random_mutation_from_set` | Block | Event Reward: Applies a random mutation to a character from a specific pool. |
| `random_pool` | Array |  |
| `random_pool_consider_luck` | Array |  |
| `rare` | Block | Event Node: Story branch or dialog option representing the 'Rare' action. |
| `requires_flag` | Enum | Prerequisite: Must meet this condition. |
| `reward` | Block | Event Node: Story branch or dialog option representing the 'Reward' action. |
| `scramble_abilities` | Enum |  |
| `scramble_basic_attack` | Enum |  |
| `scramble_passives` | Enum |  |
| `select_item_from_pool_for_cutscene_only` | Enum |  |
| `self_damage` | Number | Recoil or self-inflicted damage/effects applied to the caster. |
| `self_heal` | Number |  |
| `self_status_next_fight` | Block | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. |
| `set_adventure_token` | Enum |  |
| `set_age` | Number |  |
| `set_frame` | Number |  |
| `set_legacy_token` | Enum |  |
| `set_subject` | Enum |  |
| `setup` | Block | Event Block: Pre-initialization logic executed before the event UI is drawn. |
| `shop_now` | Enum |  |
| `shuffle_options` | Boolean |  |
| `spawn_reflection_next_fight` | Number | Event Penalty: Spawns dark clones/reflections of the party in the next combat encounter. |
| `spawn_unit_next_fight` | Block | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. |
| `spin` | Enum |  |
| `transform_item` | Array |  |
| `trigger_adventure_unlock` | Enum |  |
| `trigger_butterfly_effect` | Number |  |
| `unlock_item_quest` | Enum |  |
| `upgrade_ability` | Enum |  |
| `upgrade_passive` | Enum |  |
| `weight` | Enum | Probability weight for this outcome. |

</details>

