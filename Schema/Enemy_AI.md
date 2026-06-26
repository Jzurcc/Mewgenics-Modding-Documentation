# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Enemy AI

> **Associated Files:** `data/ai_presets/`


### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 55

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `distance_to_ally` | Number | Examples: `1, -1, 0` | 110 |  |
| `distance_to_character` | Number | Examples: `1, -1, 0` | 110 |  |
| `distance_to_enemy` | Number | Examples: `1, -1, 0` | 110 |  |
| `face_closest_enemy` | Number | Examples: `1, 0` | 110 |  |
| [`preferred_distance`](./Enums.md#enum-preferred_distance) | Mixed | Examples: `mov+5, 0, mov` | 110 |  |
| `total_distance_moved` | Number | Examples: `-1, 0.01, -0.01` | 110 |  |
| `accurate_knockback` | Boolean | Examples: `false` | 64 |  |
| `buff_ally` | Number | Examples: `1, 0, 10` | 64 |  |
| `buff_enemy` | Number | Examples: `1, -1, 0` | 64 |  |
| `buff_self` | Number | Examples: `-1, 0` | 64 |  |
| `consider_overkill` | Boolean | Examples: `false, true` | 64 |  |
| `consider_secondary_damage` | Boolean | Examples: `false, true` | 64 |  |
| `consider_total_damage` | Boolean | Examples: `false, true` | 64 |  |
| `damage_ally` | Number | Examples: `1, -1, 0` | 64 |  |
| `damage_ally_corpse` | Number | Examples: `1, 0, 100` | 64 |  |
| `damage_enemy` | Number | Examples: `1, 0, 100` | 64 |  |
| `damage_enemy_corpse` | Number | Examples: `1, 0, 100` | 64 |  |
| `damage_self` | Number | Examples: `-1, -0.1, 0` | 64 |  |
| `debuff_ally` | Number | Examples: `1, -1, 0` | 64 |  |
| `debuff_enemy` | Number | Examples: `1, 0, 100` | 64 |  |
| `debuff_self` | Number | Examples: `-1, -0.1, 0` | 64 |  |
| `heal_ally` | Number | Examples: `1, 0, 100` | 64 |  |
| `heal_enemy` | Number | Examples: `1, -1, 0` | 64 |  |
| `heal_self` | Number | Examples: `-100, -1, 0` | 64 |  |
| `kill_ally` | Number | Examples: `40, 0` | 64 |  |
| `kill_enemy` | Mixed | Examples: `50, 0, .2` | 64 |  |
| [`negative_weight_scale`](./Enums.md#enum-negative_weight_scale) | Enum | Examples: `.99` | 64 |  |
| `revive_ally_corpse` | Number | Examples: `1, 0, 100` | 64 |  |
| `revive_enemy_corpse` | Number | Examples: `1, -1, 0` | 64 |  |
| `spawn_object` | Number | Examples: `1, 0` | 64 |  |
| `spawn_object_distance_to_ally` | Mixed | Examples: `.0001, 0, -.01` | 64 |  |
| `spawn_object_distance_to_enemy` | Mixed | Examples: `1, 0, -.01` | 64 |  |
| [`spend_mana_scale`](./Enums.md#enum-spend_mana_scale) | Enum | Examples: `.99` | 64 |  |
| `flat_cast_bonus` | Number | Examples: `99999` | 10 |  |
| `randomness` | Number | Examples: `50, 4, 6` | 10 |  |
| `cap_distance_to_ally` | Number | Examples: `4, 2, 7` | 8 |  |
| `simple` | Boolean | Examples: `true` | 8 |  |
| `consider_aoe` | Boolean | Examples: `false, true` | 6 |  |
| `danger_avoidance` | Mixed | Examples: `.1, 20, 1000` | 6 |  |
| `distance_to_aggro_target` | Number | Examples: `-10, -1` | 6 |  |
| `distance_to_corpse` | Mixed | Examples: `-100, 0, -.1` | 6 |  |
| `cap_distance_to_enemy` | Number | Examples: `2, 5` | 4 |  |
| `distance_to_water` | Mixed | Examples: `-1, -.0001` | 4 |  |
| `face_aggro_target` | Number | Examples: `1, 10` | 4 |  |
| `spawn_object_preferred_distance` | Number | Examples: `4, 5` | 4 |  |
| `cap_distance_to_character` | Number | Examples: `2` | 2 |  |
| `cap_total_distance_moved` | Number | Examples: `1` | 2 |  |
| `consider_aggro_target_enemy` | Boolean | Examples: `true` | 2 |  |
| `count_nomove_in_eval` | Boolean | Examples: `false` | 2 |  |
| `distance_to_center` | Number | Examples: `-1` | 2 |  |
| [`exclude_characters_tagged`](./Enums.md#enum-exclude_characters_tagged) | Enum | Examples: `siren` | 2 |  |
| `face_camera` | Number | Examples: `1000` | 2 |  |
| `lava` | Number | Examples: `5` | 2 |  |
| `tall_grass` | Number | Examples: `5` | 2 |  |

</details>

---

