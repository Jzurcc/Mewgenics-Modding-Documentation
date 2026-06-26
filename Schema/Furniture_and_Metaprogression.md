# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


## Furniture & Metaprogression

> **Associated Files:** `data/furniture_effects.gon`

### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 634

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`set`](./Enums.md#enum-set) | Array / Enum |  | 1504 |  |
| `Comfort` | Integer | Applies or references the 'Comfort' effect/state. | 406 |  |
| `Appeal` | Integer | Applies or references the 'Appeal' effect/state. | 338 |  |
| `Stimulation` | Integer | Applies or references the 'Stimulation' effect/state. | 268 |  |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 206 |  |
| `Health` | Integer | Applies or references the 'Health' effect/state. | 67 |  |
| `Evolution` | Integer | Applies or references the 'Evolution' effect/state. | 53 |  |
| `can_be_rare` | Boolean |  | 10 |  |
| `special` | Boolean |  | 10 |  |
| `BreedSuppression` | Integer | Applies or references the 'BreedSuppression' effect/state. | 1 |  |
| `FightBonusRewards` | Integer | Applies or references the 'FightBonusRewards' effect/state. | 1 |  |
| `FightRisk` | Integer | Applies or references the 'FightRisk' effect/state. | 1 |  |
| `FoodStorage` | Integer | Applies or references the 'FoodStorage' effect/state. | 1 |  |
| `removed` | Boolean |  | 1 |  |

</details>

---

