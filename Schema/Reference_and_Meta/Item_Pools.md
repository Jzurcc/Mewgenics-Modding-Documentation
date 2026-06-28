---
title: "Item Pools Schema"
description: "Identifiers for categorizing item drops."
---

# Item Pools Schema


<details open>
<summary><strong>Quick Navigation</strong></summary>

<table>
  <tr>
    <td width="22%"><strong>Core Entities & Combat</strong></td>
    <td><a href="../Core_Entities_and_Combat/Abilities_and_Spells.md">Abilities & Spells</a> • <a href="../Core_Entities_and_Combat/Characters_and_Bosses.md">Characters & Bosses</a> • <a href="../Core_Entities_and_Combat/Items_and_Equipment.md">Items & Equipment</a> • <a href="../Core_Entities_and_Combat/Passives_and_Statuses.md">Passives & Statuses</a> • <a href="../Core_Entities_and_Combat/Elite_Buffs.md">Elite Buffs</a> • <a href="../Core_Entities_and_Combat/Enemy_AI.md">Enemy AI</a> • <a href="../Core_Entities_and_Combat/Status_Effect_Keywords.md">Status Keywords</a></td>
  </tr>
  <tr>
    <td><strong>Engine Scripts & Logic</strong></td>
    <td><a href="../Engine_Scripts_and_Logic/Engine_LogicKeys.md">Logic Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_EventKeys.md">Event Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_DamagingKeys.md">Damaging Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md">Status & Passive Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_GlobalModifierKeys.md">Global Modifiers</a> • <a href="../Engine_Scripts_and_Logic/Math_Equations.md">Math Equations</a></td>
  </tr>
  <tr>
    <td><strong>Player Progression & Cats</strong></td>
    <td><a href="../Player_Progression_and_Cats/Cat_Classes.md">Cat Classes</a> • <a href="../Player_Progression_and_Cats/Cat_Mutations.md">Cat Mutations</a> • <a href="../Player_Progression_and_Cats/Custom_Cats.md">Custom Cats</a> • <a href="../Player_Progression_and_Cats/Injuries.md">Injuries</a> • <a href="../Player_Progression_and_Cats/Progression_Unlocks.md">Progression Unlocks</a> • <a href="../Player_Progression_and_Cats/Combat_Rewards.md">Combat Rewards</a></td>
  </tr>
  <tr>
    <td><strong>World, Maps & Events</strong></td>
    <td><a href="../World_Maps_and_Events/Events_and_Encounters.md">Events & Encounters</a> • <a href="../World_Maps_and_Events/House_and_Environment.md">House & Environment</a> • <a href="../World_Maps_and_Events/Map_Generation_and_Routing.md">Map Gen & Routing</a> • <a href="../World_Maps_and_Events/Furniture_and_Metaprogression.md">Furniture & Meta</a> • <a href="../World_Maps_and_Events/Shops.md">Shops</a> • <a href="../World_Maps_and_Events/Spawns_and_Enemy_Pools.md">Spawns & Enemy Pools</a> • <a href="../World_Maps_and_Events/Boss_Cutscene_Info.md">Boss Cutscenes</a> • <a href="../World_Maps_and_Events/NPC_Scripts.md">NPC Scripts</a></td>
  </tr>
  <tr>
    <td><strong>Assets & Localization</strong></td>
    <td><a href="../Assets_and_Localization/Audio_SFX_Dictionary.md">Audio SFX</a> • <a href="../Assets_and_Localization/Particles_and_VFX_Dictionary.md">Particles & VFX</a> • <a href="../Assets_and_Localization/Damage_Text_Styles.md">Damage Text</a> • <a href="../Assets_and_Localization/Localization_Guide.md">Localization Guide</a> • <a href="../Assets_and_Localization/Text_Formatting_and_Effects.md">Text Formatting</a> • <a href="../Assets_and_Localization/Strings.md">Strings</a></td>
  </tr>
  <tr>
    <td><strong>Reference & Meta</strong></td>
    <td><a href="../Reference_and_Meta/Enums.md">Enums</a> • <a href="../Reference_and_Meta/Arrays.md">Arrays</a> • <a href="../Reference_and_Meta/Item_Pools.md">Item Pools</a> • <a href="../Reference_and_Meta/Difficulties.md">Difficulties</a> • <a href="../Reference_and_Meta/Engine_Hidden_Passives_and_Statuses.md">Hidden Passives</a> • <a href="../Reference_and_Meta/Passive_Identifiers_Audit.md">Passive Audit</a> • <a href="../Reference_and_Meta/Engine_Uncategorized_Resources.md">Uncategorized Keys</a> • <a href="../Reference_and_Meta/Miscellaneous.md">Miscellaneous</a></td>
  </tr>
</table>

</details>

## Overview
> [!NOTE]
> This schema describes all predefined collections of items used to generate random loot drops (e.g. "RareWeaponsPool").

## Usage Example
Here is a real example of this object being defined in the game's data:
```gon
tinkerer_0 [ //default
    //melee
    TinkererStick
    TinkererGlassShard
    PogoStick

    //ranged
    SmallBomb
    TinkererBattery
    Spitball

    //armor
    JankAlloyHat
    JankAlloyMask
    JankAlloyArmor
]
```

## Associated Directory Files
To see extracted instances of this schema in the base game, refer to:
- [`Item_Pools.md`](../../Directory/Items_and_Passives/Item_Pools.md)

---

> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see AUDIT_GAPS.md. For enum values, see [Enums.md](./Enums.md).

This document is an exhaustive, auto-generated dictionary of `.gon` properties relevant to this subsystem. While the overview above provides high-level context, you may still need to infer exact engine execution rules through testing or context clues.

## Item Pools

> **Associated Files:** `data/item_pools/`


### Object: `ROOT`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 40

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 34 | `common`<br>`rare`<br>`cha` |
| `rare` | Integer | Defines the rare reward block for a boss encounter. | 14 | `1`<br>`10`<br>`15` |
| `uncommon` | Number | The weight value for uncommon items in a random pool distribution. | 13 | `10`<br>`20`<br>`30` |
| `very_rare` | Float | The weight value for very rare items in a random pool distribution. | 12 | `.01`<br>`1`<br>`15` |
| `common` | Integer | Defines the common reward block for a boss encounter. | 11 | `100`<br>`14`<br>`5` |
| [`current_chapter_rare`](./Enums.md#enum-current_chapter_rare) | Integer / Enum | A variable controlling the number of rare item drops for the current chapter. | 7 | `10`<br>`auto` |
| [`current_chapter_common`](./Enums.md#enum-current_chapter_common) | Integer / Enum | A variable controlling the number of common item drops for the current chapter. | 7 | `55`<br>`auto` |
| [`current_chapter_uncommon`](./Enums.md#enum-current_chapter_uncommon) | Integer / Enum | The weight or value for uncommon items specific to the current chapter. | 7 | `35`<br>`auto` |
| [`current_chapter_very_rare`](./Enums.md#enum-current_chapter_very_rare) | Integer / Enum | The weight or value for very rare items specific to the current chapter. | 7 | `1`<br>`auto` |
| `chapter_rare` | Number | An integer or variable controlling the number of rare item drops for the current chapter. | 6 | `1` |
| `Chicken` | Float | The number of chicken pickups spawned. | 5 | `.01`<br>`.1`<br>`2` |
| `consumables` | Number | The number of consumable items provided or available in this context. | 4 | `10`<br>`60` |
| `chapter_common` | Number | The weight or probability for this entry to appear in the common loot pool for its chapter. | 4 | `1` |
| [`chapter`](./Enums.md#enum-chapter) | Enum  | Specifies which chapter or scenario this ability is available in. | 4 | `1`<br>`alley` |
| [`FoodMedium`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#object-foodmedium) | Object  | Specifies the definition and weight for a medium food item in item pools. | 3 | `{ . . . }` |
| [`FoodBig`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#object-foodbig) | Object  | Specifies the definition and weight for a large food item in item pools. | 3 | `{ . . . }` |
| `shop_common` | Number | The number defining the weight or relative frequency for common shop items in a pool. | 3 | `1` |
| `basic_consumables` | Number | The weight value for basic consumable items in a random pool distribution. | 3 | `100`<br>`90` |
| [`CatnipBig`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#object-catnipbig) | Object  | Specifies the definition and weight for a large catnip item in item pools. | 3 | `{ . . . }` |
| `GlowingSeed` | Float / Object | Defines a Glowing Seed trinket entry in a loot pool, including optional custom properties and spawn weight. | 3 | `{ . . . }` |
| `MagicSeed` | Float / Object | Defines a Magic Seed trinket entry in a loot pool, including optional custom properties and spawn weight. | 3 | `{ . . . }` |
| `WeirdEgg` | Float / Object | Defines a Weird Egg trinket entry in a loot pool, including optional custom properties and spawn weight. | 3 | `{ . . . }` |
| `BirdFeed` | Float / Object | Defines a Bird Feed trinket entry in a loot pool, including optional custom properties and spawn weight. | 3 | `{ . . . }` |
| `GoldenEgg` | Float / Object | Defines a Golden Egg trinket entry in a loot pool, including optional custom properties and spawn weight. | 3 | `{ . . . }` |
| `pills` | Number | The amount of pills granted as a consumable reward. | 2 | `7` |
| `Antidote` | Float / Object  | The multiplier for the number of antidote pickups spawned. | 2 | `{ . . . }`<br>`.5`<br>`1` |
| [`Catnip`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#object-catnip) | Integer / Object  | The number of catnip pickups spawned. | 2 | `{ . . . }`<br>`20`<br>`3` |
| `Parousworm` | Float / Object | Defines a Parousworm item entry in a loot pool, including its spawn weight. | 2 | `{ . . . }` |
| [`Turkey`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#object-turkey) | Integer / Object  | The number of turkeys spawned. | 2 | `{ . . . }`<br>`1000`<br>`2` |
| `BirdPoopHat` | Float / Object | Defines a Bird Poop Hat item entry in a loot pool, including its spawn weight. | 2 | `{ . . . }` |
| `RaptorEgg` | Float / Object | An object defining a raptor egg item with a probability or weight. | 2 | `{ . . . }` |
| `LostSoul` | Float / Object | Defines a Lost Soul item entry in a loot pool, including its spawn weight. | 2 | `{ . . . }` |
| `PeaceSymbol` | Float / Object | Defines a Peace Symbol item entry in a loot pool, including its spawn weight. | 2 | `{ . . . }` |
| `PeaceSymbolFacePaint` | Float / Object | Defines a Peace Symbol Face Paint item entry in a loot pool, including its spawn weight. | 2 | `{ . . . }` |
| `TieDyeBandana` | Float / Object | Defines a Tie Dye Bandana item entry in a loot pool, including its spawn weight. | 2 | `{ . . . }` |
| `WishBone` | Float / Object | Defines a Wish Bone item entry in a loot pool, including its spawn weight. | 2 | `{ . . . }` |
| `BagOfSeeds` | Float / Object | Defines a Bag of Seeds item entry in a loot pool, including its spawn weight. | 1 | `{ . . . }` |
| `DeadHummingbird` | Float / Object | Defines a Dead Hummingbird item entry in a loot pool, including its spawn weight. | 1 | `{ . . . }` |
| `HarpysClaw` | Float / Object | Defines a Harpy's Claw item entry in a loot pool, including its spawn weight. | 1 | `{ . . . }` |
| `RavenFeather` | Float / Object | Defines a Raven Feather item entry in a loot pool, including its spawn weight. | 1 | `{ . . . }` |
| `consumables_consumable_common` | Number | The weight for selecting common consumable items from the consumables pool. | 1 | `50` |
| `consumables_consumable_rare` | Number | The weight for selecting rare consumable items from the consumables pool. | 1 | `15` |
| `consumables_consumable_uncommon` | Number | The weight for selecting uncommon consumable items from the consumables pool. | 1 | `35` |
| `consumables_consumable_very_rare` | Number | The weight for selecting very rare consumable items from the consumables pool. | 1 | `1` |
| [`general_common`](./Enums.md#enum-general_common) | Enum | Specifies the common rarity tier for an item or event outcome. | 1 | `auto` |
| [`general_rare`](./Enums.md#enum-general_rare) | Enum | Specifies the rare rarity tier for an item or event outcome. | 1 | `auto` |
| [`general_uncommon`](./Enums.md#enum-general_uncommon) | Enum | Specifies how uncommon general loot pool items are distributed; often set to 'auto' for automatic weighting. | 1 | `auto` |
| [`general_very_rare`](./Enums.md#enum-general_very_rare) | Enum | Specifies how very rare general loot pool items are distributed; often set to 'auto' for automatic weighting. | 1 | `auto` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 1 | `{ . . . }` |
| [`chapter_item_pool`](./Enums.md#enum-chapter_item_pool) | Enum | Specifies the item pool identifier used by a chapter or boss to determine which items can be found. | 0 | `alleyitems`<br>`boneyarditems`<br>`bunkeritems` |

</details>


---