# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Items & Equipment

> **Associated Files:** `data/items/, data/item_setbonuses.gon`


### Object: `ROOT`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1116

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 3307 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1571 | passives<br>class<br>	ag |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 2423 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1910 | `{ . . . }` |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. | 1195 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| `frame` | Integer | The sprite frame index to display. | 1105 | `1`<br>`10`<br>`100` |
| [`kind`](./Enums.md#enum-kind) | Enum | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1105 | `face`<br>`head`<br>`modifier` |
| [`set`](./Arrays.md#array-set) | Array / Enum  | Specifies the set name(s) the item belongs to for set bonuses. | 985 | `80s`<br>`90s`<br>`AdvancedAlloy` |
| [`rarity`](./Enums.md#enum-rarity) | Enum | Determines the rarity tier of the item, affecting drop rates and item quality. | 966 | `common`<br>`consumable_common`<br>`consumable_rare` |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 364 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`shield`](./Enums.md#enum-shield) | Enum / Integer  | The shield value granted by this mutation, or 'aux' to use the unit's auxiliary stat. | 191 | `"max((aux-1)*2, 0)"`<br>`1`<br>`10` |
| [`durability`](./Arrays.md#array-durability) | Array / Integer  | The amount of durability consumed by this ability or required for its use. | 170 | `0`<br>`1`<br>`10` |
| [`cha`](./Enums.md#enum-cha) | Enum / Integer  | The Charisma stat value or modifier. | 89 | `+1`<br>`-1`<br>`-2` |
| [`con`](./Enums.md#enum-con) | Enum / Integer  | The Constitution stat value or modifier. | 79 | `-1`<br>`-2`<br>`-3` |
| [`spd`](./Enums.md#enum-spd) | Enum / Integer  | The Speed stat value or modifier. | 78 | `-1`<br>`-10`<br>`-2` |
| `cursed` | Boolean | If true, the item is cursed and may have negative effects when equipped or used. | 77 | `true` |
| [`int`](./Enums.md#enum-int) | Enum / Integer | The Intelligence stat value or modifier. | 66 | `-1`<br>`-10`<br>`-2` |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. | 64 | `1`<br>`2`<br>`true` |
| [`lck`](./Enums.md#enum-lck) | Enum / Integer | The Luck stat value or modifier. | 53 | `-1`<br>`-2`<br>`-3` |
| [`str`](./Engine_DamagingKeys.md#valid-property-keys) | Variable | The Strength stat value or modifier. | 45 | `-1`<br>`-2`<br>`-3` |
| `quest_item` | Boolean | If true, this item is a quest item and cannot be sold or destroyed. | 40 | `false`<br>`true` |
| `parasite` | Boolean | If true, the item is a parasite that attaches to a unit and cannot be removed normally. | 36 | `true` |
| `aux` | Integer | An auxiliary integer value used for item properties, such as hunger value. | 33 | `-1`<br>`1`<br>`10` |
| [`dex`](./Enums.md#enum-dex) | Enum / Integer | The Dexterity stat value or modifier. | 30 | `-1`<br>`-2`<br>`-3` |
| [`keyword_tooltips`](./Passives_and_Statuses.md#object-keyword_tooltips) | Object  | Associates keyword tooltips with the ability, often used for status effects. | 28 | `{ . . . }` |
| [`quest_reward_item`](./Enums.md#enum-quest_reward_item) | Enum | The specific item awarded as a quest reward. The value uses a unique item identifier string. | 22 | `AirHorn_Fixed`<br>`AngryFace_Fixed`<br>`BubbleBoy_Fixed` |
| `divine_shield` | Integer | The number of stacks of the Divine Shield status this mutation provides. | 20 | `0`<br>`1`<br>`2` |
| `indestructible` | Boolean | If true, the item cannot be destroyed or removed. | 20 | `true` |
| [`speed`](./Arrays.md#array-speed) | Array / Float  | The speed of the projectile or move, can be a value or a range. | 19 | `-30`<br>`-4`<br>`.5` |
| `legacy_quest` | Boolean | If true, this item is part of a legacy quest. | 17 | `true` |
| [`hint_destination`](./Enums.md#enum-hint_destination) | Enum | Specifies the map destination hinted by this item or event. | 16 | `boneyard`<br>`caves`<br>`core` |
| [`str_aux_initialize`](./Enums.md#enum-str_aux_initialize) | Enum | Specifies a random fallback or initial auxiliary data when an item's str_aux is not set. The value is a comma-separated type string such as "random_stat" or "random_copyable_colorless_passive". | 15 | `random_class_ability`<br>`random_class_passive`<br>`random_copyable_class_ability` |
| `dont_destroy_on_0` | Boolean | If true, the item is not destroyed when its charges reach zero. | 13 | `true` |
| [`global_tags`](./Arrays.md#array-global_tags) | Array | A list of global tags that modify the run's behavior. | 12 | `[`<br>`[all_cats_are_jester]`<br>`[all_normal_events_are_weather]` |
| `max_durability` | Integer | The maximum number of uses or hits the item can endure before breaking. | 11 | `1`<br>`2`<br>`3` |
| [`on_store`](./Enums.md#enum-on_store) | Enum | Defines an action or transformation that occurs when the item is stored or placed in the player's inventory. Common values include "become_aux_coins", "become_furniture", or "become_rare_furniture". | 8 | `become_aux_coins`<br>`become_furniture`<br>`become_rare_furniture` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 7 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`hint_prerequisite_flag`](./Enums.md#enum-hint_prerequisite_flag) | Enum | Defines a map flag that must be set for the hint to appear. | 5 | `mapflag_BothObelisksUnlocked`<br>`mapflag_DimensionXUnlocked`<br>`mapflag_MeatWorldUnlocked` |
| `failable` | Boolean | If true, the event or action has a chance to fail. | 4 | `true` |
| [`global_passives`](./Miscellaneous.md#object-global_passives) | Object | An object containing global passive modifiers that apply to the entire run. | 4 | `{ . . . }` |
| `randomize_piece_frames` | Boolean | If true, the item's visual piece frames are randomized when it spawns or appears. | 4 | `true` |
| `str_aux_is_copy_passive` | Boolean | If true, the item's str_aux field is considered a passive that can be copied or duplicated by other items. | 4 | `true` |
| `fragile` | Boolean | If true, the item breaks permanently when its durability reaches zero. | 3 | `true` |
| [`icon_hint`](./Enums.md#enum-icon_hint) | Enum | Specifies a hint string used to determine the icon shown in the UI. Common values like "passive_syringe" or "ability_syringe" map to specific icon assets. | 3 | `ability_syringe`<br>`passive_syringe` |
| `max_health` | Integer | Sets a modifier to the unit's maximum health. A value of -1 might indicate no change or a default behavior. | 3 | `-1` |
| `reset_aux_on_store` | Integer | An integer flag that when set to 1, resets the item's auxiliary data when it is stored in the inventory. | 3 | `1` |
| `sticky` | Boolean | If true, the item cannot be unequipped or removed from the unit's slot under normal circumstances. | 3 | `true` |
| `weightless` | Boolean | If true, the item does not contribute to the unit's weight or encumbrance. | 3 | `true` |
| [`passive`](./Miscellaneous.md#object-passive) | Object | Defines the passive form, where the unit does nothing (uses DoNothing attack) and is inactive. | 2 | `{ . . . }` |
| `prevent_level_up` | Boolean | If true, the cat cannot gain experience or level up. | 2 | `true` |
| [`quest_item_alias`](./Enums.md#enum-quest_item_alias) | Enum | Specifies the main quest item key that this glowing variant is an alias of. The value is the identifier of the base quest item. | 2 | `BlackShard`<br>`NuclearKnife` |
| [`str_aux_is_copy_ability`](./Miscellaneous.md#object-str_aux_is_copy_ability) | Object | An object defining bonus passives and ability modifications for an auxiliary ability that is copied. | 2 | `{ . . . }` |
| `str_aux_is_copy_item_passive` | Boolean | If true, the item's str_aux field can be copied as a passive when applied to another item. | 2 | `true` |
| [`Set`](./Enums.md#enum-set) | Enum | Specifies the item set name that this item belongs to. | 1 | `Monk` |
| `aux_is_catid` | Boolean | If true, the item's auxiliary data stores or uses a cat identifier for spawning or duplication purposes. | 1 | `true` |
| `cant_equip_to_colorless` | Boolean | If true, the item cannot be equipped on a unit that has no color (i.e., is a colorless cat). | 1 | `true` |
| `degrade_after_adventure` | Boolean | If false, the item does not lose durability or quality after completing an adventure. | 1 | `false` |
| [`equip_sound`](./Enums.md#enum-equip_sound) | Enum | Specifies the sound effect played when the item is equipped. The value is a sound ID string like "SE_CatWeaponPoke_Chainsaw". | 1 | `SE_CatWeaponPoke_Chainsaw` |
| `force_sticky` | Boolean | If true, the item is forced to be sticky, overriding any other unequip conditions. | 1 | `true` |
| [`reset_str_aux_on_store`](./Enums.md#enum-reset_str_aux_on_store) | Enum | Specifies the default string identifier to reset the item's str_aux to when it is stored. | 1 | `ModelingClay_Default` |
| [`str_aux`](./Enums.md#enum-str_aux) | Enum | A string identifier that stores the item's current auxiliary data, such as "ModelingClay_Default". | 1 | `ModelingClay_Default` |
| `str_aux_is_copy_item_active` | Boolean | If true, the item's str_aux field can be copied as an active ability when applied to another item. | 1 | `true` |
| `str_aux_is_copy_item_icon` | Boolean | If true, the item's str_aux field can be copied as the icon when applied to another item. | 1 | `true` |

</details>


---


### Object: `passives`


**Definition:** A container object listing passive effects granted to the unit.
**Total Count:** 748

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveAfterXKills`](./Items_and_Equipment.md#context-passiveafterxkills), [`PassiveAtHealthThreshold`](./Items_and_Equipment.md#context-passiveathealththreshold), [`PassiveAtStatThreshold`](./Items_and_Equipment.md#context-passiveatstatthreshold), [`PassiveIfStrAuxEquals`](./Items_and_Equipment.md#context-passiveifstrauxequals), [`PassiveWhenAffectedByElement`](./Items_and_Equipment.md#context-passivewhenaffectedbyelement), [`PassiveWhenOnTile`](./Items_and_Equipment.md#context-passivewhenontile), [`ROOT`](./Items_and_Equipment.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2628 | passives<br>class<br>	ag |
| [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#object-addstatustobasicattack) | Object  | Contains status effects to add to the basic attack. | 133 | `{ . . . }` |
| [`Brace`](./Enums.md) | Array / Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 94 | `1`<br>`10`<br>`2` |
| [`Metal`](./Enums.md) | Integer | The number of armor stacks or metal keyword effects. | 90 | `1` |
| [`Trample`](./Enums.md) | Integer | The amount of bonus damage dealt when moving through an enemy. | 88 | `1`<br>`3`<br>`4` |
| [`Thorns`](./Enums.md) | Integer | The amount of thorns damage dealt to attackers on hit. | 65 | `1`<br>`2`<br>`3` |
| [`MeleeRevengeDamage`](./Passives_and_Statuses.md#object-meleerevengedamage) | Object  | Defines the damage and effects applied back to a melee attacker upon being hit. | 59 | `{ . . . }` |
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 52 | `1`<br>`2`<br>`3` |
| [`StatusEachTurnEnd`](./Passives_and_Statuses.md#object-statuseachturnend) | Object  | Specifies status effects applied to the unit at the end of each of its turns. | 49 | `{ . . . }` |
| [`StatusOnBattleEnd`](./Passives_and_Statuses.md#object-statusonbattleend) | Object  | An object containing status effects or passives applied to the unit when the battle ends. | 45 | `{ . . . }` |
| [`ElementImmune`](./Enums.md#enum-elementimmune) | Enum  | Specifies an element type (e.g., Fire, Ice) that the unit is immune to damage from. | 39 | `Creep`<br>`Electric`<br>`Fire` |
| [`SpawnOnBattleStart`](./Passives_and_Statuses.md#object-spawnonbattlestart) | Enum / Object  | Specifies the object that spawns adjacent to the unit at the start of battle. | 36 | `{ . . . }`<br>`BeefyCharmedLeech`<br>`BuffCharmedKitten`<br>`CharmedCultist` |
| [`DeathRattle`](./Enums.md#enum-deathrattle) | Enum  | Specifies an ability or effect triggered when the unit dies, optionally with a pop_corpse flag. | 35 | `BBExplode`<br>`BloatyExplodey`<br>`BombFlyExplode` |
| [`CounterAttack`](./Passives_and_Statuses.md#object-counterattack) | Object  | Specifies the ability used when the unit counterattacks after being hit. | 34 | `{ . . . }` |
| [`StatusImmunity`](./Arrays.md#array-statusimmunity) | Array / Enum  | A list of status effect names the unit is immune to. | 34 | `Burn`<br>`Poison`<br>`Tarred` |
| [`StatusOnKill`](./Passives_and_Statuses.md#object-statusonkill) | Object  | Specifies status effects or actions triggered when the unit kills an enemy. | 29 | `{ . . . }` |
| [`StatusOnTookDamage`](./Passives_and_Statuses.md#object-statusontookdamage) | Object  | Specifies status effects or actions triggered when the unit takes damage. | 29 | `{ . . . }` |
| [`SpawnThingOnDamage`](./Passives_and_Statuses.md#object-spawnthingondamage) | Object  | Specifies an object that spawns on the tile when the unit takes damage. | 28 | `{ . . . }` |
| [`Undead`](./Enums.md) | Integer | If set, flags the unit as undead (e.g., 1) with associated mechanics. | 25 | `1` |
| [`Brittle`](./Enums.md) | Integer | The number of stacks of the Brittle status, or an object defining its properties. | 24 | `1` |
| [`AbilityReaction`](./Enums.md#enum-abilityreaction) | Enum  | Specifies the ability used as a reaction when the unit is targeted by an ability. | 23 | `AnkyloSpin`<br>`GSOpen`<br>`Gassy_AssBlast` |
| [`Fragile`](./Enums.md) | Integer | The number of stacks of the Fragile status, causing increased damage taken. | 22 | `1` |
| [`StatusOnBreak`](./Passives_and_Statuses.md#object-statusonbreak) | Object | An object defining statuses or effects applied when an item or object breaks. | 22 | `{ . . . }` |
| [`AddPassivesToMinions`](./Passives_and_Statuses.md#object-addpassivestominions) | Object | An object containing passives that are granted to all minions spawned by the unit. | 21 | `{ . . . }` |
| [`DamageUp`](./Enums.md) | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 21 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`SpawnOnDeath`](./Passives_and_Statuses.md#object-spawnondeath) | Object  | Specifies an object and its faction to spawn when the unit dies. | 21 | `{ . . . }` |
| [`ArmorDodgeChance`](./Enums.md) | Integer | The percentage chance to dodge incoming attacks when wearing this armor. | 19 | `10%`<br>`15%`<br>`20%` |
| [`StatusEachTurnBegin`](./Passives_and_Statuses.md#object-statuseachturnbegin) | Object  | Specifies status effects applied to the unit at the start of each of its turns. | 18 | `{ . . . }` |
| [`CritChanceUp`](./Enums.md) | Integer | The amount of critical hit chance added as a flat percentage. | 16 | `1`<br>`10`<br>`100` |
| [`AddBonusRange`](./Enums.md) | Integer | The number of additional tiles of range added to the unit's abilities. | 15 | `1`<br>`10`<br>`2` |
| [`KineticSpikes`](./Enums.md) | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 15 | `1`<br>`2`<br>`3` |
| [`RevengeDamage`](./Passives_and_Statuses.md#object-revengedamage) | Object  | An object defining the damage and effects that trigger when the unit is attacked. | 15 | `{ . . . }` |
| [`SpawnEachTurn`](./Passives_and_Statuses.md#object-spawneachturn) | Object  | Specifies an object that spawns on a random adjacent tile each turn, with optional chance. | 15 | `{ . . . }` |
| [`StatusOnBattleStart`](./Passives_and_Statuses.md#object-statusonbattlestart) | Object | An object containing status effects to apply to the unit at the start of every battle. | 15 | `{ . . . }` |
| [`AddCorpseHealth`](./Enums.md) | Integer | The amount of bonus health the unit's corpse has before it can be resurrected. | 14 | `-999`<br>`-999999`<br>`100` |
| [`AllStatsUp`](./Enums.md) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 14 | `-1`<br>`-2`<br>`1` |
| [`DodgeChance`](./Enums.md) | Integer | The percentage chance the unit has to dodge incoming attacks. | 14 | `10%`<br>`15%`<br>`2%` |
| [`InnateElement`](./Enums.md#enum-innateelement) | Enum  | Specifies the innate elemental type of the unit (e.g., Fire, Ice, Electric). | 14 | `Earth`<br>`Electric`<br>`Fire` |
| [`AddManaRegen`](./Enums.md) | Integer | The flat amount of mana regenerated per turn. | 13 | `1`<br>`2`<br>`3` |
| [`DeathRattleRevive`](./Enums.md#enum-deathrattlerevive) | Enum  | Specifies an ability or effect that revives the unit upon death, with options for stunning behavior. | 13 | `DoNothing`<br>`HCHumanDie`<br>`ToxPuff` |
| [`Flammable`](./Enums.md) | Integer | The number of stacks of Flammable, or an object defining its properties. | 13 | `1`<br>`2` |
| [`AbilityHealthThreshold`](./Passives_and_Statuses.md#object-abilityhealththreshold) | Object  | Defines an ability and conditions for its activation when the unit's health reaches a threshold. | 12 | `{ . . . }` |
| [`ReflectProjectiles`](./Enums.md) | Integer | The percentage chance to reflect projectiles back at the attacker; optionally includes self-damage. | 12 | `1`<br>`10%`<br>`100%` |
| [`SpawnThingOnDeath`](./Enums.md#enum-spawnthingondeath) | Enum  | Specifies the name of an object to spawn upon death. | 12 | `Boulder`<br>`CharmedDemonKitten`<br>`CharmedFlySwarm` |
| [`AbilityOnBattleStart`](./Enums.md#enum-abilityonbattlestart) | Enum | Casts the specified ability when the battle begins. | 11 | `Flush`<br>`Heathens`<br>`Heathens2` |
| [`AddStatusToAllDamage`](./Passives_and_Statuses.md#object-addstatustoalldamage) | Object | Adds the contained status effects to all damage dealt by the unit. | 11 | `{ . . . }` |
| [`BleedThorns`](./Enums.md) | Integer | The amount of bleed thorns damage dealt to attackers on hit. | 11 | `1`<br>`2`<br>`3` |
| [`ExtraBasicAttacks`](./Enums.md) | Integer | The number of additional basic attacks the unit can perform per turn. | 11 | `1`<br>`2` |
| [`ReplaceBasicMove`](./Enums.md#enum-replacebasicmove) | Enum  | Specifies an alternative movement ability that replaces the unit's default move. | 11 | `BasicDashAttackMove`<br>`BasicJump`<br>`BellyFlop_BasicMove` |
| [`AddLevelUpRerolls`](./Enums.md) | Integer | The number of additional rerolls the unit gets when leveling up. | 10 | `1`<br>`2`<br>`3` |
| [`MoveTowardsDamageSource`](./Enums.md#enum-movetowardsdamagesource) | Enum  | Determines the movement behavior when moving towards the unit that dealt damage to it. | 10 | `MoveOne` |
| [`StatusOnKillEnemy`](./Passives_and_Statuses.md#object-statusonkillenemy) | Object | Specifies the effects applied when the unit kills an enemy. | 10 | `{ . . . }` |
| [`AddSelfStatusToBasicAttack`](./Passives_and_Statuses.md#object-addselfstatustobasicattack) | Object | Applies the contained status effects to the unit when it uses its basic attack. | 9 | `{ . . . }` |
| [`AddTag`](./Enums.md#enum-addtag) | Enum  | Specifies a gameplay tag (e.g., 'rock', 'plant') to add to the unit, used for interaction checks. | 9 | `bug`<br>`cat`<br>`fetus` |
| [`Bruise`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 9 | `1`<br>`2`<br>`3` |
| [`DepressionAura`](./Enums.md) | Integer | The number of stacks of Depression status applied to nearby enemies each turn; can be an object with range and ally settings. | 9 | `1`<br>`2` |
| [`Flying`](./Enums.md) | Integer | If set to 1, grants the unit the Flying passive, allowing movement over obstacles and ignoring terrain penalties. | 9 | `1` |
| [`MissChance`](./Enums.md) | Integer | The flat percentage chance that the unit's attacks will miss. | 9 | `10`<br>`15`<br>`20` |
| [`MovementReaction`](./Passives_and_Statuses.md#object-movementreaction) | Object  | Specifies an ability to cast when a unit moves within range, with options for targeting and conditions. | 9 | `{ . . . }` |
| [`PoisonThorns`](./Enums.md) | Integer | The number of stacks of Poison applied to melee attackers when they hit this unit. | 9 | `1`<br>`2`<br>`3` |
| [`StatusAlliesOnBattleStart`](./Passives_and_Statuses.md#object-statusalliesonbattlestart) | Object | An object containing status effects to apply to all allies at the start of battle. | 9 | `{ . . . }` |
| [`TrinketPassiveMultiplierBonus`](./Enums.md) | Integer | Bonus multiplier to the passive effects of equipped trinkets. | 9 | `1`<br>`2` |
| [`BoostHeals`](./Enums.md) | Integer | The number of stacks that increase healing received or dealt. | 8 | `-2`<br>`1`<br>`2` |
| [`ChanceToRevive`](./Passives_and_Statuses.md#object-chancetorevive) | Integer / Object | The percentage chance or an object defining chance, health, and statuses on revival. | 8 | `{ . . . }`<br>`100`<br>`25` |
| [`PermanentMadness`](./Enums.md) | Integer | The number of permanent madness stacks applied. | 8 | `1` |
| [`StatusOnDie`](./Passives_and_Statuses.md#object-statusondie) | Object  | Specifies status effects or actions triggered when the unit dies. | 8 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 8 | `Default`<br>`FormChange`<br>`Druid` | [`AddElementsToBasicAttack`](./Enums.md) | Enum | Specifies an elemental damage type that is added to the unit's basic attacks. | 174 | Default<br>FormChange<br>Druid |
| [`AddInitiative`](./Enums.md) | Integer | The amount of bonus or penalty to the unit's turn order initiative value. | 7 | `-10`<br>`-100`<br>`-20` |
| [`AlphaTurns`](./Enums.md) | Integer | The number of turns the unit acts first in battle; negative values may indicate last. | 7 | `-1`<br>`1` |
| [`Bleed`](./Enums.md) | Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 7 | `1`<br>`10`<br>`2` |
| [`BonusAbility`](./Enums.md#enum-bonusability) | Enum  | Specifies the name of a bonus ability granted. | 7 | `Bloodzerk`<br>`BonusToss`<br>`BonusToss2` |
| [`BrittleDuringElement`](./Enums.md#enum-brittleduringelement) | Enum | Makes the unit brittle while in contact with the specified element. | 7 | `water` |
| [`DebuffImmunity`](./Enums.md) | Integer | If 1, the unit is immune to debuffs. | 7 | `1` |
| [`DurabilityTransform`](./Passives_and_Statuses.md#object-durabilitytransform) | Object | Transforms the item into another when durability reaches specified thresholds. | 7 | `{ . . . }` |
| [`ManaCostReduction`](./Enums.md) | Integer | The amount or percentage by which ability mana costs are reduced for this unit. | 7 | `-2`<br>`1`<br>`2` |
| [`OverrideBasicAttack`](./Enums.md#enum-overridebasicattack) | Enum | Replaces the unit's basic attack with the specified ability. | 7 | `BasicExplosiveShot`<br>`BasicMelee`<br>`BasicMetronome` |
| [`PassiveAtHealthThreshold`](./Passives_and_Statuses.md#object-passiveathealththreshold) | Object | An object that grants additional passives when the unit's health meets a specified threshold, with sub-keys for threshold, mode, and passives. | 7 | `{ . . . }` |
| [`PassiveAtStatThreshold`](./Passives_and_Statuses.md#object-passiveatstatthreshold) | Object | An object defining passives granted when a unit's stat meets a specified threshold. | 7 | `{ . . . }` |
| [`SetFragileImmune`](./Enums.md) | Variable | Sets the unit's material to the specified type, granting immunity to the Fragile status. | 7 | `""`<br>`Bionic`<br>`Cardboard` |
| [`SetSpellCosts`](./Enums.md) | Integer | Overrides the cost of all spells to this value. | 7 | `0`<br>`1`<br>`3` |
| [`StatusOnEndMove`](./Passives_and_Statuses.md#object-statusonendmove) | Object  | Specifies status effects or actions triggered when the unit finishes moving. | 7 | `{ . . . }` |
| [`AddDamageToElementDamage`](./Passives_and_Statuses.md#object-adddamagetoelementdamage) | Object  | Defines additional damage of a specific element added to the unit's attacks. | 6 | `{ . . . }` |
| [`AmplifyStatus`](./Enums.md#enum-amplifystatus) | Enum | Specifies the status effect to amplify, or an object with the status and number of stacks to add. | 6 | `Bleed`<br>`Burn`<br>`Poison` |
| [`DelayedAutoRevive`](./Passives_and_Statuses.md#object-delayedautorevive) | Object  | Configures an automatic revival after a delay, with specified rounds and health percentage. | 6 | `{ . . . }` |
| [`DodgeChance_Status`](./Enums.md) | Integer | The flat percentage increase to dodge chance applied as a status effect. | 6 | `1`<br>`10`<br>`100` |
| [`ExtraWeaponAttacks`](./Enums.md) | Integer | The number of additional weapon attacks the unit can perform. | 6 | `1`<br>`2` |
| [`IgnoreTiles`](./Enums.md) | Integer | If set to 1, movement ignores tile-based penalties or restrictions. | 6 | `1` |
| [`ItemAuxTransform`](./Passives_and_Statuses.md#object-itemauxtransform) | Object | Transforms the item into another when its auxiliary value reaches specified thresholds. | 6 | `{ . . . }` |
| [`PassiveWhenOnTile`](./Passives_and_Statuses.md#object-passivewhenontile) | Object | Grants the contained passive effects while the unit is standing on one of the specified tile types. | 6 | `{ . . . }` |
| [`Poison`](./Enums.md) | Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 6 | `1`<br>`10`<br>`2` |
| [`Quivered`](./Arrays.md#array-quivered) | Array / Integer  | The amount of quivered stacks applied, or an [stacks, probability] array. | 6 | `1`<br>`2`<br>`5` |
| [`ReplaceBasicAttack`](./Enums.md#enum-replacebasicattack) | Enum  | Specifies the ability ID that replaces the unit's basic attack. | 6 | `BasicButcherMeleeWideDoubleSpin`<br>`BasicButcherMeleeWideSpin`<br>`BasicDruidAbilityVersatile` |
| [`SetBrittleImmune`](./Enums.md) | Variable | Sets the unit's material to the specified type, granting immunity to the Brittle status. | 6 | `""`<br>`AdvancedAlloy`<br>`Alloy` |
| [`SpawnOnBattleStartRandomEmptyTile`](./Passives_and_Statuses.md#object-spawnonbattlestartrandomemptytile) | Object  | Specifies an object that spawns on a random empty tile at the start of battle. | 6 | `{ . . . }` |
| [`AddBonusMeleeRange`](./Enums.md) | Integer | The number of additional tiles of range added to the unit's melee attacks. | 5 | `1`<br>`10`<br>`2` |
| [`AddHiddenTag`](./Enums.md#enum-addhiddentag) | Enum  | A hidden tag applied to the unit for internal logic and triggers. | 5 | `bowling_ball`<br>`grown_hitler_clone`<br>`hitler_clone_fetus` |
| [`BackstabCritChance`](./Enums.md) | Float | A multiplier for critical hit chance on backstab attacks. | 5 | `.25`<br>`1` |
| [`Burn`](./Enums.md) | Equation | The amount of Burn applied, either as a fixed number or a formula string. | 5 | `1`<br>`10`<br>`2` |
| [`ClassManaCostReduction`](./Passives_and_Statuses.md#object-classmanacostreduction) | Object  | Defines a reduction in mana cost for abilities of a specific class. | 5 | `{ . . . }` |
| [`CritsApplyStatus`](./Passives_and_Statuses.md#object-critsapplystatus) | Object | An object containing statuses applied to the target when the unit lands a critical hit. | 5 | `{ . . . }` |
| [`FaceShield`](./Enums.md) | Integer | If 1, the unit has a face shield that protects it from certain attacks or effects. | 5 | `0`<br>`1` |
| [`HeadArmorPassiveMultiplierBonus`](./Enums.md) | Integer | A multiplier bonus applied to passive effects granted by head armor. | 5 | `1`<br>`2` |
| [`InjuryImmunity`](./Enums.md) | Integer | The number of turns the unit is immune to injuries. | 5 | `1` |
| [`KnockbackImmunity`](./Enums.md) | Integer | If set to 1, the unit cannot be knocked back. | 5 | `1` |
| [`SharkySmellsBlood`](./Enums.md) | Integer | If 1, the unit is attracted to damaged units and may prioritize them. | 5 | `1` |
| [`SpellDamageUp`](./Enums.md) | Integer | The number of stacks of SpellDamageUp applied, increasing spell damage. | 5 | `1`<br>`3` |
| [`StatusIfUnusedMovePoints`](./Passives_and_Statuses.md#object-statusifunusedmovepoints) | Object  | Specifies status effects applied if the unit ends its turn with unused movement points. | 5 | `{ . . . }` |
| [`StatusOnTurnEndIfDidntCastAbilityTypes`](./Passives_and_Statuses.md#object-statusonturnendifdidntcastabilitytypes) | Object | Applies the contained status effects at turn end if the unit did not cast an ability of the specified type(s). | 5 | `{ . . . }` |
| [`TransformItemOnElementInfluence`](./Passives_and_Statuses.md#object-transformitemonelementinfluence) | Object | Transforms the item into the specified one when influenced by the given element, optionally fully repairing it. | 5 | `{ . . . }` |
| [`TrinketActiveEffectsMultiplierBonus`](./Enums.md) | Integer | Bonus multiplier to the active effects of equipped trinkets. | 5 | `1`<br>`2` |
| [`AddCritMultiplier`](./Enums.md) | Integer | The percentage added to the critical hit damage multiplier. | 4 | `100%`<br>`125%`<br>`150%` |
| [`AddKnockbackDamage`](./Enums.md) | Integer | The amount of additional knockback damage applied. | 4 | `1`<br>`2`<br>`3` |
| [`AddStatusToElementDamage`](./Passives_and_Statuses.md#object-addstatustoelementdamage) | Object | An object that applies a specific status effect when dealing damage of a specified element. Contains sub-keys for the element and the status to apply. | 4 | `{ . . . }` |
| [`AddStatusToWeapons`](./Passives_and_Statuses.md#object-addstatustoweapons) | Object  | Specifies status effects to add to the unit's weapon attacks, with their stack counts. | 4 | `{ . . . }` |
| [`AddTemporaryEffectsToBasicAttack`](./Passives_and_Statuses.md#object-addtemporaryeffectstobasicattack) | Object  | A container object that lists temporary status effects applied to the unit's basic attack. | 4 | `{ . . . }` |
| [`BoostWeaponDamage`](./Passives_and_Statuses.md#object-boostweapondamage) | Object  | The amount of bonus weapon damage applied, or an object with `damage` and `crit_chance` fields. | 4 | `{ . . . }` |
| [`BreakAtAux`](./Enums.md) | Integer | The number of auxiliary item uses before this item breaks. | 4 | `0` |
| [`BuffImmunity`](./Passives_and_Statuses.md#object-buffimmunity) | Object  | If 1, the unit is immune to buffs. An optional object can list buffs to exclude from immunity. | 4 | `{ . . . }` |
| [`CatchProjectiles`](./Passives_and_Statuses.md#object-catchprojectiles) | Object | An object defining chance to catch projectiles and optionally apply statuses. | 4 | `{ . . . }` |
| [`ChanceToBackflip`](./Passives_and_Statuses.md#object-chancetobackflip) | Object  | An object specifying the ability to use and the percentage chance to perform a backflip dodge when hit. | 4 | `{ . . . }` |
| [`ExtraStatusWhenDealingDamage`](./Passives_and_Statuses.md#object-extrastatuswhendealingdamage) | Object | Defines additional statuses applied to the target or source when dealing damage, with conditionals. | 4 | `{ . . . }` |
| [`FaceArmorPassiveMultiplierBonus`](./Enums.md) | Integer | A multiplier bonus applied to the effects of face armor passives. | 4 | `1`<br>`2` |
| [`FragileDuringElement`](./Enums.md#enum-fragileduringelement) | Enum | Specifies an element during which the unit becomes fragile, taking increased damage. | 4 | `water` |
| [`FreezePiercing`](./Enums.md) | Integer | The number of stacks of freeze resistance that are ignored when applying freeze. | 4 | `1` |
| [`IncreaseExplosionDamage`](./Enums.md) | Integer | The flat amount by which explosion damage is increased. | 4 | `1`<br>`2`<br>`3` |
| [`IncreaseExplosionSize`](./Enums.md) | Integer | The number of extra tiles added to the radius of explosions. | 4 | `1`<br>`2`<br>`7` |
| [`LevelUpClassOverride`](./Enums.md#enum-levelupclassoverride) | Enum | Specifies which class the unit gains upon leveling up, overriding the default class. | 4 | `Colorless`<br>`Jester` |
| [`MakeSpellsRequireCharge`](./Enums.md) | Integer | If true, spells require a charge-up turn before casting. | 4 | `1` |
| [`PassiveWhenAffectedByElement`](./Passives_and_Statuses.md#object-passivewhenaffectedbyelement) | Object  | An object containing `element` and `passives` that grants the listed passives while the unit is affected by the specified element. | 4 | `{ . . . }` |
| [`PassiveWhenDead`](./Passives_and_Statuses.md#object-passivewhendead) | Object  | Passive effects that remain active while the unit is dead. | 4 | `{ . . . }` |
| [`RandomSeededStatModifier`](./Arrays.md#array-randomseededstatmodifier) | Array | An array defining a random, seeded modifier to stats, typically in the format [modifier, offset]. | 4 | `[2 -1]` |
| [`StatusAlliesOnDeath`](./Passives_and_Statuses.md#object-statusalliesondeath) | Object | Applies the contained status effects to all allies when the unit dies. | 4 | `{ . . . }` |
| [`StatusEveryXSpellCasts`](./Passives_and_Statuses.md#object-statuseveryxspellcasts) | Object  | An object with `stacks` (number of spell casts) and status effects to apply after that many spell casts. | 4 | `{ . . . }` |
| [`StatusOnAllyCatDeath`](./Passives_and_Statuses.md#object-statusonallycatdeath) | Object  | An object listing status effects applied to the unit when an allied cat dies. | 4 | `{ . . . }` |
| [`StatusOnCastSpell`](./Passives_and_Statuses.md#object-statusoncastspell) | Object  | An object listing status effects applied to the unit whenever it casts a spell. | 4 | `{ . . . }` |
| [`StatusOnGainCoins`](./Passives_and_Statuses.md#object-statusongaincoins) | Object  | Specifies status effects applied when this unit gains coins. | 4 | `{ . . . }` |
| [`StatusOnPopCorpse`](./Passives_and_Statuses.md#object-statusonpopcorpse) | Object | Specifies the effects applied when the unit pops a corpse. | 4 | `{ . . . }` |
| [`StatusOnTakeHealthOrShieldDamage`](./Passives_and_Statuses.md#object-statusontakehealthorshielddamage) | Object | An object that applies a status effect when the unit takes damage to either health or shields. | 4 | `{ . . . }` |
| [`StatusRandomEnemiesOnBattleStart`](./Passives_and_Statuses.md#object-statusrandomenemiesonbattlestart) | Object | An object that applies a status effect to a random number of enemies at the start of battle, with sub-keys for count and the status. | 4 | `{ . . . }` |
| [`AddEndOfCombatRegen`](./Enums.md) | Integer | The amount of health regenerated after combat ends. | 3 | `12`<br>`999999` |
| [`AddPassivesToCharmed`](./Passives_and_Statuses.md#object-addpassivestocharmed) | Object | Grants the contained passive effects to units under the charm status. | 3 | `{ . . . }` |
| [`AddStatusToSpells`](./Passives_and_Statuses.md#object-addstatustospells) | Object  | Specifies status effects added to all spell attacks used by this unit. | 3 | `{ . . . }` |
| [`AllStatsUpPerDisorder`](./Enums.md) | Integer | The amount by which all stats increase for each disorder (negative status) the unit has. | 3 | `1` |
| [`AmplifyKnockback`](./Enums.md) | Integer | The additional distance (in tiles) a unit is knocked back. | 3 | `10`<br>`2` |
| [`ApplyStatusesToRandomEnemiesEachTurn`](./Passives_and_Statuses.md#object-applystatusestorandomenemieseachturn) | Object | An object specifying statuses to apply to random enemies each turn, with an optional 'count' field. | 3 | `{ . . . }` |
| [`AutoEquipConsumables`](./Enums.md) | Integer | The number of consumables automatically equipped per turn. | 3 | `1` |
| [`BasicAttackCritChance`](./Enums.md) | Float | A multiplier for the critical hit chance of basic attacks, either as a float or percentage. | 3 | `.1`<br>`100%` |
| [`BoneArmorPassive`](./Enums.md) | Integer | The number of stacks of bone armor granted, which absorbs damage. | 3 | `1` |
| [`BreakOnElement`](./Enums.md#enum-breakonelement) | Enum | Specifies an element that, when dealt to the unit, causes its armor or item to break. | 3 | `water` |
| [`CantCatchDiseases`](./Enums.md) | Integer | The number of stacks that prevent the unit from contracting diseases. | 3 | `1` |
| [`CantSpreadDiseases`](./Enums.md) | Integer | The number of stacks that prevent the unit from spreading diseases. | 3 | `1` |
| [`ChanceToBlock`](./Enums.md) | Integer | The percentage chance to block incoming damage. | 3 | `10%` |
| [`ChanceToBlockAndCounter`](./Passives_and_Statuses.md#object-chancetoblockandcounter) | Integer / Object | The percentage chance or an object defining chance and conditions to block and counter an attack. | 3 | `{ . . . }`<br>`15%`<br>`25%`<br>`33%` |
| [`Confusion`](./Enums.md) | Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 3 | `1`<br>`10`<br>`2` |
| [`DropAsFamiliarOnArmorBreak`](./Enums.md#enum-dropasfamiliaronarmorbreak) | Enum | Specifies the familiar type to drop onto the tile when this status holder's armor breaks. | 3 | `FaceGrubFamiliar`<br>`HeadGrubFamiliar`<br>`NeckGrubFamiliar` |
| [`ElementalManaCostReduction`](./Passives_and_Statuses.md#object-elementalmanacostreduction) | Object | An object that reduces the mana cost of spells of specified elements, with sub-keys for element and reduction amount. | 3 | `{ . . . }` |
| [`ExtraBasicMoves_Status`](./Enums.md) | Integer | The number of extra basic moves per turn granted. | 3 | `1` |
| [`ExtraMovePoints`](./Enums.md) | Integer | The number of additional movement points granted to this unit. | 3 | `1` |
| [`FlowersOnEndTurn`](./Enums.md) | Integer | The number of flowers spawned on the unit's tile at the end of each turn. | 3 | `1`<br>`3`<br>`4` |
| [`IncreaseSpellRange`](./Enums.md) | Integer | The number of extra tiles added to the range of spells. | 3 | `10`<br>`2`<br>`20` |
| [`KillsToMeat`](./Enums.md#enum-killstomeat) | Enum | Specifies the type of meat item spawned when killing certain enemies. | 3 | `Food` |
| [`LuckUp`](./Enums.md) | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 3 | `-1`<br>`-2`<br>`-4` |
| [`MoveAndUseAbilityEachTurnBeginIfPossible`](./Enums.md#enum-moveanduseabilityeachturnbeginifpossible) | Enum | Specifies the name of the ability the unit will move and attempt to use at the start of each of its turns. | 3 | `Cannibalize`<br>`EatShit`<br>`face_EatNeverstone` |
| [`MoveQuivered`](./Enums.md) | Float | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 3 | `1`<br>`2`<br>`[1, 0.1]` |
| [`NeckArmorPassiveMultiplierBonus`](./Enums.md) | Integer | A multiplier bonus applied to the passives of the unit's neck armor slot. | 3 | `1`<br>`2` |
| [`PassiveAfterXKills`](./Passives_and_Statuses.md#object-passiveafterxkills) | Object | Activates a set of passive effects (e.g., extra attacks, stat boosts) after the unit achieves a certain number of kills defined by the 'stacks' sub-key. | 3 | `{ . . . }` |
| [`RangedTrueShot`](./Enums.md) | Integer | Ranged attacks cannot miss or be dodged, guaranteeing a hit. Value acts as a binary flag. | 3 | `1` |
| [`ReplaceSpawnedObjects`](./Arrays.md#array-replacespawnedobjects) | Array | An array of [original_object replacement_object] pairs for swapping spawned objects. | 3 | `[Boulder AnimatedBoulder]`<br>`[Boulder AnimatedLavaBoulder]`<br>`[Crow Crow2]` |
| [`RockyArmorPassive`](./Enums.md) | Integer | The number of stacks of the Rocky Armor status effect granted. | 3 | `1` |
| [`SetDefaultFacePassive`](./Enums.md#enum-setdefaultfacepassive) | Enum | Specifies the name of the default face passive to be assigned to this unit. | 3 | `euphoric`<br>`insane` |
| [`SpawnExtraThingsOnBattleStart`](./Passives_and_Statuses.md#object-spawnextrathingsonbattlestart) | Object  | An object with `object` and `number` (or range) defining what and how many objects to spawn at battle start. | 3 | `{ . . . }` |
| [`SpawnObjectOnPopCorpse`](./Passives_and_Statuses.md#object-spawnobjectonpopcorpse) | Enum / Object | Specifies an object (as a string or an object with 'object', 'count', 'except_tiny' keys) to spawn on a corpse when it is popped. | 3 | `{ . . . }`<br>`Catnip`<br>`Coin`<br>`Food` |
| [`StackingFlowerTrail`](./Passives_and_Statuses.md#object-stackingflowertrail) | Object | An object defining how a flower trail status stacks (stacks count, stack key) when the unit moves. | 3 | `{ . . . }` |
| [`StatusAfterCastSpell`](./Passives_and_Statuses.md#object-statusaftercastspell) | Object | An object containing status effects to apply to the unit immediately after it casts any spell. | 3 | `{ . . . }` |
| [`StatusAllCharactersOnSpawn`](./Passives_and_Statuses.md#object-statusallcharactersonspawn) | Object  | Defines status effects applied to all characters when they spawn into the battlefield. | 3 | `{ . . . }` |
| [`StatusOnBreakItem`](./Passives_and_Statuses.md#object-statusonbreakitem) | Object | An object containing status effects to apply when the unit breaks a weapon or armor item. | 3 | `{ . . . }` |
| [`StatusOnEatFood`](./Passives_and_Statuses.md#object-statusoneatfood) | Object  | An object listing status effects applied to the unit when it eats food. | 3 | `{ . . . }` |
| [`TrueShot`](./Enums.md) | Integer | The number of stacks of a buff that makes the unit's attacks unmissable. | 3 | `1` |
| [`AddSelfStatusToWeapons`](./Passives_and_Statuses.md#object-addselfstatustoweapons) | Object | An object whose nested keys define status effects applied to the unit's own weapons. | 2 | `{ . . . }` |
| [`AddStatusToKnockbackDamage`](./Passives_and_Statuses.md#object-addstatustoknockbackdamage) | Object | An object whose nested keys define statuses applied to damage caused by knockback. | 2 | `{ . . . }` |
| [`AllyDamageReduction`](./Enums.md) | Integer | The amount by which damage dealt to allies is reduced. | 2 | `0` |
| [`ArmorBreakOnHit`](./Passives_and_Statuses.md#object-armorbreakonhit) | Object | An object defining durability loss and chance for armor to break when hit. | 2 | `{ . . . }` |
| [`BouncyProjectiles`](./Passives_and_Statuses.md#object-bouncyprojectiles) | Object | An object with 'max_bounces' and 'max_range' defining projectile bounciness behavior. | 2 | `{ . . . }` |
| [`BreakWhenNoShield`](./Enums.md) | Integer | If 1, the armor breaks when the unit has no shield remaining. | 2 | `1` |
| [`CanLevelUpWhenDead`](./Enums.md) | Integer | If 1, allows the unit to gain experience and level up while dead. | 2 | `1` |
| [`CanRemoveCursedItems`](./Enums.md) | Integer | If nonzero, allows the unit to remove cursed items from equipment slots. | 2 | `1` |
| [`CapMovementAbilityRange`](./Enums.md) | Integer | The maximum range allowed for movement abilities. | 2 | `1` |
| [`ConsumableEffectsMultiplierBonus`](./Enums.md) | Integer | A multiplier bonus applied to the effects of consumable items. | 2 | `1` |
| [`CopyPassiveSlot`](./Enums.md) | Integer | An index (0-based) specifying which equipment slot's passive to copy onto this unit. | 2 | `0`<br>`1` |
| [`CreateGlobalModifiers`](./Passives_and_Statuses.md#object-createglobalmodifiers) | Object  | Defines global gameplay modifiers to activate. | 2 | `{ . . . }` |
| [`DisableAbilities`](./Enums.md#enum-disableabilities) | Enum | Specifies which category of abilities to disable, such as 'all_items' or 'basic_attack'. | 2 | `all_items`<br>`all_spells`<br>`basic_attack` |
| [`DoubleCastWeapons`](./Enums.md) | Integer | The number of additional weapon casts per attack. | 2 | `1`<br>`2` |
| [`Eternal`](./Passives_and_Statuses.md#object-eternal) | Object | Defines the Eternal revival effect, setting stacks and the health percentage restored. | 2 | `{ . . . }` |
| [`FindExtraItemFromPoolOnBattleEnd`](./Enums.md#enum-findextraitemfrompoolonbattleend) | Enum  | Specifies the item pool from which an extra item is granted at the end of combat. | 2 | `combat_reward_easy`<br>`pills` |
| [`FlyDamageIncrease`](./Passives_and_Statuses.md#object-flydamageincrease) | Object | The number of stacks or alias for damage increase against flying units. | 2 | `{ . . . }` |
| [`GainExtraShield`](./Enums.md) | Integer | The amount of shield gained on turn start. | 2 | `2`<br>`4` |
| [`HPGainBlock`](./Enums.md) | Integer | If true, the unit cannot gain health from any source. | 2 | `1` |
| [`LeaveBehindOnceEachMove`](./Enums.md#enum-leavebehindonceeachmove) | Enum | Specifies the object left behind on the tile once per move. | 2 | `Poop`<br>`Scrap` |
| [`MoveSpeedMultiplier`](./Enums.md) | Float | A multiplier for the unit's movement speed. | 2 | `.5` |
| [`PassiveIfWeaponIsUsable`](./Passives_and_Statuses.md#object-passiveifweaponisusable) | Object | Activates a set of passive effects (e.g., Brace) only if the unit's current weapon is in a usable condition (not broken or disabled). | 2 | `{ . . . }` |
| [`PassiveWhileInMonkMeleeStance`](./Passives_and_Statuses.md#object-passivewhileinmonkmeleestance) | Object | Applies specific passive effects (e.g., Brace, HealthRegenUp) while the unit is in the Monk's melee combat stance. | 2 | `{ . . . }` |
| [`PoopWhenHit`](./Passives_and_Statuses.md#object-poopwhenhit) | Object  | Specifies the object (e.g., Poop) spawned when the unit is hit, or an object with `chance` and `object`. | 2 | `{ . . . }` |
| [`RefreshEquipmentAbilityOnElement`](./Passives_and_Statuses.md#object-refreshequipmentabilityonelement) | Object | Refreshes the cooldown of the unit's equipment ability when the unit's attack matches the specified element (e.g., Electric), displaying a recharge popup. | 2 | `{ . . . }` |
| [`RemoveLineOfSightRestrictions`](./Enums.md) | Integer | Line of sight requirements for targeting are ignored, allowing the unit to target any visible cell regardless of obstacles. | 2 | `1` |
| [`ScaledStatusOnSpendMana`](./Passives_and_Statuses.md#object-scaledstatusonspendmana) | Object | An object containing status effect definitions to apply when the unit spends mana, with the number of stacks scaled by the amount of mana spent. | 2 | `{ . . . }` |
| [`SpawnItemLinkedFamiliar`](./Passives_and_Statuses.md#object-spawnitemlinkedfamiliar) | Object | An object defining a familiar to spawn that is linked to a specific item, which breaks when the familiar is defeated. | 2 | `{ . . . }` |
| [`SpawnNearEnemies`](./Enums.md) | Integer | The number of units to spawn near each enemy at the start of battle. | 2 | `1` |
| [`StatusAfterXTurns`](./Passives_and_Statuses.md#object-statusafterxturns) | Object  | Applies a status effect or forces an ability usage after a set number of turns. | 2 | `{ . . . }` |
| [`StatusEachTurnEndForEachTurn`](./Passives_and_Statuses.md#object-statuseachturnendforeachturn) | Object  | Statuses applied at the end of each turn, with the number of turns as nested values. | 2 | `{ . . . }` |
| [`StatusIfUnusedActPoints`](./Passives_and_Statuses.md#object-statusifunusedactpoints) | Object | An object containing status effects to apply to the unit if it has unused action points at the end of its turn. | 2 | `{ . . . }` |
| [`StatusOnBackstab`](./Passives_and_Statuses.md#object-statusonbackstab) | Object | An object containing status effects to apply when the unit performs a backstab attack. | 2 | `{ . . . }` |
| [`StatusOnCollectPickup`](./Passives_and_Statuses.md#object-statusoncollectpickup) | Object | An object containing status effects to apply when the unit collects a pickup item. | 2 | `{ . . . }` |
| [`StatusOnHealed`](./Passives_and_Statuses.md#object-statusonhealed) | Object | An object that applies a status effect to the unit whenever it is healed. | 2 | `{ . . . }` |
| [`StatusOnPickupCoins`](./Passives_and_Statuses.md#object-statusonpickupcoins) | Object | Specifies the effects applied when the unit picks up coins. | 2 | `{ . . . }` |
| [`StatusOnUseBasicAttack`](./Passives_and_Statuses.md#object-statusonusebasicattack) | Object | Specifies the effects applied when the unit performs a basic attack. | 2 | `{ . . . }` |
| [`StatusWhenAllySpendsMana`](./Passives_and_Statuses.md#object-statuswhenallyspendsmana) | Object | Specifies the effects applied when an ally spends mana. | 2 | `{ . . . }` |
| [`TauntAlways`](./Enums.md) | Integer | If non-zero, the unit is always taunted, forcing it to target the first enemy in range. | 2 | `1` |
| [`Uncontrollable`](./Enums.md) | Integer | If non-zero, the unit becomes uncontrollable by the player. | 2 | `1` |
| [`WeaponDamageMultiplierBonus`](./Enums.md) | Integer | Bonus multiplier to weapon damage. | 2 | `1`<br>`2` |
| [`AIControlNextTurn`](./Passives_and_Statuses.md#object-aicontrolnextturn) | Object | An object that causes the unit to be controlled by the AI on its next turn, with configurable stacks and spell usage. | 1 | `{ . . . }` |
| [`AOEBonus`](./Enums.md) | Integer | The bonus number of additional targets or tiles affected by an area-of-effect ability. | 1 | `1` |
| [`AbilityOnRoundEndOnce`](./Passives_and_Statuses.md#object-abilityonroundendonce) | Object | Specifies an ability to be used once at the end of the round. | 1 | `{ . . . }` |
| [`AddAdvantageToEvent`](./Passives_and_Statuses.md#object-addadvantagetoevent) | Object | Specifies additional advantage options to add to a specific event type. | 1 | `{ . . . }` |
| [`AddStatusToBackstabs`](./Passives_and_Statuses.md#object-addstatustobackstabs) | Object | An object defining statuses applied to the target when the unit performs a backstab attack. | 1 | `{ . . . }` |
| [`AllSpellsCostCharge`](./Enums.md) | Integer | The number of charges required to cast any spell, adding a universal charge cost. | 1 | `1` |
| [`AllUnitsExplodeOnDeath`](./Enums.md) | Integer | The radius of the explosion that triggers when any unit dies. | 1 | `5` |
| [`AlliesScrambleSpellAfterCast`](./Enums.md) | Integer | The number of times an ally's next spell cast will be scrambled (randomly redirected or modified) after the owner casts a spell. | 1 | `1` |
| [`AlluringDoodieEater`](./Passives_and_Statuses.md#object-alluringdoodieeater) | Object | An object defining the chance and damage instance for a unit that consumes an alluring doodie. | 1 | `{ . . . }` |
| [`AllyDodgeChanceAura`](./Passives_and_Statuses.md#object-allydodgechanceaura) | Object | An object granting allies within a specified range a percentage chance to dodge incoming attacks. | 1 | `{ . . . }` |
| [`AlphaAllStatsUp`](./Enums.md) | Integer | The amount by which all of the unit's stats are increased if it is the alpha (highest stat total or designated leader). | 1 | `1` |
| [`AlphaCat`](./Enums.md) | Integer | The number of AlphaCat stacks applied to the source on kill. | 1 | `1` |
| [`AlwaysChosenForLevelUp`](./Enums.md) | Integer | If set to 1, this unit is always presented as a level-up option when gaining a level. | 1 | `1` |
| [`BackflipWhenTargeted`](./Passives_and_Statuses.md#object-backflipwhentargeted) | Enum / Object  | The number of backflip charges, or an object defining its ability. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`X` |
| [`BalanceStats`](./Enums.md) | Integer | If set to 1, the unit's stats are balanced (redistributed) towards an average value. | 1 | `1` |
| [`BasicAttackCantMiss`](./Enums.md) | Integer | If nonzero, the unit's basic attack cannot miss. | 1 | `1` |
| [`Blind`](./Enums.md) | Integer | The amount of blind stacks applied, or an [stacks, probability] array. | 1 | `-1`<br>`1`<br>`2` |
| [`BlockDamageUnderThreshold`](./Enums.md) | Integer | The maximum amount of damage from a single hit that will be completely blocked. | 1 | `1` |
| [`BlockNegativeStatus`](./Enums.md) | Integer | The percentage chance to completely block the application of a negative status effect. | 1 | `30%` |
| [`BoostReceivedHealing`](./Enums.md) | Integer | The amount of bonus healing received from all sources. | 1 | `2` |
| [`CapBasicAttackDamage`](./Enums.md) | Integer | The maximum amount of damage that can be dealt by a basic attack. | 1 | `1` |
| [`CatPartsSizeScale`](./Passives_and_Statuses.md#object-catpartssizescale) | Object | A multiplier for the size of specific cat parts (e.g., head, body). | 1 | `{ . . . }` |
| [`ChanceToAmbush`](./Enums.md) | Integer | The percentage chance for the unit to ambush an enemy. | 1 | `25%` |
| [`ChanceToForceEvent`](./Passives_and_Statuses.md#object-chancetoforceevent) | Object | Defines the chance and the specific event to force to occur. | 1 | `{ . . . }` |
| [`Charge`](./Enums.md) | Equation | The number of charge stacks applied. | 1 | `1`<br>`2`<br>`3` |
| [`CharismaIsMaxStat`](./Enums.md) | Integer | Treats the Charisma stat as the character's maximum stat for calculations. | 1 | `1` |
| [`CharmImmunity`](./Enums.md) | Integer | If true, the unit is immune to the Charmed status effect. | 1 | `1` |
| [`ConvertDamageToScaledStatus`](./Passives_and_Statuses.md#object-convertdamagetoscaledstatus) | Object | Converts a portion of incoming damage into a specified status effect with a given number of stacks. | 1 | `{ . . . }` |
| [`CounterNextAttacks`](./Enums.md) | Integer | The number of incoming attacks the unit will counterattack. | 1 | `2` |
| [`DisablePassiveSlot`](./Enums.md) | Integer | If non-zero, disables the specified passive slot index (0 or 1). | 1 | `0`<br>`1` |
| [`DoubleCastSpellIfManaCostUnderThreshold`](./Enums.md) | Integer | If a spell's mana cost is under this threshold, it will be cast twice. | 1 | `3` |
| [`DoubleCastTaggedSpells`](./Enums.md#enum-doublecasttaggedspells) | Enum | Specifies the spell tag (e.g., musical) that causes spells to be cast twice. | 1 | `musical` |
| [`DoubleReceivedNegativeStatus`](./Enums.md) | Integer | If true, the unit receives double the stacks of negative status effects applied to it. | 1 | `1` |
| [`DoubleReceivedPositiveStatus`](./Enums.md) | Integer | If true, the unit receives double the stacks of positive status effects applied to it. | 1 | `1` |
| [`DropAsFamiliarOnTookDamage`](./Enums.md#enum-dropasfamiliarontookdamage) | Enum | Specifies the familiar type to be dropped when the unit takes damage. | 1 | `PhantomMaskRock` |
| [`DropSoulJarOnDeath`](./Enums.md#enum-dropsouljarondeath) | Enum | Specifies the type of soul jar to be dropped when the unit dies. | 1 | `SoulJar_Full` |
| [`ExcludeFromEvents`](./Enums.md#enum-excludefromevents) | Enum | Specifies the event type (e.g., Tragedy) that this unit is excluded from participating in. | 1 | `Tragedy` |
| [`ExplosionImmunity`](./Enums.md) | Integer | If non-zero, grants immunity to explosion damage. | 1 | `1` |
| [`ExtraBasicAttacks_Status`](./Enums.md) | Integer | The number of additional basic attacks the unit can perform each turn. | 1 | `1` |
| [`ExtraTrinketUses`](./Enums.md) | Integer | The number of additional uses granted to trinkets. | 1 | `1`<br>`10` |
| [`FrankBolts`](./Enums.md) | Integer | The number of Frank Bolts applied or available. | 1 | `1` |
| [`GlobalMeleeRevengeDamage`](./Passives_and_Statuses.md#object-globalmeleerevengedamage) | Object | Defines revenge damage properties (e.g., knockback) when hit by a melee attack. | 1 | `{ . . . }` |
| [`HideSomeHudStuff`](./Enums.md) | Integer | If set to 1, hides certain HUD elements. | 1 | `1` |
| [`JesterLevelUpRerolls`](./Enums.md) | Integer | The number of additional rerolls granted when leveling up. | 1 | `1` |
| [`Lifesteal`](./Enums.md) | Integer | The amount of lifesteal stacks applied. | 1 | `1`<br>`3` |
| [`MakeBasicAttackPull`](./Enums.md) | Integer | If nonzero, the unit's basic attack pulls the target closer. | 1 | `1` |
| [`ModelingClayPassive`](./Enums.md) | Integer | If set to 1, enables the passive that duplicates the equipped item on the unit. | 1 | `1` |
| [`MultiplyCoinsOnBattleStart`](./Enums.md) | Integer | The multiplier applied to the unit's coin count at the start of battle. | 1 | `2` |
| [`MultiplyReceivedHealing`](./Enums.md) | Integer | The multiplier applied to all healing the unit receives. | 1 | `2` |
| [`ObjectDetector`](./Passives_and_Statuses.md#object-objectdetector) | Object | An object that grants a chance to detect a specific item (e.g., CharmedDip) when loot is evaluated. | 1 | `{ . . . }` |
| [`PassiveIfStrAuxEquals`](./Passives_and_Statuses.md#object-passiveifstrauxequals) | Object | Grants the contained passive effects when the unit's specified auxiliary stat equals the given value. | 1 | `{ . . . }` |
| [`PassiveWhileHasDurability`](./Passives_and_Statuses.md#object-passivewhilehasdurability) | Object | An object containing passives that are active only while the item has remaining durability. | 1 | `{ . . . }` |
| [`PassiveWhileShielded`](./Passives_and_Statuses.md#object-passivewhileshielded) | Object | An object containing passives that are active only while the unit has a shield. | 1 | `{ . . . }` |
| [`PhysicalAttacksMiss`](./Enums.md) | Integer | If set to 1, all physical attacks against the unit automatically miss. | 1 | `1` |
| [`PreventSpecificInjury`](./Enums.md) | Enum | Specifies a body part tag (e.g., 'int' for head) that cannot receive injuries. | 1 | `int` |
| [`ReclaimItemOnBreak`](./Enums.md) | Integer | If set to 1, the item returns to the inventory when it breaks instead of being lost. | 1 | `1` |
| [`ReduceManaCost`](./Enums.md) | Integer | The number of stacks reducing mana cost of abilities. | 1 | `1`<br>`2` |
| [`ReduceSpellCostsPerDisorder`](./Enums.md) | Integer | The amount of mana cost reduction per disorder the unit has. | 1 | `1` |
| [`ReduceSpellCostsPerParasite`](./Enums.md) | Integer | The amount of mana cost reduction per parasite the unit is hosting. | 1 | `1` |
| [`ReplaceBlankTilesOnBattleStart`](./Enums.md#enum-replaceblanktilesonbattlestart) | Enum | Specifies a tile type (e.g., GlassTile) that replaces all blank tiles on the battle grid at the start of combat. | 1 | `GlassTile` |
| [`RerollItemsOnBattleEnd`](./Enums.md) | Integer | If set to 1, all items in the unit's inventory are rerolled to new random items at the end of battle. | 1 | `1` |
| [`ScaldingOrbMoonBossOneShot`](./Passives_and_Statuses.md#object-scaldingorbmoonbossoneshot) | Object | An object that completes the ScaldingOrb quest and removes the item from the unit's inventory. | 1 | `{ . . . }` |
| [`ScaledStatusAlliesOnSpendMana`](./Passives_and_Statuses.md#object-scaledstatusalliesonspendmana) | Object | An object that applies a scaled status (e.g., ManaGain) to adjacent allies whenever the unit spends mana. | 1 | `{ . . . }` |
| [`ScaledStatusOnHolyShieldBlock`](./Passives_and_Statuses.md#object-scaledstatusonholyshieldblock) | Object | An object that applies a scaled status (e.g., RandomMagicMissile) when the unit blocks an attack with a holy shield. | 1 | `{ . . . }` |
| [`SetFaction`](./Enums.md#enum-setfaction) | Enum | Specifies the faction the unit belongs to (e.g., 'enemies'). | 1 | `enemies` |
| [`SpawnCatCloneOnCorpsePopped`](./Enums.md) | Integer | The number of cat clones spawned when a corpse is popped (destroyed) by the unit. | 1 | `1` |
| [`SpawnOnDowned`](./Enums.md#enum-spawnondowned) | Enum  | Specifies the character or object spawned when the unit is downed. | 1 | `CharmedFly`<br>`CharmedKitten`<br>`CharmedSpookie` |
| [`SpawnRandomPickupsOnTaggedUnitKilled`](./Passives_and_Statuses.md#object-spawnrandompickupsontaggedunitkilled) | Object | Defines a pool of random pickups (items) spawned when a unit with a specific tag is killed, with a count range. | 1 | `{ . . . }` |
| [`StatDependentPassive`](./Passives_and_Statuses.md#object-statdependentpassive) | Object | An object containing formulas that dynamically modify passive effects based on the unit's stats (e.g., str, dex, int). | 1 | `{ . . . }` |
| [`StatusAdjacentOnTheirTurnEnd`](./Passives_and_Statuses.md#object-statusadjacentontheirturnend) | Object | Defines a status effect applied to adjacent units when their turn ends, such as forcing them to move away. | 1 | `{ . . . }` |
| [`StatusAlliesEachTurn`](./Passives_and_Statuses.md#object-statusallieseachturn) | Object | Defines a status effect applied to all allies each turn, with an optional exclusion of the owner and conditional checks. | 1 | `{ . . . }` |
| [`StatusOnDodge`](./Passives_and_Statuses.md#object-statusondodge) | Object | Defines a status effect applied to the unit each time it successfully dodges an attack. | 1 | `{ . . . }` |
| [`StatusOnEnemyDeath`](./Passives_and_Statuses.md#object-statusonenemydeath) | Object | Defines a status effect applied to the unit each time an enemy dies. | 1 | `{ . . . }` |
| [`StatusOnFallAsleep`](./Passives_and_Statuses.md#object-statusonfallasleep) | Object | Defines one or more beneficial status effects applied to the unit when it falls asleep. | 1 | `{ . . . }` |
| [`StatusOnFullMana`](./Passives_and_Statuses.md#object-statusonfullmana) | Object | Defines a status effect applied to the unit when its mana is full, with an optional once-per-battle conditional. | 1 | `{ . . . }` |
| [`StevenBolts`](./Enums.md) | Integer | The number of Steven Bolts (a special resource or charge) the unit has for a unique ability. | 1 | `1` |
| [`StripKnockback`](./Enums.md) | Integer | If non-zero, removes all knockback effects from the unit's attacks or abilities. | 1 | `1` |
| [`TintItem`](./Passives_and_Statuses.md#object-tintitem) | Object | Defines additive and multiplicative color tint adjustments applied to an item's appearance, with an optional ignore condition. | 1 | `{ . . . }` |
| [`TunnelVision`](./Passives_and_Statuses.md#object-tunnelvision) | Object | If present, grants the TunnelVision status, which modifies crit_chance as defined in its sub-properties. | 1 | `{ . . . }` |

</details>


---


### Object: `AddStatusToBasicAttack`


**Definition:** Contains status effects to add to the basic attack.
**Total Count:** 65

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Items_and_Equipment.md#context-addpassivestominions), [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 121 | passives<br>class<br>	ag |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 56 | `Default`<br>`FormChange`<br>`Druid` | [`Bleed`](./Enums.md) | Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 45 | Default<br>FormChange<br>Druid |
| [`Poison`](./Enums.md) | Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 29 | `1`<br>`10`<br>`2` |
| [`Knockback`](./Enums.md) | Equation | The number of tiles the target is pushed away from the source on hit. | 24 | `1`<br>`10`<br>`2` |
| [`Burn`](./Enums.md) | Equation | The amount of Burn applied, either as a fixed number or a formula string. | 16 | `1`<br>`10`<br>`2` |
| [`Fear`](./Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 13 | `1`<br>`10`<br>`2` |
| [`Bruise`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 12 | `1`<br>`2`<br>`3` |
| [`ChangeTile`](./Enums.md#enum-changetile) | Enum  | Specifies the tile type to change to, or an object defining tile change parameters (tile type and area of effect). | 10 | `BlankTile`<br>`BrambleTile`<br>`CreepTile` |
| [`Slow`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 10 | `-1`<br>`1`<br>`2` |
| [`Stun`](./Arrays.md#array-stun) | Array  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 8 | `1`<br>`2`<br>`3` |
| [`Confusion`](./Enums.md) | Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 7 | `1`<br>`10`<br>`2` |
| [`Weakness`](./Enums.md) | Integer | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 7 | `1`<br>`2`<br>`3` |
| [`Leech`](./Enums.md) | Integer | The amount of health leeched from the target (heals the attacker). | 5 | `1`<br>`2` |
| [`Rot`](./Enums.md) | Integer | Integer, or an array [stacks, probability] specifying the amount of Rot stacks applied with the given probability. | 5 | `-999999`<br>`1`<br>`2` |
| [`DamageOrHealConditionally`](./Enums.md) | Integer | The amount of conditional damage or healing applied, based on certain conditions (e.g., ally or enemy). | 4 | `1` |
| [`Freeze`](./Arrays.md#array-freeze) | Array / Integer  | The amount of freeze stacks applied, or an [stacks, probability] array. | 4 | `1`<br>`2`<br>`[1 .01]` |
| [`Leeches`](./Enums.md) | Integer | The number of stacks of the Leeches debuff applied, which deals damage over time and heals the applier. | 4 | `1`<br>`2`<br>`3` |
| [`SoulLink`](./Enums.md) | Integer | The number of soul link stacks applied. | 4 | `1` |
| [`Tangled`](./Arrays.md#array-tangled) | Array  | The number of stacks of the Tangled status effect applied, or an object defining its properties such as `stacks` and `alt_art`. | 4 | `1`<br>`2`<br>`[1, .05]` |
| [`Conditional_GoodRoll`](./Passives_and_Statuses.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 3 | `{ . . . }` |
| [`MagicWeakness`](./Enums.md) | Integer | The amount of magic weakness stacks applied, or an [stacks, probability] array. | 3 | `1`<br>`2`<br>`3` |
| [`ApplyToSource`](./Passives_and_Statuses.md#object-applytosource) | Object  | An object of effects that are applied to the source of the ability (the caster). | 2 | `{ . . . }` |
| [`Blind`](./Enums.md) | Integer | The amount of blind stacks applied, or an [stacks, probability] array. | 2 | `-1`<br>`1`<br>`2` |
| [`KnockOutCoin`](./Enums.md) | Integer | The number of coins knocked out, with an optional probability or an object with stacks and chance. | 2 | `1`<br>`[1 .5]` |
| [`ManaLeeches`](./Enums.md) | Integer | The number of mana leech stacks applied. | 2 | `1`<br>`2` |
| [`OverrideChainKnockback`](./Enums.md) | Integer | The custom number of tiles for chain knockback, overriding the default. | 2 | `0`<br>`1`<br>`10` |
| [`SpiderInfested`](./Enums.md) | Integer | The number of spider infestation stacks applied. | 2 | `1`<br>`2`<br>`4` |
| [`ForceUseAbilityOnTarget`](./Miscellaneous.md#object-forceuseabilityontarget) | Object | Defines a chance to force the unit to use a specified ability on the target. | 1 | `{ . . . }` |
| [`KnockUpAndAway`](./Miscellaneous.md#object-knockupandaway) | Object  | Contains parameters for launching the target upward and away from the source, including stacks and distance. | 1 | `{ . . . }` |
| [`Marked`](./Enums.md) | Integer | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`3`<br>`5` |
| [`PullSourceToTarget`](./Enums.md) | Integer | The amount of tiles the source is pulled towards the target after the attack. | 1 | `1` |

</details>


---


### Object: `Conditional_GoodRoll`


**Definition:** Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability.
**Total Count:** 37

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Items_and_Equipment.md#context-addstatustobasicattack), [`StatusEachTurnEnd`](./Items_and_Equipment.md#context-statuseachturnend), [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend), [`StatusOnKill`](./Items_and_Equipment.md#context-statusonkill), [`StatusOnTakeHealthOrShieldDamage`](./Items_and_Equipment.md#context-statusontakehealthorshielddamage), [`effects`](./Items_and_Equipment.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `odds` | Float | The probability of the effect occurring, expressed as a decimal or percentage. | 37 | `.1`<br>`.16666666`<br>`.3` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 37 | Default<br>FormChange<br>Druid |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 15 | passives<br>class<br>	ag |
| [`Freeze`](./Arrays.md#array-freeze) | Array / Integer  | The amount of freeze stacks applied, or an [stacks, probability] array. | 6 | `1`<br>`2`<br>`[1 .01]` |
| [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Enum  | Specifies the loot pool from which to find an item, with an optional chance. | 5 | `blackbird_pool`<br>`chapter`<br>`chapter_common` |
| [`ForceUseAbility_NonStack`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Forces the unit to use a specific non-stackable ability when the conditional roll is successful. | 4 | `Endeavor_Auto`<br>`Indigestion_Fart`<br>`Indigestion_Fart2` |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum  | The name of the ability the source is forced to use, optionally with a chance. | 3 | `CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| [`RandomMutation`](./Enums.md) | Integer | The number of random mutations to apply. | 3 | `1`<br>`3` |
| `DestroyTrinket` | `Number` | The number of trinkets destroyed. | 1 | `1` |

</details>


---


### Object: `effects`


**Definition:** Applies a list of status effects or visual effects to targets.
**Total Count:** 35

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DoDamage`](./Items_and_Equipment.md#context-dodamage), [`MeleeRevengeDamage`](./Items_and_Equipment.md#context-meleerevengedamage), [`RevengeDamage`](./Items_and_Equipment.md#context-revengedamage), [`damage_instance`](./Items_and_Equipment.md#context-damage_instance)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1085 | passives<br>class<br>	ag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 624 | Default<br>FormChange<br>Druid |
| [`Stun`](./Arrays.md#array-stun) | Array  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 98 | `1`<br>`2`<br>`3` |
| [`Burn`](./Enums.md) | Equation | The amount of Burn applied, either as a fixed number or a formula string. | 85 | `1`<br>`10`<br>`2` |
| [`Bruise`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 79 | `1`<br>`2`<br>`3` |
| [`Poison`](./Enums.md) | Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 67 | `1`<br>`10`<br>`2` |
| [`Confusion`](./Enums.md) | Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 37 | `1`<br>`10`<br>`2` |
| [`VisualFXTile`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the name of the visual effect to play on the target tile. | 34 | `Bolt`<br>`BurnTrigger`<br>`Explosion` |
| [`Fear`](./Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 31 | `1`<br>`10`<br>`2` |
| [`Slow`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 29 | `-1`<br>`1`<br>`2` |
| [`BounceObject`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the object or projectile to spawn and bounce from the target. | 26 | `AllyRotFly`<br>`Amoeba`<br>`BeefyCharmedLeech` |
| [`Blind`](./Enums.md) | Integer | The amount of blind stacks applied, or an [stacks, probability] array. | 24 | `-1`<br>`1`<br>`2` |
| [`Immobile`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 24 | `0`<br>`1`<br>`10%` |
| [`Freeze`](./Arrays.md#array-freeze) | Array / Integer  | The amount of freeze stacks applied, or an [stacks, probability] array. | 19 | `1`<br>`2`<br>`[1 .01]` |
| [`Conditional_GoodRoll`](./Passives_and_Statuses.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 14 | `{ . . . }` |
| [`Cleave`](./Enums.md) | Integer | The number of additional targets hit; if an object, contains a chance parameter for each cleave attempt. | 12 | `1` |
| [`VisualFX`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the name of the visual effect to play. | 10 | `BigMagicMissileBlast`<br>`Bolt`<br>`Cleanse` |
| [`Grappled`](./Arrays.md#array-grappled) | Array  | The number of stacks and probability of applying the Grappled status, in format [stacks, probability] or just stacks. | 8 | `1`<br>`[1, .50]`<br>`[1, .75]` |
| `DestroyTrinket` | Integer | The number of trinkets destroyed. | 3 | `1` |

</details>


---


### Object: `MeleeRevengeDamage`


**Definition:** Defines the damage and effects applied back to a melee attacker upon being hit.
**Total Count:** 32

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 36 | `damage_instance`<br>`spell`<br>`self_damage` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 47 | `{ . . . }` |
| [`knockback`](./Enums.md#enum-knockback) | Enum / Integer  | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 24 | `"ceil(X*.25/5)"`<br>`-10`<br>`-2` |
| [`damage`](./Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 22 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |

</details>


---


### Object: `StatusOnBattleEnd`


**Definition:** An object containing status effects or passives applied to the unit when the battle ends.
**Total Count:** 25

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyPassives`](./Items_and_Equipment.md#context-applypassives), [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 56 | passives<br>class<br>	ag |
| `even_if_dead` | Boolean | If true, the effect triggers even if the unit is dead. | 25 | `true` |
| [`RandomMutation`](./Enums.md) | Integer | The number of random mutations to apply. | 9 | `1`<br>`3` |
| [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Enum  | Specifies the loot pool from which to find an item, with an optional chance. | 8 | `blackbird_pool`<br>`chapter`<br>`chapter_common` |
| [`RandomPermanentStat`](./Enums.md) | Integer | The amount of a random permanent stat change (positive or negative). | 8 | `-1`<br>`-2`<br>`-3` |
| [`Conditional_GoodRoll`](./Passives_and_Statuses.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 6 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 4 | `Default`<br>`FormChange`<br>`Druid` | [`PermanentIntelligence`](./Enums.md) | Integer | The permanent amount of intelligence added or removed. | 8 | Default<br>FormChange<br>Druid |
| [`GainCoins`](./Arrays.md#array-gaincoins) | Array / Integer  | The amount of coins gained, or a [min, max] range. | 2 | `-5`<br>`1`<br>`2` |
| [`PermanentConstitution`](./Enums.md) | Integer | The amount of permanent Constitution stat added or removed. | 2 | `-1`<br>`-2`<br>`1` |
| [`RepairTrinket`](./Enums.md) | Integer | The number of stacks of the Repair Trinket status effect to apply. | 2 | `1`<br>`99` |
| [`SetItemAux`](./Miscellaneous.md#object-setitemaux) | Object  | Configures an item's auxiliary value by specifying a target slot and a formula for the new value. | 2 | `{ . . . }` |
| [`Conditional_Corpse`](./Passives_and_Statuses.md#object-conditional_corpse) | Object | Contains an inner effect block that only executes if the target is a corpse. | 1 | `{ . . . }` |
| [`Conditional_Shielded`](./Passives_and_Statuses.md#object-conditional_shielded) | Object | An object containing effects that are only applied if the target has a shield active. | 1 | `{ . . . }` |
| [`RepairAll`](./Enums.md) | Integer | The amount of durability restored to all equipped items. | 1 | `1`<br>`10` |
| [`RepairWeapon`](./Arrays.md#array-repairweapon) | Array / Integer  | The number of weapon durability points restored; an array [stacks, probability] applies a chance-based repair. | 1 | `1`<br>`6`<br>`99` |
| [`TransformWeapon`](./Miscellaneous.md#object-transformweapon) | Object  | An object with `from` and `to` fields specifying the weapon transformation. | 1 | `{ . . . }` |

</details>


---


### Object: `StatusEachTurnEnd`


**Definition:** Specifies status effects applied to the unit at the end of each of its turns.
**Total Count:** 22

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 42 | passives<br>class<br>	ag |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum  | The name of the ability the source is forced to use, optionally with a chance. | 12 | `CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| [`Shield`](./Enums.md) | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 5 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 5 | `Default`<br>`FormChange`<br>`Druid` | [`PartialCleanse`](./Enums.md) | Integer | The number of stacks of temporary status effects to remove from the target. | 7 | Default<br>FormChange<br>Druid |
| [`Conditional_GoodRoll`](./Passives_and_Statuses.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 2 | `{ . . . }` |
| [`ImmediateUseAbility`](./Miscellaneous.md#object-immediateuseability) | Enum / Object  | Specifies the name of an ability to be triggered instantly from this effect. | 2 | `{ . . . }`<br>`FuzzerReact`<br>`HitlerCloneHeil`<br>`HitlerCloneTransform` |
| [`SpawnCoinAnywhere`](./Enums.md) | Integer | The number of coins to spawn. If an array, the second value is the probability of spawning them anywhere. | 2 | `1`<br>`[1 .5]` |
| [`AddWeaponAux`](./Enums.md) | Equation | The amount or expression to add to the source's weapon auxiliary stat. | 1 | `"-max(min(X+1, item_aux), 0)"`<br>`-item_aux`<br>`1` |
| [`Burn`](./Enums.md) | Equation | The amount of Burn applied, either as a fixed number or a formula string. | 1 | `1`<br>`10`<br>`2` |
| [`Conditional_ManaThreshold`](./Miscellaneous.md#object-conditional_manathreshold) | Object | Defines a conditional block that applies effects only if a unit's mana meets a specified threshold. | 1 | `{ . . . }` |
| [`ConstitutionUp`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 1 | `-1`<br>`-2`<br>`1` |
| [`PreEmptiveCounterNextAttacks`](./Enums.md) | Integer | The number of next incoming attacks that the unit will counter preemptively before they land. | 1 | `1` |
| [`Stealth`](./Arrays.md#array-stealth) | Array  | The number of stealth stacks applied. | 1 | `1`<br>`2`<br>`[1 .1]` |

</details>


---


### Object: `StatusOnBreak`


**Definition:** An object defining statuses or effects applied when an item or object breaks.
**Total Count:** 22

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 11 | passives<br>class<br>	ag |
| [`GainCoinsRange`](./Miscellaneous.md#object-gaincoinsrange) | Object  | An object with `min` and `max` fields specifying a range for the amount of coins gained. | 5 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 4 | `Default`<br>`FormChange`<br>`Druid` | [`Bruise`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 4 | Default<br>FormChange<br>Druid |
| [`ChangeTilesUnder`](./Enums.md#enum-changetilesunder) | Enum  | The tile type to change the ground tiles under the target to. | 3 | `DirtTile`<br>`GlassTile`<br>`LavaTile` |
| [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Enum  | Specifies the loot pool from which to find an item, with an optional chance. | 3 | `blackbird_pool`<br>`chapter`<br>`chapter_common` |
| [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 3 | `1`<br>`10`<br>`2` |
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 3 | `1`<br>`2`<br>`3` |
| [`PermanentConstitution`](./Enums.md) | Integer | The amount of permanent Constitution stat added or removed. | 3 | `-1`<br>`-2`<br>`1` |
| [`ApplyToRandomPartyMemberIfPossible`](./Miscellaneous.md#object-applytorandompartymemberifpossible) | Object  | Contains an inner effect block that is applied to a random living party member if one exists. | 1 | `{ . . . }` |
| [`ConstitutionUp`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 1 | `-1`<br>`-2`<br>`1` |
| [`DexterityUp`](./Enums.md) | Array / Equation | The amount of dexterity change, or a keyword like 'item_aux'. | 1 | `-1`<br>`1`<br>`2` |
| [`FindItem`](./Enums.md#enum-finditem) | Enum  | The name of the specific item to find and add to the source's inventory. | 1 | `BoneClub`<br>`Molars`<br>`Pearl` |
| [`GainDisorder`](./Enums.md#enum-gaindisorder) | Enum | Specifies the name of the disorder gained. | 1 | `Chungus`<br>`Psychosis` |
| [`IntelligenceUp`](./Enums.md) | Array / Equation | The amount of Intelligence added as a flat bonus. | 1 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| [`ObjectOnHitCharacter`](./Passives_and_Statuses.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 1 | `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| [`StrengthUp`](./Enums.md) | Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 1 | `"max(int, 0)"`<br>`-1`<br>`-2` |

</details>


---


### Object: `SpawnOnBattleStart`


**Definition:** Specifies the object that spawns adjacent to the unit at the start of battle.
**Total Count:** 21

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 38 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`number`](./Arrays.md#array-number) | Array / Integer | The number of objects to spawn; can be a single integer or an array `[min, max]` for a random range. | 29 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `StatusOnKill`


**Definition:** Specifies status effects or actions triggered when the unit kills an enemy.
**Total Count:** 16

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 20 | passives<br>class<br>	ag |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 6 | `Default`<br>`FormChange`<br>`Druid` | [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 8 | Default<br>FormChange<br>Druid |
| [`Conditional_GoodRoll`](./Passives_and_Statuses.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 4 | `{ . . . }` |
| [`EquipPermanentItem`](./Enums.md#enum-equippermanentitem) | Enum  | The name of the item to permanently equip to the source. | 3 | `BoneClub`<br>`Kidney` |
| [`StrengthUp`](./Enums.md) | Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 3 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| [`LuckUp`](./Enums.md) | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 2 | `-1`<br>`-2`<br>`-4` |
| [`SpeedUp`](./Enums.md) | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 2 | `-1`<br>`-2`<br>`-4` |
| [`BrittleCharismaUp`](./Enums.md) | Integer | The number of stacks of temporary Charisma gained on kill. | 1 | `2` |
| [`BrittleConstitutionUp`](./Enums.md) | Integer | The number of stacks of temporary Constitution gained on kill. | 1 | `2` |
| [`BrittleDexterityUp`](./Enums.md) | Integer | The number of stacks of temporary Dexterity gained on kill. | 1 | `2` |
| [`BrittleIntelligenceUp`](./Enums.md) | Integer | The number of stacks of temporary Intelligence gained on kill. | 1 | `2` |
| [`BrittleLuckUp`](./Enums.md) | Integer | The number of stacks of temporary Luck gained on kill. | 1 | `2` |
| [`BrittleSpeedUp`](./Enums.md) | Integer | The number of stacks of temporary Speed gained on kill. | 1 | `2` |
| [`BrittleStrengthUp`](./Enums.md) | Integer | The number of stacks of temporary Strength gained on kill. | 1 | `2` |
| [`CharismaUp`](./Enums.md) | Integer | The amount of charisma change, or a keyword like 'item_aux'. | 1 | `-1`<br>`-2`<br>`1` |
| [`ConstitutionUp`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 1 | `-1`<br>`-2`<br>`1` |
| [`DexterityUp`](./Enums.md) | Array / Equation | The amount of dexterity change, or a keyword like 'item_aux'. | 1 | `-1`<br>`1`<br>`2` |
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 1 | `1`<br>`2`<br>`3` |
| [`IntelligenceUp`](./Enums.md) | Array / Equation | The amount of Intelligence added as a flat bonus. | 1 | `"min(-int, 0)"`<br>`-1`<br>`-2` |

</details>


---


### Object: `StatusOnTookDamage`


**Definition:** Specifies status effects or actions triggered when the unit takes damage.
**Total Count:** 16

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 30 | passives<br>class<br>	ag |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 14 | `Default`<br>`FormChange`<br>`Druid` | [`Charge`](./Enums.md) | Integer | The number of charge stacks applied. | 13 | Default<br>FormChange<br>Druid |
| [`StrengthUp`](./Enums.md) | Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 4 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| [`DamageUp`](./Enums.md) | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 3 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`Temporary`](./Passives_and_Statuses.md#object-temporary) | Object  | Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions. | 3 | `{ . . . }` |
| [`Thorns`](./Enums.md) | Integer | The amount of thorns damage dealt to attackers on hit. | 3 | `1`<br>`2`<br>`3` |
| [`Conditional_HasStatus`](./Passives_and_Statuses.md#object-conditional_hasstatus) | Object | Contains an inner effect block that only executes if the target has the specified status effect. | 2 | `{ . . . }` |
| [`Bleed`](./Enums.md) | Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`10`<br>`2` |
| [`Conditional_HealthThreshold`](./Miscellaneous.md#object-conditional_healththreshold) | Object  | Contains an inner effect block that only executes if the target's health is below a threshold, defined by `threshold_flat`, `threshold_percent`, or `threshold_expr`. | 1 | `{ . . . }` |
| [`DivineShield`](./Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | `1`<br>`2`<br>`4` |
| [`DodgeChance_Status`](./Enums.md) | Integer | The flat percentage increase to dodge chance applied as a status effect. | 1 | `1`<br>`10`<br>`100` |
| [`RemoveStatus`](./Enums.md#enum-removestatus) | Enum  | The name of the status effect to remove from the source. | 1 | `AlphaCat`<br>`Brace`<br>`DodgeChance_Status` |

</details>


---


### Object: `StatusOnBattleStart`


**Definition:** An object containing status effects to apply to the unit at the start of every battle.
**Total Count:** 13

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 7 | passives<br>class<br>	ag |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 7 | `Default`<br>`FormChange`<br>`Druid` | [`Craft`](Abilities_and_Spells.md#object-craft) | Object | Specifies the loot pool and slot to craft an item for the source. | 3 | Default<br>FormChange<br>Druid |
| [`SafeDie`](./Enums.md) | Integer | The number of times the unit can survive a fatal hit. | 2 | `1` |
| [`Brace`](./Enums.md) | Array / Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 1 | `1`<br>`10`<br>`2` |
| [`DestroyEquipmentAndAttachParasite`](./Miscellaneous.md#object-destroyequipmentandattachparasite) | Object  | Attempts to destroy a random piece of the target's equipment and attach a parasite from the specified pool. | 1 | `{ . . . }` |
| [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Enum  | Specifies the loot pool from which to find an item, with an optional chance. | 1 | `blackbird_pool`<br>`chapter`<br>`chapter_common` |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum  | The name of the ability the source is forced to use, optionally with a chance. | 1 | `CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| [`ObjectOnHitCharacter`](./Passives_and_Statuses.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 1 | `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| [`RandomMagicMissile`](./Enums.md) | Integer | The number of random magic missiles fired, or an object defining its properties. | 1 | `1`<br>`10`<br>`2` |
| [`ReviveNextRound`](./Miscellaneous.md#object-revivenextround) | Object  | The number of revives granted, or an object defining revive properties. | 1 | `{ . . . }` |
| [`SetHealth`](./Enums.md) | Integer | Sets the target's health to a specific flat value or percentage. | 1 | `1`<br>`100%`<br>`50%` |
| [`StealthUntilBasicAttack`](./Enums.md) | Integer | The number of stacks of Stealth that are removed when the unit performs a basic attack. | 1 | `1` |

</details>


---


### Object: `SpawnThingOnDamage`


**Definition:** Specifies an object that spawns on the tile when the unit takes damage.
**Total Count:** 11

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 38 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 20 | `false`<br>`true` |
| [`chance`](./Enums.md#enum-chance) | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 12 | `.02`<br>`.1`<br>`.15` |
| `spawn_on_death_hit` | Boolean | If true, spawning only occurs when the damage is lethal. | 10 | `false` |
| [`number`](./Arrays.md#array-number) | Array / Integer | The number of objects to spawn; can be a single integer or an array `[min, max]` for a random range. | 1 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `SpawnEachTurn`


**Definition:** Specifies an object that spawns on a random adjacent tile each turn, with optional chance.
**Total Count:** 10

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array / Enum | Specifies the object or unit to be spawned. | 22 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`chance`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A probability (decimal or percentage) for a form change or other effect to occur. | 20 | `.02`<br>`.1`<br>`.15` |
| [`stack_key`](./Enums.md#enum-stack_key) | Enum | Specifies the key of the status stack to check for the condition. | 5 | `CATHIDE`<br>`EMPTY_GENERATOR`<br>`FANNY_PACK` |

</details>


---


### Object: `StatusEachTurnBegin`


**Definition:** Specifies status effects applied to the unit at the start of each of its turns.
**Total Count:** 10

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveWhenDead`](./Items_and_Equipment.md#context-passivewhendead), [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 9 | passives<br>class<br>	ag |
| [`Conditional_BadRoll`](./Passives_and_Statuses.md#object-conditional_badroll) | Object  | An object containing an `odds` value and effects that are applied when a random roll succeeds. | 5 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 | `Default`<br>`FormChange`<br>`Druid` | [`SpeedUp`](./Enums.md) | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 10 | Default<br>FormChange<br>Druid |
| [`BlessingOfPeace`](./Enums.md) | Integer | The number of stacks of the Blessing of Peace status applied to the unit each turn. | 1 | `1` |
| [`Burn`](./Enums.md) | Equation | The amount of Burn applied, either as a fixed number or a formula string. | 1 | `1`<br>`10`<br>`2` |
| [`DestroyTrinket`](./Enums.md) | Integer | The number of trinkets destroyed. | 1 | `1` |
| [`DoubleCastSpellThisTurn`](./Enums.md) | Integer | If non-zero, grants the unit a double cast effect for spells this turn. | 1 | `1` |
| [`DrinkWater`](./Enums.md) | Integer | The number of water-drink actions performed. | 1 | `1` |
| [`ManaGainRange`](./Miscellaneous.md#object-managainrange) | Object | Defines the minimum and maximum mana gained per turn. | 1 | `{ . . . }` |
| [`Revive`](./Enums.md) | Integer | Revives a dead target with the specified percentage of health (e.g., "50%", "100%") or a fixed number. | 1 | `1`<br>`100%`<br>`50%` |
| [`Temporary`](./Passives_and_Statuses.md#object-temporary) | Object  | Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions. | 1 | `{ . . . }` |
| [`UseAbility`](./Enums.md#enum-useability) | Enum  | The name of the ability the target is forced to use. | 1 | `GirlDinoPoop`<br>`KirbySpit`<br>`MD_PoopChain` |
| [`Wet`](./Enums.md) | Integer | The number of stacks of the Wet status effect applied. | 1 | `1` |

</details>


---


### Object: `RevengeDamage`


**Definition:** An object defining the damage and effects that trigger when the unit is attacked.
**Total Count:** 9

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 10 | `damage_instance`<br>`spell`<br>`self_damage` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 29 | `{ . . . }` |
| [`damage`](./Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 8 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`elements`](./Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 2 | `[`<br>`[Heat Fire]` |

</details>


---


### Object: `AddSelfStatusToBasicAttack`


**Definition:** Applies the contained status effects to the unit when it uses its basic attack.
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 9 | passives<br>class<br>	ag |
| [`RandomMagicMissile`](./Enums.md) | Integer | The number of random magic missiles fired, or an object defining its properties. | 7 | `1`<br>`10`<br>`2` |
| [`Bleed`](./Enums.md) | Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`10`<br>`2` |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum  | The name of the ability the source is forced to use, optionally with a chance. | 1 | `CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| [`Quivered`](./Arrays.md#array-quivered) | Array / Integer  | The amount of quivered stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`2`<br>`5` |
| [`Shield`](./Enums.md) | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 1 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `DurabilityTransform`


**Definition:** Transforms the item into another when durability reaches specified thresholds.
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`eq`](./Arrays.md#array-eq) | Array | An array specifying a [durability, item] pair to transform to when durability equals a specific value. | 7 | `[0 EstusFlask_Empty]`<br>`[0 JarOfNothing]`<br>`[0 WaterBottle_Empty]` |
| [`ge`](./Arrays.md#array-ge) | Array | An array specifying a [durability, item] pair to transform to when durability is greater than or equal to a specific value. | 4 | `[10 NuclearKnife_Glowing]`<br>`[2 WaterBottle_Full]`<br>`[20 BlackShard_Glowing]` |

</details>


---


### Object: `PassiveIfStrAuxEquals`


**Definition:** Grants the contained passive effects when the unit's specified auxiliary stat equals the given value.
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`value`](./Math_Equations.md) | Equation | The numeric value or formula associated with the buff. | 7 | `.5`<br>`0`<br>`1` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 7 | `{ . . . }` |

</details>


---


### Object: `StatusOnKillEnemy`


**Definition:** Specifies the effects applied when the unit kills an enemy.
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 10 | passives<br>class<br>	ag |
| [`DamageUp`](./Enums.md) | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 4 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`ManaGain`](./Enums.md) | Equation | The amount of mana restored to the source, which can be an expression. | 2 | `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`Brace`](./Enums.md) | Array / Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 1 | `1`<br>`10`<br>`2` |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum  | The name of the ability the source is forced to use, optionally with a chance. | 1 | `CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| [`LuckUp`](./Enums.md) | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 1 | `-1`<br>`-2`<br>`-4` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `AddStatusToAllDamage`


**Definition:** Adds the contained status effects to all damage dealt by the unit.
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 12 | passives<br>class<br>	ag |
| `must_do_damage` | Boolean | If true, the status or effect will only be applied if the attack or ability actually deals damage. | 3 | `true` |
| [`Conditional_HasStatus`](./Passives_and_Statuses.md#object-conditional_hasstatus) | Object | Contains an inner effect block that only executes if the target has the specified status effect. | 3 | `{ . . . }` |
| [`Conditional_HasTag`](./Passives_and_Statuses.md#object-conditional_hastag) | Object  | Evaluates whether the target has a specific tag; if true, applies the effects within; otherwise, runs the Else block. | 3 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 | `Default`<br>`FormChange`<br>`Druid` | [`KnockbackIfCrit`](Engine_StatusAndPassiveKeys.md#object-knockbackifcrit) | Object || 3 | Default<br>FormChange<br>Druid |
| [`Rot`](./Enums.md) | Integer | Integer, or an array [stacks, probability] specifying the amount of Rot stacks applied with the given probability. | 1 | `-999999`<br>`1`<br>`2` |

</details>


---


### Object: `ApplyToSource`


**Definition:** An object of effects that are applied to the source of the ability (the caster).
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Items_and_Equipment.md#context-addstatustobasicattack), [`Conditional_HasStatus`](./Items_and_Equipment.md#context-conditional_hasstatus), [`Else`](./Items_and_Equipment.md#context-else)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 22 | passives<br>class<br>	ag |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 20 | `Default`<br>`FormChange`<br>`Druid` | [`AllStatsUp`](./Enums.md) | Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 14 | Default<br>FormChange<br>Druid |
| [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 6 | `1`<br>`10`<br>`2` |
| [`StrengthUp`](./Enums.md) | Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 6 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| [`Charge`](./Enums.md) | Equation | The number of charge stacks applied. | 2 | `1`<br>`2`<br>`3` |
| [`SpeedUp`](./Enums.md) | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 1 | `-1`<br>`-2`<br>`-4` |

</details>


---


### Object: `GainCoinsRange`


**Definition:** An object with `min` and `max` fields specifying a range for the amount of coins gained.
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBreak`](./Items_and_Equipment.md#context-statusonbreak), [`StatusOnDie`](./Items_and_Equipment.md#context-statusondie)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max` | Integer | The maximum amount of coins that can be gained. | 11 | `10`<br>`2`<br>`25` |
| `min` | Integer | The minimum amount of coins that will be gained. | 11 | `0`<br>`1`<br>`10` |

</details>


---


### Object: `ItemAuxTransform`


**Definition:** Transforms the item into another when its auxiliary value reaches specified thresholds.
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`le`](./Arrays.md#array-le) | Array | An array specifying a [aux value, item] pair to transform to when the aux value is less than or equal to a specific value. | 3 | `[10 MoneyBag_Small]`<br>`[25 MoneyBag_Medium]`<br>`[50 MoneyBag_Large]` |
| [`ge`](./Arrays.md#array-ge) | Array | An array specifying a [durability, item] pair to transform to when durability is greater than or equal to a specific value. | 2 | `[10 NuclearKnife_Glowing]`<br>`[2 WaterBottle_Full]`<br>`[20 BlackShard_Glowing]` |
| [`lt`](./Arrays.md#array-lt) | Array | An array specifying a [aux value, item] pair to transform to when the aux value is strictly less than a specific value. | 1 | `[10 NuclearKnife]` |

</details>


---


### Object: `PassiveWhenOnTile`


**Definition:** Grants the contained passive effects while the unit is standing on one of the specified tile types.
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 7 | passives<br>class<br>	ag |
| [`tile`](./Arrays.md#array-tile) | Array / Enum | Specifies the tile type(s) to change to, either a single tile string or an array of tiles. | 7 | `BrambleTile`<br>`CreepTile`<br>`DirtTile` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 7 | `{ . . . }` |

</details>


---


### Object: `StatusAlliesOnBattleStart`


**Definition:** An object containing status effects to apply to all allies at the start of battle.
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 5 | passives<br>class<br>	ag |
| [`SpeedUp`](./Enums.md) | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 2 | `-1`<br>`-2`<br>`-4` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid` | [`Brace`](./Enums.md) | Enum / Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 2 | Default<br>FormChange<br>Druid |
| [`ConstitutionUp`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 1 | `-1`<br>`-2`<br>`1` |
| [`DamageUp`](./Enums.md) | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 1 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`StrengthUp`](./Enums.md) | Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 1 | `"max(int, 0)"`<br>`-1`<br>`-2` |

</details>


---


### Object: `StatusOnDie`


**Definition:** Specifies status effects or actions triggered when the unit dies.
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 5 | passives<br>class<br>	ag |
| [`Conditional_RandomChance`](./Miscellaneous.md#object-conditional_randomchance) | Object | An object containing effects that execute only if a random roll succeeds, with an odds value defined inside. | 1 | `{ . . . }` |
| [`CreateGlobalModifiers`](./Passives_and_Statuses.md#object-createglobalmodifiers) | Object  | Defines global gameplay modifiers to activate. | 1 | `{ . . . }` |
| [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Enum  | Specifies the loot pool from which to find an item, with an optional chance. | 1 | `blackbird_pool`<br>`chapter`<br>`chapter_common` |
| [`GainCoinsRange`](./Miscellaneous.md#object-gaincoinsrange) | Object  | An object with `min` and `max` fields specifying a range for the amount of coins gained. | 1 | `{ . . . }` |
| [`RandomMagicMissile`](./Enums.md) | Integer | The number of random magic missiles fired, or an object defining its properties. | 1 | `1`<br>`10`<br>`2` |
| [`RandomStatusFromPool`](./Passives_and_Statuses.md#object-randomstatusfrompool) | Object  | A collection of status effects; one is randomly chosen and applied to the target. | 1 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusOnEndMove`


**Definition:** Specifies status effects or actions triggered when the unit finishes moving.
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `Temporary`


**Definition:** Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions.
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_BadRoll`](./Items_and_Equipment.md#context-conditional_badroll), [`StatusEachTurnBegin`](./Items_and_Equipment.md#context-statuseachturnbegin), [`StatusOnTookDamage`](./Items_and_Equipment.md#context-statusontookdamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 57 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 56 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 52 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| `expires_on_begin_turn` | Boolean | If true, the temporary effect expires at the start of the target's turn. | 25 | `true` |
| `expires_on_end_turn` | Boolean | If true, the temporary effect expires at the end of the target's turn. | 21 | `true` |

</details>


---


### Object: `TransformItemOnElementInfluence`


**Definition:** Transforms the item into the specified one when influenced by the given element, optionally fully repairing it.
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 5 | `Electric`<br>`Fire`<br>`Gravity` |
| `full_repair` | Boolean | If true, the item's durability is fully restored when transformed by element influence. | 5 | `true` |
| [`item`](./Enums.md#enum-item) | Enum | Specifies the item to transform into, either by name, a nested item object, or a numeric value. | 5 | `1`<br>`2`<br>`EstusFlask_Full` |

</details>


---


### Object: `AddDamageToElementDamage`


**Definition:** Defines additional damage of a specific element added to the unit's attacks.
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](./Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 9 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`element`](./Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 9 | `Electric`<br>`Fire`<br>`Gravity` |

</details>


---


### Object: `AddPassivesToMinions`


**Definition:** An object containing passives that are granted to all minions spawned by the unit.
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 41 | passives<br>class<br>	ag |
| [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 7 | `1`<br>`10`<br>`2` |
| [`AddMaxHealth`](./Enums.md) | Integer | The amount added to the unit's maximum health. Negative values reduce max health. | 6 | `-25`<br>`10`<br>`2` |
| [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#object-addstatustobasicattack) | Object  | Contains status effects to add to the basic attack. | 4 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid` | [`AllStatsUp`](./Enums.md) | Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | Default<br>FormChange<br>Druid |
| [`Shield`](./Enums.md) | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 1 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |

</details>


---


### Object: `ChanceToRevive`


**Definition:** The percentage chance or an object defining chance, health, and statuses on revival.
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 5 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `health` | Integer | The maximum hit points of the unit. | 4 | `0`<br>`1`<br>`10` |

</details>


---


### Object: `Conditional_HasStatus`


**Definition:** Contains an inner effect block that only executes if the target has the specified status effect.
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToAllDamage`](./Items_and_Equipment.md#context-addstatustoalldamage), [`StatusOnTookDamage`](./Items_and_Equipment.md#context-statusontookdamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 20 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 22 | passives<br>class<br>	ag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 10 | Default<br>FormChange<br>Druid |
| [`ApplyToSource`](./Passives_and_Statuses.md#object-applytosource) | Object  | An object of effects that are applied to the source of the ability (the caster). | 3 | `{ . . . }` |
| `FlatLeechIfDamaged` | `Number` | The flat amount of health leeched when the unit takes damage. | 1 | `3`<br>`5` |
| [`RemoveStatusStacks`](./Miscellaneous.md#object-removestatusstacks) | Object  | An object specifying a status name and the number of stacks to remove from the target. | 1 | `{ . . . }` |
| [`ImmediateUseAbility_Instant`](./Enums.md#enum-immediateuseability_instant) | Enum | Specifies the name of an ability to use instantly as a passive effect. | 1 | `head_CrownOfHorns` |

</details>


---


### Object: `Conditional_OncePerBattle`


**Definition:** An object containing effects that can only trigger once per battle, preventing double-activation.
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HealthThreshold`](./Items_and_Equipment.md#context-conditional_healththreshold), [`StatusOnFullMana`](./Items_and_Equipment.md#context-statusonfullmana)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>	ag |
| [`key`](./Enums.md#enum-key) | Enum | A unique string identifier used to track if an effect has been applied once per turn, preventing reapplication. | 3 | `EtherSoakedRag`<br>`JewelOfDrog`<br>`TaintedOffering` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 3 | Default<br>FormChange<br>Druid |
| [`ShowText`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the localization key for a popup text displayed on the target. | 1 | `"COMBAT_POPUP_BRAINSTORM"`<br>`"COMBAT_POPUP_RELOAD"`<br>`"COMBAT_POPUP_REPAIRED"` |
| [`ReduceManaCost`](./Enums.md) | Integer | The number of stacks reducing mana cost of abilities. | 1 | `1`<br>`2` |
| [`Shield`](./Enums.md) | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 1 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`SpellDamageUp`](./Enums.md) | Integer | The number of stacks of SpellDamageUp applied, increasing spell damage. | 1 | `1`<br>`3` |

</details>


---


### Object: `Craft`


**Definition:** Specifies the loot pool and slot to craft an item for the source.
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusIfUnusedActPoints`](./Items_and_Equipment.md#context-statusifunusedactpoints), [`StatusOnBattleStart`](./Items_and_Equipment.md#context-statusonbattlestart)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`pool`](./Arrays.md#array-pool) | Array / Enum  | Specifies the name of the pool from which an ability is learned or an item is crafted. | 15 | `2`<br>`3`<br>`4` |
| [`slot`](./Enums.md#enum-slot) | Enum / Integer | Specifies the equipment slot (e.g., 'head', 'trinket', 'random_empty') where the crafted item is placed. | 14 | `0`<br>`1`<br>`2` |
| `works_with_tech` | Boolean | If true, the craft effect is compatible with tech-based interactions or abilities. | 4 | `true` |

</details>


---


### Object: `DelayedAutoRevive`


**Definition:** Configures an automatic revival after a delay, with specified rounds and health percentage.
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `health` | Integer | The maximum hit points of the unit. | 6 | `0`<br>`1`<br>`10` |
| `rounds` | Integer | The number of rounds after which the auto-revive triggers. | 6 | `1`<br>`2` |

</details>


---


### Object: `global_passives`


**Definition:** An object containing global passive modifiers that apply to the entire run.
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `GlobalEnemyAutoRevive` | Integer | The percentage chance for all enemies to automatically revive after being defeated. | 2 | `100%`<br>`30%` |
| `NoCorpses` | `Number` | If set to 1, corpses are prevented from spawning. | 1 | `1` |
| `RealTimePressure` | Integer | The number of real-time seconds before a pressure effect or penalty applies. | 1 | `5` |
| [`{Global Modifier Keys}`](./Engine_GlobalModifierKeys.md#valid-property-keys) | Variable | If true, activates a global modifier effect on the house environment. | 1 | `CreateGlobalModifiers`<br>`BloodRain`<br>`NextPlayerCatTakesExtraTurn` |

</details>


---


### Object: `PassiveAtHealthThreshold`


**Definition:** An object that grants additional passives when the unit's health meets a specified threshold, with sub-keys for threshold, mode, and passives.
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`mode`](./Enums.md#enum-mode) | Enum | Specifies the comparison mode (equal, greater, less_or_equal, etc.) used for a conditional check. | 9 | `equal`<br>`greater`<br>`greater_or_equal` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 15 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 9 | `{ . . . }` |
| [`threshold`](./Passives_and_Statuses.md#object-threshold) | Enum / Integer / Object  | The health threshold value, either as a formula using X (max health) or a fixed integer. | 9 | `{ . . . }`<br>`"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |

</details>


---


### Object: `SpawnObjectOnPopCorpse`


**Definition:** Specifies an object (as a string or an object with 'object', 'count', 'except_tiny' keys) to spawn on a corpse when it is popped.
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`count`](./Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 1 | `0`<br>`1`<br>`10` |
| `except_tiny` | Boolean | If true, the spawning effect is not triggered for tiny (small) corpses. | 1 | `true` |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 1 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |

</details>


---


### Object: `StatusOnTakeHealthOrShieldDamage`


**Definition:** An object that applies a status effect when the unit takes damage to either health or shields.
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`DivineShield`](./Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 2 | `1`<br>`2`<br>`4` |
| [`Conditional_GoodRoll`](./Passives_and_Statuses.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 1 | `{ . . . }` |
| `Metronome` | `Number` | The number of times Metronome triggers, or an object with stacks and banned abilities. | 1 | `1`<br>`2` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 1 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `StatusRandomEnemiesOnBattleStart`


**Definition:** An object that applies a status effect to a random number of enemies at the start of battle, with sub-keys for count and the status.
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`count`](./Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 7 | `0`<br>`1`<br>`10` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 7 | passives<br>class<br>	ag |
| [`Fear`](./Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 3 | `1`<br>`10`<br>`2` |
| [`Charmed`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 1 | `1`<br>`2`<br>`3` |
| [`Confusion`](./Enums.md) | Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`10`<br>`2` |
| [`Freeze`](./Arrays.md#array-freeze) | Array / Integer  | The amount of freeze stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`2`<br>`[1 .01]` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `CatchProjectiles`


**Definition:** An object defining chance to catch projectiles and optionally apply statuses.
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ally_chance` | Integer | The percentage chance for an ally to catch incoming projectiles. | 5 | `100%`<br>`15%` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 5 | `.02`<br>`.1`<br>`.15` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 6 | passives<br>class<br>	ag |
| [`Quivered`](./Arrays.md#array-quivered) | Array / Integer  | The amount of quivered stacks applied, or an [stacks, probability] array. | 5 | `1`<br>`2`<br>`5` |

</details>


---


### Object: `ClassManaCostReduction`


**Definition:** Defines a reduction in mana cost for abilities of a specific class.
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `reduction` | Integer | The amount or percentage by which mana cost is reduced. | 7 | `1`<br>`2`<br>`3` |
| [`class`](./Enums.md#enum-class) | Enum | Specifies the class that this ability belongs to, used for categorization and restrictions. | 6 | `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |

</details>


---


### Object: `Conditional_PartyMember`


**Definition:** A conditional block that executes its child actions only if the target is a party member.
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ExtraStatusWhenDealingDamage`](./Items_and_Equipment.md#context-extrastatuswhendealingdamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | passives<br>class<br>	ag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `CounterAttack`


**Definition:** Specifies the ability used when the unit counterattacks after being hit.
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 5 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `melee_only` | Boolean | If true, the counterattack or block effect only triggers in response to melee attacks. | 1 | `true` |
| `ranged_only` | Boolean | If true, the reaction only triggers on ranged attacks. | 1 | `true` |

</details>


---


### Object: `Else`


**Definition:** Contains the fallback effects to apply when a preceding conditional check fails.
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_PartyMember`](./Items_and_Equipment.md#context-conditional_partymember)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 19 | passives<br>class<br>	ag |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 23 | `Default`<br>`FormChange`<br>`Druid` | [`ApplyToSource`](Abilities_and_Spells.md#object-applytosource) | Object | An object of effects that are applied to the source of the ability (the caster). | 14 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `ExtraStatusWhenDealingDamage`


**Definition:** Defines additional statuses applied to the target or source when dealing damage, with conditionals.
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `PassiveWhenDead`


**Definition:** Passive effects that remain active while the unit is dead.
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `SetItemAux`


**Definition:** Configures an item's auxiliary value by specifying a target slot and a formula for the new value.
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Shielded`](./Items_and_Equipment.md#context-conditional_shielded), [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`slot`](./Enums.md#enum-slot) | Enum / Integer | Specifies the equipment slot (e.g., 'head', 'trinket', 'random_empty') where the crafted item is placed. | 3 | `0`<br>`1`<br>`2` |
| [`value`](./Math_Equations.md) | Equation | The numeric value or formula associated with the buff. | 3 | `.5`<br>`0`<br>`1` |

</details>


---


### Object: `SpawnExtraThingsOnBattleStart`


**Definition:** An object with `object` and `number` (or range) defining what and how many objects to spawn at battle start.
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`number`](./Arrays.md#array-number) | Array / Integer | The number of objects to spawn; can be a single integer or an array `[min, max]` for a random range. | 31 | `1`<br>`10`<br>`2` |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 23 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |

</details>


---


### Object: `SpawnOnBattleStartRandomEmptyTile`


**Definition:** Specifies an object that spawns on a random empty tile at the start of battle.
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 11 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`number`](./Arrays.md#array-number) | Array / Integer | The number of objects to spawn; can be a single integer or an array `[min, max]` for a random range. | 10 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `StackingFlowerTrail`


**Definition:** An object defining how a flower trail status stacks (stacks count, stack key) when the unit moves.
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`stack_key`](./Enums.md#enum-stack_key) | Enum | Specifies the key of the status stack to check for the condition. | 3 | `CATHIDE`<br>`EMPTY_GENERATOR`<br>`FANNY_PACK` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 3 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |

</details>


---


### Object: `StatusAllCharactersOnSpawn`


**Definition:** Defines status effects applied to all characters when they spawn into the battlefield.
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 | `Default`<br>`FormChange`<br>`Druid` | [`Conditional_Boss`](Abilities_and_Spells.md#object-conditional_boss) | Object || 0 | Default<br>FormChange<br>Druid |
| [`Poison`](./Enums.md) | Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `StatusEveryXSpellCasts`


**Definition:** An object with `stacks` (number of spell casts) and status effects to apply after that many spell casts.
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 8 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 9 | passives<br>class<br>	ag |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 | `Default`<br>`FormChange`<br>`Druid` | [`Charge`](./Enums.md) | Integer | The number of charge stacks applied. | 3 | Default<br>FormChange<br>Druid |
| [`IntelligenceUp`](./Enums.md) | Array / Equation | The amount of Intelligence added as a flat bonus. | 1 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| [`ObjectOnHitCharacter`](./Passives_and_Statuses.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 1 | `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |

</details>


---


### Object: `StatusOnPopCorpse`


**Definition:** Specifies the effects applied when the unit pops a corpse.
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 5 | passives<br>class<br>	ag |
| [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 3 | `1`<br>`10`<br>`2` |
| [`RepairTrinket`](./Enums.md) | Integer | The number of stacks of the Repair Trinket status effect to apply. | 1 | `1`<br>`99` |
| [`RepairWeapon`](./Arrays.md#array-repairweapon) | Array / Integer  | The number of weapon durability points restored; an array [stacks, probability] applies a chance-based repair. | 1 | `1`<br>`6`<br>`99` |

</details>


---


### Object: `StatusOnTurnEndIfDidntCastAbilityTypes`


**Definition:** Applies the contained status effects at turn end if the unit did not cast an ability of the specified type(s).
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 5 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 4 | passives<br>class<br>	ag |
| [`Charge`](./Enums.md) | Equation | The number of charge stacks applied. | 1 | `1`<br>`2`<br>`3` |
| [`DamageUp`](./Enums.md) | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 1 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 1 | `1`<br>`2`<br>`3` |
| [`Shield`](./Enums.md) | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 1 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`SpellDamageUp`](./Enums.md) | Integer | The number of stacks of SpellDamageUp applied, increasing spell damage. | 1 | `1`<br>`3` |
| [`Thorns`](./Enums.md) | Integer | The amount of thorns damage dealt to attackers on hit. | 1 | `1`<br>`2`<br>`3` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `AddStatusToElementDamage`


**Definition:** An object that applies a specific status effect when dealing damage of a specified element. Contains sub-keys for the element and the status to apply.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 6 | `Electric`<br>`Fire`<br>`Gravity` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 8 | passives<br>class<br>	ag |
| [`Burn`](./Enums.md) | Equation | The amount of Burn applied, either as a fixed number or a formula string. | 3 | `1`<br>`10`<br>`2` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid` | [`Stun`](./Enums.md) | Array | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `AddStatusToKnockbackDamage`


**Definition:** An object whose nested keys define statuses applied to damage caused by knockback.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `AddStatusToSpells`


**Definition:** Specifies status effects added to all spell attacks used by this unit.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `ApplyStatusesToRandomEnemiesEachTurn`


**Definition:** An object specifying statuses to apply to random enemies each turn, with an optional 'count' field.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 4 | passives<br>class<br>	ag |
| [`Bounty`](./Enums.md) | Integer | The number of bounty stacks applied to enemies, increasing rewards on defeat. | 3 | `1`<br>`3` |
| [`count`](./Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 2 | `0`<br>`1`<br>`10` |
| [`Marked`](./Enums.md) | Integer | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`3`<br>`5` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `ArmorBreakOnHit`


**Definition:** An object defining durability loss and chance for armor to break when hit.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance_to_break` | Integer | The percentage chance that the armor breaks on hit. | 2 | `10%`<br>`5%` |
| `durability_loss` | Integer | The amount of durability lost when the armor break effect triggers. | 2 | `0` |

</details>


---


### Object: `bonus_passives`


**Definition:** Grants temporary passive abilities to the caster for the duration of the ability.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`str_aux_is_copy_ability`](./Items_and_Equipment.md#context-str_aux_is_copy_ability)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 125 | passives<br>class<br>	ag |
| [`ModifyAbility`](./Miscellaneous.md#object-modifyability) | Object | Specifies the modifications to an ability's properties, such as cost or type. | 2 | `{ . . . }` |

</details>


---


### Object: `BoostWeaponDamage`


**Definition:** The amount of bonus weapon damage applied, or an object with `damage` and `crit_chance` fields.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `crit_chance` | `Equation` | The chance for the damage instance to critically hit, expressed as a percentage or equation; values above 1 default to 100%. | 4 | `-999999`<br>`.05*X`<br>`.25` |
| [`damage`](./Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 4 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 4 | `damage_instance`<br>`spell`<br>`self_damage` |

</details>


---


### Object: `ChanceToBackflip`


**Definition:** An object specifying the ability to use and the percentage chance to perform a backflip dodge when hit.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 6 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 6 | `.02`<br>`.1`<br>`.15` |

</details>


---


### Object: `ChanceToBlockAndCounter`


**Definition:** The percentage chance or an object defining chance and conditions to block and counter an attack.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `backstab_only` | Boolean | If true, the block and counter effect only triggers on attacks made from behind the target. | 1 | `true` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |

</details>


---


### Object: `Conditional_Adjacent`


**Definition:** An object whose nested keys define statuses or effects applied to or by units that are adjacent to the unit.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ScaledStatusAlliesOnSpendMana`](./Items_and_Equipment.md#context-scaledstatusalliesonspendmana), [`StatusAlliesEachTurn`](./Items_and_Equipment.md#context-statusallieseachturn)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 | passives<br>class<br>	ag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |
| [`Conditional_Ally`](./Passives_and_Statuses.md#object-conditional_ally) | Object | Defines effects that apply only if the target is an ally, with an optional else block for non-allies. | 1 | `{ . . . }` |
| [`Conditional_PlayerCat`](./Miscellaneous.md#object-conditional_playercat) | Object | Defines effects that only apply if the target is a player-controlled cat. | 1 | `{ . . . }` |

</details>


---


### Object: `Conditional_BadRoll`


**Definition:** An object containing an `odds` value and effects that are applied when a random roll succeeds.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnBegin`](./Items_and_Equipment.md#context-statuseachturnbegin)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`odds`](./Enums.md#enum-odds) | Float | The probability of the effect occurring, expressed as a decimal or percentage. | 8 | `.1`<br>`.16666666`<br>`.3` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 6 | passives<br>class<br>	ag |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 8 | `Default`<br>`FormChange`<br>`Druid` | [`Temporary`](Abilities_and_Spells.md#object-temporary) | Object | Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions. | 8 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `Conditional_Boss`


**Definition:** Contains effects that apply only if the target is a boss enemy.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusAllCharactersOnSpawn`](./Items_and_Equipment.md#context-statusallcharactersonspawn)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 7 | passives<br>class<br>	ag |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 6 | `Default`<br>`FormChange`<br>`Druid` | [`AllStatsUp`](./Enums.md) | Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 14 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `cost`


**Definition:** Defines the resource cost (e.g., mana) and other casting requirements.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ModifyAbility`](./Items_and_Equipment.md#context-modifyability)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `mana` | Equation | The amount of mana required to cast, as a formula or stat. | 1605 | `"4-clamp(floor(X/7), 0, 1)"`<br>`"max(4-X, 0)"`<br>`"max(7-2*X,0)"` |
| `charge` | Equation | The amount of charge required or the formula to calculate charge cost. | 18 | `"1-clamp(spd,0,1)"`<br>`0`<br>`1` |

</details>


---


### Object: `CreateGlobalModifiers`


**Definition:** Defines global gameplay modifiers to activate.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnDie`](./Items_and_Equipment.md#context-statusondie), [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Global Modifier Keys}`](./Engine_GlobalModifierKeys.md#valid-property-keys) | Variable | If true, activates a global modifier effect on the house environment. | 5 | `CreateGlobalModifiers`<br>`BloodRain`<br>`NextPlayerCatTakesExtraTurn` |
| `NextPlayerCatTakesExtraTurn` | `Number` | The number of extra turns the active player cat gains. | 1 | `1` |
| `NoCorpses` | `Number` | If set to 1, corpses are prevented from spawning. | 1 | `1` |

</details>


---


### Object: `DoDamage`


**Definition:** Contains damage parameters (amount, type, tile targets) to deal damage to the target.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachRoundEnd`](./Items_and_Equipment.md#context-statuseachroundend), [`StatusOnBreakItem`](./Items_and_Equipment.md#context-statusonbreakitem)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 7 | passives<br>class<br>	ag |
| [`damage`](./Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 7 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 7 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 7 | `damage_instance`<br>`spell`<br>`self_damage` |
| [`damage_tiles`](./Enums.md#enum-damage_tiles) | Enum | Specifies whether the damage effect applies to tiles; 'all' damages every tile in the area. | 4 | `all` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 4 | `{ . . . }` |

</details>


---


### Object: `ElementalManaCostReduction`


**Definition:** An object that reduces the mana cost of spells of specified elements, with sub-keys for element and reduction amount.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `reduction` | Integer | The amount or percentage by which mana cost is reduced. | 5 | `1`<br>`2`<br>`3` |
| [`element`](./Arrays.md#array-element) | Array / Enum | Specifies which element(s) the conditional checks against. | 5 | `Electric`<br>`Fire`<br>`Gravity` |

</details>


---


### Object: `ImmediateUseAbility`


**Definition:** Specifies the name of an ability to be triggered instantly from this effect.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnEnd`](./Items_and_Equipment.md#context-statuseachturnend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 1 | `true` |

</details>


---


### Object: `keyword_tooltips`


**Definition:** Associates keyword tooltips with the ability, often used for status effects.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 11 | passives<br>class<br>	ag |
| [`DivineShield`](./Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | `1`<br>`2`<br>`4` |
| [`Immobile`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 1 | `0`<br>`1`<br>`10%` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `meta`


**Definition:** Contains metadata for the ability including name, description, class, and type icon.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ModifyAbility`](./Items_and_Equipment.md#context-modifyability)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `is_basic_attack` | Boolean | If true, this ability is treated as a basic attack, typically used for default melee or ranged strikes without special properties. | 6 | `false`<br>`true` |
| `is_weapon` | Boolean | If true, this ability is classified as a weapon, allowing it to benefit from weapon-specific modifiers and UI grouping. | 4 | `true` |

</details>


---


### Object: `ModifyAbility`


**Definition:** Specifies the modifications to an ability's properties, such as cost or type.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Items_and_Equipment.md#context-bonus_passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 2 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 2 | `{ . . . }` |

</details>


---


### Object: `MovementReaction`


**Definition:** Specifies an ability to cast when a unit moves within range, with options for targeting and conditions.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveWhileHasDurability`](./Items_and_Equipment.md#context-passivewhilehasdurability), [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 11 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `enemies_only` | Boolean | If true, the arc lightning effect only chains to enemy units, ignoring allies. | 7 | `false`<br>`true` |
| `on_self_move_too` | Boolean | If true, the reaction triggers when the unit themselves move. | 3 | `true` |
| `create_temp_ability` | Boolean | If true, a temporary ability slot is created during movement reactions. | 2 | `true` |

</details>


---


### Object: `ObjectOnHitCharacter`


**Definition:** Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEveryXSpellCasts`](./Items_and_Equipment.md#context-statuseveryxspellcasts), [`StatusOnBattleStart`](./Items_and_Equipment.md#context-statusonbattlestart)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 7 | passives<br>class<br>	ag |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 7 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`stacks`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 5 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |

</details>


---


### Object: `passive`


**Definition:** Defines the passive form, where the unit does nothing (uses DoNothing attack) and is inactive.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`Metal`](./Enums.md) | Integer | The number of armor stacks or metal keyword effects. | 2 | `1` |

</details>


---


### Object: `PassiveAtStatThreshold`


**Definition:** An object defining passives granted when a unit's stat meets a specified threshold.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 31 | passives<br>class<br>	ag |
| [`mode`](./Enums.md#enum-mode) | Enum | Specifies the comparison mode (equal, greater, less_or_equal, etc.) used for a conditional check. | 13 | `equal`<br>`greater`<br>`greater_or_equal` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 13 | `{ . . . }` |
| [`threshold`](./Passives_and_Statuses.md#object-threshold) | Enum / Integer / Object  | The health threshold value, either as a formula using X (max health) or a fixed integer. | 13 | `{ . . . }`<br>`"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |

</details>


---


### Object: `PassiveIfWeaponIsUsable`


**Definition:** Activates a set of passive effects (e.g., Brace) only if the unit's current weapon is in a usable condition (not broken or disabled).
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`Brace`](./Enums.md) | Array / Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 2 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `RefreshEquipmentAbilityOnElement`


**Definition:** Refreshes the cooldown of the unit's equipment ability when the unit's attack matches the specified element (e.g., Electric), displaying a recharge popup.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 2 | `Electric`<br>`Fire`<br>`Gravity` |
| [`text`](./Strings.md#string-text) | String | The localization key for the name of this injury. | 2 | `""`<br>`"COMBAT_POPUP_RECHARGED"`<br>`"INJURY_NAME_BROKENLEG"` |

</details>


---


### Object: `SpawnItemLinkedFamiliar`


**Definition:** An object defining a familiar to spawn that is linked to a specific item, which breaks when the familiar is defeated.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `break_on_pop_only` | Boolean | If true, the linked familiar spawn only breaks when the item is popped. | 2 | `true` |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 2 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |

</details>


---


### Object: `StatusAfterCastSpell`


**Definition:** An object containing status effects to apply to the unit immediately after it casts any spell.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 4 | `Default`<br>`FormChange`<br>`Druid` | [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 | Default<br>FormChange<br>Druid |
| [`TempMeleeRangeUp`](./Enums.md) | Integer | The number of tiles added to the unit's melee attack range as a temporary buff. | 1 | `1` |
| [`TempRangeUp`](./Enums.md) | Integer | The amount of temporary range increase applied. | 1 | `1`<br>`2`<br>`20` |
| [`UseAbility`](./Enums.md#enum-useability) | Enum  | The name of the ability the target is forced to use. | 1 | `GirlDinoPoop`<br>`KirbySpit`<br>`MD_PoopChain` |

</details>


---


### Object: `StatusAfterXStacks`


**Definition:** Defines a condition that triggers a status effect when a specified stack key reaches a threshold, optionally expiring at turn end.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ScaledStatusOnSpendMana`](./Items_and_Equipment.md#context-scaledstatusonspendmana), [`StatusOnCollectPickup`](./Items_and_Equipment.md#context-statusoncollectpickup)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`stack_key`](./Enums.md#enum-stack_key) | Enum | Specifies the key of the status stack to check for the condition. | 2 | `CATHIDE`<br>`EMPTY_GENERATOR`<br>`FANNY_PACK` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`threshold`](./Passives_and_Statuses.md#object-threshold) | Enum / Integer / Object  | The health threshold value, either as a formula using X (max health) or a fixed integer. | 2 | `{ . . . }`<br>`"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |
| `expires_on_end_turn` | Boolean | If true, the temporary effect expires at the end of the target's turn. | 1 | `true` |
| [`ExtraBasicMoves_Status`](./Enums.md) | Integer | The number of extra basic moves per turn granted. | 1 | `1` |
| [`RefreshActPoints`](./Enums.md) | Integer | The amount of action points restored to the source. | 1 | `1` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusIfUnusedActPoints`


**Definition:** An object containing status effects to apply to the unit if it has unused action points at the end of its turn.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `StatusOnAllyCatDeath`


**Definition:** An object listing status effects applied to the unit when an allied cat dies.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 5 | passives<br>class<br>	ag |
| [`DivineShield`](./Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | `1`<br>`2`<br>`4` |
| [`RepairTrinket`](./Enums.md) | Integer | The number of stacks of the Repair Trinket status effect to apply. | 1 | `1`<br>`99` |

</details>


---


### Object: `StatusOnBackstab`


**Definition:** An object containing status effects to apply when the unit performs a backstab attack.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SerratedClaws` | Integer | The number of stacks of the SerratedClaws status applied, or an object defining its display strings. | 1 | `1` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 1 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `StatusOnBreakItem`


**Definition:** An object containing status effects to apply when the unit breaks a weapon or armor item.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>	ag |
| [`Shield`](./Enums.md) | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 2 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`DoDamage`](./Miscellaneous.md#object-dodamage) | Object  | Contains damage parameters (amount, type, tile targets) to deal damage to the target. | 1 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusOnCastSpell`


**Definition:** An object listing status effects applied to the unit whenever it casts a spell.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 5 | passives<br>class<br>	ag |
| [`Charge`](./Enums.md) | Equation | The number of charge stacks applied. | 4 | `1`<br>`2`<br>`3` |
| [`Shield`](./Enums.md) | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 1 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusOnGainCoins`


**Definition:** Specifies status effects applied when this unit gains coins.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 4 | passives<br>class<br>	ag |
| [`LuckUp`](./Enums.md) | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 1 | `-1`<br>`-2`<br>`-4` |
| [`Shield`](./Enums.md) | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 1 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `str_aux_is_copy_ability`


**Definition:** An object defining bonus passives and ability modifications for an auxiliary ability that is copied.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bonus_passives`](./Miscellaneous.md#object-bonus_passives) | Object  | Grants temporary passive abilities to the caster for the duration of the ability. | 2 | `{ . . . }` |

</details>


---


### Object: `threshold`


**Definition:** The health threshold value, either as a formula using X (max health) or a fixed integer.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveAtStatThreshold`](./Items_and_Equipment.md#context-passiveatstatthreshold)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`int`](./Enums.md#enum-int) | Enum / Integer | The Intelligence stat value or modifier. | 8 | `-1`<br>`-10`<br>`-2` |
| [`con`](./Enums.md#enum-con) | Enum / Integer  | The Constitution stat value or modifier. | 1 | `-1`<br>`-2`<br>`-3` |

</details>


---


### Object: `AbilityHealthThreshold`


**Definition:** Defines an ability and conditions for its activation when the unit's health reaches a threshold.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 13 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 12 | passives<br>class<br>	ag |
| [`threshold`](./Passives_and_Statuses.md#object-threshold) | Enum / Integer / Object  | The health threshold value, either as a formula using X (max health) or a fixed integer. | 12 | `{ . . . }`<br>`"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 7 | `true` |
| `immediate` | Boolean | If true, the action (e.g., attack) occurs instantly without waiting for the unit's turn in the initiative order. | 6 | `false`<br>`true` |
| `aux` | Integer | An auxiliary integer value used for item properties, such as hunger value. | 1 | `-1`<br>`1`<br>`10` |

</details>


---


### Object: `AbilityOnRoundEndOnce`


**Definition:** Specifies an ability to be used once at the end of the round.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `even_of_stunned` | Boolean | If true, the ability triggers only on even rounds and when the unit is stunned. | 1 | `true` |

</details>


---


### Object: `AddAdvantageToEvent`


**Definition:** Specifies additional advantage options to add to a specific event type.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`add`](./Arrays.md#array-add) | Array / Integer | The amount or an array of values added to the event's advantage or item tint. | 1 | `5`<br>`[0.05 0.05 0.05]` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`options`](./Arrays.md#array-options) | Array | An array of named option objects within an event, each defining a possible action the player can take. | 1 | `[smash bash open]` |

</details>


---


### Object: `AddPassivesToCharmed`


**Definition:** Grants the contained passive effects to units under the charm status.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 9 | passives<br>class<br>	ag |
| [`AllStatsUp`](./Enums.md) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | `-1`<br>`-2`<br>`1` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `AddSelfStatusToWeapons`


**Definition:** An object whose nested keys define status effects applied to the unit's own weapons.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `AddStatusToBackstabs`


**Definition:** An object defining statuses applied to the target when the unit performs a backstab attack.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`Bleed`](./Enums.md) | Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `AddStatusToWeapons`


**Definition:** Specifies status effects to add to the unit's weapon attacks, with their stack counts.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 4 | passives<br>class<br>	ag |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 | `Default`<br>`FormChange`<br>`Druid` | [`Leech`](./Enums.md) | Integer | The amount of health leeched from the target (heals the attacker). | 3 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `AddTemporaryEffectsToBasicAttack`


**Definition:** A container object that lists temporary status effects applied to the unit's basic attack.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CastAgainWithStatus`](./Miscellaneous.md#object-castagainwithstatus) | Object  | Defines parameters for recasting an ability when the unit has the specified status effect. | 1 | `{ . . . }` |

</details>


---


### Object: `AIControlNextTurn`


**Definition:** An object that causes the unit to be controlled by the AI on its next turn, with configurable stacks and spell usage.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `include_spells` | Boolean | If true, the AI-controlled bonus turn includes spells as available actions. | 1 | `true` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |

</details>


---


### Object: `AlluringDoodieEater`


**Definition:** An object defining the chance and damage instance for a unit that consumes an alluring doodie.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |

</details>


---


### Object: `AllyDodgeChanceAura`


**Definition:** An object granting allies within a specified range a percentage chance to dodge incoming attacks.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |
| [`range`](./Enums.md#enum-range) | Enum / Integer  | The distance in tiles for the trigger effect; `global` means any distance. | 1 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `ApplyPassives`


**Definition:** Specifies the passives or status effects to apply to the unit.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_RandomChance`](./Items_and_Equipment.md#context-conditional_randomchance)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 13 | passives<br>class<br>	ag |
| [`StatusOnBattleEnd`](./Passives_and_Statuses.md#object-statusonbattleend) | Object  | An object containing status effects or passives applied to the unit when the battle ends. | 5 | `{ . . . }` |

</details>


---


### Object: `ApplyToRandomPartyMemberIfPossible`


**Definition:** Contains an inner effect block that is applied to a random living party member if one exists.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBreak`](./Items_and_Equipment.md#context-statusonbreak)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `AutocastEachRound`


**Definition:** Contains an ability name and optional 'even_if_stunned' flag to autocast each round.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveWhenDead`](./Items_and_Equipment.md#context-passivewhendead)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 9 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 6 | `true` |

</details>


---


### Object: `BackflipWhenTargeted`


**Definition:** The number of backflip charges, or an object defining its ability.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 7 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 7 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |

</details>


---


### Object: `BouncyProjectiles`


**Definition:** An object with 'max_bounces' and 'max_range' defining projectile bounciness behavior.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max_bounces` | Integer | The maximum number of bounces for a projectile; -1 means infinite. | 3 | `-1`<br>`1`<br>`10` |
| [`max_range`](./Enums.md#enum-max_range) | Enum / Integer | The maximum range of the ability, can be a static number or an expression. | 3 | `"4+(1-clamp(spd,0,1))*2"`<br>`"max(5-int, 1)"`<br>`-1` |

</details>


---


### Object: `BuffImmunity`


**Definition:** If 1, the unit is immune to buffs. An optional object can list buffs to exclude from immunity.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exclude`](./Enums.md#enum-exclude) | Enum | Specifies an element or effect that does not trigger the form change. | 1 | `SpellDamageUp`<br>`fire`<br>`water` |

</details>


---


### Object: `CastAgainWithStatus`


**Definition:** Defines parameters for recasting an ability when the unit has the specified status effect.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddTemporaryEffectsToBasicAttack`](./Items_and_Equipment.md#context-addtemporaryeffectstobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>	ag |
| `OverrideDamage` | `Number` | Overrides the damage of the current action to this flat value (can be negative to heal). | 1 | `-10`<br>`0`<br>`1` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `CatPartsSizeScale`


**Definition:** A multiplier for the size of specific cat parts (e.g., head, body).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`head`](./Enums.md#enum-head) | Enum / Float  | The catalog ID for the cat's head part. | 1 | `-1`<br>`1`<br>`1.3` |

</details>


---


### Object: `ChanceToForceEvent`


**Definition:** Defines the chance and the specific event to force to occur.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |
| [`event`](./Enums.md#enum-event) | Enum | Specifies the event to force, either by name or by a nested object defining its type and level. | 1 | `Blessing`<br>`Death`<br>`Tragedy` |

</details>


---


### Object: `Conditional_Ally`


**Definition:** Defines effects that apply only if the target is an ally, with an optional else block for non-allies.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Adjacent`](./Items_and_Equipment.md#context-conditional_adjacent)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 21 | passives<br>class<br>	ag |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 8 | `Default`<br>`FormChange`<br>`Druid` | [`ManaGain`](./Enums.md) | Integer | The amount of mana restored to the source, which can be an expression. | 4 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `Conditional_Corpse`


**Definition:** Contains an inner effect block that only executes if the target is a corpse.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>	ag |
| [`RandomMutation`](./Enums.md) | Integer | The number of random mutations to apply. | 1 | `1`<br>`3` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `Conditional_Enemy`


**Definition:** An object containing status effects or actions applied only if the target is an enemy.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToSpells`](./Items_and_Equipment.md#context-addstatustospells)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 6 | passives<br>class<br>	ag |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 12 | `Default`<br>`FormChange`<br>`Druid` | [`Leeches`](./Enums.md) | Integer | The number of stacks of the Leeches debuff applied, which deals damage over time and heals the applier. | 8 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `Conditional_HasTag`


**Definition:** Evaluates whether the target has a specific tag; if true, applies the effects within; otherwise, runs the Else block.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToAllDamage`](./Items_and_Equipment.md#context-addstatustoalldamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](./Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 46 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 49 | passives<br>class<br>	ag |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 11 | `Default`<br>`FormChange`<br>`Druid` | [`BonusKnockbackDamage`](./Enums.md) | Integer || 43 | Default<br>FormChange<br>Druid |
| [`OverrideChainKnockback`](./Enums.md) | Integer | The custom number of tiles for chain knockback, overriding the default. | 1 | `0`<br>`1`<br>`10` |

</details>


---


### Object: `Conditional_HealthThreshold`


**Definition:** Contains an inner effect block that only executes if the target's health is below a threshold, defined by `threshold_flat`, `threshold_percent`, or `threshold_expr`.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnTookDamage`](./Items_and_Equipment.md#context-statusontookdamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | passives<br>class<br>	ag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 7 | Default<br>FormChange<br>Druid |
| `threshold_flat` | Integer | The flat health value (in hit points) below which the target must be for the conditional to trigger. | 5 | `0`<br>`10`<br>`3` |
| [`Conditional_OncePerBattle`](./Miscellaneous.md#object-conditional_onceperbattle) | Object  | An object containing effects that can only trigger once per battle, preventing double-activation. | 1 | `{ . . . }` |

</details>


---


### Object: `Conditional_ManaThreshold`


**Definition:** Defines a conditional block that applies effects only if a unit's mana meets a specified threshold.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnEnd`](./Items_and_Equipment.md#context-statuseachturnend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `threshold_flat` | Integer | The flat health value (in hit points) below which the target must be for the conditional to trigger. | 1 | `0`<br>`10`<br>`3` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`RepairTrinket`](./Enums.md) | Integer | The number of stacks of the Repair Trinket status effect to apply. | 1 | `1`<br>`99` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 1 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `Conditional_PlayerCat`


**Definition:** Defines effects that only apply if the target is a player-controlled cat.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Adjacent`](./Items_and_Equipment.md#context-conditional_adjacent)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>	ag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 1 | Default<br>FormChange<br>Druid |
| [`Charge`](./Enums.md) | Equation | The number of charge stacks applied. | 1 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `Conditional_RandomChance`


**Definition:** An object containing effects that execute only if a random roll succeeds, with an odds value defined inside.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnDie`](./Items_and_Equipment.md#context-statusondie)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `odds` | Float | The probability of the effect occurring, expressed as a decimal or percentage. | 4 | `.1`<br>`.16666666`<br>`.3` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 4 | Default<br>FormChange<br>Druid |
| [`ApplyPassives`](./Miscellaneous.md#object-applypassives) | Object  | Specifies the passives or status effects to apply to the unit. | 2 | `{ . . . }` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>	ag |

</details>


---


### Object: `Conditional_Shielded`


**Definition:** An object containing effects that are only applied if the target has a shield active.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | passives<br>class<br>	ag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 2 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `ConvertDamageToScaledStatus`


**Definition:** Converts a portion of incoming damage into a specified status effect with a given number of stacks.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`DelayedPain`](./Enums.md) | Integer | The number of stacks of DelayedPain applied, dealing damage after a delay. | 1 | `1` |

</details>


---


### Object: `CritsApplyStatus`


**Definition:** An object containing statuses applied to the target when the unit lands a critical hit.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 6 | passives<br>class<br>	ag |
| [`Fear`](./Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `damage_instance`


**Definition:** Defines damage properties, effects, and healing for the ability's direct damage.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AlluringDoodieEater`](./Items_and_Equipment.md#context-alluringdoodieeater)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 1731 | `damage_instance`<br>`spell`<br>`self_damage` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 1787 | `{ . . . }` |
| [`damage`](./Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 1447 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 359 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


<details>
<summary><b>AddSelfStatusToWeapons</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>	ag |

</details>
<details>
<summary><b>AddStatusToKnockbackDamage</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>	ag |

</details>
<details>
<summary><b>AddStatusToSpells</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |

</details>
<details>
<summary><b>ApplyToRandomPartyMemberIfPossible</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>	ag |

</details>
<details>
<summary><b>Conditional_Adjacent</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>	ag |

</details>
<details>
<summary><b>Conditional_HealthThreshold</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |

</details>
<details>
<summary><b>Conditional_PartyMember</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>	ag |

</details>
<details>
<summary><b>Conditional_Shielded</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>	ag |

</details>
<details>
<summary><b>ExtraStatusWhenDealingDamage</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |

</details>
<details>
<summary><b>PassiveWhenDead</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>	ag |

</details>
<details>
<summary><b>PassiveWhileHasDurability</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>	ag |

</details>
<details>
<summary><b>ScaledStatusAlliesOnSpendMana</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>	ag |

</details>
<details>
<summary><b>StatusAlliesEachTurn</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |

</details>
<details>
<summary><b>StatusIfUnusedActPoints</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>	ag |

</details>
<details>
<summary><b>StatusOnEndMove</b></summary>

> **Total Count:** 9

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 8 | passives<br>class<br>	ag |

</details>
<details>
<summary><b>StatusOnFallAsleep</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>	ag |

</details>


### Object: `DestroyEquipmentAndAttachParasite`


**Definition:** Attempts to destroy a random piece of the target's equipment and attach a parasite from the specified pool.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleStart`](./Items_and_Equipment.md#context-statusonbattlestart)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`pool`](./Arrays.md#array-pool) | Array / Enum | Specifies the name of the pool from which an ability is learned or an item is crafted. | 6 | `2`<br>`3`<br>`4` |
| [`chance`](./Enums.md#enum-chance) | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 4 | `.02`<br>`.1`<br>`.15` |

</details>


---


### Object: `Eternal`


**Definition:** Defines the Eternal revival effect, setting stacks and the health percentage restored.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `health_percent` | Integer | The amount of health (as a percentage) the unit retains after being revived or survived a fatal hit. | 3 | `100%`<br>`50%` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 3 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |

</details>


---


### Object: `FlyDamageIncrease`


**Definition:** The number of stacks or alias for damage increase against flying units.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allies_only` | Boolean | If true, the effect only applies to allied units. | 1 | `false`<br>`true` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |

</details>


---


### Object: `ForceUseAbilityOnTarget`


**Definition:** Defines a chance to force the unit to use a specified ability on the target.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Items_and_Equipment.md#context-addstatustobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |

</details>


---


### Object: `GlobalMeleeRevengeDamage`


**Definition:** Defines revenge damage properties (e.g., knockback) when hit by a melee attack.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`knockback`](./Enums.md#enum-knockback) | Enum / Integer  | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 1 | `"ceil(X*.25/5)"`<br>`-10`<br>`-2` |

</details>


---


### Object: `KnockbackIfCrit`


**Definition:** Defines knockback properties applied when a critical hit occurs.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToAllDamage`](./Items_and_Equipment.md#context-addstatustoalldamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`knockback`](./Enums.md#enum-knockback) | Enum / Integer  | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 1 | `"ceil(X*.25/5)"`<br>`-10`<br>`-2` |
| `override_chain_knockback` | Integer | The distance in tiles the unit is knocked back if a critical hit triggers chain knockback. | 1 | `10` |

</details>


---


### Object: `KnockUpAndAway`


**Definition:** Contains parameters for launching the target upward and away from the source, including stacks and distance.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Items_and_Equipment.md#context-addstatustobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `distance` | Integer | The number of tiles the target is knocked back or pulled. | 24 | `-3`<br>`10`<br>`2` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 22 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |

</details>


---


### Object: `ManaGainRange`


**Definition:** Defines the minimum and maximum mana gained per turn.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnBegin`](./Items_and_Equipment.md#context-statuseachturnbegin)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max` | Integer | The maximum amount of coins that can be gained. | 1 | `10`<br>`2`<br>`25` |
| `min` | Integer | The minimum amount of coins that will be gained. | 1 | `0`<br>`1`<br>`10` |

</details>


---


### Object: `ObjectDetector`


**Definition:** An object that grants a chance to detect a specific item (e.g., CharmedDip) when loot is evaluated.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 1 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |

</details>


---


### Object: `PassiveAfterXKills`


**Definition:** Activates a set of passive effects (e.g., extra attacks, stat boosts) after the unit achieves a certain number of kills defined by the 'stacks' sub-key.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 4 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 8 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 4 | `{ . . . }` |

</details>


---


### Object: `PassiveWhenAffectedByElement`


**Definition:** An object containing `element` and `passives` that grants the listed passives while the unit is affected by the specified element.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 18 | `Electric`<br>`Fire`<br>`Gravity` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 30 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 18 | `{ . . . }` |

</details>


---


### Object: `PassiveWhileHasDurability`


**Definition:** An object containing passives that are active only while the item has remaining durability.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `PassiveWhileInMonkMeleeStance`


**Definition:** Applies specific passive effects (e.g., Brace, HealthRegenUp) while the unit is in the Monk's melee combat stance.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>	ag |
| [`Brace`](./Enums.md) | Array / Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 3 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `PassiveWhileShielded`


**Definition:** An object containing passives that are active only while the unit has a shield.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 1 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `PoopWhenHit`


**Definition:** Specifies the object (e.g., Poop) spawned when the unit is hit, or an object with `chance` and `object`.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 1 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |

</details>


---


### Object: `RandomStatusFromPool`


**Definition:** A collection of status effects; one is randomly chosen and applied to the target.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnDie`](./Items_and_Equipment.md#context-statusondie)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 31 | passives<br>class<br>	ag |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 12 | `Default`<br>`FormChange`<br>`Druid` | [`PermanentCharisma`](./Enums.md) | Integer | The amount of permanent Charisma added to the unit's base stats. | 24 | Default<br>FormChange<br>Druid |
| [`PermanentConstitution`](./Enums.md) | Integer | The amount of permanent Constitution stat added or removed. | 1 | `-1`<br>`-2`<br>`1` |
| [`PermanentDexterity`](./Enums.md) | Integer | The permanent amount of dexterity added or removed. | 1 | `1`<br>`2` |
| [`PermanentIntelligence`](./Enums.md) | Integer | The permanent amount of intelligence added or removed. | 1 | `-1`<br>`1`<br>`2` |
| [`PermanentLuck`](./Enums.md) | Integer | The amount of permanent Luck added to the unit's base stats. | 1 | `1`<br>`2` |
| [`PermanentSpeed`](./Enums.md) | Integer | The permanent amount of speed added or removed. | 1 | `-1`<br>`1`<br>`2` |
| [`PermanentStrength`](./Enums.md) | Integer | The amount of permanent bonus strength (physical damage modifier) granted. | 1 | `1`<br>`2` |

</details>


---


### Object: `RemoveStatusStacks`


**Definition:** An object specifying a status name and the number of stacks to remove from the target.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasStatus`](./Items_and_Equipment.md#context-conditional_hasstatus)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 | passives<br>class<br>	ag |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 4 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 4 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |

</details>


---


### Object: `ReviveNextRound`


**Definition:** The number of revives granted, or an object defining revive properties.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleStart`](./Items_and_Equipment.md#context-statusonbattlestart)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `revive_health` | Integer | The amount of health (as a flat integer or percentage) the unit revives with. | 4 | `1`<br>`100%`<br>`50%` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`Shield`](./Enums.md) | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 3 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `ScaldingOrbMoonBossOneShot`


**Definition:** An object that completes the ScaldingOrb quest and removes the item from the unit's inventory.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CompleteItemQuest`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the item quest ID to mark as complete on kill. | 1 | `BlackShard`<br>`Nuke`<br>`ScaldingOrb` |
| [`RemoveItem`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the item ID to remove from the source on kill. | 1 | `BlackShard`<br>`BlackShard_Glowing`<br>`ScaldingOrb` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `ScaledStatusAlliesOnSpendMana`


**Definition:** An object that applies a scaled status (e.g., ManaGain) to adjacent allies whenever the unit spends mana.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `ScaledStatusOnHolyShieldBlock`


**Definition:** An object that applies a scaled status (e.g., RandomMagicMissile) when the unit blocks an attack with a holy shield.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`RandomMagicMissile`](./Enums.md) | Integer | The number of random magic missiles fired, or an object defining its properties. | 1 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `ScaledStatusOnSpendMana`


**Definition:** An object containing status effect definitions to apply when the unit spends mana, with the number of stacks scaled by the amount of mana spent.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>	ag |
| [`StatusAfterXStacks`](./Miscellaneous.md#object-statusafterxstacks) | Object | Defines a condition that triggers a status effect when a specified stack key reaches a threshold, optionally expiring at turn end. | 1 | `{ . . . }` |

</details>


---


### Object: `SpawnOnDeath`


**Definition:** Specifies an object and its faction to spawn when the unit dies.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`faction`](./Enums.md#enum-faction) | Enum | Specifies the faction of a spawned unit or projectile, determining its team allegiance and AI behavior. | 4 | `allies`<br>`auto`<br>`birds` |
| [`obj`](./Arrays.md#array-obj) | Array / Enum  | Specifies one or more object names to bounce towards the target. | 4 | `BeefyCharmedLeech`<br>`Dice`<br>`Maggot` |

</details>


---


### Object: `SpawnRandomPickupsOnTaggedUnitKilled`


**Definition:** Defines a pool of random pickups (items) spawned when a unit with a specific tag is killed, with a count range.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](./Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 1 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| [`count`](./Arrays.md#array-count) | Array / Integer | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 1 | `0`<br>`1`<br>`10` |

</details>


---


### Object: `StatDependentPassive`


**Definition:** An object containing formulas that dynamically modify passive effects based on the unit's stats (e.g., str, dex, int).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`AddDamageToBasicAttack`](./Enums.md) | Enum | Additional damage added to the basic attack, either as a flat value or formula. | 1 | `1`<br>`2`<br>`4` |

</details>


---


### Object: `StatusAdjacentOnTheirTurnEnd`


**Definition:** Defines a status effect applied to adjacent units when their turn ends, such as forcing them to move away.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ForceMoveAway` | `Number` | The distance to force the target away from the source. | 1 | `1` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `StatusAfterXTurns`


**Definition:** Applies a status effect or forces an ability usage after a set number of turns.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum  | The name of the ability the source is forced to use, optionally with a chance. | 2 | `CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |

</details>


---


### Object: `StatusAlliesEachTurn`


**Definition:** Defines a status effect applied to all allies each turn, with an optional exclusion of the owner and conditional checks.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `StatusAlliesOnDeath`


**Definition:** Applies the contained status effects to all allies when the unit dies.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 5 | passives<br>class<br>	ag |
| [`DivineShield`](./Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | `1`<br>`2`<br>`4` |

</details>


---


### Object: `StatusEachRoundEnd`


**Definition:** An object listing status effects applied to the unit at the end of each round.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveWhenDead`](./Items_and_Equipment.md#context-passivewhendead)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid` | [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | Default<br>FormChange<br>Druid |
| [`DoDamage`](./Miscellaneous.md#object-dodamage) | Object  | Contains damage parameters (amount, type, tile targets) to deal damage to the target. | 1 | `{ . . . }` |

</details>


---


### Object: `StatusEachTurnEndForEachTurn`


**Definition:** Statuses applied at the end of each turn, with the number of turns as nested values.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 4 | passives<br>class<br>	ag |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum  | The name of the ability the source is forced to use, optionally with a chance. | 1 | `CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |

</details>


---


### Object: `StatusIfUnusedMovePoints`


**Definition:** Specifies status effects applied if the unit ends its turn with unused movement points.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 7 | passives<br>class<br>	ag |
| [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 4 | `1`<br>`10`<br>`2` |
| [`Charge`](./Enums.md) | Equation | The number of charge stacks applied. | 2 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `StatusOnCollectPickup`


**Definition:** An object containing status effects to apply when the unit collects a pickup item.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`StatusAfterXStacks`](./Miscellaneous.md#object-statusafterxstacks) | Object | Defines a condition that triggers a status effect when a specified stack key reaches a threshold, optionally expiring at turn end. | 1 | `{ . . . }` |

</details>


---


### Object: `StatusOnDodge`


**Definition:** Defines a status effect applied to the unit each time it successfully dodges an attack.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`DodgeChance_Status`](./Enums.md) | Integer | The flat percentage increase to dodge chance applied as a status effect. | 1 | `1`<br>`10`<br>`100` |

</details>


---


### Object: `StatusOnEatFood`


**Definition:** An object listing status effects applied to the unit when it eats food.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 4 | passives<br>class<br>	ag |
| [`RepairTrinket`](./Enums.md) | Integer | The number of stacks of the Repair Trinket status effect to apply. | 1 | `1`<br>`99` |
| [`TempPassiveUntilSettled`](./Miscellaneous.md#object-temppassiveuntilsettled) | Object | An object containing a temporary passive that is applied until the character's position is settled. | 1 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusOnEnemyDeath`


**Definition:** Defines a status effect applied to the unit each time an enemy dies.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`Charge`](./Enums.md) | Equation | The number of charge stacks applied. | 1 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `StatusOnFallAsleep`


**Definition:** Defines one or more beneficial status effects applied to the unit when it falls asleep.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AllStatsUp`](./Enums.md) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | `-1`<br>`-2`<br>`1` |
| [`FillMana`](./Enums.md) | Integer | The amount of mana restored, or an [amount, probability] array. | 1 | `1`<br>`[1 .10]`<br>`[1 .25]` |
| [`HealRandomInjury`](./Enums.md) | Integer | The number of random injuries healed on the target. | 1 | `1` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` | [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `StatusOnFullMana`


**Definition:** Defines a status effect applied to the unit when its mana is full, with an optional once-per-battle conditional.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_OncePerBattle`](./Miscellaneous.md#object-conditional_onceperbattle) | Object  | An object containing effects that can only trigger once per battle, preventing double-activation. | 1 | `{ . . . }` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 1 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `StatusOnHealed`


**Definition:** An object that applies a status effect to the unit whenever it is healed.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>	ag |
| [`Shield`](./Enums.md) | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 1 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusOnPickupCoins`


**Definition:** Specifies the effects applied when the unit picks up coins.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`GainCoins`](./Arrays.md#array-gaincoins) | Array / Integer  | The amount of coins gained, or a [min, max] range. | 1 | `-5`<br>`1`<br>`2` |

</details>


---


### Object: `StatusOnUseBasicAttack`


**Definition:** Specifies the effects applied when the unit performs a basic attack.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>	ag |
| [`DamageUp`](./Enums.md) | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 1 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 1 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `StatusWhenAllySpendsMana`


**Definition:** Specifies the effects applied when an ally spends mana.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>	ag |
| [`Charge`](./Enums.md) | Equation | The number of charge stacks applied. | 1 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `TempPassiveUntilSettled`


**Definition:** An object containing a temporary passive that is applied until the character's position is settled.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnEatFood`](./Items_and_Equipment.md#context-statusoneatfood)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`LimitHeal`](./Enums.md) | Integer | If 1, prevents the unit from being healed. | 1 | `0`<br>`1` |

</details>


---


### Object: `TintItem`


**Definition:** Defines additive and multiplicative color tint adjustments applied to an item's appearance, with an optional ignore condition.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ignore_if_str_aux_equals`](./Enums.md#enum-ignore_if_str_aux_equals) | Enum | Specifies the string aux value at which to ignore the tinting operation. | 1 | `ModelingClay_Default` |
| [`add`](./Arrays.md#array-add) | Array / Equation | The amount or an array of values added to the event's advantage or item tint. | 1 | `5`<br>`[0.05 0.05 0.05]` |
| [`mul`](./Arrays.md#array-mul) | Array | An array of three floats (RGB) used to multiply the item's tint color. | 1 | `[0.45 0.3 0.25]` |

</details>


---


### Object: `TransformWeapon`


**Definition:** An object with `from` and `to` fields specifying the weapon transformation.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`from`](./Enums.md#enum-from) | Enum | Specifies the source equipment item to be transformed. | 2 | `JarOfChaos`<br>`Necro_SoulDagger_Charged`<br>`Necro_SoulDagger_Uncharged` |
| [`to`](./Enums.md#enum-to) | Enum | Specifies the target equipment item after transformation. | 2 | `JarOfNothing`<br>`Necro_SoulDagger_Charged`<br>`Necro_SoulDagger_Uncharged` |

</details>


---


### Object: `TunnelVision`


**Definition:** If present, grants the TunnelVision status, which modifies crit_chance as defined in its sub-properties.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `crit_chance` | `Equation` | The chance for the damage instance to critically hit, expressed as a percentage or equation; values above 1 default to 100%. | 1 | `-999999`<br>`.05*X`<br>`.25` |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 1 | `damage_instance`<br>`spell`<br>`self_damage` |

</details>


---