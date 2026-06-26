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
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Defines the unit's base stats (strength, dexterity, constitution, intelligence, speed). | 461 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 291 ||
| `id` | Integer | Specifies the unique identifier for the object or room, used for referencing or categorization. | 14 ||
| [`deathsound`](./Enums.md#enum-deathsound) | Enum || 13 ||
| [`text`](./Strings.md#string-text) | String || 13 ||
| [`scars`](#object-scars) | Object || 10 ||

</details>

---

### Object: `stats`


**Definition:** Core character metrics (Health, Strength, etc.).  
**Total Count:** 497


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `con` | Enum / Integer | The constitution stat value or modifier for the unit. | 34 ||
| `spd` | Enum / Integer | The speed stat value or modifier for the unit. | 27 ||
| `cha` | Enum / Integer | Specifies the charisma stat value as an integer or 'aux' for auxiliary stat assignment. | 24 ||
| `int` | Enum / Integer || 24 ||
| `str` | Enum / Integer || 22 ||
| `dex` | Enum / Integer || 18 ||
| `lck` | Enum / Integer || 16 ||

</details>

---

### Object: `scars`


**Definition:** No definition provided.  
**Total Count:** 10


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`head`](./Arrays.md#array-head) | Enum / Number | The visual ID (integer) of the head part applied to the cat. | 6 ||
| [`body`](./Arrays.md#array-body) | Number | The visual ID (number) of the body part applied to the cat. | 3 ||
| [`arms`](./Arrays.md#array-arms) | Array || 1 ||
| [`legs`](./Arrays.md#array-legs) | Array || 1 ||
| [`limbs`](./Arrays.md#array-limbs) | Array || 1 ||

</details>

---

