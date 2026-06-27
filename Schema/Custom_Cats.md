# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Custom Cats

> **Associated Files:** `data/custom_cats.gon`


### Object: `ROOT`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 211

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 155 | `Default`<br>`FormChange`<br>`Druid` |

</details>


---


### Object: `arm1`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `frame` | Integer | The sprite frame index to display. | 2 | `1`<br>`10`<br>`100` |

</details>


---


### Object: `arm2`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `frame` | Integer | The sprite frame index to display. | 2 | `1`<br>`10`<br>`100` |

</details>


---