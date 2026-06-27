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
| `distance_to_ally` | Number | The preferred distance (in tiles) to maintain from allies; negative values or 0 disable the preference. | 55 |  |
| `distance_to_character` | Number | The preferred distance (in tiles) to maintain from any character; negative values or 0 disable the preference. | 55 |  |
| `distance_to_enemy` | Number | The preferred distance (in tiles) to maintain from enemies; negative values or 0 disable the preference. | 55 |  |
| `face_closest_enemy` | Number | If nonzero, the character will face the closest enemy. | 55 |  |
| [`preferred_distance`](./Enums.md#enum-preferred_distance) | Variable | The ideal distance to maintain from a target, expressed either as an absolute tile count or relative to movement (e.g., `mov+2`) or reach (`mov+reach`). | 55 |  |
| `total_distance_moved` | Number | The total distance the character has moved, used in movement weight calculations. | 55 |  |
| `accurate_knockback` | Boolean | If true, knockback from attacks is applied accurately (e.g., straight line); if false, knockback may be erratic. | 32 |  |
| `buff_ally` | Number | The number of buffs applied to ally units. | 32 |  |
| `buff_enemy` | Number | The number of buffs applied to enemy units. Negative values may apply debuffs. | 32 |  |
| `buff_self` | Number | The number of buffs applied to the unit itself. Negative values may apply debuffs. | 32 |  |
| `consider_overkill` | Boolean | If true, the AI considers overkill damage when evaluating actions. | 32 |  |
| `consider_secondary_damage` | Boolean | If true, the AI considers secondary damage (e.g., splash) when evaluating actions. | 32 |  |
| `consider_total_damage` | Boolean | If true, the AI considers total damage output (including secondary) when evaluating actions. | 32 |  |
| `damage_ally` | Number | A multiplier for damage dealt to ally units. Negative values reduce damage. | 32 |  |
| `damage_ally_corpse` | Number | The amount of damage dealt to ally corpses. | 32 |  |
| `damage_enemy` | Number | The amount of damage dealt to enemy units. | 32 |  |
| `damage_enemy_corpse` | Number | A multiplier for damage dealt to enemy corpses. | 32 |  |
| `damage_self` | Number | A multiplier for damage dealt to the unit itself. | 32 |  |
| `debuff_ally` | Number | A multiplier for debuffs applied to ally units. | 32 |  |
| `debuff_enemy` | Number | The number of debuffs applied to enemy units. | 32 |  |
| `debuff_self` | Number | A multiplier for debuffs applied to the unit itself. | 32 |  |
| `heal_ally` | Number | The amount of health restored to ally units. | 32 |  |
| `heal_enemy` | Number | The amount of health restored to enemy units. Negative values deal damage. | 32 |  |
| `heal_self` | Number | The amount of health restored to the unit itself. Negative values deal damage. | 32 |  |
| `kill_ally` | Number | The chance (percentage) to instantly kill an ally unit. | 32 |  |
| `kill_enemy` | Variable | The chance (percentage or probability) to instantly kill an enemy unit. | 32 |  |
| [`negative_weight_scale`](./Enums.md#enum-negative_weight_scale) | Enum | A multiplier applied to the weight of negative (penalty) decisions in AI calculations. | 32 |  |
| `revive_ally_corpse` | Number | The chance (percentage) to revive an ally corpse. | 32 |  |
| `revive_enemy_corpse` | Number | The chance (percentage) to revive an enemy corpse. Negative values may cause destruction. | 32 |  |
| `spawn_object` | Number | If non-zero, enables spawning of an object. The value may specify the number of objects. | 32 |  |
| `spawn_object_distance_to_ally` | Variable | The distance offset from ally units for spawned objects. Negative values move closer. | 32 |  |
| `spawn_object_distance_to_enemy` | Variable | The distance offset from enemy units for spawned objects. | 32 |  |
| [`spend_mana_scale`](./Enums.md#enum-spend_mana_scale) | Enum | A multiplier applied to mana cost when making decisions. | 32 |  |
| `flat_cast_bonus` | Number | A flat bonus added to the AI's cast chance evaluation. | 5 |  |
| `randomness` | Number | The amount of randomness added to AI decision-making to avoid predictability. | 5 |  |
| `cap_distance_to_ally` | Number | The maximum distance the AI will maintain from ally units. | 4 |  |
| `simple` | Boolean | If true, the AI uses simplified decision-making logic. | 3 |  |
| `consider_aoe` | Boolean | If true, the AI considers area-of-effect damage when evaluating actions. | 3 |  |
| `danger_avoidance` | Variable | A weight multiplier for the AI's tendency to avoid dangerous positions. | 3 |  |
| `distance_to_aggro_target` | Number | The preferred distance the AI tries to maintain from its aggro target. Negative values indicate behind. | 3 |  |
| `distance_to_corpse` | Variable | The preferred distance the AI tries to maintain from corpses. Negative values indicate moving towards. | 3 |  |
| `cap_distance_to_enemy` | Number | The maximum distance the AI will maintain from enemy units. | 2 |  |
| `distance_to_water` | Variable | The preferred distance the AI tries to maintain from water tiles. Negative values indicate moving towards. | 2 |  |
| `face_aggro_target` | Number | A weight multiplier for the AI's tendency to face its aggro target. | 2 |  |
| `spawn_object_preferred_distance` | Number | The preferred distance from the unit at which objects are spawned. | 2 |  |
| `cap_distance_to_character` | Number | The maximum distance the AI will maintain from any character (ally or enemy). | 1 |  |
| `cap_total_distance_moved` | Number | The maximum number of tiles a unit can move before its movement is capped. | 1 |  |
| `consider_aggro_target_enemy` | Boolean | If true, the AI considers the aggro target when determining movement or attack behavior. | 1 |  |
| `count_nomove_in_eval` | Boolean | If true, the evaluation of a move includes the option of not moving. | 1 |  |
| `distance_to_center` | Number | The distance in tiles from the current position to the map center for AI evaluation. | 1 |  |
| [`exclude_characters_tagged`](./Enums.md#enum-exclude_characters_tagged) | Enum | Specifies a tag; characters with this tag are excluded from AI behavior targeting. | 1 |  |
| `face_camera` | Boolean | If true, the spawned unit always faces the camera. | 1 |  |
| `lava` | Number | A weight or priority value for preferring lava tiles in AI movement decisions. | 1 |  |
| `tall_grass` | Number | A weight or priority value for preferring tall grass tiles in AI movement decisions. | 1 |  |

</details>

---

