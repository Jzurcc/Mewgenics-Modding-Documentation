# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Math_Equations.md).

## Item Pools

> **Associated Files:** `data/item_pools/`


### Context: `ROOT` (13 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `rare` | Number |  | 13 |
| `uncommon` | Number |  | 12 |
| `very_rare` | Number |  | 11 |
| `common` | Number |  | 10 |
| [`current_chapter_common`](./Enums.md#enum-current_chapter_common) | Enum |  | 6 |
| [`current_chapter_rare`](./Enums.md#enum-current_chapter_rare) | Enum |  | 6 |
| [`current_chapter_uncommon`](./Enums.md#enum-current_chapter_uncommon) | Enum |  | 6 |
| [`current_chapter_very_rare`](./Enums.md#enum-current_chapter_very_rare) | Enum |  | 6 |
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
| [`BagOfSeeds`](./Enums.md#enum-bagofseeds) | Enum |  | 1 |
| [`BirdFeed`](./Enums.md#enum-birdfeed) | Enum |  | 1 |
| [`BirdPoopHat`](./Enums.md#enum-birdpoophat) | Enum |  | 1 |
| `Catnip` | Number |  | 1 |
| `CatnipBig` | Number |  | 1 |
| [`DeadHummingbird`](./Enums.md#enum-deadhummingbird) | Enum |  | 1 |
| [`GlowingSeed`](./Enums.md#enum-glowingseed) | Enum |  | 1 |
| [`GoldenEgg`](./Enums.md#enum-goldenegg) | Enum |  | 1 |
| [`HarpysClaw`](./Enums.md#enum-harpysclaw) | Enum |  | 1 |
| [`LostSoul`](./Enums.md#enum-lostsoul) | Enum |  | 1 |
| [`MagicSeed`](./Enums.md#enum-magicseed) | Enum |  | 1 |
| [`Parousworm`](./Enums.md#enum-parousworm) | Enum |  | 1 |
| [`PeaceSymbol`](./Enums.md#enum-peacesymbol) | Enum |  | 1 |
| [`PeaceSymbolFacePaint`](./Enums.md#enum-peacesymbolfacepaint) | Enum |  | 1 |
| [`RaptorEgg`](./Enums.md#enum-raptoregg) | Enum |  | 1 |
| [`RavenFeather`](./Enums.md#enum-ravenfeather) | Enum |  | 1 |
| [`TieDyeBandana`](./Enums.md#enum-tiedyebandana) | Enum |  | 1 |
| `Turkey` | Number |  | 1 |
| [`WeirdEgg`](./Enums.md#enum-weirdegg) | Enum |  | 1 |
| [`WishBone`](./Enums.md#enum-wishbone) | Enum |  | 1 |
| `consumables_consumable_common` | Number |  | 1 |
| `consumables_consumable_rare` | Number |  | 1 |
| `consumables_consumable_uncommon` | Number |  | 1 |
| `consumables_consumable_very_rare` | Number |  | 1 |
| [`general_common`](./Enums.md#enum-general_common) | Enum |  | 1 |
| [`general_rare`](./Enums.md#enum-general_rare) | Enum |  | 1 |
| [`general_uncommon`](./Enums.md#enum-general_uncommon) | Enum |  | 1 |
| [`general_very_rare`](./Enums.md#enum-general_very_rare) | Enum |  | 1 |
| `pills` | Number |  | 1 |

</details>

---

