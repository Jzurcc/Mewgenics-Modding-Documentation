# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see AUDIT_GAPS.md. For enum values, see [Enums.md](./Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Difficulties

> **Associated Files:** `data/difficulties.gon`


### Object: `ROOT`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 155 | Default<br>FormChange<br>Druid |
| [`hard`](./Miscellaneous.md#object-hard) | Object  | Configuration for hard difficulty, including elite/champ budgets and rewards. | 23 | `{ . . . }` |
| [`easy`](./Difficulties.md#object-easy) | Object  | Configuration for easy difficulty, including elite/champ budgets and rewards. | 20 | `{ . . . }` |

</details>


---


### Object: `hard`


**Definition:** Configuration for hard difficulty, including elite/champ budgets and rewards.
**Total Count:** 21

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `easy`


**Definition:** Configuration for easy difficulty, including elite/champ budgets and rewards.
**Total Count:** 8

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---