# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Enums.md#enum-mathequation).

## Furniture & Metaprogression

### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/634) |
| :--- | :--- | :--- | :--- |
| [`desc`](./Enums.md#enum-desc) | Enum/String |  | 634 |
| [`name`](./Enums.md#enum-name) | Enum/String |  | 634 |
| `Comfort` | Number | Applies or references the 'Comfort' effect/state. | 406 |
| `Appeal` | Number | Applies or references the 'Appeal' effect/state. | 338 |
| `Stimulation` | Number | Applies or references the 'Stimulation' effect/state. | 268 |
| [`set`](./Enums.md#enum-set) | Enum/String |  | 220 |
| `Health` | Number | Applies or references the 'Health' effect/state. | 67 |
| `Evolution` | Number | Applies or references the 'Evolution' effect/state. | 53 |
| `can_be_rare` | Boolean |  | 10 |
| `special` | Boolean |  | 10 |
| `BreedSuppression` | Number | Applies or references the 'BreedSuppression' effect/state. | 1 |
| `FightBonusRewards` | Number | Applies or references the 'FightBonusRewards' effect/state. | 1 |
| `FightRisk` | Number | Applies or references the 'FightRisk' effect/state. | 1 |
| `FoodStorage` | Number | Applies or references the 'FoodStorage' effect/state. | 1 |
| `removed` | Boolean |  | 1 |

</details>

---

