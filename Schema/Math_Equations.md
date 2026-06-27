# Mewgenics Mod Developer Documentation: Math Equations

> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see AUDIT_GAPS.md. For enum values, see [Enums.md](./Enums.md).

In the Mewgenics engine, many numeric fields can accept an inline math equation string instead of a raw number.

> **Referenced by:** [`Conditional_Ally`](./Abilities_and_Spells.md#object-conditional_ally), [`Conditional_Displaceable`](./Abilities_and_Spells.md#object-conditional_displaceable), [`Conditional_HealthThreshold`](./Abilities_and_Spells.md#object-conditional_healththreshold), [`Else`](./Abilities_and_Spells.md#object-else), [`RandomStatusFromPool`](./Abilities_and_Spells.md#object-randomstatusfrompool), [`XIsTargetHealth`](./Abilities_and_Spells.md#object-xistargethealth), [`damage_instance`](./Abilities_and_Spells.md#object-damage_instance), [`effects`](./Abilities_and_Spells.md#object-effects), [`self_damage`](./Abilities_and_Spells.md#object-self_damage), [`ROOT` (Enemy_AI)](./Enemy_AI.md#object-root), [`bad`](./Events_and_Encounters.md#object-bad), [`rare`](./Events_and_Encounters.md#object-rare), [`AbilityHealthThreshold`](./Items_and_Equipment.md#object-abilityhealththreshold), [`StatDependentPassive`](./Items_and_Equipment.md#object-statdependentpassive)

**Supported Functions:**<br>
`max(a, b)`, `min(a, b)`, `clamp(val, min, max)`, `pow(base, exp)`, `floor(x)`, `ceil(x)`, `abs(x)`, `round(x)`, `sqrt(x)`

**Common Variables:**<br>
| Variable | Definition |
| :--- | :--- |
| `X` | |
| `str` | |
| `dex` | |
| `int` | |
| `con` | |
| `cha` | |
| `lck` | |
| `mov` | |
| `spd` | |
| `lvl` | |
| `health` | |
| `charge` | |
| `max_range` | |
| `StrengthUp` | |
| `item_aux` | |
| `bonus_melee_damage` | |
| `bonus_ranged_damage` | |
| `bonus_melee_ability_damage` | |
| `bonus_basic_spell_damage` | |

**Examples:**<br>`"max(str, int) + 5"`, `mov+2`, `"floor(lvl/2)"`, `"100-X"`