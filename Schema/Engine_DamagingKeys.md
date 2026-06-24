# Mewgenics Mod Developer Documentation: Engine: Damaging Keys

## Engine: Damaging Keys

This document defines the shared schema for all Damage Instance blocks (`damage_instance`, `splash_damage`, `self_damage`, `bonk_damage`). Each of these blocks configures a discrete hit: its base damage, element, knockback, accuracy, and any on-hit effects.

> **Referenced by:** [`damage_instance` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-damage_instance), [`self_damage` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-self_damage), [`splash_damage` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-splash_damage), [`bonk_damage` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-bonk_damage), [`damage_instance` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-damage_instance), [`damage_instance` (Items_and_Equipment)](./Items_and_Equipment.md#context-damage_instance)

### Valid Property Keys

<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`damage_instance`](#damage_instance) | Object | Block defining the combat math and status effects applied upon successful hit. | 2346 |
| `effects` | Object | Non-damaging status applications and logic triggers executed on impact. | 2005 |
| [`damage`](./Arrays.md#array-damage) | Integer | The base damage properties of an attack. | 1527 |
| [`type`](./Enums.md#enum-type) | Enum | The classification of damage (`melee`, `ranged`, `spell`, `trample`, `knockblock`, `spawn`). | 382 |
| [`elements`](./Arrays.md#array-elements) | Array | Array of elemental tags to apply (e.g., `[Fire Holy]`). | 369 |
| `knockback` | Integer | The base physics pushing power (in tiles). | 277 |
| `ai_base_score` | Integer | How highly the AI values using this ability. | 226 |
| [`self_damage`](./Arrays.md#array-self_damage) | Object | Recoil or self-inflicted damage/effects applied to the caster. | 220 |
| `heal` | Number | Restores health instead of dealing damage. | 128 |
| `cant_miss` | Boolean | Guarantees the hit, bypassing dodge mechanics. | 120 |
| `false` | Variable |  | 103 |
| `incidentally_collects_pickups` | Boolean | Automatically grabs items in the AoE. | 103 |
| `melee` | Variable |  | 102 |
| `status_spell` | Variable |  | 87 |
| [`custom_additional_ai_weight`](./Enums.md#enum-custom_additional_ai_weight) | Enum | Granular AI preference adjustments (e.g., `prefer_dont_move`). | 82 |
| [`spell`](./Enums.md#enum-spell) | 1 | `MCHadouken` | 78 |
| `piercing` | Boolean | Ignores a percentage of target defense/armor. | 64 |
| `makes_contact` | Boolean | If false, explicitly avoids triggering contact-based passives. | 46 |
| [`splash_damage`](#splash_damage) | Object | Secondary Area of Effect blast parameters. | 35 |
| [`layer`](./Enums.md#enum-layer) | Enum | Z-index targeting (e.g., `characters`, `self`). | 27 |
| [`blocked_damage`](./Math_Equations.md) | Equation | Base damage dealt if the attack is blocked. | 24 |
| [`raw_damage`](./Math_Equations.md) | Equation | Unmitigated, unscaled base numbers. | 22 |
| `characters` | Variable |  | 17 |
| [`crit_chance`](./Enums.md#enum-crit_chance) | Float | Override for base critical hit probability. | 17 |
| `override_trample_damage` | Boolean | Custom damage value for trample moves. | 17 |
| `contact_requires_adjacency` | Boolean | Contact effects only trigger if standing next to the target. | 14 |
| `ranged` | Boolean | Boolean flagging the damage as explicitly ranged. | 10 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 10 |
| `tile_has_no_known_traps` | Variable |  | 9 |
| `can_revive` | Boolean | Healing instance that can bring dead allies back to life. | 8 |
| `force_play_hit_animation` | Boolean | Forces the flinch animation even on 0 damage. | 6 |
| `show_damage_on_0` | Boolean | Forces the "-0" floater text to appear. | 6 |
| `avoid_redundant_debuffs_strict` | Variable |  | 4 |
| `blocked_multiplier` | Integer | Multiplier applied when hitting a blocking target. | 4 |
| `item_aux` | Variable |  | 4 |
| [`accuracy`](./Enums.md#enum-accuracy) | Float | Hit chance modifier. | 3 |
| `can_collect_pickups` | Boolean | The damage instance can grab items on the ground. | 3 |
| `magnetize_favorlineup` | Variable |  | 3 |
| `non_lethal` | Boolean | Reduces target to 1 HP but will never kill. | 3 |
| `spell_cost` | Variable |  | 3 |
| `str` | 39 | `aux` | 3 |
| `tiles` | Variable |  | 3 |
| `can_instapop` | Boolean | Allows the attack to instantly destroy specific weak entities. | 2 |
| `disallow_modifications` | Boolean | Prevents passives from altering this damage instance. | 2 |
| `durability` | Number | Consumes item durability. | 2 |
| `force_no_contact` | Boolean | Bypasses all contact-based retaliation (Thorns, etc). | 2 |
| `force_no_knockback` | Boolean | Prevents the target from being pushed. | 2 |
| `knockblock` | Variable |  | 2 |
| [`level`](./Enums.md#enum-level) | 17 | `Butch_Tutorial`, `CraterWeatherEvent`, `Quest_BrokenTimeMachine`, `Quest_CoreObelisk`, `Quest_CoreObeliskGlowing` | 2 |
| `physical_spell` | Variable |  | 2 |
| `pickups` | Variable |  | 2 |
| `raw_heal` | String | Unmitigated, unscaled base numbers. | 2 |
| `self` | Variable |  | 2 |
| `tile_close_to_enemy` | Variable |  | 2 |
| `tile_exists` | Variable |  | 2 |
| `toss_farthest` | Variable |  | 2 |
| `two_way_contact` | Boolean | Both caster and target trigger contact effects on each other. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| `avoid_redundant_debuffs` | Variable |  | 1 |
| [`bonk_damage`](#bonk_damage) | Object | Damage dealt when knocked into a wall or obstacle. | 1 |
| `catch` | 1 | Event Node: Story branch or dialog option representing the \'Catch\' action. | 1 |
| `damage_shield_only` | Boolean | Depletes shields but cannot harm base health. | 1 |
| [`faction`](./Enums.md#enum-faction) | Enum | Determines alignment (`enemies`, `cats`, `neutral`). | 1 |
| `favor_enemy_already_moved` | Variable |  | 1 |
| `favor_tile_far_away` | Variable |  | 1 |
| [`final_hit_bonus_damage`](./Math_Equations.md) | Equation | Extra damage applied on the last hit of a multihit. | 1 |
| `force_adjacent_and_diagonal_contact` | Boolean | Treats diagonal hits as physical contact. | 1 |
| `generic_physical` | Variable |  | 1 |
| `hint_dont_lowgravboost` | Boolean | AI hint to ignore wind physics. | 1 |
| [`hit_animation_alt`](./Enums.md#enum-hit_animation_alt) | Enum | Custom flinch animation for the target. | 1 |
| `moonhead_punchself` | Variable |  | 1 |
| `moonhead_use_if_cracked` | Variable |  | 1 |
| `must_heal_most_missing_health` | Variable |  | 1 |
| `must_target_buddy` | Variable |  | 1 |
| `no_coins_on_map` | Variable |  | 1 |
| `no_redundant_formchange` | Variable |  | 1 |
| [`status`](./Enums.md#enum-status) | Enum | The status effect to apply. | 1 |
| `target_closest` | Variable |  | 1 |
| `target_farthest` | Variable |  | 1 |
| `teslacoil_priorities` | Variable |  | 1 |
| `tile_close_to_enemy_soft` | Variable |  | 1 |
| `toss_far` | Variable |  | 1 |
| `toss_towards_bottomleft` | Variable |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

### Valid Nested Blocks

The following blocks all behave as `{Damaging Keys}` containers. Each has its own unique parameters listed below its entry.

---

#### `bonk_damage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`effects`](#effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 1 |
| [`damage`](./Arrays.md#array-damage) | Integer | The base damage properties of an attack. | 1 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

#### `damage_instance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2346

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`effects`](#effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 1787 |
| [`damage`](./Arrays.md#array-damage) | Integer | The base damage properties of an attack. | 1447 |
| [`type`](./Enums.md#enum-type) | Enum | The classification of damage (`melee`, `ranged`, `spell`, `trample`, `knockblock`, `spawn`). | 359 |
| `knockback` | Integer | The base physics pushing power (in tiles). | 254 |
| `ai_base_score` | Integer | How highly the AI values using this ability. | 223 |
| `heal` | Integer | Restores health instead of dealing damage. | 122 |
| `cant_miss` | Boolean | Guarantees the hit, bypassing dodge mechanics. | 110 |
| `incidentally_collects_pickups` | Boolean | Automatically grabs items in the AoE. | 103 |
| [`custom_additional_ai_weight`](./Enums.md#enum-custom_additional_ai_weight) | Enum | Granular AI preference adjustments (e.g., `prefer_dont_move`). | 82 |
| `piercing` | Boolean | Ignores a percentage of target defense/armor. | 52 |
| `makes_contact` | Boolean | If false, explicitly avoids triggering contact-based passives. | 40 |
| [`layer`](./Enums.md#enum-layer) | Enum | Z-index targeting (e.g., `characters`, `self`). | 26 |
| [`blocked_damage`](./Math_Equations.md) | Equation | Base damage dealt if the attack is blocked. | 24 |
| [`raw_damage`](./Math_Equations.md) | Equation | Unmitigated, unscaled base numbers. | 22 |
| [`crit_chance`](./Enums.md#enum-crit_chance) | Float | Override for base critical hit probability. | 16 |
| `override_trample_damage` | Boolean | Custom damage value for trample moves. | 15 |
| `contact_requires_adjacency` | Boolean | Contact effects only trigger if standing next to the target. | 14 |
| `ranged` | Boolean | Boolean flagging the damage as explicitly ranged. | 10 |
| `can_revive` | Boolean | Healing instance that can bring dead allies back to life. | 8 |
| `show_damage_on_0` | Boolean | Forces the "-0" floater text to appear. | 6 |
| `force_play_hit_animation` | Boolean | Forces the flinch animation even on 0 damage. | 5 |
| `blocked_multiplier` | Integer | Multiplier applied when hitting a blocking target. | 4 |
| [`accuracy`](./Enums.md#enum-accuracy) | Float | Hit chance modifier. | 3 |
| `can_collect_pickups` | Boolean | The damage instance can grab items on the ground. | 3 |
| `can_instapop` | Boolean | Allows the attack to instantly destroy specific weak entities. | 2 |
| `disallow_modifications` | Boolean | Prevents passives from altering this damage instance. | 2 |
| `force_no_contact` | Boolean | Bypasses all contact-based retaliation (Thorns, etc). | 2 |
| `non_lethal` | Boolean | Reduces target to 1 HP but will never kill. | 2 |
| `raw_heal` | String | Unmitigated, unscaled base numbers. | 2 |
| `two_way_contact` | Boolean | Both caster and target trigger contact effects on each other. | 2 |
| [`faction`](./Enums.md#enum-faction) | Enum | Determines alignment (`enemies`, `cats`, `neutral`). | 1 |
| [`final_hit_bonus_damage`](./Math_Equations.md) | Equation | Extra damage applied on the last hit of a multihit. | 1 |
| [`hit_animation_alt`](./Enums.md#enum-hit_animation_alt) | Enum | Custom flinch animation for the target. | 1 |
| `damage_shield_only` | Boolean | Depletes shields but cannot harm base health. | 1 |
| `force_adjacent_and_diagonal_contact` | Boolean | Treats diagonal hits as physical contact. | 1 |
| `force_no_knockback` | Boolean | Prevents the target from being pushed. | 1 |
| `hint_dont_lowgravboost` | Boolean | AI hint to ignore wind physics. | 1 |
| [`elements`](./Arrays.md#array-elements) | Array | Array of elemental tags to apply (e.g., `[Fire Holy]`). | 0 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

#### `self_damage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 264

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`effects`](#effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 200 |
| [`damage`](./Arrays.md#array-damage) | Equation | The base damage properties of an attack. | 47 |
| `piercing` | Boolean | Ignores a percentage of target defense/armor. | 12 |
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 11 |
| `cant_miss` | Boolean | Guarantees the hit, bypassing dodge mechanics. | 10 |
| `knockback` | Integer | The base physics pushing power (in tiles). | 10 |
| `heal` | Integer | Restores health instead of dealing damage. | 6 |
| `ai_base_score` | Integer | How highly the AI values using this ability. | 2 |
| `non_lethal` | Boolean | Reduces target to 1 HP but will never kill. | 1 |
| [`elements`](./Arrays.md#array-elements) | Array | Array of elemental tags to apply (e.g., `[Fire Holy]`). | 0 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

#### `splash_damage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 35

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`damage`](./Arrays.md#array-damage) | Integer | The base damage properties of an attack. | 32 |
| [`effects`](#effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 17 |
| `knockback` | Integer | Knockback force of the splash blast. | 13 |
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 12 |
| `makes_contact` | Boolean | If false, explicitly avoids triggering contact-based passives. | 6 |
| `override_trample_damage` | Boolean | Custom damage value for trample moves. | 2 |
| [`layer`](./Enums.md#enum-layer) | Enum | Z-index targeting (e.g., `characters`, `self`). | 1 |
| `ai_base_score` | Integer | How highly the AI values using this ability. | 1 |
| [`crit_chance`](./Enums.md#enum-crit_chance) | Float | Override for base critical hit probability. | 1 |
| `force_no_knockback` | Boolean | Prevents the target from being pushed. | 1 |
| `force_play_hit_animation` | Boolean | Forces the flinch animation even on 0 damage. | 1 |
| [`elements`](./Arrays.md#array-elements) | Array | Array of elemental tags to apply (e.g., `[Fire Holy]`). | 0 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

