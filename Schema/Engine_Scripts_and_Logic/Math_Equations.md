---
title: "Math Equations Schema"
description: "Valid syntax and variables for Equation strings."
---

# Math Equations Schema


<details open>
<summary><strong>Quick Navigation</strong></summary>

<table>
  <tr>
    <td width="22%"><strong>Core Entities & Combat</strong></td>
    <td><a href="../Core_Entities_and_Combat/Abilities_and_Spells.md">Abilities & Spells</a> • <a href="../Core_Entities_and_Combat/Characters_and_Bosses.md">Characters & Bosses</a> • <a href="../Core_Entities_and_Combat/Items_and_Equipment.md">Items & Equipment</a> • <a href="../Core_Entities_and_Combat/Passives_and_Statuses.md">Passives & Statuses</a> • <a href="../Core_Entities_and_Combat/Elite_Buffs.md">Elite Buffs</a> • <a href="../Core_Entities_and_Combat/Enemy_AI.md">Enemy AI</a> • <a href="../Core_Entities_and_Combat/Status_Effect_Keywords.md">Status Keywords</a></td>
  </tr>
  <tr>
    <td><strong>Engine Scripts & Logic</strong></td>
    <td><a href="../Engine_Scripts_and_Logic/Engine_LogicKeys.md">Logic Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_EventKeys.md">Event Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_DamagingKeys.md">Damaging Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md">Status & Passive Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_GlobalModifierKeys.md">Global Modifiers</a> • <a href="../Engine_Scripts_and_Logic/Math_Equations.md">Math Equations</a></td>
  </tr>
  <tr>
    <td><strong>Player Progression & Cats</strong></td>
    <td><a href="../Player_Progression_and_Cats/Cat_Classes.md">Cat Classes</a> • <a href="../Player_Progression_and_Cats/Cat_Mutations.md">Cat Mutations</a> • <a href="../Player_Progression_and_Cats/Custom_Cats.md">Custom Cats</a> • <a href="../Player_Progression_and_Cats/Injuries.md">Injuries</a> • <a href="../Player_Progression_and_Cats/Progression_Unlocks.md">Progression Unlocks</a> • <a href="../Player_Progression_and_Cats/Combat_Rewards.md">Combat Rewards</a></td>
  </tr>
  <tr>
    <td><strong>World, Maps & Events</strong></td>
    <td><a href="../World_Maps_and_Events/Events_and_Encounters.md">Events & Encounters</a> • <a href="../World_Maps_and_Events/House_and_Environment.md">House & Environment</a> • <a href="../World_Maps_and_Events/Map_Generation_and_Routing.md">Map Gen & Routing</a> • <a href="../World_Maps_and_Events/Furniture_and_Metaprogression.md">Furniture & Meta</a> • <a href="../World_Maps_and_Events/Shops.md">Shops</a> • <a href="../World_Maps_and_Events/Spawns_and_Enemy_Pools.md">Spawns & Enemy Pools</a> • <a href="../World_Maps_and_Events/Boss_Cutscene_Info.md">Boss Cutscenes</a> • <a href="../World_Maps_and_Events/NPC_Scripts.md">NPC Scripts</a></td>
  </tr>
  <tr>
    <td><strong>Assets & Localization</strong></td>
    <td><a href="../Assets_and_Localization/Audio_SFX_Dictionary.md">Audio SFX</a> • <a href="../Assets_and_Localization/Particles_and_VFX_Dictionary.md">Particles & VFX</a> • <a href="../Assets_and_Localization/Damage_Text_Styles.md">Damage Text</a> • <a href="../Assets_and_Localization/Localization_Guide.md">Localization Guide</a> • <a href="../Assets_and_Localization/Text_Formatting_and_Effects.md">Text Formatting</a> • <a href="../Assets_and_Localization/Strings.md">Strings</a></td>
  </tr>
  <tr>
    <td><strong>Reference & Meta</strong></td>
    <td><a href="../Reference_and_Meta/Enums.md">Enums</a> • <a href="../Reference_and_Meta/Arrays.md">Arrays</a> • <a href="../Reference_and_Meta/Item_Pools.md">Item Pools</a> • <a href="../Reference_and_Meta/Difficulties.md">Difficulties</a> • <a href="../Reference_and_Meta/Engine_Hidden_Passives_and_Statuses.md">Hidden Passives</a> • <a href="../Reference_and_Meta/Passive_Identifiers_Audit.md">Passive Audit</a> • <a href="../Reference_and_Meta/Engine_Uncategorized_Resources.md">Uncategorized Keys</a> • <a href="../Reference_and_Meta/Miscellaneous.md">Miscellaneous</a></td>
  </tr>
</table>

</details>

## Overview
> [!NOTE]
> This schema specifies how to write math equations in GON strings, allowing values to scale dynamically based on player stats.

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
| `aux` | |
| `bonus_melee_damage` | |
| `bonus_ranged_damage` | |
| `bonus_melee_ability_damage` | |
| `bonus_basic_spell_damage` | |

**Examples:**<br>`"max(str, int) + 5"`, `mov+2`, `"floor(lvl/2)"`, `"100-X"`