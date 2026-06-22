# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Math_Equations.md).

## Enemy AI

> **Associated Files:** `data/ai_presets/`


### Context: `ROOT` (55 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `distance_to_ally` | Number |  | 55 |
| `distance_to_character` | Number |  | 55 |
| `distance_to_enemy` | Number |  | 55 |
| `face_closest_enemy` | Number |  | 55 |
| `preferred_distance` | Equation |  | 55 |
| `total_distance_moved` | Number |  | 55 |
| `accurate_knockback` | Boolean |  | 32 |
| `buff_ally` | Number |  | 32 |
| `buff_enemy` | Number |  | 32 |
| `buff_self` | Number |  | 32 |
| `consider_overkill` | Boolean |  | 32 |
| `consider_secondary_damage` | Boolean |  | 32 |
| `consider_total_damage` | Boolean |  | 32 |
| `damage_ally` | Number |  | 32 |
| `damage_ally_corpse` | Number |  | 32 |
| `damage_enemy` | Number |  | 32 |
| `damage_enemy_corpse` | Number |  | 32 |
| `damage_self` | Number |  | 32 |
| `debuff_ally` | Number |  | 32 |
| `debuff_enemy` | Number |  | 32 |
| `debuff_self` | Number |  | 32 |
| `heal_ally` | Number |  | 32 |
| `heal_enemy` | Number |  | 32 |
| `heal_self` | Number |  | 32 |
| `kill_ally` | Number |  | 32 |
| `kill_enemy` | Number |  | 32 |
| [`negative_weight_scale`](./Enums.md#enum-negative_weight_scale) | Enum |  | 32 |
| `revive_ally_corpse` | Number |  | 32 |
| `revive_enemy_corpse` | Number |  | 32 |
| `spawn_object` | Number |  | 32 |
| [`spawn_object_distance_to_ally`](./Enums.md#enum-spawn_object_distance_to_ally) | Enum |  | 32 |
| `spawn_object_distance_to_enemy` | Enum |  | 32 |
| [`spend_mana_scale`](./Enums.md#enum-spend_mana_scale) | Enum |  | 32 |
| `flat_cast_bonus` | Number |  | 5 |
| `randomness` | Number |  | 5 |
| `cap_distance_to_ally` | Number |  | 4 |
| `consider_aoe` | Boolean |  | 3 |
| `danger_avoidance` | Number |  | 3 |
| `distance_to_aggro_target` | Number |  | 3 |
| `distance_to_corpse` | Enum |  | 3 |
| `simple` | Boolean |  | 3 |
| `cap_distance_to_enemy` | Number |  | 2 |
| [`distance_to_water`](./Enums.md#enum-distance_to_water) | Number |  | 2 |
| `face_aggro_target` | Number |  | 2 |
| `spawn_object_preferred_distance` | Number |  | 2 |
| `cap_distance_to_character` | Number |  | 1 |
| `cap_total_distance_moved` | Number |  | 1 |
| `consider_aggro_target_enemy` | Boolean |  | 1 |
| `count_nomove_in_eval` | Boolean |  | 1 |
| `distance_to_center` | Number |  | 1 |
| [`exclude_characters_tagged`](./Enums.md#enum-exclude_characters_tagged) | Enum |  | 1 |
| `face_camera` | Number |  | 1 |
| `lava` | Number |  | 1 |
| `tall_grass` | Number |  | 1 |

</details>

---

