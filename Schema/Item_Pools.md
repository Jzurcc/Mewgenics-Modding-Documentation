# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Item Pools

> **Associated Files:** `data/item_pools/`


### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 13

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `uncommon` | Number | Examples: `35, 75, 60` | 574 |
| `very_rare` | Mixed | Examples: `.01, 2, 1` | 316 |
| `current_chapter_common` | Mixed | Examples: `auto, 55` | 12 |
| `current_chapter_rare` | Mixed | Examples: `auto, 10` | 12 |
| `current_chapter_uncommon` | Mixed | Examples: `35, auto` | 12 |
| `current_chapter_very_rare` | Mixed | Examples: `auto, 1` | 12 |
| `chapter_rare` | Number | Examples: `1` | 10 |
| `chapter_common` | Number | Examples: `1` | 7 |
| `chapter` | Number | Examples: `1` | 6 |
| `Chicken` | Mixed | Examples: `.1, 2, .01` | 6 |
| `consumables` | Number | Examples: `60, 10` | 6 |
| `basic_consumables` | Number | Examples: `90, 100` | 4 |
| `FoodBig` | Number | Examples: `2, 1` | 4 |
| `FoodMedium` | Number | Examples: `1, 5` | 4 |
| `shop_common` | Number | Examples: `1` | 4 |
| `Antidote` | Number | Examples: `1` | 2 |
| [`BagOfSeeds`](./Enums.md#enum-bagofseeds) | Enum | Examples: `.3` | 2 |
| [`BirdFeed`](./Enums.md#enum-birdfeed) | Enum | Examples: `.3` | 2 |
| [`BirdPoopHat`](./Enums.md#enum-birdpoophat) | Enum | Examples: `.3` | 2 |
| `Catnip` | Number | Examples: `3` | 2 |
| `CatnipBig` | Number | Examples: `2` | 2 |
| `consumables_consumable_common` | Number | Examples: `50` | 2 |
| `consumables_consumable_rare` | Number | Examples: `15` | 2 |
| `consumables_consumable_uncommon` | Number | Examples: `35` | 2 |
| `consumables_consumable_very_rare` | Number | Examples: `1` | 2 |
| [`DeadHummingbird`](./Enums.md#enum-deadhummingbird) | Enum | Examples: `.3` | 2 |
| [`general_common`](./Enums.md#enum-general_common) | Enum | Examples: `auto` | 2 |
| [`general_rare`](./Enums.md#enum-general_rare) | Enum | Examples: `auto` | 2 |
| [`general_uncommon`](./Enums.md#enum-general_uncommon) | Enum | Examples: `auto` | 2 |
| [`general_very_rare`](./Enums.md#enum-general_very_rare) | Enum | Examples: `auto` | 2 |
| [`GlowingSeed`](./Enums.md#enum-glowingseed) | Enum | Examples: `.3` | 2 |
| [`GoldenEgg`](./Enums.md#enum-goldenegg) | Enum | Examples: `.3` | 2 |
| [`HarpysClaw`](./Enums.md#enum-harpysclaw) | Enum | Examples: `.5` | 2 |
| [`LostSoul`](./Enums.md#enum-lostsoul) | Enum | Examples: `.5` | 2 |
| [`MagicSeed`](./Enums.md#enum-magicseed) | Enum | Examples: `.3` | 2 |
| [`Parousworm`](./Enums.md#enum-parousworm) | Enum | Examples: `.5` | 2 |
| [`PeaceSymbol`](./Enums.md#enum-peacesymbol) | Enum | Examples: `.3` | 2 |
| [`PeaceSymbolFacePaint`](./Enums.md#enum-peacesymbolfacepaint) | Enum | Examples: `.3` | 2 |
| `pills` | Number | Examples: `7` | 2 |
| [`RaptorEgg`](./Enums.md#enum-raptoregg) | Enum | Examples: `.1` | 2 |
| [`RavenFeather`](./Enums.md#enum-ravenfeather) | Enum | Examples: `.3` | 2 |
| [`TieDyeBandana`](./Enums.md#enum-tiedyebandana) | Enum | Examples: `.3` | 2 |
| `Turkey` | Number | Examples: `2` | 2 |
| [`WeirdEgg`](./Enums.md#enum-weirdegg) | Enum | Examples: `.3` | 2 |
| [`WishBone`](./Enums.md#enum-wishbone) | Enum | Examples: `.3` | 2 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Properties for configuring event outcomes (rewards, penalties, dialog options, status applications). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 0 |

</details>

---

