# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Cat Mutations

> **Associated Files:** `data/mutations/`


### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 489

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 2985 |  |
| [`desc`](./Strings.md#string-desc) | Enum | Examples: `"MUTATION_BODY_309_DESC", "MUTATION_BODY_312_DESC", "MUTATION_BODY_301_DESC"` | 2423 |  |
| `shield` | Enum / Integer | Examples: `12, 5, 10` | 191 |  |
| `cha` | Enum / Integer | Examples: `2, -1, 1` | 89 |  |
| `con` | Enum / Integer | Examples: `-2, -3, 1` | 79 |  |
| `spd` | Enum / Integer | Examples: `1, -1, -2` | 78 |  |
| `int` | Enum / Integer | Examples: `2, -1, 1` | 66 |  |
| `lck` | Enum / Integer | Examples: `2, -1, 1` | 53 |  |
| `str` | Enum / Integer | Examples: `2, -1, 1` | 45 |  |
| `dex` | Enum / Integer | Examples: `2, -1, -2` | 30 |  |
| `divine_shield` | Integer | Examples: `1` | 20 |  |
| `speed` | Array / Number | Examples: `-4` | 19 |  |
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Examples: `common, melted, animal` | 7 |  |
| [`attack`](./Enums.md#enum-attack) | Enum | Examples: `FetusSpit` | 7 |  |

</details>

---

### Object: `passives`


**Definition:** Object listing intrinsic passive modifiers.  
**Total Count:** 284


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveWhenAffectedByElement`](./Cat_Mutations.md#context-passivewhenaffectedbyelement), [`PassiveWhileHasStatus`](./Cat_Mutations.md#context-passivewhilehasstatus), [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 2039 |  |
| [`AddStatusToBasicAttack`](Abilities_and_Spells.md#object-addstatustobasicattack) | Object | An object defining status effects to apply on basic attacks, with optional conditions. | 133 ||
| [`Brace`](./Enums.md) | Integer | The amount of flat damage reduction applied to the source. | 94 | 1 |
| [`Trample`](./Enums.md) | Integer | The number of tiles this character can move through enemies, dealing damage or applying effects equal to the value. | 88 | 3 |
| [`Thorns`](./Enums.md) | Integer | The number of Thorns stacks applied, which deals damage back to melee attackers. | 65 | 2 |
| [`MeleeRevengeDamage`](Abilities_and_Spells.md#object-meleerevengedamage) | Object | A damage instance object that triggers when the unit is hit by melee attacks while this passive is active. | 59 ||
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of health regeneration (HealthRegen) granted by this damage instance. | 52 | 2 |
| [`StatusEachTurnEnd`](#object-statuseachturnend) | Object | Status effects that are applied to the unit at the end of each turn. | 49 ||
| [`StatusOnBattleEnd`](Abilities_and_Spells.md#object-statusonbattleend) | Object | A block containing status effects or passives that are applied to the unit when a battle ends. | 45 ||
| [`ElementImmune`](./Enums.md) | Enum | Specifies an element (e.g., Fire, Ice) the unit is immune to. | 39 | Ice |
| [`CounterAttack`](#object-counterattack) | Object | Specifies the ability name used for counterattacking when hit. | 34 ||
| [`StatusImmunity`](./Enums.md) | Array | List of status effects the unit is immune to. | 34 | [Freeze] |
| [`StatusOnKill`](#object-statusonkill) | Object | Status effects applied to the unit whenever it kills an enemy. | 29 ||
| [`StatusOnTookDamage`](#object-statusontookdamage) | Object | Status effects applied to the unit whenever it takes damage. | 29 ||
| [`SpawnThingOnDamage`](#object-spawnthingondamage) | Object | Object specifying an entity to spawn when the unit takes damage, with optional conditions. | 28 ||
| [`AbilityReaction`](./Enums.md) | Enum | Specifies an ability to trigger as a reaction when certain conditions are met. | 23 | SkunkTail |
| [`DamageUp`](./Enums.md) | Integer | The amount of damage increase, or a string formula for dynamic calculation. | 21 | 2 |
| [`AddMovement`](./Enums.md) | Integer | The number of extra movement tiles the unit gains per turn. | 20 | 1 |
| [`StatusEachTurnBegin`](#object-statuseachturnbegin) | Object | Status effects applied to the unit at the beginning of each turn. | 18 ||
| [`CritChanceUp`](./Enums.md) | Integer | The amount of critical hit chance increase, in percentage points. | 16 | 5 |
| [`AddBonusRange`](./Enums.md) | Integer | The number of extra tiles added to the unit's attack range. | 15 | 1 |
| [`KineticSpikes`](./Enums.md) | Integer | The number of Kinetic Spikes stacks applied, which deal damage back to attackers when the unit is hit. | 15 | 1 |
| [`RevengeDamage`](Abilities_and_Spells.md#object-revengedamage) | Object | An object specifying the effects (e.g., Marked, Charmed, Petrify) applied to the attacker when the unit takes damage. | 15 ||
| [`SpawnEachTurn`](#object-spawneachturn) | Object | Object specifying an entity to spawn each turn, with chance and number. | 15 ||
| [`AddCorpseHealth`](./Enums.md) | Integer | The amount of additional health a corpse has when the unit dies. | 14 | 2 |
| [`AllStatsUp`](./Enums.md) | Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 14 | 1 |
| [`DodgeChance`](./Enums.md) | Integer | The percentage chance to dodge incoming attacks. | 14 | 2 |
| [`WaterWalk`](./Enums.md) | Integer | If set to 1, allows the unit to move over water tiles as if they were normal terrain. | 14 | 1 |
| [`AddManaRegen`](./Enums.md) | Integer | The amount of additional mana regeneration per turn granted while this passive is active. | 13 | 1 |
| [`MulticlassLevelUp`](./Enums.md) | Enum | Specifies the class that the unit gains a level in upon leveling up. | 12 | Hunter |
| [`ReflectProjectiles`](./Enums.md) | Integer | The percentage chance to reflect projectiles back at the attacker. | 12 | 10 |
| [`BleedThorns`](./Enums.md) | Integer | The number of Bleed Thorns stacks applied, which deals bleeding damage back to melee attackers. | 11 | 2 |
| [`ExtraBasicAttacks`](./Enums.md) | Integer | The number of additional basic attacks the unit can perform each turn. | 11 | 2 |
| [`MoveWhenDamaged`](#object-movewhendamaged) | Object | Defines movement behavior triggered when the unit takes damage, including the ability to use and movement weights. | 11 ||
| [`ReplaceBasicMove`](./Enums.md) | Enum | Specifies the ability that replaces the unit's default basic move. | 11 | ToadJump_BasicMove |
| [`AddLevelUpRerolls`](./Enums.md) | Integer | The number of additional rerolls the unit gets when leveling up. | 10 | 1 |
| [`BackstabImmunity`](./Enums.md) | Integer | If set to 1, the unit is immune to backstab damage. | 9 | 1 |
| [`Bruise`](./Enums.md) | Integer | The number of Bruise stacks applied, or an array with duration and chance. | 9 | 2 |
| [`DepressionAura`](./Enums.md) | Integer | The number of Depression stacks applied to nearby units as an aura. | 9 | 1 |
| [`MissChance`](./Enums.md) | Integer | The percentage chance that the unit's attacks will miss. | 9 | 20 |
| [`PoisonThorns`](./Enums.md) | Integer | Applies Poison stacks to any unit that attacks this unit in melee. | 9 | 2 |
| [`StatusOnDie`](#object-statusondie) | Object | Defines statuses or effects that are applied when the unit dies. | 8 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 8 |
| [`AddElementsToBasicAttack`](./Enums.md) | Enum | Specifies the elemental damage type added to the unit's basic attack. | 7 | Ice |
| [`AddInitiative`](./Enums.md) | Integer | The amount to add to the unit's initiative score, affecting turn order. | 7 | -20 |
| [`AlphaTurns`](./Enums.md) | Integer | The number of additional alpha turns the unit receives at the start of combat. | 7 | 1 |
| [`Bleed`](./Enums.md) | Array / Integer | The number of Bleed stacks applied, which deals bleeding damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 7 | [3] |
| [`ManaCostReduction`](./Enums.md) | Integer | The amount or percentage by which the mana cost of abilities is reduced. | 7 | 1 |
| [`StatusOnEndMove`](#object-statusonendmove) | Object | Defines statuses or effects applied when the unit finishes moving. | 7 ||
| [`AddDamageToElementDamage`](#object-adddamagetoelementdamage) | Object | Adds extra damage to attacks that deal a specified element type. | 6 ||
| [`DodgeChance_Status`](./Enums.md) | Integer | The percentage of dodge chance granted by this status effect. | 6 | 10 |
| [`IgnoreTiles`](./Enums.md) | Integer | If set to 1, the unit ignores tile effects while moving. | 6 | 1 |
| [`Poison`](./Enums.md) | Integer | The number of Poison stacks applied, which deals poison damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 6 | 1 |
| [`Quivered`](./Enums.md) | Array / Integer | The number of stacks of Quivered, which grants bonus attacks; can be an array [stacks, probability]. | 6 | [0.1] |
| [`SpawnOnBattleStartRandomEmptyTile`](#object-spawnonbattlestartrandomemptytile) | Object | Spawns specified objects on random empty tiles at the start of battle. | 6 ||
| [`StatusOnTookDamageFromAbility`](#object-statusontookdamagefromability) | Object | Defines statuses applied when the unit takes damage from an ability. | 6 ||
| [`YOffset`](./Enums.md) | Number | A vertical offset multiplier used to adjust the unit's visual position on the tile. | 6 | .25 |
| [`AddBonusMeleeRange`](./Enums.md) | Integer | The number of additional tiles of range added to melee attacks. | 5 | 1 |
| [`ClassManaCostReduction`](#object-classmanacostreduction) | Object | Reduces the mana cost of abilities belonging to a specified class. | 5 ||
| [`KnockbackImmunity`](./Enums.md) | Integer | If set to 1, the unit is immune to knockback effects. | 5 | 1 |
| [`StatusIfUnusedMovePoints`](#object-statusifunusedmovepoints) | Object | Defines statuses applied if the unit has leftover movement points at the end of its turn. | 5 ||
| [`AddKnockbackDamage`](./Enums.md) | Integer | The amount of additional damage dealt when the unit knocks back an enemy. | 4 | 1 |
| [`AddTemporaryEffectsToBasicAttack`](#object-addtemporaryeffectstobasicattack) | Object | Adds temporary statuses or effects to the unit's basic attack for the current turn. | 4 ||
| [`BoostWeaponDamage`](./Enums.md) | Integer | Increases the damage dealt by the unit's weapon. | 4 | 1 |
| [`ChanceToBackflip`](#object-chancetobackflip) | Object | Defines the chance and ability used for the unit to backflip and dodge an incoming attack. | 4 ||
| [`EquipTemporaryItem`](./Enums.md) | Enum | Specifies the item that is temporarily equipped to the unit. | 4 | WaterBottle_Full |
| [`PassiveWhenAffectedByElement`](#object-passivewhenaffectedbyelement) | Object | Grants additional passive effects when the unit is under the effects of a specified element. | 4 ||
| [`StatusEveryXSpellCasts`](#object-statuseveryxspellcasts) | Object | Applies specified statuses after the unit casts a certain number of spells. | 4 ||
| [`StatusOnAllyCatDeath`](#object-statusonallycatdeath) | Object | Defines statuses applied when an ally cat dies. | 4 ||
| [`StatusOnCastSpell`](#object-statusoncastspell) | Object | Defines statuses applied when the unit casts a spell. | 4 ||
| [`AbilityWhenTaggedCharacterMovesNear`](#object-abilitywhentaggedcharactermovesnear) | Object | Triggers a specified ability when a character with a specific tag moves within range. | 3 ||
| [`AddStatusToBasicMeleeAttack`](#object-addstatustobasicmeleeattack) | Object | Adds specified statuses to the unit's basic melee attacks. | 3 ||
| [`Confusion`](./Enums.md) | Array / Integer | The number of turns of Confusion applied, or an array with duration and chance. | 3 | [2] |
| [`SpawnExtraThingsOnBattleStart`](#object-spawnextrathingsonbattlestart) | Object | Spawns specified objects, tiles, or traps at the start of battle. | 3 ||
| [`StatusOnEatFood`](#object-statusoneatfood) | Object | Defines statuses applied when the unit consumes food. | 3 ||
| [`CanRemoveCursedItems`](./Enums.md) | Integer | If set to 1, the unit can remove cursed items from their inventory. | 2 | 1 |
| [`FreePathfindElement`](./Enums.md) | Enum | Specifies a terrain element that the unit can pathfind through without penalty. | 2 | Water |
| [`MoveAwayFromDamageSource`](./Enums.md) | Enum | Specifies the ability used by the unit to move away from the source of damage. | 2 | BasicJump |
| [`PassiveWhenAtFullMana`](#object-passivewhenatfullmana) | Object | Grants additional passive effects when the unit's mana is full. | 2 ||
| [`PassiveWhileHasStatus`](#object-passivewhilehasstatus) | Object | Grants additional passive effects while the unit is afflicted with a specified status. | 2 ||
| [`PoopWhenHit`](./Enums.md) | Enum | Specifies the object dropped when the unit is hit, optionally with a chance. | 2 | Poop |
| [`StatusKilledCharacters`](#object-statuskilledcharacters) | Object | Defines statuses applied to characters killed by the unit, or to the unit itself upon kill. | 2 ||
| [`BackflipWhenTargeted`](Abilities_and_Spells.md#object-backflipwhentargeted) | Object | The number of stacks of BackflipWhenTargeted or an object defining the dodge ability; causes the unit to perform a backflip dodge when targeted. | 1 ||
| [`BasicAttackCantMiss`](./Enums.md) | Integer | If set to 1, the unit's basic attacks cannot miss. | 1 | 1 |
| [`BlacklistPickupType`](./Enums.md) | Enum | Specifies the type of pickup that the unit cannot collect. | 1 | catnip |
| [`Blind`](./Enums.md) | Array / Integer | The number of stacks of Blind to apply, reducing accuracy; can be an array `[stacks, probability]` for a chance-based application. | 1 | [.10] |
| [`ConjureBonusAbility`](./Enums.md) | Enum | Specifies the bonus ability that the unit gains, either by class or by specific ability name. | 1 | random |
| [`DisableAbilitiesWithTag`](./Enums.md) | Enum | Specifies the tag of abilities that are disabled for the unit. | 1 | consumable |
| [`HouseFoodRequirementMultiplier`](./Enums.md) | Integer | Multiplier for the food required by the house. A value of 0 may remove the requirement. | 1 | 0 |
| [`MakeBasicAttackPull`](./Enums.md) | Integer | If set to 1, the unit's basic attacks pull the target closer. | 1 | 1 |
| [`ShowHiddenThings`](./Enums.md) | Integer | If non-zero, reveals hidden things (e.g., traps, secrets) on the map. | 1 | 1 |
| [`Slow`](./Enums.md) | Array / Integer | The number of turns of Slow applied, or an array with duration and chance. | 1 | [.1] |
| [`SpawnOnDowned`](./Enums.md) | Enum | Specifies the entity (e.g., CharmedSpookie) to spawn when this unit is downed. | 1 | CharmedFly |
| [`StatusEachRoundEnd`](#object-statuseachroundend) | Object | Defines effects that trigger at the end of each round for the unit. | 1 ||
| [`Vegan`](./Enums.md) | Integer | If non-zero (or defined as an object), applies the Vegan disorder, preventing the unit from consuming meat-based items. | 1 | 1 |

</details>

---

### Object: `AddStatusToBasicAttack`


**Definition:** Injects a status effect payload that applies whenever the character performs a basic attack.  
**Total Count:** 52


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root), [`passives`](./Cat_Mutations.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 205 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 56 |
| [`Bleed`](./Enums.md) | Array / Integer | The number of Bleed stacks applied, which deals bleeding damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 30 | [3] |
| [`Poison`](./Enums.md) | Integer | The number of Poison stacks applied, which deals poison damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 29 | 1 |
| [`Knockback`](./Enums.md) | Integer | The number of tiles the target is knocked back. | 24 | 2 |
| [`Burn`](./Enums.md) | Integer | The number of Burn stacks applied, which deals fire damage over time; can be an integer, a variable X, or an array `[stacks, probability]` to specify chance of application. | 16 | 1 |
| [`Fear`](./Enums.md) | Array | The number of Fear stacks applied, which reduces the target's accuracy and may cause it to flee; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 13 | [.15] |
| [`Bruise`](./Enums.md) | Integer | The number of Bruise stacks applied, or an array with duration and chance. | 12 | 2 |
| [`ChangeTile`](./Enums.md) | Enum | Specifies the tile type to change the target's tile into (e.g., BrambleTile, LavaTile). | 10 | WaterTile |
| [`Slow`](./Enums.md) | Array / Integer | The number of turns of Slow applied, or an array with duration and chance. | 10 | [.1] |
| [`Stun`](./Enums.md) | Array | The number of Stun stacks applied, which prevents the target from taking actions; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 8 | [.05] |
| [`Confusion`](./Enums.md) | Array / Integer | The number of turns of Confusion applied, or an array with duration and chance. | 7 | [2] |
| [`Freeze`](./Enums.md) | Array | The number of stacks of Freeze, immobilizing the unit for that many turns; can be an array `[stacks, probability]`. | 4 | [0.15] |
| [`Leeches`](./Enums.md) | Integer | The number of Leech stacks applied, healing the attacker. | 4 | 1 |
| [`SoulLink`](./Enums.md) | Integer | The number of turns the linked status lasts, sharing damage between linked units. | 4 | 1 |
| [`Charmed`](./Enums.md) | Array | The number of turns of Charmed applied, or an array with duration and chance. | 3 | [.15] |
| [`VisualFXTile`](./Enums.md) | Enum | Specifies the visual effect to play on the target tile. | 2 | fx_windSpell |
| [`FaceAway`](./Enums.md) | Integer | If non-zero, forces the target to face away from the attacker. | 1 | 1 |
| [`FlatLeech`](./Enums.md) | Integer | The amount of flat health restored per hit (leech). | 1 | 1 |
| [`Immobile`](./Enums.md) | Array / Integer | The number of turns of Immobile applied, or an array with duration and chance. | 1 | [.05] |
| [`Instakill`](./Enums.md) | Array | If an integer, the percentage chance to instantly kill the target. If an array [stacks, probability], applies that many stacks with the given probability per stack. | 1 | [25] |
| [`Petrify`](./Enums.md) | Array | The number of stacks of Petrify, turning the unit to stone and immobilizing it; can be an array `[stacks, probability]`. | 1 | [.05] |
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object | An object listing possible status effects to randomly pick from and apply. | 1 ||
| [`VaporizeInanimate`](./Enums.md) | Integer | The number of stacks of Vaporize applied to inanimate objects. | 1 | 1 |
| [`Webbed`](./Enums.md) | Array | The number of Webbed stacks applied, which immobilizes the target and prevents movement; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | [.1] |

</details>

---

### Object: `PassiveWhenAffectedByElement`


**Definition:** Examples: `{ ... }`  
**Total Count:** 12


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root), [`passives`](./Cat_Mutations.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Array / Enum | Examples: `water` | 18 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 18 ||
| [`passives`](#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 18 ||

</details>

---

### Object: `effects`
### Object: `effects`

**Definition:** Non-damaging status applications and logic triggers executed on impact.  
**Total Count:** 10


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeleeRevengeDamage`](./Cat_Mutations.md#context-meleerevengedamage), [`RevengeDamage`](./Cat_Mutations.md#context-revengedamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 1695 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 750 |
| [`Confusion`](./Enums.md) | Array / Integer | The number of turns of Confusion applied, or an array with duration and chance. | 37 | [2] |
| [`Fear`](./Enums.md) | Array | The number of Fear stacks applied, which reduces the target's accuracy and may cause it to flee; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 31 | [.15] |
| [`Blind`](./Enums.md) | Array / Integer | The number of stacks of Blind to apply, reducing accuracy; can be an array `[stacks, probability]` for a chance-based application. | 24 | [.10] |
| [`Charmed`](./Enums.md) | Array | The number of turns of Charmed applied, or an array with duration and chance. | 22 | [.15] |
| [`Petrify`](./Enums.md) | Array | The number of stacks of Petrify, turning the unit to stone and immobilizing it; can be an array `[stacks, probability]`. | 15 | [.05] |
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object | An object listing possible status effects to randomly pick from and apply. | 14 ||

</details>

---

### Object: `RevengeDamage`


**Definition:** Reaction trigger: Deals damage to the attacker when hit.  
**Total Count:** 9


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 31 ||
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Defines the effects (e.g., statuses, damage) applied by the revenge damage. | 29 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 29 |
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Examples: `0` | 8 ||
| [`type`](./Enums.md#enum-type) | Enum | Examples: `status` | 5 ||

</details>

---

### Object: `MeleeRevengeDamage`


**Definition:** Reaction trigger: Applies nested status effects to the attacker when hit by a melee attack.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 70 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 49 |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Defines the effects (e.g., statuses, damage) applied by the revenge damage. | 47 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 43 ||
| `knockback` | Enum / Integer | Examples: `2, 1` | 24 ||
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Examples: `0` | 22 ||
| [`type`](./Enums.md#enum-type) | Enum | Examples: `status` | 10 ||
| [`Freeze`](./Enums.md) | Array | The number of stacks of Freeze, immobilizing the unit for that many turns; can be an array `[stacks, probability]`. | 1 | [0.15] |
| [`Immobile`](./Enums.md) | Array / Integer | The number of turns of Immobile applied, or an array with duration and chance. | 1 | [.05] |

</details>

---

### Object: `SpawnThingOnDamage`


**Definition:** Applies or references the 'SpawnThingOnDamage' effect/state.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum | Examples: `CharmedFlea, SmallRock, Coin` | 38 ||
| `good` | Boolean | Examples: `false` | 20 ||
| `chance` | Number | Examples: `20, 100, 10` | 12 ||

</details>

---

### Object: `AddStatusToBasicMeleeAttack`


**Definition:** Examples: `{ ... }`  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 9 ||
| [`Bleed`](./Enums.md) | Array / Integer | The number of Bleed stacks applied, which deals bleeding damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 2 | [3] |
| [`Knockback`](./Enums.md) | Integer | The number of tiles the target is knocked back. | 2 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`Immobile`](./Enums.md) | Array / Integer | The number of turns of Immobile applied, or an array with duration and chance. | 1 | [.05] |
| [`KnockUpAndAway`](Abilities_and_Spells.md#object-knockupandaway) | Object | Defines a knockback that launches the target up and away, with optional distance and stacks. | 1 ||

</details>

---

### Object: `StatusOnTookDamage`


**Definition:** Event Trigger: Applies nested statuses when took damage.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 38 ||
| [`Charge`](./Enums.md) | Integer | The number of stacks of Charge, which makes the caster gain 1 Mana per stack at the start of its next turn. | 8 | 2 |
| [`ChangeTilesUnder`](./Enums.md) | Enum | Determines which tile type (e.g., GlassTile, DirtTile) replaces the tiles beneath the target. | 2 | GlassTile |
| [`LuckUp`](./Enums.md) | Integer | Specifies the number of Luck stacks applied, where positive values increase critical hit chance and loot quality and negative values decrease them. | 1 | 1 |

</details>

---

### Object: `StatusEachTurnBegin`


**Definition:** Event Trigger: Applies nested statuses to each turn begin.  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 24 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| [`Quivered`](./Enums.md) | Array / Integer | The number of stacks of Quivered, which grants bonus attacks; can be an array [stacks, probability]. | 2 | [0.1] |
| [`SpeedUp`](./Enums.md) | Integer | Specifies the number of Speed stacks applied, where each stack modifies the unit's turn order and dodge chance. | 2 | 1 |
| [`MissChance`](./Enums.md) | Integer | The percentage chance that the unit's attacks will miss. | 1 | 20 |
| [`MoveQuivered`](./Enums.md) | Array | Specifies the number of bonus movement points granted; an array `[stacks, probability]` specifies the amount and its chance of application. | 1 | [0.1] |

</details>

---

### Object: `RandomStatusFromPool`


**Definition:** Selects and applies a random status effect from the provided nested object.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Cat_Mutations.md#context-addstatustobasicattack), [`StatusOnTookDamageFromAbility`](./Cat_Mutations.md#context-statusontookdamagefromability), [`effects`](./Cat_Mutations.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 33 ||
| [`Shield`](./Enums.md) | Integer | Specifies the number of Shield stacks applied, where each stack reduces incoming damage by a flat amount. | 12 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 12 |
| [`Thorns`](./Enums.md) | Integer | The number of Thorns stacks applied, which deals damage back to melee attackers. | 10 | 2 |
| [`KineticSpikes`](./Enums.md) | Integer | The number of Kinetic Spikes stacks applied, which deal damage back to attackers when the unit is hit. | 9 | 1 |
| [`Poison`](./Enums.md) | Integer | The number of Poison stacks applied, which deals poison damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 9 | 1 |
| [`Bleed`](./Enums.md) | Array / Integer | The number of Bleed stacks applied, which deals bleeding damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 8 | [3] |
| [`Charge`](./Enums.md) | Integer | The number of stacks of Charge, which makes the caster gain 1 Mana per stack at the start of its next turn. | 8 | 2 |
| [`Weakness`](./Enums.md) | Integer | The number of Weakness stacks applied, which increases damage taken by the target; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 8 | 1 |
| [`Blind`](./Enums.md) | Array / Integer | The number of stacks of Blind to apply, reducing accuracy; can be an array `[stacks, probability]` for a chance-based application. | 6 | [.10] |
| [`DiminishingHealthRegen`](./Enums.md) | Integer | The number of stacks of DiminishingHealthRegen, providing health regeneration each turn that decreases with each stack. | 6 | 1 |
| [`Burn`](./Enums.md) | Integer | The number of Burn stacks applied, which deals fire damage over time; can be an integer, a variable X, or an array `[stacks, probability]` to specify chance of application. | 5 | 1 |
| [`RandomStatUp`](./Enums.md) | Integer | The amount of random stat increase (or decrease if negative) applied to a random stat. | 5 | 2 |

</details>

---

### Object: `SpawnEachTurn`


**Definition:** Applies or references the 'SpawnEachTurn' effect/state.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum | Examples: `RandomPickup, CharmedFly, CharmedMaggot` | 22 ||
| `chance` | Number | Examples: `50, 5, 25` | 20 ||
| `good` | Boolean | Examples: `false` | 2 ||

</details>

---

### Object: `StatusEachTurnEnd`


**Definition:** Applies or references the 'StatusEachTurnEnd' effect/state.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root), [`passives`](./Cat_Mutations.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 55 ||
| [`Shield`](./Enums.md) | Integer | Specifies the number of Shield stacks applied, where each stack reduces incoming damage by a flat amount. | 5 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 5 |
| [`RandomStatUp`](./Enums.md) | Integer | The amount of random stat increase (or decrease if negative) applied to a random stat. | 3 | 2 |
| [`IntelligenceUp`](./Enums.md) | Integer | The amount of intelligence increase, which can be a fixed integer or a mathematical expression. | 2 | 1 |
| [`Charge`](./Enums.md) | Integer | The number of stacks of Charge, which makes the caster gain 1 Mana per stack at the start of its next turn. | 1 | 2 |
| [`RandomStatDown`](./Enums.md) | Integer | The number of stacks or chance to decrease a random stat; can be an array `[stacks, probability]` or a formula. | 1 | 1 |

</details>

---

### Object: `SpawnOnBattleStartRandomEmptyTile`


**Definition:** Applies or references the 'SpawnOnBattleStartRandomEmptyTile' effect/state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum | Examples: `Coin, RandomFoodPickup` | 11 ||
| [`number`](./Arrays.md#array-number) | Array / Integer | Examples: `[ 1 3 ], 2` | 10 ||

</details>

---

### Object: `Conditional_RandomChance`


**Definition:** Conditional trigger: Executes nested logic based on a flat percentage random roll.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusKilledCharacters`](./Cat_Mutations.md#context-statuskilledcharacters)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `odds` | Number | Examples: `10` | 4 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |
| [`AutoReanimate`](./Enums.md) | Integer | The percentage chance to automatically revive a killed character. | 2 | 50 |

</details>

---

### Object: `StatusEveryXSpellCasts`


**Definition:** Applies or references the 'StatusEveryXSpellCasts' effect/state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Examples: `4, 8` | 8 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 8 ||
| [`Charge`](./Enums.md) | Integer | The number of stacks of Charge, which makes the caster gain 1 Mana per stack at the start of its next turn. | 2 | 2 |
| [`RandomMagicMissile`](./Enums.md) | Integer | The number of random magic missiles fired, each dealing independent damage; can also be an object with custom tooltip data. | 1 | 4 |

</details>

---

### Object: `StatusKilledCharacters`


**Definition:** Event Trigger: Applies nested statuses to killed characters.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusOnBattleEnd`


**Definition:** Applies the nested status effects when the encounter finishes.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 52 ||
| [`FindItemFromPool`](./Enums.md) | Enum | Determines the item pool name from which a random item is granted to the source. | 8 | consumables |
| [`PermanentIntelligence`](./Enums.md) | Integer | The number of permanent intelligence stat points added or subtracted. | 3 | 1 |

</details>

---

### Object: `StatusOnEndMove`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusOnTookDamageFromAbility`


**Definition:** Event Trigger: Applies statuses when taking damage from an ability.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 8 ||
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object | An object listing possible status effects to randomly pick from and apply. | 2 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Object: `AbilityWhenTaggedCharacterMovesNear`


**Definition:** AI Trigger: Executes an ability when a character with a specific tag moves adjacent.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Examples: `move` | 5 ||
| `range` | Enum / Integer | Examples: `2` | 5 ||
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Examples: `food` | 5 ||

</details>

---

### Object: `AddDamageToElementDamage`


**Definition:** Applies or references the 'AddDamageToElementDamage' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Examples: `1` | 9 ||
| [`element`](./Enums.md#enum-element) | Array / Enum | Examples: `Electric` | 9 ||

</details>

---

### Object: `AddTemporaryEffectsToBasicAttack`


**Definition:** Applies the 'AddTemporaryEffectsToBasicAttack' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Fury` | Integer | Examples: `10` | 4 ||

</details>

---

### Object: `BackflipWhenTargeted`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Examples: `BackflipDodge` | 7 ||
| `stacks` | Enum / Integer | Examples: `2` | 7 ||

</details>

---

### Object: `ChanceToBackflip`


**Definition:** Applies or references the 'ChanceToBackflip' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Examples: `BackflipDodge` | 6 ||
| `chance` | Number | Examples: `10` | 6 ||

</details>

---

### Object: `ClassManaCostReduction`


**Definition:** Applies or references the 'ClassManaCostReduction' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `reduction` | Integer | Examples: `1` | 7 ||
| [`class`](./Enums.md#enum-class) | Enum | Examples: `Colorless` | 6 ||

</details>

---

### Object: `Conditional_FirstApplicationThisTurn`


**Definition:** Conditional trigger: Executes nested logic only if this is the first time this specific effect has been applied this turn.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnEndMove`](./Cat_Mutations.md#context-statusonendmove)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 8 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution. | 3 | |
| [`Charge`](./Enums.md) | Integer | The number of stacks of Charge, which makes the caster gain 1 Mana per stack at the start of its next turn. | 1 | 2 |

</details>

---

### Object: `Conditional_GoodRoll`


**Definition:** Conditional trigger: Executes nested logic based on a randomized favorable outcome probability.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnEndMove`](./Cat_Mutations.md#context-statusonendmove)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `odds` | Number | Examples: `25` | 37 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution. | 37 | |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 28 ||
| [`ChangeTilesUnder`](./Enums.md) | Enum | Determines which tile type (e.g., GlassTile, DirtTile) replaces the tiles beneath the target. | 1 | GlassTile |

</details>

---

### Object: `CounterAttack`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Examples: `ChainLightning` | 5 ||
| `chance` | Number | Examples: `15` | 1 ||

</details>

---

### Object: `KnockUpAndAway`


**Definition:** Displaces the target vertically and horizontally away from the source.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicMeleeAttack`](./Cat_Mutations.md#context-addstatustobasicmeleeattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `distance` | Integer | Examples: `3` | 24 ||
| `stacks` | Enum / Integer | Examples: `3` | 22 ||

</details>

---

### Object: `MoveWhenDamaged`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`weights`](./Enums.md#enum-weights) | Array / Enum | Examples: `chaotic` | 9 ||
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | Examples: `MoveOne` | 2 ||

</details>

---

### Object: `PassiveWhenAtFullMana`


**Definition:** State Trigger: Grants nested passives when at full mana.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 5 ||
| [`DamageUp`](./Enums.md) | Integer | The amount of damage increase, or a string formula for dynamic calculation. | 1 | 2 |

</details>

---

### Object: `PassiveWhileHasStatus`


**Definition:** Passive: Activates only while the character has the specified status.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | Examples: `Bleed` | 6 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 6 ||
| [`passives`](#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 6 ||

</details>

---

### Object: `SpawnExtraThingsOnBattleStart`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`number`](./Arrays.md#array-number) | Array / Integer | Examples: `[ 1 2 ]` | 31 ||
| [`object`](./Enums.md#enum-object) | Array / Enum | Examples: `RandomPickup` | 23 ||

</details>

---

### Object: `StatusEachRoundEnd`


**Definition:** Applies or references the 'StatusEachRoundEnd' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 1 ||
| [`UseAbility`](./Enums.md) | Enum | Specifies the ability name the unit will use at the end of each round. | 1 | Spit |

</details>

---

### Object: `StatusEveryXSpellCastsEachTurn`


**Definition:** Examples: `{ ... }`  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Examples: `3` | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 1 ||
| [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 1 | 2 |

</details>

---

### Object: `StatusIfDidntMove`


**Definition:** Examples: `{ ... }`  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 1 ||
| [`Charge`](./Enums.md) | Integer | The number of stacks of Charge, which makes the caster gain 1 Mana per stack at the start of its next turn. | 1 | 2 |

</details>

---

### Object: `StatusIfUnusedMovePoints`


**Definition:** Event Trigger: Applies nested statuses to if unused move points.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 8 ||
| [`ManaGain`](./Enums.md) | Integer | The amount of mana gained; can be a fixed integer or a formula using variables like `X` (e.g., damage dealt or ability cost). | 2 | 3 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `StatusOnAllyCatDeath`


**Definition:** Event Trigger: Applies nested statuses when ally cat death.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 6 ||
| [`DamageUp`](./Enums.md) | Integer | The amount of damage increase, or a string formula for dynamic calculation. | 1 | 2 |

</details>

---

### Object: `StatusOnCastSpell`


**Definition:** Event Trigger: Applies nested statuses when cast spell.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 8 ||
| [`Charge`](./Enums.md) | Integer | The number of stacks of Charge, which makes the caster gain 1 Mana per stack at the start of its next turn. | 4 | 2 |

</details>

---

### Object: `StatusOnDie`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 9 ||
| [`ScatterCoins`](./Enums.md) | Array / Integer | The number of coins scattered, or an object with stacks and stacking behavior. | 1 | [.5] |

</details>

---

### Object: `StatusOnEatFood`


**Definition:** Event Trigger: Applies nested statuses when eat food.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 5 ||
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of health regeneration (HealthRegen) granted by this damage instance. | 1 | 2 |

</details>

---

### Object: `StatusOnKill`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 34 ||
| [`RangeUp`](./Enums.md) | Integer | The amount of bonus range added to the unit's attacks. Each stack adds one tile of range. | 1 | 1 |

</details>

---


<details>
<summary><b>Conditional_RandomChance</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 34 ||

</details>

<details>
<summary><b>StatusKilledCharacters</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 34 ||

</details>

<details>
<summary><b>StatusOnEndMove</b></summary>

> **Total Count:** 9

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 34 ||

</details>
