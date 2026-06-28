# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see AUDIT_GAPS.md. For enum values, see [Enums.md](../Reference_and_Meta/Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Spawns & Enemy Pools

> **Associated Files:** `data/spawns.gon`


### Object: `ROOT`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 550

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`image`](../Assets_and_Localization/Strings.md#string-image) | String | Array of image filenames used for the related editor object. | 578 | `"empty.png"`<br>`["1.png" "pyrophina.png"]`<br>`["1.png" "zaratana.png"]` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 155 | Default<br>FormChange<br>Druid |
| `value` | Equation | The numeric value or formula associated with the buff. | 54 | `.5`<br>`0`<br>`1` |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 3 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`element`](../Reference_and_Meta/Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 1 | `Electric`<br>`Fire`<br>`Gravity` |

</details>


---


### Object: `editor`


**Definition:** An object containing metadata for the level editor, such as category, image, and name.
**Total Count:** 578

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 3 | `damage_instance`<br>`spell`<br>`false` |
`damage_instance`<br>`spell`<br>`self_damage`

</details>


---


### Object: `weather_element_alt`


**Definition:** Defines an alternative weather element, specifying its element type and associated object.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---