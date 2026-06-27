# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Injuries

> **Associated Files:** `data/injuries.gon`


### Object: `ROOT`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 13

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 461 | `{ . . . }` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 155 | Default<br>FormChange<br>Druid |
| `id` | Integer | The unique numerical identifier for this injury or status effect. | 14 | `-1`<br>`0`<br>`1` |
| [`deathsound`](./Enums.md#enum-deathsound) | Enum | The name of the sound effect played when the unit dies from this injury. | 13 | `Injury_Bleed`<br>`Injury_BrokenLeg`<br>`Injury_BrokenPaw` |
| [`text`](./Strings.md#string-text) | String | The localization key for the name of this injury. | 13 | `""`<br>`"COMBAT_POPUP_RECHARGED"`<br>`"INJURY_NAME_BROKENLEG"` |
| [`scars`](./Miscellaneous.md#object-scars) | Object | An object mapping body parts to ranges of scar texture indices applied on injury. | 10 | `{ . . . }` |

</details>


---


### Object: `stats`


**Definition:** A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.).
**Total Count:** 497

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`con`](./Enums.md#enum-con) | Enum / Integer  | The Constitution stat value or modifier. | 34 | `-1`<br>`-2`<br>`-3` |
| [`spd`](./Enums.md#enum-spd) | Enum / Integer  | The Speed stat value or modifier. | 27 | `-1`<br>`-10`<br>`-2` |
| [`cha`](./Enums.md#enum-cha) | Enum / Integer  | The Charisma stat value or modifier. | 24 | `+1`<br>`-1`<br>`-2` |
| [`int`](./Enums.md#enum-int) | Enum / Integer | The Intelligence stat value or modifier. | 24 | `-1`<br>`-10`<br>`-2` |
| [`str`](./Enums.md#enum-str) | Enum / Integer | The Strength stat value or modifier. | 22 | `-1`<br>`-2`<br>`-3` |
| [`dex`](./Enums.md#enum-dex) | Enum / Integer | The Dexterity stat value or modifier. | 18 | `-1`<br>`-2`<br>`-3` |
| [`lck`](./Enums.md#enum-lck) | Enum / Integer | The Luck stat value or modifier. | 16 | `-1`<br>`-2`<br>`-3` |

</details>


---


### Object: `scars`


**Definition:** An object mapping body parts to ranges of scar texture indices applied on injury.
**Total Count:** 10

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`head`](./Enums.md#enum-head) | Enum / Float  | The catalog ID for the cat's head part. | 6 | `-1`<br>`1`<br>`1.3` |
| [`body`](./Arrays.md#array-body) | Float | The catalog ID for the cat's body part. | 3 | `-1`<br>`1`<br>`1.1` |
| [`arms`](./Arrays.md#array-arms) | Array | The ID or range of IDs for the arm mutation appearance. | 1 | `900`<br>`[10 20]` |
| [`legs`](./Arrays.md#array-legs) | Array | The ID or range of IDs for the leg mutation appearance. | 1 | `-1`<br>`306`<br>`322` |
| [`limbs`](./Arrays.md#array-limbs) | Array | Array of limb IDs associated with this scar. | 1 | `[21 31]` |

</details>


---