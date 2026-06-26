# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Item Pools

> **Associated Files:** `data/item_pools/`


### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 13

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Properties for configuring event outcomes (rewards, penalties, dialog options, status applications). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 664 |  |
| `chapter_item_pool` | Enum |  | 19 | `cavesitems` (Enum), `alleyitems` (Enum) |
| `uncommon` | Number | Examples: `35, 75, 60` | 12 |  |
| `very_rare` | Mixed | Examples: `.01, 2, 1` | 11 |  |
| `current_chapter_common` | Mixed | Examples: `auto, 55` | 2 |  |
| `current_chapter_rare` | Mixed | Examples: `auto, 10` | 2 |  |
| `current_chapter_uncommon` | Mixed | Examples: `35, auto` | 2 |  |
| `current_chapter_very_rare` | Mixed | Examples: `auto, 1` | 2 |  |
| `chapter_rare` | Number | Examples: `1` | 5 |  |
| `chapter_common` | Number | Examples: `1` | 3 |  |
| `chapter` | Enum | Examples: `1` | 3 |  |
| `Chicken` | Mixed | Examples: `.1, 2, .01` | 3 |  |
| `consumables` | Number | Examples: `60, 10` | 3 |  |
| `basic_consumables` | Number | Examples: `90, 100` | 2 |  |
| [`FoodBig`](Engine_LogicKeys.md#object-foodbig) | Object | Examples: `2, 1` | 2 ||
| [`FoodMedium`](Engine_LogicKeys.md#object-foodmedium) | Object | Examples: `1, 5` | 2 ||
| `shop_common` | Number | Examples: `1` | 2 ||
| [`Antidote`](Engine_LogicKeys.md#object-antidote) | Number / Object | Examples: `1` | 1 ||
| [`BagOfSeeds`](Engine_LogicKeys.md#object-bagofseeds) | Object | Examples: `.3` | 1 ||
| [`BirdFeed`](Engine_LogicKeys.md#object-birdfeed) | Object | Examples: `.3` | 1 ||
| [`BirdPoopHat`](Engine_LogicKeys.md#object-birdpoophat) | Object | Examples: `.3` | 1 ||
| [`Catnip`](Engine_LogicKeys.md#object-catnip) | Integer / Object | Examples: `3` | 1 ||
| [`CatnipBig`](Engine_LogicKeys.md#object-catnipbig) | Object | Examples: `2` | 1 ||
| `consumables_consumable_common` | Number | Examples: `50` | 1 ||
| `consumables_consumable_rare` | Number | Examples: `15` | 1 ||
| `consumables_consumable_uncommon` | Number | Examples: `35` | 1 ||
| `consumables_consumable_very_rare` | Number | Examples: `1` | 1 ||
| [`DeadHummingbird`](Engine_LogicKeys.md#object-deadhummingbird) | Object | Examples: `.3` | 1 ||
| [`general_common`](./Enums.md#enum-general_common) | Enum | Examples: `auto` | 1 ||
| [`general_rare`](./Enums.md#enum-general_rare) | Enum | Examples: `auto` | 1 ||
| [`general_uncommon`](./Enums.md#enum-general_uncommon) | Enum | Examples: `auto` | 1 ||
| [`general_very_rare`](./Enums.md#enum-general_very_rare) | Enum | Examples: `auto` | 1 ||
| [`GlowingSeed`](Engine_LogicKeys.md#object-glowingseed) | Object | Examples: `.3` | 1 ||
| [`GoldenEgg`](Engine_LogicKeys.md#object-goldenegg) | Object | Examples: `.3` | 1 ||
| [`HarpysClaw`](Engine_LogicKeys.md#object-harpysclaw) | Object | Examples: `.5` | 1 ||
| [`LostSoul`](Engine_LogicKeys.md#object-lostsoul) | Object | Examples: `.5` | 1 ||
| [`MagicSeed`](Engine_LogicKeys.md#object-magicseed) | Object | Examples: `.3` | 1 ||
| [`Parousworm`](Engine_LogicKeys.md#object-parousworm) | Object | Examples: `.5` | 1 ||
| [`PeaceSymbol`](Engine_LogicKeys.md#object-peacesymbol) | Object | Examples: `.3` | 1 ||
| [`PeaceSymbolFacePaint`](Engine_LogicKeys.md#object-peacesymbolfacepaint) | Object | Examples: `.3` | 1 ||
| `pills` | Number | Examples: `7` | 1 ||
| [`RaptorEgg`](Engine_LogicKeys.md#object-raptoregg) | Object | Examples: `.1` | 1 ||
| [`RavenFeather`](Engine_LogicKeys.md#object-ravenfeather) | Object | Examples: `.3` | 1 ||
| [`TieDyeBandana`](Engine_LogicKeys.md#object-tiedyebandana) | Object | Examples: `.3` | 1 ||
| [`Turkey`](Engine_LogicKeys.md#object-turkey) | Integer / Object | Examples: `2` | 1 ||
| [`WeirdEgg`](Engine_LogicKeys.md#object-weirdegg) | Object | Examples: `.3` | 1 ||
| [`WishBone`](Engine_LogicKeys.md#object-wishbone) | Object | Examples: `.3` | 1 ||
| [`common`](./Enums.md) | Integer || 11 | 50 |
| [`rare`](./Enums.md) | Integer || 34 | 40 |

</details>

---

