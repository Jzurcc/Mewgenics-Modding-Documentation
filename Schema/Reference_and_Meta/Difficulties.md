---
title: "Difficulties Schema"
description: "Scaling multipliers across game difficulty settings."
---

# Difficulties Schema


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
> This schema lists the modifiers that are applied to the engine based on the difficulty tier the player selected.

## Usage Example
Here is a real example of this object being defined in the game's data:
```gon
easy {
		elite_budget 0
		champ_budget 0

		elite_buffs 1
		rare_elite_buffs 1
	}
```

## Associated Directory Files
To see extracted instances of this schema in the base game, refer to:
- [`Difficulties.md`](../../Directory/System_and_Engine/Difficulties.md)

---

> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see AUDIT_GAPS.md. For enum values, see [Enums.md](./Enums.md).

This document is an exhaustive, auto-generated dictionary of `.gon` properties relevant to this subsystem. While the overview above provides high-level context, you may still need to infer exact engine execution rules through testing or context clues.

## Difficulties

> **Associated Files:** `data/difficulties.gon`


### Object: `ROOT`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`easy`](./Difficulties.md#object-easy) | Object  | Configuration for easy difficulty, including elite/champ budgets and rewards. | 8 | `{ . . . }` |
| [`hard`](./Difficulties.md#object-hard) | Object  | Configuration for hard difficulty, including elite/champ budgets and rewards. | 8 | `{ . . . }` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


---


### Object: `easy`


**Definition:** Configuration for easy difficulty, including elite/champ budgets and rewards.  
**Total Count:** 67

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Difficulties.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---
### Object: `hard`


**Definition:** Configuration for hard difficulty, including elite/champ budgets and rewards.  
**Total Count:** 47

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Difficulties.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---

