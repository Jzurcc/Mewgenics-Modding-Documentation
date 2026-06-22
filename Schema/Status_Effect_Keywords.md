# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Enums.md#enum-mathequation).

## Status Effect Keywords

### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/236) |
| :--- | :--- | :--- | :--- |
| `name` | String |  | 236 |
| `tooltip` | String |  | 157 |
| `tooltip_stackless` | String |  | 76 |
| `tooltip_stacks` | String |  | 69 |
| [`alias`](./Enums.md#enum-alias) | Enum/String |  | 57 |
| `icon_frame` | Number |  | 20 |
| `tooltip_stacks_singular` | String |  | 15 |
| `tooltip_stacks_neg` | String |  | 13 |
| `name_stacks_neg` | String |  | 11 |
| `tooltip_stacks_pos` | String |  | 10 |
| `name_reference_applier` | String |  | 3 |
| `tooltip_reference_applier` | String |  | 3 |
| `tooltip_stackless_neg` | String |  | 3 |
| `tooltip_stackless_pos` | String |  | 2 |

</details>

---
