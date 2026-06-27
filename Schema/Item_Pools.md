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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 883 | `common`<br>`rare`<br>`cha` |
| [`rare`](./Enums.md) | Integer | Defines the rare reward block for a boss encounter. | 34 | `1`<br>`10`<br>`15` |
| [`chapter_item_pool`](./Enums.md#enum-chapter_item_pool) | Enum   |  | 19 | `alleyitems`<br>`boneyarditems`<br>`bunkeritems` |
| `uncommon` | Number | The weight value for uncommon items in a random pool distribution. | 12 | `10`<br>`20`<br>`30` |
| `very_rare` | Variable | The weight value for very rare items in a random pool distribution. | 11 | `.01`<br>`1`<br>`15` |
| [`common`](./Enums.md) | Integer | Defines the common reward block for a boss encounter. | 11 | `100`<br>`14`<br>`5` |
| `chapter_rare` | Number | An integer or variable controlling the number of rare item drops for the current chapter. | 5 | `1` |
| `chapter_common` | Number | The weight or probability for this entry to appear in the common loot pool for its chapter. | 3 | `1` |
| [`chapter`](./Enums.md#enum-chapter) | Enum  | Specifies which chapter or scenario this ability is available in. | 3 | `1`<br>`alley` |
| `Chicken` | Equation | The number of chicken pickups spawned. | 3 | `.01`<br>`.1`<br>`2` |
| `consumables` | Number | The number of consumable items provided or available in this context. | 3 | `10`<br>`60` |
| `current_chapter_common` | Variable | A variable controlling the number of common item drops for the current chapter. | 2 | `55`<br>`auto` |
| `current_chapter_rare` | Variable | A variable controlling the number of rare item drops for the current chapter. | 2 | `10`<br>`auto` |
| `current_chapter_uncommon` | Variable | The weight or value for uncommon items specific to the current chapter. | 2 | `35`<br>`auto` |
| `current_chapter_very_rare` | Variable | The weight or value for very rare items specific to the current chapter. | 2 | `1`<br>`auto` |
| `basic_consumables` | Number | The weight value for basic consumable items in a random pool distribution. | 2 | `100`<br>`90` |
| [`FoodBig`](./Engine_LogicKeys.md#object-foodbig) | Object  | Specifies the definition and weight for a large food item in item pools. | 2 | `{ . . . }` |
| [`FoodMedium`](./Engine_LogicKeys.md#object-foodmedium) | Object  | Specifies the definition and weight for a medium food item in item pools. | 2 | `{ . . . }` |
| `shop_common` | Number | The number defining the weight or relative frequency for common shop items in a pool. | 2 | `1` |
| [`Antidote`](./Engine_LogicKeys.md#object-antidote) | Float / Object  | The multiplier for the number of antidote pickups spawned. | 1 | `{ . . . }`<br>`.5`<br>`1` |
| [`BagOfSeeds`](./Engine_LogicKeys.md#object-bagofseeds) | Object  | Defines a Bag of Seeds item entry in a loot pool, including its spawn weight. | 1 | `{ . . . }` |
| [`BirdFeed`](./Engine_LogicKeys.md#object-birdfeed) | Object  | Defines a Bird Feed trinket entry in a loot pool, including optional custom properties and spawn weight. | 1 | `{ . . . }` |
| [`BirdPoopHat`](./Engine_LogicKeys.md#object-birdpoophat) | Object  | Defines a Bird Poop Hat item entry in a loot pool, including its spawn weight. | 1 | `{ . . . }` |
| [`Catnip`](./Engine_LogicKeys.md#object-catnip) | Integer / Object  | The number of catnip pickups spawned. | 1 | `{ . . . }`<br>`20`<br>`3` |
| [`CatnipBig`](./Engine_LogicKeys.md#object-catnipbig) | Object  | Specifies the definition and weight for a large catnip item in item pools. | 1 | `{ . . . }` |
| `consumables_consumable_common` | Number | The weight for selecting common consumable items from the consumables pool. | 1 | `50` |
| `consumables_consumable_rare` | Number | The weight for selecting rare consumable items from the consumables pool. | 1 | `15` |
| `consumables_consumable_uncommon` | Number | The weight for selecting uncommon consumable items from the consumables pool. | 1 | `35` |
| `consumables_consumable_very_rare` | Number | The weight for selecting very rare consumable items from the consumables pool. | 1 | `1` |
| [`DeadHummingbird`](./Engine_LogicKeys.md#object-deadhummingbird) | Object  | Defines a Dead Hummingbird item entry in a loot pool, including its spawn weight. | 1 | `{ . . . }` |
| [`general_common`](./Enums.md#enum-general_common) | Enum | Specifies the common rarity tier for an item or event outcome. | 1 | `auto` |
| [`general_rare`](./Enums.md#enum-general_rare) | Enum | Specifies the rare rarity tier for an item or event outcome. | 1 | `auto` |
| [`general_uncommon`](./Enums.md#enum-general_uncommon) | Enum | Specifies how uncommon general loot pool items are distributed; often set to 'auto' for automatic weighting. | 1 | `auto` |
| [`general_very_rare`](./Enums.md#enum-general_very_rare) | Enum | Specifies how very rare general loot pool items are distributed; often set to 'auto' for automatic weighting. | 1 | `auto` |
| [`GlowingSeed`](./Engine_LogicKeys.md#object-glowingseed) | Object  | Defines a Glowing Seed trinket entry in a loot pool, including optional custom properties and spawn weight. | 1 | `{ . . . }` |
| [`GoldenEgg`](./Engine_LogicKeys.md#object-goldenegg) | Object  | Defines a Golden Egg trinket entry in a loot pool, including optional custom properties and spawn weight. | 1 | `{ . . . }` |
| [`HarpysClaw`](./Engine_LogicKeys.md#object-harpysclaw) | Object  | Defines a Harpy's Claw item entry in a loot pool, including its spawn weight. | 1 | `{ . . . }` |
| [`LostSoul`](./Engine_LogicKeys.md#object-lostsoul) | Object  | Defines a Lost Soul item entry in a loot pool, including its spawn weight. | 1 | `{ . . . }` |
| [`MagicSeed`](./Engine_LogicKeys.md#object-magicseed) | Object  | Defines a Magic Seed trinket entry in a loot pool, including optional custom properties and spawn weight. | 1 | `{ . . . }` |
| [`Parousworm`](./Engine_LogicKeys.md#object-parousworm) | Object  | Defines a Parousworm item entry in a loot pool, including its spawn weight. | 1 | `{ . . . }` |
| [`PeaceSymbol`](./Engine_LogicKeys.md#object-peacesymbol) | Object  | Defines a Peace Symbol item entry in a loot pool, including its spawn weight. | 1 | `{ . . . }` |
| [`PeaceSymbolFacePaint`](./Engine_LogicKeys.md#object-peacesymbolfacepaint) | Object  | Defines a Peace Symbol Face Paint item entry in a loot pool, including its spawn weight. | 1 | `{ . . . }` |
| `pills` | Number | The amount of pills granted as a consumable reward. | 1 | `7` |
| [`RaptorEgg`](./Engine_LogicKeys.md#object-raptoregg) | Object  | An object defining a raptor egg item with a probability or weight. | 1 | `{ . . . }` |
| [`RavenFeather`](./Engine_LogicKeys.md#object-ravenfeather) | Object  | Defines a Raven Feather item entry in a loot pool, including its spawn weight. | 1 | `{ . . . }` |
| [`TieDyeBandana`](./Engine_LogicKeys.md#object-tiedyebandana) | Object  | Defines a Tie Dye Bandana item entry in a loot pool, including its spawn weight. | 1 | `{ . . . }` |
| [`Turkey`](./Engine_LogicKeys.md#object-turkey) | Integer / Object  | The number of turkeys spawned. | 1 | `{ . . . }`<br>`1000`<br>`2` |
| [`WeirdEgg`](./Engine_LogicKeys.md#object-weirdegg) | Object  | Defines a Weird Egg trinket entry in a loot pool, including optional custom properties and spawn weight. | 1 | `{ . . . }` |
| [`WishBone`](./Engine_LogicKeys.md#object-wishbone) | Object  | Defines a Wish Bone item entry in a loot pool, including its spawn weight. | 1 | `{ . . . }` |

</details>


---