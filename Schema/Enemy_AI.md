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
| `distance_to_ally` | Number | Examples: `1, -1, 0` | 55 |  |
| `distance_to_character` | Number | Examples: `1, -1, 0` | 55 |  |
| `distance_to_enemy` | Number | Examples: `1, -1, 0` | 55 |  |
| `face_closest_enemy` | Number | Examples: `1, 0` | 55 |  |
| [`preferred_distance`](./Enums.md#enum-preferred_distance) | Variable | Examples: `mov+5, 0, mov` | 55 |  |
| `total_distance_moved` | Number | Examples: `-1, 0.01, -0.01` | 55 |  |
| `accurate_knockback` | Boolean | Examples: `false` | 32 |  |
| `buff_ally` | Number | Examples: `1, 0, 10` | 32 |  |
| `buff_enemy` | Number | Examples: `1, -1, 0` | 32 |  |
| `buff_self` | Number | Examples: `-1, 0` | 32 |  |
| `consider_overkill` | Boolean | Examples: `false, true` | 32 |  |
| `consider_secondary_damage` | Boolean | Examples: `false, true` | 32 |  |
| `consider_total_damage` | Boolean | Examples: `false, true` | 32 |  |
| `damage_ally` | Number | Examples: `1, -1, 0` | 32 |  |
| `damage_ally_corpse` | Number | Examples: `1, 0, 100` | 32 |  |
| `damage_enemy` | Number | Examples: `1, 0, 100` | 32 |  |
| `damage_enemy_corpse` | Number | Examples: `1, 0, 100` | 32 |  |
| `damage_self` | Number | Examples: `-1, -0.1, 0` | 32 |  |
| `debuff_ally` | Number | Examples: `1, -1, 0` | 32 |  |
| `debuff_enemy` | Number | Examples: `1, 0, 100` | 32 |  |
| `debuff_self` | Number | Examples: `-1, -0.1, 0` | 32 |  |
| `heal_ally` | Number | Examples: `1, 0, 100` | 32 |  |
| `heal_enemy` | Number | Examples: `1, -1, 0` | 32 |  |
| `heal_self` | Number | Examples: `-100, -1, 0` | 32 |  |
| `kill_ally` | Number | Examples: `40, 0` | 32 |  |
| `kill_enemy` | Variable | Examples: `50, 0, .2` | 32 |  |
| [`negative_weight_scale`](./Enums.md#enum-negative_weight_scale) | Enum | Examples: `.99` | 32 |  |
| `revive_ally_corpse` | Number | Examples: `1, 0, 100` | 32 |  |
| `revive_enemy_corpse` | Number | Examples: `1, -1, 0` | 32 |  |
| `spawn_object` | Number | Examples: `1, 0` | 32 |  |
| `spawn_object_distance_to_ally` | Variable | Examples: `.0001, 0, -.01` | 32 |  |
| `spawn_object_distance_to_enemy` | Variable | Examples: `1, 0, -.01` | 32 |  |
| [`spend_mana_scale`](./Enums.md#enum-spend_mana_scale) | Enum | Examples: `.99` | 32 |  |
| `flat_cast_bonus` | Number | Examples: `99999` | 5 |  |
| `randomness` | Number | Examples: `50, 4, 6` | 5 |  |
| `cap_distance_to_ally` | Number | Examples: `4, 2, 7` | 4 |  |
| `simple` | Boolean | Examples: `true` | 3 |  |
| `consider_aoe` | Boolean | Examples: `false, true` | 3 |  |
| `danger_avoidance` | Variable | Examples: `.1, 20, 1000` | 3 |  |
| `distance_to_aggro_target` | Number | Examples: `-10, -1` | 3 |  |
| `distance_to_corpse` | Variable | Examples: `-100, 0, -.1` | 3 |  |
| `cap_distance_to_enemy` | Number | Examples: `2, 5` | 2 |  |
| `distance_to_water` | Variable | Examples: `-1, -.0001` | 2 |  |
| `face_aggro_target` | Number | Examples: `1, 10` | 2 |  |
| `spawn_object_preferred_distance` | Number | Examples: `4, 5` | 2 |  |
| `cap_distance_to_character` | Number | Examples: `2` | 1 |  |
| `cap_total_distance_moved` | Number | Examples: `1` | 1 |  |
| `consider_aggro_target_enemy` | Boolean | Examples: `true` | 1 |  |
| `count_nomove_in_eval` | Boolean | Examples: `false` | 1 |  |
| `distance_to_center` | Number | Examples: `-1` | 1 |  |
| [`exclude_characters_tagged`](./Enums.md#enum-exclude_characters_tagged) | Enum | Examples: `siren` | 1 |  |
| `face_camera` | Boolean | Examples: `1000` | 1 |  |
| `lava` | Number | Examples: `5` | 1 |  |
| `tall_grass` | Number | Examples: `5` | 1 |  |

</details>

---

