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
| [`set`](./Arrays.md#array-set) | Array / Enum  | Specifies the set name(s) the item belongs to for set bonuses. | 985 | `80s`<br>`90s`<br>`AdvancedAlloy` |
| `Comfort` | Integer | The amount of comfort provided by the furniture piece to the room. | 406 | `-1`<br>`-2`<br>`-3` |
| `Appeal` | Integer | The amount of appeal provided by the furniture piece to the room. | 338 | `-1`<br>`-2`<br>`-4` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 291 | `Default`<br>`FormChange`<br>`Druid` |
| `Stimulation` | Integer | The amount of stimulation provided by the furniture piece to the room. | 268 | `-1`<br>`-2`<br>`1` |
| `Health` | Integer | The amount of health provided by the furniture piece to the room. | 67 | `-1`<br>`-2`<br>`-5` |
| `Evolution` | Integer | The amount of evolution provided by the furniture piece to the room. | 53 | `1`<br>`2`<br>`4` |
| `special` | Boolean |  | 29 | `[special]`<br>`true` |
| `can_be_rare` | Boolean |  | 10 | `false` |
| `BreedSuppression` | Integer | The amount of breeding suppression provided by the furniture piece. | 1 | `1` |
| `FightBonusRewards` | Integer | The number of bonus rewards earned from fights due to the furniture piece. | 1 | `1` |
| `FightRisk` | Integer | The increased risk level of fights triggered by the furniture piece. | 1 | `2` |
| `FoodStorage` | Integer | The amount of food storage capacity added by the furniture piece. | 1 | `40` |
| `removed` | Boolean |  | 1 | `true` |

</details>
---

