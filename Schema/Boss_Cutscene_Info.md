# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Math_Equations.md).

## Boss Cutscene Info

> **Associated Files:** `data/boss_cutscene_info.gon`


### Context: `ROOT` (67 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`frame_label`](./Enums.md#enum-frame_label) | Enum |  | 67 |
| [`name`](./Enums.md#enum-name) | String |  | 67 |
| [`quotes`](./Arrays.md#array-quotes) | Array |  | 36 |

</details>

---

