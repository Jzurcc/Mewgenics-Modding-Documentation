# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Enums.md#enum-mathequation).

## Item Pools

### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/13) |
| :--- | :--- | :--- | :--- |
| `rare` | Number |  | 13 |
| `uncommon` | Number |  | 12 |
| `very_rare` | Number |  | 11 |
| `common` | Number |  | 10 |
| `current_chapter_common` | Number |  | 6 |
| `current_chapter_rare` | Number |  | 6 |
| `current_chapter_uncommon` | Number |  | 6 |
| `current_chapter_very_rare` | Number |  | 6 |
| `chapter_rare` | Number |  | 5 |
| `Chicken` | Number |  | 3 |
| `chapter` | Number |  | 3 |
| `chapter_common` | Number |  | 3 |
| `consumables` | Number |  | 3 |
| `FoodBig` | Number |  | 2 |
| `FoodMedium` | Number |  | 2 |
| `basic_consumables` | Number |  | 2 |
| `shop_common` | Number |  | 2 |
| `Antidote` | Number |  | 1 |
| [`BagOfSeeds`](./Enums.md#enum-bagofseeds) | Enum/String |  | 1 |
| [`BirdFeed`](./Enums.md#enum-birdfeed) | Enum/String |  | 1 |
| [`BirdPoopHat`](./Enums.md#enum-birdpoophat) | Enum/String |  | 1 |
| `Catnip` | Number |  | 1 |
| `CatnipBig` | Number |  | 1 |
| [`DeadHummingbird`](./Enums.md#enum-deadhummingbird) | Enum/String |  | 1 |
| [`GlowingSeed`](./Enums.md#enum-glowingseed) | Enum/String |  | 1 |
| [`GoldenEgg`](./Enums.md#enum-goldenegg) | Enum/String |  | 1 |
| [`HarpysClaw`](./Enums.md#enum-harpysclaw) | Enum/String |  | 1 |
| [`LostSoul`](./Enums.md#enum-lostsoul) | Enum/String |  | 1 |
| [`MagicSeed`](./Enums.md#enum-magicseed) | Enum/String |  | 1 |
| [`Parousworm`](./Enums.md#enum-parousworm) | Enum/String |  | 1 |
| [`PeaceSymbol`](./Enums.md#enum-peacesymbol) | Enum/String |  | 1 |
| [`PeaceSymbolFacePaint`](./Enums.md#enum-peacesymbolfacepaint) | Enum/String |  | 1 |
| [`RaptorEgg`](./Enums.md#enum-raptoregg) | Enum/String |  | 1 |
| [`RavenFeather`](./Enums.md#enum-ravenfeather) | Enum/String |  | 1 |
| [`TieDyeBandana`](./Enums.md#enum-tiedyebandana) | Enum/String |  | 1 |
| `Turkey` | Number |  | 1 |
| [`WeirdEgg`](./Enums.md#enum-weirdegg) | Enum/String |  | 1 |
| [`WishBone`](./Enums.md#enum-wishbone) | Enum/String |  | 1 |
| `consumables_consumable_common` | Number |  | 1 |
| `consumables_consumable_rare` | Number |  | 1 |
| `consumables_consumable_uncommon` | Number |  | 1 |
| `consumables_consumable_very_rare` | Number |  | 1 |
| [`general_common`](./Enums.md#enum-general_common) | Enum/String |  | 1 |
| [`general_rare`](./Enums.md#enum-general_rare) | Enum/String |  | 1 |
| [`general_uncommon`](./Enums.md#enum-general_uncommon) | Enum/String |  | 1 |
| [`general_very_rare`](./Enums.md#enum-general_very_rare) | Enum/String |  | 1 |
| `pills` | Number |  | 1 |

</details>

---

