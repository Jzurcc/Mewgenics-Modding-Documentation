---
title: "Items & Equipment Schema"
description: "Defines consumables, weapons, and wearable trinkets."
---

# Items & Equipment Schema


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
> This schema is used for anything that can be equipped, consumed, or held in the inventory. It defines stat modifiers, activated abilities, and usage rules.

## Usage Example
Here is a real example of this object being defined in the game's data:
```gon
ScrapHat {
        name "ARMOR_SCRAPMETALHAT_NAME"
        desc "ARMOR_SCRAPMETALHAT_DESC"
        rarity common
        kind head
        frame 12
        set Scrap

        shield 4

        passives {
            Metal 1
        }
    }
```

## Associated Directory Files
To see extracted instances of this schema in the base game, refer to:
- [`Items_and_Equipment.md`](../../Directory/Items_and_Passives/Items_and_Equipment.md)
- [`Item_Set_Bonuses.md`](../../Directory/Items_and_Passives/Item_Set_Bonuses.md)

---



This document is an exhaustive, auto-generated dictionary of `.gon` properties relevant to this subsystem. While the overview above provides high-level context, you may still need to infer exact engine execution rules through testing or context clues.

## Items & Equipment

> **Associated Files:** `data/items/, data/item_setbonuses.gon`


### Object: `ROOT`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1235

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1217 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1206 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `frame` | Integer | The sprite frame index to display. | 1106 | `1`<br>`10`<br>`100` |
| [`kind`](../Reference_and_Meta/Enums.md#enum-kind) | Enum | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1106 | `face`<br>`head`<br>`modifier` |
| [`rarity`](../Reference_and_Meta/Enums.md#enum-rarity) | Enum | Determines the rarity tier of the item, affecting drop rates and item quality. | 967 | `common`<br>`consumable_common`<br>`consumable_rare` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 940 | passives<br>class<br>tag |
| [`passives`](./Items_and_Equipment.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 823 | `{ . . . }` |
| [`set`](../Reference_and_Meta/Arrays.md#array-set) | Array / Enum  | Specifies the set name(s) the item belongs to for set bonuses. | 766 | `80s`<br>`90s`<br>`AdvancedAlloy` |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 368 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `shield` | Equation | The shield value granted by this mutation, or 'aux' to use the unit's auxiliary stat. | 186 | `"max((aux-1)*2, 0)"`<br>`1`<br>`10` |
| [`durability`](../Reference_and_Meta/Arrays.md#array-durability) | Array / Integer  | The amount of durability consumed by this ability or required for its use. | 171 | `0`<br>`1`<br>`10` |
| `cursed` | Boolean | If true, the item is cursed and may have negative effects when equipped or used. | 77 | `true` |
| `cha` | Integer | The Charisma stat value or modifier. | 75 | `+1`<br>`-1`<br>`-2` |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. | 64 | `1`<br>`2`<br>`true` |
| `spd` | Integer | The Speed stat value or modifier. | 60 | `-1`<br>`-10`<br>`-2` |
| `con` | Integer | The Constitution stat value or modifier. | 57 | `-1`<br>`-2`<br>`-3` |
| `int` | Integer | The Intelligence stat value or modifier. | 54 | `-1`<br>`-10`<br>`-2` |
| `lck` | Integer | The Luck stat value or modifier. | 44 | `-1`<br>`-2`<br>`-3` |
| `aux` | Integer | An auxiliary integer value used for item properties, such as hunger value. | 41 | `-1`<br>`1`<br>`10` |
| `quest_item` | Boolean | If true, this item is a quest item and cannot be sold or destroyed. | 40 | `false`<br>`true` |
| `parasite` | Boolean | If true, the item is a parasite that attaches to a unit and cannot be removed normally. | 36 | `true` |
| [`variant_of`](../Reference_and_Meta/Enums.md#enum-variant_of) | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. | 29 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| `str` | Integer | The Strength stat value or modifier. | 28 | `-1`<br>`-2`<br>`-3` |
| `dex` | Integer | The Dexterity stat value or modifier. | 22 | `-1`<br>`-2`<br>`-3` |
| [`quest_reward_item`](../Reference_and_Meta/Enums.md#enum-quest_reward_item) | Enum | The specific item awarded as a quest reward. The value uses a unique item identifier string. | 22 | `AirHorn_Fixed`<br>`AngryFace_Fixed`<br>`BubbleBoy_Fixed` |
| `indestructible` | Boolean | If true, the item cannot be destroyed or removed. | 20 | `true` |
| `divine_shield` | Integer | The number of stacks of the Divine Shield status this mutation provides. | 17 | `0`<br>`1`<br>`2` |
| `legacy_quest` | Boolean | If true, this item is part of a legacy quest. | 17 | `true` |
| [`hint_destination`](../Reference_and_Meta/Enums.md#enum-hint_destination) | Enum | Specifies the map destination hinted by this item or event. | 16 | `boneyard`<br>`caves`<br>`core` |
| [`str_aux_initialize`](../Reference_and_Meta/Enums.md#enum-str_aux_initialize) | Enum | Specifies a random fallback or initial auxiliary data when an item's str_aux is not set. The value is a comma-separated type string such as "random_stat" or "random_copyable_colorless_passive". | 15 | `random_class_ability`<br>`random_class_passive`<br>`random_copyable_class_ability` |
| `dont_destroy_on_0` | Boolean | If true, the item is not destroyed when its charges reach zero. | 13 | `true` |
| [`global_tags`](../Reference_and_Meta/Arrays.md#array-global_tags) | Array | A list of global tags that modify the run's behavior. | 12 | `[`<br>`[all_cats_are_jester]`<br>`[all_normal_events_are_weather]` |
| `max_durability` | Integer | The maximum number of uses or hits the item can endure before breaking. | 11 | `1`<br>`2`<br>`3` |
| [`on_store`](../Reference_and_Meta/Enums.md#enum-on_store) | Enum | Defines an action or transformation that occurs when the item is stored or placed in the player's inventory. Common values include "become_aux_coins", "become_furniture", or "become_rare_furniture". | 8 | `become_aux_coins`<br>`become_furniture`<br>`become_rare_furniture` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 6 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`hint_prerequisite_flag`](../Reference_and_Meta/Enums.md#enum-hint_prerequisite_flag) | Enum | Defines a map flag that must be set for the hint to appear. | 5 | `mapflag_BothObelisksUnlocked`<br>`mapflag_DimensionXUnlocked`<br>`mapflag_MeatWorldUnlocked` |
| `failable` | Boolean | If true, the event or action has a chance to fail. | 4 | `true` |
| [`global_passives`](./Items_and_Equipment.md#object-global_passives) | Object | An object containing global passive modifiers that apply to the entire run. | 4 | `{ . . . }` |
| `randomize_piece_frames` | Boolean | If true, the item's visual piece frames are randomized when it spawns or appears. | 4 | `true` |
| `str_aux_is_copy_passive` | Boolean | If true, the item's str_aux field is considered a passive that can be copied or duplicated by other items. | 4 | `true` |
| `max_health` | Integer | Sets a modifier to the unit's maximum health. A value of -1 might indicate no change or a default behavior. | 3 | `-1` |
| `fragile` | Boolean | If true, the item breaks permanently when its durability reaches zero. | 3 | `true` |
| [`icon_hint`](../Reference_and_Meta/Enums.md#enum-icon_hint) | Enum | Specifies a hint string used to determine the icon shown in the UI. Common values like "passive_syringe" or "ability_syringe" map to specific icon assets. | 3 | `ability_syringe`<br>`passive_syringe` |
| `reset_aux_on_store` | Integer | An integer flag that when set to 1, resets the item's auxiliary data when it is stored in the inventory. | 3 | `1` |
| `sticky` | Boolean | If true, the item cannot be unequipped or removed from the unit's slot under normal circumstances. | 3 | `true` |
| `weightless` | Boolean | If true, the item does not contribute to the unit's weight or encumbrance. | 3 | `true` |
| `speed` | Array / Float  | The speed of the projectile or move, can be a value or a range. | 2 | `-30`<br>`-4`<br>`.5` |
| [`keyword_tooltips`](./Items_and_Equipment.md#object-keyword_tooltips) | Object  | Associates keyword tooltips with the ability, often used for status effects. | 2 | `{ . . . }` |
| [`passive`](./Items_and_Equipment.md#object-passive) | Object | Defines the passive form, where the unit does nothing (uses DoNothing attack) and is inactive. | 2 | `{ . . . }` |
| `prevent_level_up` | Boolean | If true, the cat cannot gain experience or level up. | 2 | `true` |
| [`quest_item_alias`](../Reference_and_Meta/Enums.md#enum-quest_item_alias) | Enum | Specifies the main quest item key that this glowing variant is an alias of. The value is the identifier of the base quest item. | 2 | `BlackShard`<br>`NuclearKnife` |
| [`str_aux_is_copy_ability`](./Items_and_Equipment.md#object-str_aux_is_copy_ability) | Object | An object defining bonus passives and ability modifications for an auxiliary ability that is copied. | 2 | `{ . . . }` |
| `str_aux_is_copy_item_passive` | Boolean | If true, the item's str_aux field can be copied as a passive when applied to another item. | 2 | `true` |
| [`Set`](../Reference_and_Meta/Enums.md#enum-set) | Enum | Specifies the item set name that this item belongs to. | 1 | `Monk` |
| `aux_is_catid` | Boolean | If true, the item's auxiliary data stores or uses a cat identifier for spawning or duplication purposes. | 1 | `true` |
| `cant_equip_to_colorless` | Boolean | If true, the item cannot be equipped on a unit that has no color (i.e., is a colorless cat). | 1 | `true` |
| `degrade_after_adventure` | Boolean | If false, the item does not lose durability or quality after completing an adventure. | 1 | `false` |
| [`equip_sound`](../Reference_and_Meta/Enums.md#enum-equip_sound) | Enum | Specifies the sound effect played when the item is equipped. The value is a sound ID string like "SE_CatWeaponPoke_Chainsaw". | 1 | `SE_CatWeaponPoke_Chainsaw` |
| `force_sticky` | Boolean | If true, the item is forced to be sticky, overriding any other unequip conditions. | 1 | `true` |
| [`reset_str_aux_on_store`](../Reference_and_Meta/Enums.md#enum-reset_str_aux_on_store) | Enum | Specifies the default string identifier to reset the item's str_aux to when it is stored. | 1 | `ModelingClay_Default` |
| [`str_aux`](../Reference_and_Meta/Enums.md#enum-str_aux) | Enum | A string identifier that stores the item's current auxiliary data, such as "ModelingClay_Default". | 1 | `ModelingClay_Default` |
| `str_aux_is_copy_item_active` | Boolean | If true, the item's str_aux field can be copied as an active ability when applied to another item. | 1 | `true` |
| `str_aux_is_copy_item_icon` | Boolean | If true, the item's str_aux field can be copied as the icon when applied to another item. | 1 | `true` |

</details>


---


### Object: `passives`


**Definition:** A container object listing passive effects granted to the unit.  
**Total Count:** 2807

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveAfterXKills`](./Items_and_Equipment.md#object-passiveafterxkills), [`PassiveAtHealthThreshold`](./Items_and_Equipment.md#object-passiveathealththreshold), [`PassiveAtStatThreshold`](./Items_and_Equipment.md#object-passiveatstatthreshold), [`PassiveIfStrAuxEquals`](./Items_and_Equipment.md#object-passiveifstrauxequals), [`PassiveWhenAffectedByElement`](./Items_and_Equipment.md#object-passivewhenaffectedbyelement), [`PassiveWhenOnTile`](./Items_and_Equipment.md#object-passivewhenontile), [`ROOT`](./Items_and_Equipment.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 811 | passives<br>class<br>tag |
| `Metal` | Integer | The number of armor stacks or metal keyword effects. | 89 | `1` |
| [`AddStatusToBasicAttack`](./Items_and_Equipment.md#object-addstatustobasicattack) | Object  | Contains status effects to add to the basic attack. | 68 | `{ . . . }` |
| `Brace` | Array / Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 47 | `1`<br>`10`<br>`2` |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 44 | `1`<br>`2`<br>`3` |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 38 | `1`<br>`2`<br>`3` |
| [`MeleeRevengeDamage`](./Items_and_Equipment.md#object-meleerevengedamage) | Object  | Defines the damage and effects applied back to a melee attacker upon being hit. | 34 | `{ . . . }` |
| [`SpawnOnBattleStart`](./Items_and_Equipment.md#object-spawnonbattlestart) | Enum / Object  | Specifies the object that spawns adjacent to the unit at the start of battle. | 30 | `{ . . . }`<br>`BeefyCharmedLeech`<br>`BuffCharmedKitten`<br>`CharmedCultist` |
| [`StatusOnBattleEnd`](./Items_and_Equipment.md#object-statusonbattleend) | Object  | An object containing status effects or passives applied to the unit when the battle ends. | 30 | `{ . . . }` |
| [`StatusEachTurnEnd`](./Items_and_Equipment.md#object-statuseachturnend) | Object  | Specifies status effects applied to the unit at the end of each of its turns. | 27 | `{ . . . }` |
| `Brittle` | Integer | The number of stacks of the Brittle status, or an object defining its properties. | 24 | `1` |
| `Fragile` | Integer | The number of stacks of the Fragile status, causing increased damage taken. | 22 | `1` |
| [`StatusOnBreak`](./Items_and_Equipment.md#object-statusonbreak) | Object | An object defining statuses or effects applied when an item or object breaks. | 22 | `{ . . . }` |
| `ArmorDodgeChance` | Integer | The percentage chance to dodge incoming attacks when wearing this armor. | 19 | `10%`<br>`15%`<br>`20%` |
| [`StatusOnKill`](./Items_and_Equipment.md#object-statusonkill) | Object  | Specifies status effects or actions triggered when the unit kills an enemy. | 18 | `{ . . . }` |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 17 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`StatusOnTookDamage`](./Items_and_Equipment.md#object-statusontookdamage) | Object  | Specifies status effects or actions triggered when the unit takes damage. | 17 | `{ . . . }` |
| [`SpawnThingOnDamage`](./Items_and_Equipment.md#object-spawnthingondamage) | Object  | Specifies an object that spawns on the tile when the unit takes damage. | 13 | `{ . . . }` |
| [`StatusOnBattleStart`](./Items_and_Equipment.md#object-statusonbattlestart) | Object | An object containing status effects to apply to the unit at the start of every battle. | 13 | `{ . . . }` |
| `Flammable` | Integer | The number of stacks of Flammable, or an object defining its properties. | 13 | `1`<br>`2` |
| [`SpawnEachTurn`](./Items_and_Equipment.md#object-spawneachturn) | Object  | Specifies an object that spawns on a random adjacent tile each turn, with optional chance. | 12 | `{ . . . }` |
| `AddBonusRange` | Integer | The number of additional tiles of range added to the unit's abilities. | 11 | `1`<br>`10`<br>`2` |
| `Poison` | Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 10 | `1`<br>`10`<br>`2` |
| [`StatusImmunity`](../Reference_and_Meta/Arrays.md#array-statusimmunity) | Array / Enum  | A list of status effect names the unit is immune to. | 10 | `Burn`<br>`Poison`<br>`Tarred` |
| `BleedThorns` | Integer | The amount of bleed thorns damage dealt to attackers on hit. | 10 | `1`<br>`2`<br>`3` |
| [`RevengeDamage`](./Items_and_Equipment.md#object-revengedamage) | Object  | An object defining the damage and effects that trigger when the unit is attacked. | 9 | `{ . . . }` |
| [`StatusEachTurnBegin`](./Items_and_Equipment.md#object-statuseachturnbegin) | Object  | Specifies status effects applied to the unit at the start of each of its turns. | 9 | `{ . . . }` |
| [`SpawnThingOnDeath`](../Reference_and_Meta/Enums.md#enum-spawnthingondeath) | Enum  | Specifies the name of an object to spawn upon death. | 9 | `Boulder`<br>`CharmedDemonKitten`<br>`CharmedFlySwarm` |
| `CritChanceUp` | Integer | The amount of critical hit chance added as a flat percentage. | 8 | `1`<br>`10`<br>`100` |
| `KineticSpikes` | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 8 | `1`<br>`2`<br>`3` |
| [`ReplaceBasicMove`](../Reference_and_Meta/Enums.md#enum-replacebasicmove) | Enum  | Specifies an alternative movement ability that replaces the unit's default move. | 8 | `BasicDashAttackMove`<br>`BasicJump`<br>`BellyFlop_BasicMove` |
| [`AddStatusToAllDamage`](./Items_and_Equipment.md#object-addstatustoalldamage) | Object | Adds the contained status effects to all damage dealt by the unit. | 8 | `{ . . . }` |
| [`StatusOnKillEnemy`](./Items_and_Equipment.md#object-statusonkillenemy) | Object | Specifies the effects applied when the unit kills an enemy. | 8 | `{ . . . }` |
| [`AddSelfStatusToBasicAttack`](./Items_and_Equipment.md#object-addselfstatustobasicattack) | Object | Applies the contained status effects to the unit when it uses its basic attack. | 8 | `{ . . . }` |
| [`StatusAlliesOnBattleStart`](./Items_and_Equipment.md#object-statusalliesonbattlestart) | Object | An object containing status effects to apply to all allies at the start of battle. | 8 | `{ . . . }` |
| [`AddPassivesToMinions`](./Items_and_Equipment.md#object-addpassivestominions) | Object | An object containing passives that are granted to all minions spawned by the unit. | 7 | `{ . . . }` |
| `AddManaRegen` | Integer | The flat amount of mana regenerated per turn. | 7 | `1`<br>`2`<br>`3` |
| [`AbilityOnBattleStart`](../Reference_and_Meta/Enums.md#enum-abilityonbattlestart) | Enum | Casts the specified ability when the battle begins. | 7 | `Flush`<br>`Heathens`<br>`Heathens2` |
| `PoisonThorns` | Integer | The number of stacks of Poison applied to melee attackers when they hit this unit. | 7 | `1`<br>`2`<br>`3` |
| `AddLevelUpRerolls` | Integer | The number of additional rerolls the unit gets when leveling up. | 7 | `1`<br>`2`<br>`3` |
| `ManaCostReduction` | Integer | The amount or percentage by which ability mana costs are reduced for this unit. | 7 | `-2`<br>`1`<br>`2` |
| `TrinketPassiveMultiplierBonus` | Integer | Bonus multiplier to the passive effects of equipped trinkets. | 7 | `1`<br>`2` |
| [`BrittleDuringElement`](../Reference_and_Meta/Enums.md#enum-brittleduringelement) | Enum | Makes the unit brittle while in contact with the specified element. | 7 | `water` |
| [`DurabilityTransform`](./Items_and_Equipment.md#object-durabilitytransform) | Object | Transforms the item into another when durability reaches specified thresholds. | 7 | `{ . . . }` |
| [`SetFragileImmune`](../Reference_and_Meta/Enums.md#enum-setfragileimmune) | Enum | Sets the unit's material to the specified type, granting immunity to the Fragile status. | 7 | `""`<br>`Bionic`<br>`Cardboard` |
| [`PassiveWhenOnTile`](./Items_and_Equipment.md#object-passivewhenontile) | Object | Grants the contained passive effects while the unit is standing on one of the specified tile types. | 7 | `{ . . . }` |
| [`PassiveIfStrAuxEquals`](./Items_and_Equipment.md#object-passiveifstrauxequals) | Object | Grants the contained passive effects when the unit's specified auxiliary stat equals the given value. | 7 | `{ . . . }` |
| `Bleed` | Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 6 | `1`<br>`10`<br>`2` |
| `Bruise` | Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 6 | `1`<br>`2`<br>`3` |
| `Trample` | Integer | The amount of bonus damage dealt when moving through an enemy. | 6 | `1`<br>`3`<br>`4` |
| [`ElementImmune`](../Reference_and_Meta/Enums.md#enum-elementimmune) | Enum  | Specifies an element type (e.g., Fire, Ice) that the unit is immune to damage from. | 6 | `Creep`<br>`Electric`<br>`Fire` |
| `AddCorpseHealth` | Integer | The amount of bonus health the unit's corpse has before it can be resurrected. | 6 | `-999`<br>`-999999`<br>`100` |
| `Flying` | Integer | If set to 1, grants the unit the Flying passive, allowing movement over obstacles and ignoring terrain penalties. | 6 | `1` |
| [`StatusOnDie`](./Items_and_Equipment.md#object-statusondie) | Object  | Specifies status effects or actions triggered when the unit dies. | 6 | `{ . . . }` |
| [`ItemAuxTransform`](./Items_and_Equipment.md#object-itemauxtransform) | Object | Transforms the item into another when its auxiliary value reaches specified thresholds. | 6 | `{ . . . }` |
| [`SetBrittleImmune`](../Reference_and_Meta/Enums.md#enum-setbrittleimmune) | Enum | Sets the unit's material to the specified type, granting immunity to the Brittle status. | 6 | `""`<br>`AdvancedAlloy`<br>`Alloy` |
| `Burn` | Equation | The amount of Burn applied, either as a fixed number or a formula string. | 5 | `1`<br>`10`<br>`2` |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 5 | `-1`<br>`-2`<br>`1` |
| [`Quivered`](../Reference_and_Meta/Arrays.md#array-quivered) | Array / Integer  | The amount of quivered stacks applied, or an [stacks, probability] array. | 5 | `1`<br>`2`<br>`5` |
| `SpellDamageUp` | Integer | The number of stacks of SpellDamageUp applied, increasing spell damage. | 5 | `1`<br>`3` |
| [`SpawnOnBattleStartRandomEmptyTile`](./Items_and_Equipment.md#object-spawnonbattlestartrandomemptytile) | Object  | Specifies an object that spawns on a random empty tile at the start of battle. | 5 | `{ . . . }` |
| [`StatusOnEndMove`](./Items_and_Equipment.md#object-statusonendmove) | Object  | Specifies status effects or actions triggered when the unit finishes moving. | 5 | `{ . . . }` |
| `BoostHeals` | Integer | The number of stacks that increase healing received or dealt. | 5 | `-2`<br>`1`<br>`2` |
| [`ChanceToRevive`](./Items_and_Equipment.md#object-chancetorevive) | Integer / Object | The percentage chance or an object defining chance, health, and statuses on revival. | 5 | `{ . . . }`<br>`100`<br>`25` |
| [`PassiveAtHealthThreshold`](./Items_and_Equipment.md#object-passiveathealththreshold) | Object | An object that grants additional passives when the unit's health meets a specified threshold, with sub-keys for threshold, mode, and passives. | 5 | `{ . . . }` |
| [`OverrideBasicAttack`](../Reference_and_Meta/Enums.md#enum-overridebasicattack) | Enum | Replaces the unit's basic attack with the specified ability. | 5 | `BasicExplosiveShot`<br>`BasicMelee`<br>`BasicMetronome` |
| [`DelayedAutoRevive`](./Items_and_Equipment.md#object-delayedautorevive) | Object  | Configures an automatic revival after a delay, with specified rounds and health percentage. | 5 | `{ . . . }` |
| [`TransformItemOnElementInfluence`](./Items_and_Equipment.md#object-transformitemonelementinfluence) | Object | Transforms the item into the specified one when influenced by the given element, optionally fully repairing it. | 5 | `{ . . . }` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 4 | `Default`<br>`FormChange`<br>`Druid` | `AddElementsToBasicAttack` | Enum | Specifies an elemental damage type that is added to the unit's basic attacks. | 174 | Default<br>FormChange<br>Druid |
| `Confusion` | Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 4 | `1`<br>`10`<br>`2` |
| [`DeathRattle`](../Reference_and_Meta/Enums.md#enum-deathrattle) | Enum  | Specifies an ability or effect triggered when the unit dies, optionally with a pop_corpse flag. | 4 | `BBExplode`<br>`BloatyExplodey`<br>`BombFlyExplode` |
| `DodgeChance_Status` | Integer | The flat percentage increase to dodge chance applied as a status effect. | 4 | `1`<br>`10`<br>`100` |
| `MissChance` | Integer | The flat percentage chance that the unit's attacks will miss. | 4 | `10`<br>`15`<br>`20` |
| `PermanentMadness` | Integer | The number of permanent madness stacks applied. | 4 | `1` |
| `ExtraBasicAttacks` | Integer | The number of additional basic attacks the unit can perform per turn. | 4 | `1`<br>`2` |
| [`AddTag`](../Reference_and_Meta/Enums.md#enum-addtag) | Enum  | Specifies a gameplay tag (e.g., 'rock', 'plant') to add to the unit, used for interaction checks. | 4 | `bug`<br>`cat`<br>`fetus` |
| [`AmplifyStatus`](../Reference_and_Meta/Enums.md#enum-amplifystatus) | Enum | Specifies the status effect to amplify, or an object with the status and number of stacks to add. | 4 | `Bleed`<br>`Burn`<br>`Poison` |
| `DepressionAura` | Integer | The number of stacks of Depression status applied to nearby enemies each turn; can be an object with range and ally settings. | 4 | `1`<br>`2` |
| `ExtraWeaponAttacks` | Integer | The number of additional weapon attacks the unit can perform. | 4 | `1`<br>`2` |
| [`AddDamageToElementDamage`](./Items_and_Equipment.md#object-adddamagetoelementdamage) | Object  | Defines additional damage of a specific element added to the unit's attacks. | 4 | `{ . . . }` |
| [`ClassManaCostReduction`](./Items_and_Equipment.md#object-classmanacostreduction) | Object  | Defines a reduction in mana cost for abilities of a specific class. | 4 | `{ . . . }` |
| [`StatusRandomEnemiesOnBattleStart`](./Items_and_Equipment.md#object-statusrandomenemiesonbattlestart) | Object | An object that applies a status effect to a random number of enemies at the start of battle, with sub-keys for count and the status. | 4 | `{ . . . }` |
| [`SpawnObjectOnPopCorpse`](./Items_and_Equipment.md#object-spawnobjectonpopcorpse) | Enum / Object | Specifies an object (as a string or an object with 'object', 'count', 'except_tiny' keys) to spawn on a corpse when it is popped. | 4 | `{ . . . }`<br>`Catnip`<br>`Coin`<br>`Food` |
| [`StatusOnTurnEndIfDidntCastAbilityTypes`](./Items_and_Equipment.md#object-statusonturnendifdidntcastabilitytypes) | Object | Applies the contained status effects at turn end if the unit did not cast an ability of the specified type(s). | 4 | `{ . . . }` |
| [`FragileDuringElement`](../Reference_and_Meta/Enums.md#enum-fragileduringelement) | Enum | Specifies an element during which the unit becomes fragile, taking increased damage. | 4 | `water` |
| `BreakAtAux` | Integer | The number of auxiliary item uses before this item breaks. | 4 | `0` |
| [`RandomSeededStatModifier`](../Reference_and_Meta/Arrays.md#array-randomseededstatmodifier) | Array | An array defining a random, seeded modifier to stats, typically in the format [modifier, offset]. | 4 | `[2 -1]` |
| [`StatusOnTakeHealthOrShieldDamage`](./Items_and_Equipment.md#object-statusontakehealthorshielddamage) | Object | An object that applies a status effect when the unit takes damage to either health or shields. | 4 | `{ . . . }` |
| [`CounterAttack`](./Items_and_Equipment.md#object-counterattack) | Object  | Specifies the ability used when the unit counterattacks after being hit. | 3 | `{ . . . }` |
| [`SpawnExtraThingsOnBattleStart`](./Items_and_Equipment.md#object-spawnextrathingsonbattlestart) | Object  | An object with `object` and `number` (or range) defining what and how many objects to spawn at battle start. | 3 | `{ . . . }` |
| [`DeathRattleRevive`](../Reference_and_Meta/Enums.md#enum-deathrattlerevive) | Enum  | Specifies an ability or effect that revives the unit upon death, with options for stunning behavior. | 3 | `DoNothing`<br>`HCHumanDie`<br>`ToxPuff` |
| `AlphaTurns` | Integer | The number of turns the unit acts first in battle; negative values may indicate last. | 3 | `-1`<br>`1` |
| [`PassiveAtStatThreshold`](./Items_and_Equipment.md#object-passiveatstatthreshold) | Object | An object defining passives granted when a unit's stat meets a specified threshold. | 3 | `{ . . . }` |
| `AddBonusMeleeRange` | Integer | The number of additional tiles of range added to the unit's melee attacks. | 3 | `1`<br>`10`<br>`2` |
| [`StatusIfUnusedMovePoints`](./Items_and_Equipment.md#object-statusifunusedmovepoints) | Object  | Specifies status effects applied if the unit ends its turn with unused movement points. | 3 | `{ . . . }` |
| `AddKnockbackDamage` | Integer | The amount of additional knockback damage applied. | 3 | `1`<br>`2`<br>`3` |
| [`CatchProjectiles`](./Items_and_Equipment.md#object-catchprojectiles) | Object | An object defining chance to catch projectiles and optionally apply statuses. | 3 | `{ . . . }` |
| [`StatusEveryXSpellCasts`](./Items_and_Equipment.md#object-statuseveryxspellcasts) | Object  | An object with `stacks` (number of spell casts) and status effects to apply after that many spell casts. | 3 | `{ . . . }` |
| `IncreaseExplosionSize` | Integer | The number of extra tiles added to the radius of explosions. | 3 | `1`<br>`2`<br>`7` |
| `TrinketActiveEffectsMultiplierBonus` | Integer | Bonus multiplier to the active effects of equipped trinkets. | 3 | `1`<br>`2` |
| `HeadArmorPassiveMultiplierBonus` | Integer | A multiplier bonus applied to passive effects granted by head armor. | 3 | `1`<br>`2` |
| [`ExtraStatusWhenDealingDamage`](./Items_and_Equipment.md#object-extrastatuswhendealingdamage) | Object | Defines additional statuses applied to the target or source when dealing damage, with conditionals. | 3 | `{ . . . }` |
| [`StatusOnPopCorpse`](./Items_and_Equipment.md#object-statusonpopcorpse) | Object | Specifies the effects applied when the unit pops a corpse. | 3 | `{ . . . }` |
| [`StatusAllCharactersOnSpawn`](./Items_and_Equipment.md#object-statusallcharactersonspawn) | Object  | Defines status effects applied to all characters when they spawn into the battlefield. | 3 | `{ . . . }` |
| `FaceArmorPassiveMultiplierBonus` | Integer | A multiplier bonus applied to the effects of face armor passives. | 3 | `1`<br>`2` |
| [`PassiveWhenDead`](./Items_and_Equipment.md#object-passivewhendead) | Object  | Passive effects that remain active while the unit is dead. | 3 | `{ . . . }` |
| [`DisableAbilities`](../Reference_and_Meta/Enums.md#enum-disableabilities) | Enum | Specifies which category of abilities to disable, such as 'all_items' or 'basic_attack'. | 3 | `all_items`<br>`all_spells`<br>`basic_attack` |
| `AddEndOfCombatRegen` | Integer | The amount of health regenerated after combat ends. | 3 | `12`<br>`999999` |
| `AllStatsUpPerDisorder` | Integer | The amount by which all stats increase for each disorder (negative status) the unit has. | 3 | `1` |
| `BoneArmorPassive` | Integer | The number of stacks of bone armor granted, which absorbs damage. | 3 | `1` |
| [`BreakOnElement`](../Reference_and_Meta/Enums.md#enum-breakonelement) | Enum | Specifies an element that, when dealt to the unit, causes its armor or item to break. | 3 | `water` |
| `CantCatchDiseases` | Integer | The number of stacks that prevent the unit from contracting diseases. | 3 | `1` |
| `CantSpreadDiseases` | Integer | The number of stacks that prevent the unit from spreading diseases. | 3 | `1` |
| `ChanceToBlock` | Integer | The percentage chance to block incoming damage. | 3 | `10%` |
| [`DropAsFamiliarOnArmorBreak`](../Reference_and_Meta/Enums.md#enum-dropasfamiliaronarmorbreak) | Enum | Specifies the familiar type to drop onto the tile when this status holder's armor breaks. | 3 | `FaceGrubFamiliar`<br>`HeadGrubFamiliar`<br>`NeckGrubFamiliar` |
| `RockyArmorPassive` | Integer | The number of stacks of the Rocky Armor status effect granted. | 3 | `1` |
| [`StackingFlowerTrail`](./Items_and_Equipment.md#object-stackingflowertrail) | Object | An object defining how a flower trail status stacks (stacks count, stack key) when the unit moves. | 3 | `{ . . . }` |
| `TrueShot` | Integer | The number of stacks of a buff that makes the unit's attacks unmissable. | 3 | `1` |
| `CopyPassiveSlot` | Integer | An index (0-based) specifying which equipment slot's passive to copy onto this unit. | 3 | `0`<br>`1` |
| `DodgeChance` | Integer | The percentage chance the unit has to dodge incoming attacks. | 2 | `10%`<br>`15%`<br>`2%` |
| [`ReplaceBasicAttack`](../Reference_and_Meta/Enums.md#enum-replacebasicattack) | Enum  | Specifies the ability ID that replaces the unit's basic attack. | 2 | `BasicButcherMeleeWideDoubleSpin`<br>`BasicButcherMeleeWideSpin`<br>`BasicDruidAbilityVersatile` |
| `MoveQuivered` | Float | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 2 | `1`<br>`2`<br>`[1, 0.1]` |
| [`InnateElement`](../Reference_and_Meta/Enums.md#enum-innateelement) | Enum  | Specifies the innate elemental type of the unit (e.g., Fire, Ice, Electric). | 2 | `Earth`<br>`Electric`<br>`Fire` |
| [`BonusAbility`](../Reference_and_Meta/Enums.md#enum-bonusability) | Enum  | Specifies the name of a bonus ability granted. | 2 | `Bloodzerk`<br>`BonusToss`<br>`BonusToss2` |
| `ReflectProjectiles` | Integer | The percentage chance to reflect projectiles back at the attacker; optionally includes self-damage. | 2 | `1`<br>`10%`<br>`100%` |
| [`ReplaceSpawnedObjects`](../Reference_and_Meta/Arrays.md#array-replacespawnedobjects) | Array | An array of [original_object replacement_object] pairs for swapping spawned objects. | 2 | `[Boulder AnimatedBoulder]`<br>`[Boulder AnimatedLavaBoulder]`<br>`[Crow Crow2]` |
| `InjuryImmunity` | Integer | The number of turns the unit is immune to injuries. | 2 | `1` |
| `KnockbackImmunity` | Integer | If set to 1, the unit cannot be knocked back. | 2 | `1` |
| `AddInitiative` | Integer | The amount of bonus or penalty to the unit's turn order initiative value. | 2 | `-10`<br>`-100`<br>`-20` |
| `IncreaseExplosionDamage` | Integer | The flat amount by which explosion damage is increased. | 2 | `1`<br>`2`<br>`3` |
| [`BoostWeaponDamage`](./Items_and_Equipment.md#object-boostweapondamage) | Object  | The amount of bonus weapon damage applied, or an object with `damage` and `crit_chance` fields. | 2 | `{ . . . }` |
| [`StatusOnCastSpell`](./Items_and_Equipment.md#object-statusoncastspell) | Object  | An object listing status effects applied to the unit whenever it casts a spell. | 2 | `{ . . . }` |
| `BackstabCritChance` | Float | A multiplier for critical hit chance on backstab attacks. | 2 | `.25`<br>`1` |
| [`AddStatusToElementDamage`](./Items_and_Equipment.md#object-addstatustoelementdamage) | Object | An object that applies a specific status effect when dealing damage of a specified element. Contains sub-keys for the element and the status to apply. | 2 | `{ . . . }` |
| [`ChanceToBackflip`](./Items_and_Equipment.md#object-chancetobackflip) | Object  | An object specifying the ability to use and the percentage chance to perform a backflip dodge when hit. | 2 | `{ . . . }` |
| `FreezePiercing` | Integer | The number of stacks of freeze resistance that are ignored when applying freeze. | 2 | `1` |
| [`LevelUpClassOverride`](../Reference_and_Meta/Enums.md#enum-levelupclassoverride) | Enum | Specifies which class the unit gains upon leveling up, overriding the default class. | 2 | `Colorless`<br>`Jester` |
| [`StatusOnAllyCatDeath`](./Items_and_Equipment.md#object-statusonallycatdeath) | Object  | An object listing status effects applied to the unit when an allied cat dies. | 2 | `{ . . . }` |
| [`StatusOnGainCoins`](./Items_and_Equipment.md#object-statusongaincoins) | Object  | Specifies status effects applied when this unit gains coins. | 2 | `{ . . . }` |
| `ExtraBasicMoves_Status` | Integer | The number of extra basic moves per turn granted. | 2 | `1` |
| `Uncontrollable` | Integer | If non-zero, the unit becomes uncontrollable by the player. | 2 | `1` |
| `AmplifyKnockback` | Integer | The additional distance (in tiles) a unit is knocked back. | 2 | `10`<br>`2` |
| [`ElementalManaCostReduction`](./Items_and_Equipment.md#object-elementalmanacostreduction) | Object | An object that reduces the mana cost of spells of specified elements, with sub-keys for element and reduction amount. | 2 | `{ . . . }` |
| [`AddStatusToSpells`](./Items_and_Equipment.md#object-addstatustospells) | Object  | Specifies status effects added to all spell attacks used by this unit. | 2 | `{ . . . }` |
| [`ApplyStatusesToRandomEnemiesEachTurn`](./Items_and_Equipment.md#object-applystatusestorandomenemieseachturn) | Object | An object specifying statuses to apply to random enemies each turn, with an optional 'count' field. | 2 | `{ . . . }` |
| `AutoEquipConsumables` | Integer | The number of consumables automatically equipped per turn. | 2 | `1` |
| [`ChanceToBlockAndCounter`](./Items_and_Equipment.md#object-chancetoblockandcounter) | Integer / Object | The percentage chance or an object defining chance and conditions to block and counter an attack. | 2 | `{ . . . }`<br>`15%`<br>`25%`<br>`33%` |
| `FlowersOnEndTurn` | Integer | The number of flowers spawned on the unit's tile at the end of each turn. | 2 | `1`<br>`3`<br>`4` |
| `IncreaseSpellRange` | Integer | The number of extra tiles added to the range of spells. | 2 | `10`<br>`2`<br>`20` |
| [`KillsToMeat`](../Reference_and_Meta/Enums.md#enum-killstomeat) | Enum | Specifies the type of meat item spawned when killing certain enemies. | 2 | `Food` |
| [`PassiveAfterXKills`](./Items_and_Equipment.md#object-passiveafterxkills) | Object | Activates a set of passive effects (e.g., extra attacks, stat boosts) after the unit achieves a certain number of kills defined by the 'stacks' sub-key. | 2 | `{ . . . }` |
| `RangedTrueShot` | Integer | Ranged attacks cannot miss or be dodged, guaranteeing a hit. Value acts as a binary flag. | 2 | `1` |
| [`StatusAfterCastSpell`](./Items_and_Equipment.md#object-statusaftercastspell) | Object | An object containing status effects to apply to the unit immediately after it casts any spell. | 2 | `{ . . . }` |
| [`StatusOnBreakItem`](./Items_and_Equipment.md#object-statusonbreakitem) | Object | An object containing status effects to apply when the unit breaks a weapon or armor item. | 2 | `{ . . . }` |
| `NeckArmorPassiveMultiplierBonus` | Integer | A multiplier bonus applied to the passives of the unit's neck armor slot. | 2 | `1`<br>`2` |
| [`SetDefaultFacePassive`](../Reference_and_Meta/Enums.md#enum-setdefaultfacepassive) | Enum | Specifies the name of the default face passive to be assigned to this unit. | 2 | `euphoric`<br>`insane` |
| [`AddStatusToKnockbackDamage`](./Items_and_Equipment.md#object-addstatustoknockbackdamage) | Object | An object whose nested keys define statuses applied to damage caused by knockback. | 2 | `{ . . . }` |
| [`FindExtraItemFromPoolOnBattleEnd`](../Reference_and_Meta/Enums.md#enum-findextraitemfrompoolonbattleend) | Enum  | Specifies the item pool from which an extra item is granted at the end of combat. | 2 | `combat_reward_easy`<br>`pills` |
| [`ArmorBreakOnHit`](./Items_and_Equipment.md#object-armorbreakonhit) | Object | An object defining durability loss and chance for armor to break when hit. | 2 | `{ . . . }` |
| `BreakWhenNoShield` | Integer | If 1, the armor breaks when the unit has no shield remaining. | 2 | `1` |
| `CanLevelUpWhenDead` | Integer | If 1, allows the unit to gain experience and level up while dead. | 2 | `1` |
| [`LeaveBehindOnceEachMove`](../Reference_and_Meta/Enums.md#enum-leavebehindonceeachmove) | Enum | Specifies the object left behind on the tile once per move. | 2 | `Poop`<br>`Scrap` |
| [`PassiveIfWeaponIsUsable`](./Items_and_Equipment.md#object-passiveifweaponisusable) | Object | Activates a set of passive effects (e.g., Brace) only if the unit's current weapon is in a usable condition (not broken or disabled). | 2 | `{ . . . }` |
| [`RefreshEquipmentAbilityOnElement`](./Items_and_Equipment.md#object-refreshequipmentabilityonelement) | Object | Refreshes the cooldown of the unit's equipment ability when the unit's attack matches the specified element (e.g., Electric), displaying a recharge popup. | 2 | `{ . . . }` |
| [`SpawnItemLinkedFamiliar`](./Items_and_Equipment.md#object-spawnitemlinkedfamiliar) | Object | An object defining a familiar to spawn that is linked to a specific item, which breaks when the familiar is defeated. | 2 | `{ . . . }` |
| `SpawnNearEnemies` | Integer | The number of units to spawn near each enemy at the start of battle. | 2 | `1` |
| [`StatusIfUnusedActPoints`](./Items_and_Equipment.md#object-statusifunusedactpoints) | Object | An object containing status effects to apply to the unit if it has unused action points at the end of its turn. | 2 | `{ . . . }` |
| [`StatusOnBackstab`](./Items_and_Equipment.md#object-statusonbackstab) | Object | An object containing status effects to apply when the unit performs a backstab attack. | 2 | `{ . . . }` |
| `DisablePassiveSlot` | Integer | If non-zero, disables the specified passive slot index (0 or 1). | 2 | `0`<br>`1` |
| [`SpawnOnDeath`](./Items_and_Equipment.md#object-spawnondeath) | Object  | Specifies an object and its faction to spawn when the unit dies. | 1 | `{ . . . }` |
| `LuckUp` | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 1 | `-1`<br>`-2`<br>`-4` |
| `Blind` | Integer | The amount of blind stacks applied, or an [stacks, probability] array. | 1 | `-1`<br>`1`<br>`2` |
| `Charge` | Equation | The number of charge stacks applied. | 1 | `1`<br>`2`<br>`3` |
| `Undead` | Integer | If set, flags the unit as undead (e.g., 1) with associated mechanics. | 1 | `1` |
| [`AbilityReaction`](../Reference_and_Meta/Enums.md#enum-abilityreaction) | Enum  | Specifies the ability used as a reaction when the unit is targeted by an ability. | 1 | `AnkyloSpin`<br>`GSOpen`<br>`Gassy_AssBlast` |
| `AddCritMultiplier` | Integer | The percentage added to the critical hit damage multiplier. | 1 | `100%`<br>`125%`<br>`150%` |
| [`PassiveWhenAffectedByElement`](./Items_and_Equipment.md#object-passivewhenaffectedbyelement) | Object  | An object containing `element` and `passives` that grants the listed passives while the unit is affected by the specified element. | 1 | `{ . . . }` |
| `AlphaCat` | Integer | The number of AlphaCat stacks applied to the source on kill. | 1 | `1` |
| `IgnoreTiles` | Integer | If set to 1, movement ignores tile-based penalties or restrictions. | 1 | `1` |
| [`BackflipWhenTargeted`](./Items_and_Equipment.md#object-backflipwhentargeted) | Enum / Object  | The number of backflip charges, or an object defining its ability. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`X` |
| [`AbilityHealthThreshold`](./Items_and_Equipment.md#object-abilityhealththreshold) | Object  | Defines an ability and conditions for its activation when the unit's health reaches a threshold. | 1 | `{ . . . }` |
| [`CritsApplyStatus`](./Items_and_Equipment.md#object-critsapplystatus) | Object | An object containing statuses applied to the target when the unit lands a critical hit. | 1 | `{ . . . }` |
| [`MoveTowardsDamageSource`](../Reference_and_Meta/Enums.md#enum-movetowardsdamagesource) | Enum  | Determines the movement behavior when moving towards the unit that dealt damage to it. | 1 | `MoveOne` |
| [`MovementReaction`](./Items_and_Equipment.md#object-movementreaction) | Object  | Specifies an ability to cast when a unit moves within range, with options for targeting and conditions. | 1 | `{ . . . }` |
| `ExtraMovePoints` | Integer | The number of additional movement points granted to this unit. | 1 | `1` |
| `DebuffImmunity` | Integer | If 1, the unit is immune to debuffs. | 1 | `1` |
| `SetSpellCosts` | Integer | Overrides the cost of all spells to this value. | 1 | `0`<br>`1`<br>`3` |
| [`AddStatusToWeapons`](./Items_and_Equipment.md#object-addstatustoweapons) | Object  | Specifies status effects to add to the unit's weapon attacks, with their stack counts. | 1 | `{ . . . }` |
| [`StatusAlliesOnDeath`](./Items_and_Equipment.md#object-statusalliesondeath) | Object | Applies the contained status effects to all allies when the unit dies. | 1 | `{ . . . }` |
| [`SpawnOnDowned`](../Reference_and_Meta/Enums.md#enum-spawnondowned) | Enum  | Specifies the character or object spawned when the unit is downed. | 1 | `CharmedFly`<br>`CharmedKitten`<br>`CharmedSpookie` |
| [`AddTemporaryEffectsToBasicAttack`](./Items_and_Equipment.md#object-addtemporaryeffectstobasicattack) | Object  | A container object that lists temporary status effects applied to the unit's basic attack. | 1 | `{ . . . }` |
| `ExtraBasicAttacks_Status` | Integer | The number of additional basic attacks the unit can perform each turn. | 1 | `1` |
| [`AddHiddenTag`](../Reference_and_Meta/Enums.md#enum-addhiddentag) | Enum  | A hidden tag applied to the unit for internal logic and triggers. | 1 | `bowling_ball`<br>`grown_hitler_clone`<br>`hitler_clone_fetus` |
| `FaceShield` | Integer | If 1, the unit has a face shield that protects it from certain attacks or effects. | 1 | `0`<br>`1` |
| `Lifesteal` | Integer | The amount of lifesteal stacks applied. | 1 | `1`<br>`3` |
| `SharkySmellsBlood` | Integer | If 1, the unit is attracted to damaged units and may prioritize them. | 1 | `1` |
| `MakeSpellsRequireCharge` | Integer | If true, spells require a charge-up turn before casting. | 1 | `1` |
| [`AddPassivesToCharmed`](./Items_and_Equipment.md#object-addpassivestocharmed) | Object | Grants the contained passive effects to units under the charm status. | 1 | `{ . . . }` |
| [`StatusOnEatFood`](./Items_and_Equipment.md#object-statusoneatfood) | Object  | An object listing status effects applied to the unit when it eats food. | 1 | `{ . . . }` |
| [`CreateGlobalModifiers`](./Items_and_Equipment.md#object-createglobalmodifiers) | Object  | Defines global gameplay modifiers to activate. | 1 | `{ . . . }` |
| [`Eternal`](./Items_and_Equipment.md#object-eternal) | Object | Defines the Eternal revival effect, setting stacks and the health percentage restored. | 1 | `{ . . . }` |
| `ReduceManaCost` | Integer | The number of stacks reducing mana cost of abilities. | 1 | `1`<br>`2` |
| [`BuffImmunity`](./Items_and_Equipment.md#object-buffimmunity) | Object  | If 1, the unit is immune to buffs. An optional object can list buffs to exclude from immunity. | 1 | `{ . . . }` |
| `AllyDamageReduction` | Integer | The amount by which damage dealt to allies is reduced. | 1 | `0` |
| [`FlyDamageIncrease`](./Items_and_Equipment.md#object-flydamageincrease) | Object | The number of stacks or alias for damage increase against flying units. | 1 | `{ . . . }` |
| [`PoopWhenHit`](./Items_and_Equipment.md#object-poopwhenhit) | Object  | Specifies the object (e.g., Poop) spawned when the unit is hit, or an object with `chance` and `object`. | 1 | `{ . . . }` |
| [`StatusEachTurnEndForEachTurn`](./Items_and_Equipment.md#object-statuseachturnendforeachturn) | Object  | Statuses applied at the end of each turn, with the number of turns as nested values. | 1 | `{ . . . }` |
| [`StatusOnHealed`](./Items_and_Equipment.md#object-statusonhealed) | Object | An object that applies a status effect to the unit whenever it is healed. | 1 | `{ . . . }` |
| `TauntAlways` | Integer | If non-zero, the unit is always taunted, forcing it to target the first enemy in range. | 1 | `1` |
| `FrankBolts` | Integer | The number of Frank Bolts applied or available. | 1 | `1` |
| `BasicAttackCritChance` | Float | A multiplier for the critical hit chance of basic attacks, either as a float or percentage. | 1 | `.1`<br>`100%` |
| [`MoveAndUseAbilityEachTurnBeginIfPossible`](../Reference_and_Meta/Enums.md#enum-moveanduseabilityeachturnbeginifpossible) | Enum | Specifies the name of the ability the unit will move and attempt to use at the start of each of its turns. | 1 | `Cannibalize`<br>`EatShit`<br>`face_EatNeverstone` |
| [`AddSelfStatusToWeapons`](./Items_and_Equipment.md#object-addselfstatustoweapons) | Object | An object whose nested keys define status effects applied to the unit's own weapons. | 1 | `{ . . . }` |
| [`BouncyProjectiles`](./Items_and_Equipment.md#object-bouncyprojectiles) | Object | An object with 'max_bounces' and 'max_range' defining projectile bounciness behavior. | 1 | `{ . . . }` |
| `CanRemoveCursedItems` | Integer | If nonzero, allows the unit to remove cursed items from equipment slots. | 1 | `1` |
| `ConsumableEffectsMultiplierBonus` | Integer | A multiplier bonus applied to the effects of consumable items. | 1 | `1` |
| `DoubleCastWeapons` | Integer | The number of additional weapon casts per attack. | 1 | `1`<br>`2` |
| `GainExtraShield` | Integer | The amount of shield gained on turn start. | 1 | `2`<br>`4` |
| [`PassiveWhileInMonkMeleeStance`](./Items_and_Equipment.md#object-passivewhileinmonkmeleestance) | Object | Applies specific passive effects (e.g., Brace, HealthRegenUp) while the unit is in the Monk's melee combat stance. | 1 | `{ . . . }` |
| `RemoveLineOfSightRestrictions` | Integer | Line of sight requirements for targeting are ignored, allowing the unit to target any visible cell regardless of obstacles. | 1 | `1` |
| [`ScaledStatusOnSpendMana`](./Items_and_Equipment.md#object-scaledstatusonspendmana) | Object | An object containing status effect definitions to apply when the unit spends mana, with the number of stacks scaled by the amount of mana spent. | 1 | `{ . . . }` |
| [`StatusOnCollectPickup`](./Items_and_Equipment.md#object-statusoncollectpickup) | Object | An object containing status effects to apply when the unit collects a pickup item. | 1 | `{ . . . }` |
| [`StatusOnPickupCoins`](./Items_and_Equipment.md#object-statusonpickupcoins) | Object | Specifies the effects applied when the unit picks up coins. | 1 | `{ . . . }` |
| [`StatusOnUseBasicAttack`](./Items_and_Equipment.md#object-statusonusebasicattack) | Object | Specifies the effects applied when the unit performs a basic attack. | 1 | `{ . . . }` |
| [`StatusWhenAllySpendsMana`](./Items_and_Equipment.md#object-statuswhenallyspendsmana) | Object | Specifies the effects applied when an ally spends mana. | 1 | `{ . . . }` |
| `WeaponDamageMultiplierBonus` | Integer | Bonus multiplier to weapon damage. | 1 | `1`<br>`2` |
| `CapMovementAbilityRange` | Integer | The maximum range allowed for movement abilities. | 1 | `1` |
| `HPGainBlock` | Integer | If true, the unit cannot gain health from any source. | 1 | `1` |
| `MoveSpeedMultiplier` | Float | A multiplier for the unit's movement speed. | 1 | `.5` |
| [`StatusAfterXTurns`](./Items_and_Equipment.md#object-statusafterxturns) | Object  | Applies a status effect or forces an ability usage after a set number of turns. | 1 | `{ . . . }` |
| [`AllyDodgeChanceAura`](./Items_and_Equipment.md#object-allydodgechanceaura) | Object | An object granting allies within a specified range a percentage chance to dodge incoming attacks. | 1 | `{ . . . }` |
| `AlphaAllStatsUp` | Integer | The amount by which all of the unit's stats are increased if it is the alpha (highest stat total or designated leader). | 1 | `1` |
| `BasicAttackCantMiss` | Integer | If nonzero, the unit's basic attack cannot miss. | 1 | `1` |
| `CounterNextAttacks` | Integer | The number of incoming attacks the unit will counterattack. | 1 | `2` |
| `ExplosionImmunity` | Integer | If non-zero, grants immunity to explosion damage. | 1 | `1` |
| `ExtraTrinketUses` | Integer | The number of additional uses granted to trinkets. | 1 | `1`<br>`10` |
| `MakeBasicAttackPull` | Integer | If nonzero, the unit's basic attack pulls the target closer. | 1 | `1` |
| [`StatusAlliesEachTurn`](./Items_and_Equipment.md#object-statusallieseachturn) | Object | Defines a status effect applied to all allies each turn, with an optional exclusion of the owner and conditional checks. | 1 | `{ . . . }` |
| [`AIControlNextTurn`](./Items_and_Equipment.md#object-aicontrolnextturn) | Object | An object that causes the unit to be controlled by the AI on its next turn, with configurable stacks and spell usage. | 1 | `{ . . . }` |
| `AOEBonus` | Integer | The bonus number of additional targets or tiles affected by an area-of-effect ability. | 1 | `1` |
| [`AbilityOnRoundEndOnce`](./Items_and_Equipment.md#object-abilityonroundendonce) | Object | Specifies an ability to be used once at the end of the round. | 1 | `{ . . . }` |
| [`AddAdvantageToEvent`](./Items_and_Equipment.md#object-addadvantagetoevent) | Object | Specifies additional advantage options to add to a specific event type. | 1 | `{ . . . }` |
| [`AddStatusToBackstabs`](./Items_and_Equipment.md#object-addstatustobackstabs) | Object | An object defining statuses applied to the target when the unit performs a backstab attack. | 1 | `{ . . . }` |
| `AllSpellsCostCharge` | Integer | The number of charges required to cast any spell, adding a universal charge cost. | 1 | `1` |
| `AllUnitsExplodeOnDeath` | Integer | The radius of the explosion that triggers when any unit dies. | 1 | `5` |
| `AlliesScrambleSpellAfterCast` | Integer | The number of times an ally's next spell cast will be scrambled (randomly redirected or modified) after the owner casts a spell. | 1 | `1` |
| [`AlluringDoodieEater`](./Items_and_Equipment.md#object-alluringdoodieeater) | Object | An object defining the chance and damage instance for a unit that consumes an alluring doodie. | 1 | `{ . . . }` |
| `AlwaysChosenForLevelUp` | Integer | If set to 1, this unit is always presented as a level-up option when gaining a level. | 1 | `1` |
| `BalanceStats` | Integer | If set to 1, the unit's stats are balanced (redistributed) towards an average value. | 1 | `1` |
| `BlockDamageUnderThreshold` | Integer | The maximum amount of damage from a single hit that will be completely blocked. | 1 | `1` |
| `BlockNegativeStatus` | Integer | The percentage chance to completely block the application of a negative status effect. | 1 | `30%` |
| `BoostReceivedHealing` | Integer | The amount of bonus healing received from all sources. | 1 | `2` |
| `CapBasicAttackDamage` | Integer | The maximum amount of damage that can be dealt by a basic attack. | 1 | `1` |
| [`CatPartsSizeScale`](./Items_and_Equipment.md#object-catpartssizescale) | Object | A multiplier for the size of specific cat parts (e.g., head, body). | 1 | `{ . . . }` |
| `ChanceToAmbush` | Integer | The percentage chance for the unit to ambush an enemy. | 1 | `25%` |
| [`ChanceToForceEvent`](./Items_and_Equipment.md#object-chancetoforceevent) | Object | Defines the chance and the specific event to force to occur. | 1 | `{ . . . }` |
| `CharismaIsMaxStat` | Integer | Treats the Charisma stat as the character's maximum stat for calculations. | 1 | `1` |
| `CharmImmunity` | Integer | If true, the unit is immune to the Charmed status effect. | 1 | `1` |
| [`ConvertDamageToScaledStatus`](./Items_and_Equipment.md#object-convertdamagetoscaledstatus) | Object | Converts a portion of incoming damage into a specified status effect with a given number of stacks. | 1 | `{ . . . }` |
| `DoubleCastSpellIfManaCostUnderThreshold` | Integer | If a spell's mana cost is under this threshold, it will be cast twice. | 1 | `3` |
| [`DoubleCastTaggedSpells`](../Reference_and_Meta/Enums.md#enum-doublecasttaggedspells) | Enum | Specifies the spell tag (e.g., musical) that causes spells to be cast twice. | 1 | `musical` |
| `DoubleReceivedNegativeStatus` | Integer | If true, the unit receives double the stacks of negative status effects applied to it. | 1 | `1` |
| `DoubleReceivedPositiveStatus` | Integer | If true, the unit receives double the stacks of positive status effects applied to it. | 1 | `1` |
| [`DropAsFamiliarOnTookDamage`](../Reference_and_Meta/Enums.md#enum-dropasfamiliarontookdamage) | Enum | Specifies the familiar type to be dropped when the unit takes damage. | 1 | `PhantomMaskRock` |
| [`DropSoulJarOnDeath`](../Reference_and_Meta/Enums.md#enum-dropsouljarondeath) | Enum | Specifies the type of soul jar to be dropped when the unit dies. | 1 | `SoulJar_Full` |
| [`ExcludeFromEvents`](../Reference_and_Meta/Enums.md#enum-excludefromevents) | Enum | Specifies the event type (e.g., Tragedy) that this unit is excluded from participating in. | 1 | `Tragedy` |
| [`GlobalMeleeRevengeDamage`](./Items_and_Equipment.md#object-globalmeleerevengedamage) | Object | Defines revenge damage properties (e.g., knockback) when hit by a melee attack. | 1 | `{ . . . }` |
| `HideSomeHudStuff` | Integer | If set to 1, hides certain HUD elements. | 1 | `1` |
| `JesterLevelUpRerolls` | Integer | The number of additional rerolls granted when leveling up. | 1 | `1` |
| `ModelingClayPassive` | Integer | If set to 1, enables the passive that duplicates the equipped item on the unit. | 1 | `1` |
| `MultiplyCoinsOnBattleStart` | Integer | The multiplier applied to the unit's coin count at the start of battle. | 1 | `2` |
| `MultiplyReceivedHealing` | Integer | The multiplier applied to all healing the unit receives. | 1 | `2` |
| [`ObjectDetector`](./Items_and_Equipment.md#object-objectdetector) | Object | An object that grants a chance to detect a specific item (e.g., CharmedDip) when loot is evaluated. | 1 | `{ . . . }` |
| [`PassiveWhileHasDurability`](./Items_and_Equipment.md#object-passivewhilehasdurability) | Object | An object containing passives that are active only while the item has remaining durability. | 1 | `{ . . . }` |
| [`PassiveWhileShielded`](./Items_and_Equipment.md#object-passivewhileshielded) | Object | An object containing passives that are active only while the unit has a shield. | 1 | `{ . . . }` |
| `PhysicalAttacksMiss` | Integer | If set to 1, all physical attacks against the unit automatically miss. | 1 | `1` |
| `PreventSpecificInjury` | Enum | Specifies a body part tag (e.g., 'int' for head) that cannot receive injuries. | 1 | `int` |
| `ReclaimItemOnBreak` | Integer | If set to 1, the item returns to the inventory when it breaks instead of being lost. | 1 | `1` |
| `ReduceSpellCostsPerDisorder` | Integer | The amount of mana cost reduction per disorder the unit has. | 1 | `1` |
| `ReduceSpellCostsPerParasite` | Integer | The amount of mana cost reduction per parasite the unit is hosting. | 1 | `1` |
| [`ReplaceBlankTilesOnBattleStart`](../Reference_and_Meta/Enums.md#enum-replaceblanktilesonbattlestart) | Enum | Specifies a tile type (e.g., GlassTile) that replaces all blank tiles on the battle grid at the start of combat. | 1 | `GlassTile` |
| `RerollItemsOnBattleEnd` | Integer | If set to 1, all items in the unit's inventory are rerolled to new random items at the end of battle. | 1 | `1` |
| [`ScaldingOrbMoonBossOneShot`](./Items_and_Equipment.md#object-scaldingorbmoonbossoneshot) | Object | An object that completes the ScaldingOrb quest and removes the item from the unit's inventory. | 1 | `{ . . . }` |
| [`ScaledStatusAlliesOnSpendMana`](./Items_and_Equipment.md#object-scaledstatusalliesonspendmana) | Object | An object that applies a scaled status (e.g., ManaGain) to adjacent allies whenever the unit spends mana. | 1 | `{ . . . }` |
| [`ScaledStatusOnHolyShieldBlock`](./Items_and_Equipment.md#object-scaledstatusonholyshieldblock) | Object | An object that applies a scaled status (e.g., RandomMagicMissile) when the unit blocks an attack with a holy shield. | 1 | `{ . . . }` |
| [`SetFaction`](../Reference_and_Meta/Enums.md#enum-setfaction) | Enum | Specifies the faction the unit belongs to (e.g., 'enemies'). | 1 | `enemies` |
| `SpawnCatCloneOnCorpsePopped` | Integer | The number of cat clones spawned when a corpse is popped (destroyed) by the unit. | 1 | `1` |
| [`SpawnRandomPickupsOnTaggedUnitKilled`](./Items_and_Equipment.md#object-spawnrandompickupsontaggedunitkilled) | Object | Defines a pool of random pickups (items) spawned when a unit with a specific tag is killed, with a count range. | 1 | `{ . . . }` |
| [`StatDependentPassive`](./Items_and_Equipment.md#object-statdependentpassive) | Object | An object containing formulas that dynamically modify passive effects based on the unit's stats (e.g., str, dex, int). | 1 | `{ . . . }` |
| [`StatusAdjacentOnTheirTurnEnd`](./Items_and_Equipment.md#object-statusadjacentontheirturnend) | Object | Defines a status effect applied to adjacent units when their turn ends, such as forcing them to move away. | 1 | `{ . . . }` |
| [`StatusOnDodge`](./Items_and_Equipment.md#object-statusondodge) | Object | Defines a status effect applied to the unit each time it successfully dodges an attack. | 1 | `{ . . . }` |
| [`StatusOnEnemyDeath`](./Items_and_Equipment.md#object-statusonenemydeath) | Object | Defines a status effect applied to the unit each time an enemy dies. | 1 | `{ . . . }` |
| [`StatusOnFallAsleep`](./Items_and_Equipment.md#object-statusonfallasleep) | Object | Defines one or more beneficial status effects applied to the unit when it falls asleep. | 1 | `{ . . . }` |
| [`StatusOnFullMana`](./Items_and_Equipment.md#object-statusonfullmana) | Object | Defines a status effect applied to the unit when its mana is full, with an optional once-per-battle conditional. | 1 | `{ . . . }` |
| `StevenBolts` | Integer | The number of Steven Bolts (a special resource or charge) the unit has for a unique ability. | 1 | `1` |
| `StripKnockback` | Integer | If non-zero, removes all knockback effects from the unit's attacks or abilities. | 1 | `1` |
| [`TintItem`](./Items_and_Equipment.md#object-tintitem) | Object | Defines additive and multiplicative color tint adjustments applied to an item's appearance, with an optional ignore condition. | 1 | `{ . . . }` |
| [`TunnelVision`](./Items_and_Equipment.md#object-tunnelvision) | Object | If present, grants the TunnelVision status, which modifies crit_chance as defined in its sub-properties. | 1 | `{ . . . }` |

</details>


---


### Object: `meta`


**Definition:** Contains metadata for the ability including name, description, class, and type icon.  
**Total Count:** 2374

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ModifyAbility`](./Items_and_Equipment.md#object-modifyability)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `is_basic_attack` | Boolean | If true, this ability is treated as a basic attack, typically used for default melee or ranged strikes without special properties. | 2 | `false`<br>`true` |
| `is_weapon` | Boolean | If true, this ability is classified as a weapon, allowing it to benefit from weapon-specific modifiers and UI grouping. | 2 | `true` |

</details>


---


### Object: `damage_instance`


**Definition:** Defines damage properties, effects, and healing for the ability's direct damage.  
**Total Count:** 2346

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AlluringDoodieEater`](./Items_and_Equipment.md#object-alluringdoodieeater)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 1 | `damage_instance`<br>`spell`<br>`self_damage` |
| [`effects`](./Items_and_Equipment.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 1 | `{ . . . }` |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 1 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 1 | `{ . . . }` |

</details>


---


### Object: `effects`


**Definition:** Applies a list of status effects or visual effects to targets.  
**Total Count:** 2166

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DoDamage`](./Items_and_Equipment.md#object-dodamage), [`MeleeRevengeDamage`](./Items_and_Equipment.md#object-meleerevengedamage), [`RevengeDamage`](./Items_and_Equipment.md#object-revengedamage), [`damage_instance`](./Items_and_Equipment.md#object-damage_instance)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 13 | passives<br>class<br>tag |
| `Bruise` | Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 9 | `1`<br>`2`<br>`3` |
| `Burn` | Equation | The amount of Burn applied, either as a fixed number or a formula string. | 4 | `1`<br>`10`<br>`2` |
| [`Fear`](../Reference_and_Meta/Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 4 | `1`<br>`10`<br>`2` |
| `BounceObject` | `String` | Specifies the object or projectile to spawn and bounce from the target. | 4 | `AllyRotFly`<br>`Amoeba`<br>`BeefyCharmedLeech` |
| [`Grappled`](../Reference_and_Meta/Arrays.md#array-grappled) | Array  | The number of stacks and probability of applying the Grappled status, in format [stacks, probability] or just stacks. | 4 | `1`<br>`[1, .50]`<br>`[1, .75]` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 3 | Default<br>FormChange<br>Druid |
| `Slow` | Integer | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 3 | `-1`<br>`1`<br>`2` |
| `Immobile` | Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 3 | `0`<br>`1`<br>`10%` |
| [`Conditional_GoodRoll`](./Items_and_Equipment.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 3 | `{ . . . }` |
| `Poison` | Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`10`<br>`2` |
| [`Stun`](../Reference_and_Meta/Arrays.md#array-stun) | Array  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`2`<br>`3` |
| `Confusion` | Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`10`<br>`2` |
| [`Freeze`](../Reference_and_Meta/Arrays.md#array-freeze) | Array / Integer  | The amount of freeze stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`2`<br>`[1 .01]` |
| `Blind` | Integer | The amount of blind stacks applied, or an [stacks, probability] array. | 1 | `-1`<br>`1`<br>`2` |
| `VisualFXTile` | `String` | Specifies the name of the visual effect to play on the target tile. | 1 | `Bolt`<br>`BurnTrigger`<br>`Explosion` |
| `Cleave` | Integer | The number of additional targets hit; if an object, contains a chance parameter for each cleave attempt. | 1 | `1` |
| `VisualFX` | `String` | Specifies the name of the visual effect to play. | 1 | `BigMagicMissileBlast`<br>`Bolt`<br>`Cleanse` |
| `DestroyTrinket` | Integer | The number of trinkets destroyed. | 0 | `1` |

</details>


---


### Object: `cost`


**Definition:** Defines the resource cost (e.g., mana) and other casting requirements.  
**Total Count:** 1903

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ModifyAbility`](./Items_and_Equipment.md#object-modifyability)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `mana` | Equation | The amount of mana required to cast, as a formula or stat. | 2 | `"4-clamp(floor(X/7), 0, 1)"`<br>`"max(4-X, 0)"`<br>`"max(7-2*X,0)"` |
| `charge` | Equation | The amount of charge required or the formula to calculate charge cost. | 2 | `"1-clamp(spd,0,1)"`<br>`0`<br>`1` |

</details>


---


### Object: `AddStatusToBasicAttack`


**Definition:** Contains status effects to add to the basic attack.  
**Total Count:** 248

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Items_and_Equipment.md#object-addpassivestominions), [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 45 | passives<br>class<br>tag |
| `Knockback` | Equation | The number of tiles the target is pushed away from the source on hit. | 10 | `1`<br>`10`<br>`2` |
| `Poison` | Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 7 | `1`<br>`10`<br>`2` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 5 | `Default`<br>`FormChange`<br>`Druid` | `Bleed` | Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 45 | Default<br>FormChange<br>Druid |
| `Burn` | Equation | The amount of Burn applied, either as a fixed number or a formula string. | 5 | `1`<br>`10`<br>`2` |
| [`Fear`](../Reference_and_Meta/Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 4 | `1`<br>`10`<br>`2` |
| `Slow` | Integer | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 4 | `-1`<br>`1`<br>`2` |
| [`Tangled`](../Reference_and_Meta/Arrays.md#array-tangled) | Array  | The number of stacks of the Tangled status effect applied, or an object defining its properties such as `stacks` and `alt_art`. | 4 | `1`<br>`2`<br>`[1, .05]` |
| [`ChangeTile`](../Reference_and_Meta/Enums.md#enum-changetile) | Enum  | Specifies the tile type to change to, or an object defining tile change parameters (tile type and area of effect). | 3 | `BlankTile`<br>`BrambleTile`<br>`CreepTile` |
| [`Conditional_GoodRoll`](./Items_and_Equipment.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 3 | `{ . . . }` |
| `DamageOrHealConditionally` | Integer | The amount of conditional damage or healing applied, based on certain conditions (e.g., ally or enemy). | 3 | `1` |
| [`Stun`](../Reference_and_Meta/Arrays.md#array-stun) | Array  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`2`<br>`3` |
| `Bruise` | Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 2 | `1`<br>`2`<br>`3` |
| `Confusion` | Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`10`<br>`2` |
| `Weakness` | Integer | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`2`<br>`3` |
| `Rot` | Integer | Integer, or an array [stacks, probability] specifying the amount of Rot stacks applied with the given probability. | 2 | `-999999`<br>`1`<br>`2` |
| `SpiderInfested` | Integer | The number of spider infestation stacks applied. | 2 | `1`<br>`2`<br>`4` |
| [`ApplyToSource`](./Items_and_Equipment.md#object-applytosource) | Object  | An object of effects that are applied to the source of the ability (the caster). | 1 | `{ . . . }` |
| [`Freeze`](../Reference_and_Meta/Arrays.md#array-freeze) | Array / Integer  | The amount of freeze stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`2`<br>`[1 .01]` |
| `Blind` | Integer | The amount of blind stacks applied, or an [stacks, probability] array. | 1 | `-1`<br>`1`<br>`2` |
| `Leech` | Integer | The amount of health leeched from the target (heals the attacker). | 1 | `1`<br>`2` |
| `Marked` | Integer | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`3`<br>`5` |
| `Leeches` | Integer | The number of stacks of the Leeches debuff applied, which deals damage over time and heals the applier. | 1 | `1`<br>`2`<br>`3` |
| [`KnockUpAndAway`](./Items_and_Equipment.md#object-knockupandaway) | Object  | Contains parameters for launching the target upward and away from the source, including stacks and distance. | 1 | `{ . . . }` |
| `MagicWeakness` | Integer | The amount of magic weakness stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`2`<br>`3` |
| `SoulLink` | Integer | The number of soul link stacks applied. | 1 | `1` |
| `OverrideChainKnockback` | Integer | The custom number of tiles for chain knockback, overriding the default. | 1 | `0`<br>`1`<br>`10` |
| `KnockOutCoin` | Integer | The number of coins knocked out, with an optional probability or an object with stacks and chance. | 1 | `1`<br>`[1 .5]` |
| `ManaLeeches` | Integer | The number of mana leech stacks applied. | 1 | `1`<br>`2` |
| `PullSourceToTarget` | Integer | The amount of tiles the source is pulled towards the target after the attack. | 1 | `1` |
| [`ForceUseAbilityOnTarget`](./Items_and_Equipment.md#object-forceuseabilityontarget) | Object | Defines a chance to force the unit to use a specified ability on the target. | 1 | `{ . . . }` |

</details>


---


### Object: `bonus_passives`


**Definition:** Grants temporary passive abilities to the caster for the duration of the ability.  
**Total Count:** 138

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`str_aux_is_copy_ability`](./Items_and_Equipment.md#object-str_aux_is_copy_ability)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| [`ModifyAbility`](./Items_and_Equipment.md#object-modifyability) | Object | Specifies the modifications to an ability's properties, such as cost or type. | 2 | `{ . . . }` |

</details>


---


### Object: `Else`


**Definition:** Contains the fallback effects to apply when a preceding conditional check fails.  
**Total Count:** 86

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_PartyMember`](./Items_and_Equipment.md#object-conditional_partymember)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 | `Default`<br>`FormChange`<br>`Druid` | [`ApplyToSource`](./Items_and_Equipment.md#object-applytosource) | Object | An object of effects that are applied to the source of the ability (the caster). | 14 | Default<br>FormChange<br>Druid |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>


---


### Object: `SpawnOnDeath`


**Definition:** Specifies an object and its faction to spawn when the unit dies.  
**Total Count:** 81

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`faction`](../Reference_and_Meta/Enums.md#enum-faction) | Enum | Specifies the faction of a spawned unit or projectile, determining its team allegiance and AI behavior. | 1 | `allies`<br>`auto`<br>`birds` |
| [`obj`](../Reference_and_Meta/Arrays.md#array-obj) | Array / Enum  | Specifies one or more object names to bounce towards the target. | 1 | `BeefyCharmedLeech`<br>`Dice`<br>`Maggot` |

</details>


---


### Object: `MeleeRevengeDamage`


**Definition:** Defines the damage and effects applied back to a melee attacker upon being hit.  
**Total Count:** 73

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 34 | `damage_instance`<br>`spell`<br>`self_damage` |
| [`effects`](./Items_and_Equipment.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 25 | `{ . . . }` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 14 | `{ . . . }` |
| `knockback` | Equation | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 9 | `"ceil(X*.25/5)"`<br>`-10`<br>`-2` |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 5 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |

</details>


---


### Object: `ApplyToSource`


**Definition:** An object of effects that are applied to the source of the ability (the caster).  
**Total Count:** 59

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Items_and_Equipment.md#object-addstatustobasicattack), [`Conditional_HasStatus`](./Items_and_Equipment.md#object-conditional_hasstatus), [`Else`](./Items_and_Equipment.md#object-else)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| `Charge` | Equation | The number of charge stacks applied. | 2 | `1`<br>`2`<br>`3` |
| `SpeedUp` | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 1 | `-1`<br>`-2`<br>`-4` |
| `StrengthUp` | Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 1 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| `HealthGain` | Integer | The amount of health restored to the source. | 1 | `1`<br>`10`<br>`2` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` | `AllStatsUp` | Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 14 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `Temporary`


**Definition:** Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions.  
**Total Count:** 57

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_BadRoll`](./Items_and_Equipment.md#object-conditional_badroll), [`StatusEachTurnBegin`](./Items_and_Equipment.md#object-statuseachturnbegin), [`StatusOnTookDamage`](./Items_and_Equipment.md#object-statusontookdamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 5 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`status`](../Reference_and_Meta/Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 5 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 5 | `{ . . . }` |
| [`turns`](../Reference_and_Meta/Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 4 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| `expires_on_end_turn` | Boolean | If true, the temporary effect expires at the end of the target's turn. | 4 | `true` |
| `expires_on_begin_turn` | Boolean | If true, the temporary effect expires at the start of the target's turn. | 1 | `true` |

</details>


---


### Object: `StatusEachTurnEnd`


**Definition:** Specifies status effects applied to the unit at the end of each of its turns.  
**Total Count:** 57

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 17 | passives<br>class<br>tag |
| [`ForceUseAbility`](../Reference_and_Meta/Enums.md#enum-forceuseability) | Enum  | The name of the ability the source is forced to use, optionally with a chance. | 6 | `CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| `Shield` | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 4 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`Conditional_GoodRoll`](./Items_and_Equipment.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 2 | `{ . . . }` |
| [`ImmediateUseAbility`](./Items_and_Equipment.md#object-immediateuseability) | Enum / Object  | Specifies the name of an ability to be triggered instantly from this effect. | 2 | `{ . . . }`<br>`FuzzerReact`<br>`HitlerCloneHeil`<br>`HitlerCloneTransform` |
| `SpawnCoinAnywhere` | Integer | The number of coins to spawn. If an array, the second value is the probability of spawning them anywhere. | 2 | `1`<br>`[1 .5]` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid` | `PartialCleanse` | Integer | The number of stacks of temporary status effects to remove from the target. | 7 | Default<br>FormChange<br>Druid |
| `Burn` | Equation | The amount of Burn applied, either as a fixed number or a formula string. | 1 | `1`<br>`10`<br>`2` |
| `ConstitutionUp` | Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 1 | `-1`<br>`-2`<br>`1` |
| [`Stealth`](../Reference_and_Meta/Arrays.md#array-stealth) | Array  | The number of stealth stacks applied. | 1 | `1`<br>`2`<br>`[1 .1]` |
| `AddWeaponAux` | Equation | The amount or expression to add to the source's weapon auxiliary stat. | 1 | `"-max(min(X+1, item_aux), 0)"`<br>`-item_aux`<br>`1` |
| `PreEmptiveCounterNextAttacks` | Integer | The number of next incoming attacks that the unit will counter preemptively before they land. | 1 | `1` |
| [`Conditional_ManaThreshold`](./Items_and_Equipment.md#object-conditional_manathreshold) | Object | Defines a conditional block that applies effects only if a unit's mana meets a specified threshold. | 1 | `{ . . . }` |

</details>


---


### Object: `SpawnOnBattleStart`


**Definition:** Specifies the object that spawns adjacent to the unit at the start of battle.  
**Total Count:** 54

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 22 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`number`](../Reference_and_Meta/Arrays.md#array-number) | Array / Integer | The number of objects to spawn; can be a single integer or an array `[min, max]` for a random range. | 16 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `StatusOnBattleEnd`


**Definition:** An object containing status effects or passives applied to the unit when the battle ends.  
**Total Count:** 53

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyPassives`](./Items_and_Equipment.md#object-applypassives), [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 30 | passives<br>class<br>tag |
| `even_if_dead` | Boolean | If true, the effect triggers even if the unit is dead. | 12 | `true` |
| `RandomPermanentStat` | Integer | The amount of a random permanent stat change (positive or negative). | 7 | `-1`<br>`-2`<br>`-3` |
| [`Conditional_GoodRoll`](./Items_and_Equipment.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 6 | `{ . . . }` |
| `RandomMutation` | Integer | The number of random mutations to apply. | 5 | `1`<br>`3` |
| [`FindItemFromPool`](../Reference_and_Meta/Enums.md#enum-finditemfrompool) | Enum  | Specifies the loot pool from which to find an item, with an optional chance. | 4 | `blackbird_pool`<br>`chapter`<br>`chapter_common` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid` | `PermanentIntelligence` | Integer | The permanent amount of intelligence added or removed. | 8 | Default<br>FormChange<br>Druid |
| [`GainCoins`](../Reference_and_Meta/Arrays.md#array-gaincoins) | Array / Integer  | The amount of coins gained, or a [min, max] range. | 2 | `-5`<br>`1`<br>`2` |
| `RepairTrinket` | Integer | The number of stacks of the Repair Trinket status effect to apply. | 2 | `1`<br>`99` |
| [`SetItemAux`](./Items_and_Equipment.md#object-setitemaux) | Object  | Configures an item's auxiliary value by specifying a target slot and a formula for the new value. | 2 | `{ . . . }` |
| `PermanentConstitution` | Integer | The amount of permanent Constitution stat added or removed. | 1 | `-1`<br>`-2`<br>`1` |
| [`Conditional_Corpse`](./Items_and_Equipment.md#object-conditional_corpse) | Object | Contains an inner effect block that only executes if the target is a corpse. | 1 | `{ . . . }` |
| [`RepairWeapon`](../Reference_and_Meta/Arrays.md#array-repairweapon) | Array / Integer  | The number of weapon durability points restored; an array [stacks, probability] applies a chance-based repair. | 1 | `1`<br>`6`<br>`99` |
| [`Conditional_Shielded`](./Items_and_Equipment.md#object-conditional_shielded) | Object | An object containing effects that are only applied if the target has a shield active. | 1 | `{ . . . }` |
| `RepairAll` | Integer | The amount of durability restored to all equipped items. | 1 | `1`<br>`10` |
| [`TransformWeapon`](./Items_and_Equipment.md#object-transformweapon) | Object  | An object with `from` and `to` fields specifying the weapon transformation. | 1 | `{ . . . }` |

</details>


---


### Object: `threshold`


**Definition:** The health threshold value, either as a formula using X (max health) or a fixed integer.  
**Total Count:** 49

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveAtStatThreshold`](./Items_and_Equipment.md#object-passiveatstatthreshold)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `int` | Integer | The Intelligence stat value or modifier. | 2 | `-1`<br>`-10`<br>`-2` |
| `con` | Integer | The Constitution stat value or modifier. | 1 | `-1`<br>`-2`<br>`-3` |

</details>


---


### Object: `Conditional_HasTag`


**Definition:** Evaluates whether the target has a specific tag; if true, applies the effects within; otherwise, runs the Else block.  
**Total Count:** 47

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToAllDamage`](./Items_and_Equipment.md#object-addstatustoalldamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid` | `BonusKnockbackDamage` | Integer || 43 | Default<br>FormChange<br>Druid |
| [`tag`](../Reference_and_Meta/Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 2 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| `OverrideChainKnockback` | Integer | The custom number of tiles for chain knockback, overriding the default. | 1 | `0`<br>`1`<br>`10` |

</details>


---


### Object: `StatusOnTookDamage`


**Definition:** Specifies status effects or actions triggered when the unit takes damage.  
**Total Count:** 46

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 12 | passives<br>class<br>tag |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 2 | `1`<br>`2`<br>`3` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid` | `Charge` | Integer | The number of charge stacks applied. | 13 | Default<br>FormChange<br>Druid |
| `Bleed` | Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`10`<br>`2` |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 1 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `StrengthUp` | Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 1 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| [`Temporary`](./Items_and_Equipment.md#object-temporary) | Object  | Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions. | 1 | `{ . . . }` |
| [`DivineShield`](../Reference_and_Meta/Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | `1`<br>`2`<br>`4` |
| `DodgeChance_Status` | Integer | The flat percentage increase to dodge chance applied as a status effect. | 1 | `1`<br>`10`<br>`100` |
| [`Conditional_HasStatus`](./Items_and_Equipment.md#object-conditional_hasstatus) | Object | Contains an inner effect block that only executes if the target has the specified status effect. | 1 | `{ . . . }` |
| [`RemoveStatus`](../Reference_and_Meta/Enums.md#enum-removestatus) | Enum  | The name of the status effect to remove from the source. | 1 | `AlphaCat`<br>`Brace`<br>`DodgeChance_Status` |
| [`Conditional_HealthThreshold`](./Items_and_Equipment.md#object-conditional_healththreshold) | Object  | Contains an inner effect block that only executes if the target's health is below a threshold, defined by `threshold_flat`, `threshold_percent`, or `threshold_expr`. | 1 | `{ . . . }` |

</details>


---


### Object: `Conditional_Enemy`


**Definition:** An object containing status effects or actions applied only if the target is an enemy.  
**Total Count:** 44

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToSpells`](./Items_and_Equipment.md#object-addstatustospells)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` | `Leeches` | Integer | The number of stacks of the Leeches debuff applied, which deals damage over time and heals the applier. | 8 | Default<br>FormChange<br>Druid |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>


---


### Object: `StatusOnKill`


**Definition:** Specifies status effects or actions triggered when the unit kills an enemy.  
**Total Count:** 40

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 12 | passives<br>class<br>tag |
| [`Conditional_GoodRoll`](./Items_and_Equipment.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 4 | `{ . . . }` |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 1 | `1`<br>`2`<br>`3` |
| `SpeedUp` | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 1 | `-1`<br>`-2`<br>`-4` |
| `StrengthUp` | Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 1 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| `LuckUp` | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 1 | `-1`<br>`-2`<br>`-4` |
| `ConstitutionUp` | Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 1 | `-1`<br>`-2`<br>`1` |
| `IntelligenceUp` | Array / Equation | The amount of Intelligence added as a flat bonus. | 1 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| `DexterityUp` | Array / Equation | The amount of dexterity change, or a keyword like 'item_aux'. | 1 | `-1`<br>`1`<br>`2` |
| `CharismaUp` | Integer | The amount of charisma change, or a keyword like 'item_aux'. | 1 | `-1`<br>`-2`<br>`1` |
| [`EquipPermanentItem`](../Reference_and_Meta/Enums.md#enum-equippermanentitem) | Enum  | The name of the item to permanently equip to the source. | 1 | `BoneClub`<br>`Kidney` |
| `BrittleCharismaUp` | Integer | The number of stacks of temporary Charisma gained on kill. | 1 | `2` |
| `BrittleConstitutionUp` | Integer | The number of stacks of temporary Constitution gained on kill. | 1 | `2` |
| `BrittleDexterityUp` | Integer | The number of stacks of temporary Dexterity gained on kill. | 1 | `2` |
| `BrittleIntelligenceUp` | Integer | The number of stacks of temporary Intelligence gained on kill. | 1 | `2` |
| `BrittleLuckUp` | Integer | The number of stacks of temporary Luck gained on kill. | 1 | `2` |
| `BrittleSpeedUp` | Integer | The number of stacks of temporary Speed gained on kill. | 1 | `2` |
| `BrittleStrengthUp` | Integer | The number of stacks of temporary Strength gained on kill. | 1 | `2` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` | `HealthGain` | Integer | The amount of health restored to the source. | 8 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `CounterAttack`


**Definition:** Specifies the ability used when the unit counterattacks after being hit.  
**Total Count:** 39

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 3 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `ranged_only` | Boolean | If true, the reaction only triggers on ranged attacks. | 1 | `true` |
| `melee_only` | Boolean | If true, the counterattack or block effect only triggers in response to melee attacks. | 1 | `true` |

</details>


---


### Object: `SpawnThingOnDamage`


**Definition:** Specifies an object that spawns on the tile when the unit takes damage.  
**Total Count:** 38

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 13 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 4 | `false`<br>`true` |
| `spawn_on_death_hit` | Boolean | If true, spawning only occurs when the damage is lethal. | 2 | `false` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |
| [`number`](../Reference_and_Meta/Arrays.md#array-number) | Array / Integer | The number of objects to spawn; can be a single integer or an array `[min, max]` for a random range. | 1 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `Conditional_GoodRoll`


**Definition:** Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability.  
**Total Count:** 37

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Items_and_Equipment.md#object-addstatustobasicattack), [`StatusEachTurnEnd`](./Items_and_Equipment.md#object-statuseachturnend), [`StatusOnBattleEnd`](./Items_and_Equipment.md#object-statusonbattleend), [`StatusOnKill`](./Items_and_Equipment.md#object-statusonkill), [`StatusOnTakeHealthOrShieldDamage`](./Items_and_Equipment.md#object-statusontakehealthorshielddamage), [`effects`](./Items_and_Equipment.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 19 | Default<br>FormChange<br>Druid |
| `odds` | Float | The probability of the effect occurring, expressed as a decimal or percentage. | 19 | `.1`<br>`.16666666`<br>`.3` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 9 | passives<br>class<br>tag |
| [`Freeze`](../Reference_and_Meta/Arrays.md#array-freeze) | Array / Integer  | The amount of freeze stacks applied, or an [stacks, probability] array. | 6 | `1`<br>`2`<br>`[1 .01]` |
| `ForceUseAbility_NonStack` | `String` | Forces the unit to use a specific non-stackable ability when the conditional roll is successful. | 4 | `Endeavor_Auto`<br>`Indigestion_Fart`<br>`Indigestion_Fart2` |
| [`FindItemFromPool`](../Reference_and_Meta/Enums.md#enum-finditemfrompool) | Enum  | Specifies the loot pool from which to find an item, with an optional chance. | 3 | `blackbird_pool`<br>`chapter`<br>`chapter_common` |
| [`ForceUseAbility`](../Reference_and_Meta/Enums.md#enum-forceuseability) | Enum  | The name of the ability the source is forced to use, optionally with a chance. | 3 | `CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| `RandomMutation` | Integer | The number of random mutations to apply. | 3 | `1`<br>`3` |
| `DestroyTrinket` | `Number` | The number of trinkets destroyed. | 1 | `1` |

</details>


---


### Object: `Conditional_Ally`


**Definition:** Defines effects that apply only if the target is an ally, with an optional else block for non-allies.  
**Total Count:** 37

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Adjacent`](./Items_and_Equipment.md#object-conditional_adjacent)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` | `ManaGain` | Integer | The amount of mana restored to the source, which can be an expression. | 4 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `AddPassivesToMinions`


**Definition:** An object containing passives that are granted to all minions spawned by the unit.  
**Total Count:** 36

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 6 | passives<br>class<br>tag |
| `HealthGain` | Integer | The amount of health restored to the source. | 5 | `1`<br>`10`<br>`2` |
| `AddMaxHealth` | Integer | The amount added to the unit's maximum health. Negative values reduce max health. | 4 | `-25`<br>`10`<br>`2` |
| [`AddStatusToBasicAttack`](./Items_and_Equipment.md#object-addstatustobasicattack) | Object  | Contains status effects to add to the basic attack. | 1 | `{ . . . }` |
| `Shield` | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 1 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` | `AllStatsUp` | Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `RandomStatusFromPool`


**Definition:** A collection of status effects; one is randomly chosen and applied to the target.  
**Total Count:** 35

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnDie`](./Items_and_Equipment.md#object-statusondie)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| `PermanentConstitution` | Integer | The amount of permanent Constitution stat added or removed. | 1 | `-1`<br>`-2`<br>`1` |
| `PermanentIntelligence` | Integer | The permanent amount of intelligence added or removed. | 1 | `-1`<br>`1`<br>`2` |
| `PermanentDexterity` | Integer | The permanent amount of dexterity added or removed. | 1 | `1`<br>`2` |
| `PermanentSpeed` | Integer | The permanent amount of speed added or removed. | 1 | `-1`<br>`1`<br>`2` |
| `PermanentStrength` | Integer | The amount of permanent bonus strength (physical damage modifier) granted. | 1 | `1`<br>`2` |
| `PermanentLuck` | Integer | The amount of permanent Luck added to the unit's base stats. | 1 | `1`<br>`2` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` | `PermanentCharisma` | Integer | The amount of permanent Charisma added to the unit's base stats. | 24 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `keyword_tooltips`


**Definition:** Associates keyword tooltips with the ability, often used for status effects.  
**Total Count:** 35

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| [`DivineShield`](../Reference_and_Meta/Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | `1`<br>`2`<br>`4` |
| `Immobile` | Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 1 | `0`<br>`1`<br>`10%` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `SpawnExtraThingsOnBattleStart`


**Definition:** An object with `object` and `number` (or range) defining what and how many objects to spawn at battle start.  
**Total Count:** 32

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 3 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`number`](../Reference_and_Meta/Arrays.md#array-number) | Array / Integer | The number of objects to spawn; can be a single integer or an array `[min, max]` for a random range. | 3 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `RevengeDamage`


**Definition:** An object defining the damage and effects that trigger when the unit is attacked.  
**Total Count:** 31

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 9 | `damage_instance`<br>`spell`<br>`self_damage` |
| [`effects`](./Items_and_Equipment.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 9 | `{ . . . }` |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 3 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`elements`](../Reference_and_Meta/Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 2 | `[`<br>`[Heat Fire]` |

</details>


---


### Object: `ObjectOnHitCharacter`


**Definition:** Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit.  
**Total Count:** 31

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEveryXSpellCasts`](./Items_and_Equipment.md#object-statuseveryxspellcasts), [`StatusOnBattleStart`](./Items_and_Equipment.md#object-statusonbattlestart)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | passives<br>class<br>tag |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 2 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| `stacks` | Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |

</details>


---


### Object: `StatusEachTurnBegin`


**Definition:** Specifies status effects applied to the unit at the start of each of its turns.  
**Total Count:** 27

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveWhenDead`](./Items_and_Equipment.md#object-passivewhendead), [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 6 | passives<br>class<br>tag |
| [`Conditional_BadRoll`](./Items_and_Equipment.md#object-conditional_badroll) | Object  | An object containing an `odds` value and effects that are applied when a random roll succeeds. | 2 | `{ . . . }` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid` | `SpeedUp` | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 10 | Default<br>FormChange<br>Druid |
| `Burn` | Equation | The amount of Burn applied, either as a fixed number or a formula string. | 1 | `1`<br>`10`<br>`2` |
| [`Temporary`](./Items_and_Equipment.md#object-temporary) | Object  | Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions. | 1 | `{ . . . }` |
| `Revive` | Integer | Revives a dead target with the specified percentage of health (e.g., "50%", "100%") or a fixed number. | 1 | `1`<br>`100%`<br>`50%` |
| [`UseAbility`](../Reference_and_Meta/Enums.md#enum-useability) | Enum  | The name of the ability the target is forced to use. | 1 | `GirlDinoPoop`<br>`KirbySpit`<br>`MD_PoopChain` |
| `DestroyTrinket` | Integer | The number of trinkets destroyed. | 1 | `1` |
| `DoubleCastSpellThisTurn` | Integer | If non-zero, grants the unit a double cast effect for spells this turn. | 1 | `1` |
| `DrinkWater` | Integer | The number of water-drink actions performed. | 1 | `1` |
| `BlessingOfPeace` | Integer | The number of stacks of the Blessing of Peace status applied to the unit each turn. | 1 | `1` |
| `Wet` | Integer | The number of stacks of the Wet status effect applied. | 1 | `1` |
| [`ManaGainRange`](./Items_and_Equipment.md#object-managainrange) | Object | Defines the minimum and maximum mana gained per turn. | 1 | `{ . . . }` |

</details>


---


### Object: `KnockUpAndAway`


**Definition:** Contains parameters for launching the target upward and away from the source, including stacks and distance.  
**Total Count:** 25

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Items_and_Equipment.md#object-addstatustobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `distance` | Integer | The number of tiles the target is knocked back or pulled. | 1 | `-3`<br>`10`<br>`2` |

</details>


---


### Object: `StatusOnBreak`


**Definition:** An object defining statuses or effects applied when an item or object breaks.  
**Total Count:** 22

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 16 | passives<br>class<br>tag |
| [`GainCoinsRange`](./Items_and_Equipment.md#object-gaincoinsrange) | Object  | An object with `min` and `max` fields specifying a range for the amount of coins gained. | 5 | `{ . . . }` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 4 | `Default`<br>`FormChange`<br>`Druid` | `Bruise` | Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 4 | Default<br>FormChange<br>Druid |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 3 | `1`<br>`2`<br>`3` |
| `HealthGain` | Integer | The amount of health restored to the source. | 3 | `1`<br>`10`<br>`2` |
| [`FindItemFromPool`](../Reference_and_Meta/Enums.md#enum-finditemfrompool) | Enum  | Specifies the loot pool from which to find an item, with an optional chance. | 3 | `blackbird_pool`<br>`chapter`<br>`chapter_common` |
| `PermanentConstitution` | Integer | The amount of permanent Constitution stat added or removed. | 3 | `-1`<br>`-2`<br>`1` |
| [`ChangeTilesUnder`](../Reference_and_Meta/Enums.md#enum-changetilesunder) | Enum  | The tile type to change the ground tiles under the target to. | 3 | `DirtTile`<br>`GlassTile`<br>`LavaTile` |
| `StrengthUp` | Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 1 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| `ConstitutionUp` | Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 1 | `-1`<br>`-2`<br>`1` |
| `IntelligenceUp` | Array / Equation | The amount of Intelligence added as a flat bonus. | 1 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| [`ObjectOnHitCharacter`](./Items_and_Equipment.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 1 | `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| `DexterityUp` | Array / Equation | The amount of dexterity change, or a keyword like 'item_aux'. | 1 | `-1`<br>`1`<br>`2` |
| [`ApplyToRandomPartyMemberIfPossible`](./Items_and_Equipment.md#object-applytorandompartymemberifpossible) | Object  | Contains an inner effect block that is applied to a random living party member if one exists. | 1 | `{ . . . }` |
| [`FindItem`](../Reference_and_Meta/Enums.md#enum-finditem) | Enum  | The name of the specific item to find and add to the source's inventory. | 1 | `BoneClub`<br>`Molars`<br>`Pearl` |
| [`GainDisorder`](../Reference_and_Meta/Enums.md#enum-gaindisorder) | Enum | Specifies the name of the disorder gained. | 1 | `Chungus`<br>`Psychosis` |

</details>


---


### Object: `SpawnEachTurn`


**Definition:** Specifies an object that spawns on a random adjacent tile each turn, with optional chance.  
**Total Count:** 22

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum | Specifies the object or unit to be spawned. | 12 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 11 | `.02`<br>`.1`<br>`.15` |
| [`stack_key`](../Reference_and_Meta/Enums.md#enum-stack_key) | Enum | Specifies the key of the status stack to check for the condition. | 5 | `CATHIDE`<br>`EMPTY_GENERATOR`<br>`FANNY_PACK` |

</details>


---


### Object: `Conditional_Boss`


**Definition:** Contains effects that apply only if the target is a boss enemy.  
**Total Count:** 21

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusAllCharactersOnSpawn`](./Items_and_Equipment.md#object-statusallcharactersonspawn)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` | `AllStatsUp` | Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 14 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `Craft`


**Definition:** Specifies the loot pool and slot to craft an item for the source.  
**Total Count:** 20

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusIfUnusedActPoints`](./Items_and_Equipment.md#object-statusifunusedactpoints), [`StatusOnBattleStart`](./Items_and_Equipment.md#object-statusonbattlestart)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`pool`](../Reference_and_Meta/Arrays.md#array-pool) | Array / Enum  | Specifies the name of the pool from which an ability is learned or an item is crafted. | 4 | `2`<br>`3`<br>`4` |
| `slot` | Integer | Specifies the equipment slot (e.g., 'head', 'trinket', 'random_empty') where the crafted item is placed. | 4 | `0`<br>`1`<br>`2` |
| `works_with_tech` | Boolean | If true, the craft effect is compatible with tech-based interactions or abilities. | 3 | `true` |

</details>


---


### Object: `Conditional_HasStatus`


**Definition:** Contains an inner effect block that only executes if the target has the specified status effect.  
**Total Count:** 20

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToAllDamage`](./Items_and_Equipment.md#object-addstatustoalldamage), [`StatusOnTookDamage`](./Items_and_Equipment.md#object-statusontookdamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 4 | passives<br>class<br>tag |
| [`status`](../Reference_and_Meta/Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 4 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 3 | Default<br>FormChange<br>Druid |
| [`ApplyToSource`](./Items_and_Equipment.md#object-applytosource) | Object  | An object of effects that are applied to the source of the ability (the caster). | 2 | `{ . . . }` |
| [`RemoveStatusStacks`](./Items_and_Equipment.md#object-removestatusstacks) | Object  | An object specifying a status name and the number of stacks to remove from the target. | 1 | `{ . . . }` |
| `FlatLeechIfDamaged` | `Number` | The flat amount of health leeched when the unit takes damage. | 1 | `3`<br>`5` |
| [`ImmediateUseAbility_Instant`](../Reference_and_Meta/Enums.md#enum-immediateuseability_instant) | Enum | Specifies the name of an ability to use instantly as a passive effect. | 1 | `head_CrownOfHorns` |

</details>


---


### Object: `PassiveWhenAffectedByElement`


**Definition:** An object containing `element` and `passives` that grants the listed passives while the unit is affected by the specified element.  
**Total Count:** 18

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| [`passives`](./Items_and_Equipment.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`element`](../Reference_and_Meta/Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 1 | `Electric`<br>`Fire`<br>`Gravity` |

</details>


---


### Object: `StatusOnBattleStart`


**Definition:** An object containing status effects to apply to the unit at the start of every battle.  
**Total Count:** 16

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 6 | passives<br>class<br>tag |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 4 | `Default`<br>`FormChange`<br>`Druid` | [`Craft`](./Items_and_Equipment.md#object-craft) | Object | Specifies the loot pool and slot to craft an item for the source. | 3 | Default<br>FormChange<br>Druid |
| `SafeDie` | Integer | The number of times the unit can survive a fatal hit. | 2 | `1` |
| `Brace` | Array / Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 1 | `1`<br>`10`<br>`2` |
| [`FindItemFromPool`](../Reference_and_Meta/Enums.md#enum-finditemfrompool) | Enum  | Specifies the loot pool from which to find an item, with an optional chance. | 1 | `blackbird_pool`<br>`chapter`<br>`chapter_common` |
| `RandomMagicMissile` | Integer | The number of random magic missiles fired, or an object defining its properties. | 1 | `1`<br>`10`<br>`2` |
| [`ForceUseAbility`](../Reference_and_Meta/Enums.md#enum-forceuseability) | Enum  | The name of the ability the source is forced to use, optionally with a chance. | 1 | `CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| [`ObjectOnHitCharacter`](./Items_and_Equipment.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 1 | `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| `SetHealth` | Integer | Sets the target's health to a specific flat value or percentage. | 1 | `1`<br>`100%`<br>`50%` |
| [`DestroyEquipmentAndAttachParasite`](./Items_and_Equipment.md#object-destroyequipmentandattachparasite) | Object  | Attempts to destroy a random piece of the target's equipment and attach a parasite from the specified pool. | 1 | `{ . . . }` |
| [`ReviveNextRound`](./Items_and_Equipment.md#object-revivenextround) | Object  | The number of revives granted, or an object defining revive properties. | 1 | `{ . . . }` |
| `StealthUntilBasicAttack` | Integer | The number of stacks of Stealth that are removed when the unit performs a basic attack. | 1 | `1` |

</details>


---


### Object: `BackflipWhenTargeted`


**Definition:** The number of backflip charges, or an object defining its ability.  
**Total Count:** 15

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |

</details>


---


### Object: `PassiveAtStatThreshold`


**Definition:** An object defining passives granted when a unit's stat meets a specified threshold.  
**Total Count:** 13

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |
| [`passives`](./Items_and_Equipment.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 3 | `{ . . . }` |
| `threshold` | Equation / Object | The health threshold value, either as a formula using X (max health) or a fixed integer. | 3 | `{ . . . }`<br>`"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |
| [`mode`](../Reference_and_Meta/Enums.md#enum-mode) | Enum | Specifies the comparison mode (equal, greater, less_or_equal, etc.) used for a conditional check. | 3 | `equal`<br>`greater`<br>`greater_or_equal` |

</details>


---


### Object: `ApplyPassives`


**Definition:** Specifies the passives or status effects to apply to the unit.  
**Total Count:** 13

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_RandomChance`](./Items_and_Equipment.md#object-conditional_randomchance)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| [`StatusOnBattleEnd`](./Items_and_Equipment.md#object-statusonbattleend) | Object  | An object containing status effects or passives applied to the unit when the battle ends. | 1 | `{ . . . }` |

</details>


---


### Object: `AddStatusToAllDamage`


**Definition:** Adds the contained status effects to all damage dealt by the unit.  
**Total Count:** 13

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 5 | passives<br>class<br>tag |
| [`Conditional_HasStatus`](./Items_and_Equipment.md#object-conditional_hasstatus) | Object | Contains an inner effect block that only executes if the target has the specified status effect. | 3 | `{ . . . }` |
| `must_do_damage` | Boolean | If true, the status or effect will only be applied if the attack or ability actually deals damage. | 3 | `true` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid` | [`KnockbackIfCrit`](./Items_and_Equipment.md#object-knockbackifcrit) | Object || 3 | Default<br>FormChange<br>Druid |
| [`Conditional_HasTag`](./Items_and_Equipment.md#object-conditional_hastag) | Object  | Evaluates whether the target has a specific tag; if true, applies the effects within; otherwise, runs the Else block. | 2 | `{ . . . }` |
| `Rot` | Integer | Integer, or an array [stacks, probability] specifying the amount of Rot stacks applied with the given probability. | 1 | `-999999`<br>`1`<br>`2` |

</details>


---


### Object: `AbilityHealthThreshold`


**Definition:** Defines an ability and conditions for its activation when the unit's health reaches a threshold.  
**Total Count:** 13

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `immediate` | Boolean | If true, the action (e.g., attack) occurs instantly without waiting for the unit's turn in the initiative order. | 1 | `false`<br>`true` |
| `threshold` | Equation / Object | The health threshold value, either as a formula using X (max health) or a fixed integer. | 1 | `{ . . . }`<br>`"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |
| `aux` | Integer | An auxiliary integer value used for item properties, such as hunger value. | 1 | `-1`<br>`1`<br>`10` |
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 1 | `true` |

</details>


---


### Object: `CritsApplyStatus`


**Definition:** An object containing statuses applied to the target when the unit lands a critical hit.  
**Total Count:** 12

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| [`Fear`](../Reference_and_Meta/Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `StatusOnKillEnemy`


**Definition:** Specifies the effects applied when the unit kills an enemy.  
**Total Count:** 11

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 7 | passives<br>class<br>tag |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 4 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `Brace` | Array / Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 1 | `1`<br>`10`<br>`2` |
| `LuckUp` | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 1 | `-1`<br>`-2`<br>`-4` |
| `ManaGain` | Equation | The amount of mana restored to the source, which can be an expression. | 1 | `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`ForceUseAbility`](../Reference_and_Meta/Enums.md#enum-forceuseability) | Enum  | The name of the ability the source is forced to use, optionally with a chance. | 1 | `CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `SpawnOnBattleStartRandomEmptyTile`


**Definition:** Specifies an object that spawns on a random empty tile at the start of battle.  
**Total Count:** 11

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 5 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`number`](../Reference_and_Meta/Arrays.md#array-number) | Array / Integer | The number of objects to spawn; can be a single integer or an array `[min, max]` for a random range. | 5 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `MovementReaction`


**Definition:** Specifies an ability to cast when a unit moves within range, with options for targeting and conditions.  
**Total Count:** 11

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveWhileHasDurability`](./Items_and_Equipment.md#object-passivewhilehasdurability), [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `enemies_only` | Boolean | If true, the arc lightning effect only chains to enemy units, ignoring allies. | 2 | `false`<br>`true` |
| `create_temp_ability` | Boolean | If true, a temporary ability slot is created during movement reactions. | 2 | `true` |
| `on_self_move_too` | Boolean | If true, the reaction triggers when the unit themselves move. | 1 | `true` |

</details>


---


### Object: `ImmediateUseAbility`


**Definition:** Specifies the name of an ability to be triggered instantly from this effect.  
**Total Count:** 11

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnEnd`](./Items_and_Equipment.md#object-statuseachturnend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 1 | `true` |

</details>


---


### Object: `GainCoinsRange`


**Definition:** An object with `min` and `max` fields specifying a range for the amount of coins gained.  
**Total Count:** 11

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBreak`](./Items_and_Equipment.md#object-statusonbreak), [`StatusOnDie`](./Items_and_Equipment.md#object-statusondie)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max` | Integer | The maximum amount of coins that can be gained. | 7 | `10`<br>`2`<br>`25` |
| `min` | Integer | The minimum amount of coins that will be gained. | 7 | `0`<br>`1`<br>`10` |

</details>


---


### Object: `Conditional_Corpse`


**Definition:** Contains an inner effect block that only executes if the target is a corpse.  
**Total Count:** 11

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Items_and_Equipment.md#object-statusonbattleend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| `RandomMutation` | Integer | The number of random mutations to apply. | 1 | `1`<br>`3` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `AddSelfStatusToBasicAttack`


**Definition:** Applies the contained status effects to the unit when it uses its basic attack.  
**Total Count:** 11

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 7 | passives<br>class<br>tag |
| `RandomMagicMissile` | Integer | The number of random magic missiles fired, or an object defining its properties. | 4 | `1`<br>`10`<br>`2` |
| `Bleed` | Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`10`<br>`2` |
| `Shield` | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 1 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`Quivered`](../Reference_and_Meta/Arrays.md#array-quivered) | Array / Integer  | The amount of quivered stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`2`<br>`5` |
| [`ForceUseAbility`](../Reference_and_Meta/Enums.md#enum-forceuseability) | Enum  | The name of the ability the source is forced to use, optionally with a chance. | 1 | `CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusOnEndMove`


**Definition:** Specifies status effects or actions triggered when the unit finishes moving.  
**Total Count:** 10

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 4 | `{ . . . }` |

</details>


---


### Object: `StatusAlliesOnBattleStart`


**Definition:** An object containing status effects to apply to all allies at the start of battle.  
**Total Count:** 10

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |
| `SpeedUp` | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 2 | `-1`<br>`-2`<br>`-4` |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 1 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `StrengthUp` | Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 1 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| `ConstitutionUp` | Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 1 | `-1`<br>`-2`<br>`1` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` | `Brace` | Enum / Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 2 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `AutocastEachRound`


**Definition:** Contains an ability name and optional 'even_if_stunned' flag to autocast each round.  
**Total Count:** 10

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveWhenDead`](./Items_and_Equipment.md#object-passivewhendead)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 2 | `true` |

</details>


---


### Object: `StatusOnDie`


**Definition:** Specifies status effects or actions triggered when the unit dies.  
**Total Count:** 9

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 6 | passives<br>class<br>tag |
| [`FindItemFromPool`](../Reference_and_Meta/Enums.md#enum-finditemfrompool) | Enum  | Specifies the loot pool from which to find an item, with an optional chance. | 1 | `blackbird_pool`<br>`chapter`<br>`chapter_common` |
| `RandomMagicMissile` | Integer | The number of random magic missiles fired, or an object defining its properties. | 1 | `1`<br>`10`<br>`2` |
| [`RandomStatusFromPool`](./Items_and_Equipment.md#object-randomstatusfrompool) | Object  | A collection of status effects; one is randomly chosen and applied to the target. | 1 | `{ . . . }` |
| [`GainCoinsRange`](./Items_and_Equipment.md#object-gaincoinsrange) | Object  | An object with `min` and `max` fields specifying a range for the amount of coins gained. | 1 | `{ . . . }` |
| [`CreateGlobalModifiers`](./Items_and_Equipment.md#object-createglobalmodifiers) | Object  | Defines global gameplay modifiers to activate. | 1 | `{ . . . }` |
| [`Conditional_RandomChance`](./Items_and_Equipment.md#object-conditional_randomchance) | Object | An object containing effects that execute only if a random roll succeeds, with an odds value defined inside. | 1 | `{ . . . }` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `PassiveAtHealthThreshold`


**Definition:** An object that grants additional passives when the unit's health meets a specified threshold, with sub-keys for threshold, mode, and passives.  
**Total Count:** 9

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 5 | passives<br>class<br>tag |
| [`passives`](./Items_and_Equipment.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 5 | `{ . . . }` |
| `threshold` | Equation / Object | The health threshold value, either as a formula using X (max health) or a fixed integer. | 5 | `{ . . . }`<br>`"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |
| [`mode`](../Reference_and_Meta/Enums.md#enum-mode) | Enum | Specifies the comparison mode (equal, greater, less_or_equal, etc.) used for a conditional check. | 5 | `equal`<br>`greater`<br>`greater_or_equal` |

</details>


---


### Object: `passive`


**Definition:** Defines the passive form, where the unit does nothing (uses DoNothing attack) and is inactive.  
**Total Count:** 9

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Metal` | Integer | The number of armor stacks or metal keyword effects. | 2 | `1` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |

</details>


---


### Object: `ChanceToRevive`


**Definition:** The percentage chance or an object defining chance, health, and statuses on revival.  
**Total Count:** 9

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `health` | Integer | The maximum hit points of the unit. | 2 | `0`<br>`1`<br>`10` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |

</details>


---


### Object: `BoostWeaponDamage`


**Definition:** The amount of bonus weapon damage applied, or an object with `damage` and `crit_chance` fields.  
**Total Count:** 9

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 2 | `damage_instance`<br>`spell`<br>`self_damage` |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 2 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| `crit_chance` | Float | The chance for the damage instance to critically hit, expressed as a percentage or equation; values above 1 default to 100%. | 2 | `-999999`<br>`.05*X`<br>`.25` |

</details>


---


### Object: `AddDamageToElementDamage`


**Definition:** Defines additional damage of a specific element added to the unit's attacks.  
**Total Count:** 9

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 4 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`element`](../Reference_and_Meta/Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 4 | `Electric`<br>`Fire`<br>`Gravity` |

</details>


---


### Object: `StatusOnCastSpell`


**Definition:** An object listing status effects applied to the unit whenever it casts a spell.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| `Shield` | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 1 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `Charge` | Equation | The number of charge stacks applied. | 1 | `1`<br>`2`<br>`3` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusIfUnusedMovePoints`


**Definition:** Specifies status effects applied if the unit ends its turn with unused movement points.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |
| `HealthGain` | Integer | The amount of health restored to the source. | 2 | `1`<br>`10`<br>`2` |
| `Charge` | Equation | The number of charge stacks applied. | 2 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `StatusEveryXSpellCasts`


**Definition:** An object with `stacks` (number of spell casts) and status effects to apply after that many spell casts.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 3 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `IntelligenceUp` | Array / Equation | The amount of Intelligence added as a flat bonus. | 1 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| [`ObjectOnHitCharacter`](./Items_and_Equipment.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 1 | `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` | `Charge` | Integer | The number of charge stacks applied. | 3 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `StatusAlliesOnDeath`


**Definition:** Applies the contained status effects to all allies when the unit dies.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| [`DivineShield`](../Reference_and_Meta/Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | `1`<br>`2`<br>`4` |

</details>


---


### Object: `Conditional_BadRoll`


**Definition:** An object containing an `odds` value and effects that are applied when a random roll succeeds.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnBegin`](./Items_and_Equipment.md#object-statuseachturnbegin)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid` | [`Temporary`](./Items_and_Equipment.md#object-temporary) | Object | Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions. | 8 | Default<br>FormChange<br>Druid |
| `odds` | Float | The probability of the effect occurring, expressed as a decimal or percentage. | 2 | `.1`<br>`.16666666`<br>`.3` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>


---


### Object: `CatchProjectiles`


**Definition:** An object defining chance to catch projectiles and optionally apply statuses.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 3 | `.02`<br>`.1`<br>`.15` |
| [`Quivered`](../Reference_and_Meta/Arrays.md#array-quivered) | Array / Integer  | The amount of quivered stacks applied, or an [stacks, probability] array. | 3 | `1`<br>`2`<br>`5` |
| `ally_chance` | Integer | The percentage chance for an ally to catch incoming projectiles. | 3 | `100%`<br>`15%` |

</details>


---


### Object: `AddStatusToWeapons`


**Definition:** Specifies status effects to add to the unit's weapon attacks, with their stack counts.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` | `Leech` | Integer | The amount of health leeched from the target (heals the attacker). | 3 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `StatusRandomEnemiesOnBattleStart`


**Definition:** An object that applies a status effect to a random number of enemies at the start of battle, with sub-keys for count and the status.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 4 | passives<br>class<br>tag |
| [`count`](../Reference_and_Meta/Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 4 | `0`<br>`1`<br>`10` |
| [`Fear`](../Reference_and_Meta/Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`10`<br>`2` |
| `Confusion` | Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`10`<br>`2` |
| [`Freeze`](../Reference_and_Meta/Arrays.md#array-freeze) | Array / Integer  | The amount of freeze stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`2`<br>`[1 .01]` |
| `Charmed` | Integer | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 1 | `1`<br>`2`<br>`3` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `PassiveWhenOnTile`


**Definition:** Grants the contained passive effects while the unit is standing on one of the specified tile types.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](./Items_and_Equipment.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 7 | `{ . . . }` |
| [`tile`](../Reference_and_Meta/Arrays.md#array-tile) | Array / Enum | Specifies the tile type(s) to change to, either a single tile string or an array of tiles. | 7 | `BrambleTile`<br>`CreepTile`<br>`DirtTile` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 7 | passives<br>class<br>tag |

</details>


---


### Object: `PassiveIfStrAuxEquals`


**Definition:** Grants the contained passive effects when the unit's specified auxiliary stat equals the given value.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](./Items_and_Equipment.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 7 | `{ . . . }` |
| `value` | Float | The numeric value or formula associated with the buff. | 7 | `.5`<br>`0`<br>`1` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 7 | passives<br>class<br>tag |

</details>


---


### Object: `DurabilityTransform`


**Definition:** Transforms the item into another when durability reaches specified thresholds.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`eq`](../Reference_and_Meta/Arrays.md#array-eq) | Array | An array specifying a [durability, item] pair to transform to when durability equals a specific value. | 11 | `[0 EstusFlask_Empty]`<br>`[0 JarOfNothing]`<br>`[0 WaterBottle_Empty]` |
| [`ge`](../Reference_and_Meta/Arrays.md#array-ge) | Array | An array specifying a [durability, item] pair to transform to when durability is greater than or equal to a specific value. | 4 | `[10 NuclearKnife_Glowing]`<br>`[2 WaterBottle_Full]`<br>`[20 BlackShard_Glowing]` |

</details>


---


### Object: `DoDamage`


**Definition:** Contains damage parameters (amount, type, tile targets) to deal damage to the target.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachRoundEnd`](./Items_and_Equipment.md#object-statuseachroundend), [`StatusOnBreakItem`](./Items_and_Equipment.md#object-statusonbreakitem)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | passives<br>class<br>tag |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 2 | `damage_instance`<br>`spell`<br>`self_damage` |
| [`effects`](./Items_and_Equipment.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 2 | `{ . . . }` |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 2 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 2 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`damage_tiles`](../Reference_and_Meta/Enums.md#enum-damage_tiles) | Enum | Specifies whether the damage effect applies to tiles; 'all' damages every tile in the area. | 2 | `all` |

</details>


---


### Object: `Conditional_PlayerCat`


**Definition:** Defines effects that only apply if the target is a player-controlled cat.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Adjacent`](./Items_and_Equipment.md#object-conditional_adjacent)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| `Charge` | Equation | The number of charge stacks applied. | 1 | `1`<br>`2`<br>`3` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `Conditional_HealthThreshold`


**Definition:** Contains an inner effect block that only executes if the target's health is below a threshold, defined by `threshold_flat`, `threshold_percent`, or `threshold_expr`.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnTookDamage`](./Items_and_Equipment.md#object-statusontookdamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 1 | Default<br>FormChange<br>Druid |
| `threshold_flat` | Integer | The flat health value (in hit points) below which the target must be for the conditional to trigger. | 1 | `0`<br>`10`<br>`3` |
| [`Conditional_OncePerBattle`](./Items_and_Equipment.md#object-conditional_onceperbattle) | Object  | An object containing effects that can only trigger once per battle, preventing double-activation. | 1 | `{ . . . }` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | passives<br>class<br>tag |

</details>


---


### Object: `ClassManaCostReduction`


**Definition:** Defines a reduction in mana cost for abilities of a specific class.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `reduction` | Integer | The amount or percentage by which mana cost is reduced. | 4 | `1`<br>`2`<br>`3` |
| [`class`](../Reference_and_Meta/Enums.md#enum-class) | Enum | Specifies the class that this ability belongs to, used for categorization and restrictions. | 3 | `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |

</details>


---


### Object: `AddTemporaryEffectsToBasicAttack`


**Definition:** A container object that lists temporary status effects applied to the unit's basic attack.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CastAgainWithStatus`](./Items_and_Equipment.md#object-castagainwithstatus) | Object  | Defines parameters for recasting an ability when the unit has the specified status effect. | 1 | `{ . . . }` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


---


### Object: `StatusOnGainCoins`


**Definition:** Specifies status effects applied when this unit gains coins.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| `Shield` | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 1 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `LuckUp` | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 1 | `-1`<br>`-2`<br>`-4` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusOnAllyCatDeath`


**Definition:** An object listing status effects applied to the unit when an allied cat dies.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| [`DivineShield`](../Reference_and_Meta/Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | `1`<br>`2`<br>`4` |
| `RepairTrinket` | Integer | The number of stacks of the Repair Trinket status effect to apply. | 1 | `1`<br>`99` |

</details>


---


### Object: `SpawnObjectOnPopCorpse`


**Definition:** Specifies an object (as a string or an object with 'object', 'count', 'except_tiny' keys) to spawn on a corpse when it is popped.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 1 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`count`](../Reference_and_Meta/Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 1 | `0`<br>`1`<br>`10` |
| `except_tiny` | Boolean | If true, the spawning effect is not triggered for tiny (small) corpses. | 1 | `true` |

</details>


---


### Object: `ReviveNextRound`


**Definition:** The number of revives granted, or an object defining revive properties.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleStart`](./Items_and_Equipment.md#object-statusonbattlestart)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 1 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `revive_health` | Integer | The amount of health (as a flat integer or percentage) the unit revives with. | 1 | `1`<br>`100%`<br>`50%` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `ItemAuxTransform`


**Definition:** Transforms the item into another when its auxiliary value reaches specified thresholds.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`le`](../Reference_and_Meta/Arrays.md#array-le) | Array | An array specifying a [aux value, item] pair to transform to when the aux value is less than or equal to a specific value. | 6 | `[10 MoneyBag_Small]`<br>`[25 MoneyBag_Medium]`<br>`[50 MoneyBag_Large]` |
| [`ge`](../Reference_and_Meta/Arrays.md#array-ge) | Array | An array specifying a [durability, item] pair to transform to when durability is greater than or equal to a specific value. | 2 | `[10 NuclearKnife_Glowing]`<br>`[2 WaterBottle_Full]`<br>`[20 BlackShard_Glowing]` |
| [`lt`](../Reference_and_Meta/Arrays.md#array-lt) | Array | An array specifying a [aux value, item] pair to transform to when the aux value is strictly less than a specific value. | 1 | `[10 NuclearKnife]` |

</details>


---


### Object: `DestroyEquipmentAndAttachParasite`


**Definition:** Attempts to destroy a random piece of the target's equipment and attach a parasite from the specified pool.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleStart`](./Items_and_Equipment.md#object-statusonbattlestart)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`pool`](../Reference_and_Meta/Arrays.md#array-pool) | Array / Enum | Specifies the name of the pool from which an ability is learned or an item is crafted. | 1 | `2`<br>`3`<br>`4` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |

</details>


---


### Object: `DelayedAutoRevive`


**Definition:** Configures an automatic revival after a delay, with specified rounds and health percentage.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `health` | Integer | The maximum hit points of the unit. | 5 | `0`<br>`1`<br>`10` |
| `rounds` | Integer | The number of rounds after which the auto-revive triggers. | 5 | `1`<br>`2` |

</details>


---


### Object: `Conditional_PartyMember`


**Definition:** A conditional block that executes its child actions only if the target is a party member.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ExtraStatusWhenDealingDamage`](./Items_and_Equipment.md#object-extrastatuswhendealingdamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 3 | Default<br>FormChange<br>Druid |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | passives<br>class<br>tag |

</details>


---


### Object: `ChanceToBackflip`


**Definition:** An object specifying the ability to use and the percentage chance to perform a backflip dodge when hit.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 2 | `.02`<br>`.1`<br>`.15` |

</details>


---


### Object: `AddStatusToElementDamage`


**Definition:** An object that applies a specific status effect when dealing damage of a specified element. Contains sub-keys for the element and the status to apply.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| [`element`](../Reference_and_Meta/Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 2 | `Electric`<br>`Fire`<br>`Gravity` |
| `Burn` | Equation | The amount of Burn applied, either as a fixed number or a formula string. | 1 | `1`<br>`10`<br>`2` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` | `Stun` | Array | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `TransformItemOnElementInfluence`


**Definition:** Transforms the item into the specified one when influenced by the given element, optionally fully repairing it.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](../Reference_and_Meta/Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 5 | `Electric`<br>`Fire`<br>`Gravity` |
| [`item`](../Reference_and_Meta/Enums.md#enum-item) | Enum | Specifies the item to transform into, either by name, a nested item object, or a numeric value. | 5 | `1`<br>`2`<br>`EstusFlask_Full` |
| `full_repair` | Boolean | If true, the item's durability is fully restored when transformed by element influence. | 5 | `true` |

</details>


---


### Object: `StatusOnTurnEndIfDidntCastAbilityTypes`


**Definition:** Applies the contained status effects at turn end if the unit did not cast an ability of the specified type(s).  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 4 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 4 | passives<br>class<br>tag |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 1 | `1`<br>`2`<br>`3` |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 1 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `Shield` | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 1 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 1 | `1`<br>`2`<br>`3` |
| `Charge` | Equation | The number of charge stacks applied. | 1 | `1`<br>`2`<br>`3` |
| `SpellDamageUp` | Integer | The number of stacks of SpellDamageUp applied, increasing spell damage. | 1 | `1`<br>`3` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusOnPopCorpse`


**Definition:** Specifies the effects applied when the unit pops a corpse.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |
| `HealthGain` | Integer | The amount of health restored to the source. | 1 | `1`<br>`10`<br>`2` |
| [`RepairWeapon`](../Reference_and_Meta/Arrays.md#array-repairweapon) | Array / Integer  | The number of weapon durability points restored; an array [stacks, probability] applies a chance-based repair. | 1 | `1`<br>`6`<br>`99` |
| `RepairTrinket` | Integer | The number of stacks of the Repair Trinket status effect to apply. | 1 | `1`<br>`99` |

</details>


---


### Object: `StatusOnEndMove`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 4 | passives<br>class<br>tag |

</details>
### Object: `StatusOnEatFood`


**Definition:** An object listing status effects applied to the unit when it eats food.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| `RepairTrinket` | Integer | The number of stacks of the Repair Trinket status effect to apply. | 1 | `1`<br>`99` |
| [`TempPassiveUntilSettled`](./Items_and_Equipment.md#object-temppassiveuntilsettled) | Object | An object containing a temporary passive that is applied until the character's position is settled. | 1 | `{ . . . }` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusAllCharactersOnSpawn`


**Definition:** Defines status effects applied to all characters when they spawn into the battlefield.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid` | [`Conditional_Boss`](./Items_and_Equipment.md#object-conditional_boss) | Object || 0 | Default<br>FormChange<br>Druid |
| `Poison` | Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`10`<br>`2` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>


---


### Object: `ExtraStatusWhenDealingDamage`


**Definition:** Defines additional statuses applied to the target or source when dealing damage, with conditionals.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `Eternal`


**Definition:** Defines the Eternal revival effect, setting stacks and the health percentage restored.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `health_percent` | Integer | The amount of health (as a percentage) the unit retains after being revived or survived a fatal hit. | 1 | `100%`<br>`50%` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 1 | `{ . . . }` |

</details>


---


### Object: `ElementalManaCostReduction`


**Definition:** An object that reduces the mana cost of spells of specified elements, with sub-keys for element and reduction amount.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](../Reference_and_Meta/Arrays.md#array-element) | Array / Enum | Specifies which element(s) the conditional checks against. | 2 | `Electric`<br>`Fire`<br>`Gravity` |
| `reduction` | Integer | The amount or percentage by which mana cost is reduced. | 2 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `CreateGlobalModifiers`


**Definition:** Defines global gameplay modifiers to activate.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnDie`](./Items_and_Equipment.md#object-statusondie), [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Global Modifier Keys}`](../Engine_Scripts_and_Logic/Engine_GlobalModifierKeys.md#valid-property-keys) | Variable | If true, activates a global modifier effect on the house environment. | 2 | `CreateGlobalModifiers`<br>`BloodRain`<br>`NextPlayerCatTakesExtraTurn` |
| `NoCorpses` | `Number` | If set to 1, corpses are prevented from spawning. | 1 | `1` |
| `NextPlayerCatTakesExtraTurn` | `Number` | The number of extra turns the active player cat gains. | 1 | `1` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


---


### Object: `Conditional_Shielded`


**Definition:** An object containing effects that are only applied if the target has a shield active.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Items_and_Equipment.md#object-statusonbattleend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>tag |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `AddPassivesToCharmed`


**Definition:** Grants the contained passive effects to units under the charm status.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | `-1`<br>`-2`<br>`1` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusOnTakeHealthOrShieldDamage`


**Definition:** An object that applies a status effect when the unit takes damage to either health or shields.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 4 | passives<br>class<br>tag |
| [`DivineShield`](../Reference_and_Meta/Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 2 | `1`<br>`2`<br>`4` |
| [`Conditional_GoodRoll`](./Items_and_Equipment.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 1 | `{ . . . }` |
| `Metronome` | `Number` | The number of times Metronome triggers, or an object with stacks and banned abilities. | 1 | `1`<br>`2` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `StatusOnHealed`


**Definition:** An object that applies a status effect to the unit whenever it is healed.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 1 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusOnBreakItem`


**Definition:** An object containing status effects to apply when the unit breaks a weapon or armor item.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 1 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`DoDamage`](./Items_and_Equipment.md#object-dodamage) | Object  | Contains damage parameters (amount, type, tile targets) to deal damage to the target. | 1 | `{ . . . }` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid`
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>


---


### Object: `StatusEachTurnEndForEachTurn`


**Definition:** Statuses applied at the end of each turn, with the number of turns as nested values.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| [`ForceUseAbility`](../Reference_and_Meta/Enums.md#enum-forceuseability) | Enum  | The name of the ability the source is forced to use, optionally with a chance. | 1 | `CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |

</details>


---


### Object: `StatusAfterCastSpell`


**Definition:** An object containing status effects to apply to the unit immediately after it casts any spell.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid` | [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 | Default<br>FormChange<br>Druid |
| [`UseAbility`](../Reference_and_Meta/Enums.md#enum-useability) | Enum  | The name of the ability the target is forced to use. | 1 | `GirlDinoPoop`<br>`KirbySpit`<br>`MD_PoopChain` |
| `TempRangeUp` | Integer | The amount of temporary range increase applied. | 1 | `1`<br>`2`<br>`20` |
| `TempMeleeRangeUp` | Integer | The number of tiles added to the unit's melee attack range as a temporary buff. | 1 | `1` |

</details>


---


### Object: `RemoveStatusStacks`


**Definition:** An object specifying a status name and the number of stacks to remove from the target.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasStatus`](./Items_and_Equipment.md#object-conditional_hasstatus)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>tag |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`status`](../Reference_and_Meta/Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 1 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |

</details>


---


### Object: `PoopWhenHit`


**Definition:** Specifies the object (e.g., Poop) spawned when the unit is hit, or an object with `chance` and `object`.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 1 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |

</details>


---


### Object: `PassiveWhenDead`


**Definition:** Passive effects that remain active while the unit is dead.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `PassiveAfterXKills`


**Definition:** Activates a set of passive effects (e.g., extra attacks, stat boosts) after the unit achieves a certain number of kills defined by the 'stacks' sub-key.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| [`passives`](./Items_and_Equipment.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |

</details>


---


### Object: `global_passives`


**Definition:** An object containing global passive modifiers that apply to the entire run.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `GlobalEnemyAutoRevive` | Integer | The percentage chance for all enemies to automatically revive after being defeated. | 2 | `100%`<br>`30%` |
| `NoCorpses` | `Number` | If set to 1, corpses are prevented from spawning. | 1 | `1` |
| `RealTimePressure` | Integer | The number of real-time seconds before a pressure effect or penalty applies. | 1 | `5` |
| [`{Global Modifier Keys}`](../Engine_Scripts_and_Logic/Engine_GlobalModifierKeys.md#valid-property-keys) | Variable | If true, activates a global modifier effect on the house environment. | 1 | `CreateGlobalModifiers`<br>`BloodRain`<br>`NextPlayerCatTakesExtraTurn` |

</details>


---


### Object: `FlyDamageIncrease`


**Definition:** The number of stacks or alias for damage increase against flying units.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `allies_only` | Boolean | If true, the effect only applies to allied units. | 1 | `false`<br>`true` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 1 | `{ . . . }` |

</details>


---


### Object: `Conditional_RandomChance`


**Definition:** An object containing effects that execute only if a random roll succeeds, with an odds value defined inside.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnDie`](./Items_and_Equipment.md#object-statusondie)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 1 | Default<br>FormChange<br>Druid |
| `odds` | Float | The probability of the effect occurring, expressed as a decimal or percentage. | 1 | `.1`<br>`.16666666`<br>`.3` |
| [`ApplyPassives`](./Items_and_Equipment.md#object-applypassives) | Object  | Specifies the passives or status effects to apply to the unit. | 1 | `{ . . . }` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>


---


### Object: `Conditional_OncePerBattle`


**Definition:** An object containing effects that can only trigger once per battle, preventing double-activation.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HealthThreshold`](./Items_and_Equipment.md#object-conditional_healththreshold), [`StatusOnFullMana`](./Items_and_Equipment.md#object-statusonfullmana)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 1 | Default<br>FormChange<br>Druid |
| `Shield` | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 1 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `SpellDamageUp` | Integer | The number of stacks of SpellDamageUp applied, increasing spell damage. | 1 | `1`<br>`3` |
| [`key`](../Reference_and_Meta/Enums.md#enum-key) | Enum | A unique string identifier used to track if an effect has been applied once per turn, preventing reapplication. | 1 | `EtherSoakedRag`<br>`JewelOfDrog`<br>`TaintedOffering` |
| `ReduceManaCost` | Integer | The number of stacks reducing mana cost of abilities. | 1 | `1`<br>`2` |
| `ShowText` | `String` | Specifies the localization key for a popup text displayed on the target. | 1 | `"COMBAT_POPUP_BRAINSTORM"`<br>`"COMBAT_POPUP_RELOAD"`<br>`"COMBAT_POPUP_REPAIRED"` |

</details>


---


### Object: `Conditional_Adjacent`


**Definition:** An object whose nested keys define statuses or effects applied to or by units that are adjacent to the unit.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ScaledStatusAlliesOnSpendMana`](./Items_and_Equipment.md#object-scaledstatusalliesonspendmana), [`StatusAlliesEachTurn`](./Items_and_Equipment.md#object-statusallieseachturn)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 2 | Default<br>FormChange<br>Druid |
| [`Conditional_Ally`](./Items_and_Equipment.md#object-conditional_ally) | Object | Defines effects that apply only if the target is an ally, with an optional else block for non-allies. | 1 | `{ . . . }` |
| [`Conditional_PlayerCat`](./Items_and_Equipment.md#object-conditional_playercat) | Object | Defines effects that only apply if the target is a player-controlled cat. | 1 | `{ . . . }` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | passives<br>class<br>tag |

</details>


---


### Object: `ChanceToBlockAndCounter`


**Definition:** The percentage chance or an object defining chance and conditions to block and counter an attack.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |
| `backstab_only` | Boolean | If true, the block and counter effect only triggers on attacks made from behind the target. | 1 | `true` |

</details>


---


### Object: `BuffImmunity`


**Definition:** If 1, the unit is immune to buffs. An optional object can list buffs to exclude from immunity.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exclude`](../Reference_and_Meta/Enums.md#enum-exclude) | Enum | Specifies an element or effect that does not trigger the form change. | 1 | `SpellDamageUp`<br>`fire`<br>`water` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 1 | `{ . . . }` |

</details>


---


### Object: `ApplyStatusesToRandomEnemiesEachTurn`


**Definition:** An object specifying statuses to apply to random enemies each turn, with an optional 'count' field.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| [`count`](../Reference_and_Meta/Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 1 | `0`<br>`1`<br>`10` |
| `Marked` | Integer | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`3`<br>`5` |
| `Bounty` | Integer | The number of bounty stacks applied to enemies, increasing rewards on defeat. | 1 | `1`<br>`3` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `AddStatusToSpells`


**Definition:** Specifies status effects added to all spell attacks used by this unit.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


---


### Object: `TempPassiveUntilSettled`


**Definition:** An object containing a temporary passive that is applied until the character's position is settled.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnEatFood`](./Items_and_Equipment.md#object-statusoneatfood)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `LimitHeal` | Integer | If 1, prevents the unit from being healed. | 1 | `0`<br>`1` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>


---


### Object: `StatusWhenAllySpendsMana`


**Definition:** Specifies the effects applied when an ally spends mana.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| `Charge` | Equation | The number of charge stacks applied. | 1 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `StatusOnUseBasicAttack`


**Definition:** Specifies the effects applied when the unit performs a basic attack.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 1 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `HealthGain` | Integer | The amount of health restored to the source. | 1 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `StatusOnPickupCoins`


**Definition:** Specifies the effects applied when the unit picks up coins.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`GainCoins`](../Reference_and_Meta/Arrays.md#array-gaincoins) | Array / Integer  | The amount of coins gained, or a [min, max] range. | 1 | `-5`<br>`1`<br>`2` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>


---


### Object: `StatusOnCollectPickup`


**Definition:** An object containing status effects to apply when the unit collects a pickup item.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`StatusAfterXStacks`](./Items_and_Equipment.md#object-statusafterxstacks) | Object | Defines a condition that triggers a status effect when a specified stack key reaches a threshold, optionally expiring at turn end. | 1 | `{ . . . }` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>


---


### Object: `StatusEachRoundEnd`


**Definition:** An object listing status effects applied to the unit at the end of each round.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveWhenDead`](./Items_and_Equipment.md#object-passivewhendead)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid` | [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | Default<br>FormChange<br>Druid |
| [`DoDamage`](./Items_and_Equipment.md#object-dodamage) | Object  | Contains damage parameters (amount, type, tile targets) to deal damage to the target. | 1 | `{ . . . }` |

</details>


---


### Object: `StackingFlowerTrail`


**Definition:** An object defining how a flower trail status stacks (stacks count, stack key) when the unit moves.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 3 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`stack_key`](../Reference_and_Meta/Enums.md#enum-stack_key) | Enum | Specifies the key of the status stack to check for the condition. | 3 | `CATHIDE`<br>`EMPTY_GENERATOR`<br>`FANNY_PACK` |

</details>


---


### Object: `SetItemAux`


**Definition:** Configures an item's auxiliary value by specifying a target slot and a formula for the new value.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Shielded`](./Items_and_Equipment.md#object-conditional_shielded), [`StatusOnBattleEnd`](./Items_and_Equipment.md#object-statusonbattleend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `value` | Float | The numeric value or formula associated with the buff. | 3 | `.5`<br>`0`<br>`1` |
| `slot` | Integer | Specifies the equipment slot (e.g., 'head', 'trinket', 'random_empty') where the crafted item is placed. | 3 | `0`<br>`1`<br>`2` |

</details>


---


### Object: `ScaledStatusOnSpendMana`


**Definition:** An object containing status effect definitions to apply when the unit spends mana, with the number of stacks scaled by the amount of mana spent.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| [`StatusAfterXStacks`](./Items_and_Equipment.md#object-statusafterxstacks) | Object | Defines a condition that triggers a status effect when a specified stack key reaches a threshold, optionally expiring at turn end. | 1 | `{ . . . }` |

</details>


---


### Object: `PassiveWhileInMonkMeleeStance`


**Definition:** Applies specific passive effects (e.g., Brace, HealthRegenUp) while the unit is in the Monk's melee combat stance.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| `Brace` | Array / Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 1 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `PassiveWhenDead`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |

</details>
### Object: `ExtraStatusWhenDealingDamage`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |

</details>
### Object: `Conditional_PartyMember`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>
### Object: `BouncyProjectiles`


**Definition:** An object with 'max_bounces' and 'max_range' defining projectile bounciness behavior.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`max_range`](../Reference_and_Meta/Enums.md#enum-max_range) | Equation | The maximum range of the ability, can be a static number or an expression. | 1 | `"4+(1-clamp(spd,0,1))*2"`<br>`"max(5-int, 1)"`<br>`-1` |
| `max_bounces` | Integer | The maximum number of bounces for a projectile; -1 means infinite. | 1 | `-1`<br>`1`<br>`10` |

</details>


---


### Object: `ApplyToRandomPartyMemberIfPossible`


**Definition:** Contains an inner effect block that is applied to a random living party member if one exists.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBreak`](./Items_and_Equipment.md#object-statusonbreak)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `AddStatusToKnockbackDamage`


**Definition:** An object whose nested keys define statuses applied to damage caused by knockback.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


---


### Object: `AddSelfStatusToWeapons`


**Definition:** An object whose nested keys define status effects applied to the unit's own weapons.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 1 | `{ . . . }` |

</details>


---


### Object: `TransformWeapon`


**Definition:** An object with `from` and `to` fields specifying the weapon transformation.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Items_and_Equipment.md#object-statusonbattleend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`to`](../Reference_and_Meta/Enums.md#enum-to) | Enum | Specifies the target equipment item after transformation. | 1 | `JarOfNothing`<br>`Necro_SoulDagger_Charged`<br>`Necro_SoulDagger_Uncharged` |
| [`from`](../Reference_and_Meta/Enums.md#enum-from) | Enum | Specifies the source equipment item to be transformed. | 1 | `JarOfChaos`<br>`Necro_SoulDagger_Charged`<br>`Necro_SoulDagger_Uncharged` |

</details>


---


### Object: `str_aux_is_copy_ability`


**Definition:** An object defining bonus passives and ability modifications for an auxiliary ability that is copied.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bonus_passives`](./Items_and_Equipment.md#object-bonus_passives) | Object  | Grants temporary passive abilities to the caster for the duration of the ability. | 2 | `{ . . . }` |

</details>


---


### Object: `StatusOnBackstab`


**Definition:** An object containing status effects to apply when the unit performs a backstab attack.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthGain` | Integer | The amount of health restored to the source. | 1 | `1`<br>`10`<br>`2` |
| `SerratedClaws` | Integer | The number of stacks of the SerratedClaws status applied, or an object defining its display strings. | 1 | `1` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>


---


### Object: `StatusIfUnusedActPoints`


**Definition:** An object containing status effects to apply to the unit if it has unused action points at the end of its turn.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


---


### Object: `StatusIfUnusedActPoints`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>
### Object: `StatusAlliesEachTurn`


**Definition:** Defines a status effect applied to all allies each turn, with an optional exclusion of the owner and conditional checks.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 1 | `{ . . . }` |

</details>


---


### Object: `StatusAfterXTurns`


**Definition:** Applies a status effect or forces an ability usage after a set number of turns.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`ForceUseAbility`](../Reference_and_Meta/Enums.md#enum-forceuseability) | Enum  | The name of the ability the source is forced to use, optionally with a chance. | 1 | `CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |

</details>


---


### Object: `StatusAfterXStacks`


**Definition:** Defines a condition that triggers a status effect when a specified stack key reaches a threshold, optionally expiring at turn end.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ScaledStatusOnSpendMana`](./Items_and_Equipment.md#object-scaledstatusonspendmana), [`StatusOnCollectPickup`](./Items_and_Equipment.md#object-statusoncollectpickup)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `threshold` | Equation / Object | The health threshold value, either as a formula using X (max health) or a fixed integer. | 2 | `{ . . . }`<br>`"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |
| [`stack_key`](../Reference_and_Meta/Enums.md#enum-stack_key) | Enum | Specifies the key of the status stack to check for the condition. | 2 | `CATHIDE`<br>`EMPTY_GENERATOR`<br>`FANNY_PACK` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| `expires_on_end_turn` | Boolean | If true, the temporary effect expires at the end of the target's turn. | 1 | `true` |
| `RefreshActPoints` | Integer | The amount of action points restored to the source. | 1 | `1` |
| `ExtraBasicMoves_Status` | Integer | The number of extra basic moves per turn granted. | 1 | `1` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `SpawnItemLinkedFamiliar`


**Definition:** An object defining a familiar to spawn that is linked to a specific item, which breaks when the familiar is defeated.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 2 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| `break_on_pop_only` | Boolean | If true, the linked familiar spawn only breaks when the item is popped. | 2 | `true` |

</details>


---


### Object: `RefreshEquipmentAbilityOnElement`


**Definition:** Refreshes the cooldown of the unit's equipment ability when the unit's attack matches the specified element (e.g., Electric), displaying a recharge popup.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](../Reference_and_Meta/Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 2 | `Electric`<br>`Fire`<br>`Gravity` |
| [`text`](../Assets_and_Localization/Strings.md#string-text) | String | The localization key for the name of this injury. | 2 | `""`<br>`"COMBAT_POPUP_RECHARGED"`<br>`"INJURY_NAME_BROKENLEG"` |

</details>


---


### Object: `PassiveIfWeaponIsUsable`


**Definition:** Activates a set of passive effects (e.g., Brace) only if the unit's current weapon is in a usable condition (not broken or disabled).  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Brace` | Array / Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 2 | `1`<br>`10`<br>`2` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |

</details>


---


### Object: `ModifyAbility`


**Definition:** Specifies the modifications to an ability's properties, such as cost or type.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Items_and_Equipment.md#object-bonus_passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`meta`](./Items_and_Equipment.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 2 | `{ . . . }` |
| [`cost`](./Items_and_Equipment.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 2 | `{ . . . }` |

</details>


---


### Object: `Conditional_Adjacent`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>
### Object: `ArmorBreakOnHit`


**Definition:** An object defining durability loss and chance for armor to break when hit.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance_to_break` | Integer | The percentage chance that the armor breaks on hit. | 2 | `10%`<br>`5%` |
| `durability_loss` | Integer | The amount of durability lost when the armor break effect triggers. | 2 | `0` |

</details>


---


### Object: `AllyDodgeChanceAura`


**Definition:** An object granting allies within a specified range a percentage chance to dodge incoming attacks.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |
| `range` | Integer | The distance in tiles for the trigger effect; `global` means any distance. | 1 | `1`<br>`10`<br>`2` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 1 | `{ . . . }` |

</details>


---


### Object: `AddStatusToSpells`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>
### Object: `AddStatusToKnockbackDamage`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>
### Object: `TunnelVision`


**Definition:** If present, grants the TunnelVision status, which modifies crit_chance as defined in its sub-properties.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `crit_chance` | Float | The chance for the damage instance to critically hit, expressed as a percentage or equation; values above 1 default to 100%. | 1 | `-999999`<br>`.05*X`<br>`.25` |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 1 | `damage_instance`<br>`spell`<br>`self_damage` |

</details>


---
### Object: `TintItem`


**Definition:** Defines additive and multiplicative color tint adjustments applied to an item's appearance, with an optional ignore condition.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`add`](../Reference_and_Meta/Arrays.md#array-add) | Array / Equation | The amount or an array of values added to the event's advantage or item tint. | 1 | `5`<br>`[0.05 0.05 0.05]` |
| [`ignore_if_str_aux_equals`](../Reference_and_Meta/Enums.md#enum-ignore_if_str_aux_equals) | Enum | Specifies the string aux value at which to ignore the tinting operation. | 1 | `ModelingClay_Default` |
| [`mul`](../Reference_and_Meta/Arrays.md#array-mul) | Array | An array of three floats (RGB) used to multiply the item's tint color. | 1 | `[0.45 0.3 0.25]` |

</details>


---


### Object: `StatusOnFullMana`


**Definition:** Defines a status effect applied to the unit when its mana is full, with an optional once-per-battle conditional.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_OncePerBattle`](./Items_and_Equipment.md#object-conditional_onceperbattle) | Object  | An object containing effects that can only trigger once per battle, preventing double-activation. | 1 | `{ . . . }` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 1 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `StatusOnFallAsleep`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>


### Object: `StatusOnFallAsleep`


**Definition:** Defines one or more beneficial status effects applied to the unit when it falls asleep.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | `-1`<br>`-2`<br>`1` |
| `FillMana` | Integer | The amount of mana restored, or an [amount, probability] array. | 1 | `1`<br>`[1 .10]`<br>`[1 .25]` |
| `HealRandomInjury` | Integer | The number of random injuries healed on the target. | 1 | `1` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag` | [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `StatusOnEnemyDeath`


**Definition:** Defines a status effect applied to the unit each time an enemy dies.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Charge` | Equation | The number of charge stacks applied. | 1 | `1`<br>`2`<br>`3` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>


---


### Object: `StatusOnDodge`


**Definition:** Defines a status effect applied to the unit each time it successfully dodges an attack.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DodgeChance_Status` | Integer | The flat percentage increase to dodge chance applied as a status effect. | 1 | `1`<br>`10`<br>`100` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>


---


### Object: `StatusAlliesEachTurn`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>
### Object: `StatusAdjacentOnTheirTurnEnd`


**Definition:** Defines a status effect applied to adjacent units when their turn ends, such as forcing them to move away.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ForceMoveAway` | `Number` | The distance to force the target away from the source. | 1 | `1` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


---


### Object: `StatDependentPassive`


**Definition:** An object containing formulas that dynamically modify passive effects based on the unit's stats (e.g., str, dex, int).  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AddDamageToBasicAttack` | Enum | Additional damage added to the basic attack, either as a flat value or formula. | 1 | `1`<br>`2`<br>`4` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>


---


### Object: `SpawnRandomPickupsOnTaggedUnitKilled`


**Definition:** Defines a pool of random pickups (items) spawned when a unit with a specific tag is killed, with a count range.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](../Reference_and_Meta/Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 1 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| [`count`](../Reference_and_Meta/Arrays.md#array-count) | Array / Integer | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 1 | `0`<br>`1`<br>`10` |

</details>


---


### Object: `ScaledStatusOnHolyShieldBlock`


**Definition:** An object that applies a scaled status (e.g., RandomMagicMissile) when the unit blocks an attack with a holy shield.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RandomMagicMissile` | Integer | The number of random magic missiles fired, or an object defining its properties. | 1 | `1`<br>`10`<br>`2` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>


---


### Object: `ScaledStatusAlliesOnSpendMana`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>
### Object: `ScaledStatusAlliesOnSpendMana`


**Definition:** An object that applies a scaled status (e.g., ManaGain) to adjacent allies whenever the unit spends mana.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `ScaldingOrbMoonBossOneShot`


**Definition:** An object that completes the ScaldingOrb quest and removes the item from the unit's inventory.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CompleteItemQuest` | `String` | Specifies the item quest ID to mark as complete on kill. | 1 | `BlackShard`<br>`Nuke`<br>`ScaldingOrb` |
| `RemoveItem` | `String` | Specifies the item ID to remove from the source on kill. | 1 | `BlackShard`<br>`BlackShard_Glowing`<br>`ScaldingOrb` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `PassiveWhileShielded`


**Definition:** An object containing passives that are active only while the unit has a shield.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 1 | `1`<br>`2`<br>`3` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>


---


### Object: `PassiveWhileHasDurability`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>
### Object: `PassiveWhileHasDurability`


**Definition:** An object containing passives that are active only while the item has remaining durability.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `ObjectDetector`


**Definition:** An object that grants a chance to detect a specific item (e.g., CharmedDip) when loot is evaluated.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 1 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |

</details>


---


### Object: `ManaGainRange`


**Definition:** Defines the minimum and maximum mana gained per turn.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnBegin`](./Items_and_Equipment.md#object-statuseachturnbegin)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max` | Integer | The maximum amount of coins that can be gained. | 1 | `10`<br>`2`<br>`25` |
| `min` | Integer | The minimum amount of coins that will be gained. | 1 | `0`<br>`1`<br>`10` |

</details>


---


### Object: `KnockbackIfCrit`


**Definition:** Defines knockback properties applied when a critical hit occurs.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToAllDamage`](./Items_and_Equipment.md#object-addstatustoalldamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `knockback` | Equation | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 1 | `"ceil(X*.25/5)"`<br>`-10`<br>`-2` |
| `override_chain_knockback` | Integer | The distance in tiles the unit is knocked back if a critical hit triggers chain knockback. | 1 | `10` |

</details>


---


### Object: `GlobalMeleeRevengeDamage`


**Definition:** Defines revenge damage properties (e.g., knockback) when hit by a melee attack.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `knockback` | Equation | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 1 | `"ceil(X*.25/5)"`<br>`-10`<br>`-2` |

</details>


---


### Object: `ForceUseAbilityOnTarget`


**Definition:** Defines a chance to force the unit to use a specified ability on the target.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Items_and_Equipment.md#object-addstatustobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |

</details>


---


### Object: `ConvertDamageToScaledStatus`


**Definition:** Converts a portion of incoming damage into a specified status effect with a given number of stacks.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `DelayedPain` | Integer | The number of stacks of DelayedPain applied, dealing damage after a delay. | 1 | `1` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>


---


### Object: `Conditional_Shielded`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>
### Object: `Conditional_ManaThreshold`


**Definition:** Defines a conditional block that applies effects only if a unit's mana meets a specified threshold.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnEnd`](./Items_and_Equipment.md#object-statuseachturnend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `threshold_flat` | Integer | The flat health value (in hit points) below which the target must be for the conditional to trigger. | 1 | `0`<br>`10`<br>`3` |
| `RepairTrinket` | Integer | The number of stacks of the Repair Trinket status effect to apply. | 1 | `1`<br>`99` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 1 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `Conditional_HealthThreshold`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>
### Object: `ChanceToForceEvent`


**Definition:** Defines the chance and the specific event to force to occur.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |
| [`event`](../Reference_and_Meta/Enums.md#enum-event) | Enum | Specifies the event to force, either by name or by a nested object defining its type and level. | 1 | `Blessing`<br>`Death`<br>`Tragedy` |

</details>


---


### Object: `CatPartsSizeScale`


**Definition:** A multiplier for the size of specific cat parts (e.g., head, body).  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `head` | Float | The catalog ID for the cat's head part. | 1 | `-1`<br>`1`<br>`1.3` |

</details>


---


### Object: `CastAgainWithStatus`


**Definition:** Defines parameters for recasting an ability when the unit has the specified status effect.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddTemporaryEffectsToBasicAttack`](./Items_and_Equipment.md#object-addtemporaryeffectstobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `OverrideDamage` | `Number` | Overrides the damage of the current action to this flat value (can be negative to heal). | 1 | `-10`<br>`0`<br>`1` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>tag |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `ApplyToRandomPartyMemberIfPossible`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>
### Object: `AlluringDoodieEater`


**Definition:** An object defining the chance and damage instance for a unit that consumes an alluring doodie.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Items_and_Equipment.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |

</details>


---


### Object: `AIControlNextTurn`


**Definition:** An object that causes the unit to be controlled by the AI on its next turn, with configurable stacks and spell usage.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `include_spells` | Boolean | If true, the AI-controlled bonus turn includes spells as available actions. | 1 | `true` |

</details>


---


### Object: `AddStatusToBackstabs`


**Definition:** An object defining statuses applied to the target when the unit performs a backstab attack.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Bleed` | Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`10`<br>`2` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>


---


### Object: `AddSelfStatusToWeapons`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>
### Object: `AddAdvantageToEvent`


**Definition:** Specifies additional advantage options to add to a specific event type.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`options`](../Reference_and_Meta/Arrays.md#array-options) | Array | An array of named option objects within an event, each defining a possible action the player can take. | 1 | `[smash bash open]` |
| [`add`](../Reference_and_Meta/Arrays.md#array-add) | Array / Integer | The amount or an array of values added to the event's advantage or item tint. | 1 | `5`<br>`[0.05 0.05 0.05]` |

</details>


---


### Object: `AbilityOnRoundEndOnce`


**Definition:** Specifies an ability to be used once at the end of the round.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `even_of_stunned` | Boolean | If true, the ability triggers only on even rounds and when the unit is stunned. | 1 | `true` |

</details>


---

