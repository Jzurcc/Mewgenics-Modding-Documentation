---
title: "Damaging Keys Schema"
description: "Hooks for calculating and modifying damage."
---

# Damaging Keys Schema

## Overview
> [!NOTE]
> This schema contains all properties relating to how damage is calculated, mitigated, and applied by the engine.

## Usage Example
Here is a real example of this object being defined in the game's data:
```gon
PhysicalDamage {
    damage_type physical
    ignores_armor true
    lifesteal 0.5
}
```

---



## Engine: Damaging Keys

This document defines the shared schema for all Damage Instance blocks (`damage_instance`, `splash_damage`, `self_damage`, `bonk_damage`). Each of these blocks configures a discrete hit: its base damage, element, knockback, accuracy, and any on-hit effects.

> **Referenced by:** [`damage_instance` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-damage_instance), [`self_damage` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-self_damage), [`splash_damage` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-splash_damage), [`bonk_damage` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-bonk_damage), [`damage_instance` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-damage_instance), [`damage_instance` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-damage_instance)

### Valid Property Keys

<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 2346 | `{ . . . }` |
| [`spell`](../Reference_and_Meta/Enums.md#enum-spell) | Enum | Specifies the spell ability to use as a reaction. | 569 | `MCHadouken` |
| [`self_damage`](../Reference_and_Meta/Miscellaneous.md#object-self_damage) | Boolean / Integer / Object  | Defines damage or effects applied to the caster when using the ability. | 271 | `{ . . . }`<br>`1`<br>`10`<br>`100%` |
| [`elements`](../Reference_and_Meta/Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 414 | `[`<br>`[Heat Fire]` |
| [`str`](../Reference_and_Meta/Enums.md#enum-str) | Enum / Integer  | The Strength stat value or modifier. | 335 | `-1`<br>`-2`<br>`-3` |
| [`knockback`](../Reference_and_Meta/Enums.md#enum-knockback) | Enum / Integer  | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 314 | `"ceil(X*.25/5)"`<br>`-10`<br>`-2` |
| [`durability`](../Reference_and_Meta/Arrays.md#array-durability) | Array / Integer  | The amount of durability consumed by this ability or required for its use. | 182 | `0`<br>`1`<br>`10` |
| `ai_base_score` | Integer | The base priority score the AI assigns to using this damage instance, with higher values indicating greater preference. | 257 | `-99999`<br>`-999999`<br>`1` |
| `heal` | Enum / Equation | An equation string that determines the amount of health restored by this damage instance. | 168 | `"ceil(X*item_aux/100)"`<br>`0`<br>`1` |
| `cant_miss` | Boolean | If true, the damage instance always hits its target regardless of accuracy or evasion. | 131 | `true` |
| `incidentally_collects_pickups` | Boolean | If true, the damage instance collects nearby pickups (e.g., coins, items) as part of its effect. | 103 | `false`<br>`true` |
| `melee` | Enum | The melee attack type or category. | 131 | `Melee` |
| `status_spell` | Variable | The category for spells that apply status effects. | 97 ||
| [`custom_additional_ai_weight`](../Reference_and_Meta/Enums.md#enum-custom_additional_ai_weight) | Enum | A string identifier for a custom AI weighting condition that modifies the AI's scoring for this damage instance. | 83 | `avoid_redundant_debuffs`<br>`avoid_redundant_debuffs_strict`<br>`avoid_target_map_top` |
| [`splash_damage`](../Reference_and_Meta/Miscellaneous.md#object-splash_damage) | Object  | Defines additional damage or effects applied to nearby targets around the primary target. | 35 | `{ . . . }` |
| `piercing` | Boolean | If true, the damage instance ignores armor or damage reduction effects on the target. | 67 | `true` |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 2166 | `{ . . . }` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 836 | `[attack move spell]`<br>`attack`<br>`battle` |
| `makes_contact` | Boolean | If true, the damage instance is considered a contact hit, triggering contact-based passives on both the attacker and target. | 47 | `false`<br>`true` |
| [`level`](../Reference_and_Meta/Enums.md#enum-level) | Enum | The level or quest identifier to load. | 67 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| `blocked_damage` | Equation | An equation string that calculates the amount of damage that can be blocked or reduced by the target's defenses. | 24 | `"(3+bonus_melee_ability_damage)*2"`<br>`3+bonus_melee_ability_damage`<br>`5` |
| `raw_damage` | Equation | An equation string that calculates the base damage before any modifiers or bonuses are applied. | 22 | `"(con+1)/2"`<br>`"8-X"`<br>`"max((X-1)*2, 0)"` |
| `characters` | Variable | A list of characters or character references. | 18 ||
| `crit_chance` | Equation | The chance for the damage instance to critically hit, expressed as a percentage or equation; values above 1 default to 100%. | 24 | `-999999`<br>`.05*X`<br>`.25` |
| `override_trample_damage` | Boolean | If true, this damage instance replaces any default trample damage when the unit passes through an occupied tile. | 17 | `true` |
| `contact_requires_adjacency` | Boolean | If false, contact effects are not restricted to adjacent tiles, allowing contact to trigger at range. | 14 | `false` |
| `ranged` | Boolean | If true, the damage instance is considered a ranged attack, interacting with ranged-specific modifiers and passives. | 18 | `Ranged`<br>`true` |
| `tile_has_no_known_traps` | Variable | A condition that checks if a tile has no known traps. | 9 ||
| `can_revive` | Boolean | If true, the damage instance can revive a downed unit instead of dealing damage. | 8 | `true` |
| `force_play_hit_animation` | Boolean | If true, the hit animation is forced to play regardless of other conditions (e.g., miss or block). | 6 | `true` |
| `show_damage_on_0` | Boolean | If true, the damage number is still displayed even when the resulting damage is zero. | 6 | `true` |
| `avoid_redundant_debuffs_strict` | Variable | A flag to strictly avoid applying redundant debuffs. | 7 ||
| `blocked_multiplier` | Integer | A multiplier applied to blocked damage, increasing the effectiveness of the defensive reduction. | 4 | `2` |
| `item_aux` | Variable | An auxiliary stat for items, often used for extra damage or value. | 22 ||
| [`layer`](../Reference_and_Meta/Enums.md#enum-layer) | Enum | Specifies the layer on which the ability's effect operates (e.g., characters, tiles, gas). | 61 | `2`<br>`all`<br>`characters` |
| `accuracy` | Float | A decimal value (e.g., .5) representing the base hit chance of the damage instance, where 1.0 is guaranteed. | 3 | `.5` |
| `can_collect_pickups` | Boolean | If true, the damage instance can collect pickups from the target's tile as part of its effect. | 3 | `true` |
| `magnetize_favorlineup` | Variable | A condition or effect related to magnetizing and favor lineup. | 3 ||
| `non_lethal` | Boolean | If true, the damage instance cannot reduce a unit below 1 HP, preventing kills. | 3 | `true` |
| `spell_cost` | Variable | The cost of a spell, usually in mana. | 3 ||
| `tiles` | Variable | A collection of tiles. | 3 ||
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 1684 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| `can_instapop` | Boolean | If false, the ability cannot instantly kill or remove the target, often used for non-lethal effects. | 3 | `false` |
| `disallow_modifications` | Boolean | If true, the damage instance cannot be modified by external effects (e.g., passives, statuses). | 2 | `true` |
| `force_no_contact` | Boolean | If true, the damage instance does not trigger contact-based passives even if it would normally be a contact hit. | 3 | `true` |
| `force_no_knockback` | Boolean | If true, the damage instance applies no knockback regardless of any knockback values set. | 2 | `true` |
| `knockblock` | Variable | A property that blocks knockback effects. | 2 ||
| `physical_spell` | Variable | A variable that determines whether an ability is considered a physical spell for mechanics that differentiate between physical and magical attacks. | 4 ||
| `pickups` | Variable | A variable that refers to collectable items or units on the map that can be picked up. | 25 ||
| `raw_heal` | String | An equation string that calculates the base healing amount before any modifiers are applied. | 2 | `"(str+1)/2"`<br>`"100-X"` |
| `self` | Variable | A variable that refers to the unit itself, often used for targeting or self-referential effects. | 67 ||
| `tile_close_to_enemy` | Variable | A variable that prioritizes selecting a tile that is adjacent or very near to an enemy unit. | 5 ||
| `tile_exists` | Variable | A variable that checks for the existence of a specific tile condition, often used to filter targeting. | 4 ||
| `toss_farthest` | Variable | A variable that determines the maximum distance a unit or object can be tossed. | 5 ||
| `two_way_contact` | Boolean | If true, contact effects apply to both the attacker and the target when the damage instance hits. | 2 | `true` |
| [`bonk_damage`](../Reference_and_Meta/Miscellaneous.md#object-bonk_damage) | Object  | Defines damage and effects applied when a dash or move hits a wall or obstacle. | 1 | `{ . . . }` |
| `avoid_redundant_debuffs` | Variable | If true, prevents the application of a debuff that the target already has. | 3 ||
| [`catch`](../Reference_and_Meta/Miscellaneous.md#object-catch) | Object  | An object defining a response option for catching an entity, including stat checks and rewards. | 2 | `{ . . . }` |
| `damage_shield_only` | Boolean | If true, the damage instance only affects damage shields (e.g., barrier effects) and not health directly. | 1 | `true` |
| [`faction`](../Reference_and_Meta/Enums.md#enum-faction) | Enum | Specifies the faction of a spawned unit or projectile, determining its team allegiance and AI behavior. | 570 | `allies`<br>`auto`<br>`birds` |
| `favor_enemy_already_moved` | Variable | A variable that weights targeting towards enemies that have already taken their turn. | 1 ||
| `favor_tile_far_away` | Variable | A variable that weights targeting towards tiles that are far from the unit. | 2 ||
| `final_hit_bonus_damage` | Equation | An equation string that adds bonus damage to the final hit of a multi-hit damage instance. | 1 | `5+bonus_melee_ability_damage` |
| `force_adjacent_and_diagonal_contact` | Boolean | If true, contact effects are forced for both adjacent and diagonal tiles even if not normally triggered. | 1 | `true` |
| `generic_physical` | Variable | A variable indicating a standard physical action without specific special properties. | 2 ||
| `hint_dont_lowgravboost` | Boolean | If true, the damage instance does not receive a damage boost from low gravity tiles. | 1 | `true` |
| [`hit_animation_alt`](../Reference_and_Meta/Enums.md#enum-hit_animation_alt) | Enum | Specifies an alternative hit animation name (e.g., "catch") to play instead of the default on successful hit. | 1 | `catch` |
| `moonhead_punchself` | Variable | A variable used by the Moonhead AI to determine if it should punch itself. | 1 ||
| `moonhead_use_if_cracked` | Variable | A variable used by the Moonhead AI to check if it should use an ability when cracked. | 1 ||
| `must_heal_most_missing_health` | Variable | If true, the unit must target the ally with the highest amount of missing health. | 1 ||
| `must_target_buddy` | Variable | If true, the unit must target its designated buddy. | 4 ||
| `no_coins_on_map` | Variable | If true, the AI behaves as if there are no coins on the map for decision-making. | 1 ||
| `no_redundant_formchange` | Variable | If true, prevents a form change if the unit is already in that form. | 1 ||
| [`status`](../Reference_and_Meta/Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 160 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| `target_closest` | Variable | A variable that causes the AI to select the nearest valid target. | 3 ||
| `target_farthest` | Variable | A variable that causes the AI to select the farthest valid target. | 1 ||
| `teslacoil_priorities` | Variable | A variable defining the targeting priorities for the Teslacoil unit. | 1 ||
| `tile_close_to_enemy_soft` | Variable | A variable that prioritizes tiles near enemies but with softer constraints than the hard version. | 1 ||
| `toss_far` | Variable | A variable that specifies a far distance for tossing a unit or object. | 10 ||
| `toss_towards_bottomleft` | Variable | A variable that specifies the direction of a toss towards the bottom-left of the map. | 1 ||

</details>

### Valid Nested Objects

The following objects all behave as `{Damaging Keys}` containers. Each has its own unique parameters listed below its entry.


---


#### `bonk_damage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 1 | `damage_instance`<br>`spell`<br>`self_damage` |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 2166 | `{ . . . }` |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Equation / Object | Specifies the amount of damage dealt, can be a number or expression. | 1684 | `"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |

</details>


---


#### `damage_instance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2346

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 1731 | `damage_instance`<br>`spell`<br>`self_damage` |
| [`knockback`](../Reference_and_Meta/Enums.md#enum-knockback) | Enum / Integer  | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 314 | `"ceil(X*.25/5)"`<br>`-10`<br>`-2` |
| `ai_base_score` | Integer | The base priority score the AI assigns to using this damage instance, with higher values indicating greater preference. | 257 | `-99999`<br>`-999999`<br>`1` |
| `heal` | Enum / Equation | An equation string that determines the amount of health restored by this damage instance. | 168 | `"ceil(X*item_aux/100)"`<br>`0`<br>`1` |
| `cant_miss` | Boolean | If true, the damage instance always hits its target regardless of accuracy or evasion. | 131 | `true` |
| `incidentally_collects_pickups` | Boolean | If true, the damage instance collects nearby pickups (e.g., coins, items) as part of its effect. | 103 | `false`<br>`true` |
| [`custom_additional_ai_weight`](../Reference_and_Meta/Enums.md#enum-custom_additional_ai_weight) | Enum | A string identifier for a custom AI weighting condition that modifies the AI's scoring for this damage instance. | 83 | `avoid_redundant_debuffs`<br>`avoid_redundant_debuffs_strict`<br>`avoid_target_map_top` |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 2166 | `{ . . . }` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 836 | `[attack move spell]`<br>`attack`<br>`battle` |
| `piercing` | Boolean | If true, the damage instance ignores armor or damage reduction effects on the target. | 67 | `true` |
| `makes_contact` | Boolean | If true, the damage instance is considered a contact hit, triggering contact-based passives on both the attacker and target. | 47 | `false`<br>`true` |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 95 | `1`<br>`2`<br>`3` |
| `blocked_damage` | Equation | An equation string that calculates the amount of damage that can be blocked or reduced by the target's defenses. | 24 | `"(3+bonus_melee_ability_damage)*2"`<br>`3+bonus_melee_ability_damage`<br>`5` |
| `raw_damage` | Enum / Equation | An equation string that calculates the base damage before any modifiers or bonuses are applied. | 22 | `"(con+1)/2"`<br>`"8-X"`<br>`"max((X-1)*2, 0)"` |
| `crit_chance` | Equation | The chance for the damage instance to critically hit, expressed as a percentage or equation; values above 1 default to 100%. | 24 | `-999999`<br>`.05*X`<br>`.25` |
| `override_trample_damage` | Boolean | If true, this damage instance replaces any default trample damage when the unit passes through an occupied tile. | 17 | `true` |
| `contact_requires_adjacency` | Boolean | If false, contact effects are not restricted to adjacent tiles, allowing contact to trigger at range. | 14 | `false` |
| `ranged` | Boolean | If true, the damage instance is considered a ranged attack, interacting with ranged-specific modifiers and passives. | 18 | `Ranged`<br>`true` |
| `can_revive` | Boolean | If true, the damage instance can revive a downed unit instead of dealing damage. | 8 | `true` |
| `show_damage_on_0` | Boolean | If true, the damage number is still displayed even when the resulting damage is zero. | 6 | `true` |
| `force_play_hit_animation` | Boolean | If true, the hit animation is forced to play regardless of other conditions (e.g., miss or block). | 6 | `true` |
| `blocked_multiplier` | Integer | A multiplier applied to blocked damage, increasing the effectiveness of the defensive reduction. | 4 | `2` |
| `accuracy` | Float | A decimal value (e.g., .5) representing the base hit chance of the damage instance, where 1.0 is guaranteed. | 3 | `.5` |
| `can_collect_pickups` | Boolean | If true, the damage instance can collect pickups from the target's tile as part of its effect. | 3 | `true` |
| [`layer`](../Reference_and_Meta/Enums.md#enum-layer) | Enum | Specifies the layer on which the ability's effect operates (e.g., characters, tiles, gas). | 61 | `2`<br>`all`<br>`characters` |
| `can_instapop` | Boolean | If false, the ability cannot instantly kill or remove the target, often used for non-lethal effects. | 3 | `false` |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Equation / Object | Specifies the amount of damage dealt, can be a number or expression. | 1684 | `"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| `disallow_modifications` | Boolean | If true, the damage instance cannot be modified by external effects (e.g., passives, statuses). | 2 | `true` |
| `force_no_contact` | Boolean | If true, the damage instance does not trigger contact-based passives even if it would normally be a contact hit. | 3 | `true` |
| `non_lethal` | Boolean | If true, the damage instance cannot reduce a unit below 1 HP, preventing kills. | 3 | `true` |
| `raw_heal` | String | An equation string that calculates the base healing amount before any modifiers are applied. | 2 | `"(str+1)/2"`<br>`"100-X"` |
| `two_way_contact` | Boolean | If true, contact effects apply to both the attacker and the target when the damage instance hits. | 2 | `true` |
| `damage_shield_only` | Boolean | If true, the damage instance only affects damage shields (e.g., barrier effects) and not health directly. | 1 | `true` |
| [`faction`](../Reference_and_Meta/Enums.md#enum-faction) | Enum | Specifies the faction of a spawned unit or projectile, determining its team allegiance and AI behavior. | 570 | `allies`<br>`auto`<br>`birds` |
| `final_hit_bonus_damage` | String | An equation string that adds bonus damage to the final hit of a multi-hit damage instance. | 1 | `5+bonus_melee_ability_damage` |
| `force_adjacent_and_diagonal_contact` | Boolean | If true, contact effects are forced for both adjacent and diagonal tiles even if not normally triggered. | 1 | `true` |
| `force_no_knockback` | Boolean | If true, the damage instance applies no knockback regardless of any knockback values set. | 2 | `true` |
| `hint_dont_lowgravboost` | Boolean | If true, the damage instance does not receive a damage boost from low gravity tiles. | 1 | `true` |
| [`hit_animation_alt`](../Reference_and_Meta/Enums.md#enum-hit_animation_alt) | Enum | Specifies an alternative hit animation name (e.g., "catch") to play instead of the default on successful hit. | 1 | `catch` |
| [`elements`](../Reference_and_Meta/Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 414 | `[`<br>`[Heat Fire]` |

</details>


---


#### `self_damage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 264

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 65 | `damage_instance`<br>`spell`<br>`self_damage` |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 2166 | `{ . . . }` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 836 | `[attack move spell]`<br>`attack`<br>`battle` |
| `piercing` | Boolean | If true, the damage instance ignores armor or damage reduction effects on the target. | 67 | `true` |
| `cant_miss` | Boolean | If true, the damage instance always hits its target regardless of accuracy or evasion. | 131 | `true` |
| [`knockback`](../Reference_and_Meta/Enums.md#enum-knockback) | Enum / Integer  | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 314 | `"ceil(X*.25/5)"`<br>`-10`<br>`-2` |
| `heal` | Enum / Equation | An equation string that determines the amount of health restored by this damage instance. | 168 | `"ceil(X*item_aux/100)"`<br>`0`<br>`1` |
| `ai_base_score` | Integer | The base priority score the AI assigns to using this damage instance, with higher values indicating greater preference. | 257 | `-99999`<br>`-999999`<br>`1` |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Equation / Object | Specifies the amount of damage dealt, can be a number or expression. | 1684 | `"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| `non_lethal` | Boolean | If true, the damage instance cannot reduce a unit below 1 HP, preventing kills. | 3 | `true` |
| [`elements`](../Reference_and_Meta/Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 414 | `[`<br>`[Heat Fire]` |

</details>


---


#### `splash_damage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 35

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 33 | `damage_instance`<br>`spell`<br>`self_damage` |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 2166 | `{ . . . }` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 836 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`knockback`](../Reference_and_Meta/Enums.md#enum-knockback) | Enum / Integer  | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 314 | `"ceil(X*.25/5)"`<br>`-10`<br>`-2` |
| `makes_contact` | Boolean | If true, the damage instance is considered a contact hit, triggering contact-based passives on both the attacker and target. | 47 | `false`<br>`true` |
| [`layer`](../Reference_and_Meta/Enums.md#enum-layer) | Enum | Specifies the layer on which the ability's effect operates (e.g., characters, tiles, gas). | 61 | `2`<br>`all`<br>`characters` |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Equation / Object | Specifies the amount of damage dealt, can be a number or expression. | 1684 | `"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| `override_trample_damage` | Boolean | If true, this damage instance replaces any default trample damage when the unit passes through an occupied tile. | 17 | `true` |
| `ai_base_score` | Integer | The base priority score the AI assigns to using this damage instance, with higher values indicating greater preference. | 257 | `-99999`<br>`-999999`<br>`1` |
| `crit_chance` | Equation | The chance for the damage instance to critically hit, expressed as a percentage or equation; values above 1 default to 100%. | 24 | `-999999`<br>`.05*X`<br>`.25` |
| `force_no_knockback` | Boolean | If true, the damage instance applies no knockback regardless of any knockback values set. | 2 | `true` |
| `force_play_hit_animation` | Boolean | If true, the hit animation is forced to play regardless of other conditions (e.g., miss or block). | 6 | `true` |
| [`elements`](../Reference_and_Meta/Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 414 | `[`<br>`[Heat Fire]` |

</details>