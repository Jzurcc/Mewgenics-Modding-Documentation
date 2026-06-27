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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1571 | passives<br>class<br>	ag |
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
| [`int`](./Enums.md#enum-int) | Enum / Integer  |  | 66 | `-1`<br>`-10`<br>`-2` |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. | 64 | `1`<br>`2`<br>`true` |
| [`lck`](./Enums.md#enum-lck) | Enum / Integer  |  | 53 | `-1`<br>`-2`<br>`-3` |
| [`str`](./Engine_DamagingKeys.md#valid-property-keys) | Variable |  | 45 | `-1`<br>`-2`<br>`-3` |
| `quest_item` | Boolean | If true, this item is a quest item and cannot be sold or destroyed. | 40 | `false`<br>`true` |
| `parasite` | Boolean | If true, the item is a parasite that attaches to a unit and cannot be removed normally. | 36 | `true` |
| `aux` | Integer | An auxiliary integer value used for item properties, such as hunger value. | 33 | `-1`<br>`1`<br>`10` |
| [`dex`](./Enums.md#enum-dex) | Enum / Integer  |  | 30 | `-1`<br>`-2`<br>`-3` |
| [`keyword_tooltips`](./Passives_and_Statuses.md#object-keyword_tooltips) | Object  | Associates keyword tooltips with the ability, often used for status effects. | 28 | `{ . . . }` |
| [`quest_reward_item`](./Enums.md#enum-quest_reward_item) | Enum || 22 | `AirHorn_Fixed`<br>`AngryFace_Fixed`<br>`BubbleBoy_Fixed` |
| `divine_shield` | Integer | The number of stacks of the Divine Shield status this mutation provides. | 20 | `0`<br>`1`<br>`2` |
| `indestructible` | Boolean | If true, the item cannot be destroyed or removed. | 20 | `true` |
| [`speed`](./Arrays.md#array-speed) | Array / Float  | The speed of the projectile or move, can be a value or a range. | 19 | `-30`<br>`-4`<br>`.5` |
| `legacy_quest` | Boolean | If true, this item is part of a legacy quest. | 17 | `true` |
| [`hint_destination`](./Enums.md#enum-hint_destination) | Enum | Specifies the map destination hinted by this item or event. | 16 | `boneyard`<br>`caves`<br>`core` |
| [`str_aux_initialize`](./Enums.md#enum-str_aux_initialize) | Enum || 15 | `random_class_ability`<br>`random_class_passive`<br>`random_copyable_class_ability` |
| `dont_destroy_on_0` | Boolean || 13 | `true` |
| [`global_tags`](./Arrays.md#array-global_tags) | Array || 12 | `[`<br>`[all_cats_are_jester]`<br>`[all_normal_events_are_weather]` |
| `max_durability` | Integer || 11 | `1`<br>`2`<br>`3` |
| [`on_store`](./Enums.md#enum-on_store) | Enum || 8 | `become_aux_coins`<br>`become_furniture`<br>`become_rare_furniture` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 7 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`hint_prerequisite_flag`](./Enums.md#enum-hint_prerequisite_flag) | Enum || 5 | `mapflag_BothObelisksUnlocked`<br>`mapflag_DimensionXUnlocked`<br>`mapflag_MeatWorldUnlocked` |
| `failable` | Boolean | If true, the event or action has a chance to fail. | 4 | `true` |
| [`global_passives`](./Miscellaneous.md#object-global_passives) | Object  || 4 | `{ . . . }` |
| `randomize_piece_frames` | Boolean || 4 | `true` |
| `str_aux_is_copy_passive` | Boolean || 4 | `true` |
| `fragile` | Boolean || 3 | `true` |
| [`icon_hint`](./Enums.md#enum-icon_hint) | Enum || 3 | `ability_syringe`<br>`passive_syringe` |
| `max_health` | Integer || 3 | `-1` |
| `reset_aux_on_store` | Integer || 3 | `1` |
| `sticky` | Boolean || 3 | `true` |
| `weightless` | Boolean || 3 | `true` |
| [`passive`](./Miscellaneous.md#object-passive) | Object  || 2 | `{ . . . }` |
| `prevent_level_up` | Boolean || 2 | `true` |
| [`quest_item_alias`](./Enums.md#enum-quest_item_alias) | Enum || 2 | `BlackShard`<br>`NuclearKnife` |
| [`str_aux_is_copy_ability`](./Miscellaneous.md#object-str_aux_is_copy_ability) | Object  || 2 | `{ . . . }` |
| `str_aux_is_copy_item_passive` | Boolean || 2 | `true` |
| [`Set`](./Enums.md#enum-set) | Enum | Specifies the item set name that this item belongs to. | 1 | `Monk` |
| `aux_is_catid` | Boolean || 1 | `true` |
| `cant_equip_to_colorless` | Boolean || 1 | `true` |
| `degrade_after_adventure` | Boolean || 1 | `false` |
| [`equip_sound`](./Enums.md#enum-equip_sound) | Enum || 1 | `SE_CatWeaponPoke_Chainsaw` |
| `force_sticky` | Boolean || 1 | `true` |
| [`reset_str_aux_on_store`](./Enums.md#enum-reset_str_aux_on_store) | Enum || 1 | `ModelingClay_Default` |
| [`str_aux`](./Enums.md#enum-str_aux) | Enum || 1 | `ModelingClay_Default` |
| `str_aux_is_copy_item_active` | Boolean || 1 | `true` |
| `str_aux_is_copy_item_icon` | Boolean || 1 | `true` |

</details>


---


### Object: `passives`


**Definition:** Object listing intrinsic passive modifiers.  
**Total Count:** 748

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveAfterXKills`](./Items_and_Equipment.md#context-passiveafterxkills), [`PassiveAtHealthThreshold`](./Items_and_Equipment.md#context-passiveathealththreshold), [`PassiveAtStatThreshold`](./Items_and_Equipment.md#context-passiveatstatthreshold), [`PassiveIfStrAuxEquals`](./Items_and_Equipment.md#context-passiveifstrauxequals), [`PassiveWhenAffectedByElement`](./Items_and_Equipment.md#context-passivewhenaffectedbyelement), [`PassiveWhenOnTile`](./Items_and_Equipment.md#context-passivewhenontile), [`ROOT`](./Items_and_Equipment.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2628 | passives<br>class<br>	ag |
| [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#object-addstatustobasicattack) | Object  | Contains status effects to add to the basic attack. | 133 | `{ . . . }` |
| [`Brace`](./Enums.md) | Array / Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 94 | `1`<br>`10`<br>`2` |
| [`Metal`](./Enums.md) | Integer || 90 | `1` |
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
| [`Brittle`](./Enums.md) | Integer || 24 | `1` |
| [`AbilityReaction`](./Enums.md#enum-abilityreaction) | Enum  | Specifies the ability used as a reaction when the unit is targeted by an ability. | 23 | `AnkyloSpin`<br>`GSOpen`<br>`Gassy_AssBlast` |
| [`Fragile`](./Enums.md) | Integer || 22 | `1` |
| [`StatusOnBreak`](./Passives_and_Statuses.md#object-statusonbreak) | Object  || 22 | `{ . . . }` |
| [`AddPassivesToMinions`](./Passives_and_Statuses.md#object-addpassivestominions) | Object  || 21 | `{ . . . }` |
| [`DamageUp`](./Enums.md) | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 21 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`SpawnOnDeath`](./Passives_and_Statuses.md#object-spawnondeath) | Object  | Specifies an object and its faction to spawn when the unit dies. | 21 | `{ . . . }` |
| [`ArmorDodgeChance`](./Enums.md) | Integer || 19 | `10%`<br>`15%`<br>`20%` |
| [`StatusEachTurnBegin`](./Passives_and_Statuses.md#object-statuseachturnbegin) | Object  | Specifies status effects applied to the unit at the start of each of its turns. | 18 | `{ . . . }` |
| [`CritChanceUp`](./Enums.md) | Integer | The amount of critical hit chance added as a flat percentage. | 16 | `1`<br>`10`<br>`100` |
| [`AddBonusRange`](./Enums.md) | Integer | The number of additional tiles of range added to the unit's abilities. | 15 | `1`<br>`10`<br>`2` |
| [`KineticSpikes`](./Enums.md) | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 15 | `1`<br>`2`<br>`3` |
| [`RevengeDamage`](./Passives_and_Statuses.md#object-revengedamage) | Object  | An object defining the damage and effects that trigger when the unit is attacked. | 15 | `{ . . . }` |
| [`SpawnEachTurn`](./Passives_and_Statuses.md#object-spawneachturn) | Object  | Specifies an object that spawns on a random adjacent tile each turn, with optional chance. | 15 | `{ . . . }` |
| [`StatusOnBattleStart`](./Passives_and_Statuses.md#object-statusonbattlestart) | Object  || 15 | `{ . . . }` |
| [`AddCorpseHealth`](./Enums.md) | Integer | The amount of bonus health the unit's corpse has before it can be resurrected. | 14 | `-999`<br>`-999999`<br>`100` |
| [`AllStatsUp`](./Enums.md) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 14 | `-1`<br>`-2`<br>`1` |
| [`DodgeChance`](./Enums.md) | Integer | The percentage chance the unit has to dodge incoming attacks. | 14 | `10%`<br>`15%`<br>`2%` |
| [`InnateElement`](./Enums.md#enum-innateelement) | Enum  | Specifies the innate elemental type of the unit (e.g., Fire, Ice, Electric). | 14 | `Earth`<br>`Electric`<br>`Fire` |
| [`AddManaRegen`](./Enums.md) | Integer | The flat amount of mana regenerated per turn. | 13 | `1`<br>`2`<br>`3` |
| [`DeathRattleRevive`](./Enums.md#enum-deathrattlerevive) | Enum  | Specifies an ability or effect that revives the unit upon death, with options for stunning behavior. | 13 | `DoNothing`<br>`HCHumanDie`<br>`ToxPuff` |
| [`Flammable`](./Enums.md) | Integer || 13 | `1`<br>`2` |
| [`AbilityHealthThreshold`](./Passives_and_Statuses.md#object-abilityhealththreshold) | Object  | Defines an ability and conditions for its activation when the unit's health reaches a threshold. | 12 | `{ . . . }` |
| [`ReflectProjectiles`](./Enums.md) | Integer | The percentage chance to reflect projectiles back at the attacker; optionally includes self-damage. | 12 | `1`<br>`10%`<br>`100%` |
| [`SpawnThingOnDeath`](./Enums.md#enum-spawnthingondeath) | Enum  | Specifies the name of an object to spawn upon death. | 12 | `Boulder`<br>`CharmedDemonKitten`<br>`CharmedFlySwarm` |
| [`AbilityOnBattleStart`](./Enums.md#enum-abilityonbattlestart) | Enum  || 11 | `Flush`<br>`Heathens`<br>`Heathens2` |
| [`AddStatusToAllDamage`](./Passives_and_Statuses.md#object-addstatustoalldamage) | Object  || 11 | `{ . . . }` |
| [`BleedThorns`](./Enums.md) | Integer | The amount of bleed thorns damage dealt to attackers on hit. | 11 | `1`<br>`2`<br>`3` |
| [`ExtraBasicAttacks`](./Enums.md) | Integer | The number of additional basic attacks the unit can perform per turn. | 11 | `1`<br>`2` |
| [`ReplaceBasicMove`](./Enums.md#enum-replacebasicmove) | Enum  | Specifies an alternative movement ability that replaces the unit's default move. | 11 | `BasicDashAttackMove`<br>`BasicJump`<br>`BellyFlop_BasicMove` |
| [`AddLevelUpRerolls`](./Enums.md) | Integer | The number of additional rerolls the unit gets when leveling up. | 10 | `1`<br>`2`<br>`3` |
| [`MoveTowardsDamageSource`](./Enums.md#enum-movetowardsdamagesource) | Enum  | Determines the movement behavior when moving towards the unit that dealt damage to it. | 10 | `MoveOne` |
| [`StatusOnKillEnemy`](./Passives_and_Statuses.md#object-statusonkillenemy) | Object  || 10 | `{ . . . }` |
| [`AddSelfStatusToBasicAttack`](./Passives_and_Statuses.md#object-addselfstatustobasicattack) | Object  || 9 | `{ . . . }` |
| [`AddTag`](./Enums.md#enum-addtag) | Enum  | Specifies a gameplay tag (e.g., 'rock', 'plant') to add to the unit, used for interaction checks. | 9 | `bug`<br>`cat`<br>`fetus` |
| [`Bruise`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 9 | `1`<br>`2`<br>`3` |
| [`DepressionAura`](./Enums.md) | Integer | The number of stacks of Depression status applied to nearby enemies each turn; can be an object with range and ally settings. | 9 | `1`<br>`2` |
| [`Flying`](./Enums.md) | Integer | If set to 1, grants the unit the Flying passive, allowing movement over obstacles and ignoring terrain penalties. | 9 | `1` |
| [`MissChance`](./Enums.md) | Integer | The flat percentage chance that the unit's attacks will miss. | 9 | `10`<br>`15`<br>`20` |
| [`MovementReaction`](./Passives_and_Statuses.md#object-movementreaction) | Object  | Specifies an ability to cast when a unit moves within range, with options for targeting and conditions. | 9 | `{ . . . }` |
| [`PoisonThorns`](./Enums.md) | Integer | The number of stacks of Poison applied to melee attackers when they hit this unit. | 9 | `1`<br>`2`<br>`3` |
| [`StatusAlliesOnBattleStart`](./Passives_and_Statuses.md#object-statusalliesonbattlestart) | Object  || 9 | `{ . . . }` |
| [`TrinketPassiveMultiplierBonus`](./Enums.md) | Integer || 9 | `1`<br>`2` |
| [`BoostHeals`](./Enums.md) | Integer || 8 | `-2`<br>`1`<br>`2` |
| [`ChanceToRevive`](./Passives_and_Statuses.md#object-chancetorevive) | Integer / Object  || 8 | `{ . . . }`<br>`100`<br>`25` |
| [`PermanentMadness`](./Enums.md) | Integer | The number of permanent madness stacks applied. | 8 | `1` |
| [`StatusOnDie`](./Passives_and_Statuses.md#object-statusondie) | Object  | Specifies status effects or actions triggered when the unit dies. | 8 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 8 | `Default`<br>`FormChange`<br>`Druid` | [`AddElementsToBasicAttack`](./Enums.md) | Enum | Specifies an elemental damage type that is added to the unit's basic attacks. | 174 | Default<br>FormChange<br>Druid |
| [`AddInitiative`](./Enums.md) | Integer | The amount of bonus or penalty to the unit's turn order initiative value. | 7 | `-10`<br>`-100`<br>`-20` |
| [`AlphaTurns`](./Enums.md) | Integer | The number of turns the unit acts first in battle; negative values may indicate last. | 7 | `-1`<br>`1` |
| [`Bleed`](./Enums.md) | Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 7 | `1`<br>`10`<br>`2` |
| [`BonusAbility`](./Enums.md#enum-bonusability) | Enum  | Specifies the name of a bonus ability granted. | 7 | `Bloodzerk`<br>`BonusToss`<br>`BonusToss2` |
| [`BrittleDuringElement`](./Enums.md#enum-brittleduringelement) | Enum  || 7 | `water` |
| [`DebuffImmunity`](./Enums.md) | Integer | If 1, the unit is immune to debuffs. | 7 | `1` |
| [`DurabilityTransform`](./Passives_and_Statuses.md#object-durabilitytransform) | Object  || 7 | `{ . . . }` |
| [`ManaCostReduction`](./Enums.md) | Integer | The amount or percentage by which ability mana costs are reduced for this unit. | 7 | `-2`<br>`1`<br>`2` |
| [`OverrideBasicAttack`](./Enums.md#enum-overridebasicattack) | Enum  || 7 | `BasicExplosiveShot`<br>`BasicMelee`<br>`BasicMetronome` |
| [`PassiveAtHealthThreshold`](./Passives_and_Statuses.md#object-passiveathealththreshold) | Object  || 7 | `{ . . . }` |
| [`PassiveAtStatThreshold`](./Passives_and_Statuses.md#object-passiveatstatthreshold) | Object  || 7 | `{ . . . }` |
| [`SetFragileImmune`](./Enums.md) | Variable || 7 | `""`<br>`Bionic`<br>`Cardboard` |
| [`SetSpellCosts`](./Enums.md) | Integer | Overrides the cost of all spells to this value. | 7 | `0`<br>`1`<br>`3` |
| [`StatusOnEndMove`](./Passives_and_Statuses.md#object-statusonendmove) | Object  | Specifies status effects or actions triggered when the unit finishes moving. | 7 | `{ . . . }` |
| [`AddDamageToElementDamage`](./Passives_and_Statuses.md#object-adddamagetoelementdamage) | Object  | Defines additional damage of a specific element added to the unit's attacks. | 6 | `{ . . . }` |
| [`AmplifyStatus`](./Enums.md#enum-amplifystatus) | Enum  || 6 | `Bleed`<br>`Burn`<br>`Poison` |
| [`DelayedAutoRevive`](./Passives_and_Statuses.md#object-delayedautorevive) | Object  | Configures an automatic revival after a delay, with specified rounds and health percentage. | 6 | `{ . . . }` |
| [`DodgeChance_Status`](./Enums.md) | Integer | The flat percentage increase to dodge chance applied as a status effect. | 6 | `1`<br>`10`<br>`100` |
| [`ExtraWeaponAttacks`](./Enums.md) | Integer || 6 | `1`<br>`2` |
| [`IgnoreTiles`](./Enums.md) | Integer | If set to 1, movement ignores tile-based penalties or restrictions. | 6 | `1` |
| [`ItemAuxTransform`](./Passives_and_Statuses.md#object-itemauxtransform) | Object  || 6 | `{ . . . }` |
| [`PassiveWhenOnTile`](./Passives_and_Statuses.md#object-passivewhenontile) | Object  || 6 | `{ . . . }` |
| [`Poison`](./Enums.md) | Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 6 | `1`<br>`10`<br>`2` |
| [`Quivered`](./Arrays.md#array-quivered) | Array / Integer  | The amount of quivered stacks applied, or an [stacks, probability] array. | 6 | `1`<br>`2`<br>`5` |
| [`ReplaceBasicAttack`](./Enums.md#enum-replacebasicattack) | Enum  | Specifies the ability ID that replaces the unit's basic attack. | 6 | `BasicButcherMeleeWideDoubleSpin`<br>`BasicButcherMeleeWideSpin`<br>`BasicDruidAbilityVersatile` |
| [`SetBrittleImmune`](./Enums.md) | Variable || 6 | `""`<br>`AdvancedAlloy`<br>`Alloy` |
| [`SpawnOnBattleStartRandomEmptyTile`](./Passives_and_Statuses.md#object-spawnonbattlestartrandomemptytile) | Object  | Specifies an object that spawns on a random empty tile at the start of battle. | 6 | `{ . . . }` |
| [`AddBonusMeleeRange`](./Enums.md) | Integer | The number of additional tiles of range added to the unit's melee attacks. | 5 | `1`<br>`10`<br>`2` |
| [`AddHiddenTag`](./Enums.md#enum-addhiddentag) | Enum  | A hidden tag applied to the unit for internal logic and triggers. | 5 | `bowling_ball`<br>`grown_hitler_clone`<br>`hitler_clone_fetus` |
| [`BackstabCritChance`](./Enums.md) | Float || 5 | `.25`<br>`1` |
| [`Burn`](./Enums.md) | Equation | The amount of Burn applied, either as a fixed number or a formula string. | 5 | `1`<br>`10`<br>`2` |
| [`ClassManaCostReduction`](./Passives_and_Statuses.md#object-classmanacostreduction) | Object  | Defines a reduction in mana cost for abilities of a specific class. | 5 | `{ . . . }` |
| [`CritsApplyStatus`](./Passives_and_Statuses.md#object-critsapplystatus) | Object  || 5 | `{ . . . }` |
| [`FaceShield`](./Enums.md) | Integer | If 1, the unit has a face shield that protects it from certain attacks or effects. | 5 | `0`<br>`1` |
| [`HeadArmorPassiveMultiplierBonus`](./Enums.md) | Integer || 5 | `1`<br>`2` |
| [`InjuryImmunity`](./Enums.md) | Integer | The number of turns the unit is immune to injuries. | 5 | `1` |
| [`KnockbackImmunity`](./Enums.md) | Integer | If set to 1, the unit cannot be knocked back. | 5 | `1` |
| [`SharkySmellsBlood`](./Enums.md) | Integer | If 1, the unit is attracted to damaged units and may prioritize them. | 5 | `1` |
| [`SpellDamageUp`](./Enums.md) | Integer | The number of stacks of SpellDamageUp applied, increasing spell damage. | 5 | `1`<br>`3` |
| [`StatusIfUnusedMovePoints`](./Passives_and_Statuses.md#object-statusifunusedmovepoints) | Object  | Specifies status effects applied if the unit ends its turn with unused movement points. | 5 | `{ . . . }` |
| [`StatusOnTurnEndIfDidntCastAbilityTypes`](./Passives_and_Statuses.md#object-statusonturnendifdidntcastabilitytypes) | Object  || 5 | `{ . . . }` |
| [`TransformItemOnElementInfluence`](./Passives_and_Statuses.md#object-transformitemonelementinfluence) | Object  || 5 | `{ . . . }` |
| [`TrinketActiveEffectsMultiplierBonus`](./Enums.md) | Integer || 5 | `1`<br>`2` |
| [`AddCritMultiplier`](./Enums.md) | Integer || 4 | `100%`<br>`125%`<br>`150%` |
| [`AddKnockbackDamage`](./Enums.md) | Integer | The amount of additional knockback damage applied. | 4 | `1`<br>`2`<br>`3` |
| [`AddStatusToElementDamage`](./Passives_and_Statuses.md#object-addstatustoelementdamage) | Object  || 4 | `{ . . . }` |
| [`AddStatusToWeapons`](./Passives_and_Statuses.md#object-addstatustoweapons) | Object  | Specifies status effects to add to the unit's weapon attacks, with their stack counts. | 4 | `{ . . . }` |
| [`AddTemporaryEffectsToBasicAttack`](./Passives_and_Statuses.md#object-addtemporaryeffectstobasicattack) | Object  | A container object that lists temporary status effects applied to the unit's basic attack. | 4 | `{ . . . }` |
| [`BoostWeaponDamage`](./Passives_and_Statuses.md#object-boostweapondamage) | Object  | The amount of bonus weapon damage applied, or an object with `damage` and `crit_chance` fields. | 4 | `{ . . . }` |
| [`BreakAtAux`](./Enums.md) | Integer || 4 | `0` |
| [`BuffImmunity`](./Passives_and_Statuses.md#object-buffimmunity) | Object  | If 1, the unit is immune to buffs. An optional object can list buffs to exclude from immunity. | 4 | `{ . . . }` |
| [`CatchProjectiles`](./Passives_and_Statuses.md#object-catchprojectiles) | Object  || 4 | `{ . . . }` |
| [`ChanceToBackflip`](./Passives_and_Statuses.md#object-chancetobackflip) | Object  | An object specifying the ability to use and the percentage chance to perform a backflip dodge when hit. | 4 | `{ . . . }` |
| [`ExtraStatusWhenDealingDamage`](./Passives_and_Statuses.md#object-extrastatuswhendealingdamage) | Object  || 4 | `{ . . . }` |
| [`FaceArmorPassiveMultiplierBonus`](./Enums.md) | Integer || 4 | `1`<br>`2` |
| [`FragileDuringElement`](./Enums.md#enum-fragileduringelement) | Enum  || 4 | `water` |
| [`FreezePiercing`](./Enums.md) | Integer || 4 | `1` |
| [`IncreaseExplosionDamage`](./Enums.md) | Integer || 4 | `1`<br>`2`<br>`3` |
| [`IncreaseExplosionSize`](./Enums.md) | Integer || 4 | `1`<br>`2`<br>`7` |
| [`LevelUpClassOverride`](./Enums.md#enum-levelupclassoverride) | Enum  || 4 | `Colorless`<br>`Jester` |
| [`MakeSpellsRequireCharge`](./Enums.md) | Integer || 4 | `1` |
| [`PassiveWhenAffectedByElement`](./Passives_and_Statuses.md#object-passivewhenaffectedbyelement) | Object  | An object containing `element` and `passives` that grants the listed passives while the unit is affected by the specified element. | 4 | `{ . . . }` |
| [`PassiveWhenDead`](./Passives_and_Statuses.md#object-passivewhendead) | Object  | Passive effects that remain active while the unit is dead. | 4 | `{ . . . }` |
| [`RandomSeededStatModifier`](./Arrays.md#array-randomseededstatmodifier) | Array  || 4 | `[2 -1]` |
| [`StatusAlliesOnDeath`](./Passives_and_Statuses.md#object-statusalliesondeath) | Object  || 4 | `{ . . . }` |
| [`StatusEveryXSpellCasts`](./Passives_and_Statuses.md#object-statuseveryxspellcasts) | Object  | An object with `stacks` (number of spell casts) and status effects to apply after that many spell casts. | 4 | `{ . . . }` |
| [`StatusOnAllyCatDeath`](./Passives_and_Statuses.md#object-statusonallycatdeath) | Object  | An object listing status effects applied to the unit when an allied cat dies. | 4 | `{ . . . }` |
| [`StatusOnCastSpell`](./Passives_and_Statuses.md#object-statusoncastspell) | Object  | An object listing status effects applied to the unit whenever it casts a spell. | 4 | `{ . . . }` |
| [`StatusOnGainCoins`](./Passives_and_Statuses.md#object-statusongaincoins) | Object  | Specifies status effects applied when this unit gains coins. | 4 | `{ . . . }` |
| [`StatusOnPopCorpse`](./Passives_and_Statuses.md#object-statusonpopcorpse) | Object  || 4 | `{ . . . }` |
| [`StatusOnTakeHealthOrShieldDamage`](./Passives_and_Statuses.md#object-statusontakehealthorshielddamage) | Object  || 4 | `{ . . . }` |
| [`StatusRandomEnemiesOnBattleStart`](./Passives_and_Statuses.md#object-statusrandomenemiesonbattlestart) | Object  || 4 | `{ . . . }` |
| [`AddEndOfCombatRegen`](./Enums.md) | Integer || 3 | `12`<br>`999999` |
| [`AddPassivesToCharmed`](./Passives_and_Statuses.md#object-addpassivestocharmed) | Object  || 3 | `{ . . . }` |
| [`AddStatusToSpells`](./Passives_and_Statuses.md#object-addstatustospells) | Object  | Specifies status effects added to all spell attacks used by this unit. | 3 | `{ . . . }` |
| [`AllStatsUpPerDisorder`](./Enums.md) | Integer || 3 | `1` |
| [`AmplifyKnockback`](./Enums.md) | Integer || 3 | `10`<br>`2` |
| [`ApplyStatusesToRandomEnemiesEachTurn`](./Passives_and_Statuses.md#object-applystatusestorandomenemieseachturn) | Object  || 3 | `{ . . . }` |
| [`AutoEquipConsumables`](./Enums.md) | Integer || 3 | `1` |
| [`BasicAttackCritChance`](./Enums.md) | Float || 3 | `.1`<br>`100%` |
| [`BoneArmorPassive`](./Enums.md) | Integer || 3 | `1` |
| [`BreakOnElement`](./Enums.md#enum-breakonelement) | Enum  || 3 | `water` |
| [`CantCatchDiseases`](./Enums.md) | Integer || 3 | `1` |
| [`CantSpreadDiseases`](./Enums.md) | Integer || 3 | `1` |
| [`ChanceToBlock`](./Enums.md) | Integer || 3 | `10%` |
| [`ChanceToBlockAndCounter`](./Passives_and_Statuses.md#object-chancetoblockandcounter) | Integer / Object  || 3 | `{ . . . }`<br>`15%`<br>`25%`<br>`33%` |
| [`Confusion`](./Enums.md) | Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 3 | `1`<br>`10`<br>`2` |
| [`DropAsFamiliarOnArmorBreak`](./Enums.md#enum-dropasfamiliaronarmorbreak) | Enum  || 3 | `FaceGrubFamiliar`<br>`HeadGrubFamiliar`<br>`NeckGrubFamiliar` |
| [`ElementalManaCostReduction`](./Passives_and_Statuses.md#object-elementalmanacostreduction) | Object  || 3 | `{ . . . }` |
| [`ExtraBasicMoves_Status`](./Enums.md) | Integer | The number of extra basic moves per turn granted. | 3 | `1` |
| [`ExtraMovePoints`](./Enums.md) | Integer | The number of additional movement points granted to this unit. | 3 | `1` |
| [`FlowersOnEndTurn`](./Enums.md) | Integer || 3 | `1`<br>`3`<br>`4` |
| [`IncreaseSpellRange`](./Enums.md) | Integer || 3 | `10`<br>`2`<br>`20` |
| [`KillsToMeat`](./Enums.md#enum-killstomeat) | Enum  || 3 | `Food` |
| [`LuckUp`](./Enums.md) | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 3 | `-1`<br>`-2`<br>`-4` |
| [`MoveAndUseAbilityEachTurnBeginIfPossible`](./Enums.md#enum-moveanduseabilityeachturnbeginifpossible) | Enum  || 3 | `Cannibalize`<br>`EatShit`<br>`face_EatNeverstone` |
| [`MoveQuivered`](./Enums.md) | Float | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 3 | `1`<br>`2`<br>`[1, 0.1]` |
| [`NeckArmorPassiveMultiplierBonus`](./Enums.md) | Integer || 3 | `1`<br>`2` |
| [`PassiveAfterXKills`](./Passives_and_Statuses.md#object-passiveafterxkills) | Object  || 3 | `{ . . . }` |
| [`RangedTrueShot`](./Enums.md) | Integer || 3 | `1` |
| [`ReplaceSpawnedObjects`](./Arrays.md#array-replacespawnedobjects) | Array  || 3 | `[Boulder AnimatedBoulder]`<br>`[Boulder AnimatedLavaBoulder]`<br>`[Crow Crow2]` |
| [`RockyArmorPassive`](./Enums.md) | Integer || 3 | `1` |
| [`SetDefaultFacePassive`](./Enums.md#enum-setdefaultfacepassive) | Enum  || 3 | `euphoric`<br>`insane` |
| [`SpawnExtraThingsOnBattleStart`](./Passives_and_Statuses.md#object-spawnextrathingsonbattlestart) | Object  | An object with `object` and `number` (or range) defining what and how many objects to spawn at battle start. | 3 | `{ . . . }` |
| [`SpawnObjectOnPopCorpse`](./Passives_and_Statuses.md#object-spawnobjectonpopcorpse) | Enum / Object  || 3 | `{ . . . }`<br>`Catnip`<br>`Coin`<br>`Food` |
| [`StackingFlowerTrail`](./Passives_and_Statuses.md#object-stackingflowertrail) | Object  || 3 | `{ . . . }` |
| [`StatusAfterCastSpell`](./Passives_and_Statuses.md#object-statusaftercastspell) | Object  || 3 | `{ . . . }` |
| [`StatusAllCharactersOnSpawn`](./Passives_and_Statuses.md#object-statusallcharactersonspawn) | Object  | Defines status effects applied to all characters when they spawn into the battlefield. | 3 | `{ . . . }` |
| [`StatusOnBreakItem`](./Passives_and_Statuses.md#object-statusonbreakitem) | Object  || 3 | `{ . . . }` |
| [`StatusOnEatFood`](./Passives_and_Statuses.md#object-statusoneatfood) | Object  | An object listing status effects applied to the unit when it eats food. | 3 | `{ . . . }` |
| [`TrueShot`](./Enums.md) | Integer || 3 | `1` |
| [`AddSelfStatusToWeapons`](./Passives_and_Statuses.md#object-addselfstatustoweapons) | Object  || 2 | `{ . . . }` |
| [`AddStatusToKnockbackDamage`](./Passives_and_Statuses.md#object-addstatustoknockbackdamage) | Object  || 2 | `{ . . . }` |
| [`AllyDamageReduction`](./Enums.md) | Integer || 2 | `0` |
| [`ArmorBreakOnHit`](./Passives_and_Statuses.md#object-armorbreakonhit) | Object  || 2 | `{ . . . }` |
| [`BouncyProjectiles`](./Passives_and_Statuses.md#object-bouncyprojectiles) | Object  || 2 | `{ . . . }` |
| [`BreakWhenNoShield`](./Enums.md) | Integer || 2 | `1` |
| [`CanLevelUpWhenDead`](./Enums.md) | Integer || 2 | `1` |
| [`CanRemoveCursedItems`](./Enums.md) | Integer | If nonzero, allows the unit to remove cursed items from equipment slots. | 2 | `1` |
| [`CapMovementAbilityRange`](./Enums.md) | Integer || 2 | `1` |
| [`ConsumableEffectsMultiplierBonus`](./Enums.md) | Integer || 2 | `1` |
| [`CopyPassiveSlot`](./Enums.md) | Integer || 2 | `0`<br>`1` |
| [`CreateGlobalModifiers`](./Passives_and_Statuses.md#object-createglobalmodifiers) | Object  | Defines global gameplay modifiers to activate. | 2 | `{ . . . }` |
| [`DisableAbilities`](./Enums.md#enum-disableabilities) | Enum  || 2 | `all_items`<br>`all_spells`<br>`basic_attack` |
| [`DoubleCastWeapons`](./Enums.md) | Integer || 2 | `1`<br>`2` |
| [`Eternal`](./Passives_and_Statuses.md#object-eternal) | Object  || 2 | `{ . . . }` |
| [`FindExtraItemFromPoolOnBattleEnd`](./Enums.md#enum-findextraitemfrompoolonbattleend) | Enum  | Specifies the item pool from which an extra item is granted at the end of combat. | 2 | `combat_reward_easy`<br>`pills` |
| [`FlyDamageIncrease`](./Passives_and_Statuses.md#object-flydamageincrease) | Object  || 2 | `{ . . . }` |
| [`GainExtraShield`](./Enums.md) | Integer || 2 | `2`<br>`4` |
| [`HPGainBlock`](./Enums.md) | Integer || 2 | `1` |
| [`LeaveBehindOnceEachMove`](./Enums.md#enum-leavebehindonceeachmove) | Enum  || 2 | `Poop`<br>`Scrap` |
| [`MoveSpeedMultiplier`](./Enums.md) | Float || 2 | `.5` |
| [`PassiveIfWeaponIsUsable`](./Passives_and_Statuses.md#object-passiveifweaponisusable) | Object  || 2 | `{ . . . }` |
| [`PassiveWhileInMonkMeleeStance`](./Passives_and_Statuses.md#object-passivewhileinmonkmeleestance) | Object  || 2 | `{ . . . }` |
| [`PoopWhenHit`](./Passives_and_Statuses.md#object-poopwhenhit) | Object  | Specifies the object (e.g., Poop) spawned when the unit is hit, or an object with `chance` and `object`. | 2 | `{ . . . }` |
| [`RefreshEquipmentAbilityOnElement`](./Passives_and_Statuses.md#object-refreshequipmentabilityonelement) | Object  || 2 | `{ . . . }` |
| [`RemoveLineOfSightRestrictions`](./Enums.md) | Integer || 2 | `1` |
| [`ScaledStatusOnSpendMana`](./Passives_and_Statuses.md#object-scaledstatusonspendmana) | Object  || 2 | `{ . . . }` |
| [`SpawnItemLinkedFamiliar`](./Passives_and_Statuses.md#object-spawnitemlinkedfamiliar) | Object  || 2 | `{ . . . }` |
| [`SpawnNearEnemies`](./Enums.md) | Integer || 2 | `1` |
| [`StatusAfterXTurns`](./Passives_and_Statuses.md#object-statusafterxturns) | Object  | Applies a status effect or forces an ability usage after a set number of turns. | 2 | `{ . . . }` |
| [`StatusEachTurnEndForEachTurn`](./Passives_and_Statuses.md#object-statuseachturnendforeachturn) | Object  | Statuses applied at the end of each turn, with the number of turns as nested values. | 2 | `{ . . . }` |
| [`StatusIfUnusedActPoints`](./Passives_and_Statuses.md#object-statusifunusedactpoints) | Object  || 2 | `{ . . . }` |
| [`StatusOnBackstab`](./Passives_and_Statuses.md#object-statusonbackstab) | Object  || 2 | `{ . . . }` |
| [`StatusOnCollectPickup`](./Passives_and_Statuses.md#object-statusoncollectpickup) | Object  || 2 | `{ . . . }` |
| [`StatusOnHealed`](./Passives_and_Statuses.md#object-statusonhealed) | Object  || 2 | `{ . . . }` |
| [`StatusOnPickupCoins`](./Passives_and_Statuses.md#object-statusonpickupcoins) | Object  || 2 | `{ . . . }` |
| [`StatusOnUseBasicAttack`](./Passives_and_Statuses.md#object-statusonusebasicattack) | Object  || 2 | `{ . . . }` |
| [`StatusWhenAllySpendsMana`](./Passives_and_Statuses.md#object-statuswhenallyspendsmana) | Object  || 2 | `{ . . . }` |
| [`TauntAlways`](./Enums.md) | Integer || 2 | `1` |
| [`Uncontrollable`](./Enums.md) | Integer || 2 | `1` |
| [`WeaponDamageMultiplierBonus`](./Enums.md) | Integer || 2 | `1`<br>`2` |
| [`AIControlNextTurn`](./Passives_and_Statuses.md#object-aicontrolnextturn) | Object  || 1 | `{ . . . }` |
| [`AOEBonus`](./Enums.md) | Integer || 1 | `1` |
| [`AbilityOnRoundEndOnce`](./Passives_and_Statuses.md#object-abilityonroundendonce) | Object  || 1 | `{ . . . }` |
| [`AddAdvantageToEvent`](./Passives_and_Statuses.md#object-addadvantagetoevent) | Object  || 1 | `{ . . . }` |
| [`AddStatusToBackstabs`](./Passives_and_Statuses.md#object-addstatustobackstabs) | Object  || 1 | `{ . . . }` |
| [`AllSpellsCostCharge`](./Enums.md) | Integer || 1 | `1` |
| [`AllUnitsExplodeOnDeath`](./Enums.md) | Integer || 1 | `5` |
| [`AlliesScrambleSpellAfterCast`](./Enums.md) | Integer || 1 | `1` |
| [`AlluringDoodieEater`](./Passives_and_Statuses.md#object-alluringdoodieeater) | Object  || 1 | `{ . . . }` |
| [`AllyDodgeChanceAura`](./Passives_and_Statuses.md#object-allydodgechanceaura) | Object  || 1 | `{ . . . }` |
| [`AlphaAllStatsUp`](./Enums.md) | Integer || 1 | `1` |
| [`AlphaCat`](./Enums.md) | Integer | The number of AlphaCat stacks applied to the source on kill. | 1 | `1` |
| [`AlwaysChosenForLevelUp`](./Enums.md) | Integer || 1 | `1` |
| [`BackflipWhenTargeted`](./Passives_and_Statuses.md#object-backflipwhentargeted) | Enum / Object  | The number of backflip charges, or an object defining its ability. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`X` |
| [`BalanceStats`](./Enums.md) | Integer || 1 | `1` |
| [`BasicAttackCantMiss`](./Enums.md) | Integer | If nonzero, the unit's basic attack cannot miss. | 1 | `1` |
| [`Blind`](./Enums.md) | Integer | The amount of blind stacks applied, or an [stacks, probability] array. | 1 | `-1`<br>`1`<br>`2` |
| [`BlockDamageUnderThreshold`](./Enums.md) | Integer || 1 | `1` |
| [`BlockNegativeStatus`](./Enums.md) | Integer || 1 | `30%` |
| [`BoostReceivedHealing`](./Enums.md) | Integer || 1 | `2` |
| [`CapBasicAttackDamage`](./Enums.md) | Integer || 1 | `1` |
| [`CatPartsSizeScale`](./Passives_and_Statuses.md#object-catpartssizescale) | Object  || 1 | `{ . . . }` |
| [`ChanceToAmbush`](./Enums.md) | Integer || 1 | `25%` |
| [`ChanceToForceEvent`](./Passives_and_Statuses.md#object-chancetoforceevent) | Object  || 1 | `{ . . . }` |
| [`Charge`](./Enums.md) | Equation | The number of charge stacks applied. | 1 | `1`<br>`2`<br>`3` |
| [`CharismaIsMaxStat`](./Enums.md) | Integer || 1 | `1` |
| [`CharmImmunity`](./Enums.md) | Integer || 1 | `1` |
| [`ConvertDamageToScaledStatus`](./Passives_and_Statuses.md#object-convertdamagetoscaledstatus) | Object  || 1 | `{ . . . }` |
| [`CounterNextAttacks`](./Enums.md) | Integer || 1 | `2` |
| [`DisablePassiveSlot`](./Enums.md) | Integer || 1 | `0`<br>`1` |
| [`DoubleCastSpellIfManaCostUnderThreshold`](./Enums.md) | Integer || 1 | `3` |
| [`DoubleCastTaggedSpells`](./Enums.md#enum-doublecasttaggedspells) | Enum  || 1 | `musical` |
| [`DoubleReceivedNegativeStatus`](./Enums.md) | Integer || 1 | `1` |
| [`DoubleReceivedPositiveStatus`](./Enums.md) | Integer || 1 | `1` |
| [`DropAsFamiliarOnTookDamage`](./Enums.md#enum-dropasfamiliarontookdamage) | Enum  || 1 | `PhantomMaskRock` |
| [`DropSoulJarOnDeath`](./Enums.md#enum-dropsouljarondeath) | Enum  || 1 | `SoulJar_Full` |
| [`ExcludeFromEvents`](./Enums.md#enum-excludefromevents) | Enum  || 1 | `Tragedy` |
| [`ExplosionImmunity`](./Enums.md) | Integer || 1 | `1` |
| [`ExtraBasicAttacks_Status`](./Enums.md) | Integer | The number of additional basic attacks the unit can perform each turn. | 1 | `1` |
| [`ExtraTrinketUses`](./Enums.md) | Integer || 1 | `1`<br>`10` |
| [`FrankBolts`](./Enums.md) | Integer || 1 | `1` |
| [`GlobalMeleeRevengeDamage`](./Passives_and_Statuses.md#object-globalmeleerevengedamage) | Object  || 1 | `{ . . . }` |
| [`HideSomeHudStuff`](./Enums.md) | Integer || 1 | `1` |
| [`JesterLevelUpRerolls`](./Enums.md) | Integer || 1 | `1` |
| [`Lifesteal`](./Enums.md) | Integer | The amount of lifesteal stacks applied. | 1 | `1`<br>`3` |
| [`MakeBasicAttackPull`](./Enums.md) | Integer | If nonzero, the unit's basic attack pulls the target closer. | 1 | `1` |
| [`ModelingClayPassive`](./Enums.md) | Integer || 1 | `1` |
| [`MultiplyCoinsOnBattleStart`](./Enums.md) | Integer || 1 | `2` |
| [`MultiplyReceivedHealing`](./Enums.md) | Integer || 1 | `2` |
| [`ObjectDetector`](./Passives_and_Statuses.md#object-objectdetector) | Object  || 1 | `{ . . . }` |
| [`PassiveIfStrAuxEquals`](./Passives_and_Statuses.md#object-passiveifstrauxequals) | Object  || 1 | `{ . . . }` |
| [`PassiveWhileHasDurability`](./Passives_and_Statuses.md#object-passivewhilehasdurability) | Object  || 1 | `{ . . . }` |
| [`PassiveWhileShielded`](./Passives_and_Statuses.md#object-passivewhileshielded) | Object  || 1 | `{ . . . }` |
| [`PhysicalAttacksMiss`](./Enums.md) | Integer || 1 | `1` |
| [`PreventSpecificInjury`](./Enums.md) | Enum || 1 | `int` |
| [`ReclaimItemOnBreak`](./Enums.md) | Integer || 1 | `1` |
| [`ReduceManaCost`](./Enums.md) | Integer | The number of stacks reducing mana cost of abilities. | 1 | `1`<br>`2` |
| [`ReduceSpellCostsPerDisorder`](./Enums.md) | Integer || 1 | `1` |
| [`ReduceSpellCostsPerParasite`](./Enums.md) | Integer || 1 | `1` |
| [`ReplaceBlankTilesOnBattleStart`](./Enums.md#enum-replaceblanktilesonbattlestart) | Enum  || 1 | `GlassTile` |
| [`RerollItemsOnBattleEnd`](./Enums.md) | Integer || 1 | `1` |
| [`ScaldingOrbMoonBossOneShot`](./Passives_and_Statuses.md#object-scaldingorbmoonbossoneshot) | Object  || 1 | `{ . . . }` |
| [`ScaledStatusAlliesOnSpendMana`](./Passives_and_Statuses.md#object-scaledstatusalliesonspendmana) | Object  || 1 | `{ . . . }` |
| [`ScaledStatusOnHolyShieldBlock`](./Passives_and_Statuses.md#object-scaledstatusonholyshieldblock) | Object  || 1 | `{ . . . }` |
| [`SetFaction`](./Enums.md#enum-setfaction) | Enum  || 1 | `enemies` |
| [`SpawnCatCloneOnCorpsePopped`](./Enums.md) | Integer || 1 | `1` |
| [`SpawnOnDowned`](./Enums.md#enum-spawnondowned) | Enum  | Specifies the character or object spawned when the unit is downed. | 1 | `CharmedFly`<br>`CharmedKitten`<br>`CharmedSpookie` |
| [`SpawnRandomPickupsOnTaggedUnitKilled`](./Passives_and_Statuses.md#object-spawnrandompickupsontaggedunitkilled) | Object  || 1 | `{ . . . }` |
| [`StatDependentPassive`](./Passives_and_Statuses.md#object-statdependentpassive) | Object  || 1 | `{ . . . }` |
| [`StatusAdjacentOnTheirTurnEnd`](./Passives_and_Statuses.md#object-statusadjacentontheirturnend) | Object  || 1 | `{ . . . }` |
| [`StatusAlliesEachTurn`](./Passives_and_Statuses.md#object-statusallieseachturn) | Object  || 1 | `{ . . . }` |
| [`StatusOnDodge`](./Passives_and_Statuses.md#object-statusondodge) | Object  || 1 | `{ . . . }` |
| [`StatusOnEnemyDeath`](./Passives_and_Statuses.md#object-statusonenemydeath) | Object  || 1 | `{ . . . }` |
| [`StatusOnFallAsleep`](./Passives_and_Statuses.md#object-statusonfallasleep) | Object  || 1 | `{ . . . }` |
| [`StatusOnFullMana`](./Passives_and_Statuses.md#object-statusonfullmana) | Object  || 1 | `{ . . . }` |
| [`StevenBolts`](./Enums.md) | Integer || 1 | `1` |
| [`StripKnockback`](./Enums.md) | Integer || 1 | `1` |
| [`TintItem`](./Passives_and_Statuses.md#object-tintitem) | Object  || 1 | `{ . . . }` |
| [`TunnelVision`](./Passives_and_Statuses.md#object-tunnelvision) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `AddStatusToBasicAttack`


**Definition:** Injects a status effect payload that applies whenever the character performs a basic attack.  
**Total Count:** 65

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Items_and_Equipment.md#context-addpassivestominions), [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 121 | passives<br>class<br>	ag |
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
| [`ForceUseAbilityOnTarget`](./Miscellaneous.md#object-forceuseabilityontarget) | Object  || 1 | `{ . . . }` |
| [`KnockUpAndAway`](./Miscellaneous.md#object-knockupandaway) | Object  | Contains parameters for launching the target upward and away from the source, including stacks and distance. | 1 | `{ . . . }` |
| [`Marked`](./Enums.md) | Integer | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`3`<br>`5` |
| [`PullSourceToTarget`](./Enums.md) | Integer | The amount of tiles the source is pulled towards the target after the attack. | 1 | `1` |

</details>


---


### Object: `Conditional_GoodRoll`


**Definition:** Conditional trigger: Executes nested logic based on a randomized favorable outcome probability.  
**Total Count:** 37

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Items_and_Equipment.md#context-addstatustobasicattack), [`StatusEachTurnEnd`](./Items_and_Equipment.md#context-statuseachturnend), [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend), [`StatusOnKill`](./Items_and_Equipment.md#context-statusonkill), [`StatusOnTakeHealthOrShieldDamage`](./Items_and_Equipment.md#context-statusontakehealthorshielddamage), [`effects`](./Items_and_Equipment.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `odds` | Float | The probability of the effect occurring, expressed as a decimal or percentage. | 37 | `.1`<br>`.16666666`<br>`.3` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 37 | Default<br>FormChange<br>Druid |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 15 | passives<br>class<br>	ag |
| [`Freeze`](./Arrays.md#array-freeze) | Array / Integer  | The amount of freeze stacks applied, or an [stacks, probability] array. | 6 | `1`<br>`2`<br>`[1 .01]` |
| [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Enum  | Specifies the loot pool from which to find an item, with an optional chance. | 5 | `blackbird_pool`<br>`chapter`<br>`chapter_common` |
| [`ForceUseAbility_NonStack`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Forces the unit to use a specific non-stackable ability when the conditional roll is successful. | 4 | `Endeavor_Auto`<br>`Indigestion_Fart`<br>`Indigestion_Fart2` |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum  | The name of the ability the source is forced to use, optionally with a chance. | 3 | `CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| [`RandomMutation`](./Enums.md) | Integer | The number of random mutations to apply. | 3 | `1`<br>`3` |
| `DestroyTrinket` | `Number` | The number of trinkets destroyed. | 1 | `1` |

</details>


---


### Object: `effects`


**Definition:** Non-damaging status applications and logic triggers executed on impact.  
**Total Count:** 35

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DoDamage`](./Items_and_Equipment.md#context-dodamage), [`MeleeRevengeDamage`](./Items_and_Equipment.md#context-meleerevengedamage), [`RevengeDamage`](./Items_and_Equipment.md#context-revengedamage), [`damage_instance`](./Items_and_Equipment.md#context-damage_instance)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1085 | passives<br>class<br>	ag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 624 | Default<br>FormChange<br>Druid |
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


**Definition:** Reaction trigger: Applies nested status effects to the attacker when hit by a melee attack.  
**Total Count:** 32

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Variable | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 36 | `damage_instance`<br>`spell`<br>`self_damage` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 47 | `{ . . . }` |
| [`knockback`](./Enums.md#enum-knockback) | Enum / Integer  | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 24 | `"ceil(X*.25/5)"`<br>`-10`<br>`-2` |
| [`damage`](./Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 22 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |

</details>


---


### Object: `StatusOnBattleEnd`


**Definition:** Applies the nested status effects when the encounter finishes.  
**Total Count:** 25

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyPassives`](./Items_and_Equipment.md#context-applypassives), [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 56 | passives<br>class<br>	ag |
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
| [`Conditional_Corpse`](./Passives_and_Statuses.md#object-conditional_corpse) | Object  || 1 | `{ . . . }` |
| [`Conditional_Shielded`](./Passives_and_Statuses.md#object-conditional_shielded) | Object  || 1 | `{ . . . }` |
| [`RepairAll`](./Enums.md) | Integer | The amount of durability restored to all equipped items. | 1 | `1`<br>`10` |
| [`RepairWeapon`](./Arrays.md#array-repairweapon) | Array / Integer  | The number of weapon durability points restored; an array [stacks, probability] applies a chance-based repair. | 1 | `1`<br>`6`<br>`99` |
| [`TransformWeapon`](./Miscellaneous.md#object-transformweapon) | Object  | An object with `from` and `to` fields specifying the weapon transformation. | 1 | `{ . . . }` |

</details>


---


### Object: `StatusEachTurnEnd`


**Definition:** Applies or references the 'StatusEachTurnEnd' effect/state.  
**Total Count:** 22

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 42 | passives<br>class<br>	ag |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum  | The name of the ability the source is forced to use, optionally with a chance. | 12 | `CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| [`Shield`](./Enums.md) | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 5 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 5 | `Default`<br>`FormChange`<br>`Druid` | [`PartialCleanse`](./Enums.md) | Integer | The number of stacks of temporary status effects to remove from the target. | 7 | Default<br>FormChange<br>Druid |
| [`Conditional_GoodRoll`](./Passives_and_Statuses.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 2 | `{ . . . }` |
| [`ImmediateUseAbility`](./Miscellaneous.md#object-immediateuseability) | Enum / Object  | Specifies the name of an ability to be triggered instantly from this effect. | 2 | `{ . . . }`<br>`FuzzerReact`<br>`HitlerCloneHeil`<br>`HitlerCloneTransform` |
| [`SpawnCoinAnywhere`](./Enums.md) | Integer | The number of coins to spawn. If an array, the second value is the probability of spawning them anywhere. | 2 | `1`<br>`[1 .5]` |
| [`AddWeaponAux`](./Enums.md) | Equation | The amount or expression to add to the source's weapon auxiliary stat. | 1 | `"-max(min(X+1, item_aux), 0)"`<br>`-item_aux`<br>`1` |
| [`Burn`](./Enums.md) | Equation | The amount of Burn applied, either as a fixed number or a formula string. | 1 | `1`<br>`10`<br>`2` |
| [`Conditional_ManaThreshold`](./Miscellaneous.md#object-conditional_manathreshold) | Object  || 1 | `{ . . . }` |
| [`ConstitutionUp`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 1 | `-1`<br>`-2`<br>`1` |
| [`PreEmptiveCounterNextAttacks`](./Enums.md) | Integer | The number of next incoming attacks that the unit will counter preemptively before they land. | 1 | `1` |
| [`Stealth`](./Arrays.md#array-stealth) | Array  | The number of stealth stacks applied. | 1 | `1`<br>`2`<br>`[1 .1]` |

</details>


---


### Object: `StatusOnBreak`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 22

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 11 | passives<br>class<br>	ag |
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
| [`GainDisorder`](./Enums.md#enum-gaindisorder) | Enum  || 1 | `Chungus`<br>`Psychosis` |
| [`IntelligenceUp`](./Enums.md) | Array / Equation | The amount of Intelligence added as a flat bonus. | 1 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| [`ObjectOnHitCharacter`](./Passives_and_Statuses.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 1 | `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| [`StrengthUp`](./Enums.md) | Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 1 | `"max(int, 0)"`<br>`-1`<br>`-2` |

</details>


---


### Object: `SpawnOnBattleStart`


**Definition:** No definition provided.  
**Total Count:** 21

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 38 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`number`](./Arrays.md#array-number) | Array / Integer || 29 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `StatusOnKill`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 16

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 20 | passives<br>class<br>	ag |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 6 | `Default`<br>`FormChange`<br>`Druid` | [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 8 | Default<br>FormChange<br>Druid |
| [`Conditional_GoodRoll`](./Passives_and_Statuses.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 4 | `{ . . . }` |
| [`EquipPermanentItem`](./Enums.md#enum-equippermanentitem) | Enum  | The name of the item to permanently equip to the source. | 3 | `BoneClub`<br>`Kidney` |
| [`StrengthUp`](./Enums.md) | Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 3 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| [`LuckUp`](./Enums.md) | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 2 | `-1`<br>`-2`<br>`-4` |
| [`SpeedUp`](./Enums.md) | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 2 | `-1`<br>`-2`<br>`-4` |
| [`BrittleCharismaUp`](./Enums.md) | Integer || 1 | `2` |
| [`BrittleConstitutionUp`](./Enums.md) | Integer || 1 | `2` |
| [`BrittleDexterityUp`](./Enums.md) | Integer || 1 | `2` |
| [`BrittleIntelligenceUp`](./Enums.md) | Integer || 1 | `2` |
| [`BrittleLuckUp`](./Enums.md) | Integer || 1 | `2` |
| [`BrittleSpeedUp`](./Enums.md) | Integer || 1 | `2` |
| [`BrittleStrengthUp`](./Enums.md) | Integer || 1 | `2` |
| [`CharismaUp`](./Enums.md) | Integer | The amount of charisma change, or a keyword like 'item_aux'. | 1 | `-1`<br>`-2`<br>`1` |
| [`ConstitutionUp`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 1 | `-1`<br>`-2`<br>`1` |
| [`DexterityUp`](./Enums.md) | Array / Equation | The amount of dexterity change, or a keyword like 'item_aux'. | 1 | `-1`<br>`1`<br>`2` |
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 1 | `1`<br>`2`<br>`3` |
| [`IntelligenceUp`](./Enums.md) | Array / Equation | The amount of Intelligence added as a flat bonus. | 1 | `"min(-int, 0)"`<br>`-1`<br>`-2` |

</details>


---


### Object: `StatusOnTookDamage`


**Definition:** Event Trigger: Applies nested statuses when took damage.  
**Total Count:** 16

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 30 | passives<br>class<br>	ag |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 14 | `Default`<br>`FormChange`<br>`Druid` | [`Charge`](./Enums.md) | Integer | The number of charge stacks applied. | 13 | Default<br>FormChange<br>Druid |
| [`StrengthUp`](./Enums.md) | Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 4 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| [`DamageUp`](./Enums.md) | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 3 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`Temporary`](./Passives_and_Statuses.md#object-temporary) | Object  | Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions. | 3 | `{ . . . }` |
| [`Thorns`](./Enums.md) | Integer | The amount of thorns damage dealt to attackers on hit. | 3 | `1`<br>`2`<br>`3` |
| [`Conditional_HasStatus`](./Passives_and_Statuses.md#object-conditional_hasstatus) | Object  || 2 | `{ . . . }` |
| [`Bleed`](./Enums.md) | Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`10`<br>`2` |
| [`Conditional_HealthThreshold`](./Miscellaneous.md#object-conditional_healththreshold) | Object  | Contains an inner effect block that only executes if the target's health is below a threshold, defined by `threshold_flat`, `threshold_percent`, or `threshold_expr`. | 1 | `{ . . . }` |
| [`DivineShield`](./Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | `1`<br>`2`<br>`4` |
| [`DodgeChance_Status`](./Enums.md) | Integer | The flat percentage increase to dodge chance applied as a status effect. | 1 | `1`<br>`10`<br>`100` |
| [`RemoveStatus`](./Enums.md#enum-removestatus) | Enum  | The name of the status effect to remove from the source. | 1 | `AlphaCat`<br>`Brace`<br>`DodgeChance_Status` |

</details>


---


### Object: `StatusOnBattleStart`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 13

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 7 | passives<br>class<br>	ag |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 7 | `Default`<br>`FormChange`<br>`Druid` | [`Craft`](Abilities_and_Spells.md#object-craft) | Object | Specifies the loot pool and slot to craft an item for the source. | 3 | Default<br>FormChange<br>Druid |
| [`SafeDie`](./Enums.md) | Integer | The number of times the unit can survive a fatal hit. | 2 | `1` |
| [`Brace`](./Enums.md) | Array / Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 1 | `1`<br>`10`<br>`2` |
| [`DestroyEquipmentAndAttachParasite`](./Miscellaneous.md#object-destroyequipmentandattachparasite) | Object  | Attempts to destroy a random piece of the target's equipment and attach a parasite from the specified pool. | 1 | `{ . . . }` |
| [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Enum  | Specifies the loot pool from which to find an item, with an optional chance. | 1 | `blackbird_pool`<br>`chapter`<br>`chapter_common` |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum  | The name of the ability the source is forced to use, optionally with a chance. | 1 | `CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| [`ObjectOnHitCharacter`](./Passives_and_Statuses.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 1 | `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| [`RandomMagicMissile`](./Enums.md) | Integer | The number of random magic missiles fired, or an object defining its properties. | 1 | `1`<br>`10`<br>`2` |
| [`ReviveNextRound`](./Miscellaneous.md#object-revivenextround) | Object  | The number of revives granted, or an object defining revive properties. | 1 | `{ . . . }` |
| [`SetHealth`](./Enums.md) | Integer || 1 | `1`<br>`100%`<br>`50%` |
| [`StealthUntilBasicAttack`](./Enums.md) | Integer | The number of stacks of Stealth that are removed when the unit performs a basic attack. | 1 | `1` |

</details>


---


### Object: `SpawnThingOnDamage`


**Definition:** Applies or references the 'SpawnThingOnDamage' effect/state.  
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
| [`number`](./Arrays.md#array-number) | Array / Integer  || 1 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `SpawnEachTurn`


**Definition:** Applies or references the 'SpawnEachTurn' effect/state.  
**Total Count:** 10

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array / Enum | Specifies the object or unit to be spawned. | 22 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`chance`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A probability (decimal or percentage) for a form change or other effect to occur. | 20 | `.02`<br>`.1`<br>`.15` |
| [`stack_key`](./Enums.md#enum-stack_key) | Enum || 5 | `CATHIDE`<br>`EMPTY_GENERATOR`<br>`FANNY_PACK` |

</details>


---


### Object: `StatusEachTurnBegin`


**Definition:** Event Trigger: Applies nested statuses to each turn begin.  
**Total Count:** 10

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveWhenDead`](./Items_and_Equipment.md#context-passivewhendead), [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 9 | passives<br>class<br>	ag |
| [`Conditional_BadRoll`](./Passives_and_Statuses.md#object-conditional_badroll) | Object  | An object containing an `odds` value and effects that are applied when a random roll succeeds. | 5 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 | `Default`<br>`FormChange`<br>`Druid` | [`SpeedUp`](./Enums.md) | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 10 | Default<br>FormChange<br>Druid |
| [`BlessingOfPeace`](./Enums.md) | Integer | The number of stacks of the Blessing of Peace status applied to the unit each turn. | 1 | `1` |
| [`Burn`](./Enums.md) | Equation | The amount of Burn applied, either as a fixed number or a formula string. | 1 | `1`<br>`10`<br>`2` |
| [`DestroyTrinket`](./Enums.md) | Integer || 1 | `1` |
| [`DoubleCastSpellThisTurn`](./Enums.md) | Integer | If non-zero, grants the unit a double cast effect for spells this turn. | 1 | `1` |
| [`DrinkWater`](./Enums.md) | Integer | The number of water-drink actions performed. | 1 | `1` |
| [`ManaGainRange`](./Miscellaneous.md#object-managainrange) | Object  || 1 | `{ . . . }` |
| [`Revive`](./Enums.md) | Integer | Revives a dead target with the specified percentage of health (e.g., "50%", "100%") or a fixed number. | 1 | `1`<br>`100%`<br>`50%` |
| [`Temporary`](./Passives_and_Statuses.md#object-temporary) | Object  | Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions. | 1 | `{ . . . }` |
| [`UseAbility`](./Enums.md#enum-useability) | Enum  | The name of the ability the target is forced to use. | 1 | `GirlDinoPoop`<br>`KirbySpit`<br>`MD_PoopChain` |
| [`Wet`](./Enums.md) | Integer | The number of stacks of the Wet status effect applied. | 1 | `1` |

</details>


---


### Object: `RevengeDamage`


**Definition:** Reaction trigger: Deals damage to the attacker when hit.  
**Total Count:** 9

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Variable | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 10 | `damage_instance`<br>`spell`<br>`self_damage` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 29 | `{ . . . }` |
| [`damage`](./Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 8 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`elements`](./Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 2 | `[`<br>`[Heat Fire]` |

</details>


---


### Object: `AddSelfStatusToBasicAttack`


**Definition:** Applies or references the 'AddSelfStatusToBasicAttack' effect/state.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 9 | passives<br>class<br>	ag |
| [`RandomMagicMissile`](./Enums.md) | Integer | The number of random magic missiles fired, or an object defining its properties. | 7 | `1`<br>`10`<br>`2` |
| [`Bleed`](./Enums.md) | Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`10`<br>`2` |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum  | The name of the ability the source is forced to use, optionally with a chance. | 1 | `CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| [`Quivered`](./Arrays.md#array-quivered) | Array / Integer  | The amount of quivered stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`2`<br>`5` |
| [`Shield`](./Enums.md) | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 1 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `DurabilityTransform`


**Definition:** Applies or references the 'DurabilityTransform' effect/state.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`eq`](./Arrays.md#array-eq) | Array || 7 | `[0 EstusFlask_Empty]`<br>`[0 JarOfNothing]`<br>`[0 WaterBottle_Empty]` |
| [`ge`](./Arrays.md#array-ge) | Array || 4 | `[10 NuclearKnife_Glowing]`<br>`[2 WaterBottle_Full]`<br>`[20 BlackShard_Glowing]` |

</details>


---


### Object: `PassiveIfStrAuxEquals`


**Definition:** Applies or references the 'PassiveIfStrAuxEquals' effect/state.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`value`](./Math_Equations.md) | Equation | The numeric value or formula associated with the buff. | 7 | `.5`<br>`0`<br>`1` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 7 | `{ . . . }` |

</details>


---


### Object: `StatusOnKillEnemy`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 10 | passives<br>class<br>	ag |
| [`DamageUp`](./Enums.md) | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 4 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`ManaGain`](./Enums.md) | Equation | The amount of mana restored to the source, which can be an expression. | 2 | `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`Brace`](./Enums.md) | Array / Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 1 | `1`<br>`10`<br>`2` |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum  | The name of the ability the source is forced to use, optionally with a chance. | 1 | `CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| [`LuckUp`](./Enums.md) | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 1 | `-1`<br>`-2`<br>`-4` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `AddStatusToAllDamage`


**Definition:** Modifier: Injects a status effect into a specific action.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 12 | passives<br>class<br>	ag |
| `must_do_damage` | Boolean || 3 | `true` |
| [`Conditional_HasStatus`](./Passives_and_Statuses.md#object-conditional_hasstatus) | Object  || 3 | `{ . . . }` |
| [`Conditional_HasTag`](./Passives_and_Statuses.md#object-conditional_hastag) | Object  | Evaluates whether the target has a specific tag; if true, applies the effects within; otherwise, runs the Else block. | 3 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 | `Default`<br>`FormChange`<br>`Druid` | [`KnockbackIfCrit`](Engine_StatusAndPassiveKeys.md#object-knockbackifcrit) | Object || 3 | Default<br>FormChange<br>Druid |
| [`Rot`](./Enums.md) | Integer | Integer, or an array [stacks, probability] specifying the amount of Rot stacks applied with the given probability. | 1 | `-999999`<br>`1`<br>`2` |

</details>


---


### Object: `ApplyToSource`


**Definition:** Redirects the nested effects to apply to the caster/source of the ability instead of the target.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Items_and_Equipment.md#context-addstatustobasicattack), [`Conditional_HasStatus`](./Items_and_Equipment.md#context-conditional_hasstatus), [`Else`](./Items_and_Equipment.md#context-else)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 22 | passives<br>class<br>	ag |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 20 | `Default`<br>`FormChange`<br>`Druid` | [`AllStatsUp`](./Enums.md) | Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 14 | Default<br>FormChange<br>Druid |
| [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 6 | `1`<br>`10`<br>`2` |
| [`StrengthUp`](./Enums.md) | Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 6 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| [`Charge`](./Enums.md) | Equation | The number of charge stacks applied. | 2 | `1`<br>`2`<br>`3` |
| [`SpeedUp`](./Enums.md) | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 1 | `-1`<br>`-2`<br>`-4` |

</details>


---


### Object: `GainCoinsRange`


**Definition:** No definition provided.  
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


**Definition:** Applies or references the 'ItemAuxTransform' effect/state.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`le`](./Arrays.md#array-le) | Array || 3 | `[10 MoneyBag_Small]`<br>`[25 MoneyBag_Medium]`<br>`[50 MoneyBag_Large]` |
| [`ge`](./Arrays.md#array-ge) | Array || 2 | `[10 NuclearKnife_Glowing]`<br>`[2 WaterBottle_Full]`<br>`[20 BlackShard_Glowing]` |
| [`lt`](./Arrays.md#array-lt) | Array || 1 | `[10 NuclearKnife]` |

</details>


---


### Object: `PassiveWhenOnTile`


**Definition:** State Trigger: Grants passives when this condition is met.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 7 | passives<br>class<br>	ag |
| [`tile`](./Arrays.md#array-tile) | Array / Enum | Specifies the tile type(s) to change to, either a single tile string or an array of tiles. | 7 | `BrambleTile`<br>`CreepTile`<br>`DirtTile` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 7 | `{ . . . }` |

</details>


---


### Object: `StatusAlliesOnBattleStart`


**Definition:** Applies or references the 'StatusAlliesOnBattleStart' effect/state.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 5 | passives<br>class<br>	ag |
| [`SpeedUp`](./Enums.md) | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 2 | `-1`<br>`-2`<br>`-4` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid` | [`Brace`](./Enums.md) | Enum / Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 2 | Default<br>FormChange<br>Druid |
| [`ConstitutionUp`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 1 | `-1`<br>`-2`<br>`1` |
| [`DamageUp`](./Enums.md) | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 1 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`StrengthUp`](./Enums.md) | Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 1 | `"max(int, 0)"`<br>`-1`<br>`-2` |

</details>


---


### Object: `StatusOnDie`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 5 | passives<br>class<br>	ag |
| [`Conditional_RandomChance`](./Miscellaneous.md#object-conditional_randomchance) | Object  || 1 | `{ . . . }` |
| [`CreateGlobalModifiers`](./Passives_and_Statuses.md#object-createglobalmodifiers) | Object  | Defines global gameplay modifiers to activate. | 1 | `{ . . . }` |
| [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Enum  | Specifies the loot pool from which to find an item, with an optional chance. | 1 | `blackbird_pool`<br>`chapter`<br>`chapter_common` |
| [`GainCoinsRange`](./Miscellaneous.md#object-gaincoinsrange) | Object  | An object with `min` and `max` fields specifying a range for the amount of coins gained. | 1 | `{ . . . }` |
| [`RandomMagicMissile`](./Enums.md) | Integer | The number of random magic missiles fired, or an object defining its properties. | 1 | `1`<br>`10`<br>`2` |
| [`RandomStatusFromPool`](./Passives_and_Statuses.md#object-randomstatusfrompool) | Object  | A collection of status effects; one is randomly chosen and applied to the target. | 1 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusOnEndMove`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `Temporary`


**Definition:** A wrapper object for applying status effects that automatically expire.  
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


**Definition:** Applies or references the 'TransformItemOnElementInfluence' effect/state.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 5 | `Electric`<br>`Fire`<br>`Gravity` |
| `full_repair` | Boolean || 5 | `true` |
| [`item`](./Enums.md#enum-item) | Enum | Specifies the item to transform into, either by name, a nested item object, or a numeric value. | 5 | `1`<br>`2`<br>`EstusFlask_Full` |

</details>


---


### Object: `AddDamageToElementDamage`


**Definition:** Applies or references the 'AddDamageToElementDamage' effect/state.  
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


**Definition:** Applies the 'AddPassivesToMinions' effect.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 41 | passives<br>class<br>	ag |
| [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 7 | `1`<br>`10`<br>`2` |
| [`AddMaxHealth`](./Enums.md) | Integer | The amount added to the unit's maximum health. Negative values reduce max health. | 6 | `-25`<br>`10`<br>`2` |
| [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#object-addstatustobasicattack) | Object  | Contains status effects to add to the basic attack. | 4 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid` | [`AllStatsUp`](./Enums.md) | Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | Default<br>FormChange<br>Druid |
| [`Shield`](./Enums.md) | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 1 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |

</details>


---


### Object: `ChanceToRevive`


**Definition:** No definition provided.  
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


**Definition:** Conditional trigger: Executes nested logic if the target currently has the specified status effect.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToAllDamage`](./Items_and_Equipment.md#context-addstatustoalldamage), [`StatusOnTookDamage`](./Items_and_Equipment.md#context-statusontookdamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 20 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 22 | passives<br>class<br>	ag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 10 | Default<br>FormChange<br>Druid |
| [`ApplyToSource`](./Passives_and_Statuses.md#object-applytosource) | Object  | An object of effects that are applied to the source of the ability (the caster). | 3 | `{ . . . }` |
| `FlatLeechIfDamaged` | `Number` | The flat amount of health leeched when the unit takes damage. | 1 | `3`<br>`5` |
| [`RemoveStatusStacks`](./Miscellaneous.md#object-removestatusstacks) | Object  | An object specifying a status name and the number of stacks to remove from the target. | 1 | `{ . . . }` |
| [`ImmediateUseAbility_Instant`](./Enums.md#enum-immediateuseability_instant) | Enum  || 1 | `head_CrownOfHorns` |

</details>


---


### Object: `Conditional_OncePerBattle`


**Definition:** Conditional trigger: Executes nested logic only once per encounter/battle.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HealthThreshold`](./Items_and_Equipment.md#context-conditional_healththreshold), [`StatusOnFullMana`](./Items_and_Equipment.md#context-statusonfullmana)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 | passives<br>class<br>	ag |
| [`key`](./Enums.md#enum-key) | Enum | A unique string identifier used to track if an effect has been applied once per turn, preventing reapplication. | 3 | `EtherSoakedRag`<br>`JewelOfDrog`<br>`TaintedOffering` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 | Default<br>FormChange<br>Druid |
| [`ShowText`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the localization key for a popup text displayed on the target. | 1 | `"COMBAT_POPUP_BRAINSTORM"`<br>`"COMBAT_POPUP_RELOAD"`<br>`"COMBAT_POPUP_REPAIRED"` |
| [`ReduceManaCost`](./Enums.md) | Integer | The number of stacks reducing mana cost of abilities. | 1 | `1`<br>`2` |
| [`Shield`](./Enums.md) | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 1 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`SpellDamageUp`](./Enums.md) | Integer | The number of stacks of SpellDamageUp applied, increasing spell damage. | 1 | `1`<br>`3` |

</details>


---


### Object: `Craft`


**Definition:** Synthesizes or spawns a new item from a specific pool.  
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


**Definition:** Applies or references the 'DelayedAutoRevive' effect/state.  
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


**Definition:** No definition provided.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `GlobalEnemyAutoRevive` | Integer | The percentage chance for all enemies to automatically revive after being defeated. | 2 | `100%`<br>`30%` |
| `NoCorpses` | `Number` | If set to 1, corpses are prevented from spawning. | 1 | `1` |
| `RealTimePressure` | Integer | The number of real-time seconds before a pressure effect or penalty applies. | 1 | `5` |
| [`{Global Modifier Keys}`](./Engine_GlobalModifierKeys.md#valid-property-keys) | Variable | Inherits game-wide rule modifiers. You can utilize any key from the Engine Global Modifier Keys list here to alter overarching game mechanics (e.g., changing gravity or stamina costs). | 1 | `CreateGlobalModifiers`<br>`BloodRain`<br>`NextPlayerCatTakesExtraTurn` |

</details>


---


### Object: `PassiveAtHealthThreshold`


**Definition:** Applies or references the 'PassiveAtHealthThreshold' effect/state.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`mode`](./Enums.md#enum-mode) | Enum | Specifies the comparison mode (equal, greater, less_or_equal, etc.) used for a conditional check. | 9 | `equal`<br>`greater`<br>`greater_or_equal` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 15 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 9 | `{ . . . }` |
| [`threshold`](./Passives_and_Statuses.md#object-threshold) | Enum / Integer / Object  | The health threshold value, either as a formula using X (max health) or a fixed integer. | 9 | `{ . . . }`<br>`"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |

</details>


---


### Object: `SpawnObjectOnPopCorpse`


**Definition:** No definition provided.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`count`](./Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 1 | `0`<br>`1`<br>`10` |
| `except_tiny` | Boolean || 1 | `true` |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 1 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |

</details>


---


### Object: `StatusOnTakeHealthOrShieldDamage`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | passives<br>class<br>	ag |
| [`DivineShield`](./Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 2 | `1`<br>`2`<br>`4` |
| [`Conditional_GoodRoll`](./Passives_and_Statuses.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 1 | `{ . . . }` |
| `Metronome` | `Number` | The number of times Metronome triggers, or an object with stacks and banned abilities. | 1 | `1`<br>`2` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `StatusRandomEnemiesOnBattleStart`


**Definition:** Applies or references the 'StatusRandomEnemiesOnBattleStart' effect/state.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`count`](./Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 7 | `0`<br>`1`<br>`10` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 7 | passives<br>class<br>	ag |
| [`Fear`](./Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 3 | `1`<br>`10`<br>`2` |
| [`Charmed`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 1 | `1`<br>`2`<br>`3` |
| [`Confusion`](./Enums.md) | Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`10`<br>`2` |
| [`Freeze`](./Arrays.md#array-freeze) | Array / Integer  | The amount of freeze stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`2`<br>`[1 .01]` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `CatchProjectiles`


**Definition:** Applies or references the 'CatchProjectiles' effect/state.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ally_chance` | Integer || 5 | `100%`<br>`15%` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 5 | `.02`<br>`.1`<br>`.15` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 6 | passives<br>class<br>	ag |
| [`Quivered`](./Arrays.md#array-quivered) | Array / Integer  | The amount of quivered stacks applied, or an [stacks, probability] array. | 5 | `1`<br>`2`<br>`5` |

</details>


---


### Object: `ClassManaCostReduction`


**Definition:** Applies or references the 'ClassManaCostReduction' effect/state.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `reduction` | Integer || 7 | `1`<br>`2`<br>`3` |
| [`class`](./Enums.md#enum-class) | Enum | Specifies the class that this ability belongs to, used for categorization and restrictions. | 6 | `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |

</details>


---


### Object: `Conditional_PartyMember`


**Definition:** Conditional constraint. Nested properties only trigger if this is true.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ExtraStatusWhenDealingDamage`](./Items_and_Equipment.md#context-extrastatuswhendealingdamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | passives<br>class<br>	ag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `CounterAttack`


**Definition:** No definition provided.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 5 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `melee_only` | Boolean || 1 | `true` |
| `ranged_only` | Boolean | If true, the reaction only triggers on ranged attacks. | 1 | `true` |

</details>


---


### Object: `Else`


**Definition:** Fallback object that executes if the preceding `Conditional_` block evaluated to false.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_PartyMember`](./Items_and_Equipment.md#context-conditional_partymember)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 19 | passives<br>class<br>	ag |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 23 | `Default`<br>`FormChange`<br>`Druid` | [`ApplyToSource`](Abilities_and_Spells.md#object-applytosource) | Object | An object of effects that are applied to the source of the ability (the caster). | 14 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `ExtraStatusWhenDealingDamage`


**Definition:** Applies or references the 'ExtraStatusWhenDealingDamage' effect/state.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `PassiveWhenDead`


**Definition:** State Trigger: Grants passives when this condition is met.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `SetItemAux`


**Definition:** No definition provided.  
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


**Definition:** No definition provided.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`number`](./Arrays.md#array-number) | Array / Integer || 31 | `1`<br>`10`<br>`2` |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 23 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |

</details>


---


### Object: `SpawnOnBattleStartRandomEmptyTile`


**Definition:** Applies or references the 'SpawnOnBattleStartRandomEmptyTile' effect/state.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 11 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`number`](./Arrays.md#array-number) | Array / Integer || 10 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `StackingFlowerTrail`


**Definition:** Applies or references the 'StackingFlowerTrail' effect/state.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`stack_key`](./Enums.md#enum-stack_key) | Enum || 3 | `CATHIDE`<br>`EMPTY_GENERATOR`<br>`FANNY_PACK` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 3 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |

</details>


---


### Object: `StatusAllCharactersOnSpawn`


**Definition:** Applies or references the 'StatusAllCharactersOnSpawn' effect/state.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>	ag |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 | `Default`<br>`FormChange`<br>`Druid` | [`Conditional_Boss`](Abilities_and_Spells.md#object-conditional_boss) | Object || 0 | Default<br>FormChange<br>Druid |
| [`Poison`](./Enums.md) | Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `StatusEveryXSpellCasts`


**Definition:** Applies or references the 'StatusEveryXSpellCasts' effect/state.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 8 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 9 | passives<br>class<br>	ag |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 | `Default`<br>`FormChange`<br>`Druid` | [`Charge`](./Enums.md) | Integer | The number of charge stacks applied. | 3 | Default<br>FormChange<br>Druid |
| [`IntelligenceUp`](./Enums.md) | Array / Equation | The amount of Intelligence added as a flat bonus. | 1 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| [`ObjectOnHitCharacter`](./Passives_and_Statuses.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 1 | `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |

</details>


---


### Object: `StatusOnPopCorpse`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 5 | passives<br>class<br>	ag |
| [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 3 | `1`<br>`10`<br>`2` |
| [`RepairTrinket`](./Enums.md) | Integer | The number of stacks of the Repair Trinket status effect to apply. | 1 | `1`<br>`99` |
| [`RepairWeapon`](./Arrays.md#array-repairweapon) | Array / Integer  | The number of weapon durability points restored; an array [stacks, probability] applies a chance-based repair. | 1 | `1`<br>`6`<br>`99` |

</details>


---


### Object: `StatusOnTurnEndIfDidntCastAbilityTypes`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 5 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 | passives<br>class<br>	ag |
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


**Definition:** Applies the 'AddStatusToElementDamage' effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 6 | `Electric`<br>`Fire`<br>`Gravity` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 8 | passives<br>class<br>	ag |
| [`Burn`](./Enums.md) | Equation | The amount of Burn applied, either as a fixed number or a formula string. | 3 | `1`<br>`10`<br>`2` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid` | [`Stun`](./Enums.md) | Array | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `AddStatusToKnockbackDamage`


**Definition:** Modifier: Injects a status effect into a specific action.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `AddStatusToSpells`


**Definition:** Modifier: Injects a status effect into a specific action.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `ApplyStatusesToRandomEnemiesEachTurn`


**Definition:** Applies or references the 'ApplyStatusesToRandomEnemiesEachTurn' effect/state.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 | passives<br>class<br>	ag |
| [`Bounty`](./Enums.md) | Integer | The number of bounty stacks applied to enemies, increasing rewards on defeat. | 3 | `1`<br>`3` |
| [`count`](./Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 2 | `0`<br>`1`<br>`10` |
| [`Marked`](./Enums.md) | Integer | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`3`<br>`5` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `ArmorBreakOnHit`


**Definition:** Applies or references the 'ArmorBreakOnHit' effect/state.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance_to_break` | Integer || 2 | `10%`<br>`5%` |
| `durability_loss` | Integer || 2 | `0` |

</details>


---


### Object: `bonus_passives`


**Definition:** Passives granted to the character while this ability is equipped.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`str_aux_is_copy_ability`](./Items_and_Equipment.md#context-str_aux_is_copy_ability)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 125 | passives<br>class<br>	ag |
| [`ModifyAbility`](./Miscellaneous.md#object-modifyability) | Object  || 2 | `{ . . . }` |

</details>


---


### Object: `BoostWeaponDamage`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `crit_chance` | `Equation` | The chance for the damage instance to critically hit, expressed as a percentage or equation; values above 1 default to 100%. | 4 | `-999999`<br>`.05*X`<br>`.25` |
| [`damage`](./Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 4 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Variable | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 4 | `damage_instance`<br>`spell`<br>`self_damage` |

</details>


---


### Object: `ChanceToBackflip`


**Definition:** Applies or references the 'ChanceToBackflip' effect/state.  
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


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `backstab_only` | Boolean || 1 | `true` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |

</details>


---


### Object: `Conditional_Adjacent`


**Definition:** Conditional object: Executes nested logic only if the target is/has Adjacent.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ScaledStatusAlliesOnSpendMana`](./Items_and_Equipment.md#context-scaledstatusalliesonspendmana), [`StatusAlliesEachTurn`](./Items_and_Equipment.md#context-statusallieseachturn)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 | passives<br>class<br>	ag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | Default<br>FormChange<br>Druid |
| [`Conditional_Ally`](./Passives_and_Statuses.md#object-conditional_ally) | Object  || 1 | `{ . . . }` |
| [`Conditional_PlayerCat`](./Miscellaneous.md#object-conditional_playercat) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `Conditional_BadRoll`


**Definition:** Conditional trigger: Executes nested logic based on a randomized bad outcome probability.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnBegin`](./Items_and_Equipment.md#context-statuseachturnbegin)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`odds`](./Enums.md#enum-odds) | Float | The probability of the effect occurring, expressed as a decimal or percentage. | 8 | `.1`<br>`.16666666`<br>`.3` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 6 | passives<br>class<br>	ag |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 8 | `Default`<br>`FormChange`<br>`Druid` | [`Temporary`](Abilities_and_Spells.md#object-temporary) | Object | Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions. | 8 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `Conditional_Boss`


**Definition:** Conditional trigger: Executes nested logic if the target is a Boss.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusAllCharactersOnSpawn`](./Items_and_Equipment.md#context-statusallcharactersonspawn)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 7 | passives<br>class<br>	ag |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 6 | `Default`<br>`FormChange`<br>`Druid` | [`AllStatsUp`](./Enums.md) | Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 14 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `cost`


**Definition:** Object defining resource requirements (Mana, Act Points, Moves) needed to cast.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ModifyAbility`](./Items_and_Equipment.md#context-modifyability)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `mana` | Equation || 1605 | `"4-clamp(floor(X/7), 0, 1)"`<br>`"max(4-X, 0)"`<br>`"max(7-2*X,0)"` |
| `charge` | Equation || 18 | `"1-clamp(spd,0,1)"`<br>`0`<br>`1` |

</details>


---


### Object: `CreateGlobalModifiers`


**Definition:** Generates global map or encounter rules/modifiers.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnDie`](./Items_and_Equipment.md#context-statusondie), [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Global Modifier Keys}`](./Engine_GlobalModifierKeys.md#valid-property-keys) | Variable | Inherits game-wide rule modifiers. You can utilize any key from the Engine Global Modifier Keys list here to alter overarching game mechanics (e.g., changing gravity or stamina costs). | 5 | `CreateGlobalModifiers`<br>`BloodRain`<br>`NextPlayerCatTakesExtraTurn` |
| `NextPlayerCatTakesExtraTurn` | `Number` | The number of extra turns the active player cat gains. | 1 | `1` |
| `NoCorpses` | `Number` | If set to 1, corpses are prevented from spawning. | 1 | `1` |

</details>


---


### Object: `DoDamage`


**Definition:** Explicitly triggers a secondary damage instance independent of the main attack.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachRoundEnd`](./Items_and_Equipment.md#context-statuseachroundend), [`StatusOnBreakItem`](./Items_and_Equipment.md#context-statusonbreakitem)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 7 | passives<br>class<br>	ag |
| [`damage`](./Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 7 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 7 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Variable | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 7 | `damage_instance`<br>`spell`<br>`self_damage` |
| [`damage_tiles`](./Enums.md#enum-damage_tiles) | Enum | Specifies whether the damage effect applies to tiles; 'all' damages every tile in the area. | 4 | `all` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 4 | `{ . . . }` |

</details>


---


### Object: `ElementalManaCostReduction`


**Definition:** Applies the 'ElementalManaCostReduction' effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `reduction` | Integer || 5 | `1`<br>`2`<br>`3` |
| [`element`](./Arrays.md#array-element) | Array / Enum | Specifies which element(s) the conditional checks against. | 5 | `Electric`<br>`Fire`<br>`Gravity` |

</details>


---


### Object: `ImmediateUseAbility`


**Definition:** No definition provided.  
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


**Definition:** Forces specific UI tooltips to appear when hovering over the ability.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 11 | passives<br>class<br>	ag |
| [`DivineShield`](./Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | `1`<br>`2`<br>`4` |
| [`Immobile`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 1 | `0`<br>`1`<br>`10%` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `meta`


**Definition:** Object defining UI display data (Name, Description, Icon).  
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


**Definition:** Applies or references the 'ModifyAbility' effect/state.  
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


**Definition:** Reaction: Triggers an effect or ability when forced to move.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveWhileHasDurability`](./Items_and_Equipment.md#context-passivewhilehasdurability), [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 11 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `enemies_only` | Boolean | If true, the arc lightning effect only chains to enemy units, ignoring allies. | 7 | `false`<br>`true` |
| `on_self_move_too` | Boolean | If true, the reaction triggers when the unit themselves move. | 3 | `true` |
| `create_temp_ability` | Boolean || 2 | `true` |

</details>


---


### Object: `ObjectOnHitCharacter`


**Definition:** No definition provided.  
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


**Definition:** Intrinsic passive modifier.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | passives<br>class<br>	ag |
| [`Metal`](./Enums.md) | Integer || 2 | `1` |

</details>


---


### Object: `PassiveAtStatThreshold`


**Definition:** Applies the 'PassiveAtStatThreshold' effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 31 | passives<br>class<br>	ag |
| [`mode`](./Enums.md#enum-mode) | Enum | Specifies the comparison mode (equal, greater, less_or_equal, etc.) used for a conditional check. | 13 | `equal`<br>`greater`<br>`greater_or_equal` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 13 | `{ . . . }` |
| [`threshold`](./Passives_and_Statuses.md#object-threshold) | Enum / Integer / Object  | The health threshold value, either as a formula using X (max health) or a fixed integer. | 13 | `{ . . . }`<br>`"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |

</details>


---


### Object: `PassiveIfWeaponIsUsable`


**Definition:** Applies or references the 'PassiveIfWeaponIsUsable' effect/state.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | passives<br>class<br>	ag |
| [`Brace`](./Enums.md) | Array / Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 2 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `RefreshEquipmentAbilityOnElement`


**Definition:** Applies or references the 'RefreshEquipmentAbilityOnElement' effect/state.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 2 | `Electric`<br>`Fire`<br>`Gravity` |
| [`text`](./Strings.md#string-text) | String || 2 | `""`<br>`"COMBAT_POPUP_RECHARGED"`<br>`"INJURY_NAME_BROKENLEG"` |

</details>


---


### Object: `SpawnItemLinkedFamiliar`


**Definition:** Applies or references the 'SpawnItemLinkedFamiliar' effect/state.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `break_on_pop_only` | Boolean || 2 | `true` |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 2 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |

</details>


---


### Object: `StatusAfterCastSpell`


**Definition:** Applies or references the 'StatusAfterCastSpell' effect/state.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 4 | `Default`<br>`FormChange`<br>`Druid` | [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 | Default<br>FormChange<br>Druid |
| [`TempMeleeRangeUp`](./Enums.md) | Integer || 1 | `1` |
| [`TempRangeUp`](./Enums.md) | Integer | The amount of temporary range increase applied. | 1 | `1`<br>`2`<br>`20` |
| [`UseAbility`](./Enums.md#enum-useability) | Enum  | The name of the ability the target is forced to use. | 1 | `GirlDinoPoop`<br>`KirbySpit`<br>`MD_PoopChain` |

</details>


---


### Object: `StatusAfterXStacks`


**Definition:** Applies or references the 'StatusAfterXStacks' effect/state.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ScaledStatusOnSpendMana`](./Items_and_Equipment.md#context-scaledstatusonspendmana), [`StatusOnCollectPickup`](./Items_and_Equipment.md#context-statusoncollectpickup)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`stack_key`](./Enums.md#enum-stack_key) | Enum || 2 | `CATHIDE`<br>`EMPTY_GENERATOR`<br>`FANNY_PACK` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | passives<br>class<br>	ag |
| [`threshold`](./Passives_and_Statuses.md#object-threshold) | Enum / Integer / Object  | The health threshold value, either as a formula using X (max health) or a fixed integer. | 2 | `{ . . . }`<br>`"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |
| `expires_on_end_turn` | Boolean | If true, the temporary effect expires at the end of the target's turn. | 1 | `true` |
| [`ExtraBasicMoves_Status`](./Enums.md) | Integer | The number of extra basic moves per turn granted. | 1 | `1` |
| [`RefreshActPoints`](./Enums.md) | Integer | The amount of action points restored to the source. | 1 | `1` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusIfUnusedActPoints`


**Definition:** Applies or references the 'StatusIfUnusedActPoints' effect/state.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `StatusOnAllyCatDeath`


**Definition:** Event Trigger: Applies nested statuses when ally cat death.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 5 | passives<br>class<br>	ag |
| [`DivineShield`](./Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | `1`<br>`2`<br>`4` |
| [`RepairTrinket`](./Enums.md) | Integer | The number of stacks of the Repair Trinket status effect to apply. | 1 | `1`<br>`99` |

</details>


---


### Object: `StatusOnBackstab`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SerratedClaws` | Integer | The number of stacks of the SerratedClaws status applied, or an object defining its display strings. | 1 | `1` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>	ag |
| [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 1 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `StatusOnBreakItem`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 | passives<br>class<br>	ag |
| [`Shield`](./Enums.md) | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 2 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`DoDamage`](./Miscellaneous.md#object-dodamage) | Object  | Contains damage parameters (amount, type, tile targets) to deal damage to the target. | 1 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusOnCastSpell`


**Definition:** Event Trigger: Applies nested statuses when cast spell.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 5 | passives<br>class<br>	ag |
| [`Charge`](./Enums.md) | Equation | The number of charge stacks applied. | 4 | `1`<br>`2`<br>`3` |
| [`Shield`](./Enums.md) | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 1 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusOnGainCoins`


**Definition:** Event Trigger: Applies nested statuses when gain coins.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 | passives<br>class<br>	ag |
| [`LuckUp`](./Enums.md) | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 1 | `-1`<br>`-2`<br>`-4` |
| [`Shield`](./Enums.md) | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 1 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `str_aux_is_copy_ability`


**Definition:** No definition provided.  
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


**Definition:** Examples: `4*champion_multiplier, 3*champion_multiplier, 1`  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveAtStatThreshold`](./Items_and_Equipment.md#context-passiveatstatthreshold)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`int`](./Enums.md#enum-int) | Enum / Integer  || 8 | `-1`<br>`-10`<br>`-2` |
| [`con`](./Enums.md#enum-con) | Enum / Integer  | The Constitution stat value or modifier. | 1 | `-1`<br>`-2`<br>`-3` |

</details>


---


### Object: `AbilityHealthThreshold`


**Definition:** AI Trigger: Executes an ability when health drops below a specific threshold.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 13 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 12 | passives<br>class<br>	ag |
| [`threshold`](./Passives_and_Statuses.md#object-threshold) | Enum / Integer / Object  | The health threshold value, either as a formula using X (max health) or a fixed integer. | 12 | `{ . . . }`<br>`"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 7 | `true` |
| `immediate` | Boolean | If true, the action (e.g., attack) occurs instantly without waiting for the unit's turn in the initiative order. | 6 | `false`<br>`true` |
| `aux` | Integer | An auxiliary integer value used for item properties, such as hunger value. | 1 | `-1`<br>`1`<br>`10` |

</details>


---


### Object: `AbilityOnRoundEndOnce`


**Definition:** Applies or references the 'AbilityOnRoundEndOnce' effect/state.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `even_of_stunned` | Boolean || 1 | `true` |

</details>


---


### Object: `AddAdvantageToEvent`


**Definition:** Applies or references the 'AddAdvantageToEvent' effect/state.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`add`](./Arrays.md#array-add) | Array / Integer  || 1 | `5`<br>`[0.05 0.05 0.05]` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`options`](./Arrays.md#array-options) | Array  || 1 | `[smash bash open]` |

</details>


---


### Object: `AddPassivesToCharmed`


**Definition:** Applies the 'AddPassivesToCharmed' effect.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 9 | passives<br>class<br>	ag |
| [`AllStatsUp`](./Enums.md) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | `-1`<br>`-2`<br>`1` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `AddSelfStatusToWeapons`


**Definition:** Applies the 'AddSelfStatusToWeapons' effect.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `AddStatusToBackstabs`


**Definition:** Modifier: Injects a status effect into a specific action.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>	ag |
| [`Bleed`](./Enums.md) | Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `AddStatusToWeapons`


**Definition:** Applies the 'AddStatusToWeapons' effect.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 | passives<br>class<br>	ag |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 | `Default`<br>`FormChange`<br>`Druid` | [`Leech`](./Enums.md) | Integer | The amount of health leeched from the target (heals the attacker). | 3 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `AddTemporaryEffectsToBasicAttack`


**Definition:** Applies the 'AddTemporaryEffectsToBasicAttack' effect.  
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


**Definition:** Applies or references the 'AIControlNextTurn' effect/state.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `include_spells` | Boolean || 1 | `true` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |

</details>


---


### Object: `AlluringDoodieEater`


**Definition:** Applies or references the 'AlluringDoodieEater' effect/state.  
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


**Definition:** Applies or references the 'AllyDodgeChanceAura' effect/state.  
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


**Definition:** Grants the nested passive abilities dynamically.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_RandomChance`](./Items_and_Equipment.md#context-conditional_randomchance)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 13 | passives<br>class<br>	ag |
| [`StatusOnBattleEnd`](./Passives_and_Statuses.md#object-statusonbattleend) | Object  | An object containing status effects or passives applied to the unit when the battle ends. | 5 | `{ . . . }` |

</details>


---


### Object: `ApplyToRandomPartyMemberIfPossible`


**Definition:** Redirects the nested effects to apply to a random living member of the player's party.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBreak`](./Items_and_Equipment.md#context-statusonbreak)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `AutocastEachRound`


**Definition:** Forces the character to automatically cast a specific ability at the start of each combat round.  
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


**Definition:** No definition provided.  
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


**Definition:** Applies the 'BouncyProjectiles' effect.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max_bounces` | Integer || 3 | `-1`<br>`1`<br>`10` |
| [`max_range`](./Enums.md#enum-max_range) | Enum / Integer   || 3 | `"4+(1-clamp(spd,0,1))*2"`<br>`"max(5-int, 1)"`<br>`-1` |

</details>


---


### Object: `BuffImmunity`


**Definition:** No definition provided.  
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


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddTemporaryEffectsToBasicAttack`](./Items_and_Equipment.md#context-addtemporaryeffectstobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>	ag |
| `OverrideDamage` | `Number` | Overrides the damage of the current action to this flat value (can be negative to heal). | 1 | `-10`<br>`0`<br>`1` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `CatPartsSizeScale`


**Definition:** Applies or references the 'CatPartsSizeScale' effect/state.  
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


**Definition:** Applies or references the 'ChanceToForceEvent' effect/state.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |
| [`event`](./Enums.md#enum-event) | Enum || 1 | `Blessing`<br>`Death`<br>`Tragedy` |

</details>


---


### Object: `Conditional_Ally`


**Definition:** Conditional trigger: Executes nested logic if the target is friendly to the caster.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Adjacent`](./Items_and_Equipment.md#context-conditional_adjacent)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 21 | passives<br>class<br>	ag |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 8 | `Default`<br>`FormChange`<br>`Druid` | [`ManaGain`](./Enums.md) | Integer | The amount of mana restored to the source, which can be an expression. | 4 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `Conditional_Corpse`


**Definition:** Conditional trigger: Executes nested logic if the target is a dead body/corpse.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 | passives<br>class<br>	ag |
| [`RandomMutation`](./Enums.md) | Integer | The number of random mutations to apply. | 1 | `1`<br>`3` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `Conditional_Enemy`


**Definition:** Conditional trigger: Executes nested logic if the target is hostile to the caster.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToSpells`](./Items_and_Equipment.md#context-addstatustospells)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 6 | passives<br>class<br>	ag |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 12 | `Default`<br>`FormChange`<br>`Druid` | [`Leeches`](./Enums.md) | Integer | The number of stacks of the Leeches debuff applied, which deals damage over time and heals the applier. | 8 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `Conditional_HasTag`


**Definition:** Conditional trigger: Executes nested logic if the target possesses the specified entity tag.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToAllDamage`](./Items_and_Equipment.md#context-addstatustoalldamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](./Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 46 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 49 | passives<br>class<br>	ag |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 11 | `Default`<br>`FormChange`<br>`Druid` | [`BonusKnockbackDamage`](./Enums.md) | Integer || 43 | Default<br>FormChange<br>Druid |
| [`OverrideChainKnockback`](./Enums.md) | Integer | The custom number of tiles for chain knockback, overriding the default. | 1 | `0`<br>`1`<br>`10` |

</details>


---


### Object: `Conditional_HealthThreshold`


**Definition:** Conditional trigger: Executes nested logic if the target's health falls below the specified threshold.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnTookDamage`](./Items_and_Equipment.md#context-statusontookdamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | passives<br>class<br>	ag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 7 | Default<br>FormChange<br>Druid |
| `threshold_flat` | Integer | The flat health value (in hit points) below which the target must be for the conditional to trigger. | 5 | `0`<br>`10`<br>`3` |
| [`Conditional_OncePerBattle`](./Miscellaneous.md#object-conditional_onceperbattle) | Object  | An object containing effects that can only trigger once per battle, preventing double-activation. | 1 | `{ . . . }` |

</details>


---


### Object: `Conditional_ManaThreshold`


**Definition:** Conditional constraint. Nested properties only trigger if this is true.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnEnd`](./Items_and_Equipment.md#context-statuseachturnend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `threshold_flat` | Integer || 1 | `0`<br>`10`<br>`3` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>	ag |
| [`RepairTrinket`](./Enums.md) | Integer | The number of stacks of the Repair Trinket status effect to apply. | 1 | `1`<br>`99` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `Conditional_PlayerCat`


**Definition:** Conditional trigger: Executes nested logic if the target is a player-controlled cat.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Adjacent`](./Items_and_Equipment.md#context-conditional_adjacent)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 | passives<br>class<br>	ag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | Default<br>FormChange<br>Druid |
| [`Charge`](./Enums.md) | Equation | The number of charge stacks applied. | 1 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `Conditional_RandomChance`


**Definition:** Conditional trigger: Executes nested logic based on a flat percentage random roll.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnDie`](./Items_and_Equipment.md#context-statusondie)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `odds` | Float | The probability of the effect occurring, expressed as a decimal or percentage. | 4 | `.1`<br>`.16666666`<br>`.3` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 4 | Default<br>FormChange<br>Druid |
| [`ApplyPassives`](./Miscellaneous.md#object-applypassives) | Object  | Specifies the passives or status effects to apply to the unit. | 2 | `{ . . . }` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | passives<br>class<br>	ag |

</details>


---


### Object: `Conditional_Shielded`


**Definition:** Conditional trigger: Executes nested logic if the target currently has a Shield status.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | passives<br>class<br>	ag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `ConvertDamageToScaledStatus`


**Definition:** Applies or references the 'ConvertDamageToScaledStatus' effect/state.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>	ag |
| [`DelayedPain`](./Enums.md) | Integer | The number of stacks of DelayedPain applied, dealing damage after a delay. | 1 | `1` |

</details>


---


### Object: `CritsApplyStatus`


**Definition:** Applies the 'CritsApplyStatus' effect.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 6 | passives<br>class<br>	ag |
| [`Fear`](./Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `damage_instance`


**Definition:** Object defining the combat math and status effects applied upon successful hit.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AlluringDoodieEater`](./Items_and_Equipment.md#context-alluringdoodieeater)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Variable | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 1731 | `damage_instance`<br>`spell`<br>`self_damage` |
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
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | passives<br>class<br>	ag |

</details>
<details>
<summary><b>AddStatusToKnockbackDamage</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | passives<br>class<br>	ag |

</details>
<details>
<summary><b>AddStatusToSpells</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>	ag |

</details>
<details>
<summary><b>ApplyToRandomPartyMemberIfPossible</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | passives<br>class<br>	ag |

</details>
<details>
<summary><b>Conditional_Adjacent</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 | passives<br>class<br>	ag |

</details>
<details>
<summary><b>Conditional_HealthThreshold</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | passives<br>class<br>	ag |

</details>
<details>
<summary><b>Conditional_PartyMember</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | passives<br>class<br>	ag |

</details>
<details>
<summary><b>Conditional_Shielded</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | passives<br>class<br>	ag |

</details>
<details>
<summary><b>ExtraStatusWhenDealingDamage</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | passives<br>class<br>	ag |

</details>
<details>
<summary><b>PassiveWhenDead</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | passives<br>class<br>	ag |

</details>
<details>
<summary><b>PassiveWhileHasDurability</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | passives<br>class<br>	ag |

</details>
<details>
<summary><b>ScaledStatusAlliesOnSpendMana</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | passives<br>class<br>	ag |

</details>
<details>
<summary><b>StatusAlliesEachTurn</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>	ag |

</details>
<details>
<summary><b>StatusIfUnusedActPoints</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | passives<br>class<br>	ag |

</details>
<details>
<summary><b>StatusOnEndMove</b></summary>

> **Total Count:** 9

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 8 | passives<br>class<br>	ag |

</details>
<details>
<summary><b>StatusOnFallAsleep</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | passives<br>class<br>	ag |

</details>


### Object: `DestroyEquipmentAndAttachParasite`


**Definition:** Removes an equipped item and replaces it with a parasite from a specified pool.  
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


**Definition:** Applies the 'Eternal' effect.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `health_percent` | Integer || 3 | `100%`<br>`50%` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 3 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |

</details>


---


### Object: `FlyDamageIncrease`


**Definition:** No definition provided.  
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


**Definition:** Applies or references the 'ForceUseAbilityOnTarget' effect/state.  
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


**Definition:** Applies or references the 'GlobalMeleeRevengeDamage' effect/state.  
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


**Definition:** Applies or references the 'KnockbackIfCrit' effect/state.  
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


**Definition:** Displaces the target vertically and horizontally away from the source.  
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


**Definition:** Applies or references the 'ManaGainRange' effect/state.  
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


**Definition:** Applies or references the 'ObjectDetector' effect/state.  
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


**Definition:** Applies or references the 'PassiveAfterXKills' effect/state.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 4 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 8 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 4 | `{ . . . }` |

</details>


---


### Object: `PassiveWhenAffectedByElement`


**Definition:** Examples: `{ ... }`  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 18 | `Electric`<br>`Fire`<br>`Gravity` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 30 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 18 | `{ . . . }` |

</details>


---


### Object: `PassiveWhileHasDurability`


**Definition:** Applies or references the 'PassiveWhileHasDurability' effect/state.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `PassiveWhileInMonkMeleeStance`


**Definition:** Applies the 'PassiveWhileInMonkMeleeStance' effect.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 | passives<br>class<br>	ag |
| [`Brace`](./Enums.md) | Array / Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 3 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `PassiveWhileShielded`


**Definition:** Applies or references the 'PassiveWhileShielded' effect/state.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>	ag |
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 1 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `PoopWhenHit`


**Definition:** No definition provided.  
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


**Definition:** Selects and applies a random status effect from the provided nested object.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnDie`](./Items_and_Equipment.md#context-statusondie)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 31 | passives<br>class<br>	ag |
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


**Definition:** Removes a specific number of stacks of a status effect.  
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


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleStart`](./Items_and_Equipment.md#context-statusonbattlestart)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `revive_health` | Integer | The amount of health (as a flat integer or percentage) the unit revives with. | 4 | `1`<br>`100%`<br>`50%` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | passives<br>class<br>	ag |
| [`Shield`](./Enums.md) | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 3 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `ScaldingOrbMoonBossOneShot`


**Definition:** Applies or references the 'ScaldingOrbMoonBossOneShot' effect/state.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CompleteItemQuest`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the item quest ID to mark as complete on kill. | 1 | `BlackShard`<br>`Nuke`<br>`ScaldingOrb` |
| [`RemoveItem`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the item ID to remove from the source on kill. | 1 | `BlackShard`<br>`BlackShard_Glowing`<br>`ScaldingOrb` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `ScaledStatusAlliesOnSpendMana`


**Definition:** Applies or references the 'ScaledStatusAlliesOnSpendMana' effect/state.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `ScaledStatusOnHolyShieldBlock`


**Definition:** Applies or references the 'ScaledStatusOnHolyShieldBlock' effect/state.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>	ag |
| [`RandomMagicMissile`](./Enums.md) | Integer | The number of random magic missiles fired, or an object defining its properties. | 1 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `ScaledStatusOnSpendMana`


**Definition:** Applies the 'ScaledStatusOnSpendMana' effect.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 | passives<br>class<br>	ag |
| [`StatusAfterXStacks`](./Miscellaneous.md#object-statusafterxstacks) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `SpawnOnDeath`


**Definition:** No definition provided.  
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


**Definition:** Applies or references the 'SpawnRandomPickupsOnTaggedUnitKilled' effect/state.  
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


**Definition:** Applies or references the 'StatDependentPassive' effect/state.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>	ag |
| [`AddDamageToBasicAttack`](./Enums.md) | Enum || 1 | `1`<br>`2`<br>`4` |

</details>


---


### Object: `StatusAdjacentOnTheirTurnEnd`


**Definition:** Applies or references the 'StatusAdjacentOnTheirTurnEnd' effect/state.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ForceMoveAway` | `Number` | The distance to force the target away from the source. | 1 | `1` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `StatusAfterXTurns`


**Definition:** Event Trigger: Applies a status effect after X turns have passed.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | passives<br>class<br>	ag |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum  | The name of the ability the source is forced to use, optionally with a chance. | 2 | `CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |

</details>


---


### Object: `StatusAlliesEachTurn`


**Definition:** Applies or references the 'StatusAlliesEachTurn' effect/state.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `StatusAlliesOnDeath`


**Definition:** Event Trigger: Applies nested statuses to allies on death.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 5 | passives<br>class<br>	ag |
| [`DivineShield`](./Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | `1`<br>`2`<br>`4` |

</details>


---


### Object: `StatusEachRoundEnd`


**Definition:** Applies or references the 'StatusEachRoundEnd' effect/state.  
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


**Definition:** Event Trigger: Applies nested statuses to each turn end for each turn.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 | passives<br>class<br>	ag |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum  | The name of the ability the source is forced to use, optionally with a chance. | 1 | `CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |

</details>


---


### Object: `StatusIfUnusedMovePoints`


**Definition:** Event Trigger: Applies nested statuses to if unused move points.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 7 | passives<br>class<br>	ag |
| [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 4 | `1`<br>`10`<br>`2` |
| [`Charge`](./Enums.md) | Equation | The number of charge stacks applied. | 2 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `StatusOnCollectPickup`


**Definition:** Event Trigger: Applies nested statuses when collect pickup.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>	ag |
| [`StatusAfterXStacks`](./Miscellaneous.md#object-statusafterxstacks) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `StatusOnDodge`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>	ag |
| [`DodgeChance_Status`](./Enums.md) | Integer | The flat percentage increase to dodge chance applied as a status effect. | 1 | `1`<br>`10`<br>`100` |

</details>


---


### Object: `StatusOnEatFood`


**Definition:** Event Trigger: Applies nested statuses when eat food.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 | passives<br>class<br>	ag |
| [`RepairTrinket`](./Enums.md) | Integer | The number of stacks of the Repair Trinket status effect to apply. | 1 | `1`<br>`99` |
| [`TempPassiveUntilSettled`](./Miscellaneous.md#object-temppassiveuntilsettled) | Object  || 1 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusOnEnemyDeath`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>	ag |
| [`Charge`](./Enums.md) | Equation | The number of charge stacks applied. | 1 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `StatusOnFallAsleep`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
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


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_OncePerBattle`](./Miscellaneous.md#object-conditional_onceperbattle) | Object  | An object containing effects that can only trigger once per battle, preventing double-activation. | 1 | `{ . . . }` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `StatusOnHealed`


**Definition:** Event Trigger: Applies nested statuses when healed.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 | passives<br>class<br>	ag |
| [`Shield`](./Enums.md) | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 1 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusOnPickupCoins`


**Definition:** Event Trigger: Applies nested statuses when pickup coins.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>	ag |
| [`GainCoins`](./Arrays.md#array-gaincoins) | Array / Integer  | The amount of coins gained, or a [min, max] range. | 1 | `-5`<br>`1`<br>`2` |

</details>


---


### Object: `StatusOnUseBasicAttack`


**Definition:** Event Trigger: Applies nested statuses when use basic attack.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 | passives<br>class<br>	ag |
| [`DamageUp`](./Enums.md) | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 1 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 1 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `StatusWhenAllySpendsMana`


**Definition:** Event Trigger: Applies nested statuses to when ally spends mana.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 | passives<br>class<br>	ag |
| [`Charge`](./Enums.md) | Equation | The number of charge stacks applied. | 1 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `TempPassiveUntilSettled`


**Definition:** Passive: Active only until the physics engine stops moving the character.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnEatFood`](./Items_and_Equipment.md#context-statusoneatfood)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>	ag |
| [`LimitHeal`](./Enums.md) | Integer | If 1, prevents the unit from being healed. | 1 | `0`<br>`1` |

</details>


---


### Object: `TintItem`


**Definition:** Applies or references the 'TintItem' effect/state.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ignore_if_str_aux_equals`](./Enums.md#enum-ignore_if_str_aux_equals) | Enum || 1 | `ModelingClay_Default` |
| [`add`](./Arrays.md#array-add) | Array / Equation || 1 | `5`<br>`[0.05 0.05 0.05]` |
| [`mul`](./Arrays.md#array-mul) | Array || 1 | `[0.45 0.3 0.25]` |

</details>


---


### Object: `TransformWeapon`


**Definition:** Transforms the equipped weapon into another specific weapon state.  
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


**Definition:** Applies or references the 'TunnelVision' effect/state.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `crit_chance` | `Equation` | The chance for the damage instance to critically hit, expressed as a percentage or equation; values above 1 default to 100%. | 1 | `-999999`<br>`.05*X`<br>`.25` |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Variable | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 1 | `damage_instance`<br>`spell`<br>`self_damage` |

</details>


---