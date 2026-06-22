# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Enums.md#enum-mathequation).

## Item Pools

### Context: `ROOT`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `rare` | Number | `10, 40, 15` |  |
| `uncommon` | Number | `75, 35, 60` |  |
| `very_rare` | Number | `2, 1, .01` |  |
| `common` | Number | `55, 50, 60` |  |
| `current_chapter_common` | [`Enum/String`](./Enums.md#enum-current_chapter_common) | `auto, 55` |  |
| `current_chapter_rare` | [`Enum/String`](./Enums.md#enum-current_chapter_rare) | `auto, 10` |  |
| `current_chapter_uncommon` | [`Enum/String`](./Enums.md#enum-current_chapter_uncommon) | `auto, 35` |  |
| `current_chapter_very_rare` | [`Enum/String`](./Enums.md#enum-current_chapter_very_rare) | `auto, 1` |  |
| `chapter_rare` | Number | `1` |  |
| `Chicken` | Number | `2, .01, .1` |  |
| `chapter` | Number | `1` |  |
| `chapter_common` | Number | `1` |  |
| `consumables` | Number | `10, 60` |  |
| `FoodBig` | Number | `2, 1` |  |
| `FoodMedium` | Number | `1, 5` |  |
| `basic_consumables` | Number | `90, 100` |  |
| `shop_common` | Number | `1` |  |
| `Antidote` | Number | `1` |  |
| `BagOfSeeds` | [`Enum/String`](./Enums.md#enum-bagofseeds) | `.3` |  |
| `BirdFeed` | [`Enum/String`](./Enums.md#enum-birdfeed) | `.3` |  |
| `BirdPoopHat` | [`Enum/String`](./Enums.md#enum-birdpoophat) | `.3` |  |
| `Catnip` | Number | `3` |  |
| `CatnipBig` | Number | `2` |  |
| `DeadHummingbird` | [`Enum/String`](./Enums.md#enum-deadhummingbird) | `.3` |  |
| `GlowingSeed` | [`Enum/String`](./Enums.md#enum-glowingseed) | `.3` |  |
| `GoldenEgg` | [`Enum/String`](./Enums.md#enum-goldenegg) | `.3` |  |
| `HarpysClaw` | [`Enum/String`](./Enums.md#enum-harpysclaw) | `.5` |  |
| `LostSoul` | [`Enum/String`](./Enums.md#enum-lostsoul) | `.5` |  |
| `MagicSeed` | [`Enum/String`](./Enums.md#enum-magicseed) | `.3` |  |
| `Parousworm` | [`Enum/String`](./Enums.md#enum-parousworm) | `.5` |  |
| `PeaceSymbol` | [`Enum/String`](./Enums.md#enum-peacesymbol) | `.3` |  |
| `PeaceSymbolFacePaint` | [`Enum/String`](./Enums.md#enum-peacesymbolfacepaint) | `.3` |  |
| `RaptorEgg` | [`Enum/String`](./Enums.md#enum-raptoregg) | `.1` |  |
| `RavenFeather` | [`Enum/String`](./Enums.md#enum-ravenfeather) | `.3` |  |
| `TieDyeBandana` | [`Enum/String`](./Enums.md#enum-tiedyebandana) | `.3` |  |
| `Turkey` | Number | `2` |  |
| `WeirdEgg` | [`Enum/String`](./Enums.md#enum-weirdegg) | `.3` |  |
| `WishBone` | [`Enum/String`](./Enums.md#enum-wishbone) | `.3` |  |
| `consumables_consumable_common` | Number | `50` |  |
| `consumables_consumable_rare` | Number | `15` |  |
| `consumables_consumable_uncommon` | Number | `35` |  |
| `consumables_consumable_very_rare` | Number | `1` |  |
| `general_common` | [`Enum/String`](./Enums.md#enum-general_common) | `auto` |  |
| `general_rare` | [`Enum/String`](./Enums.md#enum-general_rare) | `auto` |  |
| `general_uncommon` | [`Enum/String`](./Enums.md#enum-general_uncommon) | `auto` |  |
| `general_very_rare` | [`Enum/String`](./Enums.md#enum-general_very_rare) | `auto` |  |
| `pills` | Number | `7` |  |

</details>

---

