# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Math_Equations.md).

## Damage Text Styles

> **Associated Files:** `data/damage_text_styles.gon`


### Context: `ROOT` (26 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`color`](./Arrays.md#array-color) | Array |  | 26 |
| [`right_icon`](./Enums.md#enum-right_icon) | Enum |  | 10 |
| [`back_icon`](./Enums.md#enum-back_icon) | Enum |  | 8 |
| `scale` | Number |  | 4 |
| [`outline_color`](./Enums.md#enum-outline_color) | Enum |  | 2 |
| [`suffix`](./Strings.md#string-suffix) | String |  | 1 |

</details>

---

