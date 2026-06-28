# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see AUDIT_GAPS.md. For enum values, see [Enums.md](../Reference_and_Meta/Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Damage Text Styles

> **Associated Files:** `data/damage_text_styles.gon`


### Object: `ROOT`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 26

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 155 | Default<br>FormChange<br>Druid |
| [`color`](../Reference_and_Meta/Arrays.md#array-color) | Array | The RGB color of the light source. | 26 | `[.27 .47 .18]`<br>`[.3, .7, 1]`<br>`[.32 .10 .10]` |
| `right_icon` | String | The name of the icon to display on the right side of the damage text. | 10 | `coin`<br>`divineshield`<br>`heal` |
| `back_icon` | String | The name of the icon to display behind the damage text. | 8 | `bleed`<br>`burn`<br>`confusion` |
| [`outline_color`](../Reference_and_Meta/Enums.md#enum-outline_color) | Enum | The color of the text outline. | 2 | `white` |
| [`suffix`](./Strings.md#string-suffix) | String | A string appended to the damage text. | 1 | `"!!!"` |

</details>


---