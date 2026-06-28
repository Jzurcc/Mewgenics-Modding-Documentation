---
title: "Math Equations Schema"
description: "Valid syntax and variables for Equation strings."
---

# Math Equations Schema

## Overview
This schema specifies how to write math equations in GON strings, allowing values to scale dynamically based on player stats.

## Usage Example
Here is a real example of this object being defined in the game's data:
```gon
DamageCalc {
    damage_calc "base_damage * (1 + bonus_strength / 100)"
}
```

---



In the Mewgenics engine, many numeric fields can accept an inline math equation string instead of a raw number.

> **Referenced by:** [`Conditional_Ally`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_ally), [`Conditional_Displaceable`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_displaceable), [`Conditional_HealthThreshold`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_healththreshold), [`Else`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-else), [`RandomStatusFromPool`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-randomstatusfrompool), [`XIsTargetHealth`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-xistargethealth), [`damage_instance`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-damage_instance), [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects), [`self_damage`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-self_damage), [`ROOT` (Enemy_AI)](../Core_Entities_and_Combat/Enemy_AI.md#object-root), [`bad`](../World_Maps_and_Events/Events_and_Encounters.md#object-bad), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare), [`AbilityHealthThreshold`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-abilityhealththreshold), [`StatDependentPassive`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statdependentpassive)

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