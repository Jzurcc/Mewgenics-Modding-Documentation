---
title: "Injuries Schema"
description: "Defines post-combat injuries and permanent disorders."
---

# Injuries Schema


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
> This schema describes negative traits that cats acquire if they fall in combat, persisting until treated in the house.

## Usage Example
Here is a real example of this object being defined in the game's data:
```gon
str {
    text "INJURY_NAME_BROKENPAW"
    id 0

    stats {
        str -1
    }

    scars {
        arms [10 20]
    }

    alt_animations [
        [dying, brokenPaw]
        [dead, brokenPawLoop]
        [deadhit, brokenPawHit]
        [weak, brokenPawIdle]
        [walk, brokenPawWalk]
        //hit_brokenPaw
    ]

    deathsound Injury_BrokenPaw
}
```

## Associated Directory Files
To see extracted instances of this schema in the base game, refer to:
- [`Injuries.md`](../../Directory/Statuses_and_Injuries/Injuries.md)

---



This document is an exhaustive, auto-generated dictionary of `.gon` properties relevant to this subsystem. While the overview above provides high-level context, you may still need to infer exact engine execution rules through testing or context clues.

## Injuries

> **Associated Files:** `data/injuries.gon`


### Object: `ROOT`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 13

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `id` | Integer | The unique numerical identifier for this injury or status effect. | 13 | `-1`<br>`0`<br>`1` |
| [`text`](../Assets_and_Localization/Strings.md#string-text) | String | The localization key for the name of this injury. | 13 | `""`<br>`"COMBAT_POPUP_RECHARGED"`<br>`"INJURY_NAME_BROKENLEG"` |
| [`deathsound`](../Reference_and_Meta/Enums.md#enum-deathsound) | Enum | The name of the sound effect played when the unit dies from this injury. | 13 | `Injury_Bleed`<br>`Injury_BrokenLeg`<br>`Injury_BrokenPaw` |
| [`stats`](./Injuries.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 12 | `{ . . . }` |
| [`scars`](./Injuries.md#object-scars) | Object | An object mapping body parts to ranges of scar texture indices applied on injury. | 10 | `{ . . . }` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


---


### Object: `stats`


**Definition:** A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.).  
**Total Count:** 498

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Injuries.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `con` | Integer | The Constitution stat value or modifier. | 3 | `-1`<br>`-2`<br>`-3` |
| `lck` | Integer | The Luck stat value or modifier. | 3 | `-1`<br>`-2`<br>`-3` |
| `int` | Integer | The Intelligence stat value or modifier. | 2 | `-1`<br>`-10`<br>`-2` |
| `cha` | Integer | The Charisma stat value or modifier. | 2 | `+1`<br>`-1`<br>`-2` |
| `str` | Integer | The Strength stat value or modifier. | 2 | `-1`<br>`-2`<br>`-3` |
| `dex` | Integer | The Dexterity stat value or modifier. | 2 | `-1`<br>`-2`<br>`-3` |
| `spd` | Integer | The Speed stat value or modifier. | 1 | `-1`<br>`-10`<br>`-2` |

</details>


---


### Object: `scars`


**Definition:** An object mapping body parts to ranges of scar texture indices applied on injury.  
**Total Count:** 10

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Injuries.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `head` | Float | The catalog ID for the cat's head part. | 6 | `-1`<br>`1`<br>`1.3` |
| `body` | Float | The catalog ID for the cat's body part. | 3 | `-1`<br>`1`<br>`1.1` |
| [`legs`](../Reference_and_Meta/Arrays.md#array-legs) | Array | The ID or range of IDs for the leg mutation appearance. | 1 | `-1`<br>`306`<br>`322` |
| [`arms`](../Reference_and_Meta/Arrays.md#array-arms) | Array | The ID or range of IDs for the arm mutation appearance. | 1 | `900`<br>`[10 20]` |
| [`limbs`](../Reference_and_Meta/Arrays.md#array-limbs) | Array | Array of limb IDs associated with this scar. | 1 | `[21 31]` |

</details>


---