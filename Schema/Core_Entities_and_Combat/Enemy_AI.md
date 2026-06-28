---
title: "Enemy AI Schema"
description: "Defines behavior trees and targeting priorities for the AI."
---

# Enemy AI Schema

## Overview
> [!NOTE]
> This schema acts as the brain for enemies. It assigns weights to different actions (like attacking vs moving) so the engine can determine the best move.

## Usage Example
Here is a real example of this object being defined in the game's data:
```gon
default {
    damage_ally -1
    damage_enemy 1
    heal_ally 1
    heal_enemy -1
    
    kill_enemy 0
    kill_ally  0
    
    debuff_ally -1
    buff_ally 1
    debuff_enemy 1
    buff_enemy -1
    
    damage_self -0.1
    heal_self 0
    buff_self 0
    debuff_self -0.1
    
    damage_ally_corpse 0
    damage_enemy_corpse 0
    revive_ally_corpse 1
    revive_enemy_corpse -1
    
    spawn_object 1
    spawn_object_distance_to_enemy -.01
    spawn_object_distance_to_ally .0001
    
    negative_weight_scale .99
    spend_mana_scale .99
    
    consider_total_damage true
    consider_secondary_damage true
    accurate_knockback false
    consider_overkill true
}
```

## Associated Directory Files
To see extracted instances of this schema in the base game, refer to:
- [`Enemy_AI.md`](../../Directory/Enemies_and_Combat/Enemy_AI.md)

---



This document is an exhaustive, auto-generated dictionary of `.gon` properties relevant to this subsystem. While the overview above provides high-level context, you may still need to infer exact engine execution rules through testing or context clues.

## Enemy AI

> **Associated Files:** `data/ai_presets/`


### Object: `ROOT`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 87

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `distance_to_ally` | Float | The preferred distance (in tiles) to maintain from allies; negative values or 0 disable the preference. | 55 | `-.1`<br>`-1`<br>`0` |
| `distance_to_character` | Number | The preferred distance (in tiles) to maintain from any character; negative values or 0 disable the preference. | 55 | `-1`<br>`0`<br>`1` |
| `distance_to_enemy` | Float | The preferred distance (in tiles) to maintain from enemies; negative values or 0 disable the preference. | 55 | `-.01`<br>`-.5`<br>`-1` |
| `face_closest_enemy` | Number | If nonzero, the character will face the closest enemy. | 55 | `0`<br>`1` |
| `preferred_distance` | Integer | The ideal distance to maintain from a target, expressed either as an absolute tile count or relative to movement (e.g., `mov+2`) or reach (`mov+reach`). | 55 | `0`<br>`1`<br>`2` |
| `total_distance_moved` | Float | The total distance the character has moved, used in movement weight calculations. | 55 | `-0.001`<br>`-0.01`<br>`-1` |
| `accurate_knockback` | Boolean | If true, knockback from attacks is applied accurately (e.g., straight line); if false, knockback may be erratic. | 32 | `false` |
| `buff_ally` | Number | The number of buffs applied to ally units. | 32 | `0`<br>`1`<br>`10` |
| `buff_enemy` | Number | The number of buffs applied to enemy units. Negative values may apply debuffs. | 32 | `-1`<br>`-100`<br>`0` |
| `buff_self` | Number | The number of buffs applied to the unit itself. Negative values may apply debuffs. | 32 | `-1`<br>`0` |
| `consider_overkill` | Boolean | If true, the AI considers overkill damage when evaluating actions. | 32 | `false`<br>`true` |
| `consider_secondary_damage` | Boolean | If true, the AI considers secondary damage (e.g., splash) when evaluating actions. | 32 | `false`<br>`true` |
| `consider_total_damage` | Boolean | If true, the AI considers total damage output (including secondary) when evaluating actions. | 32 | `false`<br>`true` |
| `damage_ally` | Float | A multiplier for damage dealt to ally units. Negative values reduce damage. | 32 | `-1`<br>`-100`<br>`.5` |
| `damage_ally_corpse` | Number | The amount of damage dealt to ally corpses. | 32 | `0`<br>`1`<br>`100` |
| `damage_enemy` | Number | The amount of damage dealt to enemy units. | 32 | `0`<br>`1`<br>`100` |
| `damage_enemy_corpse` | Float | A multiplier for damage dealt to enemy corpses. | 32 | `.1`<br>`0`<br>`0.1` |
| `damage_self` | Float | A multiplier for damage dealt to the unit itself. | 32 | `-0.1`<br>`-1`<br>`-1.1` |
| `debuff_ally` | Float | A multiplier for debuffs applied to ally units. | 32 | `-1`<br>`-100`<br>`.5` |
| `debuff_enemy` | Number | The number of debuffs applied to enemy units. | 32 | `0`<br>`1`<br>`100` |
| `debuff_self` | Float | A multiplier for debuffs applied to the unit itself. | 32 | `-0.1`<br>`-1`<br>`-1.1` |
| `heal_ally` | Number | The amount of health restored to ally units. | 32 | `0`<br>`1`<br>`10` |
| `heal_enemy` | Number | The amount of health restored to enemy units. Negative values deal damage. | 32 | `-1`<br>`-100`<br>`0` |
| `heal_self` | Number | The amount of health restored to the unit itself. Negative values deal damage. | 32 | `-1`<br>`-100`<br>`0` |
| `kill_ally` | Number | The chance (percentage) to instantly kill an ally unit. | 32 | `0`<br>`40` |
| `kill_enemy` | Float | The chance (percentage or probability) to instantly kill an enemy unit. | 32 | `.2`<br>`0`<br>`100` |
| `negative_weight_scale` | Enum | A multiplier applied to the weight of negative (penalty) decisions in AI calculations. | 32 | `.99` |
| `revive_ally_corpse` | Number | The chance (percentage) to revive an ally corpse. | 32 | `0`<br>`1`<br>`10` |
| `revive_enemy_corpse` | Number | The chance (percentage) to revive an enemy corpse. Negative values may cause destruction. | 32 | `-1`<br>`-100`<br>`0` |
| `spawn_object` | Number | If non-zero, enables spawning of an object. The value may specify the number of objects. | 32 | `0`<br>`1` |
| `spawn_object_distance_to_ally` | Float | The distance offset from ally units for spawned objects. Negative values move closer. | 32 | `-.0001`<br>`-.01`<br>`.0001` |
| `spawn_object_distance_to_enemy` | Float | The distance offset from enemy units for spawned objects. | 32 | `-.01`<br>`0`<br>`1` |
| `spend_mana_scale` | Enum | A multiplier applied to mana cost when making decisions. | 32 | `.99` |
| `flat_cast_bonus` | Number | A flat bonus added to the AI's cast chance evaluation. | 5 | `99999` |
| `randomness` | Number | The amount of randomness added to AI decision-making to avoid predictability. | 5 | `4`<br>`50`<br>`6` |
| `cap_distance_to_ally` | Number | The maximum distance the AI will maintain from ally units. | 4 | `2`<br>`4`<br>`7` |
| `simple` | Boolean | If true, the AI uses simplified decision-making logic. | 3 | `true` |
| `consider_aoe` | Boolean | If true, the AI considers area-of-effect damage when evaluating actions. | 3 | `false`<br>`true` |
| `danger_avoidance` | Float | A weight multiplier for the AI's tendency to avoid dangerous positions. | 3 | `.1`<br>`1000`<br>`20` |
| `distance_to_aggro_target` | Number | The preferred distance the AI tries to maintain from its aggro target. Negative values indicate behind. | 3 | `-1`<br>`-10` |
| `distance_to_corpse` | Float | The preferred distance the AI tries to maintain from corpses. Negative values indicate moving towards. | 3 | `-.1`<br>`-100`<br>`0` |
| `cap_distance_to_enemy` | Number | The maximum distance the AI will maintain from enemy units. | 2 | `2`<br>`5` |
| `distance_to_water` | Float | The preferred distance the AI tries to maintain from water tiles. Negative values indicate moving towards. | 2 | `-.0001`<br>`-1` |
| `face_aggro_target` | Number | A weight multiplier for the AI's tendency to face its aggro target. | 2 | `1`<br>`10` |
| `spawn_object_preferred_distance` | Number | The preferred distance from the unit at which objects are spawned. | 2 | `4`<br>`5` |
| `face_camera` | Boolean | If true, the spawned unit always faces the camera. | 1 | `1000`<br>`true` |
| `lava` | Number | A weight or priority value for preferring lava tiles in AI movement decisions. | 1 | `5` |
| `tall_grass` | Number | A weight or priority value for preferring tall grass tiles in AI movement decisions. | 1 | `5` |
| `cap_distance_to_character` | Number | The maximum distance the AI will maintain from any character (ally or enemy). | 1 | `2` |
| `cap_total_distance_moved` | Number | The maximum number of tiles a unit can move before its movement is capped. | 1 | `1` |
| `consider_aggro_target_enemy` | Boolean | If true, the AI considers the aggro target when determining movement or attack behavior. | 1 | `true` |
| `count_nomove_in_eval` | Boolean | If true, the evaluation of a move includes the option of not moving. | 1 | `false` |
| `distance_to_center` | Number | The distance in tiles from the current position to the map center for AI evaluation. | 1 | `-1` |
| [`exclude_characters_tagged`](../Reference_and_Meta/Enums.md#enum-exclude_characters_tagged) | Enum | Specifies a tag; characters with this tag are excluded from AI behavior targeting. | 1 | `siren` |

</details>


---