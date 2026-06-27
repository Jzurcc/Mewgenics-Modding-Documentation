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
| [`set`](./Enums.md#enum-set) | Array / Enum | Specifies the set name(s) the item belongs to for set bonuses. | 985 |  |
| `Comfort` | Integer | The amount of comfort provided by the furniture piece to the room. | 406 |  |
| `Appeal` | Integer | The amount of appeal provided by the furniture piece to the room. | 338 |  |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 291 |  |
| `Stimulation` | Integer | The amount of stimulation provided by the furniture piece to the room. | 268 |  |
| `Health` | Integer | The amount of health provided by the furniture piece to the room. | 67 |  |
| `Evolution` | Integer | The amount of evolution provided by the furniture piece to the room. | 53 |  |
| `special` | Boolean |  | 29 |  |
| `can_be_rare` | Boolean |  | 10 |  |
| `BreedSuppression` | Integer | The amount of breeding suppression provided by the furniture piece. | 1 |  |
| `FightBonusRewards` | Integer | The number of bonus rewards earned from fights due to the furniture piece. | 1 |  |
| `FightRisk` | Integer | The increased risk level of fights triggered by the furniture piece. | 1 |  |
| `FoodStorage` | Integer | The amount of food storage capacity added by the furniture piece. | 1 |  |
| `removed` | Boolean |  | 1 |  |

</details>

---

