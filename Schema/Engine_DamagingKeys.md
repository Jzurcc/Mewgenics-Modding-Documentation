# Mewgenics Mod Developer Documentation: Engine: Damaging Keys

> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

## Engine: Damaging Keys

This document defines the shared schema for all Damage Instance blocks (`damage_instance`, `splash_damage`, `self_damage`, `bonk_damage`). Each of these blocks configures a discrete hit: its base damage, element, knockback, accuracy, and any on-hit effects.

> **Referenced by:** [`damage_instance` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-damage_instance), [`self_damage` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-self_damage), [`splash_damage` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-splash_damage), [`bonk_damage` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-bonk_damage), [`damage_instance` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-damage_instance), [`damage_instance` (Items_and_Equipment)](./Items_and_Equipment.md#context-damage_instance)

### Valid Property Keys

<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Object defining the combat math and status effects applied upon successful hit. | 4688 ||
| [`spell`](./Enums.md#enum-spell) | Enum | `MCHadouken` | 924 ||
| `false` | Variable | Evaluates to the boolean false value. | 655 ||
| [`self_damage`](Abilities_and_Spells.md#object-self_damage) | Boolean / Integer / Object | Recoil or self-inflicted damage/effects applied to the caster. | 436 ||
| [`elements`](./Arrays.md#array-elements) | Array | Array of elemental tags to apply (e.g., `[Fire Holy]`). | 369 ||
| `str` | Enum / Integer | `aux` | 337 ||
| `knockback` | Enum / Integer | The base physics pushing power (in tiles). | 277 ||
| `durability` | Array / Integer | Consumes item durability. | 264 ||
| `ai_base_score` | Integer | How highly the AI values using this ability. | 226 ||
| `heal` | Enum / Integer | Restores health instead of dealing damage. | 128 ||
| `cant_miss` | Boolean | Guarantees the hit, bypassing dodge mechanics. | 120 ||
| `incidentally_collects_pickups` | Boolean | Automatically grabs items in the AoE. | 103 ||
| `melee` | Variable | Variable representing the melee damage type or keyword. | 102 ||
| `status_spell` | Variable | Variable representing the status spells category. | 87 ||
| [`custom_additional_ai_weight`](./Enums.md#enum-custom_additional_ai_weight) | Enum | Granular AI preference adjustments (e.g., `prefer_dont_move`). | 82 ||
| [`splash_damage`](Abilities_and_Spells.md#object-splash_damage) | Object | Secondary Area of Effect blast parameters. | 68 ||
| `piercing` | Boolean | Ignores a percentage of target defense/armor. | 64 ||
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 62 ||
| [`type`](./Enums.md#enum-type) | Enum | The classification of damage (`melee`, `ranged`, `spell`, `trample`, `knockblock`, `spawn`). | 54 ||
| `makes_contact` | Boolean | If false, explicitly avoids triggering contact-based passives. | 46 ||
| [`level`](./Enums.md#enum-level) | Enum | `Butch_Tutorial`, `CraterWeatherEvent`, `Quest_BrokenTimeMachine`, `Quest_CoreObelisk`, `Quest_CoreObeliskGlowing` | 33 ||
| [`blocked_damage`](./Math_Equations.md) | Equation | Base damage dealt if the attack is blocked. | 24 ||
| [`raw_damage`](./Math_Equations.md) | Equation | Unmitigated, unscaled base numbers. | 22 ||
| `characters` | Variable | Variable representing all characters on the map. | 17 ||
| [`crit_chance`](./Enums.md#enum-crit_chance) | Float | Override for base critical hit probability. | 17 ||
| `override_trample_damage` | Boolean | Custom damage value for trample moves. | 17 ||
| `contact_requires_adjacency` | Boolean | Contact effects only trigger if standing next to the target. | 14 ||
| `ranged` | Boolean | Boolean flagging the damage as explicitly ranged. | 10 ||
| `tile_has_no_known_traps` | Variable | Condition variable that is true if the tile has no known traps. | 9 ||
| `can_revive` | Boolean | Healing instance that can bring dead allies back to life. | 8 ||
| `force_play_hit_animation` | Boolean | Forces the flinch animation even on 0 damage. | 6 ||
| `show_damage_on_0` | Boolean | Forces the "-0" floater text to appear. | 6 ||
| `avoid_redundant_debuffs_strict` | Variable | AI logic variable to strictly avoid applying debuffs that already exist. | 4 ||
| `blocked_multiplier` | Integer | Multiplier applied when hitting a blocking target. | 4 ||
| `item_aux` | Variable | Variable referring to the auxiliary item slot or its value. | 4 ||
| [`layer`](./Enums.md#enum-layer) | Enum | Z-index targeting (e.g., `characters`, `self`). | 3 ||
| [`accuracy`](./Enums.md#enum-accuracy) | Float | Hit chance modifier. | 3 ||
| `can_collect_pickups` | Boolean | The damage instance can grab items on the ground. | 3 ||
| `magnetize_favorlineup` | Variable | AI variable that favors lining up enemies for magnetize effects. | 3 ||
| `non_lethal` | Boolean | Reduces target to 1 HP but will never kill. | 3 ||
| `spell_cost` | Variable | Variable representing the cost of a spell. | 3 ||
| `tiles` | Variable | Variable representing a set of tiles. | 3 ||
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | The base damage properties of an attack. | 2 ||
| `can_instapop` | Boolean | Allows the attack to instantly destroy specific weak entities. | 2 ||
| `disallow_modifications` | Boolean | Prevents passives from altering this damage instance. | 2 ||
| `force_no_contact` | Boolean | Bypasses all contact-based retaliation (Thorns, etc). | 2 ||
| `force_no_knockback` | Boolean | Prevents the target from being pushed. | 2 ||
| `knockblock` | Variable | Variable representing the knockback blocking property. | 2 ||
| `physical_spell` | Variable | Variable representing the physical spell type. | 2 ||
| `pickups` | Variable | Variable representing pickups on the map. | 2 ||
| `raw_heal` | String | Unmitigated, unscaled base numbers. | 2 ||
| `self` | Variable | Variable representing the current unit. | 2 ||
| `tile_close_to_enemy` | Variable | Condition variable true if the tile is adjacent to an enemy. | 2 ||
| `tile_exists` | Variable | Condition variable true if the specified tile exists. | 2 ||
| `toss_farthest` | Variable | AI variable that favors tossing the target the farthest distance. | 2 ||
| `two_way_contact` | Boolean | Both caster and target trigger contact effects on each other. | 2 ||
| [`bonk_damage`](Abilities_and_Spells.md#object-bonk_damage) | Object | Damage dealt when knocked into a wall or obstacle. | 2 ||
| `avoid_redundant_debuffs` | Variable | AI variable to avoid reapplying debuffs already present. | 1 ||
| [`catch`](Events_and_Encounters.md#object-catch) | Object | Event Object: Story branch or dialog option representing the \'Catch\' action. | 1 ||
| `damage_shield_only` | Boolean | Depletes shields but cannot harm base health. | 1 ||
| [`faction`](./Enums.md#enum-faction) | Enum | Determines alignment (`enemies`, `cats`, `neutral`). | 1 ||
| `favor_enemy_already_moved` | Variable | AI variable that favors targeting an enemy that has already acted this turn. | 1 ||
| `favor_tile_far_away` | Variable | Increases the priority of targeting tiles far from the unit. | 1 ||
| [`final_hit_bonus_damage`](./Math_Equations.md) | Equation | Extra damage applied on the last hit of a multihit. | 1 ||
| `force_adjacent_and_diagonal_contact` | Boolean | Treats diagonal hits as physical contact. | 1 ||
| `generic_physical` | Variable | Specifies that the ability deals generic physical damage. | 1 ||
| `hint_dont_lowgravboost` | Boolean | AI hint to ignore wind physics. | 1 ||
| [`hit_animation_alt`](./Enums.md#enum-hit_animation_alt) | Enum | Custom flinch animation for the target. | 1 ||
| `moonhead_punchself` | Variable | Determines if the Moonhead cat punches itself. | 1 ||
| `moonhead_use_if_cracked` | Variable | When true, the Moonhead cat uses the ability if its shell is cracked. | 1 ||
| `must_heal_most_missing_health` | Variable | Requires the ability to target the ally with the most missing health. | 1 ||
| `must_target_buddy` | Variable | Requires the ability to target a buddy (paired unit). | 1 ||
| `no_coins_on_map` | Variable | When true, prevents coins from appearing on the map. | 1 ||
| `no_redundant_formchange` | Variable | Prevents the ability from changing form if it would result in the same form. | 1 ||
| [`status`](./Enums.md#enum-status) | Enum | The status effect to apply. | 1 ||
| `target_closest` | Variable | Forces the ability to target the closest valid target. | 1 ||
| `target_farthest` | Variable | Forces the ability to target the farthest valid target. | 1 ||
| `teslacoil_priorities` | Variable | Specifies targeting priorities for Tesla Coil abilities. | 1 ||
| `tile_close_to_enemy_soft` | Variable | Prefers tiles that are close to an enemy, with a soft constraint. | 1 ||
| `toss_far` | Variable | Increases the distance the target is tossed. | 1 ||
| `toss_towards_bottomleft` | Variable | Forces the toss direction towards the bottom-left of the map. | 1 ||

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
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 62 ||
| [`damage`](./Arrays.md#array-damage) | Equation | The base damage properties of an attack. | 2 ||

</details>

---

#### `damage_instance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2346

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `knockback` | Enum / Integer | The base physics pushing power (in tiles). | 254 ||
| `ai_base_score` | Integer | How highly the AI values using this ability. | 223 ||
| `heal` | Enum / Integer | Restores health instead of dealing damage. | 122 ||
| `cant_miss` | Boolean | Guarantees the hit, bypassing dodge mechanics. | 110 ||
| `incidentally_collects_pickups` | Boolean | Automatically grabs items in the AoE. | 103 ||
| [`custom_additional_ai_weight`](./Enums.md#enum-custom_additional_ai_weight) | Enum | Granular AI preference adjustments (e.g., `prefer_dont_move`). | 82 ||
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 62 ||
| [`type`](./Enums.md#enum-type) | Enum | The classification of damage (`melee`, `ranged`, `spell`, `trample`, `knockblock`, `spawn`). | 54 ||
| `piercing` | Boolean | Ignores a percentage of target defense/armor. | 52 ||
| `makes_contact` | Boolean | If false, explicitly avoids triggering contact-based passives. | 40 ||
| `HealthRegenUp` | Integer | The amount of health regeneration (HealthRegen) granted by this damage instance. | 26 | `[1 .5]` (Array), `4` (Number), `3` (Number), `{ ... }` (Object) |
| [`blocked_damage`](./Math_Equations.md) | Integer / String | Base damage dealt if the attack is blocked. | 24 ||
| [`raw_damage`](./Math_Equations.md) | Enum / Integer | Unmitigated, unscaled base numbers. | 22 ||
| [`crit_chance`](./Enums.md#enum-crit_chance) | Number | Override for base critical hit probability. | 16 ||
| `override_trample_damage` | Boolean | Custom damage value for trample moves. | 15 ||
| `contact_requires_adjacency` | Boolean | Contact effects only trigger if standing next to the target. | 14 ||
| `ranged` | Boolean | Boolean flagging the damage as explicitly ranged. | 10 ||
| `can_revive` | Boolean | Healing instance that can bring dead allies back to life. | 8 ||
| `show_damage_on_0` | Boolean | Forces the "-0" floater text to appear. | 6 ||
| `force_play_hit_animation` | Boolean | Forces the flinch animation even on 0 damage. | 5 ||
| `blocked_multiplier` | Integer | Multiplier applied when hitting a blocking target. | 4 ||
| [`accuracy`](./Enums.md#enum-accuracy) | Number | Hit chance modifier. | 3 ||
| `can_collect_pickups` | Boolean | The damage instance can grab items on the ground. | 3 ||
| [`layer`](./Enums.md#enum-layer) | Enum | Z-index targeting (e.g., `characters`, `self`). | 3 ||
| `can_instapop` | Boolean | Allows the attack to instantly destroy specific weak entities. | 2 ||
| [`damage`](./Arrays.md#array-damage) | Equation | The base damage properties of an attack. | 2 ||
| `disallow_modifications` | Boolean | Prevents passives from altering this damage instance. | 2 ||
| `force_no_contact` | Boolean | Bypasses all contact-based retaliation (Thorns, etc). | 2 ||
| `non_lethal` | Boolean | Reduces target to 1 HP but will never kill. | 2 ||
| `raw_heal` | String | Unmitigated, unscaled base numbers. | 2 ||
| `two_way_contact` | Boolean | Both caster and target trigger contact effects on each other. | 2 ||
| `damage_shield_only` | Boolean | Depletes shields but cannot harm base health. | 1 ||
| [`faction`](./Enums.md#enum-faction) | Enum | Determines alignment (`enemies`, `cats`, `neutral`). | 1 ||
| [`final_hit_bonus_damage`](./Math_Equations.md) | String | Extra damage applied on the last hit of a multihit. | 1 ||
| `force_adjacent_and_diagonal_contact` | Boolean | Treats diagonal hits as physical contact. | 1 ||
| `force_no_knockback` | Boolean | Prevents the target from being pushed. | 1 ||
| `hint_dont_lowgravboost` | Boolean | AI hint to ignore wind physics. | 1 ||
| [`hit_animation_alt`](./Enums.md#enum-hit_animation_alt) | Enum | Custom flinch animation for the target. | 1 ||
| [`elements`](./Arrays.md#array-elements) | Array | Array of elemental tags to apply (e.g., `[Fire Holy]`). | 0 ||

</details>

---

#### `self_damage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 264

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 62 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 54 ||
| `piercing` | Boolean | Ignores a percentage of target defense/armor. | 12 ||
| `cant_miss` | Boolean | Guarantees the hit, bypassing dodge mechanics. | 10 ||
| `knockback` | Enum / Integer | The base physics pushing power (in tiles). | 10 ||
| `heal` | Enum / Integer | Restores health instead of dealing damage. | 6 ||
| `ai_base_score` | Integer | How highly the AI values using this ability. | 2 ||
| [`damage`](./Arrays.md#array-damage) | Equation | The base damage properties of an attack. | 2 ||
| `non_lethal` | Boolean | Reduces target to 1 HP but will never kill. | 1 ||
| [`elements`](./Arrays.md#array-elements) | Array | Array of elemental tags to apply (e.g., `[Fire Holy]`). | 0 ||

</details>

---

#### `splash_damage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 35

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 62 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 54 ||
| `knockback` | Enum / Integer | Knockback force of the splash blast. | 13 ||
| `makes_contact` | Boolean | If false, explicitly avoids triggering contact-based passives. | 6 ||
| [`layer`](./Enums.md#enum-layer) | Enum | Z-index targeting (e.g., `characters`, `self`). | 3 ||
| [`damage`](./Arrays.md#array-damage) | Equation | The base damage properties of an attack. | 2 ||
| `override_trample_damage` | Boolean | Custom damage value for trample moves. | 2 ||
| `ai_base_score` | Integer | How highly the AI values using this ability. | 1 ||
| [`crit_chance`](./Enums.md#enum-crit_chance) | Float | Override for base critical hit probability. | 1 ||
| `force_no_knockback` | Boolean | Prevents the target from being pushed. | 1 ||
| `force_play_hit_animation` | Boolean | Forces the flinch animation even on 0 damage. | 1 ||
| [`elements`](./Arrays.md#array-elements) | Array | Array of elemental tags to apply (e.g., `[Fire Holy]`). | 0 ||

</details>

