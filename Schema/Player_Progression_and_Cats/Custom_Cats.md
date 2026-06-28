# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see AUDIT_GAPS.md. For enum values, see [Enums.md](../Reference_and_Meta/Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Custom Cats

> **Associated Files:** `data/custom_cats.gon`


### Object: `ROOT`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 211

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 155 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `arm1`


**Definition:** The catalog ID for the cat's first arm part.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `frame` | Integer | The sprite frame index to display. | 2 | `1`<br>`10`<br>`100` |

</details>


---


### Object: `arm2`


**Definition:** The catalog ID for the cat's second arm part.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `frame` | Integer | The sprite frame index to display. | 2 | `1`<br>`10`<br>`100` |

</details>


---