# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.



## Enemy AI

> **Associated Files:** `data/ai_presets/`

### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 55

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| `distance_to_ally` | Float |  | 55 |
| `distance_to_character` | Integer |  | 55 |
| `distance_to_enemy` | Float |  | 55 |
| `face_closest_enemy` | Integer |  | 55 |
| `preferred_distance` | Equation |  | 55 |
| `total_distance_moved` | Float |  | 55 |
| `accurate_knockback` | Boolean |  | 32 |
| `buff_ally` | Integer |  | 32 |
| `buff_enemy` | Integer |  | 32 |
| `buff_self` | Integer |  | 32 |
| `consider_overkill` | Boolean |  | 32 |
| `consider_secondary_damage` | Boolean |  | 32 |
| `consider_total_damage` | Boolean |  | 32 |
| `damage_ally` | Float |  | 32 |
| `damage_ally_corpse` | Integer |  | 32 |
| `damage_enemy` | Integer |  | 32 |
| `damage_enemy_corpse` | Float |  | 32 |
| `damage_self` | Integer |  | 32 |
| `debuff_ally` | Float |  | 32 |
| `debuff_enemy` | Integer |  | 32 |
| `debuff_self` | Integer |  | 32 |
| `heal_ally` | Integer |  | 32 |
| `heal_enemy` | Integer |  | 32 |
| `heal_self` | Integer |  | 32 |
| `kill_ally` | Integer |  | 32 |
| `kill_enemy` | Float |  | 32 |
| `negative_weight_scale` | Float |  | 32 |
| `revive_ally_corpse` | Integer |  | 32 |
| `revive_enemy_corpse` | Integer |  | 32 |
| `spawn_object` | Integer |  | 32 |
| `spawn_object_distance_to_ally` | Float |  | 32 |
| `spawn_object_distance_to_enemy` | Float |  | 32 |
| `spend_mana_scale` | Float |  | 32 |
| `flat_cast_bonus` | Integer |  | 5 |
| `randomness` | Integer |  | 5 |
| `cap_distance_to_ally` | Integer |  | 4 |
| `consider_aoe` | Boolean |  | 3 |
| `danger_avoidance` | Float |  | 3 |
| `distance_to_aggro_target` | Integer |  | 3 |
| `distance_to_corpse` | Float |  | 3 |
| `simple` | Boolean |  | 3 |
| `cap_distance_to_enemy` | Integer |  | 2 |
| [`distance_to_water`](./Enums.md#enum-distance_to_water) | Float |  | 2 |
| `face_aggro_target` | Integer |  | 2 |
| `spawn_object_preferred_distance` | Integer |  | 2 |
| `cap_distance_to_character` | Integer |  | 1 |
| `cap_total_distance_moved` | Integer |  | 1 |
| `consider_aggro_target_enemy` | Boolean |  | 1 |
| `count_nomove_in_eval` | Boolean |  | 1 |
| `distance_to_center` | Integer |  | 1 |
| [`exclude_characters_tagged`](./Enums.md#enum-exclude_characters_tagged) | Enum |  | 1 |
| `face_camera` | Integer |  | 1 |
| `lava` | Integer |  | 1 |
| `tall_grass` | Integer |  | 1 |

</details>

---

