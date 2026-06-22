# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** Some keys labeled as `Number` actually support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Math_Equations.md).

## Furniture & Metaprogression

> **Associated Files:** `data/furniture_effects.gon`


### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 634

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Effects}`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |  |
| [`desc`](./Strings.md#string-desc) | String |  | 634 |
| [`name`](./Strings.md#string-name) | String |  | 634 |
| `Comfort` | Number | Applies or references the 'Comfort' effect/state. | 406 |
| `Appeal` | Number | Applies or references the 'Appeal' effect/state. | 338 |
| `Stimulation` | Number | Applies or references the 'Stimulation' effect/state. | 268 |
| [`set`](./Enums.md#enum-set) | Enum |  | 220 |
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

