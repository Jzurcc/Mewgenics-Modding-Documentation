---
title: "Injuries Schema"
description: "Defines post-combat injuries and permanent disorders."
---

# Injuries Schema

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
- [`Disorders.md`](../../Directory/Statuses_and_Injuries/Disorders.md)

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
| [`con`](../Reference_and_Meta/Enums.md#enum-con) | Enum / Integer  | The Constitution stat value or modifier. | 3 | `-1`<br>`-2`<br>`-3` |
| [`lck`](../Reference_and_Meta/Enums.md#enum-lck) | Enum / Integer | The Luck stat value or modifier. | 3 | `-1`<br>`-2`<br>`-3` |
| [`int`](../Reference_and_Meta/Enums.md#enum-int) | Enum / Integer | The Intelligence stat value or modifier. | 2 | `-1`<br>`-10`<br>`-2` |
| [`cha`](../Reference_and_Meta/Enums.md#enum-cha) | Enum / Integer  | The Charisma stat value or modifier. | 2 | `+1`<br>`-1`<br>`-2` |
| [`str`](../Reference_and_Meta/Enums.md#enum-str) | Enum / Integer | The Strength stat value or modifier. | 2 | `-1`<br>`-2`<br>`-3` |
| [`dex`](../Reference_and_Meta/Enums.md#enum-dex) | Enum / Integer | The Dexterity stat value or modifier. | 2 | `-1`<br>`-2`<br>`-3` |
| [`spd`](../Reference_and_Meta/Enums.md#enum-spd) | Enum / Integer  | The Speed stat value or modifier. | 1 | `-1`<br>`-10`<br>`-2` |

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
| [`head`](../Reference_and_Meta/Enums.md#enum-head) | Enum / Float  | The catalog ID for the cat's head part. | 6 | `-1`<br>`1`<br>`1.3` |
| `body` | Float | The catalog ID for the cat's body part. | 3 | `-1`<br>`1`<br>`1.1` |
| [`legs`](../Reference_and_Meta/Arrays.md#array-legs) | Array | The ID or range of IDs for the leg mutation appearance. | 1 | `-1`<br>`306`<br>`322` |
| [`arms`](../Reference_and_Meta/Arrays.md#array-arms) | Array | The ID or range of IDs for the arm mutation appearance. | 1 | `900`<br>`[10 20]` |
| [`limbs`](../Reference_and_Meta/Arrays.md#array-limbs) | Array | Array of limb IDs associated with this scar. | 1 | `[21 31]` |

</details>


---