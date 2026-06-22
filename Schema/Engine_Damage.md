# Mewgenics Mod Developer Documentation: Engine: Damage Instances

## Engine: Damage Instances

This document defines the shared schema for all Damage Instance blocks (`damage_instance`, `splash_damage`, `self_damage`, `bonk_damage`). Each of these blocks configures a discrete hit: its base damage, element, knockback, accuracy, and any on-hit effects.

> **Referenced by:** [`damage_instance` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-damage_instance), [`self_damage` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-self_damage), [`splash_damage` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-splash_damage), [`bonk_damage` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-bonk_damage), [`damage_instance` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-damage_instance), [`damage_instance` (Items_and_Equipment)](./Items_and_Equipment.md#context-damage_instance)

### Valid Property Keys

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| `accuracy` | Float | Hit chance modifier. |
| `ai_base_score` | Integer | How highly the AI values using this ability. |
| [`blocked_damage`](./Math_Equations.md) | Equation | Base damage dealt if the attack is blocked. |
| `blocked_multiplier` | Integer | Multiplier applied when hitting a blocking target. |
| `can_collect_pickups` | Boolean | The damage instance can grab items on the ground. |
| `can_instapop` | Boolean | Allows the attack to instantly destroy specific weak entities. |
| `can_revive` | Boolean | Healing instance that can bring dead allies back to life. |
| `cant_miss` | Boolean | Guarantees the hit, bypassing dodge mechanics. |
| `contact_requires_adjacency` | Boolean | Contact effects only trigger if standing next to the target. |
| `crit_chance` | Float | Override for base critical hit probability. |
| [`custom_additional_ai_weight`](./Enums.md#enum-custom_additional_ai_weight) | Enum | Granular AI preference adjustments (e.g., `prefer_dont_move`). |
| `damage` | Integer | The base damage properties of an attack. |
| `damage_shield_only` | Boolean | Depletes shields but cannot harm base health. |
| `disallow_modifications` | Boolean | Prevents passives from altering this damage instance. |
| [`effects`](#effects) | Block | Non-damaging status applications and logic triggers executed on impact. |
| [`elements`](./Arrays.md#array-elements) | Array | Array of elemental tags to apply (e.g., `[Fire Holy]`). |
| [`faction`](./Enums.md#enum-faction) | Enum | Determines alignment (`enemies`, `cats`, `neutral`). |
| [`final_hit_bonus_damage`](./Math_Equations.md) | Equation | Extra damage applied on the last hit of a multihit. |
| `force_adjacent_and_diagonal_contact` | Boolean | Treats diagonal hits as physical contact. |
| `force_no_contact` | Boolean | Bypasses all contact-based retaliation (Thorns, etc). |
| `force_no_knockback` | Boolean | Prevents the target from being pushed. |
| `force_play_hit_animation` | Boolean | Forces the flinch animation even on 0 damage. |
| `heal` | Integer | Restores health instead of dealing damage. |
| `hint_dont_lowgravboost` | Boolean | AI hint to ignore wind physics. |
| [`hit_animation_alt`](./Enums.md#enum-hit_animation_alt) | Enum | Custom flinch animation for the target. |
| `incidentally_collects_pickups` | Boolean | Automatically grabs items in the AoE. |
| `knockback` | Integer | The base physics pushing power (in tiles). |
| [`layer`](./Enums.md#enum-layer) | Enum | Z-index targeting (e.g., `characters`, `self`). |
| `makes_contact` | Boolean | If false, explicitly avoids triggering contact-based passives. |
| `non_lethal` | Boolean | Reduces target to 1 HP but will never kill. |
| `override_trample_damage` | Boolean | Custom damage value for trample moves. |
| `piercing` | Boolean | Ignores a percentage of target defense/armor. |
| `ranged` | Boolean | Boolean flagging the damage as explicitly ranged. |
| [`raw_damage`](./Math_Equations.md) | Equation | Unmitigated, unscaled base numbers. |
| `raw_heal` | String | Unmitigated, unscaled base numbers. |
| `show_damage_on_0` | Boolean | Forces the "-0" floater text to appear. |
| `two_way_contact` | Boolean | Both caster and target trigger contact effects on each other. |
| [`type`](./Enums.md#enum-type) | Enum | The classification of damage (`melee`, `ranged`, `spell`, `trample`, `knockblock`, `spawn`). |
| `{Statuses / Passives}` | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |

</details>

### Valid Nested Blocks

The following blocks all behave as `[damage_instance]` containers. Each has its own unique parameters listed below its entry.

---

#### `bonk_damage`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[damage_instance]`](./Engine_Damage.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| `damage` | Integer | The base damage properties of an attack. |
| [`effects`](#effects) | Block | Non-damaging status applications and logic triggers executed on impact. |

</details>

---

#### `damage_instance`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[damage_instance]`](./Engine_Damage.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| `accuracy` | Float | Hit chance modifier. |
| `ai_base_score` | Integer | How highly the AI values using this ability. |
| [`blocked_damage`](./Math_Equations.md) | Equation | Base damage dealt if the attack is blocked. |
| `blocked_multiplier` | Integer | Multiplier applied when hitting a blocking target. |
| `can_collect_pickups` | Boolean | The damage instance can grab items on the ground. |
| `can_instapop` | Boolean | Allows the attack to instantly destroy specific weak entities. |
| `can_revive` | Boolean | Healing instance that can bring dead allies back to life. |
| `cant_miss` | Boolean | Guarantees the hit, bypassing dodge mechanics. |
| `contact_requires_adjacency` | Boolean | Contact effects only trigger if standing next to the target. |
| `crit_chance` | Float | Override for base critical hit probability. |
| [`custom_additional_ai_weight`](./Enums.md#enum-custom_additional_ai_weight) | Enum | Granular AI preference adjustments (e.g., `prefer_dont_move`). |
| `damage` | Integer | The base damage properties of an attack. |
| `damage_shield_only` | Boolean | Depletes shields but cannot harm base health. |
| `disallow_modifications` | Boolean | Prevents passives from altering this damage instance. |
| [`effects`](#effects) | Block | Non-damaging status applications and logic triggers executed on impact. |
| [`elements`](./Arrays.md#array-elements) | Array | Array of elemental tags to apply (e.g., `[Fire Holy]`). |
| [`faction`](./Enums.md#enum-faction) | Enum | Determines alignment (`enemies`, `cats`, `neutral`). |
| [`final_hit_bonus_damage`](./Math_Equations.md) | Equation | Extra damage applied on the last hit of a multihit. |
| `force_adjacent_and_diagonal_contact` | Boolean | Treats diagonal hits as physical contact. |
| `force_no_contact` | Boolean | Bypasses all contact-based retaliation (Thorns, etc). |
| `force_no_knockback` | Boolean | Prevents the target from being pushed. |
| `force_play_hit_animation` | Boolean | Forces the flinch animation even on 0 damage. |
| `heal` | Integer | Restores health instead of dealing damage. |
| `hint_dont_lowgravboost` | Boolean | AI hint to ignore wind physics. |
| [`hit_animation_alt`](./Enums.md#enum-hit_animation_alt) | Enum | Custom flinch animation for the target. |
| `incidentally_collects_pickups` | Boolean | Automatically grabs items in the AoE. |
| `knockback` | Integer | The base physics pushing power (in tiles). |
| [`layer`](./Enums.md#enum-layer) | Enum | Z-index targeting (e.g., `characters`, `self`). |
| `makes_contact` | Boolean | If false, explicitly avoids triggering contact-based passives. |
| `non_lethal` | Boolean | Reduces target to 1 HP but will never kill. |
| `override_trample_damage` | Boolean | Custom damage value for trample moves. |
| `piercing` | Boolean | Ignores a percentage of target defense/armor. |
| `ranged` | Boolean | Boolean flagging the damage as explicitly ranged. |
| [`raw_damage`](./Math_Equations.md) | Equation | Unmitigated, unscaled base numbers. |
| `raw_heal` | String | Unmitigated, unscaled base numbers. |
| `show_damage_on_0` | Boolean | Forces the "-0" floater text to appear. |
| `two_way_contact` | Boolean | Both caster and target trigger contact effects on each other. |
| [`type`](./Enums.md#enum-type) | Enum | The classification of damage (`melee`, `ranged`, `spell`, `trample`, `knockblock`, `spawn`). |

</details>

---

#### `self_damage`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[damage_instance]`](./Engine_Damage.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| `ai_base_score` | Integer |  |
| `cant_miss` | Boolean |  |
| [`damage`](./Math_Equations.md) | Equation | The base damage properties of an attack. |
| [`effects`](#effects) | Block | Non-damaging status applications and logic triggers executed on impact. |
| [`elements`](./Arrays.md#array-elements) | Array |  |
| `heal` | Integer |  |
| `knockback` | Integer |  |
| `non_lethal` | Boolean |  |
| `piercing` | Boolean |  |
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. |

</details>

---

#### `splash_damage`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[damage_instance]`](./Engine_Damage.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| `ai_base_score` | Integer |  |
| `crit_chance` | Float |  |
| `damage` | Integer | The base damage properties of an attack. |
| [`effects`](#effects) | Block | Non-damaging status applications and logic triggers executed on impact. |
| [`elements`](./Arrays.md#array-elements) | Array |  |
| `force_no_knockback` | Boolean |  |
| `force_play_hit_animation` | Boolean |  |
| `knockback` | Integer | Knockback force of the splash blast. |
| [`layer`](./Enums.md#enum-layer) | Enum |  |
| `makes_contact` | Boolean |  |
| `override_trample_damage` | Boolean |  |
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. |

</details>

