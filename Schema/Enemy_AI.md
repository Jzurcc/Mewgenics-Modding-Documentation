# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Enums.md#enum-mathequation).

## Enemy AI

### Context: `ROOT`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `distance_to_ally` | Number | `1, 0, -1` |  |
| `distance_to_character` | Number | `1, 0, -1` |  |
| `distance_to_enemy` | Number | `1, 0, -1` |  |
| `face_closest_enemy` | Number | `0, 1` |  |
| `preferred_distance` | Number | `0, mov, mov+5` |  |
| `total_distance_moved` | Number | `-0.01, 0.01, -1` |  |
| `accurate_knockback` | Boolean | `false` |  |
| `buff_ally` | Number | `0, 1, 10` |  |
| `buff_enemy` | Number | `1, 0, -1` |  |
| `buff_self` | Number | `0, -1` |  |
| `consider_overkill` | Boolean | `false, true` |  |
| `consider_secondary_damage` | Boolean | `false, true` |  |
| `consider_total_damage` | Boolean | `false, true` |  |
| `damage_ally` | Number | `1, 0, -1` |  |
| `damage_ally_corpse` | Number | `1, 100, 0` |  |
| `damage_enemy` | Number | `0, 1, 100` |  |
| `damage_enemy_corpse` | Number | `1, 100, 0` |  |
| `damage_self` | Number | `-0.1, 0, -1` |  |
| `debuff_ally` | Number | `1, 0, -1` |  |
| `debuff_enemy` | Number | `0, 1, 100` |  |
| `debuff_self` | Number | `-0.1, 0, -1` |  |
| `heal_ally` | Number | `0, 1, 100` |  |
| `heal_enemy` | Number | `1, 0, -1` |  |
| `heal_self` | Number | `-100, 0, -1` |  |
| `kill_ally` | Number | `40, 0` |  |
| `kill_enemy` | [`Enum/String`](./Enums.md#enum-kill_enemy) | `.2, 50, 0` |  |
| `negative_weight_scale` | [`Enum/String`](./Enums.md#enum-negative_weight_scale) | `.99` |  |
| `revive_ally_corpse` | Number | `0, 1, 100` |  |
| `revive_enemy_corpse` | Number | `1, 0, -1` |  |
| `spawn_object` | Number | `0, 1` |  |
| `spawn_object_distance_to_ally` | [`Enum/String`](./Enums.md#enum-spawn_object_distance_to_ally) | `.0001, 0, -.01` |  |
| `spawn_object_distance_to_enemy` | Number | `1, 0, -.01` |  |
| `spend_mana_scale` | [`Enum/String`](./Enums.md#enum-spend_mana_scale) | `.99` |  |
| `flat_cast_bonus` | Number | `99999` |  |
| `randomness` | Number | `6, 50, 4` |  |
| `cap_distance_to_ally` | Number | `7, 2, 4` |  |
| `consider_aoe` | Boolean | `false, true` |  |
| `danger_avoidance` | Number | `1000, 20, .1` |  |
| `distance_to_aggro_target` | Number | `-10, -1` |  |
| `distance_to_corpse` | Number | `0, -100, -.1` |  |
| `simple` | Boolean | `true` |  |
| `cap_distance_to_enemy` | Number | `2, 5` |  |
| `distance_to_water` | [`Enum/String`](./Enums.md#enum-distance_to_water) | `-.0001, -1` |  |
| `face_aggro_target` | Number | `10, 1` |  |
| `spawn_object_preferred_distance` | Number | `5, 4` |  |
| `cap_distance_to_character` | Number | `2` |  |
| `cap_total_distance_moved` | Number | `1` |  |
| `consider_aggro_target_enemy` | Boolean | `true` |  |
| `count_nomove_in_eval` | Boolean | `false` |  |
| `distance_to_center` | Number | `-1` |  |
| `exclude_characters_tagged` | [`Enum/String`](./Enums.md#enum-exclude_characters_tagged) | `siren` |  |
| `face_camera` | Number | `1000` |  |
| `lava` | Number | `5` |  |
| `tall_grass` | Number | `5` |  |

</details>

---

