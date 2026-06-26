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
| [`name`](./Strings.md#string-name) | Enum | Localization key for the item's name. | 3307 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2985 |  |
| [`desc`](./Strings.md#string-desc) | Enum | Localization key for the item's desc. | 2423 |  |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1910 ||
| [`variant_of`](./Enums.md#enum-variant_of) | Enum | Specifies the base character that this entry is a variant of. | 1195 |  |
| `frame` | Integer | The sprite frame index used for this arm. | 1105 |  |
| [`kind`](./Enums.md#enum-kind) | Enum | Specifies the equipment slot type (e.g., head, face, neck, trinket, modifier). | 1105 |  |
| [`set`](./Enums.md#enum-set) | Array / Enum | The visual set or furniture style tag (e.g., elegant, guts, Tentacle, wooden, Druid). | 985 |  |
| [`rarity`](./Enums.md#enum-rarity) | Enum | Determines the loot rarity tier of the item (e.g., very_rare, consumable_common). | 966 |  |
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 364 |  |
| `shield` | Enum / Integer | The unit's shield value, specified as an integer or a formula. | 191 |  |
| `durability` | Array / Integer | Maximum uses before breaking. | 170 |  |
| `cha` | Enum / Integer | Specifies the charisma stat value as an integer or 'aux' for auxiliary stat assignment. | 89 |  |
| `con` | Enum / Integer | The constitution stat value or modifier for the unit. | 79 |  |
| `spd` | Enum / Integer | The speed stat value or modifier for the unit. | 78 |  |
| `cursed` | Boolean | If true, the item is cursed and cannot be unequipped. | 77 |  |
| `int` | Enum / Integer |  | 66 |  |
| `consumable` | Boolean | If true, marks the item as consumable; can also specify a sub-object defining its item pool. | 64 |  |
| `lck` | Enum / Integer |  | 53 |  |
| [`str`](./Engine_DamagingKeys.md#valid-property-keys) | Variable |  | 45 |  |
| `quest_item` | Boolean | If true, the item is a critical quest item that cannot be discarded or destroyed. | 40 |  |
| `parasite` | Boolean | If true, this creature behaves as a parasite (e.g., attaches to or inhabits another unit). | 36 |  |
| `aux` | Integer | An integer modifier for the auxiliary stat, often used for scaling or effect values. | 33 |  |
| `dex` | Enum / Integer |  | 30 |  |
| [`keyword_tooltips`](Abilities_and_Spells.md#object-keyword_tooltips) | Object | Forces specific UI tooltips to appear when hovering over the ability. | 28 ||
| [`quest_reward_item`](./Enums.md#enum-quest_reward_item) | Enum || 22 ||
| `divine_shield` | Integer | The number of charges of divine shield that block incoming damage fully. | 20 ||
| `indestructible` | Boolean | If true, the object cannot be destroyed by any means. | 20 ||
| `speed` | Array / Number | The movement speed of the projectile or graphic, as a single number or a range [min max]. | 19 ||
| `legacy_quest` | Boolean | If true, this item is tied to a legacy quest system. | 17 ||
| [`hint_destination`](./Enums.md#enum-hint_destination) | Enum | Specifies the destination key or name that the item gives a hint towards. | 16 ||
| [`str_aux_initialize`](./Enums.md#enum-str_aux_initialize) | Enum || 15 ||
| `dont_destroy_on_0` | Boolean || 13 ||
| [`global_tags`](./Arrays.md#array-global_tags) | Array || 12 ||
| `max_durability` | Integer || 11 ||
| [`on_store`](./Enums.md#enum-on_store) | Enum || 8 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 7 ||
| [`hint_prerequisite_flag`](./Enums.md#enum-hint_prerequisite_flag) | Enum || 5 ||
| `failable` | Boolean | If true, the nuclear device's effect can fail to trigger. | 4 ||
| [`global_passives`](#object-global_passives) | Object || 4 ||
| `randomize_piece_frames` | Boolean || 4 ||
| `str_aux_is_copy_passive` | Boolean || 4 ||
| `fragile` | Boolean || 3 ||
| [`icon_hint`](./Enums.md#enum-icon_hint) | Enum || 3 ||
| `max_health` | Integer || 3 ||
| `reset_aux_on_store` | Integer || 3 ||
| `sticky` | Boolean || 3 ||
| `weightless` | Boolean || 3 ||
| [`passive`](Characters_and_Bosses.md#object-passive) | Object || 2 ||
| `prevent_level_up` | Boolean || 2 ||
| [`quest_item_alias`](./Enums.md#enum-quest_item_alias) | Enum || 2 ||
| [`str_aux_is_copy_ability`](#object-str_aux_is_copy_ability) | Object || 2 ||
| `str_aux_is_copy_item_passive` | Boolean || 2 ||
| [`Set`](./Enums.md#enum-set) | Enum | Applies or references the 'Set' effect/state. | 1 |  |
| `aux_is_catid` | Boolean || 1 ||
| `cant_equip_to_colorless` | Boolean || 1 ||
| `degrade_after_adventure` | Boolean || 1 ||
| [`equip_sound`](./Enums.md#enum-equip_sound) | Enum || 1 ||
| `force_sticky` | Boolean || 1 ||
| [`reset_str_aux_on_store`](./Enums.md#enum-reset_str_aux_on_store) | Enum || 1 ||
| [`str_aux`](./Enums.md#enum-str_aux) | Enum || 1 ||
| `str_aux_is_copy_item_active` | Boolean || 1 ||
| `str_aux_is_copy_item_icon` | Boolean || 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2039 ||
| [`AddStatusToBasicAttack`](Abilities_and_Spells.md#object-addstatustobasicattack) | Object | An object defining status effects to apply on basic attacks, with optional conditions. | 133 ||
| [`Brace`](./Enums.md) | Enum / Integer | The amount of flat damage reduction applied to the source. | 94 | 2 |
| [`Metal`](./Enums.md) | Integer || 90 | 1 |
| [`Trample`](./Enums.md) | Integer | The number of tiles this character can move through enemies, dealing damage or applying effects equal to the value. | 88 | 3 |
| [`Thorns`](./Enums.md) | Integer | The number of Thorns stacks applied, which deals damage back to melee attackers. | 65 | 2 |
| [`MeleeRevengeDamage`](Abilities_and_Spells.md#object-meleerevengedamage) | Object | A damage instance object that triggers when the unit is hit by melee attacks while this passive is active. | 59 ||
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of health regeneration (HealthRegen) granted by this damage instance. | 52 | 2 |
| [`StatusEachTurnEnd`](Cat_Mutations.md#object-statuseachturnend) | Object | Status effects that are applied to the unit at the end of each turn. | 49 ||
| [`StatusOnBattleEnd`](Abilities_and_Spells.md#object-statusonbattleend) | Object | A block containing status effects or passives that are applied to the unit when a battle ends. | 45 ||
| [`ElementImmune`](./Enums.md) | Enum | Specifies an element (e.g., Fire, Ice) the unit is immune to. | 39 | Ice |
| [`SpawnOnBattleStart`](Elite_Buffs.md#object-spawnonbattlestart) | Enum / Object | Specifies the object (e.g., Food, CharmedGamete) to spawn at the start of battle. | 36 | BuffCharmedKitten |
| [`DeathRattle`](./Enums.md) | Enum | Defines an ability or explosion that triggers upon the unit's death. | 35 | neck_NukeExplode |
| [`CounterAttack`](Cat_Mutations.md#object-counterattack) | Object | Specifies the ability name used for counterattacking when hit. | 34 ||
| [`StatusImmunity`](./Enums.md) | Array / Enum | List of status effects the unit is immune to. | 34 | [Confusion] |
| [`StatusOnKill`](Cat_Mutations.md#object-statusonkill) | Object | Status effects applied to the unit whenever it kills an enemy. | 29 ||
| [`StatusOnTookDamage`](Cat_Mutations.md#object-statusontookdamage) | Object | Status effects applied to the unit whenever it takes damage. | 29 ||
| [`SpawnThingOnDamage`](Cat_Mutations.md#object-spawnthingondamage) | Object | Object specifying an entity to spawn when the unit takes damage, with optional conditions. | 28 ||
| [`Undead`](./Enums.md) | Integer | Marks the unit as undead. Higher values may indicate undead type or tier. | 25 | 1 |
| [`Brittle`](./Enums.md) | Integer || 24 | 1 |
| [`AbilityReaction`](./Enums.md) | Enum | Specifies an ability to trigger as a reaction when certain conditions are met. | 23 | head_EmoSong |
| [`Fragile`](./Enums.md) | Integer || 22 | 1 |
| [`StatusOnBreak`](#object-statusonbreak) | Object || 22 ||
| [`AddPassivesToMinions`](#object-addpassivestominions) | Object || 21 ||
| [`DamageUp`](./Enums.md) | Integer | The amount of damage increase, or a string formula for dynamic calculation. | 21 | 2 |
| [`SpawnOnDeath`](Characters_and_Bosses.md#object-spawnondeath) | Object | Specifies the entity to spawn upon the unit's death. | 21 ||
| [`ArmorDodgeChance`](./Enums.md) | Integer || 19 | 5 |
| [`StatusEachTurnBegin`](Cat_Mutations.md#object-statuseachturnbegin) | Object | Status effects applied to the unit at the beginning of each turn. | 18 ||
| [`CritChanceUp`](./Enums.md) | Integer | The amount of critical hit chance increase, in percentage points. | 16 | 20 |
| [`AddBonusRange`](./Enums.md) | Integer | The number of extra tiles added to the unit's attack range. | 15 | 2 |
| [`KineticSpikes`](./Enums.md) | Integer | The number of Kinetic Spikes stacks applied, which deal damage back to attackers when the unit is hit. | 15 | 3 |
| [`RevengeDamage`](Abilities_and_Spells.md#object-revengedamage) | Object | An object specifying the effects (e.g., Marked, Charmed, Petrify) applied to the attacker when the unit takes damage. | 15 ||
| [`SpawnEachTurn`](Cat_Mutations.md#object-spawneachturn) | Object | Object specifying an entity to spawn each turn, with chance and number. | 15 ||
| [`StatusOnBattleStart`](#object-statusonbattlestart) | Object || 15 ||
| [`AddCorpseHealth`](./Enums.md) | Integer | The amount of additional health a corpse has when the unit dies. | 14 | 6 |
| [`AllStatsUp`](./Enums.md) | Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 14 | -2 |
| [`DodgeChance`](./Enums.md) | Integer | The percentage chance to dodge incoming attacks. | 14 | 25 |
| [`InnateElement`](./Enums.md) | Enum | Specifies the unit's innate elemental type (Fire, Ice, Electric, etc.). | 14 | Ice |
| [`AddManaRegen`](./Enums.md) | Integer | The amount of additional mana regeneration per turn granted while this passive is active. | 13 | 2 |
| [`DeathRattleRevive`](./Enums.md) | Enum | Defines an ability or effect that triggers when the unit would die but revives instead. | 13 | tk_PetrifiedPinky |
| [`Flammable`](./Enums.md) | Integer || 13 | 2 |
| [`AbilityHealthThreshold`](Characters_and_Bosses.md#object-abilityhealththreshold) | Object | Triggers an ability when the unit's health drops below a specified threshold. | 12 ||
| [`ReflectProjectiles`](./Enums.md) | Integer | The percentage chance to reflect projectiles back at the attacker. | 12 | 20 |
| [`SpawnThingOnDeath`](./Enums.md) | Enum | Specifies a specific entity to spawn upon death, distinct from standard spawns. | 12 | CharmedTinyTumor |
| [`AbilityOnBattleStart`](./Enums.md) | Enum || 11 | head_SpiderInjector |
| [`AddStatusToAllDamage`](#object-addstatustoalldamage) | Object || 11 ||
| [`BleedThorns`](./Enums.md) | Integer | The number of Bleed Thorns stacks applied, which deals bleeding damage back to melee attackers. | 11 | 3 |
| [`ExtraBasicAttacks`](./Enums.md) | Integer | The number of additional basic attacks the unit can perform each turn. | 11 | 2 |
| [`ReplaceBasicMove`](./Enums.md) | Enum | Specifies the ability that replaces the unit's default basic move. | 11 | head_HeadBrandJump |
| [`AddLevelUpRerolls`](./Enums.md) | Integer | The number of additional rerolls the unit gets when leveling up. | 10 | 3 |
| [`MoveTowardsDamageSource`](./Enums.md) | Enum | Causes the unit to move towards the source of damage, using a specified move ability. | 10 | MoveOne |
| [`StatusOnKillEnemy`](#object-statusonkillenemy) | Object || 10 ||
| [`AddSelfStatusToBasicAttack`](#object-addselfstatustobasicattack) | Object || 9 ||
| [`AddTag`](./Enums.md) | Enum | Specifies a unit tag (e.g., fetus, plant, bug) to add to the unit. | 9 | rock |
| [`Bruise`](./Enums.md) | Integer | The number of Bruise stacks applied, or an array with duration and chance. | 9 | 2 |
| [`DepressionAura`](./Enums.md) | Integer | The number of Depression stacks applied to nearby units as an aura. | 9 | 2 |
| [`Flying`](./Enums.md) | Integer | The number of stacks of the Flying status effect applied to the unit. | 9 | 1 |
| [`MissChance`](./Enums.md) | Integer | The percentage chance that the unit's attacks will miss. | 9 | 10 |
| [`MovementReaction`](Characters_and_Bosses.md#object-movementreaction) | Object | Triggers an ability when an entity moves near the unit. | 9 ||
| [`PoisonThorns`](./Enums.md) | Integer | Applies Poison stacks to any unit that attacks this unit in melee. | 9 | 1 |
| [`StatusAlliesOnBattleStart`](#object-statusalliesonbattlestart) | Object || 9 ||
| [`TrinketPassiveMultiplierBonus`](./Enums.md) | Integer || 9 | 2 |
| [`BoostHeals`](./Enums.md) | Integer || 8 | 2 |
| [`ChanceToRevive`](Elite_Buffs.md#object-chancetorevive) | Integer / Object || 8 | 100 |
| [`PermanentMadness`](./Enums.md) | Integer | If set to 1, the Madness status is permanent and will never expire; can use an alias for the status. | 8 | 1 |
| [`StatusOnDie`](Cat_Mutations.md#object-statusondie) | Object | Defines statuses or effects that are applied when the unit dies. | 8 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 8 |
| [`AddElementsToBasicAttack`](./Enums.md) | Enum | Specifies the elemental damage type added to the unit's basic attack. | 7 | Holy |
| [`AddInitiative`](./Enums.md) | Integer | The amount to add to the unit's initiative score, affecting turn order. | 7 | -20 |
| [`AlphaTurns`](./Enums.md) | Integer | The number of additional alpha turns the unit receives at the start of combat. | 7 | -1 |
| [`Bleed`](./Enums.md) | Integer | The number of Bleed stacks applied, which deals bleeding damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 7 | 3 |
| [`BonusAbility`](./Enums.md) | Enum | Determines which additional ability is granted to the character (e.g., as a passive or keyword tooltip link). | 7 | neck_NukeBonus |
| [`BrittleDuringElement`](./Enums.md) | Enum || 7 | water |
| [`DebuffImmunity`](./Enums.md) | Integer | Grants immunity to debuffs (value likely toggle or tier). | 7 | 1 |
| [`DurabilityTransform`](#object-durabilitytransform) | Object || 7 ||
| [`ManaCostReduction`](./Enums.md) | Integer | The amount or percentage by which the mana cost of abilities is reduced. | 7 | -2 |
| [`OverrideBasicAttack`](./Enums.md) | Enum || 7 | IsaacBasicAttack |
| [`PassiveAtHealthThreshold`](#object-passiveathealththreshold) | Object || 7 ||
| [`PassiveAtStatThreshold`](#object-passiveatstatthreshold) | Object || 7 ||
| [`SetFragileImmune`](./Enums.md) | Variable || 7 ||
| [`SetSpellCosts`](./Enums.md) | Integer | Overrides all spell costs to a fixed value. | 7 | 0 |
| [`StatusOnEndMove`](Cat_Mutations.md#object-statusonendmove) | Object | Defines statuses or effects applied when the unit finishes moving. | 7 ||
| [`AddDamageToElementDamage`](Cat_Mutations.md#object-adddamagetoelementdamage) | Object | Adds extra damage to attacks that deal a specified element type. | 6 ||
| [`AmplifyStatus`](./Enums.md) | Enum || 6 | Poison |
| [`DelayedAutoRevive`](Characters_and_Bosses.md#object-delayedautorevive) | Object | Automatically revives the unit after a specified number of rounds with a given health percentage. | 6 ||
| [`DodgeChance_Status`](./Enums.md) | Integer | The percentage of dodge chance granted by this status effect. | 6 | 2 |
| [`ExtraWeaponAttacks`](./Enums.md) | Integer || 6 | 2 |
| [`IgnoreTiles`](./Enums.md) | Integer | If set to 1, the unit ignores tile effects while moving. | 6 | 1 |
| [`ItemAuxTransform`](#object-itemauxtransform) | Object || 6 ||
| [`PassiveWhenOnTile`](#object-passivewhenontile) | Object || 6 ||
| [`Poison`](./Enums.md) | Integer | The number of Poison stacks applied, which deals poison damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 6 | 2 |
| [`Quivered`](./Enums.md) | Array / Integer | The number of stacks of Quivered, which grants bonus attacks; can be an array [stacks, probability]. | 6 | [.10] |
| [`ReplaceBasicAttack`](./Enums.md) | Enum | Specifies the name of the ability that replaces the unit's basic attack. | 6 | BasicPoke |
| [`SetBrittleImmune`](./Enums.md) | Variable || 6 ||
| [`SpawnOnBattleStartRandomEmptyTile`](Cat_Mutations.md#object-spawnonbattlestartrandomemptytile) | Object | Spawns specified objects on random empty tiles at the start of battle. | 6 ||
| [`AddBonusMeleeRange`](./Enums.md) | Integer | The number of additional tiles of range added to melee attacks. | 5 | 1 |
| [`AddHiddenTag`](./Enums.md) | Enum | Adds a hidden tag to the unit for internal logic or quest tracking. | 5 | the_nuke_bearer |
| [`BackstabCritChance`](./Enums.md) | Number || 5 | .25 |
| [`Burn`](./Enums.md) | Integer | The number of Burn stacks applied, which deals fire damage over time; can be an integer, a variable X, or an array `[stacks, probability]` to specify chance of application. | 5 | 2 |
| [`ClassManaCostReduction`](Cat_Mutations.md#object-classmanacostreduction) | Object | Reduces the mana cost of abilities belonging to a specified class. | 5 ||
| [`CritsApplyStatus`](#object-critsapplystatus) | Object || 5 ||
| [`FaceShield`](./Enums.md) | Integer | A boolean flag (1 or 0) indicating whether the unit has a face shield that blocks specific effects. | 5 | 1 |
| [`HeadArmorPassiveMultiplierBonus`](./Enums.md) | Integer || 5 | 2 |
| [`InjuryImmunity`](./Enums.md) | Integer | The number of stacks of InjuryImmunity, granting immunity to receiving injuries (permanent wounds) for that many instances. | 5 | 1 |
| [`KnockbackImmunity`](./Enums.md) | Integer | If set to 1, the unit is immune to knockback effects. | 5 | 1 |
| [`SharkySmellsBlood`](./Enums.md) | Integer | If set to 1, enables blood-sensing behavior, often targeting wounded enemies. | 5 | 1 |
| [`SpellDamageUp`](./Enums.md) | Integer | The number of stacks of SpellDamageUp, increasing spell damage dealt by the unit. | 5 | 3 |
| [`StatusIfUnusedMovePoints`](Cat_Mutations.md#object-statusifunusedmovepoints) | Object | Defines statuses applied if the unit has leftover movement points at the end of its turn. | 5 ||
| [`StatusOnTurnEndIfDidntCastAbilityTypes`](#object-statusonturnendifdidntcastabilitytypes) | Object || 5 ||
| [`TransformItemOnElementInfluence`](#object-transformitemonelementinfluence) | Object || 5 ||
| [`TrinketActiveEffectsMultiplierBonus`](./Enums.md) | Integer || 5 | 2 |
| [`AddCritMultiplier`](./Enums.md) | Integer || 4 | 33 |
| [`AddKnockbackDamage`](./Enums.md) | Integer | The amount of additional damage dealt when the unit knocks back an enemy. | 4 | 1 |
| [`AddStatusToElementDamage`](#object-addstatustoelementdamage) | Object || 4 ||
| [`AddStatusToWeapons`](Characters_and_Bosses.md#object-addstatustoweapons) | Object | A dictionary of status effects to apply to the unit's weapon attacks. | 4 ||
| [`AddTemporaryEffectsToBasicAttack`](Cat_Mutations.md#object-addtemporaryeffectstobasicattack) | Object | Adds temporary statuses or effects to the unit's basic attack for the current turn. | 4 ||
| [`BoostWeaponDamage`](#object-boostweapondamage) | Object | Increases the damage dealt by the unit's weapon. | 4 ||
| [`BreakAtAux`](./Enums.md) | Integer || 4 | 0 |
| [`BuffImmunity`](#object-buffimmunity) | Object | If set to 1, the unit is immune to buffs. As an object, can exclude specific buffs. | 4 ||
| [`CatchProjectiles`](#object-catchprojectiles) | Object || 4 ||
| [`ChanceToBackflip`](Cat_Mutations.md#object-chancetobackflip) | Object | Defines the chance and ability used for the unit to backflip and dodge an incoming attack. | 4 ||
| [`ExtraStatusWhenDealingDamage`](#object-extrastatuswhendealingdamage) | Object || 4 ||
| [`FaceArmorPassiveMultiplierBonus`](./Enums.md) | Integer || 4 | 2 |
| [`FragileDuringElement`](./Enums.md) | Enum || 4 | water |
| [`FreezePiercing`](./Enums.md) | Integer || 4 | 1 |
| [`IncreaseExplosionDamage`](./Enums.md) | Integer || 4 | 2 |
| [`IncreaseExplosionSize`](./Enums.md) | Integer || 4 | 7 |
| [`LevelUpClassOverride`](./Enums.md) | Enum || 4 | Jester |
| [`MakeSpellsRequireCharge`](./Enums.md) | Integer || 4 | 1 |
| [`PassiveWhenAffectedByElement`](Cat_Mutations.md#object-passivewhenaffectedbyelement) | Object | Grants additional passive effects when the unit is under the effects of a specified element. | 4 ||
| [`PassiveWhenDead`](Characters_and_Bosses.md#object-passivewhendead) | Object | A set of passive effects that remain active after the unit's death. | 4 ||
| [`RandomSeededStatModifier`](./Enums.md) | Array || 4 | [2] |
| [`StatusAlliesOnDeath`](#object-statusalliesondeath) | Object || 4 ||
| [`StatusEveryXSpellCasts`](Cat_Mutations.md#object-statuseveryxspellcasts) | Object | Applies specified statuses after the unit casts a certain number of spells. | 4 ||
| [`StatusOnAllyCatDeath`](Cat_Mutations.md#object-statusonallycatdeath) | Object | Defines statuses applied when an ally cat dies. | 4 ||
| [`StatusOnCastSpell`](Cat_Mutations.md#object-statusoncastspell) | Object | Defines statuses applied when the unit casts a spell. | 4 ||
| [`StatusOnGainCoins`](Characters_and_Bosses.md#object-statusongaincoins) | Object | A dictionary of status effects applied when the unit collects coins. | 4 ||
| [`StatusOnPopCorpse`](#object-statusonpopcorpse) | Object || 4 ||
| [`StatusOnTakeHealthOrShieldDamage`](#object-statusontakehealthorshielddamage) | Object || 4 ||
| [`StatusRandomEnemiesOnBattleStart`](Events_and_Encounters.md#object-statusrandomenemiesonbattlestart) | Object || 4 ||
| [`AddEndOfCombatRegen`](./Enums.md) | Integer || 3 | 999999 |
| [`AddPassivesToCharmed`](#object-addpassivestocharmed) | Object || 3 ||
| [`AddStatusToSpells`](Characters_and_Bosses.md#object-addstatustospells) | Object | A dictionary of status effects to apply to the unit's spell attacks. | 3 ||
| [`AllStatsUpPerDisorder`](./Enums.md) | Integer || 3 | 1 |
| [`AmplifyKnockback`](./Enums.md) | Integer || 3 | 2 |
| [`ApplyStatusesToRandomEnemiesEachTurn`](#object-applystatusestorandomenemieseachturn) | Object || 3 ||
| [`AutoEquipConsumables`](./Enums.md) | Integer || 3 | 1 |
| [`BasicAttackCritChance`](./Enums.md) | Number || 3 | .1 |
| [`BoneArmorPassive`](./Enums.md) | Integer || 3 | 1 |
| [`BreakOnElement`](./Enums.md) | Enum || 3 | water |
| [`CantCatchDiseases`](./Enums.md) | Integer || 3 | 1 |
| [`CantSpreadDiseases`](./Enums.md) | Integer || 3 | 1 |
| [`ChanceToBlock`](./Enums.md) | Integer || 3 | 10 |
| [`ChanceToBlockAndCounter`](#object-chancetoblockandcounter) | Integer / Object || 3 | 25 |
| [`Confusion`](./Enums.md) | Integer | The number of turns of Confusion applied, or an array with duration and chance. | 3 | 2 |
| [`DropAsFamiliarOnArmorBreak`](./Enums.md) | Enum || 3 | FaceGrubFamiliar |
| [`ElementalManaCostReduction`](#object-elementalmanacostreduction) | Object || 3 ||
| [`ExtraBasicMoves_Status`](./Enums.md) | Integer | The number of extra basic moves the unit can perform each turn. Stacks for additional moves. | 3 | 1 |
| [`ExtraMovePoints`](./Enums.md) | Integer | Additional movement points granted each turn. | 3 | 1 |
| [`FlowersOnEndTurn`](./Enums.md) | Integer || 3 | 1 |
| [`IncreaseSpellRange`](./Enums.md) | Integer || 3 | 2 |
| [`KillsToMeat`](./Enums.md) | Enum || 3 | Food |
| [`LuckUp`](./Enums.md) | Integer | Specifies the number of Luck stacks applied, where positive values increase critical hit chance and loot quality and negative values decrease them. | 3 | 2 |
| [`MoveAndUseAbilityEachTurnBeginIfPossible`](./Enums.md) | Enum || 3 | face_EatNeverstone |
| [`MoveQuivered`](./Enums.md) | Integer | Specifies the number of bonus movement points granted; an array `[stacks, probability]` specifies the amount and its chance of application. | 3 | 2 |
| [`NeckArmorPassiveMultiplierBonus`](./Enums.md) | Integer || 3 | 1 |
| [`PassiveAfterXKills`](#object-passiveafterxkills) | Object || 3 ||
| [`RangedTrueShot`](./Enums.md) | Integer || 3 | 1 |
| [`ReplaceSpawnedObjects`](./Enums.md) | Array || 3 | [Poop] |
| [`RockyArmorPassive`](./Enums.md) | Integer || 3 | 1 |
| [`SetDefaultFacePassive`](./Enums.md) | Enum || 3 | euphoric |
| [`SpawnExtraThingsOnBattleStart`](Cat_Mutations.md#object-spawnextrathingsonbattlestart) | Object | Spawns specified objects, tiles, or traps at the start of battle. | 3 ||
| [`SpawnObjectOnPopCorpse`](#object-spawnobjectonpopcorpse) | Enum / Object || 3 | Coin |
| [`StackingFlowerTrail`](#object-stackingflowertrail) | Object || 3 ||
| [`StatusAfterCastSpell`](#object-statusaftercastspell) | Object || 3 ||
| [`StatusAllCharactersOnSpawn`](House_and_Environment.md#object-statusallcharactersonspawn) | Object | Applies the nested status effects to all characters when this object spawns. | 3 ||
| [`StatusOnBreakItem`](#object-statusonbreakitem) | Object || 3 ||
| [`StatusOnEatFood`](Cat_Mutations.md#object-statusoneatfood) | Object | Defines statuses applied when the unit consumes food. | 3 ||
| [`TrueShot`](./Enums.md) | Integer || 3 | 1 |
| [`AddSelfStatusToWeapons`](#object-addselfstatustoweapons) | Object || 2 ||
| [`AddStatusToKnockbackDamage`](#object-addstatustoknockbackdamage) | Object || 2 ||
| [`AllyDamageReduction`](./Enums.md) | Integer || 2 | 0 |
| [`ArmorBreakOnHit`](#object-armorbreakonhit) | Object || 2 ||
| [`BouncyProjectiles`](#object-bouncyprojectiles) | Object || 2 ||
| [`BreakWhenNoShield`](./Enums.md) | Integer || 2 | 1 |
| [`CanLevelUpWhenDead`](./Enums.md) | Integer || 2 | 1 |
| [`CanRemoveCursedItems`](./Enums.md) | Integer | If set to 1, the unit can remove cursed items from their inventory. | 2 | 1 |
| [`CapMovementAbilityRange`](./Enums.md) | Integer || 2 | 1 |
| [`ConsumableEffectsMultiplierBonus`](./Enums.md) | Integer || 2 | 1 |
| [`CopyPassiveSlot`](./Enums.md) | Integer || 2 | 0 |
| [`CreateGlobalModifiers`](Abilities_and_Spells.md#object-createglobalmodifiers) | Object | An object containing global modifier effects to apply after the time delay. | 2 ||
| [`DisableAbilities`](./Enums.md) | Enum || 2 | all_items |
| [`DoubleCastWeapons`](./Enums.md) | Integer || 2 | 1 |
| [`Eternal`](#object-eternal) | Object || 2 ||
| [`FindExtraItemFromPoolOnBattleEnd`](./Enums.md) | Enum | The loot pool from which to grant an extra item at battle end. | 2 | combat_reward_easy |
| [`FlyDamageIncrease`](#object-flydamageincrease) | Object || 2 ||
| [`GainExtraShield`](./Enums.md) | Integer || 2 | 4 |
| [`HPGainBlock`](./Enums.md) | Integer || 2 | 1 |
| [`LeaveBehindOnceEachMove`](./Enums.md) | Enum || 2 | Scrap |
| [`MoveSpeedMultiplier`](./Enums.md) | Number || 2 | .5 |
| [`PassiveIfWeaponIsUsable`](#object-passiveifweaponisusable) | Object || 2 ||
| [`PassiveWhileInMonkMeleeStance`](#object-passivewhileinmonkmeleestance) | Object || 2 ||
| [`PoopWhenHit`](#object-poopwhenhit) | Object | Specifies the object dropped when the unit is hit, optionally with a chance. | 2 ||
| [`RefreshEquipmentAbilityOnElement`](#object-refreshequipmentabilityonelement) | Object || 2 ||
| [`RemoveLineOfSightRestrictions`](./Enums.md) | Integer || 2 | 1 |
| [`ScaledStatusOnSpendMana`](#object-scaledstatusonspendmana) | Object || 2 ||
| [`SpawnItemLinkedFamiliar`](#object-spawnitemlinkedfamiliar) | Object || 2 ||
| [`SpawnNearEnemies`](./Enums.md) | Integer || 2 | 1 |
| [`StatusAfterXTurns`](Characters_and_Bosses.md#object-statusafterxturns) | Object | Defines a status effect that is applied after a certain number of turns, with optional forced ability use. | 2 ||
| [`StatusEachTurnEndForEachTurn`](Characters_and_Bosses.md#object-statuseachturnendforeachturn) | Object | Specifies an object defining status effects applied at end of each turn for each turn. | 2 ||
| [`StatusIfUnusedActPoints`](#object-statusifunusedactpoints) | Object || 2 ||
| [`StatusOnBackstab`](#object-statusonbackstab) | Object || 2 ||
| [`StatusOnCollectPickup`](#object-statusoncollectpickup) | Object || 2 ||
| [`StatusOnHealed`](#object-statusonhealed) | Object || 2 ||
| [`StatusOnPickupCoins`](#object-statusonpickupcoins) | Object || 2 ||
| [`StatusOnUseBasicAttack`](#object-statusonusebasicattack) | Object || 2 ||
| [`StatusWhenAllySpendsMana`](#object-statuswhenallyspendsmana) | Object || 2 ||
| [`TauntAlways`](./Enums.md) | Integer || 2 | 1 |
| [`Uncontrollable`](./Enums.md) | Integer || 2 | 1 |
| [`WeaponDamageMultiplierBonus`](./Enums.md) | Integer || 2 | 1 |
| [`AIControlNextTurn`](#object-aicontrolnextturn) | Object || 1 ||
| [`AOEBonus`](./Enums.md) | Integer || 1 | 1 |
| [`AbilityOnRoundEndOnce`](#object-abilityonroundendonce) | Object || 1 ||
| [`AddAdvantageToEvent`](#object-addadvantagetoevent) | Object || 1 ||
| [`AddStatusToBackstabs`](#object-addstatustobackstabs) | Object || 1 ||
| [`AllSpellsCostCharge`](./Enums.md) | Integer || 1 | 1 |
| [`AllUnitsExplodeOnDeath`](./Enums.md) | Integer || 1 | 5 |
| [`AlliesScrambleSpellAfterCast`](./Enums.md) | Integer || 1 | 1 |
| [`AlluringDoodieEater`](#object-alluringdoodieeater) | Object || 1 ||
| [`AllyDodgeChanceAura`](#object-allydodgechanceaura) | Object || 1 ||
| [`AlphaAllStatsUp`](./Enums.md) | Integer || 1 | 1 |
| [`AlphaCat`](./Enums.md) | Integer | The number of stacks of the AlphaCat status effect. | 1 | 1 |
| [`AlwaysChosenForLevelUp`](./Enums.md) | Integer || 1 | 1 |
| [`BackflipWhenTargeted`](Abilities_and_Spells.md#object-backflipwhentargeted) | Enum / Object | The number of stacks of BackflipWhenTargeted or an object defining the dodge ability; causes the unit to perform a backflip dodge when targeted. | 1 | X |
| [`BalanceStats`](./Enums.md) | Integer || 1 | 1 |
| [`BasicAttackCantMiss`](./Enums.md) | Integer | If set to 1, the unit's basic attacks cannot miss. | 1 | 1 |
| [`Blind`](./Enums.md) | Integer | The number of stacks of Blind to apply, reducing accuracy; can be an array `[stacks, probability]` for a chance-based application. | 1 | -1 |
| [`BlockDamageUnderThreshold`](./Enums.md) | Integer || 1 | 1 |
| [`BlockNegativeStatus`](./Enums.md) | Integer || 1 | 30 |
| [`BoostReceivedHealing`](./Enums.md) | Integer || 1 | 2 |
| [`CapBasicAttackDamage`](./Enums.md) | Integer || 1 | 1 |
| [`CatPartsSizeScale`](#object-catpartssizescale) | Object || 1 ||
| [`ChanceToAmbush`](./Enums.md) | Integer || 1 | 25 |
| [`ChanceToForceEvent`](#object-chancetoforceevent) | Object || 1 ||
| [`Charge`](./Enums.md) | Integer | The number of stacks of Charge, which makes the caster gain 1 Mana per stack at the start of its next turn. | 1 | 2 |
| [`CharismaIsMaxStat`](./Enums.md) | Integer || 1 | 1 |
| [`CharmImmunity`](./Enums.md) | Integer || 1 | 1 |
| [`ConvertDamageToScaledStatus`](#object-convertdamagetoscaledstatus) | Object || 1 ||
| [`CounterNextAttacks`](./Enums.md) | Integer || 1 | 2 |
| [`DisablePassiveSlot`](./Enums.md) | Integer || 1 | 0 |
| [`DoubleCastSpellIfManaCostUnderThreshold`](./Enums.md) | Integer || 1 | 3 |
| [`DoubleCastTaggedSpells`](./Enums.md) | Enum || 1 | musical |
| [`DoubleReceivedNegativeStatus`](./Enums.md) | Integer || 1 | 1 |
| [`DoubleReceivedPositiveStatus`](./Enums.md) | Integer || 1 | 1 |
| [`DropAsFamiliarOnTookDamage`](./Enums.md) | Enum || 1 | PhantomMaskRock |
| [`DropSoulJarOnDeath`](./Enums.md) | Enum || 1 | SoulJar_Full |
| [`ExcludeFromEvents`](./Enums.md) | Enum || 1 | Tragedy |
| [`ExplosionImmunity`](./Enums.md) | Integer || 1 | 1 |
| [`ExtraBasicAttacks_Status`](./Enums.md) | Integer | The number of extra basic attacks the unit can perform each turn. Stacks for additional attacks. | 1 | 1 |
| [`ExtraTrinketUses`](./Enums.md) | Integer || 1 | 10 |
| [`FrankBolts`](./Enums.md) | Integer || 1 | 1 |
| [`GlobalMeleeRevengeDamage`](#object-globalmeleerevengedamage) | Object || 1 ||
| [`HideSomeHudStuff`](./Enums.md) | Integer || 1 | 1 |
| [`JesterLevelUpRerolls`](./Enums.md) | Integer || 1 | 1 |
| [`Lifesteal`](./Enums.md) | Integer | The number of stacks of Lifesteal, converting a percentage of damage dealt into healing for the attacker. | 1 | 1 |
| [`MakeBasicAttackPull`](./Enums.md) | Integer | If set to 1, the unit's basic attacks pull the target closer. | 1 | 1 |
| [`ModelingClayPassive`](./Enums.md) | Integer || 1 | 1 |
| [`MultiplyCoinsOnBattleStart`](./Enums.md) | Integer || 1 | 2 |
| [`MultiplyReceivedHealing`](./Enums.md) | Integer || 1 | 2 |
| [`ObjectDetector`](#object-objectdetector) | Object || 1 ||
| [`PassiveIfStrAuxEquals`](#object-passiveifstrauxequals) | Object || 1 ||
| [`PassiveWhileHasDurability`](#object-passivewhilehasdurability) | Object || 1 ||
| [`PassiveWhileShielded`](#object-passivewhileshielded) | Object || 1 ||
| [`PhysicalAttacksMiss`](./Enums.md) | Integer || 1 | 1 |
| [`PreventSpecificInjury`](./Enums.md) | Enum || 1 | int |
| [`ReclaimItemOnBreak`](./Enums.md) | Integer || 1 | 1 |
| [`ReduceManaCost`](./Enums.md) | Integer | The number by which mana cost of abilities is reduced, up to a minimum of zero. | 1 | 2 |
| [`ReduceSpellCostsPerDisorder`](./Enums.md) | Integer || 1 | 1 |
| [`ReduceSpellCostsPerParasite`](./Enums.md) | Integer || 1 | 1 |
| [`ReplaceBlankTilesOnBattleStart`](./Enums.md) | Enum || 1 | GlassTile |
| [`RerollItemsOnBattleEnd`](./Enums.md) | Integer || 1 | 1 |
| [`ScaldingOrbMoonBossOneShot`](#object-scaldingorbmoonbossoneshot) | Object || 1 ||
| [`ScaledStatusAlliesOnSpendMana`](#object-scaledstatusalliesonspendmana) | Object || 1 ||
| [`ScaledStatusOnHolyShieldBlock`](#object-scaledstatusonholyshieldblock) | Object || 1 ||
| [`SetFaction`](./Enums.md) | Enum || 1 | enemies |
| [`SpawnCatCloneOnCorpsePopped`](./Enums.md) | Integer || 1 | 1 |
| [`SpawnOnDowned`](./Enums.md) | Enum | Specifies the entity (e.g., CharmedSpookie) to spawn when this unit is downed. | 1 | CharmedSpookie |
| [`SpawnRandomPickupsOnTaggedUnitKilled`](#object-spawnrandompickupsontaggedunitkilled) | Object || 1 ||
| [`StatDependentPassive`](#object-statdependentpassive) | Object || 1 ||
| [`StatusAdjacentOnTheirTurnEnd`](#object-statusadjacentontheirturnend) | Object || 1 ||
| [`StatusAlliesEachTurn`](#object-statusallieseachturn) | Object || 1 ||
| [`StatusOnDodge`](#object-statusondodge) | Object || 1 ||
| [`StatusOnEnemyDeath`](#object-statusonenemydeath) | Object || 1 ||
| [`StatusOnFallAsleep`](#object-statusonfallasleep) | Object || 1 ||
| [`StatusOnFullMana`](#object-statusonfullmana) | Object || 1 ||
| [`StevenBolts`](./Enums.md) | Integer || 1 | 1 |
| [`StripKnockback`](./Enums.md) | Integer || 1 | 1 |
| [`TintItem`](#object-tintitem) | Object || 1 ||
| [`TunnelVision`](#object-tunnelvision) | Object || 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 205 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 56 |
| [`Bleed`](./Enums.md) | Integer | The number of Bleed stacks applied, which deals bleeding damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 30 | 3 |
| [`Poison`](./Enums.md) | Integer | The number of Poison stacks applied, which deals poison damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 29 | 2 |
| [`Knockback`](./Enums.md) | Integer | The number of tiles the target is knocked back. | 24 | 2 |
| [`Burn`](./Enums.md) | Integer | The number of Burn stacks applied, which deals fire damage over time; can be an integer, a variable X, or an array `[stacks, probability]` to specify chance of application. | 16 | 2 |
| [`Fear`](./Enums.md) | Array / Integer | The number of Fear stacks applied, which reduces the target's accuracy and may cause it to flee; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 13 | [.15] |
| [`Bruise`](./Enums.md) | Integer | The number of Bruise stacks applied, or an array with duration and chance. | 12 | 2 |
| [`ChangeTile`](./Enums.md) | Enum | Specifies the tile type to change the target's tile into (e.g., BrambleTile, LavaTile). | 10 | GlassTile |
| [`Slow`](./Enums.md) | Integer | The number of turns of Slow applied, or an array with duration and chance. | 10 | 1 |
| [`Stun`](./Enums.md) | Array | The number of Stun stacks applied, which prevents the target from taking actions; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 8 | [.1] |
| [`Confusion`](./Enums.md) | Integer | The number of turns of Confusion applied, or an array with duration and chance. | 7 | 2 |
| [`Weakness`](./Enums.md) | Integer | The number of Weakness stacks applied, which increases damage taken by the target; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 7 | 3 |
| [`Leech`](./Enums.md) | Integer | The amount of health stolen per hit as a percentage of damage dealt. | 5 | 1 |
| [`Rot`](./Enums.md) | Integer | The number of stacks of Rot, causing damage over time and potentially spawning a fly on death; can be an array `[stacks, probability]`. | 5 | 1 |
| [`DamageOrHealConditionally`](./Enums.md) | Integer | If set to 1, the status group effect conditionally deals damage or heals based on target. | 4 | 1 |
| [`Freeze`](./Enums.md) | Array / Integer | The number of stacks of Freeze, immobilizing the unit for that many turns; can be an array `[stacks, probability]`. | 4 | [.1] |
| [`Leeches`](./Enums.md) | Integer | The number of Leech stacks applied, healing the attacker. | 4 | 1 |
| [`SoulLink`](./Enums.md) | Integer | The number of turns the linked status lasts, sharing damage between linked units. | 4 | 1 |
| [`Tangled`](./Enums.md) | Array | The number of turns the target is unable to move, with optional [stacks, probability] format. | 4 | [.05] |
| [`Conditional_GoodRoll`](Abilities_and_Spells.md#object-conditional_goodroll) | Object | Defines a random roll with odds; if successful, the specified effects are applied. | 3 ||
| [`MagicWeakness`](./Enums.md) | Integer | The number of stacks of MagicWeakness, increasing incoming magic damage; can be an array `[stacks, probability]`. | 3 | 1 |
| [`ApplyToSource`](Abilities_and_Spells.md#object-applytosource) | Object | An object containing status effects or modifiers applied to the source (attacker) of the triggering condition rather than the target. | 2 ||
| [`Blind`](./Enums.md) | Integer | The number of stacks of Blind to apply, reducing accuracy; can be an array `[stacks, probability]` for a chance-based application. | 2 | -1 |
| [`KnockOutCoin`](./Enums.md) | Integer | Either an integer for guaranteed stacks or an object with `stacks` and `chance` for a probability-based knock-out effect. | 2 | 1 |
| [`ManaLeeches`](./Enums.md) | Integer | The number of mana leech stacks that drain mana on hit. | 2 | 1 |
| [`OverrideChainKnockback`](./Enums.md) | Integer | The number of tiles to override the default chain knockback distance. | 2 | 0 |
| [`SpiderInfested`](./Enums.md) | Integer | The number of turns the target is infested with spiders, taking damage over time. | 2 | 1 |
| [`ForceUseAbilityOnTarget`](Engine_StatusAndPassiveKeys.md#object-forceuseabilityontarget) | Object || 1 ||
| [`KnockUpAndAway`](Abilities_and_Spells.md#object-knockupandaway) | Object | Defines a knockback that launches the target up and away, with optional distance and stacks. | 1 ||
| [`Marked`](./Enums.md) | Integer | The number of Marked stacks applied, which increases damage taken from all sources; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | 1 |
| [`PullSourceToTarget`](./Enums.md) | Integer | If 1, pulls the source (attacker) to the target's adjacent tile after the attack. | 1 | 1 |

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
| `odds` | Number | The probability (0.0 to 1.0) of triggering the 'good roll' success state. | 37 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 37 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 28 ||
| [`Freeze`](./Enums.md) | Array / Integer | The number of stacks of Freeze, immobilizing the unit for that many turns; can be an array `[stacks, probability]`. | 6 | [.1] |
| [`FindItemFromPool`](./Enums.md) | Enum | Determines the item pool name from which a random item is granted to the source. | 5 | consumables |
| [`ForceUseAbility_NonStack`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'ForceUseAbility_NonStack' effect/state. | 4 ||
| [`ForceUseAbility`](./Enums.md) | Enum | Determines which ability the target is forced to cast immediately, ignoring normal costs and cooldowns. | 3 | tk_SuckStone |
| [`RandomMutation`](./Enums.md) | Integer | The number of random mutations to apply. | 3 | 1 |
| `DestroyTrinket` | `Number` | Applies or references the 'DestroyTrinket' effect/state. | 1 ||

</details>

---

### Object: `effects`
### Object: `effects`

**Definition:** Non-damaging status applications and logic triggers executed on impact.  
**Total Count:** 35


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DoDamage`](./Items_and_Equipment.md#context-dodamage), [`MeleeRevengeDamage`](./Items_and_Equipment.md#context-meleerevengedamage), [`RevengeDamage`](./Items_and_Equipment.md#context-revengedamage), [`damage_instance`](./Items_and_Equipment.md#context-damage_instance)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1695 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 750 ||
| [`Stun`](./Enums.md) | Array | The number of Stun stacks applied, which prevents the target from taking actions; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 98 | [.1] |
| [`Burn`](./Enums.md) | Integer | The number of Burn stacks applied, which deals fire damage over time; can be an integer, a variable X, or an array `[stacks, probability]` to specify chance of application. | 85 | 2 |
| [`Bruise`](./Enums.md) | Integer | The number of Bruise stacks applied, or an array with duration and chance. | 79 | 2 |
| [`Poison`](./Enums.md) | Integer | The number of Poison stacks applied, which deals poison damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 67 | 2 |
| [`Confusion`](./Enums.md) | Integer | The number of turns of Confusion applied, or an array with duration and chance. | 37 | 2 |
| [`VisualFXTile`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'VisualFXTile' effect/state. | 34 ||
| [`Fear`](./Enums.md) | Array / Integer | The number of Fear stacks applied, which reduces the target's accuracy and may cause it to flee; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 31 | [.15] |
| [`Slow`](./Enums.md) | Integer | The number of turns of Slow applied, or an array with duration and chance. | 29 | 1 |
| [`BounceObject`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Spawns a physics object that visually bounces off the target. | 26 ||
| [`Blind`](./Enums.md) | Integer | The number of stacks of Blind to apply, reducing accuracy; can be an array `[stacks, probability]` for a chance-based application. | 24 | -1 |
| [`Immobile`](./Enums.md) | Integer | The number of turns of Immobile applied, or an array with duration and chance. | 24 | 1 |
| [`Freeze`](./Enums.md) | Array / Integer | The number of stacks of Freeze, immobilizing the unit for that many turns; can be an array `[stacks, probability]`. | 19 | [.1] |
| [`Conditional_GoodRoll`](Abilities_and_Spells.md#object-conditional_goodroll) | Object | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 14 ||
| [`Cleave`](./Enums.md) | Integer | If an integer, the number of cleave hits; if an object, may contain a chance for cleave. | 12 | 1 |
| [`VisualFX`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'VisualFX' effect/state. | 10 ||
| [`Grappled`](./Enums.md) | Array | The number of turns the target is grappled, preventing movement and actions. | 8 | [.50] |
| `DestroyTrinket` | Integer | Applies or references the 'DestroyTrinket' effect/state. | 3 ||

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
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 70 ||
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 47 ||
| `knockback` | Enum / Integer | The number of tiles to push the target away from the attacker; can be negative to pull the target closer, or 'str' to scale with the attacker's strength stat. | 24 ||
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | The base damage properties of an attack. | 22 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 52 ||
| `even_if_dead` | Boolean | If true, triggers the effect even if the character died during the battle. | 25 ||
| [`RandomMutation`](./Enums.md) | Integer | The number of random mutations to apply. | 9 | 1 |
| [`FindItemFromPool`](./Enums.md) | Enum | Determines the item pool name from which a random item is granted to the source. | 8 | consumables |
| [`RandomPermanentStat`](./Enums.md) | Integer | The amount of random permanent stat change applied, positive or negative. | 8 | 2 |
| [`Conditional_GoodRoll`](Abilities_and_Spells.md#object-conditional_goodroll) | Object | Defines a random roll with odds; if successful, the specified effects are applied. | 6 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |
| [`PermanentIntelligence`](./Enums.md) | Integer | The number of permanent intelligence stat points added or subtracted. | 3 | -1 |
| [`GainCoins`](./Enums.md) | Array / Integer | The number of coins gained or lost; can be a fixed integer, a range `[min, max]`, or a negative value to deduct coins. | 2 | [3] |
| [`PermanentConstitution`](./Enums.md) | Integer | The amount of permanent Constitution (max HP) added. | 2 | 2 |
| [`RepairTrinket`](./Enums.md) | Integer | The amount of durability restored to the trinket item slot. | 2 | 99 |
| [`SetItemAux`](Engine_StatusAndPassiveKeys.md#object-setitemaux) | Object | Sets the auxiliary value of a specific item slot (e.g., face, trinket, head) to a calculated value. | 2 ||
| [`Conditional_Corpse`](Abilities_and_Spells.md#object-conditional_corpse) | Object || 1 ||
| [`Conditional_Shielded`](Abilities_and_Spells.md#object-conditional_shielded) | Object || 1 ||
| [`RepairAll`](./Enums.md) | Integer | The amount of condition restored to all equipment. | 1 | 1 |
| [`RepairWeapon`](./Enums.md) | Array / Integer | The number of stacks of RepairWeapon applied (or an array [stacks, probability] for random application). | 1 | [.25] |
| [`TransformWeapon`](Abilities_and_Spells.md#object-transformweapon) | Object | An object specifying a weapon transformation from one ID to another. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 55 ||
| [`ForceUseAbility`](./Enums.md) | Enum | Determines which ability the target is forced to cast immediately, ignoring normal costs and cooldowns. | 12 | tk_SuckStone |
| [`Shield`](./Enums.md) | Enum / Integer | Specifies the number of Shield stacks applied, where each stack reduces incoming damage by a flat amount. | 5 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 5 |
| [`PartialCleanse`](./Enums.md) | Integer | The number of status effects removed from the target (partial cleanse). | 4 | 1 |
| [`Conditional_GoodRoll`](Abilities_and_Spells.md#object-conditional_goodroll) | Object | Defines a random roll with odds; if successful, the specified effects are applied. | 2 ||
| [`ImmediateUseAbility`](Engine_StatusAndPassiveKeys.md#object-immediateuseability) | Enum / Object | Forces the unit to immediately use the specified ability, even if stunned. | 2 | head_MagnetoAttract |
| [`SpawnCoinAnywhere`](./Enums.md) | Integer | If integer, the number of coins spawned; if array, [stacks, probability] of spawning a coin anywhere on the map. | 2 | 1 |
| [`AddWeaponAux`](./Enums.md) | Integer | Adds to the weapon's auxiliary value, supporting integer or formula input. | 1 | 1 |
| [`Burn`](./Enums.md) | Integer | The number of Burn stacks applied, which deals fire damage over time; can be an integer, a variable X, or an array `[stacks, probability]` to specify chance of application. | 1 | 2 |
| [`Conditional_ManaThreshold`](Engine_LogicKeys.md#conditional_manathreshold) | Object || 1 ||
| [`ConstitutionUp`](./Enums.md) | Integer | The amount of Constitution (HP) increase, or an array with duration and chance. | 1 | 1 |
| [`PreEmptiveCounterNextAttacks`](./Enums.md) | Integer | The number of stacks of PreEmptiveCounterNextAttacks applied, allowing a counterattack before the next incoming attacks. | 1 | 1 |
| [`Stealth`](./Enums.md) | Array | The number of turns the unit is invisible, or [stacks, probability] of gaining stealth. | 1 | [.1] |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 20 ||
| [`GainCoinsRange`](Abilities_and_Spells.md#object-gaincoinsrange) | Object | An object with min and max values defining the range of coins gained. | 5 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |
| [`Bruise`](./Enums.md) | Integer | The number of Bruise stacks applied, or an array with duration and chance. | 3 | 2 |
| [`ChangeTilesUnder`](./Enums.md) | Enum | Determines which tile type (e.g., GlassTile, DirtTile) replaces the tiles beneath the target. | 3 | WaterTile |
| [`FindItemFromPool`](./Enums.md) | Enum | Determines the item pool name from which a random item is granted to the source. | 3 | consumables |
| [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 3 | 2 |
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of health regeneration (HealthRegen) granted by this damage instance. | 3 | 2 |
| [`PermanentConstitution`](./Enums.md) | Integer | The amount of permanent Constitution (max HP) added. | 3 | 2 |
| [`ApplyToRandomPartyMemberIfPossible`](Abilities_and_Spells.md#object-applytorandompartymemberifpossible) | Object | An object containing effects to apply to a random party member if one is available. | 1 ||
| [`ConstitutionUp`](./Enums.md) | Integer | The amount of Constitution (HP) increase, or an array with duration and chance. | 1 | 1 |
| [`DexterityUp`](./Enums.md) | Integer | The amount of Dexterity stat increased or decreased (negative values lower the stat); can be a formula or fixed integer. | 1 | 1 |
| [`FindItem`](./Enums.md) | Enum | Determines which specific item (e.g., Molars, Pearl) is granted to the source. | 1 | Pearl |
| [`GainDisorder`](./Enums.md) | Enum || 1 | Psychosis |
| [`IntelligenceUp`](./Enums.md) | Integer | The amount of intelligence increase, which can be a fixed integer or a mathematical expression. | 1 | 2 |
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object | An object or entity name that spawns upon hitting a character, with optional stacks and chance. | 1 | BestBud |
| [`StrengthUp`](./Enums.md) | Integer | Specifies the number of Strength stacks applied, where positive values increase melee damage and negative values decrease it. | 1 | 1 |

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
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the template identifier of the entity to spawn, referencing a predefined character or object in the game data. | 38 ||
| [`number`](./Arrays.md#array-number) | Array / Integer || 29 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 34 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 6 |
| [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 5 | 2 |
| [`Conditional_GoodRoll`](Abilities_and_Spells.md#object-conditional_goodroll) | Object | Defines a random roll with odds; if successful, the specified effects are applied. | 4 ||
| [`EquipPermanentItem`](./Enums.md) | Enum | Determines which permanent item (e.g., a body part or bone club) is equipped to the source. | 3 | BoneClub |
| [`StrengthUp`](./Enums.md) | Integer | Specifies the number of Strength stacks applied, where positive values increase melee damage and negative values decrease it. | 3 | 1 |
| [`LuckUp`](./Enums.md) | Integer | Specifies the number of Luck stacks applied, where positive values increase critical hit chance and loot quality and negative values decrease them. | 2 | 2 |
| [`SpeedUp`](./Enums.md) | Integer | Specifies the number of Speed stacks applied, where each stack modifies the unit's turn order and dodge chance. | 2 | 2 |
| [`BrittleCharismaUp`](./Enums.md) | Integer || 1 | 2 |
| [`BrittleConstitutionUp`](./Enums.md) | Integer || 1 | 2 |
| [`BrittleDexterityUp`](./Enums.md) | Integer || 1 | 2 |
| [`BrittleIntelligenceUp`](./Enums.md) | Integer || 1 | 2 |
| [`BrittleLuckUp`](./Enums.md) | Integer || 1 | 2 |
| [`BrittleSpeedUp`](./Enums.md) | Integer || 1 | 2 |
| [`BrittleStrengthUp`](./Enums.md) | Integer || 1 | 2 |
| [`CharismaUp`](./Enums.md) | Integer | The amount of Charisma stat increased or decreased (negative values lower the stat); can be a formula or fixed integer. | 1 | 1 |
| [`ConstitutionUp`](./Enums.md) | Integer | The amount of Constitution (HP) increase, or an array with duration and chance. | 1 | 1 |
| [`DexterityUp`](./Enums.md) | Integer | The amount of Dexterity stat increased or decreased (negative values lower the stat); can be a formula or fixed integer. | 1 | 1 |
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of health regeneration (HealthRegen) granted by this damage instance. | 1 | 2 |
| [`IntelligenceUp`](./Enums.md) | Integer | The amount of intelligence increase, which can be a fixed integer or a mathematical expression. | 1 | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 38 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 14 |
| [`Charge`](./Enums.md) | Integer | The number of stacks of Charge, which makes the caster gain 1 Mana per stack at the start of its next turn. | 8 | 2 |
| [`StrengthUp`](./Enums.md) | Integer | Specifies the number of Strength stacks applied, where positive values increase melee damage and negative values decrease it. | 4 | 1 |
| [`DamageUp`](./Enums.md) | Integer | The amount of damage increase, or a string formula for dynamic calculation. | 3 | 2 |
| [`Temporary`](Abilities_and_Spells.md#object-temporary) | Object | An object that defines a temporary status effect with duration and expiration conditions. | 3 ||
| [`Thorns`](./Enums.md) | Integer | The number of Thorns stacks applied, which deals damage back to melee attackers. | 3 | 2 |
| [`Conditional_HasStatus`](Abilities_and_Spells.md#object-conditional_hasstatus) | Object || 2 ||
| [`Bleed`](./Enums.md) | Integer | The number of Bleed stacks applied, which deals bleeding damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | 3 |
| [`Conditional_HealthThreshold`](Abilities_and_Spells.md#object-conditional_healththreshold) | Object | A block containing effects that trigger only if the target's health is below a certain threshold. | 1 ||
| [`DivineShield`](./Enums.md) | Array / Integer | The number of charges of Divine Shield applied, which blocks the next instances of damage entirely; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | [.5] |
| [`DodgeChance_Status`](./Enums.md) | Integer | The percentage of dodge chance granted by this status effect. | 1 | 2 |
| [`RemoveStatus`](./Enums.md) | Enum | Specifies the name of a status effect to remove from the target. | 1 | AlphaCat |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 9 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 7 |
| [`Craft`](Abilities_and_Spells.md#object-craft) | Object | An object defining a crafting action, including the item pool and target slot. | 3 ||
| [`SafeDie`](./Enums.md) | Integer | If 1, prevents death once per battle, leaving the unit at 1 HP instead. | 2 | 1 |
| [`Brace`](./Enums.md) | Enum / Integer | The amount of flat damage reduction applied to the source. | 1 | 2 |
| [`DestroyEquipmentAndAttachParasite`](Abilities_and_Spells.md#object-destroyequipmentandattachparasite) | Object | An object that destroys a piece of equipment and attaches a parasite from a specified pool, with optional chance. | 1 ||
| [`FindItemFromPool`](./Enums.md) | Enum | Determines the item pool name from which a random item is granted to the source. | 1 | consumables |
| [`ForceUseAbility`](./Enums.md) | Enum | Determines which ability the target is forced to cast immediately, ignoring normal costs and cooldowns. | 1 | tk_SuckStone |
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object | An object or entity name that spawns upon hitting a character, with optional stacks and chance. | 1 | BestBud |
| [`RandomMagicMissile`](./Enums.md) | Integer | The number of random magic missiles fired, each dealing independent damage; can also be an object with custom tooltip data. | 1 | 2 |
| [`ReviveNextRound`](Abilities_and_Spells.md#object-revivenextround) | Object | The number of stacks of ReviveNextRound or an object defining revival properties; causes the unit to revive with specified health, shields, or buffs at the start of the next round. | 1 ||
| [`SetHealth`](./Enums.md) | Integer || 1 | 50 |
| [`StealthUntilBasicAttack`](./Enums.md) | Integer | The number of stacks of stealth that persist until the unit makes a basic attack. | 1 | 1 |

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
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the template identifier of the entity to spawn, referencing a predefined character or object in the game data. | 38 ||
| `good` | Boolean | The outcome block triggered on successful condition when spawning something on damage. | 20 ||
| [`chance`](./Enums.md#enum-chance) | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 12 ||
| `spawn_on_death_hit` | Boolean | If true, the spawn occurs specifically when the damaging hit kills the target. | 10 ||
| `number` | Array / Integer || 1 ||

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
| [`object`](./Arrays.md#array-object) | Array / Enum | Specifies the template identifier of the entity to spawn, referencing a predefined character or object in the game data. | 22 ||
| [`chance`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Probability (0.0 to 1.0 or percentage) of this occurring. | 20 ||
| [`stack_key`](./Enums.md#enum-stack_key) | Enum || 5 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 24 ||
| [`Conditional_BadRoll`](Abilities_and_Spells.md#object-conditional_badroll) | Object | Defines a conditional effect that triggers on a bad roll with a given probability, optionally with an else clause. | 5 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| [`SpeedUp`](./Enums.md) | Integer | Specifies the number of Speed stacks applied, where each stack modifies the unit's turn order and dodge chance. | 2 | 2 |
| [`BlessingOfPeace`](./Enums.md) | Integer | The number of BlessingOfPeace stacks applied, which reduces damage taken from enemies. | 1 | 1 |
| [`Burn`](./Enums.md) | Integer | The number of Burn stacks applied, which deals fire damage over time; can be an integer, a variable X, or an array `[stacks, probability]` to specify chance of application. | 1 | 2 |
| [`DestroyTrinket`](./Enums.md) | Integer || 1 | 1 |
| [`DoubleCastSpellThisTurn`](./Enums.md) | Integer | If set to 1, allows the unit to cast spells twice this turn. | 1 | 1 |
| [`DrinkWater`](./Enums.md) | Integer | The number of stacks of the Drink Water status effect applied, which may trigger water-related behaviors or effects. | 1 | 1 |
| [`ManaGainRange`](Engine_StatusAndPassiveKeys.md#object-managainrange) | Object || 1 ||
| [`Revive`](./Enums.md) | Integer | The percentage or flat amount of HP restored when reviving a dead ally. | 1 | 1 |
| [`Temporary`](Abilities_and_Spells.md#object-temporary) | Object | An object that defines a temporary status effect with duration and expiration conditions. | 1 ||
| [`UseAbility`](./Enums.md) | Enum | Specifies the ability name the unit will use at the end of each round. | 1 | neck_DarkFriend |
| [`Wet`](./Enums.md) | Integer | The number of Wet status stacks applied, affecting elemental reactions. | 1 | 1 |

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
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 31 ||
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 29 ||
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | The base damage properties of an attack. | 8 ||
| [`elements`](./Arrays.md#array-elements) | Array | A list of elemental types applied to the damage instance, such as Heat or Fire, used for weaknesses, resistances, and visual effects. | 2 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 11 ||
| [`RandomMagicMissile`](./Enums.md) | Integer | The number of random magic missiles fired, each dealing independent damage; can also be an object with custom tooltip data. | 7 | 2 |
| [`Bleed`](./Enums.md) | Integer | The number of Bleed stacks applied, which deals bleeding damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | 3 |
| [`ForceUseAbility`](./Enums.md) | Enum | Determines which ability the target is forced to cast immediately, ignoring normal costs and cooldowns. | 1 | tk_SuckStone |
| [`Quivered`](./Enums.md) | Array / Integer | The number of stacks of Quivered, which grants bonus attacks; can be an array [stacks, probability]. | 1 | [.10] |
| [`Shield`](./Enums.md) | Enum / Integer | Specifies the number of Shield stacks applied, where each stack reduces incoming damage by a flat amount. | 1 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

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
| [`eq`](./Arrays.md#array-eq) | Array || 7 ||
| [`ge`](./Arrays.md#array-ge) | Array || 4 ||

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
| [`value`](./Math_Equations.md) | Equation | The magnitude or stat reference for this elite buff (e.g., numeric, 'spd', 'con'). | 7 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 7 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 11 ||
| [`DamageUp`](./Enums.md) | Integer | The amount of damage increase, or a string formula for dynamic calculation. | 4 | 2 |
| [`ManaGain`](./Enums.md) | Integer | The amount of mana gained; can be a fixed integer or a formula using variables like `X` (e.g., damage dealt or ability cost). | 2 | 2 |
| [`Brace`](./Enums.md) | Enum / Integer | The amount of flat damage reduction applied to the source. | 1 | 2 |
| [`ForceUseAbility`](./Enums.md) | Enum | Determines which ability the target is forced to cast immediately, ignoring normal costs and cooldowns. | 1 | tk_SuckStone |
| [`LuckUp`](./Enums.md) | Integer | Specifies the number of Luck stacks applied, where positive values increase critical hit chance and loot quality and negative values decrease them. | 1 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 10 ||
| `must_do_damage` | Boolean || 3 ||
| [`Conditional_HasStatus`](Abilities_and_Spells.md#object-conditional_hasstatus) | Object || 3 ||
| [`Conditional_HasTag`](Abilities_and_Spells.md#object-conditional_hastag) | Object | An object that executes inner effects if the target has the specified tag, else falls back. | 3 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| [`KnockbackIfCrit`](Engine_StatusAndPassiveKeys.md#object-knockbackifcrit) | Object || 1 ||
| [`Rot`](./Enums.md) | Integer | The number of stacks of Rot, causing damage over time and potentially spawning a fly on death; can be an array `[stacks, probability]`. | 1 | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 43 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 20 |
| [`AllStatsUp`](./Enums.md) | Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 6 | -2 |
| [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 6 | 2 |
| [`StrengthUp`](./Enums.md) | Integer | Specifies the number of Strength stacks applied, where positive values increase melee damage and negative values decrease it. | 6 | 1 |
| [`Charge`](./Enums.md) | Integer | The number of stacks of Charge, which makes the caster gain 1 Mana per stack at the start of its next turn. | 2 | 2 |
| [`SpeedUp`](./Enums.md) | Integer | Specifies the number of Speed stacks applied, where each stack modifies the unit's turn order and dodge chance. | 1 | 2 |

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
| `max` | Integer | Maximum coins granted. | 11 ||
| `min` | Integer | Minimum coins granted. | 11 ||

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
| [`le`](./Arrays.md#array-le) | Array || 3 ||
| [`ge`](./Arrays.md#array-ge) | Array || 2 ||
| [`lt`](./Arrays.md#array-lt) | Array || 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 ||
| [`tile`](./Arrays.md#array-tile) | Array / Enum | Specifies the tile type(s) to change to (e.g., RoadTile, WaterTile). Can be a single tile or an array of tiles. | 7 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 7 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 9 ||
| [`SpeedUp`](./Enums.md) | Integer | Specifies the number of Speed stacks applied, where each stack modifies the unit's turn order and dodge chance. | 2 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`Brace`](./Enums.md) | Enum / Integer | The amount of flat damage reduction applied to the source. | 1 | 2 |
| [`ConstitutionUp`](./Enums.md) | Integer | The amount of Constitution (HP) increase, or an array with duration and chance. | 1 | 1 |
| [`DamageUp`](./Enums.md) | Integer | The amount of damage increase, or a string formula for dynamic calculation. | 1 | 2 |
| [`StrengthUp`](./Enums.md) | Integer | Specifies the number of Strength stacks applied, where positive values increase melee damage and negative values decrease it. | 1 | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 9 ||
| [`Conditional_RandomChance`](Abilities_and_Spells.md#object-conditional_randomchance) | Object || 1 ||
| [`CreateGlobalModifiers`](Abilities_and_Spells.md#object-createglobalmodifiers) | Object | An object containing global modifier effects to apply after the time delay. | 1 ||
| [`FindItemFromPool`](./Enums.md) | Enum | Determines the item pool name from which a random item is granted to the source. | 1 | consumables |
| [`GainCoinsRange`](Abilities_and_Spells.md#object-gaincoinsrange) | Object | An object with min and max values defining the range of coins gained. | 1 ||
| [`RandomMagicMissile`](./Enums.md) | Integer | The number of random magic missiles fired, each dealing independent damage; can also be an object with custom tooltip data. | 1 | 2 |
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object | An object listing possible status effects to randomly pick from and apply. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

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
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 57 ||
| [`status`](./Enums.md#enum-status) | Enum | The status effect to apply. | 56 ||
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Duration in turns. | 52 ||
| `expires_on_begin_turn` | Boolean | If true, ticks down at the start of the turn rather than the end. | 25 ||
| `expires_on_end_turn` | Boolean | If true, the temporary effect expires at the end of the owning unit's turn. | 21 ||

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
| [`element`](./Enums.md#enum-element) | Array / Enum | Specific element type required or applied. | 5 ||
| `full_repair` | Boolean || 5 ||
| [`item`](./Enums.md#enum-item) | Enum | Item ID to reference. | 5 ||

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
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | The base damage properties of an attack. | 9 ||
| [`element`](./Enums.md#enum-element) | Array / Enum | Specific element type required or applied. | 9 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 35 ||
| [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 7 | 2 |
| [`AddMaxHealth`](./Enums.md) | Integer | The amount to add to the unit's maximum health. Negative values reduce max health. | 6 | 2 |
| [`AddStatusToBasicAttack`](Abilities_and_Spells.md#object-addstatustobasicattack) | Object | An object defining status effects to apply on basic attacks, with optional conditions. | 4 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`AllStatsUp`](./Enums.md) | Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 1 | -2 |
| [`Shield`](./Enums.md) | Enum / Integer | Specifies the number of Shield stacks applied, where each stack reduces incoming damage by a flat amount. | 1 | 2 |

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
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 5 ||
| `health` | Integer | The unit's base health, specified as an absolute integer or a percentage modifier. | 4 ||

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
| [`status`](./Enums.md#enum-status) | Enum | The specific status effect ID to remove. | 20 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 20 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||
| [`ApplyToSource`](Abilities_and_Spells.md#object-applytosource) | Object | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 3 ||
| `FlatLeechIfDamaged` | `Number` | Applies or references the 'FlatLeechIfDamaged' effect/state. | 1 ||
| [`RemoveStatusStacks`](Abilities_and_Spells.md#object-removestatusstacks) | Object | Removes a specific number of stacks of a status effect. | 1 ||
| [`ImmediateUseAbility_Instant`](./Enums.md) | Enum || 1 | head_CrownOfHorns |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||
| [`key`](./Enums.md#enum-key) | Enum | A unique identifier string that marks this condition as one-time per battle. | 3 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`ShowText`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'ShowText' effect/state. | 1 ||
| [`ReduceManaCost`](./Enums.md) | Integer | The number by which mana cost of abilities is reduced, up to a minimum of zero. | 1 | 2 |
| [`Shield`](./Enums.md) | Enum / Integer | Specifies the number of Shield stacks applied, where each stack reduces incoming damage by a flat amount. | 1 | 2 |
| [`SpellDamageUp`](./Enums.md) | Integer | The number of stacks of SpellDamageUp, increasing spell damage dealt by the unit. | 1 | 3 |

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
| [`pool`](./Enums.md#enum-pool) | Array / Enum | Specifies the loot pool, ability pool, or item category from which an item or effect is selected; can be a specific pool name, table index, or inline array. | 15 ||
| [`slot`](./Enums.md#enum-slot) | Enum / Integer | Equipment slot (weapon, hat, face, chest, etc.). | 14 ||
| `works_with_tech` | Boolean | If true, the craft ability can be used in technological (non-organic) crafting contexts. | 4 ||

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
| `health` | Integer | The unit's base health, specified as an absolute integer or a percentage modifier. | 6 ||
| `rounds` | Integer | The number of rounds the unit must wait before reviving. | 6 ||

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
| `GlobalEnemyAutoRevive` | Integer | Applies or references the 'GlobalEnemyAutoRevive' effect/state. | 2 ||
| `NoCorpses` | `Number` | Applies or references the 'NoCorpses' effect/state. | 1 ||
| `RealTimePressure` | Integer | Applies or references the 'RealTimePressure' effect/state. | 1 ||
| [`{Global Modifier Keys}`](./Engine_GlobalModifierKeys.md#valid-property-keys) | Boolean | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

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
| [`mode`](./Enums.md#enum-mode) | Enum | Specifies the comparison operator for evaluating a condition against a threshold (e.g., equal, greater). | 9 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 9 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 9 ||
| [`threshold`](#object-threshold) | Enum / Integer / Object | The health threshold value (absolute or equation) at which this ability becomes available. | 9 | 2 |

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
| `count` | Array / Integer | Quantity. | 1 ||
| `except_tiny` | Boolean || 1 ||
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the template identifier of the entity to spawn, referencing a predefined character or object in the game data. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||
| [`DivineShield`](./Enums.md) | Array / Integer | The number of charges of Divine Shield applied, which blocks the next instances of damage entirely; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 2 | [.5] |
| [`Conditional_GoodRoll`](Abilities_and_Spells.md#object-conditional_goodroll) | Object | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 1 ||
| `Metronome` | `Number` | Executes a random musical or metronome ability. | 1 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

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
| `count` | Array / Integer | Quantity. | 7 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 ||
| [`Fear`](./Enums.md) | Array / Integer | The number of Fear stacks applied, which reduces the target's accuracy and may cause it to flee; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 3 | [.15] |
| [`Charmed`](./Enums.md) | Integer | The number of turns of Charmed applied, or an array with duration and chance. | 1 | 2 |
| [`Confusion`](./Enums.md) | Integer | The number of turns of Confusion applied, or an array with duration and chance. | 1 | 2 |
| [`Freeze`](./Enums.md) | Array / Integer | The number of stacks of Freeze, immobilizing the unit for that many turns; can be an array `[stacks, probability]`. | 1 | [.1] |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

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
| `ally_chance` | Integer || 5 ||
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 5 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 ||
| [`Quivered`](./Enums.md) | Array / Integer | The number of stacks of Quivered, which grants bonus attacks; can be an array [stacks, probability]. | 5 | [.10] |

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
| `reduction` | Integer || 7 ||
| [`class`](./Enums.md#enum-class) | Enum | Character class identifier. | 6 ||

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
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution. | 3 | |

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
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 5 ||
| `melee_only` | Boolean || 1 ||
| `ranged_only` | Boolean | If true, this reaction only triggers from ranged attacks. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 66 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 23 |
| [`ApplyToSource`](Abilities_and_Spells.md#object-applytosource) | Object | An object containing status effects or modifiers applied to the source (attacker) of the triggering condition rather than the target. | 6 ||

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
| [`slot`](./Enums.md#enum-slot) | Enum / Integer | Equipment slot (weapon, hat, face, chest, etc.). | 3 ||
| [`value`](./Math_Equations.md) | Equation | The magnitude or stat reference for this elite buff (e.g., numeric, 'spd', 'con'). | 3 ||

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
| [`number`](./Arrays.md#array-number) | Array / Integer || 31 ||
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the template identifier of the entity to spawn, referencing a predefined character or object in the game data. | 23 ||

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
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the template identifier of the entity to spawn, referencing a predefined character or object in the game data. | 11 ||
| [`number`](./Arrays.md#array-number) | Array / Integer || 10 ||

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
| [`stack_key`](./Enums.md#enum-stack_key) | Enum || 3 ||
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 3 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| [`Conditional_Boss`](Abilities_and_Spells.md#object-conditional_boss) | Object || 2 ||
| [`Poison`](./Enums.md) | Integer | The number of Poison stacks applied, which deals poison damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | 2 |

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
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 8 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| [`Charge`](./Enums.md) | Integer | The number of stacks of Charge, which makes the caster gain 1 Mana per stack at the start of its next turn. | 2 | 2 |
| [`IntelligenceUp`](./Enums.md) | Integer | The amount of intelligence increase, which can be a fixed integer or a mathematical expression. | 1 | 2 |
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object | An object or entity name that spawns upon hitting a character, with optional stacks and chance. | 1 | BestBud |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 ||
| [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 3 | 2 |
| [`RepairTrinket`](./Enums.md) | Integer | The amount of durability restored to the trinket item slot. | 1 | 99 |
| [`RepairWeapon`](./Enums.md) | Array / Integer | The number of stacks of RepairWeapon applied (or an array [stacks, probability] for random application). | 1 | [.25] |

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
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 5 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 ||
| [`Charge`](./Enums.md) | Integer | The number of stacks of Charge, which makes the caster gain 1 Mana per stack at the start of its next turn. | 1 | 2 |
| [`DamageUp`](./Enums.md) | Integer | The amount of damage increase, or a string formula for dynamic calculation. | 1 | 2 |
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of health regeneration (HealthRegen) granted by this damage instance. | 1 | 2 |
| [`Shield`](./Enums.md) | Enum / Integer | Specifies the number of Shield stacks applied, where each stack reduces incoming damage by a flat amount. | 1 | 2 |
| [`SpellDamageUp`](./Enums.md) | Integer | The number of stacks of SpellDamageUp, increasing spell damage dealt by the unit. | 1 | 3 |
| [`Thorns`](./Enums.md) | Integer | The number of Thorns stacks applied, which deals damage back to melee attackers. | 1 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

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
| [`element`](./Enums.md#enum-element) | Array / Enum | Specific element type required or applied. | 6 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 ||
| [`Burn`](./Enums.md) | Integer | The number of Burn stacks applied, which deals fire damage over time; can be an integer, a variable X, or an array `[stacks, probability]` to specify chance of application. | 3 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`Stun`](./Enums.md) | Array | The number of Stun stacks applied, which prevents the target from taking actions; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | [.1] |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||
| [`Bounty`](./Enums.md) | Integer | The number of Bounty status stacks applied to random enemies each turn. | 3 | 1 |
| `count` | Array / Integer | Quantity. | 2 ||
| [`Marked`](./Enums.md) | Integer | The number of Marked stacks applied, which increases damage taken from all sources; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

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
| `chance_to_break` | Integer || 2 ||
| `durability_loss` | Integer || 2 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 137 ||
| [`ModifyAbility`](Engine_StatusAndPassiveKeys.md#object-modifyability) | Object || 2 ||

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
| `crit_chance` | `Number` | The chance for the damage instance to critically hit, expressed as a percentage (e.g., 50%) or a decimal fraction (e.g., .5). | 4 ||
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | The base damage properties of an attack. | 4 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 6 ||
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 6 ||

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
| `backstab_only` | Boolean || 1 ||
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 ||

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
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`Conditional_Ally`](Abilities_and_Spells.md#object-conditional_ally) | Object || 1 ||
| [`Conditional_PlayerCat`](Abilities_and_Spells.md#object-conditional_playercat) | Object || 1 ||

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
| [`odds`](./Enums.md#enum-odds) | Number | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. | 8 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 8 |
| [`Temporary`](Abilities_and_Spells.md#object-temporary) | Object | An object that defines a temporary status effect with duration and expiration conditions. | 5 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 19 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 6 |
| [`AllStatsUp`](./Enums.md) | Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 2 | -2 |

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
| `mana` | Enum / Integer || 1605 ||
| `charge` | Integer / String || 18 ||

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
| [`{Global Modifier Keys}`](./Engine_GlobalModifierKeys.md#valid-property-keys) | Boolean | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 ||
| `NextPlayerCatTakesExtraTurn` | `Number` | Applies or references the 'NextPlayerCatTakesExtraTurn' effect/state. | 1 ||
| `NoCorpses` | `Number` | Applies or references the 'NoCorpses' effect/state. | 1 ||

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
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | The flat damage amount. | 7 ||
| [`type`](./Enums.md#enum-type) | Enum | The classification of the damage (e.g., spell, melee). | 7 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 ||
| [`damage_tiles`](./Enums.md#enum-damage_tiles) | Enum | Determines which tiles are damaged by the effect (e.g., 'all'). | 4 ||
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 4 ||

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
| `reduction` | Integer || 5 ||
| [`element`](./Arrays.md#array-element) | Array / Enum | Specific element type required or applied. | 5 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 1 ||
| `even_if_stunned` | Boolean | If true, the reaction triggers even if the unit is stunned. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 16 ||
| [`DivineShield`](./Enums.md) | Array / Integer | The number of charges of Divine Shield applied, which blocks the next instances of damage entirely; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | [.5] |
| [`Immobile`](./Enums.md) | Integer | The number of turns of Immobile applied, or an array with duration and chance. | 1 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

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
| `is_basic_attack` | Boolean | If true, the ability is considered a basic attack and uses basic attack rules. | 6 ||
| `is_weapon` | Boolean | If true, the ability is treated as a ability item. | 4 ||

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
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Currency value in shops/merchants. | 2 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for an ability such as name, description, class, and icon type. | 2 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 11 ||
| `enemies_only` | Boolean | If true, this effect only targets enemies. | 7 ||
| `on_self_move_too` | Boolean | If true, the movement reaction also triggers when the unit moves itself. | 3 ||
| `create_temp_ability` | Boolean || 2 ||

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
| [`object`](./Enums.md#enum-object) | Array / Enum | The entity ID of the character to spawn (e.g., CharmedFlea). | 7 ||
| [`stacks`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Number of stacks or intensity to apply. | 5 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`Metal`](./Enums.md) | Integer || 2 | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 13 ||
| [`mode`](./Enums.md#enum-mode) | Enum | Specifies the comparison operator for evaluating a condition against a threshold (e.g., equal, greater). | 13 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 13 ||
| [`threshold`](#object-threshold) | Enum / Integer / Object | The health threshold value (absolute or equation) at which this ability becomes available. | 13 | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`Brace`](./Enums.md) | Enum / Integer | The amount of flat damage reduction applied to the source. | 2 | 2 |

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
| [`element`](./Enums.md#enum-element) | Array / Enum | Specific element type required or applied. | 2 ||
| [`text`](./Strings.md#string-text) | String || 2 ||

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
| `break_on_pop_only` | Boolean || 2 ||
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the template identifier of the entity to spawn, referencing a predefined character or object in the game data. | 2 ||

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
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`TempMeleeRangeUp`](./Enums.md) | Integer || 1 | 1 |
| [`TempRangeUp`](./Enums.md) | Integer | The number of turns this unit gains increased attack range. | 1 | 1 |
| [`UseAbility`](./Enums.md) | Enum | Specifies the ability name the unit will use at the end of each round. | 1 | neck_DarkFriend |

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
| [`stack_key`](./Enums.md#enum-stack_key) | Enum || 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`threshold`](#object-threshold) | Enum / Integer / Object | The health threshold value (absolute or equation) at which this ability becomes available. | 2 | 2 |
| `expires_on_end_turn` | Boolean | If true, the temporary effect expires at the end of the owning unit's turn. | 1 ||
| [`ExtraBasicMoves_Status`](./Enums.md) | Integer | The number of extra basic moves the unit can perform each turn. Stacks for additional moves. | 1 | 1 |
| [`RefreshActPoints`](./Enums.md) | Integer | The amount of action points restored to the unit. | 1 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 ||
| [`DivineShield`](./Enums.md) | Array / Integer | The number of charges of Divine Shield applied, which blocks the next instances of damage entirely; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | [.5] |
| [`RepairTrinket`](./Enums.md) | Integer | The amount of durability restored to the trinket item slot. | 1 | 99 |

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
| `SerratedClaws` | Integer | Applies or references the 'SerratedClaws' effect/state. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 1 | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`Shield`](./Enums.md) | Enum / Integer | Specifies the number of Shield stacks applied, where each stack reduces incoming damage by a flat amount. | 2 | 2 |
| [`DoDamage`](Abilities_and_Spells.md#object-dodamage) | Object | An object defining damage to deal, including damage amount and type. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 ||
| [`Charge`](./Enums.md) | Integer | The number of stacks of Charge, which makes the caster gain 1 Mana per stack at the start of its next turn. | 4 | 2 |
| [`Shield`](./Enums.md) | Enum / Integer | Specifies the number of Shield stacks applied, where each stack reduces incoming damage by a flat amount. | 1 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 ||
| [`LuckUp`](./Enums.md) | Integer | Specifies the number of Luck stacks applied, where positive values increase critical hit chance and loot quality and negative values decrease them. | 1 | 2 |
| [`Shield`](./Enums.md) | Enum / Integer | Specifies the number of Shield stacks applied, where each stack reduces incoming damage by a flat amount. | 1 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

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
| [`bonus_passives`](Abilities_and_Spells.md#object-bonus_passives) | Object | Passives granted to the character while this ability is equipped. | 2 ||

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
| `int` | Enum / Integer || 8 ||
| `con` | Enum / Integer | The constitution stat value or modifier for the unit. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 13 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 12 ||
| [`threshold`](#object-threshold) | Enum / Integer / Object | The health threshold value (absolute or equation) at which this ability becomes available. | 12 | 2 |
| `even_if_stunned` | Boolean | If true, the reaction triggers even if the unit is stunned. | 7 ||
| `immediate` | Boolean | If true, the forced attack executes immediately without waiting. | 6 ||
| `aux` | Integer | An integer modifier for the auxiliary stat, often used for scaling or effect values. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 1 ||
| `even_of_stunned` | Boolean || 1 ||

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
| `add` | Array / Integer || 1 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 ||
| [`options`](./Enums.md) | Array || 1 | [smash] |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 ||
| [`AllStatsUp`](./Enums.md) | Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 1 | -2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`Bleed`](./Enums.md) | Integer | The number of Bleed stacks applied, which deals bleeding damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | 3 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| [`Leech`](./Enums.md) | Integer | The amount of health stolen per hit as a percentage of damage dealt. | 1 | 1 |

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
| [`CastAgainWithStatus`](Engine_StatusAndPassiveKeys.md#object-castagainwithstatus) | Object | Applies or references the 'CastAgainWithStatus' effect/state. | 1 ||

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
| `include_spells` | Boolean || 1 ||
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 1 ||

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
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | A damage instance object that defines the damage, type, effects, and AI scoring for an ability. | 1 ||

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
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 ||
| `range` | Enum / Integer | Distance or area of effect in tiles. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 13 ||
| [`StatusOnBattleEnd`](Abilities_and_Spells.md#object-statusonbattleend) | Object | A block containing status effects or passives that are applied to the unit when a battle ends. | 5 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to autocast. | 9 ||
| `even_if_stunned` | Boolean | If true, bypasses stun and hard-CC restrictions to cast anyway. | 6 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | The specific dodge ability to trigger (e.g., DestroyerDodge). | 7 ||
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 7 ||

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
| `max_bounces` | Integer || 3 ||
| `max_range` | Enum / Integer || 3 ||

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
| [`exclude`](./Enums.md#enum-exclude) | Enum | Specifies an element type that is excluded from triggering the form change. | 1 ||

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
| `OverrideDamage` | `Number` | Applies or references the 'OverrideDamage' effect/state. | 1 ||
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 1 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

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
| `head` | Enum / Number | The visual ID (integer) of the head part applied to the cat. | 1 ||

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
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 ||
| [`event`](./Enums.md#enum-event) | Enum || 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 28 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 8 |
| [`ManaGain`](./Enums.md) | Integer | The amount of mana gained; can be a fixed integer or a formula using variables like `X` (e.g., damage dealt or ability cost). | 1 | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 10 ||
| [`RandomMutation`](./Enums.md) | Integer | The number of random mutations to apply. | 1 | 1 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution. | 1 | |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 34 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 12 |
| [`Leeches`](./Enums.md) | Integer | The number of Leech stacks applied, healing the attacker. | 1 | 1 |

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
| [`tag`](./Enums.md#enum-tag) | Array / Enum | The specific string tag to check for. | 46 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 46 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 11 |
| [`BonusKnockbackDamage`](./Enums.md) | Integer || 1 | 5 |
| [`OverrideChainKnockback`](./Enums.md) | Integer | The number of tiles to override the default chain knockback distance. | 1 | 0 |

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
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 ||
| `threshold_flat` | Integer | A flat numerical health value threshold. | 5 ||
| [`Conditional_OncePerBattle`](Abilities_and_Spells.md#object-conditional_onceperbattle) | Object | Conditional trigger: Executes nested logic only once per encounter/battle. | 1 ||

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
| `threshold_flat` | Integer || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`RepairTrinket`](./Enums.md) | Integer | The amount of durability restored to the trinket item slot. | 1 | 99 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution. | 1 | |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution. | 2 | |
| [`Charge`](./Enums.md) | Integer | The number of stacks of Charge, which makes the caster gain 1 Mana per stack at the start of its next turn. | 1 | 2 |

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
| `odds` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 4 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||
| [`ApplyPassives`](Abilities_and_Spells.md#object-applypassives) | Object | Grants the nested passive abilities dynamically. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||

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
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution. | 2 | |

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
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`DelayedPain`](./Enums.md) | Integer | The number of stacks of DelayedPain, which deals damage to the unit after a delay (e.g., at the end of its next turn). | 1 | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 12 ||
| [`Fear`](./Enums.md) | Array / Integer | The number of Fear stacks applied, which reduces the target's accuracy and may cause it to flee; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | [.15] |

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
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2344 ||
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 1787 ||
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | The base damage properties of an attack. | 1447 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 359 ||

</details>

---


<details>
<summary><b>AddSelfStatusToWeapons</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1554 ||

</details>

<details>
<summary><b>AddStatusToKnockbackDamage</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1554 ||

</details>

<details>
<summary><b>AddStatusToSpells</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1554 ||

</details>

<details>
<summary><b>ApplyToRandomPartyMemberIfPossible</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1554 ||

</details>

<details>
<summary><b>Conditional_Adjacent</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1554 ||

</details>

<details>
<summary><b>Conditional_HealthThreshold</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1554 ||

</details>

<details>
<summary><b>Conditional_PartyMember</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1554 ||

</details>

<details>
<summary><b>Conditional_Shielded</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1554 ||

</details>

<details>
<summary><b>ExtraStatusWhenDealingDamage</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1554 ||

</details>

<details>
<summary><b>PassiveWhenDead</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1554 ||

</details>

<details>
<summary><b>PassiveWhileHasDurability</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1554 ||

</details>

<details>
<summary><b>ScaledStatusAlliesOnSpendMana</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1554 ||

</details>

<details>
<summary><b>StatusAlliesEachTurn</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1554 ||

</details>

<details>
<summary><b>StatusIfUnusedActPoints</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1554 ||

</details>

<details>
<summary><b>StatusOnEndMove</b></summary>

> **Total Count:** 9

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1554 ||

</details>

<details>
<summary><b>StatusOnFallAsleep</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1554 ||

</details>

### Object: `DestroyEquipmentAndAttachParasite`


**Definition:** Removes an equipped item and replaces it with a parasite from a specified pool.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleStart`](./Items_and_Equipment.md#context-statusonbattlestart)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`pool`](./Arrays.md#array-pool) | Array / Enum | The item pool to draw the parasite from. | 6 ||
| [`chance`](./Enums.md#enum-chance) | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 4 ||

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
| `health_percent` | Integer || 3 ||
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 3 ||

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
| `allies_only` | Boolean | If true, the Buddy effect only targets allies. | 1 ||
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 1 ||
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 ||

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
| `knockback` | Enum / Integer | The number of tiles to push the target away from the attacker; can be negative to pull the target closer, or 'str' to scale with the attacker's strength stat. | 1 ||

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
| `knockback` | Enum / Integer | The number of tiles to push the target away from the attacker; can be negative to pull the target closer, or 'str' to scale with the attacker's strength stat. | 1 ||
| `override_chain_knockback` | Integer | Overrides the chain knockback distance for the knockback effect. | 1 ||

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
| `distance` | Integer | The distance in tiles to knock the target away. | 24 ||
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 22 ||

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
| `max` | Integer | The maximum value that the auxiliary counter can reach. | 1 ||
| `min` | Integer | The minimum amount of coins gained from the range. | 1 ||

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
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 ||
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the template identifier of the entity to spawn, referencing a predefined character or object in the game data. | 1 ||

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
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 4 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 4 ||

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
| [`element`](./Enums.md#enum-element) | Array / Enum | Specific element type required or applied. | 18 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 18 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 18 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`Brace`](./Enums.md) | Enum / Integer | The amount of flat damage reduction applied to the source. | 3 | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of health regeneration (HealthRegen) granted by this damage instance. | 1 | 2 |

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
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 ||
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the template identifier of the entity to spawn, referencing a predefined character or object in the game data. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 33 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 12 |
| [`PermanentCharisma`](./Enums.md) | Integer | The amount of permanent Charisma stat increase applied. | 1 | 1 |
| [`PermanentConstitution`](./Enums.md) | Integer | The amount of permanent Constitution (max HP) added. | 1 | 2 |
| [`PermanentDexterity`](./Enums.md) | Integer | The amount of permanent dexterity added to the unit. | 1 | 1 |
| [`PermanentIntelligence`](./Enums.md) | Integer | The number of permanent intelligence stat points added or subtracted. | 1 | -1 |
| [`PermanentLuck`](./Enums.md) | Integer | The amount of permanent Luck stat increase applied. | 1 | 1 |
| [`PermanentSpeed`](./Enums.md) | Integer | The number of permanent speed stat points added or subtracted. | 1 | 1 |
| [`PermanentStrength`](./Enums.md) | Integer | The amount of permanent Strength stat increase applied. | 1 | 1 |

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
| `stacks` | Enum / Integer | The number of stacks to remove. | 4 ||
| [`status`](./Enums.md#enum-status) | Enum | The specific status effect ID to remove. | 4 ||

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
| `revive_health` | Integer | The flat amount of health to revive with. | 4 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`Shield`](./Enums.md) | Enum / Integer | Specifies the number of Shield stacks applied, where each stack reduces incoming damage by a flat amount. | 3 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

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
| [`CompleteItemQuest`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'CompleteItemQuest' effect/state. | 1 ||
| [`RemoveItem`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'RemoveItem' effect/state. | 1 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`RandomMagicMissile`](./Enums.md) | Integer | The number of random magic missiles fired, each dealing independent damage; can also be an object with custom tooltip data. | 1 | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`StatusAfterXStacks`](Engine_StatusAndPassiveKeys.md#object-statusafterxstacks) | Object || 1 ||

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
| [`faction`](./Enums.md#enum-faction) | Enum | Determines which faction the spawned entity belongs to, controlling its team allegiance and targeting behavior. | 4 ||
| [`obj`](./Enums.md#enum-obj) | Array / Enum | The object(s) spawned when this passive triggers. | 4 ||

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
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specific entity tag required. | 1 ||
| [`count`](./Arrays.md#array-count) | Array / Integer | Quantity. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`AddDamageToBasicAttack`](./Enums.md) | Enum || 1 | min(min(min(min(min(min(str,dex),int),con),lck),spd),cha)-2 |

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
| `ForceMoveAway` | `Number` | Applies or references the 'ForceMoveAway' effect/state. | 1 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

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
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`ForceUseAbility`](./Enums.md) | Enum | Determines which ability the target is forced to cast immediately, ignoring normal costs and cooldowns. | 2 | tk_SuckStone |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 ||
| [`DivineShield`](./Enums.md) | Array / Integer | The number of charges of Divine Shield applied, which blocks the next instances of damage entirely; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | [.5] |

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
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`DoDamage`](Abilities_and_Spells.md#object-dodamage) | Object | An object defining damage to deal, including damage amount and type. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||
| [`ForceUseAbility`](./Enums.md) | Enum | Determines which ability the target is forced to cast immediately, ignoring normal costs and cooldowns. | 1 | tk_SuckStone |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 ||
| [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 4 | 2 |
| [`Charge`](./Enums.md) | Integer | The number of stacks of Charge, which makes the caster gain 1 Mana per stack at the start of its next turn. | 2 | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`StatusAfterXStacks`](Engine_StatusAndPassiveKeys.md#object-statusafterxstacks) | Object || 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`DodgeChance_Status`](./Enums.md) | Integer | The percentage of dodge chance granted by this status effect. | 1 | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 ||
| [`RepairTrinket`](./Enums.md) | Integer | The amount of durability restored to the trinket item slot. | 1 | 99 |
| [`TempPassiveUntilSettled`](Characters_and_Bosses.md#object-temppassiveuntilsettled) | Object || 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`Charge`](./Enums.md) | Integer | The number of stacks of Charge, which makes the caster gain 1 Mana per stack at the start of its next turn. | 1 | 2 |

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
| [`AllStatsUp`](./Enums.md) | Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 1 | -2 |
| [`FillMana`](./Enums.md) | Integer | The amount of mana restored to the unit; can be a fixed integer or an array `[stacks, probability]` for a chance-based application. | 1 | 1 |
| [`HealRandomInjury`](./Enums.md) | Integer | The number of random injuries healed on the target. | 1 | 1 |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

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
| [`Conditional_OncePerBattle`](Abilities_and_Spells.md#object-conditional_onceperbattle) | Object | Conditional trigger: Executes nested logic only once per encounter/battle. | 1 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||
| [`Shield`](./Enums.md) | Enum / Integer | Specifies the number of Shield stacks applied, where each stack reduces incoming damage by a flat amount. | 1 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`GainCoins`](./Enums.md) | Array / Integer | The number of coins gained or lost; can be a fixed integer, a range `[min, max]`, or a negative value to deduct coins. | 1 | [3] |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`DamageUp`](./Enums.md) | Integer | The amount of damage increase, or a string formula for dynamic calculation. | 1 | 2 |
| [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 1 | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`Charge`](./Enums.md) | Integer | The number of stacks of Charge, which makes the caster gain 1 Mana per stack at the start of its next turn. | 1 | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`LimitHeal`](./Enums.md) | Integer | The maximum amount of health the unit can heal per instance. | 1 | 0 |

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
| [`ignore_if_str_aux_equals`](./Enums.md#enum-ignore_if_str_aux_equals) | Enum || 1 ||
| [`add`](./Arrays.md#array-add) | Array / Integer || 1 ||
| [`mul`](./Arrays.md#array-mul) | Array || 1 ||

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
| [`from`](./Enums.md#enum-from) | Enum | The original weapon ID. | 2 ||
| [`to`](./Enums.md#enum-to) | Enum | The transformed weapon ID. | 2 ||

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
| `crit_chance` | `Number` | The chance for the damage instance to critically hit, expressed as a percentage (e.g., 50%) or a decimal fraction (e.g., .5). | 1 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

---
