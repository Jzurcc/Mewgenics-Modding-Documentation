# Mewgenics Mod Developer Documentation: Engine: Damage Instances

> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Math_Equations.md).

## Engine: Damage Instances

This document defines the shared schema for all Damage Instance blocks (`damage_instance`, `splash_damage`, `self_damage`, `bonk_damage`). Each of these blocks configures a discrete hit: its base damage, element, knockback, accuracy, and any on-hit effects.

### Known Explicit Parameters

These are hardcoded configuration keys found within these blocks (not dynamic IDs).

<details>
<summary><b>Expand</b></summary>

| Parameter | Type | Notes |
| :--- | :--- | :--- |
| `accuracy` | Enum | Hit chance modifier. |
| `ai_base_score` | Number | How highly the AI values using this ability. |
| `blocked_damage` | Equation | Base damage dealt if the attack is blocked. |
| `blocked_multiplier` | Number | Multiplier applied when hitting a blocking target. |
| `can_collect_pickups` | Boolean | The damage instance can grab items on the ground. |
| `can_instapop` | Boolean | Allows the attack to instantly destroy specific weak entities. |
| `can_revive` | Boolean | Healing instance that can bring dead allies back to life. |
| `cant_miss` | Boolean | Guarantees the hit, bypassing dodge mechanics. |
| `contact_requires_adjacency` | Boolean | Contact effects only trigger if standing next to the target. |
| `crit_chance` | Number | Override for base critical hit probability. |
| `custom_additional_ai_weight` | Enum | Granular AI preference adjustments (e.g., `prefer_dont_move`). |
| `damage` | Number | The base damage properties of an attack. |
| `damage_shield_only` | Boolean | Depletes shields but cannot harm base health. |
| `disallow_modifications` | Boolean | Prevents passives from altering this damage instance. |
| `effects` | Block | Non-damaging status applications and logic triggers executed on impact. |
| `elements` | Array | Array of elemental tags to apply (e.g., `[Fire Holy]`). |
| `faction` | Enum | Determines alignment (`enemies`, `cats`, `neutral`). |
| `final_hit_bonus_damage` | Equation | Extra damage applied on the last hit of a multihit. |
| `force_adjacent_and_diagonal_contact` | Boolean | Treats diagonal hits as physical contact. |
| `force_no_contact` | Boolean | Bypasses all contact-based retaliation (Thorns, etc). |
| `force_no_knockback` | Boolean |  |
| `force_play_hit_animation` | Boolean | Forces the flinch animation even on 0 damage. |
| `heal` | Number | Restores health instead of dealing damage. |
| `hint_dont_lowgravboost` | Boolean | AI hint to ignore wind physics. |
| `hit_animation_alt` | Enum | Custom flinch animation for the target. |
| `incidentally_collects_pickups` | Boolean | Automatically grabs items in the AoE. |
| `knockback` | Number | The base physics pushing power (in tiles). |
| `layer` | Enum | Z-index targeting (e.g., `characters`, `self`). |
| `makes_contact` | Boolean | If false, explicitly avoids triggering contact-based passives. |
| `non_lethal` | Boolean | Reduces target to 1 HP but will never kill. |
| `override_trample_damage` | Boolean | Custom damage value for trample moves. |
| `piercing` | Boolean | Ignores a percentage of target defense/armor. |
| `ranged` | Boolean | Boolean flagging the damage as explicitly ranged. |
| `raw_damage` | Equation | Unmitigated, unscaled base numbers. |
| `raw_heal` | String | Unmitigated, unscaled base numbers. |
| `show_damage_on_0` | Boolean | Forces the "-0" floater text to appear. |
| `two_way_contact` | Boolean | Both caster and target trigger contact effects on each other. |
| `type` | Enum | The classification of damage (`melee`, `ranged`, `spell`, `trample`, `knockblock`, `spawn`). |

</details>

