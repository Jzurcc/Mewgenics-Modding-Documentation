# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Enums.md#enum-mathequation).

## Furniture & Metaprogression

### Context: `ROOT`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | [`Enum/String`](./Enums.md#enum-desc) | `FURNITURE_DESC_AUTOFEEDER, FURNITURE_DESC_SPECIAL_FOODBOX, FURNITURE_DESC_POOP` |  |
| `name` | [`Enum/String`](./Enums.md#enum-name) | `FURNITURE_NAME_SPECIAL_FOODBOX, FURNITURE_NAME_AUTOFEEDER, FURNITURE_NAME_POOP` |  |
| `Comfort` | Number | `-5, -2, 5` | Applies or references the 'Comfort' effect/state. |
| `Appeal` | Number | `2, 1, 5` | Applies or references the 'Appeal' effect/state. |
| `Stimulation` | Number | `2, 1, 5` | Applies or references the 'Stimulation' effect/state. |
| `set` | [`Enum/String`](./Enums.md#enum-set) | `spider, sewn, junk` |  |
| `Health` | Number | `-2, 5, -1` | Applies or references the 'Health' effect/state. |
| `Evolution` | Number | `2, 1, 5` | Applies or references the 'Evolution' effect/state. |
| `can_be_rare` | Boolean | `false` |  |
| `special` | Boolean | `true` |  |
| `BreedSuppression` | Number | `1` | Applies or references the 'BreedSuppression' effect/state. |
| `FightBonusRewards` | Number | `1` | Applies or references the 'FightBonusRewards' effect/state. |
| `FightRisk` | Number | `2` | Applies or references the 'FightRisk' effect/state. |
| `FoodStorage` | Number | `40` | Applies or references the 'FoodStorage' effect/state. |
| `removed` | Boolean | `true` |  |

</details>

---

