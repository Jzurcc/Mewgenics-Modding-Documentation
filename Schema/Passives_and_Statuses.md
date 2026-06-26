# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Passives & Statuses

> **Associated Files:** `data/passives/, data/passive_pools.gon`


### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 885

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Strings.md#string-name) | Enum | Localization key for the passive's display name. | 3307 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2985 |  |
| [`desc`](./Strings.md#string-desc) | Enum | Localization key for the passive's display description. | 2423 |  |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1910 ||
| [`class`](./Enums.md#enum-class) | Enum | Character class identifier. | 600 |  |
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Defines the unit's base stats (strength, dexterity, constitution, intelligence, speed). | 461 ||
| [`tags`](./Arrays.md#array-tags) | Array / Enum | Array of gameplay-relevant tags for item or unit categorization (e.g., 'consumable', 'cat'). | 241 ||
| `shield` | Enum / Integer | The unit's shield value, specified as an integer or a formula. | 191 ||
| `cha` | Enum / Integer | Specifies the charisma stat value as an integer or 'aux' for auxiliary stat assignment. | 89 ||
| `con` | Enum / Integer | The constitution stat value or modifier for the unit. | 79 ||
| `spd` | Enum / Integer | The speed stat value or modifier for the unit. | 78 ||
| `int` | Enum / Integer || 66 ||
| `lck` | Enum / Integer || 53 ||
| `str` | Enum / Integer || 45 ||
| `dex` | Enum / Integer || 30 ||
| [`keyword_tooltips`](Abilities_and_Spells.md#object-keyword_tooltips) | Object | Examples: `{ ... }` | 28 ||
| `divine_shield` | Integer | Examples: `3, 1` | 20 ||
| `CritChanceUp` | Integer | The amount of critical hit chance increase, in percentage points. | 18 | `[1 .5]` (Array), `1` (Number), `50` (Number), `{ ... }` (Object) |
| `Thorns` | Integer | The number of Thorns stacks applied, which deals damage back to melee attackers. | 18 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`lock_item_slot`](Miscellaneous.md#object-lock_item_slot) | Object || 16 ||
| `MissChance` | Integer | The percentage chance that the unit's attacks will miss. | 12 | `[1 .5]` (Array), `1` (Number), `20` (Number), `{ ... }` (Object) |
| [`name_mod`](./Strings.md#string-name_mod) | String || 11 ||
| [`SpawnOnBattleStart`](Elite_Buffs.md#object-spawnonbattlestart) | Enum / Object | Specifies the object (e.g., Food, CharmedGamete) to spawn at the start of battle. | 9 | `ZombieCatFamiliar` (Enum), `BeefyCharmedLeech` (Enum), `{ ... }` (Object) |
| `Trample` | Integer | The number of tiles this character can move through enemies, dealing damage or applying effects equal to the value. | 7 | `[1 .5]` (Array), `[3 X-8]` (Array), `1` (Number), `6` (Number), `{ ... }` (Object) |
| [`override_basic_attack`](./Enums.md#enum-override_basic_attack) | Enum || 6 ||
| [`BoostWeaponDamage`](Items_and_Equipment.md#object-boostweapondamage) | Object | Increases the damage dealt by the unit's weapon. | 5 | `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Quivered` | Array / Integer | The number of stacks of Quivered, which grants bonus attacks; can be an array [stacks, probability]. | 5 | `[1 0.1]` (Array), `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`desc_multiclass`](./Strings.md#string-desc_multiclass) | String || 5 ||
| [`bonus_items`](./Arrays.md#array-bonus_items) | Array | Flat addition to a base value. | 5 ||
| `AmplifyStatus` | Enum || 4 | `Burn` (Enum), `Poison` (Enum), `{ ... }` (Object) |
| `BleedThorns` | Integer | The number of Bleed Thorns stacks applied, which deals bleeding damage back to melee attackers. | 4 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `StatusImmunity` | Array / Enum | List of status effects the unit is immune to. | 4 | `[Burn]` (Array), `[Freeze Slow]` (Array), `Burn` (Enum), `Webbed` (Enum) |
| `auto_plus_signs_on_name` | Boolean || 4 ||
| [`BlastResistance`](#object-blastresistance) | Array / Number / Object || 3 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Blind` | Array / Integer | The number of stacks of Blind to apply, reducing accuracy; can be an array `[stacks, probability]` for a chance-based application. | 3 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `KineticSpikes` | Integer | The number of Kinetic Spikes stacks applied, which deal damage back to attackers when the unit is hit. | 3 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `MoveQuivered` | Integer | Specifies the number of bonus movement points granted; an array `[stacks, probability]` specifies the amount and its chance of application. | 3 | `[1 0.1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `PoisonThorns` | Integer | Applies Poison stacks to any unit that attacks this unit in melee. | 3 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `YOffset` | Number | A vertical offset multiplier used to adjust the unit's visual position on the tile. | 3 | `-.18` (String), `.25` (String) |
| [`AbilityReaction`](Characters_and_Bosses.md#object-abilityreaction) | Enum / Object | Specifies an ability to trigger as a reaction when certain conditions are met. | 2 | `SCSneakUp` (Enum), `attack` (Enum), `{ ... }` (Object) |
| [`CounterAttack`](Cat_Mutations.md#object-counterattack) | Array / Enum / Object | Specifies the ability name used for counterattacking when hit. | 2 | `[attack GSScream]` (Array), `Shove` (Enum), `YeticatSnowball_Counter` (Enum), `{ ... }` (Object) |
| `Immobile` | Array / Integer | The number of turns of Immobile applied, or an array with duration and chance. | 2 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `10` (Number), `{ ... }` (Object) |
| [`PoopWhenHit`](Items_and_Equipment.md#object-poopwhenhit) | Object | Specifies the object dropped when the unit is hit, optionally with a chance. | 2 | `Poop` (Enum), `{ ... }` (Object) |
| [`ReflectProjectiles`](Characters_and_Bosses.md#object-reflectprojectiles) | Integer / Object | The percentage chance to reflect projectiles back at the attacker. | 2 | `1` (Number), `100` (Number), `{ ... }` (Object) |
| `SizeScale` | Number | A multiplier for the unit's visual size. Values above 1 increase size, values below 1 decrease size. | 2 | `1.1` (Number), `1.3` (Number), `.6` (String), `.75` (String) |
| [`empty_armor_scaled_stats`](Miscellaneous.md#object-empty_armor_scaled_stats) | Object | Examples: `{ ... }` | 2 ||
| [`Vegan`](#object-vegan) | Number / Object | If non-zero (or defined as an object), applies the Vegan disorder, preventing the unit from consuming meat-based items. | 2 | `1` (Number), `{ ... }` (Object) |
| [`AfterImage`](Abilities_and_Spells.md#object-afterimage) | Object | An object defining an afterimage entity (e.g., PlayerCat_ThiefShade) that appears when the character moves. | 1 | `PlayerCat_ThiefShade2` (Enum), `PlayerCat_ThiefShade` (Enum), `{ ... }` (Object) |
| [`AllyBonusAbilityAura`](Miscellaneous.md#object-allybonusabilityaura) | Enum / Object || 1 | `NubbyToss` (Enum), `{ ... }` (Object) |
| `AlphaCat` | Integer | The number of stacks of the AlphaCat status effect. | 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`AutocastEachTurnBegin`](Miscellaneous.md#object-autocasteachturnbegin) | Enum / Object || 1 | `MindCrack_EldritchVisage2` (Enum), `MindCrack_EldritchVisage` (Enum), `{ ... }` (Object) |
| [`BackflipWhenTargeted`](Abilities_and_Spells.md#object-backflipwhentargeted) | Enum / Integer / Object | The number of stacks of BackflipWhenTargeted or an object defining the dodge ability; causes the unit to perform a backflip dodge when targeted. | 1 | `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `BackstabCritChance` | Number || 1 | `1` (Number), `.25` (String) |
| [`BoostDamageGlobalAura`](#object-boostdamageglobalaura) | Array / Number / Object || 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`BraceForEachNeighboringEnemy`](#object-braceforeachneighboringenemy) | Array / Number / Object || 1 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`ChainKnockback`](#object-chainknockback) | Number / Object || 1 | `1` (Number), `{ ... }` (Object) |
| [`ChanceToBlockAndCounter`](Items_and_Equipment.md#object-chancetoblockandcounter) | Integer / Object || 1 | `15` (Number), `33` (Number), `{ ... }` (Object) |
| [`ChanceToRevive`](Elite_Buffs.md#object-chancetorevive) | Integer / Object || 1 | `100` (Number), `25` (Number), `{ ... }` (Object) |
| [`CharmAllFlies`](#object-charmallflies) | Array / Number / Object || 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`CollectPickupsOnBattleEnd`](Miscellaneous.md#object-collectpickupsonbattleend) | Number / Object || 1 | `1` (Number), `{ ... }` (Object) |
| [`Conductor`](#object-conductor) | Boolean (Flag) / Number / Object || 1 | `(Flag)` (Boolean (Flag)), `2` (Number), `{ ... }` (Object) |
| [`ConjureBonusAbility`](Abilities_and_Spells.md#object-conjurebonusability) | Enum / Object | Specifies the bonus ability that the unit gains, either by class or by specific ability name. | 1 | `Class` (Enum), `Mage` (Enum), `{ ... }` (Object) |
| [`DamageReductionAura`](Miscellaneous.md#object-damagereductionaura) | Array / Number / Object || 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`DeathChill`](#object-deathchill) | Number / Object || 1 | `1` (Number), `{ ... }` (Object) |
| [`DeathRattle`](Characters_and_Bosses.md#object-deathrattle) | Enum / Object | Defines an ability or explosion that triggers upon the unit's death. | 1 | `BoomerCatExplode` (Enum), `BombFlyExplode` (Enum), `{ ... }` (Object) |
| [`DejaVu`](#object-dejavu) | Number / Object || 1 | `10` (Number), `{ ... }` (Object) |
| `DepressionAura` | Integer | The number of Depression stacks applied to nearby units as an aura. | 1 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`DirtyClaws`](#object-dirtyclaws) | Number / Object || 1 | `1` (Number), `{ ... }` (Object) |
| [`DukeOfFlies`](#object-dukeofflies) | Number / Object || 1 | `1` (Number), `{ ... }` (Object) |
| [`Empath`](#object-empath) | Number / Object || 1 | `50` (Number), `100` (Number), `{ ... }` (Object) |
| [`EnergyStorm`](Miscellaneous.md#object-energystorm) | Number / Object || 1 | `3` (Number), `{ ... }` (Object) |
| [`FlyDamageIncrease`](Items_and_Equipment.md#object-flydamageincrease) | Object || 1 | `[1 .5]` (Array), `1` (Number), `4` (Number), `{ ... }` (Object) |
| `Flying` | Integer | The number of stacks of the Flying status effect applied to the unit. | 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`FollowUp`](#object-followup) | Enum / Object || 1 | `FollowUpDash` (Enum), `FollowUpDash2` (Enum), `{ ... }` (Object) |
| [`FullPower`](#object-fullpower) | Number / Object || 1 | `3` (Number), `{ ... }` (Object) |
| [`HealingAura`](#object-healingaura) | Number / Object || 1 | `1` (Number), `{ ... }` (Object) |
| [`ImmortalLeeches`](#object-immortalleeches) | Number / Object || 1 | `1` (Number), `{ ... }` (Object) |
| [`KillsHeal`](#object-killsheal) | Number / Object || 1 | `5` (Number), `50` (Number), `{ ... }` (Object) |
| [`LateBloomer`](Miscellaneous.md#object-latebloomer) | Array / Number / Object || 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `LineOfSightTrueSightAura` | Number / String || 1 | `0` (Number), `.5` (String) |
| [`LowHealthAllyDodgeChanceAura`](Miscellaneous.md#object-lowhealthallydodgechanceaura) | Array / Number / Object || 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`MegaMinions`](Miscellaneous.md#object-megaminions) | Number / Object || 1 | `3` (Number), `{ ... }` (Object) |
| `Metal` | Integer || 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`MetalDetector`](#object-metaldetector) | Number / Object || 1 | `5` (Number), `10` (Number), `{ ... }` (Object) |
| [`MoveAwayFromDamageSource`](Characters_and_Bosses.md#object-moveawayfromdamagesource) | Object | Specifies the ability used by the unit to move away from the source of damage. | 1 | `MoveOne` (Enum), `BasicJump` (Enum), `{ ... }` (Object) |
| [`MoveTowardsDamageSource`](Characters_and_Bosses.md#object-movetowardsdamagesource) | Enum / Object | Causes the unit to move towards the source of damage, using a specified move ability. | 1 | `MoveOne` (Enum), `{ ... }` (Object) |
| [`MoveWhenDamaged`](Cat_Mutations.md#object-movewhendamaged) | Enum / Object | Defines movement behavior triggered when the unit takes damage, including the ability to use and movement weights. | 1 | `TKNG_Hop` (Enum), `move` (Enum), `{ ... }` (Object) |
| [`NumbingLeeches`](#object-numbingleeches) | Number / Object || 1 | `3` (Number), `{ ... }` (Object) |
| [`ProtectTargetedAllies`](Characters_and_Bosses.md#object-protecttargetedallies) | Object | Configures protection behavior for allies being targeted, using a specified ability or action. | 1 | `SwapPositions_WideLoad2` (Enum), `SwapPositions_WideLoad` (Enum), `{ ... }` (Object) |
| [`Quiver`](#object-quiver) | Number / Object || 1 | `2` (Number), `1` (Number), `{ ... }` (Object) |
| `RandomStatUp` | Integer / String | The amount of random stat increase (or decrease if negative) applied to a random stat. | 1 | `"ceil(X/3)"` (Enum), `"ceil(X/2)"` (Enum), `2` (Number), `-5` (Number) |
| [`Robot`](Characters_and_Bosses.md#object-robot) | Integer / Object | Marks the unit as a robot. An integer enables the passive; an object can specify alternate energized effects or allow self-energize. | 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`SharePickups`](Characters_and_Bosses.md#object-sharepickups) | Object | If set, the unit shares pickups with allies, optionally including coins. | 1 | `1` (Number), `{ ... }` (Object) |
| [`ShoulderCheck`](#object-shouldercheck) | Number / Object || 1 | `100` (Number), `33` (Number), `{ ... }` (Object) |
| [`ShovingMatch`](#object-shovingmatch) | Enum / Object || 1 | `attack` (Enum), `{ ... }` (Object) |
| [`SpawnExtraThingsOnBattleStart`](Cat_Mutations.md#object-spawnextrathingsonbattlestart) | Object | Spawns specified objects, tiles, or traps at the start of battle. | 1 | `{ ... }` (Object) |
| [`SpawnObjectOnPopCorpse`](Items_and_Equipment.md#object-spawnobjectonpopcorpse) | Enum / Object || 1 | `Coin` (Enum), `Catnip` (Enum), `{ ... }` (Object) |
| `Stealth` | Array / Integer | The number of turns the unit is invisible, or [stacks, probability] of gaining stealth. | 1 | `[1 .1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| [`schadenfreude_scaled_stats`](Miscellaneous.md#object-schadenfreude_scaled_stats) | Object | Examples: `{ ... }` | 1 ||
| [`grant_ability`](./Enums.md#enum-grant_ability) | Enum || 1 ||
| [`StrengthForEachNeighboringEnemy`](#object-strengthforeachneighboringenemy) | Array / Number / Object || 1 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`StrengthInNumbersAura`](Miscellaneous.md#object-strengthinnumbersaura) | Number / Object || 1 | `1` (Number), `{ ... }` (Object) |
| [`Study`](Miscellaneous.md#object-study) | Number / Object || 1 | `1` (Number), `{ ... }` (Object) |
| `SwapHighestAndLowestStat` | Integer || 1 | `1` (Number) |
| `Tech` | Integer | The number of Tech stacks applied, which increase the damage of the next ability used. | 1 | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| [`TileDamageMultiplier`](Miscellaneous.md#object-tiledamagemultiplier) | Number / Object || 1 | `2` (Number), `{ ... }` (Object) |
| [`Vengeful`](#object-vengeful) | Number / Object || 1 | `1` (Number), `{ ... }` (Object) |
| [`Weakness`](#object-weakness) | Array / Integer / Object | The number of Weakness stacks applied, which increases damage taken by the target; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

### Object: `passives`


**Definition:** Object listing intrinsic passive modifiers.  
**Total Count:** 884


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveAfterXKills`](./Passives_and_Statuses.md#context-passiveafterxkills), [`PassiveAtHealthThreshold`](./Passives_and_Statuses.md#context-passiveathealththreshold), [`PassiveAtInjuryThreshold`](./Passives_and_Statuses.md#context-passiveatinjurythreshold), [`PassiveAtStatThreshold`](./Passives_and_Statuses.md#context-passiveatstatthreshold), [`PassiveWhenAffectedByElement`](./Passives_and_Statuses.md#context-passivewhenaffectedbyelement), [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2039 ||
| [`AddStatusToBasicAttack`](Abilities_and_Spells.md#object-addstatustobasicattack) | Object | An object defining status effects to apply on basic attacks, with optional conditions. | 133 ||
| [`Brace`](./Enums.md) | Integer | The amount of flat damage reduction applied to the source. | 94 | 2 |
| [`Metal`](./Enums.md) | Integer || 90 | 1 |
| [`Trample`](./Enums.md) | Array / Integer | The number of tiles this character can move through enemies, dealing damage or applying effects equal to the value. | 88 | [3] |
| [`Thorns`](./Enums.md) | Integer | The number of Thorns stacks applied, which deals damage back to melee attackers. | 65 | 2 |
| [`MeleeRevengeDamage`](Abilities_and_Spells.md#object-meleerevengedamage) | Object | A damage instance object that triggers when the unit is hit by melee attacks while this passive is active. | 59 ||
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of health regeneration (HealthRegen) granted by this damage instance. | 52 | 2 |
| [`StatusEachTurnEnd`](Cat_Mutations.md#object-statuseachturnend) | Object | Status effects that are applied to the unit at the end of each turn. | 49 ||
| [`Robot`](Characters_and_Bosses.md#object-robot) | Object | Marks the unit as a robot. An integer enables the passive; an object can specify alternate energized effects or allow self-energize. | 47 ||
| [`StatusOnBattleEnd`](Abilities_and_Spells.md#object-statusonbattleend) | Object | A block containing status effects or passives that are applied to the unit when a battle ends. | 45 ||
| [`ElementImmune`](./Enums.md) | Enum | Specifies an element (e.g., Fire, Ice) the unit is immune to. | 39 | Ice |
| [`SpawnOnBattleStart`](Elite_Buffs.md#object-spawnonbattlestart) | Enum / Object | Specifies the object (e.g., Food, CharmedGamete) to spawn at the start of battle. | 36 | CharmedTinySpider |
| [`DeathRattle`](Characters_and_Bosses.md#object-deathrattle) | Enum / Object | Defines an ability or explosion that triggers upon the unit's death. | 35 | BoomerCatExplode |
| [`CounterAttack`](./Enums.md) | Enum | Specifies the ability name used for counterattacking when hit. | 34 | ReflexPunchJab |
| [`StatusImmunity`](./Enums.md) | Array / Enum | List of status effects the unit is immune to. | 34 | [Sleep] |
| [`StatusOnKill`](Cat_Mutations.md#object-statusonkill) | Object | Status effects applied to the unit whenever it kills an enemy. | 29 ||
| [`StatusOnTookDamage`](Cat_Mutations.md#object-statusontookdamage) | Object | Status effects applied to the unit whenever it takes damage. | 29 ||
| [`SpawnThingOnDamage`](Cat_Mutations.md#object-spawnthingondamage) | Object | Object specifying an entity to spawn when the unit takes damage, with optional conditions. | 28 ||
| [`AbilityReaction`](Characters_and_Bosses.md#object-abilityreaction) | Enum / Object | Specifies an ability to trigger as a reaction when certain conditions are met. | 23 | PissYourself |
| [`AddPassivesToMinions`](Items_and_Equipment.md#object-addpassivestominions) | Object || 21 ||
| [`DamageUp`](./Enums.md) | Integer | The amount of damage increase, or a string formula for dynamic calculation. | 21 | 2 |
| [`AddMovement`](./Enums.md) | Integer | The number of extra movement tiles the unit gains per turn. | 20 | 20 |
| [`ArmorDodgeChance`](./Enums.md) | Integer || 19 | 10 |
| [`StatusEachTurnBegin`](Cat_Mutations.md#object-statuseachturnbegin) | Object | Status effects applied to the unit at the beginning of each turn. | 18 ||
| [`CritChanceUp`](./Enums.md) | Integer | The amount of critical hit chance increase, in percentage points. | 16 | 80 |
| [`AddBonusRange`](./Enums.md) | Integer | The number of extra tiles added to the unit's attack range. | 15 | 2 |
| [`RevengeDamage`](Abilities_and_Spells.md#object-revengedamage) | Object | An object specifying the effects (e.g., Marked, Charmed, Petrify) applied to the attacker when the unit takes damage. | 15 ||
| [`SpawnEachTurn`](Cat_Mutations.md#object-spawneachturn) | Object | Object specifying an entity to spawn each turn, with chance and number. | 15 ||
| [`StatusOnBattleStart`](Items_and_Equipment.md#object-statusonbattlestart) | Object || 15 ||
| [`AddCorpseHealth`](./Enums.md) | Integer | The amount of additional health a corpse has when the unit dies. | 14 | 96 |
| [`AllStatsUp`](./Enums.md) | Array / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 14 | [.5] |
| [`DodgeChance`](./Enums.md) | Integer | The percentage chance to dodge incoming attacks. | 14 | 50 |
| [`InnateElement`](./Enums.md) | Enum | Specifies the unit's innate elemental type (Fire, Ice, Electric, etc.). | 14 | Ice |
| [`SizeScale`](./Enums.md) | Number | A multiplier for the unit's visual size. Values above 1 increase size, values below 1 decrease size. | 14 | .4 |
| [`WaterWalk`](./Enums.md) | Integer | If set to 1, allows the unit to move over water tiles as if they were normal terrain. | 14 | 1 |
| [`AddManaRegen`](./Enums.md) | Integer | The amount of additional mana regeneration per turn granted while this passive is active. | 13 | 7 |
| [`MulticlassLevelUp`](./Enums.md) | Enum | Specifies the class that the unit gains a level in upon leveling up. | 12 | Druid |
| [`SpawnThingOnDeath`](./Enums.md) | Enum | Specifies a specific entity to spawn upon death, distinct from standard spawns. | 12 | CharmedDemonKitten |
| [`AbilityOnBattleStart`](./Enums.md) | Enum || 11 | neck_ChefsApron |
| [`AddStatusToAllDamage`](Items_and_Equipment.md#object-addstatustoalldamage) | Object || 11 ||
| [`BleedThorns`](./Enums.md) | Integer | The number of Bleed Thorns stacks applied, which deals bleeding damage back to melee attackers. | 11 | 2 |
| [`ExtraBasicAttacks`](./Enums.md) | Integer | The number of additional basic attacks the unit can perform each turn. | 11 | 2 |
| [`MoveWhenDamaged`](Cat_Mutations.md#object-movewhendamaged) | Object | Defines movement behavior triggered when the unit takes damage, including the ability to use and movement weights. | 11 ||
| [`ReplaceBasicMove`](./Enums.md) | Enum | Specifies the ability that replaces the unit's default basic move. | 11 | ToadJump_BasicMove |
| [`AddLevelUpRerolls`](./Enums.md) | Integer | The number of additional rerolls the unit gets when leveling up. | 10 | 2 |
| [`LimitDamage`](./Enums.md) | Integer | The maximum damage the unit can take per hit (limiter). | 10 | 1 |
| [`MoveTowardsDamageSource`](Characters_and_Bosses.md#object-movetowardsdamagesource) | Object | Causes the unit to move towards the source of damage, using a specified move ability. | 10 ||
| [`StatusOnKillEnemy`](Items_and_Equipment.md#object-statusonkillenemy) | Object || 10 ||
| [`AddSelfStatusToBasicAttack`](Items_and_Equipment.md#object-addselfstatustobasicattack) | Object || 9 ||
| [`AddTag`](./Enums.md) | Enum | Specifies a unit tag (e.g., fetus, plant, bug) to add to the unit. | 9 | rock |
| [`BackstabImmunity`](./Enums.md) | Integer | If set to 1, the unit is immune to backstab damage. | 9 | 1 |
| [`Bruise`](./Enums.md) | Integer | The number of Bruise stacks applied, or an array with duration and chance. | 9 | 2 |
| [`DepressionAura`](./Enums.md) | Integer | The number of Depression stacks applied to nearby units as an aura. | 9 | 2 |
| [`Flying`](./Enums.md) | Integer | The number of stacks of the Flying status effect applied to the unit. | 9 | 1 |
| [`LimitHeal`](./Enums.md) | Integer | The maximum amount of health the unit can heal per instance. | 9 | 1 |
| [`MissChance`](./Enums.md) | Integer | The percentage chance that the unit's attacks will miss. | 9 | 15 |
| [`MovementReaction`](Characters_and_Bosses.md#object-movementreaction) | Object | Triggers an ability when an entity moves near the unit. | 9 ||
| [`PoisonThorns`](./Enums.md) | Integer | Applies Poison stacks to any unit that attacks this unit in melee. | 9 | 2 |
| [`SmallRockBehavior`](./Enums.md) | Integer | Defines the damage, knockback, and chain properties of small rocks spawned by asteroid enemies. | 9 | 5 |
| [`StatusAlliesOnBattleStart`](Items_and_Equipment.md#object-statusalliesonbattlestart) | Object || 9 ||
| [`TrinketPassiveMultiplierBonus`](./Enums.md) | Integer || 9 | 2 |
| [`BoostHeals`](./Enums.md) | Integer || 8 | -2 |
| [`ChanceToRevive`](Elite_Buffs.md#object-chancetorevive) | Integer / Object || 8 | 25 |
| [`PermanentMadness`](./Enums.md) | Integer | If set to 1, the Madness status is permanent and will never expire; can use an alias for the status. | 8 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 8 |
| [`AddElementsToBasicAttack`](./Enums.md) | Enum | Specifies the elemental damage type added to the unit's basic attack. | 7 | Ice |
| [`AddInitiative`](./Enums.md) | Integer | The amount to add to the unit's initiative score, affecting turn order. | 7 | -100 |
| [`AlphaTurns`](./Enums.md) | Integer | The number of additional alpha turns the unit receives at the start of combat. | 7 | -1 |
| [`Bleed`](./Enums.md) | Array / Integer | The number of Bleed stacks applied, which deals bleeding damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 7 | [.1] |
| [`BonusAbility`](./Enums.md) | Enum | Determines which additional ability is granted to the character (e.g., as a passive or keyword tooltip link). | 7 | FighterBonusThrow |
| [`DamageNeighborsOnEndMove`](Miscellaneous.md#object-damageneighborsonendmove) | Object || 7 ||
| [`DebuffImmunity`](./Enums.md) | Integer | Grants immunity to debuffs (value likely toggle or tier). | 7 | 1 |
| [`ManaCostReduction`](./Enums.md) | Integer | The amount or percentage by which the mana cost of abilities is reduced. | 7 | 2 |
| [`OverrideBasicAttack`](./Enums.md) | Enum || 7 | GerdShot |
| [`OverrideMaxHealth`](./Enums.md) | Integer | Overrides the unit's maximum health to a specific value. | 7 | 1 |
| [`PassiveAtHealthThreshold`](Items_and_Equipment.md#object-passiveathealththreshold) | Object || 7 ||
| [`PassiveAtStatThreshold`](Items_and_Equipment.md#object-passiveatstatthreshold) | Object || 7 ||
| [`SecurityBotProtect`](Characters_and_Bosses.md#object-securitybotprotect) | Object | Defends a tagged ally by using an ability or move when threatened. | 7 ||
| [`SetSpellCosts`](./Enums.md) | Integer | Overrides all spell costs to a fixed value. | 7 | 3 |
| [`SpeedUp`](./Enums.md) | Integer | Specifies the number of Speed stacks applied, where each stack modifies the unit's turn order and dodge chance. | 7 | 2 |
| [`StatusOnEndMove`](Cat_Mutations.md#object-statusonendmove) | Object | Defines statuses or effects applied when the unit finishes moving. | 7 ||
| [`AddDamageToElementDamage`](Cat_Mutations.md#object-adddamagetoelementdamage) | Object | Adds extra damage to attacks that deal a specified element type. | 6 ||
| [`AmplifyStatus`](Miscellaneous.md#object-amplifystatus) | Enum / Object || 6 | Poison |
| [`ExtraWeaponAttacks`](./Enums.md) | Integer || 6 | 2 |
| [`IgnoreTiles`](./Enums.md) | Integer | If set to 1, the unit ignores tile effects while moving. | 6 | 1 |
| [`Poison`](./Enums.md) | Array / Enum / Integer | The number of Poison stacks applied, which deals poison damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 6 | [.5] |
| [`Quivered`](./Enums.md) | Integer | The number of stacks of Quivered, which grants bonus attacks; can be an array [stacks, probability]. | 6 | 2 |
| [`ReplaceBasicAttack`](./Enums.md) | Enum | Specifies the name of the ability that replaces the unit's basic attack. | 6 | BasicButcherMeleeWideDoubleSpin |
| [`SpawnOnBattleStartRandomEmptyTile`](Cat_Mutations.md#object-spawnonbattlestartrandomemptytile) | Object | Spawns specified objects on random empty tiles at the start of battle. | 6 ||
| [`StatusOnTookDamageFromAbility`](Cat_Mutations.md#object-statusontookdamagefromability) | Object | Defines statuses applied when the unit takes damage from an ability. | 6 ||
| [`TileTrail`](./Enums.md) | Enum | Specifies the tile type (e.g., CreepTile, WaterTile) left behind as the character moves. | 6 | FlowerTile |
| [`AddBonusMeleeRange`](./Enums.md) | Integer | The number of additional tiles of range added to melee attacks. | 5 | 2 |
| [`AddHiddenTag`](./Enums.md) | Enum | Adds a hidden tag to the unit for internal logic or quest tracking. | 5 | bowling_ball |
| [`AutocastEachRound`](Abilities_and_Spells.md#object-autocasteachround) | Object | An object defining an ability that is automatically cast each round, with optional force display or ignore stun. | 5 ||
| [`BackstabCritChance`](./Enums.md) | Integer || 5 | 1 |
| [`Burn`](./Enums.md) | Enum / Integer | The number of Burn stacks applied, which deals fire damage over time; can be an integer, a variable X, or an array `[stacks, probability]` to specify chance of application. | 5 | 2 |
| [`ClassManaCostReduction`](Cat_Mutations.md#object-classmanacostreduction) | Object | Reduces the mana cost of abilities belonging to a specified class. | 5 ||
| [`CritsApplyStatus`](Items_and_Equipment.md#object-critsapplystatus) | Object || 5 ||
| [`FaceShield`](./Enums.md) | Integer | A boolean flag (1 or 0) indicating whether the unit has a face shield that blocks specific effects. | 5 | 0 |
| [`HeadArmorPassiveMultiplierBonus`](./Enums.md) | Integer || 5 | 2 |
| [`InjuryImmunity`](./Enums.md) | Integer | The number of stacks of InjuryImmunity, granting immunity to receiving injuries (permanent wounds) for that many instances. | 5 | 1 |
| [`KnockbackImmunity`](./Enums.md) | Integer | If set to 1, the unit is immune to knockback effects. | 5 | 1 |
| [`StatusIfUnusedMovePoints`](Cat_Mutations.md#object-statusifunusedmovepoints) | Object | Defines statuses applied if the unit has leftover movement points at the end of its turn. | 5 ||
| [`StatusOnTurnEndIfDidntCastAbilityTypes`](Items_and_Equipment.md#object-statusonturnendifdidntcastabilitytypes) | Object || 5 ||
| [`TrinketActiveEffectsMultiplierBonus`](./Enums.md) | Integer || 5 | 2 |
| [`AddCritMultiplier`](./Enums.md) | Integer || 4 | 200 |
| [`AddKnockbackDamage`](./Enums.md) | Integer | The amount of additional damage dealt when the unit knocks back an enemy. | 4 | 2 |
| [`AddStatusToElementDamage`](Items_and_Equipment.md#object-addstatustoelementdamage) | Object || 4 ||
| [`AddStatusToWeapons`](Characters_and_Bosses.md#object-addstatustoweapons) | Object | A dictionary of status effects to apply to the unit's weapon attacks. | 4 ||
| [`AddTemporaryEffectsToBasicAttack`](Cat_Mutations.md#object-addtemporaryeffectstobasicattack) | Object | Adds temporary statuses or effects to the unit's basic attack for the current turn. | 4 ||
| [`BlastResistance`](./Enums.md) | Integer || 4 | 2 |
| [`BoostWeaponDamage`](Items_and_Equipment.md#object-boostweapondamage) | Integer / Object | Increases the damage dealt by the unit's weapon. | 4 | 2 |
| [`BuffImmunity`](./Enums.md) | Integer | If set to 1, the unit is immune to buffs. As an object, can exclude specific buffs. | 4 | 1 |
| [`CatchProjectiles`](Items_and_Equipment.md#object-catchprojectiles) | Object || 4 ||
| [`ChanceToBackflip`](Cat_Mutations.md#object-chancetobackflip) | Object | Defines the chance and ability used for the unit to backflip and dodge an incoming attack. | 4 ||
| [`EquipTemporaryItem`](./Enums.md) | Enum | Specifies the item that is temporarily equipped to the unit. | 4 | FoodMedium |
| [`ExtraStatusWhenDealingDamage`](Items_and_Equipment.md#object-extrastatuswhendealingdamage) | Object || 4 ||
| [`FaceArmorPassiveMultiplierBonus`](./Enums.md) | Integer || 4 | 2 |
| [`ForceSpecificInjury`](./Enums.md) | Enum || 4 | int |
| [`FreezePiercing`](./Enums.md) | Integer || 4 | 1 |
| [`IncreaseExplosionDamage`](./Enums.md) | Integer || 4 | 2 |
| [`IncreaseExplosionSize`](./Enums.md) | Integer || 4 | 2 |
| [`LevelUpClassOverride`](./Enums.md) | Enum || 4 | Jester |
| [`MakeSpellsRequireCharge`](./Enums.md) | Integer || 4 | 1 |
| [`PassiveIfAllArmorEmpty`](Miscellaneous.md#object-passiveifallarmorempty) | Object || 4 ||
| [`PassiveWhenAffectedByElement`](Cat_Mutations.md#object-passivewhenaffectedbyelement) | Object | Grants additional passive effects when the unit is under the effects of a specified element. | 4 ||
| [`StatusAlliesOnDeath`](Items_and_Equipment.md#object-statusalliesondeath) | Object || 4 ||
| [`StatusEveryXSpellCasts`](Cat_Mutations.md#object-statuseveryxspellcasts) | Object | Applies specified statuses after the unit casts a certain number of spells. | 4 ||
| [`StatusOnAllyCatDeath`](Cat_Mutations.md#object-statusonallycatdeath) | Object | Defines statuses applied when an ally cat dies. | 4 ||
| [`StatusOnCastSpell`](Cat_Mutations.md#object-statusoncastspell) | Object | Defines statuses applied when the unit casts a spell. | 4 ||
| [`StatusOnGainCoins`](Characters_and_Bosses.md#object-statusongaincoins) | Object | A dictionary of status effects applied when the unit collects coins. | 4 ||
| [`StatusOnPopCorpse`](Items_and_Equipment.md#object-statusonpopcorpse) | Object || 4 ||
| [`AbilityWhenTaggedCharacterMovesNear`](Cat_Mutations.md#object-abilitywhentaggedcharactermovesnear) | Object | Triggers a specified ability when a character with a specific tag moves within range. | 3 ||
| [`AddPassivesToCharmed`](Items_and_Equipment.md#object-addpassivestocharmed) | Object || 3 ||
| [`AddStatusToBasicMeleeAttack`](Cat_Mutations.md#object-addstatustobasicmeleeattack) | Object | Adds specified statuses to the unit's basic melee attacks. | 3 ||
| [`AddStatusToElementAbilities`](Miscellaneous.md#object-addstatustoelementabilities) | Object || 3 ||
| [`AddStatusToSpells`](Characters_and_Bosses.md#object-addstatustospells) | Object | A dictionary of status effects to apply to the unit's spell attacks. | 3 ||
| [`AllyBonusAbilityAura`](Miscellaneous.md#object-allybonusabilityaura) | Enum / Object || 3 | NubbyToss |
| [`AmplifyKnockback`](./Enums.md) | Integer || 3 | 2 |
| [`ApplyStatusesToRandomEnemiesEachTurn`](Items_and_Equipment.md#object-applystatusestorandomenemieseachturn) | Object || 3 ||
| [`AutoEquipConsumables`](./Enums.md) | Integer || 3 | 1 |
| [`BasicAttackCritChance`](./Enums.md) | Integer || 3 | 100 |
| [`BasicAttackDamageMultiplier`](./Enums.md) | Number || 3 | 33.333334 |
| [`ChanceToBlockAndCounter`](./Enums.md) | Integer || 3 | 33 |
| [`DamageNeighborsAfterMove`](Elite_Buffs.md#object-damageneighborsaftermove) | Object || 3 ||
| [`ElementalManaCostReduction`](Items_and_Equipment.md#object-elementalmanacostreduction) | Object || 3 ||
| [`ExtraBasicMoves_Status`](./Enums.md) | Integer | The number of extra basic moves the unit can perform each turn. Stacks for additional moves. | 3 | 1 |
| [`ExtraMovePoints`](./Enums.md) | Integer | Additional movement points granted each turn. | 3 | 1 |
| [`FlowersOnEndTurn`](./Enums.md) | Integer || 3 | 3 |
| [`IncreaseSpellRange`](./Enums.md) | Integer || 3 | 5 |
| [`KillsToMeat`](./Enums.md) | Enum || 3 | Food |
| [`MoveAndUseAbilityEachTurnBeginIfPossible`](./Enums.md) | Enum || 3 | EatShit |
| [`MoveQuivered`](./Enums.md) | Integer | Specifies the number of bonus movement points granted; an array `[stacks, probability]` specifies the amount and its chance of application. | 3 | 2 |
| [`NeckArmorPassiveMultiplierBonus`](./Enums.md) | Integer || 3 | 2 |
| [`PassiveAfterXKills`](Items_and_Equipment.md#object-passiveafterxkills) | Object || 3 ||
| [`PassiveIfEmptyFace`](Miscellaneous.md#object-passiveifemptyface) | Object || 3 ||
| [`PassiveIfEmptyHead`](Miscellaneous.md#object-passiveifemptyhead) | Object || 3 ||
| [`PassiveIfEmptyNeck`](Miscellaneous.md#object-passiveifemptyneck) | Object || 3 ||
| [`ProtectTargetedAllies`](./Enums.md) | Enum | Configures protection behavior for allies being targeted, using a specified ability or action. | 3 | SwapPositions_WideLoad2 |
| [`RandomPassivePool`](Characters_and_Bosses.md#object-randompassivepool) | Object | A pool of passive groups from which a random set is applied. | 3 ||
| [`RangedTrueShot`](./Enums.md) | Integer || 3 | 1 |
| [`ReplaceBasicAttackWhenCastable`](./Enums.md) | Enum || 3 | Shank2 |
| [`ReplaceSpawnedObjects`](./Enums.md) | Array || 3 | [Boulder] |
| [`SetDefaultFacePassive`](./Enums.md) | Enum || 3 | insane |
| [`SpawnCreepOnHit`](./Enums.md) | Integer | If set to 1, the unit spawns creep tiles when it is hit. | 3 | 1 |
| [`SpawnObjectOnPopCorpse`](./Enums.md) | Enum || 3 | Food |
| [`StatusAfterCastSpell`](Items_and_Equipment.md#object-statusaftercastspell) | Object || 3 ||
| [`StatusOnBreakItem`](Items_and_Equipment.md#object-statusonbreakitem) | Object || 3 ||
| [`StatusOnCrit`](Miscellaneous.md#object-statusoncrit) | Object || 3 ||
| [`StatusOnEatFood`](Cat_Mutations.md#object-statusoneatfood) | Object | Defines statuses applied when the unit consumes food. | 3 ||
| [`StatusOnOverHealed`](Miscellaneous.md#object-statusonoverhealed) | Object || 3 ||
| [`StatusOnStanceSwitch`](Miscellaneous.md#object-statusonstanceswitch) | Object || 3 ||
| [`StatusOnTurnEndIfCastNSpells`](Miscellaneous.md#object-statusonturnendifcastnspells) | Object || 3 ||
| [`StatusOnUseAbilityWithTag`](Miscellaneous.md#object-statusonuseabilitywithtag) | Object || 3 ||
| [`StrengthUp`](./Enums.md) | Integer | Specifies the number of Strength stacks applied, where positive values increase melee damage and negative values decrease it. | 3 | 2 |
| [`WeaponsDontLoseDurability`](./Enums.md) | Integer | If true, weapons do not lose durability when used. | 3 | 0 |
| [`AddDamageToBasicAttack`](./Enums.md) | Integer || 2 | 2 |
| [`AddSelfStatusToWeapons`](Items_and_Equipment.md#object-addselfstatustoweapons) | Object || 2 ||
| [`AddStartingMana`](./Enums.md) | Integer | The amount of bonus mana the unit starts each battle with. | 2 | 20 |
| [`AddStatusToKnockbackDamage`](Items_and_Equipment.md#object-addstatustoknockbackdamage) | Object || 2 ||
| [`AddUnfilledMaxHealth`](./Enums.md) | Integer || 2 | 20 |
| [`AllyDamageReduction`](./Enums.md) | Integer || 2 | 0 |
| [`AllyManaRegenAura`](Miscellaneous.md#object-allymanaregenaura) | Object || 2 ||
| [`AutocastEachTurn`](./Enums.md) | Enum || 2 | ViolentOutburst |
| [`AutocastEachTurnBegin`](Miscellaneous.md#object-autocasteachturnbegin) | Enum / Object || 2 | MindCrack_EldritchVisage |
| [`BasicAttackAOEBonus`](./Enums.md) | Integer || 2 | 2 |
| [`BouncyProjectiles`](Items_and_Equipment.md#object-bouncyprojectiles) | Object || 2 ||
| [`CCImmunity`](./Enums.md) | Integer | If true, the unit is immune to crowd control effects. | 2 | 1 |
| [`CanRemoveCursedItems`](./Enums.md) | Integer | If set to 1, the unit can remove cursed items from their inventory. | 2 | 1 |
| [`CapMovementAbilityRange`](./Enums.md) | Integer || 2 | 1 |
| [`ChangeTauntPriority`](./Enums.md) | Integer || 2 | -1 |
| [`ConsumableEffectsMultiplierBonus`](./Enums.md) | Integer || 2 | 1 |
| [`DisableAbilities`](./Enums.md) | Enum || 2 | all_items |
| [`DoubleCastWeapons`](./Enums.md) | Integer || 2 | 2 |
| [`Eternal`](Items_and_Equipment.md#object-eternal) | Object || 2 ||
| [`FlyDamageIncrease`](./Enums.md) | Integer || 2 | 4 |
| [`FreePathfindElement`](./Enums.md) | Enum | Specifies a terrain element that the unit can pathfind through without penalty. | 2 | Grass |
| [`GainExtraShield`](./Enums.md) | Integer || 2 | 2 |
| [`HPGainBlock`](./Enums.md) | Integer || 2 | 1 |
| [`InfiniteRebirth`](Characters_and_Bosses.md#object-infiniterebirth) | Object | Defines the parameters for infinite rebirth, including health percentage, player cat health, and whether immediate. | 2 ||
| [`ManaCostReductionTagged`](Miscellaneous.md#object-manacostreductiontagged) | Object || 2 ||
| [`MoveAwayFromDamageSource`](./Enums.md) | Enum | Specifies the ability used by the unit to move away from the source of damage. | 2 | MoveOne |
| [`MoveSpeedMultiplier`](./Enums.md) | Number || 2 | .5 |
| [`NubbyTossPriority`](./Enums.md) | Integer || 2 | 1 |
| [`PassiveLevelUpAtCombatEnd`](./Enums.md) | Integer || 2 | 1 |
| [`PassiveWhenAtFullMana`](Cat_Mutations.md#object-passivewhenatfullmana) | Object | Grants additional passive effects when the unit's mana is full. | 2 ||
| [`PassiveWhileInMonkMeleeStance`](Items_and_Equipment.md#object-passivewhileinmonkmeleestance) | Object || 2 ||
| [`PoopWhenHit`](./Enums.md) | Enum | Specifies the object dropped when the unit is hit, optionally with a chance. | 2 | Poop |
| [`RemoveLineOfSightRestrictions`](./Enums.md) | Integer || 2 | 1 |
| [`ScaledStatusOnSpendMana`](Items_and_Equipment.md#object-scaledstatusonspendmana) | Object || 2 ||
| [`SharePickups`](./Enums.md) | Integer | If set, the unit shares pickups with allies, optionally including coins. | 2 | 1 |
| [`SpawnCatCopyOnBattleStart`](Miscellaneous.md#object-spawncatcopyonbattlestart) | Object || 2 ||
| [`StatsAtLowHealth`](Miscellaneous.md#object-statsatlowhealth) | Object || 2 ||
| [`StatusEachTurnEndForEachTurn`](Characters_and_Bosses.md#object-statuseachturnendforeachturn) | Object | Specifies an object defining status effects applied at end of each turn for each turn. | 2 ||
| [`StatusKilledCharacters`](Cat_Mutations.md#object-statuskilledcharacters) | Object | Defines statuses applied to characters killed by the unit, or to the unit itself upon kill. | 2 ||
| [`StatusOnCollectPickup`](Items_and_Equipment.md#object-statusoncollectpickup) | Object || 2 ||
| [`StatusOnEatPill`](Miscellaneous.md#object-statusoneatpill) | Object || 2 ||
| [`StatusOnHealed`](Items_and_Equipment.md#object-statusonhealed) | Object || 2 ||
| [`StatusOnPickupCoins`](Items_and_Equipment.md#object-statusonpickupcoins) | Object || 2 ||
| [`StatusOnTurnEndIfManaExact`](Miscellaneous.md#object-statusonturnendifmanaexact) | Object || 2 ||
| [`StatusOnTurnEndIfManaOrHealthExact`](Miscellaneous.md#object-statusonturnendifmanaorhealthexact) | Object || 2 ||
| [`StatusOnUseBasicAttack`](Items_and_Equipment.md#object-statusonusebasicattack) | Object || 2 ||
| [`StatusWhenAllySpendsMana`](Items_and_Equipment.md#object-statuswhenallyspendsmana) | Object || 2 ||
| [`TauntAlways`](./Enums.md) | Integer || 2 | 1 |
| [`TowerDefenseReflex`](./Enums.md) | Enum | Specifies the reflex ability (e.g., 'attack') used in tower defense mode. | 2 | BasicRanged_1DMG |
| [`UncappedHP`](./Enums.md) | Integer | If true, the unit's HP is not capped and can exceed normal limits. | 2 | 1 |
| [`UpgradeSpawnedPickups`](./Enums.md) | Integer || 2 | 2 |
| [`Weakness`](./Enums.md) | Enum / Integer | The number of Weakness stacks applied, which increases damage taken by the target; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 2 | 2 |
| [`WeaponActiveEffectsMultiplierBonus`](./Enums.md) | Integer || 2 | 2 |
| [`WeaponDamageMultiplierBonus`](./Enums.md) | Integer || 2 | 2 |
| [`WeaponPassiveMultiplierBonus`](./Enums.md) | Integer || 2 | 2 |
| [`AbsorbManaAura`](./Enums.md) | Integer || 1 | 1 |
| [`AddAllyNeighborsToAttackRange`](./Enums.md) | Integer || 1 | 1 |
| [`AddLevelUpStatMultiplier`](./Enums.md) | Integer || 1 | 1 |
| [`AddPassiveToSpawnedRocks`](Miscellaneous.md#object-addpassivetospawnedrocks) | Object || 1 ||
| [`AddPassivesToSummonAbilityMinions`](Miscellaneous.md#object-addpassivestosummonabilityminions) | Object || 1 ||
| [`AddSpellDamage`](./Enums.md) | Integer || 1 | 2 |
| [`AddStatusToBasicAttackWithCooldown`](Miscellaneous.md#object-addstatustobasicattackwithcooldown) | Object || 1 ||
| [`AddStatusToExplosions`](Miscellaneous.md#object-addstatustoexplosions) | Object || 1 ||
| [`AddStatusToFirstBasicAttack`](Miscellaneous.md#object-addstatustofirstbasicattack) | Object || 1 ||
| [`AddStatusToMeleeDamage`](Miscellaneous.md#object-addstatustomeleedamage) | Object || 1 ||
| [`AddStatusToReceivedDamage_ExcludeStatuses`](Miscellaneous.md#object-addstatustoreceiveddamage_excludestatuses) | Object || 1 ||
| [`AddStatusToTrampleDamage`](Characters_and_Bosses.md#object-addstatustotrampledamage) | Object || 1 ||
| [`AddStatusesIfPersistentWeatherElement`](Miscellaneous.md#object-addstatusesifpersistentweatherelement) | Object || 1 ||
| [`AddStatusesToReceivedElementalDamage`](Miscellaneous.md#object-addstatusestoreceivedelementaldamage) | Object || 1 ||
| [`AddWeaponScaling`](./Enums.md) | Integer || 1 | 1 |
| [`AfterImage`](./Enums.md) | Enum | An object defining an afterimage entity (e.g., PlayerCat_ThiefShade) that appears when the character moves. | 1 | PlayerCat_ThiefShade2 |
| [`AllowPassTurn`](./Enums.md) | Integer || 1 | 0 |
| [`AllyDamageReaction`](./Enums.md) | Enum || 1 | attack |
| [`AllyHealthRegenAura`](Miscellaneous.md#object-allyhealthregenaura) | Object || 1 ||
| [`AllyMoveAbilityAura`](./Enums.md) | Enum || 1 | CatapultJump2 |
| [`AllyMultiplyKnockbackDamage`](./Enums.md) | Integer || 1 | 2 |
| [`AlphaCat`](./Enums.md) | Integer | The number of stacks of the AlphaCat status effect. | 1 | 1 |
| [`AlternateCraftingPools`](Miscellaneous.md#object-alternatecraftingpools) | Object || 1 ||
| [`AmplifyPositiveStatus`](./Enums.md) | Integer || 1 | 2 |
| [`Autism`](Miscellaneous.md#object-autism) | Object || 1 ||
| [`AutoCritLowDamage`](./Enums.md) | Integer || 1 | 2 |
| [`BackstabWeakness`](./Enums.md) | Number || 1 | 0.75 |
| [`BasicAttackStatusCarefulness`](./Enums.md) | Integer || 1 | 1 |
| [`BlacklistPickupType`](./Enums.md) | Enum | Specifies the type of pickup that the unit cannot collect. | 1 | food |
| [`BonusFoodEachBattle`](./Enums.md) | Integer || 1 | 2 |
| [`BoobyTrapItems`](Miscellaneous.md#object-boobytrapitems) | Object || 1 ||
| [`BoostAllyStatsOnDeath`](./Enums.md) | Integer || 1 | 2 |
| [`BoostDamageAura`](./Enums.md) | Integer || 1 | 1 |
| [`BoostRangeAura`](./Enums.md) | Integer || 1 | 1 |
| [`BraceForEachNeighboringEnemy`](./Enums.md) | Integer || 1 | 2 |
| [`CantDodge`](./Enums.md) | Integer || 1 | 1 |
| [`CapDamageFromAllies`](./Enums.md) | Integer || 1 | 1 |
| [`CatAPultAnimation`](Miscellaneous.md#object-catapultanimation) | Object || 1 ||
| [`ChainKnockback`](./Enums.md) | Integer || 1 | 1 |
| [`CharmAllFlies`](./Enums.md) | Integer || 1 | 1 |
| [`CobraReflex`](./Enums.md) | Enum || 1 | BasicMonkMelee |
| [`CoinsAddDamage`](./Enums.md) | Integer || 1 | 2 |
| [`CollectPickupsOnBattleEnd`](Miscellaneous.md#object-collectpickupsonbattleend) | Integer / Object || 1 | 1 |
| [`Conductor`](./Enums.md) | Integer || 1 | 2 |
| [`ConfusionEffectOnTaggedAbilities`](./Enums.md) | Enum || 1 | consumable |
| [`ConjureCastSpellsForAllies`](./Enums.md) | Integer || 1 | 2 |
| [`ConsumablesInfiniteRange`](./Enums.md) | Integer || 1 | 1 |
| [`ConsumablesMeleeRange`](./Enums.md) | Integer || 1 | 1 |
| [`DamageEnemiesOnHeal`](./Enums.md) | Integer || 1 | 2 |
| [`DamageEnemiesOnKill`](./Enums.md) | Integer || 1 | 2 |
| [`DamageIfDidntUseSpecificAbility`](Miscellaneous.md#object-damageifdidntusespecificability) | Object || 1 ||
| [`DamageNeighborTilesWhenCastSpell`](Miscellaneous.md#object-damageneighbortileswhencastspell) | Object || 1 ||
| [`DamageReductionAura`](Miscellaneous.md#object-damagereductionaura) | Object || 1 ||
| [`DeathChill`](./Enums.md) | Integer || 1 | 1 |
| [`DejaVu`](./Enums.md) | Integer || 1 | 10 |
| [`Diabetes`](Miscellaneous.md#object-diabetes) | Object || 1 ||
| [`DirtyClaws`](./Enums.md) | Integer || 1 | 1 |
| [`DisableAbilitiesWithTag`](./Enums.md) | Enum | Specifies the tag of abilities that are disabled for the unit. | 1 | meat |
| [`Doomed`](./Enums.md) | Integer | The number of turns until the target is instantly killed when this counter reaches zero. | 1 | 3 |
| [`DukeOfFlies`](./Enums.md) | Integer || 1 | 1 |
| [`Dyslexia`](./Enums.md) | Array || 1 | [3] |
| [`EMP`](Miscellaneous.md#object-emp) | Object || 1 ||
| [`ElementalAttunement`](Miscellaneous.md#object-elementalattunement) | Object || 1 ||
| [`Empath`](./Enums.md) | Integer || 1 | 50 |
| [`EnemiesGetPickupsKnockedOut`](./Enums.md) | Integer || 1 | 2 |
| [`EnergyStorm`](Miscellaneous.md#object-energystorm) | Integer / Object || 1 | 3 |
| [`EquipmentPassiveMultiplierBonus`](./Enums.md) | Integer || 1 | 1 |
| [`EquipmentSetBonusBonus`](./Enums.md) | Integer || 1 | 2 |
| [`EscapeSequence`](Miscellaneous.md#object-escapesequence) | Object || 1 ||
| [`ExhaustionRoundChange`](./Enums.md) | Integer || 1 | 3 |
| [`ExplodeOverkilledEnemies`](./Enums.md) | Integer || 1 | 2 |
| [`ExplosionImmunity`](./Enums.md) | Integer || 1 | 1 |
| [`ExtraInjuryOnDeath`](./Enums.md) | Integer || 1 | 1 |
| [`ExtraTrinketUses`](./Enums.md) | Integer || 1 | 1 |
| [`FamiliarSecondaryDamageImmunity`](./Enums.md) | Integer || 1 | 1 |
| [`FlowerPowerAuraBrace`](./Enums.md) | Integer || 1 | 1 |
| [`FlowerPowerAuraStrength`](./Enums.md) | Integer || 1 | 1 |
| [`FollowUp`](./Enums.md) | Enum || 1 | FollowUpDash2 |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object | Determines which ability the target is forced to cast immediately, ignoring normal costs and cooldowns. | 1 | Hallucinate_Disorder |
| [`FreeSpellsAtFullMana`](./Enums.md) | Integer || 1 | 1 |
| [`FrontstabBasicAttackCritChance`](./Enums.md) | Integer || 1 | 100 |
| [`FullHeal`](./Enums.md) | Integer | If 1, fully heals the target's health and status effects. | 1 | 1 |
| [`FullHealthCritChance`](./Enums.md) | Integer || 1 | 100 |
| [`FullPower`](./Enums.md) | Integer || 1 | 3 |
| [`FurnitureStats`](Miscellaneous.md#object-furniturestats) | Object || 1 ||
| [`GravityWell`](Miscellaneous.md#object-gravitywell) | Object || 1 ||
| [`HealDamagesEnemies`](./Enums.md) | Integer || 1 | 1 |
| [`HealsAlsoRegenMana`](./Enums.md) | Integer || 1 | 2 |
| [`HealsCanRevive`](./Enums.md) | Integer || 1 | 3 |
| [`HolyShieldTransferToTaggedMinions`](./Enums.md) | Enum || 1 | any |
| [`HouseFoodRequirementMultiplier`](./Enums.md) | Integer | Multiplier for the food required by the house. A value of 0 may remove the requirement. | 1 | 0 |
| [`Hypomania`](./Enums.md) | Integer || 1 | 3 |
| [`ImmortalLeeches`](./Enums.md) | Integer || 1 | 1 |
| [`IncreaseHealingSpellRange`](./Enums.md) | Integer || 1 | 2 |
| [`InvertBrainFaction`](./Enums.md) | Integer || 1 | 1 |
| [`KillsHeal`](./Enums.md) | Integer || 1 | 50 |
| [`LateBloomer`](Miscellaneous.md#object-latebloomer) | Object || 1 ||
| [`LightningAspectCharge`](./Enums.md) | Integer || 1 | 0 |
| [`LightningRod`](Miscellaneous.md#object-lightningrod) | Object || 1 ||
| [`LimitSelfKnockbackDamage`](./Enums.md) | Integer || 1 | 1 |
| [`LimitedTileTrail`](./Enums.md) | Enum || 1 | FlowerTile |
| [`LineOfSightTrueSightAura`](./Enums.md) | Number || 1 | 0 |
| [`LobbedHook`](./Enums.md) | Integer || 1 | 2 |
| [`LowHealthAllyDodgeChanceAura`](Miscellaneous.md#object-lowhealthallydodgechanceaura) | Object || 1 ||
| [`Madness`](./Enums.md) | Integer | Specifies the number of Madness stacks applied, which cause the target to act randomly or attack allies; can be an integer, array `[stacks, probability]`, or a keyword alias. | 1 | 1 |
| [`MakeBasicAttackPassThroughThings`](./Enums.md) | Integer || 1 | 1 |
| [`ManaRegenMultiplierIfManaEmpty`](./Enums.md) | Integer || 1 | 2 |
| [`MaxAccuracy`](./Enums.md) | Integer || 1 | 1 |
| [`MaxStartingMana`](./Enums.md) | Integer || 1 | 1 |
| [`MegaMinions`](Miscellaneous.md#object-megaminions) | Integer / Object || 1 | 3 |
| [`MetalDetector`](./Enums.md) | Integer || 1 | 5 |
| [`MinimumTech`](./Enums.md) | Integer || 1 | 1 |
| [`NoManaRegen`](./Enums.md) | Integer | If 1 or defined as an object, prevents mana regeneration. | 1 | 1 |
| [`NoReflection`](./Enums.md) | Integer || 1 | 1 |
| [`NumbingLeeches`](./Enums.md) | Integer || 1 | 3 |
| [`OverhealGainsBothShield`](./Enums.md) | Integer || 1 | 2 |
| [`OverrideMaxMana`](./Enums.md) | Integer || 1 | 1 |
| [`OverridePalette`](./Enums.md) | Integer || 1 | 87 |
| [`Paranoia`](./Enums.md) | Enum || 1 | ParanoiaBasicMelee |
| [`ParasitesArentCursed`](./Enums.md) | Integer || 1 | 1 |
| [`PassiveAtFullHealth`](Miscellaneous.md#object-passiveatfullhealth) | Object || 1 ||
| [`PassiveAtInjuryThreshold`](Miscellaneous.md#object-passiveatinjurythreshold) | Object || 1 ||
| [`PassiveLevelScaledStatus`](Miscellaneous.md#object-passivelevelscaledstatus) | Object || 1 ||
| [`PassiveUntilCastSpell`](Miscellaneous.md#object-passiveuntilcastspell) | Object || 1 ||
| [`PassiveUntilGetKill`](Miscellaneous.md#object-passiveuntilgetkill) | Object || 1 ||
| [`PassiveWhenTheAlpha`](Miscellaneous.md#object-passivewhenthealpha) | Object || 1 ||
| [`PassiveWhileInMonkRangedStance`](Miscellaneous.md#object-passivewhileinmonkrangedstance) | Object || 1 ||
| [`PassiveWhilePreviewingMonkRangedStance`](Miscellaneous.md#object-passivewhilepreviewingmonkrangedstance) | Object || 1 ||
| [`PassiveWhileWearingMetal`](Miscellaneous.md#object-passivewhilewearingmetal) | Object || 1 ||
| [`PermanentImmobile`](./Enums.md) | Integer | The number of stacks of permanent immobility applied, preventing the unit from moving indefinitely. | 1 | 1 |
| [`PermanentItems`](./Enums.md) | Integer || 1 | 2 |
| [`PermanentKitten`](./Enums.md) | Integer || 1 | 1 |
| [`Phasing`](./Enums.md) | Integer | If 1, the unit can phase through obstacles and walls. | 1 | 1 |
| [`Quiver`](./Enums.md) | Integer || 1 | 2 |
| [`RealTimePressure_OneUnit`](./Enums.md) | Integer || 1 | 5 |
| [`ReceivedStatusReplacement`](./Enums.md) | Array || 1 | [Sleep] |
| [`RemoveOncePerFightRestriction`](./Enums.md) | Integer || 1 | 1 |
| [`ReplaceBasicAttackWhenDead`](./Enums.md) | Enum || 1 | Haunt |
| [`ReviveOnWin`](./Enums.md) | Integer || 1 | 100 |
| [`RobotsInheritArmor`](./Enums.md) | Integer || 1 | 2 |
| [`RockDetector`](./Enums.md) | Integer || 1 | 10 |
| [`ScaledStatusOnBleedDamage`](Miscellaneous.md#object-scaledstatusonbleeddamage) | Object || 1 ||
| [`ScaledStatusOnOverMana`](Miscellaneous.md#object-scaledstatusonovermana) | Object || 1 ||
| [`SchrodingerDisorder`](./Enums.md) | Integer || 1 | 50 |
| [`Scleroderma`](./Enums.md) | Integer || 1 | 1 |
| [`SelfDamageWhenDealDamage`](Miscellaneous.md#object-selfdamagewhendealdamage) | Object || 1 ||
| [`ShareHealthRegen`](./Enums.md) | Integer || 1 | 1 |
| [`ShoulderCheck`](./Enums.md) | Integer || 1 | 33 |
| [`ShovingMatch`](./Enums.md) | Enum || 1 | attack |
| [`ShowHiddenThings`](./Enums.md) | Integer | If non-zero, reveals hidden things (e.g., traps, secrets) on the map. | 1 | 1 |
| [`Slow`](./Enums.md) | Enum / Integer | The number of turns of Slow applied, or an array with duration and chance. | 1 | 2 |
| [`SmallEnemiesIgnoreYou`](./Enums.md) | Integer || 1 | 1 |
| [`SmiteEnemiesWhoKill`](Miscellaneous.md#object-smiteenemieswhokill) | Object || 1 ||
| [`SpecialFriends`](Miscellaneous.md#object-specialfriends) | Object || 1 ||
| [`SplittableMove`](./Enums.md) | Integer || 1 | 3 |
| [`SpreadExtraDebuffs`](./Enums.md) | Integer || 1 | 2 |
| [`SpreadPainBonus`](./Enums.md) | Integer || 1 | 2 |
| [`StatMinimum`](./Enums.md) | Integer || 1 | 7 |
| [`StatusAdjacentOnTheirTurnBegin`](Miscellaneous.md#object-statusadjacentontheirturnbegin) | Object || 1 ||
| [`StatusAlliesOnGainCoins`](Miscellaneous.md#object-statusalliesongaincoins) | Object || 1 ||
| [`StatusAlliesOnKill`](Miscellaneous.md#object-statusalliesonkill) | Object || 1 ||
| [`StatusAllyWhenAllySpendsMana`](Miscellaneous.md#object-statusallywhenallyspendsmana) | Object || 1 ||
| [`StatusAnyCatAllyWhoKills`](Miscellaneous.md#object-statusanycatallywhokills) | Object || 1 ||
| [`StatusDamagers`](Miscellaneous.md#object-statusdamagers) | Object || 1 ||
| [`StatusEachTurnEndPerEnemyKill`](Miscellaneous.md#object-statuseachturnendperenemykill) | Object || 1 ||
| [`StatusEnemiesOnDeath`](Miscellaneous.md#object-statusenemiesondeath) | Object || 1 ||
| [`StatusEveryXTurnBegins`](Miscellaneous.md#object-statuseveryxturnbegins) | Object || 1 ||
| [`StatusIfBattleAlreadyBegan`](Miscellaneous.md#object-statusifbattlealreadybegan) | Object || 1 ||
| [`StatusKillers`](Abilities_and_Spells.md#object-statuskillers) | Object | An object defining status effects applied to enemies upon killing them, with possible conditional blocks for boss or non-boss targets. | 1 ||
| [`StatusOnAnyDeath`](Miscellaneous.md#object-statusonanydeath) | Object || 1 ||
| [`StatusOnBattleEndIfKillThresholdMet`](Miscellaneous.md#object-statusonbattleendifkillthresholdmet) | Object || 1 ||
| [`StatusOnDealtDamage`](Miscellaneous.md#object-statusondealtdamage) | Object || 1 ||
| [`StatusOnDealtDamageThreshold`](Miscellaneous.md#object-statusondealtdamagethreshold) | Object || 1 ||
| [`StatusOnGainShield`](Miscellaneous.md#object-statusongainshield) | Object || 1 ||
| [`StatusOnHeal`](Miscellaneous.md#object-statusonheal) | Object || 1 ||
| [`StatusOnLoseShield`](Miscellaneous.md#object-statusonloseshield) | Object || 1 ||
| [`StatusOnOverMana`](Miscellaneous.md#object-statusonovermana) | Object || 1 ||
| [`StatusOnTakeHealthDamage`](Miscellaneous.md#object-statusontakehealthdamage) | Object || 1 ||
| [`StatusOnTookDamageFromEnemyAbility`](Miscellaneous.md#object-statusontookdamagefromenemyability) | Object || 1 ||
| [`StatusOnTriggerTrap`](Miscellaneous.md#object-statusontriggertrap) | Object || 1 ||
| [`StatusOnUseElementAbility`](Miscellaneous.md#object-statusonuseelementability) | Object || 1 ||
| [`StatusPerInjury`](Miscellaneous.md#object-statusperinjury) | Object || 1 ||
| [`StatusReplacement`](./Enums.md) | Array || 1 | [Petrify] |
| [`StatusThingsKnockedBack`](Miscellaneous.md#object-statusthingsknockedback) | Object || 1 ||
| [`Stealth`](./Enums.md) | Integer | The number of turns the unit is invisible, or [stacks, probability] of gaining stealth. | 1 | 1 |
| [`StrengthForEachNeighboringEnemy`](./Enums.md) | Integer || 1 | 2 |
| [`StrengthInNumbersAura`](Miscellaneous.md#object-strengthinnumbersaura) | Integer / Object || 1 | 1 |
| [`StrictLimitDamage`](./Enums.md) | Integer || 1 | 1 |
| [`Study`](Miscellaneous.md#object-study) | Integer / Object || 1 | 1 |
| [`TaggedPickupEffectReplacement`](Miscellaneous.md#object-taggedpickupeffectreplacement) | Object || 1 ||
| [`TauntAtFullHealth`](./Enums.md) | Integer || 1 | 1 |
| [`Tech`](./Enums.md) | Integer | The number of Tech stacks applied, which increase the damage of the next ability used. | 1 | 1 |
| [`TempInitiativeChange`](./Enums.md) | Integer | The amount of temporary initiative change applied to the displaced unit. | 1 | -999 |
| [`TheHunger`](Miscellaneous.md#object-thehunger) | Object || 1 ||
| [`TileDamageMultiplier`](Miscellaneous.md#object-tiledamagemultiplier) | Integer / Object || 1 | 2 |
| [`TourettesMeows`](Miscellaneous.md#object-tourettesmeows) | Object || 1 ||
| [`TowerDefense`](Miscellaneous.md#object-towerdefense) | Object || 1 ||
| [`TrapEffectsMultiplier`](./Enums.md) | Integer || 1 | 2 |
| [`Triskaidekaphobia`](./Enums.md) | Integer || 1 | 13 |
| [`UncappedMana`](./Enums.md) | Integer || 1 | 1 |
| [`UpgradeLevelUpClassActives`](./Enums.md) | Enum || 1 | Colorless |
| [`UpgradeLevelUpClassPassives`](./Enums.md) | Enum || 1 | Colorless |
| [`Vegan`](./Enums.md) | Integer | If non-zero (or defined as an object), applies the Vegan disorder, preventing the unit from consuming meat-based items. | 1 | 1 |
| [`Vengeful`](./Enums.md) | Integer || 1 | 1 |
| [`WeaponCountsAsBasicAttack`](./Enums.md) | Integer || 1 | 1 |
| [`WobblyCat`](./Enums.md) | Integer || 1 | 25 |

</details>

---

### Object: `stats`


**Definition:** Core character metrics (Health, Strength, etc.).  
**Total Count:** 97


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `con` | Enum / Integer | The constitution stat value or modifier for the unit. | 34 ||
| `spd` | Enum / Integer | The speed stat value or modifier for the unit. | 27 ||
| `cha` | Enum / Integer | Specifies the charisma stat value as an integer or 'aux' for auxiliary stat assignment. | 24 ||
| `int` | Enum / Integer || 24 ||
| `str` | Enum / Integer || 22 ||
| `dex` | Enum / Integer || 18 ||
| `lck` | Enum / Integer || 16 ||

</details>

---

### Object: `AddStatusToBasicAttack`


**Definition:** Injects a status effect payload that applies whenever the character performs a basic attack.  
**Total Count:** 92


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToCharmed`](./Passives_and_Statuses.md#context-addpassivestocharmed), [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`PassiveWhenAtFullMana`](./Passives_and_Statuses.md#context-passivewhenatfullmana), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 205 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 56 |
| [`Bleed`](./Enums.md) | Array / Integer | The number of Bleed stacks applied, which deals bleeding damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 30 | [.1] |
| [`Poison`](./Enums.md) | Array / Enum / Integer | The number of Poison stacks applied, which deals poison damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 29 | [.5] |
| [`Knockback`](./Enums.md) | Integer | The number of tiles the target is knocked back. | 24 | 3 |
| [`Burn`](./Enums.md) | Enum / Integer | The number of Burn stacks applied, which deals fire damage over time; can be an integer, a variable X, or an array `[stacks, probability]` to specify chance of application. | 16 | 2 |
| [`Fear`](./Enums.md) | Array / Integer | The number of Fear stacks applied, which reduces the target's accuracy and may cause it to flee; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 13 | [.15] |
| [`Bruise`](./Enums.md) | Integer | The number of Bruise stacks applied, or an array with duration and chance. | 12 | 2 |
| [`ChangeTile`](Abilities_and_Spells.md#object-changetile) | Enum / Object | Specifies the tile type to change the target's tile into (e.g., BrambleTile, LavaTile). | 10 | FloatingGlassTile |
| [`Slow`](./Enums.md) | Enum / Integer | The number of turns of Slow applied, or an array with duration and chance. | 10 | 2 |
| [`Stun`](./Enums.md) | Array / Integer | The number of Stun stacks applied, which prevents the target from taking actions; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 8 | [.05*X] |
| [`Confusion`](./Enums.md) | Integer | The number of turns of Confusion applied, or an array with duration and chance. | 7 | 2 |
| [`Weakness`](./Enums.md) | Enum / Integer | The number of Weakness stacks applied, which increases damage taken by the target; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 7 | 2 |
| [`Conditional_Ally`](Abilities_and_Spells.md#object-conditional_ally) | Object || 5 ||
| [`Leech`](./Enums.md) | Integer | The amount of health stolen per hit as a percentage of damage dealt. | 5 | 1 |
| [`Rot`](./Enums.md) | Integer | The number of stacks of Rot, causing damage over time and potentially spawning a fly on death; can be an array `[stacks, probability]`. | 5 | -999999 |
| [`BounceObject`](./Enums.md) | Enum | Spawns and bounces the specified object onto a random tile, with an optional chance. | 4 | CharmedLeech |
| [`DamageOrHealConditionally`](./Enums.md) | Integer | If set to 1, the status group effect conditionally deals damage or heals based on target. | 4 | 1 |
| [`DistanceBonusDamage`](Engine_StatusAndPassiveKeys.md#object-distancebonusdamage) | Object || 4 ||
| [`Freeze`](./Enums.md) | Array / Integer | The number of stacks of Freeze, immobilizing the unit for that many turns; can be an array `[stacks, probability]`. | 4 | [.15] |
| [`Leeches`](./Enums.md) | Integer | The number of Leech stacks applied, healing the attacker. | 4 | 1 |
| [`SoulLink`](./Enums.md) | Integer | The number of turns the linked status lasts, sharing damage between linked units. | 4 | 1 |
| [`Charmed`](./Enums.md) | Array / Integer | The number of turns of Charmed applied, or an array with duration and chance. | 3 | [.40] |
| [`Conditional_Enemy`](Abilities_and_Spells.md#object-conditional_enemy) | Object || 3 ||
| [`Madness`](./Enums.md) | Integer | Specifies the number of Madness stacks applied, which cause the target to act randomly or attack allies; can be an integer, array `[stacks, probability]`, or a keyword alias. | 3 | 1 |
| [`MagicWeakness`](./Enums.md) | Integer | The number of stacks of MagicWeakness, increasing incoming magic damage; can be an array `[stacks, probability]`. | 3 | 2 |
| [`Piercing`](./Enums.md) | Integer || 3 | 1 |
| [`SpreadDisease`](Abilities_and_Spells.md#object-spreaddisease) | Object | An object defining a disease to spread, including chance and disease type. | 3 ||
| [`ApplyStatusIfCrit`](Abilities_and_Spells.md#object-applystatusifcrit) | Object || 2 ||
| [`ApplyToSource`](Abilities_and_Spells.md#object-applytosource) | Object | An object containing status effects or modifiers applied to the source (attacker) of the triggering condition rather than the target. | 2 ||
| [`Blind`](./Enums.md) | Integer | The number of stacks of Blind to apply, reducing accuracy; can be an array `[stacks, probability]` for a chance-based application. | 2 | 1 |
| [`BurgleCoin`](./Enums.md) | Integer | The number of coins stolen, or an array of [stacks, probability]. | 2 | 1 |
| [`Conditional_Adjacent`](Engine_LogicKeys.md#conditional_adjacent) | Object || 2 ||
| [`Conditional_Shielded`](Abilities_and_Spells.md#object-conditional_shielded) | Object || 2 ||
| [`KnockOutCoin`](./Enums.md) | Array / Integer | Either an integer for guaranteed stacks or an object with `stacks` and `chance` for a probability-based knock-out effect. | 2 | [.5] |
| [`LuckUp`](./Enums.md) | Integer | Specifies the number of Luck stacks applied, where positive values increase critical hit chance and loot quality and negative values decrease them. | 2 | 2 |
| [`ManaLeeches`](./Enums.md) | Integer | The number of mana leech stacks that drain mana on hit. | 2 | 1 |
| [`OverrideChainKnockback`](./Enums.md) | Integer | The number of tiles to override the default chain knockback distance. | 2 | 0 |
| [`SpawnBearTrapOnMiss`](./Enums.md) | Integer || 2 | 1 |
| [`BigSplashDamage`](./Enums.md) | Integer || 1 | 2 |
| [`Conditional_HasTag`](Abilities_and_Spells.md#object-conditional_hastag) | Object | An object that executes inner effects if the target has the specified tag, else falls back. | 1 ||
| [`Conditional_SourceHasTag`](Engine_LogicKeys.md#conditional_sourcehastag) | Object || 1 ||
| [`Else`](Abilities_and_Spells.md#object-else) | Object | An object containing effects that apply when the parent conditional condition is not met. | 1 ||
| [`OverrideChainKnockbackDamage`](./Enums.md) | Integer | A formula or value that overrides the damage dealt by chain knockback effects. | 1 | 0 |
| [`SplashDamage`](./Enums.md) | Integer | The radius in tiles for splash damage applied to the area of effect. | 1 | 2 |

</details>

---

### Object: `effects`
### Object: `effects`

**Definition:** Non-damaging status applications and logic triggers executed on impact.  
**Total Count:** 30


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DamageNeighborsAfterMove`](./Passives_and_Statuses.md#context-damageneighborsaftermove), [`DamageNeighborsOnEndMove`](./Passives_and_Statuses.md#context-damageneighborsonendmove), [`GravityWell`](./Passives_and_Statuses.md#context-gravitywell), [`MeleeRevengeDamage`](./Passives_and_Statuses.md#context-meleerevengedamage), [`RevengeDamage`](./Passives_and_Statuses.md#context-revengedamage), [`SmiteEnemiesWhoKill`](./Passives_and_Statuses.md#context-smiteenemieswhokill), [`fire`](./Passives_and_Statuses.md#context-fire), [`ice`](./Passives_and_Statuses.md#context-ice), [`lightning`](./Passives_and_Statuses.md#context-lightning), [`triattack`](./Passives_and_Statuses.md#context-triattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1695 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 750 |
| [`Stun`](./Enums.md) | Array / Integer | The number of Stun stacks applied, which prevents the target from taking actions; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 98 | [.05*X] |
| [`Burn`](./Enums.md) | Enum / Integer | The number of Burn stacks applied, which deals fire damage over time; can be an integer, a variable X, or an array `[stacks, probability]` to specify chance of application. | 85 | 2 |
| [`Bruise`](./Enums.md) | Integer | The number of Bruise stacks applied, or an array with duration and chance. | 79 | 2 |
| [`Poison`](./Enums.md) | Array / Enum / Integer | The number of Poison stacks applied, which deals poison damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 67 | [.5] |
| [`Bleed`](./Enums.md) | Array / Integer | The number of Bleed stacks applied, which deals bleeding damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 54 | [.1] |
| [`VisualFXTile`](./Enums.md) | Enum | Specifies the visual effect to play on the target tile. | 34 | IcePoof |
| [`Fear`](./Enums.md) | Array / Integer | The number of Fear stacks applied, which reduces the target's accuracy and may cause it to flee; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 31 | [.15] |
| [`Slow`](./Enums.md) | Enum / Integer | The number of turns of Slow applied, or an array with duration and chance. | 29 | 2 |
| [`Immobile`](./Enums.md) | Integer | The number of turns of Immobile applied, or an array with duration and chance. | 24 | 1 |
| [`Weakness`](./Enums.md) | Enum / Integer | The number of Weakness stacks applied, which increases damage taken by the target; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 23 | 2 |
| [`Charmed`](./Enums.md) | Array / Integer | The number of turns of Charmed applied, or an array with duration and chance. | 22 | [.40] |
| [`Freeze`](./Enums.md) | Array / Integer | The number of stacks of Freeze, immobilizing the unit for that many turns; can be an array `[stacks, probability]`. | 19 | [.15] |
| [`Madness`](./Enums.md) | Integer | Specifies the number of Madness stacks applied, which cause the target to act randomly or attack allies; can be an integer, array `[stacks, probability]`, or a keyword alias. | 19 | 1 |
| [`Petrify`](./Enums.md) | Array / Integer | The number of stacks of Petrify, turning the unit to stone and immobilizing it; can be an array `[stacks, probability]`. | 15 | [.2] |
| [`Leeches`](./Enums.md) | Integer | The number of Leech stacks applied, healing the attacker. | 14 | 1 |
| [`Marked`](./Enums.md) | Integer | The number of Marked stacks applied, which increases damage taken from all sources; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 9 | 1 |
| [`SpreadDisease`](Abilities_and_Spells.md#object-spreaddisease) | Object | An object defining a disease to spread, including chance and disease type. | 8 ||

</details>

---

### Object: `AddPassivesToMinions`


**Definition:** Applies the 'AddPassivesToMinions' effect.  
**Total Count:** 29


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 35 ||
| [`DamageUp`](./Enums.md) | Integer | The amount of damage increase, or a string formula for dynamic calculation. | 7 | 2 |
| [`HealthGain`](./Enums.md) | Integer / String | The amount of health restored to the source. | 7 | 2*X |
| [`AddMaxHealth`](./Enums.md) | Integer | The amount to add to the unit's maximum health. Negative values reduce max health. | 6 | 5 |
| [`AddStatusToBasicAttack`](Abilities_and_Spells.md#object-addstatustobasicattack) | Object | An object defining status effects to apply on basic attacks, with optional conditions. | 4 ||
| [`IncreaseExplosionDamage`](./Enums.md) | Integer || 4 | 2 |
| [`FreePathfindElement`](./Enums.md) | Enum | Specifies a terrain element that the unit can pathfind through without penalty. | 3 | Grass |
| [`tag_filter`](./Enums.md) | Enum || 3 | crow |
| [`AddSpeed`](./Enums.md) | Integer | The amount of speed added (or subtracted) to the unit. | 2 | 4 |
| [`AddStatusToExplosions`](Miscellaneous.md#object-addstatustoexplosions) | Object || 2 ||
| [`EMP`](Miscellaneous.md#object-emp) | Object || 2 ||
| [`FamiliarBonusAbility`](./Enums.md) | Enum || 2 | FamiliarSelfDestruct |
| [`ForceAttack`](./Enums.md) | Integer | Forces the unit to perform a basic attack immediately. | 2 | 1 |
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of health regeneration (HealthRegen) granted by this damage instance. | 2 | 2 |
| [`HolyShieldTransferToSpawner`](./Enums.md) | Integer || 2 | 1 |
| [`IncreaseExplosionSize`](./Enums.md) | Integer || 2 | 2 |
| [`PassiveWhenAffectedByElement`](Cat_Mutations.md#object-passivewhenaffectedbyelement) | Object | Grants additional passive effects when the unit is under the effects of a specified element. | 2 ||
| [`PoisonThorns`](./Enums.md) | Integer | Applies Poison stacks to any unit that attacks this unit in melee. | 2 | 2 |
| [`StatusAlliesOnKill`](Miscellaneous.md#object-statusalliesonkill) | Object || 2 ||
| [`StatusOnKill`](Cat_Mutations.md#object-statusonkill) | Object | Status effects applied to the unit whenever it kills an enemy. | 2 ||
| [`WaterWalk`](./Enums.md) | Integer | If set to 1, allows the unit to move over water tiles as if they were normal terrain. | 2 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`AddUnfilledMaxHealth`](./Enums.md) | Integer || 1 | 20 |
| [`DivineShield`](./Enums.md) | Integer | The number of charges of Divine Shield applied, which blocks the next instances of damage entirely; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | 1 |
| [`GrassTileHealing`](./Enums.md) | Integer || 1 | 1 |
| [`Quivered`](./Enums.md) | Integer | The number of stacks of Quivered, which grants bonus attacks; can be an array [stacks, probability]. | 1 | 2 |
| [`SafeExplosions`](./Enums.md) | Integer || 1 | 1 |
| [`TakeExtraTurn`](./Enums.md) | Integer | The number of extra turns granted to the unit. | 1 | 1 |
| [`UncappedHP`](./Enums.md) | Integer | If true, the unit's HP is not capped and can exceed normal limits. | 1 | 1 |

</details>

---

### Object: `SpawnOnBattleStart`


**Definition:** No definition provided.  
**Total Count:** 21


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array / Enum | Specifies the template identifier of the entity to spawn, referencing a predefined character or object in the game data. | 38 ||
| [`number`](./Arrays.md#array-number) | Array / Integer || 29 ||

</details>

---

### Object: `StatusOnTookDamage`


**Definition:** Event Trigger: Applies nested statuses when took damage.  
**Total Count:** 21


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 38 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 14 |
| [`StrengthUp`](./Enums.md) | Integer | Specifies the number of Strength stacks applied, where positive values increase melee damage and negative values decrease it. | 4 | 2 |
| [`ConstitutionUp`](./Enums.md) | Integer | The amount of Constitution (HP) increase, or an array with duration and chance. | 3 | 2 |
| [`DamageUp`](./Enums.md) | Integer | The amount of damage increase, or a string formula for dynamic calculation. | 3 | 2 |
| [`SpeedUp`](./Enums.md) | Integer | Specifies the number of Speed stacks applied, where each stack modifies the unit's turn order and dodge chance. | 3 | 2 |
| [`Temporary`](Abilities_and_Spells.md#object-temporary) | Object | An object that defines a temporary status effect with duration and expiration conditions. | 3 ||
| [`Thorns`](./Enums.md) | Integer | The number of Thorns stacks applied, which deals damage back to melee attackers. | 3 | 2 |
| [`Conditional_HasStatus`](Abilities_and_Spells.md#object-conditional_hasstatus) | Object || 2 ||
| [`Craft`](Abilities_and_Spells.md#object-craft) | Object | An object defining a crafting action, including the item pool and target slot. | 2 ||
| [`IntelligenceUp`](./Enums.md) | Integer | The amount of intelligence increase, which can be a fixed integer or a mathematical expression. | 2 | -1 |
| [`RandomStatUp`](./Enums.md) | Integer | The amount of random stat increase (or decrease if negative) applied to a random stat. | 2 | 2 |
| [`Shield`](./Enums.md) | Integer / String | Specifies the number of Shield stacks applied, where each stack reduces incoming damage by a flat amount. | 2 | 2 |
| [`TempDamageUp`](./Enums.md) | Integer | The number of temporary damage increase stacks applied to the target for the current turn. | 2 | 2 |
| [`DiminishingHealthRegen`](./Enums.md) | Integer | The number of stacks of DiminishingHealthRegen, providing health regeneration each turn that decreases with each stack. | 1 | 2 |
| [`Else`](Abilities_and_Spells.md#object-else) | Object | An object containing effects that apply when the parent conditional condition is not met. | 1 ||
| [`MovementUp`](./Enums.md) | Integer | The number of points of additional movement gained for a number of turns. | 1 | 2 |
| [`RandomInjury`](./Enums.md) | Integer | The number of random injuries applied to the target. | 1 | 1 |
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object | An object listing possible status effects to randomly pick from and apply. | 1 ||
| [`TempMovement`](./Enums.md) | Integer | Specifies the temporary movement range granted to the unit, either as an integer or via an alias. Stacks determine duration in turns. | 1 | 1 |

</details>

---

### Object: `StatusEachTurnEnd`


**Definition:** Applies or references the 'StatusEachTurnEnd' effect/state.  
**Total Count:** 20


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 55 ||
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object | Determines which ability the target is forced to cast immediately, ignoring normal costs and cooldowns. | 12 | Hallucinate_Disorder |
| [`NonStackingDivineShield`](./Enums.md) | Integer | A non-stacking shield that blocks the next instance of damage; applied as an integer for the number of shields. | 6 | 1 |
| [`SpeedUp`](./Enums.md) | Integer | Specifies the number of Speed stacks applied, where each stack modifies the unit's turn order and dodge chance. | 5 | 2 |
| [`EmptyMana`](./Enums.md) | Integer || 2 | 1 |
| [`IntelligenceUp`](./Enums.md) | Integer | The amount of intelligence increase, which can be a fixed integer or a mathematical expression. | 2 | -1 |
| [`RangeUp`](./Enums.md) | Integer | The amount of bonus range added to the unit's attacks. Each stack adds one tile of range. | 2 | 1 |
| [`KineticSpikes`](./Enums.md) | Integer | The number of Kinetic Spikes stacks applied, which deal damage back to attackers when the unit is hit. | 1 | 2 |
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object | An object or entity name that spawns upon hitting a character, with optional stacks and chance. | 1 | Coin |
| [`PermanentMadness`](./Enums.md) | Integer | If set to 1, the Madness status is permanent and will never expire; can use an alias for the status. | 1 | 1 |
| [`StrengthUp`](./Enums.md) | Integer | Specifies the number of Strength stacks applied, where positive values increase melee damage and negative values decrease it. | 1 | 2 |
| [`UseAbility_Madness`](./Enums.md) | Enum || 1 | weapon |

</details>

---

### Object: `lock_item_slot`


**Definition:** No definition provided.  
**Total Count:** 16


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`slot`](./Enums.md#enum-slot) | Enum / Integer | Specifies the equipment slot(s) to craft into (e.g., weapon, neck, face). Can be an integer index or an array of slot names. | 16 ||
| `frame` | Integer | The sprite frame index used for this arm. | 3 ||

</details>

---

### Object: `StatusOnBattleEnd`


**Definition:** Applies the nested status effects when the encounter finishes.  
**Total Count:** 16


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 52 ||
| `even_if_dead` | Boolean | If true, triggers the effect even if the character died during the battle. | 25 ||
| [`RandomMutation`](./Enums.md) | Integer | The number of random mutations to apply. | 9 | 1 |
| [`FindItemFromPool`](Abilities_and_Spells.md#object-finditemfrompool) | Enum / Object | Determines the item pool name from which a random item is granted to the source. | 8 | consumables |
| [`RandomPermanentStat`](./Enums.md) | Integer | The amount of random permanent stat change applied, positive or negative. | 8 | 3 |
| [`CureDisease`](Engine_StatusAndPassiveKeys.md#object-curedisease) | Object || 6 ||
| [`PermanentIntelligence`](./Enums.md) | Integer | The number of permanent intelligence stat points added or subtracted. | 3 | -1 |
| [`NextBattleStatus`](Engine_StatusAndPassiveKeys.md#object-nextbattlestatus) | Object || 2 ||
| [`PermanentConstitution`](./Enums.md) | Integer | The amount of permanent Constitution (max HP) added. | 2 | -1 |
| [`PermanentSpeed`](./Enums.md) | Integer | The number of permanent speed stat points added or subtracted. | 2 | -1 |
| [`PermanentStrength`](./Enums.md) | Integer | The amount of permanent Strength stat increase applied. | 1 | 2 |

</details>

---

### Object: `StatusOnKill`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 16


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 34 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 6 |
| [`HealthGain`](./Enums.md) | Integer / String | The amount of health restored to the source. | 5 | 2*X |
| [`EquipPermanentItem`](./Enums.md) | Enum | Determines which permanent item (e.g., a body part or bone club) is equipped to the source. | 3 | BoneClub |
| [`StrengthUp`](./Enums.md) | Integer | Specifies the number of Strength stacks applied, where positive values increase melee damage and negative values decrease it. | 3 | 2 |
| [`AllStatsUp`](./Enums.md) | Array / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 2 | [.5] |
| [`Conditional_FirstApplicationThisTurn`](Abilities_and_Spells.md#object-conditional_firstapplicationthisturn) | Object || 2 ||
| [`DamageUp`](./Enums.md) | Integer | The amount of damage increase, or a string formula for dynamic calculation. | 2 | 2 |
| [`LuckUp`](./Enums.md) | Integer | Specifies the number of Luck stacks applied, where positive values increase critical hit chance and loot quality and negative values decrease them. | 2 | 2 |
| [`RefreshActPoints`](./Enums.md) | Integer | The amount of action points restored to the unit. | 2 | 1 |
| [`RefreshMovePoints`](./Enums.md) | Integer | The amount of move points restored to the unit. | 2 | 1 |
| [`SpeedUp`](./Enums.md) | Integer | Specifies the number of Speed stacks applied, where each stack modifies the unit's turn order and dodge chance. | 2 | 2 |
| [`RandomStatUp`](./Enums.md) | Integer | The amount of random stat increase (or decrease if negative) applied to a random stat. | 1 | 2 |
| [`Stealth`](./Enums.md) | Integer | The number of turns the unit is invisible, or [stacks, probability] of gaining stealth. | 1 | 1 |
| [`TakeBonusTurnWithStatus`](Abilities_and_Spells.md#object-takebonusturnwithstatus) | Object || 1 ||

</details>

---

### Object: `StatusOnStanceSwitch`


**Definition:** Event Trigger: Applies nested statuses when stance switch.  
**Total Count:** 14


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveIfAllArmorEmpty`](./Passives_and_Statuses.md#context-passiveifallarmorempty), [`PassiveIfEmptyFace`](./Passives_and_Statuses.md#context-passiveifemptyface), [`PassiveIfEmptyHead`](./Passives_and_Statuses.md#context-passiveifemptyhead), [`PassiveIfEmptyNeck`](./Passives_and_Statuses.md#context-passiveifemptyneck), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 14 ||
| [`RandomMagicMissile`](./Enums.md) | Integer | The number of random magic missiles fired, each dealing independent damage; can also be an object with custom tooltip data. | 6 | 2 |
| `NextBasicAttackCritsThisTurn` | `Number` | Guarantees the next basic attack executed this turn will be a critical hit. | 2 ||
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object | Determines which ability the target is forced to cast immediately, ignoring normal costs and cooldowns. | 2 | Hallucinate_Disorder |
| [`RandomStatUp`](./Enums.md) | Integer | The amount of random stat increase (or decrease if negative) applied to a random stat. | 2 | 2 |
| [`Shield`](./Enums.md) | Integer / String | Specifies the number of Shield stacks applied, where each stack reduces incoming damage by a flat amount. | 2 | 2 |
| [`PartialCleanse`](./Enums.md) | Integer | The number of status effects removed from the target (partial cleanse). | 1 | 1 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

---

### Object: `SpreadDisease`


**Definition:** Provides a chance to transmit a disease status to adjacent targets.  
**Total Count:** 12


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`AddStatusToBasicMeleeAttack`](./Passives_and_Statuses.md#context-addstatustobasicmeleeattack), [`MeleeRevengeDamage`](./Passives_and_Statuses.md#context-meleerevengedamage), [`effects`](./Passives_and_Statuses.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`disease`](./Enums.md#enum-disease) | Enum | The specific status effect ID representing the disease. | 13 ||
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of transmitting. | 12 ||
| `can_apply_to_anything` | Boolean | If true, the disease can be applied to any target, ignoring immunities. | 6 ||

</details>

---

### Object: `StatusEachTurnBegin`


**Definition:** Event Trigger: Applies nested statuses to each turn begin.  
**Total Count:** 12


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 24 ||
| [`Conditional_BadRoll`](Abilities_and_Spells.md#object-conditional_badroll) | Object | Defines a conditional effect that triggers on a bad roll with a given probability, optionally with an else clause. | 5 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| [`FillMana`](./Enums.md) | Array / Integer | The amount of mana restored to the unit; can be a fixed integer or an array `[stacks, probability]` for a chance-based application. | 2 | [.25] |
| [`IntelligenceUp`](./Enums.md) | Integer | The amount of intelligence increase, which can be a fixed integer or a mathematical expression. | 2 | -1 |
| [`RandomStatUp`](./Enums.md) | Integer | The amount of random stat increase (or decrease if negative) applied to a random stat. | 2 | 2 |
| [`Conditional_GoodRoll`](Abilities_and_Spells.md#object-conditional_goodroll) | Object | Defines a random roll with odds; if successful, the specified effects are applied. | 1 ||
| [`Fear`](./Enums.md) | Array / Integer | The number of Fear stacks applied, which reduces the target's accuracy and may cause it to flee; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | [.15] |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object | Determines which ability the target is forced to cast immediately, ignoring normal costs and cooldowns. | 1 | Hallucinate_Disorder |

</details>

---

### Object: `Conditional_Ally`


**Definition:** Conditional trigger: Executes nested logic if the target is friendly to the caster.  
**Total Count:** 11


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`AddStatusToElementAbilities`](./Passives_and_Statuses.md#context-addstatustoelementabilities), [`Conditional_SourceHasTag`](./Passives_and_Statuses.md#context-conditional_sourcehastag), [`ExtraStatusWhenDealingDamage`](./Passives_and_Statuses.md#context-extrastatuswhendealingdamage), [`StatusKilledCharacters`](./Passives_and_Statuses.md#context-statuskilledcharacters)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 28 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 ||
| [`DamageUp`](./Enums.md) | Integer | The amount of damage increase, or a string formula for dynamic calculation. | 5 | 2 |
| [`AllStatsUp`](./Enums.md) | Array / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 4 | [.5] |
| `Cleanse` | `Number` | Applies the 'Cleanse' effect. | 3 ||
| [`ApplyToSource`](Abilities_and_Spells.md#object-applytosource) | Object | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 2 ||
| `ClearNegativeEffects` | `Number` | Applies the 'ClearNegativeEffects' effect. | 2 ||
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object | Selects and applies a random status effect from the provided nested block. | 2 ||
| [`Shield`](./Enums.md) | Integer / String | Specifies the number of Shield stacks applied, where each stack reduces incoming damage by a flat amount. | 2 | 2 |
| [`TempSpeedUp`](./Enums.md) | Integer | Alias for TempSpeedUp; temporarily increases the unit's speed stat. | 2 | 10 |
| [`SpeedUp`](./Enums.md) | Integer | Specifies the number of Speed stacks applied, where each stack modifies the unit's turn order and dodge chance. | 1 | 2 |

</details>

---

### Object: `CritsApplyStatus`


**Definition:** Applies the 'CritsApplyStatus' effect.  
**Total Count:** 11


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveIfAllArmorEmpty`](./Passives_and_Statuses.md#context-passiveifallarmorempty), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 12 ||
| [`Stun`](./Enums.md) | Array / Integer | The number of Stun stacks applied, which prevents the target from taking actions; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 3 | [.05*X] |
| [`Weakness`](./Enums.md) | Enum / Integer | The number of Weakness stacks applied, which increases damage taken by the target; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 3 | 2 |
| [`Conditional_HasStatus`](Abilities_and_Spells.md#object-conditional_hasstatus) | Object || 2 ||
| [`Else`](Abilities_and_Spells.md#object-else) | Object | An object containing effects that apply when the parent conditional condition is not met. | 2 ||
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object | An object or entity name that spawns upon hitting a character, with optional stacks and chance. | 2 | Coin |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`Bleed`](./Enums.md) | Array / Integer | The number of Bleed stacks applied, which deals bleeding damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | [.1] |
| [`Bruise`](./Enums.md) | Integer | The number of Bruise stacks applied, or an array with duration and chance. | 1 | 2 |
| [`Confusion`](./Enums.md) | Integer | The number of turns of Confusion applied, or an array with duration and chance. | 1 | 2 |
| [`Immobile`](./Enums.md) | Integer | The number of turns of Immobile applied, or an array with duration and chance. | 1 | 1 |

</details>

---

### Object: `Temporary`


**Definition:** A wrapper object for applying status effects that automatically expire.  
**Total Count:** 11


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_BadRoll`](./Passives_and_Statuses.md#context-conditional_badroll), [`StatusOnGainShield`](./Passives_and_Statuses.md#context-statusongainshield), [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage), [`StatusOnTurnEndIfManaOrHealthExact`](./Passives_and_Statuses.md#context-statusonturnendifmanaorhealthexact)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | The number of stacks, duration, or intensity to apply. | 57 ||
| [`status`](./Enums.md#enum-status) | Enum | The status effect to apply. | 56 ||
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Duration in turns. | 52 ||
| `expires_on_begin_turn` | Boolean | If true, ticks down at the start of the turn rather than the end. | 25 ||
| `expires_on_end_turn` | Boolean | If true, the temporary effect expires at the end of the owning unit's turn. | 21 ||

</details>

---

### Object: `PassiveAtStatThreshold`


**Definition:** Applies the 'PassiveAtStatThreshold' effect.  
**Total Count:** 10


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 13 ||
| [`mode`](./Enums.md#enum-mode) | Enum | Specifies the comparison operator for evaluating a condition against a threshold (e.g., equal, greater). | 13 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 13 ||
| [`threshold`](Items_and_Equipment.md#object-threshold) | Integer / Object | The health threshold value (absolute or equation) at which this ability becomes available. | 13 | 7 |

</details>

---

### Object: `threshold`


**Definition:** Examples: `4*champion_multiplier, 3*champion_multiplier, 1`  
**Total Count:** 10


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveAtStatThreshold`](./Passives_and_Statuses.md#context-passiveatstatthreshold)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `int` | Enum / Integer || 8 ||
| `cha` | Enum / Integer | Specifies the charisma stat value as an integer or 'aux' for auxiliary stat assignment. | 2 ||
| `spd` | Enum / Integer | The speed stat value or modifier for the unit. | 2 ||

</details>

---

### Object: `RevengeDamage`


**Definition:** Reaction trigger: Deals damage to the attacker when hit.  
**Total Count:** 9


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 31 ||
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 29 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 29 |
| `knockback` | Enum / Integer | The number of tiles to push the target away from the attacker; can be negative to pull the target closer, or 'str' to scale with the attacker's strength stat. | 3 ||

</details>

---

### Object: `MeleeRevengeDamage`


**Definition:** Reaction trigger: Applies nested status effects to the attacker when hit by a melee attack.  
**Total Count:** 8


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 70 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 49 |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 47 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 43 ||
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | The base damage properties of an attack. | 22 ||
| [`elements`](./Arrays.md#array-elements) | Array | A list of elemental types applied to the damage instance, such as Heat or Fire, used for weaknesses, resistances, and visual effects. | 10 ||
| [`Poison`](./Enums.md) | Array / Enum / Integer | The number of Poison stacks applied, which deals poison damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | [.5] |
| [`SpreadDisease`](Abilities_and_Spells.md#object-spreaddisease) | Object | An object defining a disease to spread, including chance and disease type. | 1 ||
| [`Weakness`](./Enums.md) | Enum / Integer | The number of Weakness stacks applied, which increases damage taken by the target; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | 2 |

</details>

---

### Object: `PassiveIfAllArmorEmpty`


**Definition:** Applies the 'PassiveIfAllArmorEmpty' effect.  
**Total Count:** 8


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 ||
| [`AddSpellDamage`](./Enums.md) | Integer || 2 | 2 |
| [`CounterAttack`](./Enums.md) | Enum | Specifies the ability name used for counterattacking when hit. | 2 | ReflexPunchJab |
| [`ExtraMovePoints`](./Enums.md) | Integer | Additional movement points granted each turn. | 2 | 1 |
| [`ManaCostReduction`](./Enums.md) | Integer | The amount or percentage by which the mana cost of abilities is reduced. | 2 | 2 |
| [`StatusOnStanceSwitch`](Miscellaneous.md#object-statusonstanceswitch) | Object || 2 ||
| [`CritsApplyStatus`](Items_and_Equipment.md#object-critsapplystatus) | Object || 1 ||
| [`Flying`](./Enums.md) | Integer | The number of stacks of the Flying status effect applied to the unit. | 1 | 1 |

</details>

---

### Object: `RandomStatusFromPool`


**Definition:** Selects and applies a random status effect from the provided nested object.  
**Total Count:** 8


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Ally`](./Passives_and_Statuses.md#context-conditional_ally), [`Conditional_Enemy`](./Passives_and_Statuses.md#context-conditional_enemy), [`StatusOnGainCoins`](./Passives_and_Statuses.md#context-statusongaincoins), [`StatusOnHealed`](./Passives_and_Statuses.md#context-statusonhealed), [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 33 ||
| [`Shield`](./Enums.md) | Integer / String | Specifies the number of Shield stacks applied, where each stack reduces incoming damage by a flat amount. | 12 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 12 |
| [`Thorns`](./Enums.md) | Integer | The number of Thorns stacks applied, which deals damage back to melee attackers. | 10 | 2 |
| [`DivineShield`](./Enums.md) | Integer | The number of charges of Divine Shield applied, which blocks the next instances of damage entirely; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 9 | 1 |
| [`KineticSpikes`](./Enums.md) | Integer | The number of Kinetic Spikes stacks applied, which deal damage back to attackers when the unit is hit. | 9 | 2 |
| [`Poison`](./Enums.md) | Array / Enum / Integer | The number of Poison stacks applied, which deals poison damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 9 | [.5] |
| [`Bleed`](./Enums.md) | Array / Integer | The number of Bleed stacks applied, which deals bleeding damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 8 | [.1] |
| [`Charge`](./Enums.md) | Integer | The number of stacks of Charge, which makes the caster gain 1 Mana per stack at the start of its next turn. | 8 | 2 |
| [`Weakness`](./Enums.md) | Enum / Integer | The number of Weakness stacks applied, which increases damage taken by the target; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 8 | 2 |
| [`Slow`](./Enums.md) | Enum / Integer | The number of turns of Slow applied, or an array with duration and chance. | 7 | 2 |
| [`Blind`](./Enums.md) | Integer | The number of stacks of Blind to apply, reducing accuracy; can be an array `[stacks, probability]` for a chance-based application. | 6 | 1 |
| [`Brace`](./Enums.md) | Integer | The amount of flat damage reduction applied to the source. | 6 | 2 |
| [`Bruise`](./Enums.md) | Integer | The number of Bruise stacks applied, or an array with duration and chance. | 6 | 2 |
| [`DiminishingHealthRegen`](./Enums.md) | Integer | The number of stacks of DiminishingHealthRegen, providing health regeneration each turn that decreases with each stack. | 6 | 2 |
| [`AllStatsUp`](./Enums.md) | Array / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 5 | [.5] |
| [`Burn`](./Enums.md) | Enum / Integer | The number of Burn stacks applied, which deals fire damage over time; can be an integer, a variable X, or an array `[stacks, probability]` to specify chance of application. | 5 | 2 |
| [`MoveQuivered`](./Enums.md) | Integer | Specifies the number of bonus movement points granted; an array `[stacks, probability]` specifies the amount and its chance of application. | 5 | 2 |
| [`Quivered`](./Enums.md) | Integer | The number of stacks of Quivered, which grants bonus attacks; can be an array [stacks, probability]. | 5 | 2 |
| [`BleedThorns`](./Enums.md) | Integer | The number of Bleed Thorns stacks applied, which deals bleeding damage back to melee attackers. | 4 | 2 |
| [`ConstitutionUp`](./Enums.md) | Integer | The amount of Constitution (HP) increase, or an array with duration and chance. | 4 | 2 |
| [`Madness`](./Enums.md) | Integer | Specifies the number of Madness stacks applied, which cause the target to act randomly or attack allies; can be an integer, array `[stacks, probability]`, or a keyword alias. | 4 | 1 |
| [`MagicWeakness`](./Enums.md) | Integer | The number of stacks of MagicWeakness, increasing incoming magic damage; can be an array `[stacks, probability]`. | 4 | 2 |
| [`Marked`](./Enums.md) | Integer | The number of Marked stacks applied, which increases damage taken from all sources; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 4 | 1 |
| [`Reflect`](./Enums.md) | Integer | The number of stacks of Reflect, causing a percentage of incoming damage to be reflected back to the attacker. | 4 | 1 |
| [`SpeedUp`](./Enums.md) | Integer | Specifies the number of Speed stacks applied, where each stack modifies the unit's turn order and dodge chance. | 4 | 2 |
| [`Stun`](./Enums.md) | Array / Integer | The number of Stun stacks applied, which prevents the target from taking actions; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 4 | [.05*X] |
| [`Tarred`](./Enums.md) | Integer | The number of stacks of Tarred, making the unit more vulnerable to fire damage; can be an array `[stacks, probability]`. | 4 | 1 |
| [`Charmed`](./Enums.md) | Array / Integer | The number of turns of Charmed applied, or an array with duration and chance. | 3 | [.40] |
| [`Confusion`](./Enums.md) | Integer | The number of turns of Confusion applied, or an array with duration and chance. | 3 | 2 |
| [`Fear`](./Enums.md) | Array / Integer | The number of Fear stacks applied, which reduces the target's accuracy and may cause it to flee; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 3 | [.15] |
| [`Freeze`](./Enums.md) | Array / Integer | The number of stacks of Freeze, immobilizing the unit for that many turns; can be an array `[stacks, probability]`. | 3 | [.15] |
| [`Immobile`](./Enums.md) | Integer | The number of turns of Immobile applied, or an array with duration and chance. | 3 | 1 |
| [`Petrify`](./Enums.md) | Array / Integer | The number of stacks of Petrify, turning the unit to stone and immobilizing it; can be an array `[stacks, probability]`. | 3 | [.2] |
| [`Sleep`](./Enums.md) | Integer | The number of stacks of Sleep, putting the unit to sleep for that many turns; can be an array `[stacks, probability]`. | 3 | 1 |
| [`StatusGroup`](Abilities_and_Spells.md#object-statusgroup) | Object | A collection of status effects applied together as a group, each with its own stack count. | 3 ||
| [`StrengthUp`](./Enums.md) | Integer | Specifies the number of Strength stacks applied, where positive values increase melee damage and negative values decrease it. | 3 | 2 |
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object | An object or entity name that spawns upon hitting a character, with optional stacks and chance. | 1 | Coin |
| [`SpawnCoinAnywhere`](./Enums.md) | Integer | If integer, the number of coins spawned; if array, [stacks, probability] of spawning a coin anywhere on the map. | 1 | 1 |

</details>

---

### Object: `StatusOnCrit`


**Definition:** Event Trigger: Applies nested statuses when crit.  
**Total Count:** 8


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 ||
| [`LuckUp`](./Enums.md) | Integer | Specifies the number of Luck stacks applied, where positive values increase critical hit chance and loot quality and negative values decrease them. | 3 | 2 |
| [`DamageUp`](./Enums.md) | Integer | The amount of damage increase, or a string formula for dynamic calculation. | 2 | 2 |
| [`Shield`](./Enums.md) | Integer / String | Specifies the number of Shield stacks applied, where each stack reduces incoming damage by a flat amount. | 2 | 2 |
| [`CritChanceUp`](./Enums.md) | Integer | The amount of critical hit chance increase, in percentage points. | 1 | 80 |
| [`RandomStatUp`](./Enums.md) | Integer | The amount of random stat increase (or decrease if negative) applied to a random stat. | 1 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Object: `Conditional_Enemy`


**Definition:** Conditional trigger: Executes nested logic if the target is hostile to the caster.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`AddStatusToElementAbilities`](./Passives_and_Statuses.md#context-addstatustoelementabilities), [`Conditional_NotBoss`](./Passives_and_Statuses.md#context-conditional_notboss)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 34 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 12 |
| [`Confusion`](./Enums.md) | Integer | The number of turns of Confusion applied, or an array with duration and chance. | 9 | 2 |
| [`Conditional_PartyMember`](Engine_LogicKeys.md#conditional_partymember) | Object || 2 ||
| [`Else`](Abilities_and_Spells.md#object-else) | Object | An object containing effects that apply when the parent conditional condition is not met. | 2 ||
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object | An object listing possible status effects to randomly pick from and apply. | 2 ||
| [`Stun`](./Enums.md) | Array / Integer | The number of Stun stacks applied, which prevents the target from taking actions; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 2 | [.05*X] |

</details>

---

### Object: `DamageNeighborsOnEndMove`


**Definition:** Combat Trigger: Deals damage to neighbors on end move.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | The base damage properties of an attack. | 7 ||
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 7 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 ||
| `cant_miss` | `Boolean` | If true, the damage instance always hits its target, bypassing accuracy and evasion checks. | 6 ||
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 6 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 6 |
| `knockback` | Enum / Integer | The number of tiles to push the target away from the attacker; can be negative to pull the target closer, or 'str' to scale with the attacker's strength stat. | 1 ||

</details>

---

### Object: `ForceUseAbility`


**Definition:** No definition provided.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnBegin`](./Passives_and_Statuses.md#context-statuseachturnbegin), [`StatusEachTurnEnd`](./Passives_and_Statuses.md#context-statuseachturnend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 5 ||
| [`chance`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 3 ||

</details>

---

### Object: `PassiveIfEmptyFace`


**Definition:** Applies the 'PassiveIfEmptyFace' effect.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 ||
| [`AddCritMultiplier`](./Enums.md) | Integer || 2 | 200 |
| [`CritChanceUp`](./Enums.md) | Integer | The amount of critical hit chance increase, in percentage points. | 2 | 80 |
| [`DodgeChance`](./Enums.md) | Integer | The percentage chance to dodge incoming attacks. | 2 | 50 |
| [`StatusOnStanceSwitch`](Miscellaneous.md#object-statusonstanceswitch) | Object || 2 ||
| [`KineticSpikes`](./Enums.md) | Integer | The number of Kinetic Spikes stacks applied, which deal damage back to attackers when the unit is hit. | 1 | 2 |

</details>

---

### Object: `PassiveIfEmptyHead`


**Definition:** Applies the 'PassiveIfEmptyHead' effect.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 ||
| [`AddCritMultiplier`](./Enums.md) | Integer || 2 | 200 |
| [`CritChanceUp`](./Enums.md) | Integer | The amount of critical hit chance increase, in percentage points. | 2 | 80 |
| [`DodgeChance`](./Enums.md) | Integer | The percentage chance to dodge incoming attacks. | 2 | 50 |
| [`StatusOnStanceSwitch`](Miscellaneous.md#object-statusonstanceswitch) | Object || 2 ||
| [`KineticSpikes`](./Enums.md) | Integer | The number of Kinetic Spikes stacks applied, which deal damage back to attackers when the unit is hit. | 1 | 2 |

</details>

---

### Object: `PassiveIfEmptyNeck`


**Definition:** Applies the 'PassiveIfEmptyNeck' effect.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 ||
| [`AddCritMultiplier`](./Enums.md) | Integer || 2 | 200 |
| [`CritChanceUp`](./Enums.md) | Integer | The amount of critical hit chance increase, in percentage points. | 2 | 80 |
| [`DodgeChance`](./Enums.md) | Integer | The percentage chance to dodge incoming attacks. | 2 | 50 |
| [`StatusOnStanceSwitch`](Miscellaneous.md#object-statusonstanceswitch) | Object || 2 ||
| [`KineticSpikes`](./Enums.md) | Integer | The number of Kinetic Spikes stacks applied, which deal damage back to attackers when the unit is hit. | 1 | 2 |

</details>

---

### Object: `StatusAlliesOnDeath`


**Definition:** Event Trigger: Applies nested statuses to allies on death.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| `triggers_limit` | Number || 2 ||
| [`AllStatsUp`](./Enums.md) | Array / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 2 | [.5] |
| [`HealAndOverhealToShield`](./Enums.md) | Integer || 2 | 12 |
| [`Reanimate`](./Enums.md) | Integer | The percentage chance (e.g., 50%) to revive upon death. | 2 | 33 |
| [`TakeExtraTurn`](./Enums.md) | Integer | The number of extra turns granted to the unit. | 2 | 1 |
| [`Freeze`](./Enums.md) | Array / Integer | The number of stacks of Freeze, immobilizing the unit for that many turns; can be an array `[stacks, probability]`. | 1 | [.15] |
| [`FullHeal`](./Enums.md) | Integer | If 1, fully heals the target's health and status effects. | 1 | 1 |

</details>

---

### Object: `StatusOnUseAbilityWithTag`


**Definition:** Event Trigger: Applies nested statuses when use ability with tag.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Array / Enum | The specific entity tag required or applied. | 7 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 ||
| [`RefreshActPoints`](./Enums.md) | Integer | The amount of action points restored to the unit. | 3 | 1 |
| `exclude_basicattack` | Boolean || 2 ||
| [`Conditional_FirstApplicationThisTurn`](Abilities_and_Spells.md#object-conditional_firstapplicationthisturn) | Object || 2 ||
| [`DamageUp`](./Enums.md) | Integer | The amount of damage increase, or a string formula for dynamic calculation. | 2 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`HealthGain`](./Enums.md) | Integer / String | The amount of health restored to the source. | 1 | 2*X |
| [`RandomStatUp`](./Enums.md) | Integer | The amount of random stat increase (or decrease if negative) applied to a random stat. | 1 | 2 |

</details>

---

### Object: `AddStatusToElementAbilities`


**Definition:** Applies the 'AddStatusToElementAbilities' effect.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Array / Enum | The specific element type required or applied. | 6 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 6 |
| [`ChangeTile`](Abilities_and_Spells.md#object-changetile) | Enum / Object | Specifies the tile type to change the target's tile into (e.g., BrambleTile, LavaTile). | 2 | FloatingGlassTile |
| [`Conditional_Ally`](Abilities_and_Spells.md#object-conditional_ally) | Object || 2 ||
| [`Conditional_Enemy`](Abilities_and_Spells.md#object-conditional_enemy) | Object || 2 ||
| [`Bleed`](./Enums.md) | Array / Integer | The number of Bleed stacks applied, which deals bleeding damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | [.1] |

</details>

---

### Object: `AddStatusToWeapons`


**Definition:** Applies the 'AddStatusToWeapons' effect.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 ||
| [`Bleed`](./Enums.md) | Array / Integer | The number of Bleed stacks applied, which deals bleeding damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 3 | [.1] |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| [`PullSourceToKnockbackImmuneTarget`](./Enums.md) | Integer | If 1, pulls the source to the target even if the target is immune to knockback. | 2 | 1 |
| [`Cleave`](./Enums.md) | Integer | If an integer, the number of cleave hits; if an object, may contain a chance for cleave. | 1 | 1 |
| [`LeechPercent`](./Enums.md) | Integer || 1 | 50 |

</details>

---

### Object: `CureDisease`


**Definition:** Applies the 'CureDisease' effect.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Passives_and_Statuses.md#context-statusonbattleend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 6 ||
| [`disease`](./Enums.md#enum-disease) | Enum | Specifies the disease type (e.g., Pox, Ebola) for disease-related effects. | 6 ||
| `can_apply_to_anything` | Boolean | If true, the disease can be applied to any target, ignoring immunities. | 1 ||

</details>

---

### Object: `Else`


**Definition:** Fallback object that executes if the preceding `Conditional_` block evaluated to false.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`Conditional_Enemy`](./Passives_and_Statuses.md#context-conditional_enemy), [`CritsApplyStatus`](./Passives_and_Statuses.md#context-critsapplystatus), [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 66 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 23 ||
| `CaptureFamiliar` | `Number` | Applies the 'CaptureFamiliar' effect. | 2 ||
| `FactionConversion` | `Number` | Applies the 'FactionConversion' effect. | 2 ||
| [`Fear`](./Enums.md) | Array / Integer | The number of Fear stacks applied, which reduces the target's accuracy and may cause it to flee; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 2 | [.15] |
| [`Marked`](./Enums.md) | Integer | The number of Marked stacks applied, which increases damage taken from all sources; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 2 | 1 |
| [`PermanentCharm`](./Enums.md) | Integer | If set to 1, the target is permanently charmed and becomes an ally; can use an alias for the status. | 2 | 1 |
| [`TempSpeedUp`](./Enums.md) | Integer | Alias for TempSpeedUp; temporarily increases the unit's speed stat. | 1 | 10 |

</details>

---

### Object: `keyword_tooltips`


**Definition:** Forces specific UI tooltips to appear when hovering over the ability.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 16 ||
| [`Weakness`](./Enums.md) | Enum / Integer | The number of Weakness stacks applied, which increases damage taken by the target; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | 2 |

</details>

---

### Object: `ManaCostReductionTagged`


**Definition:** Applies the 'ManaCostReductionTagged' effect.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `reduction` | Integer || 6 ||
| [`tag`](./Enums.md#enum-tag) | Array / Enum | The specific entity tag required or applied. | 6 ||

</details>

---

### Object: `SpawnEachTurn`


**Definition:** Applies or references the 'SpawnEachTurn' effect/state.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array / Enum | Specifies the template identifier of the entity to spawn, referencing a predefined character or object in the game data. | 22 ||
| [`chance`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 20 ||
| `good` | Boolean | The outcome block triggered on successful condition when spawning something on damage. | 2 ||
| `number` | Array / Integer || 2 ||

</details>

---

### Object: `SpawnThingOnDamage`


**Definition:** Applies or references the 'SpawnThingOnDamage' effect/state.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the template identifier of the entity to spawn, referencing a predefined character or object in the game data. | 38 ||
| `good` | Boolean | The outcome block triggered on successful condition when spawning something on damage. | 20 ||
| `spawn_on_death_hit` | Boolean | If true, the spawn occurs specifically when the damaging hit kills the target. | 10 ||
| `consider_all_layers` | Boolean | If true, considers all map layers when determining spawn location. | 2 ||

</details>

---

### Object: `AddStatusToAllDamage`


**Definition:** Modifier: Injects a status effect into a specific action.  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `AddStatusToBasicMeleeAttack`


**Definition:** Examples: `{ ... }`  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 9 ||
| [`Confusion`](./Enums.md) | Integer | The number of turns of Confusion applied, or an array with duration and chance. | 3 | 2 |
| [`Bruise`](./Enums.md) | Integer | The number of Bruise stacks applied, or an array with duration and chance. | 2 | 2 |
| [`FaceAway`](./Enums.md) | Integer | If non-zero, forces the target to face away from the attacker. | 2 | 1 |
| [`Stun`](./Enums.md) | Array / Integer | The number of Stun stacks applied, which prevents the target from taking actions; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 2 | [.05*X] |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`SpreadDisease`](Abilities_and_Spells.md#object-spreaddisease) | Object | An object defining a disease to spread, including chance and disease type. | 1 ||

</details>

---

### Object: `StatusOnCastSpell`


**Definition:** Event Trigger: Applies nested statuses when cast spell.  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 ||
| [`Charge`](./Enums.md) | Integer | The number of stacks of Charge, which makes the caster gain 1 Mana per stack at the start of its next turn. | 4 | 2 |
| [`CurrentWeaponDamageUp`](./Enums.md) | Integer || 2 | 1 |
| [`HealthGain`](./Enums.md) | Integer / String | The amount of health restored to the source. | 1 | 2*X |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Object: `StatusOnOverHealed`


**Definition:** Event Trigger: Applies nested statuses when over healed.  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |
| [`ForceUseAbility_NonStack`](./Enums.md) | Enum || 2 | Indigestion_Fart2 |
| [`StrengthUp`](./Enums.md) | Integer | Specifies the number of Strength stacks applied, where positive values increase melee damage and negative values decrease it. | 2 | 2 |
| `SpawnScaledRotFly` | Number | Applies the 'SpawnScaledRotFly' effect. | 1 ||
| [`CurrentWeaponDamageUp`](./Enums.md) | Integer || 1 | 1 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

---

### Object: `AddDamageToElementDamage`


**Definition:** Applies or references the 'AddDamageToElementDamage' effect/state.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | The base damage properties of an attack. | 9 ||
| [`element`](./Enums.md#enum-element) | Array / Enum | The specific element type required or applied. | 9 ||

</details>

---

### Object: `AddPassivesToCharmed`


**Definition:** Applies the 'AddPassivesToCharmed' effect.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 ||
| [`AddStatusToBasicAttack`](Abilities_and_Spells.md#object-addstatustobasicattack) | Object | An object defining status effects to apply on basic attacks, with optional conditions. | 3 ||
| [`AddMaxHealth`](./Enums.md) | Integer | The amount to add to the unit's maximum health. Negative values reduce max health. | 2 | 5 |
| [`AddSpeed`](./Enums.md) | Integer | The amount of speed added (or subtracted) to the unit. | 2 | 4 |
| [`DamageUp`](./Enums.md) | Integer | The amount of damage increase, or a string formula for dynamic calculation. | 2 | 2 |

</details>

---

### Object: `AddStatusToElementDamage`


**Definition:** Applies the 'AddStatusToElementDamage' effect.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Array / Enum | The specific element type required or applied. | 6 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 ||
| [`Burn`](./Enums.md) | Enum / Integer | The number of Burn stacks applied, which deals fire damage over time; can be an integer, a variable X, or an array `[stacks, probability]` to specify chance of application. | 3 | 2 |
| [`Conditional_Corpse`](Abilities_and_Spells.md#object-conditional_corpse) | Object || 2 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Object: `AddStatusToExplosions`


**Definition:** Applies the 'AddStatusToExplosions' effect.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AddElement`](./Enums.md#enum-addelement) | Enum | Applies the 'AddElement' effect. | 4 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||
| [`Burn`](./Enums.md) | Enum / Integer | The number of Burn stacks applied, which deals fire damage over time; can be an integer, a variable X, or an array `[stacks, probability]` to specify chance of application. | 4 | 2 |

</details>

---

### Object: `AllyBonusAbilityAura`


**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 2 ||
| `square` | Boolean || 2 ||

</details>

---

### Object: `AllyManaRegenAura`


**Definition:** Applies the 'AllyManaRegenAura' effect.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`range`](./Enums.md#enum-range) | Enum / Integer | Distance or area of effect in tiles. | 4 ||
| `stacks` | Enum / Integer | The number of stacks, duration, or intensity to apply. | 4 ||

</details>

---

### Object: `AmplifyStatus`


**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `addstacks` | Number || 3 ||
| [`status`](./Enums.md#enum-status) | Enum | The ID of the status effect to check or apply. | 3 ||

</details>

---

### Object: `AutocastEachRound`


**Definition:** Forces the character to automatically cast a specific ability at the start of each combat round.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to autocast. | 9 ||
| `even_if_stunned` | Boolean | If true, bypasses stun and hard-CC restrictions to cast anyway. | 6 ||
| `force_display_name` | Boolean | If true, forces the display of the ability name even if it would otherwise be hidden. | 2 ||

</details>

---

### Object: `Conditional_FirstApplicationThisTurn`


**Definition:** Conditional trigger: Executes nested logic only if this is the first time this specific effect has been applied this turn.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnKill`](./Passives_and_Statuses.md#context-statusonkill), [`StatusOnUseAbilityWithTag`](./Passives_and_Statuses.md#context-statusonuseabilitywithtag)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| [`TakeExtraTurn`](./Enums.md) | Integer | The number of extra turns granted to the unit. | 2 | 1 |
| [`AllStatsUp`](./Enums.md) | Array / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 1 | [.5] |
| [`FillMana`](./Enums.md) | Array / Integer | The amount of mana restored to the unit; can be a fixed integer or an array `[stacks, probability]` for a chance-based application. | 1 | [.25] |
| [`ManaGain`](./Enums.md) | Integer | The amount of mana gained; can be a fixed integer or a formula using variables like `X` (e.g., damage dealt or ability cost). | 1 | 2 |

</details>

---

### Object: `DistanceBonusDamage`


**Definition:** Applies the 'DistanceBonusDamage' effect.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `min_range` | Integer | The minimum distance in tiles required for the effect to trigger. | 4 ||
| `stacks` | Enum / Integer | The number of stacks, duration, or intensity to apply. | 4 ||

</details>

---

### Object: `EMP`


**Definition:** Applies the 'EMP' effect.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`spell_graphics_override`](Miscellaneous.md#object-spell_graphics_override) | Object || 4 ||
| [`status_explosion_override`](./Enums.md#enum-status_explosion_override) | Enum || 4 ||

</details>

---

### Object: `empty_armor_scaled_stats`


**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cha` | Enum / Integer | Specifies the charisma stat value as an integer or 'aux' for auxiliary stat assignment. | 1 ||
| `int` | Enum / Integer || 1 ||
| `spd` | Enum / Integer | The speed stat value or modifier for the unit. | 1 ||

</details>

---

### Object: `PassiveAtHealthThreshold`


**Definition:** Applies or references the 'PassiveAtHealthThreshold' effect/state.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`mode`](./Enums.md#enum-mode) | Enum | Specifies the comparison operator for evaluating a condition against a threshold (e.g., equal, greater). | 9 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 9 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 9 ||
| [`threshold`](Items_and_Equipment.md#object-threshold) | Integer / Object | The health threshold value (absolute or equation) at which this ability becomes available. | 9 | 7 |

</details>

---

### Object: `PassiveWhenAffectedByElement`


**Definition:** Examples: `{ ... }`  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Array / Enum | The specific element type required or applied. | 18 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 18 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 18 ||

</details>

---

### Object: `PassiveWhenAtFullMana`


**Definition:** State Trigger: Grants nested passives when at full mana.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 ||
| [`AddStatusToBasicAttack`](Abilities_and_Spells.md#object-addstatustobasicattack) | Object | An object defining status effects to apply on basic attacks, with optional conditions. | 2 ||
| [`Brace`](./Enums.md) | Integer | The amount of flat damage reduction applied to the source. | 2 | 2 |
| [`Flying`](./Enums.md) | Integer | The number of stacks of the Flying status effect applied to the unit. | 2 | 1 |
| [`AddMovement`](./Enums.md) | Integer | The number of extra movement tiles the unit gains per turn. | 1 | 20 |
| [`ReplaceBasicMove`](./Enums.md) | Enum | Specifies the ability that replaces the unit's default basic move. | 1 | ToadJump_BasicMove |

</details>

---

### Object: `spell_graphics_override`


**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`EMP`](./Passives_and_Statuses.md#context-emp)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`area_particle`](./Enums.md#enum-area_particle) | Enum || 4 ||
| [`center_particle`](./Enums.md#enum-center_particle) | Enum || 4 ||
| `palette` | Enum / Integer | Index or list of palette indices used for coloring the entity or its variations. | 4 ||
| [`particle`](./Enums.md#enum-particle) | Enum | Specifies the particle effect to play on form change. | 4 ||

</details>

---

### Object: `StatusAlliesOnKill`


**Definition:** Event Trigger: Applies nested statuses to allies on kill.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||
| [`AllStatsUp`](./Enums.md) | Array / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 2 | [.5] |
| [`DamageUp`](./Enums.md) | Integer | The amount of damage increase, or a string formula for dynamic calculation. | 2 | 2 |
| [`HealthGain`](./Enums.md) | Integer / String | The amount of health restored to the source. | 1 | 2*X |

</details>

---

### Object: `StatusIfUnusedMovePoints`


**Definition:** Event Trigger: Applies nested statuses to if unused move points.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 ||
| [`HealthGain`](./Enums.md) | Integer / String | The amount of health restored to the source. | 4 | 2*X |
| [`ManaGain`](./Enums.md) | Integer | The amount of mana gained; can be a fixed integer or a formula using variables like `X` (e.g., damage dealt or ability cost). | 2 | 2 |
| [`MoveQuivered`](./Enums.md) | Integer | Specifies the number of bonus movement points granted; an array `[stacks, probability]` specifies the amount and its chance of application. | 2 | 2 |
| [`Brace`](./Enums.md) | Integer | The amount of flat damage reduction applied to the source. | 1 | 2 |
| [`ConstitutionUp`](./Enums.md) | Integer | The amount of Constitution (HP) increase, or an array with duration and chance. | 1 | 2 |
| [`Shield`](./Enums.md) | Integer / String | Specifies the number of Shield stacks applied, where each stack reduces incoming damage by a flat amount. | 1 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `StatusOnTurnEndIfCastNSpells`


**Definition:** Event Trigger: Applies nested statuses when turn end if cast n spells.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `spells` | Array | The number of spells the unit has access to. | 5 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 ||
| [`DoubleCastSpell`](./Enums.md) | Integer | The number of times spells are cast twice in a single action. | 3 | 2 |
| [`Quivered`](./Enums.md) | Integer | The number of stacks of Quivered, which grants bonus attacks; can be an array [stacks, probability]. | 2 | 2 |
| [`MoveQuivered`](./Enums.md) | Integer | Specifies the number of bonus movement points granted; an array `[stacks, probability]` specifies the amount and its chance of application. | 1 | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

---

### Object: `StatusOnTurnEndIfManaExact`


**Definition:** Event Trigger: Applies nested statuses when turn end if mana exact.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `mana` | Enum / Integer || 4 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`FreeSpell`](./Enums.md) | Integer | The number of free spells granted, allowing the source to cast spells without consuming mana or charges. | 2 | 1 |
| [`Quivered`](./Enums.md) | Integer | The number of stacks of Quivered, which grants bonus attacks; can be an array [stacks, probability]. | 2 | 2 |
| [`MoveQuivered`](./Enums.md) | Integer | Specifies the number of bonus movement points granted; an array `[stacks, probability]` specifies the amount and its chance of application. | 1 | 2 |
| [`SpellDamageUp`](./Enums.md) | Integer | The number of stacks of SpellDamageUp, increasing spell damage dealt by the unit. | 1 | 1 |

</details>

---

### Object: `StatusOnTurnEndIfManaOrHealthExact`


**Definition:** Event Trigger: Applies nested statuses when turn end if mana or health exact.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `mana` | Enum / Integer || 4 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||
| [`IntelligenceUp`](./Enums.md) | Integer | The amount of intelligence increase, which can be a fixed integer or a mathematical expression. | 2 | -1 |
| [`Shield`](./Enums.md) | Integer / String | Specifies the number of Shield stacks applied, where each stack reduces incoming damage by a flat amount. | 2 | 2 |
| [`SpellDamageUp`](./Enums.md) | Integer | The number of stacks of SpellDamageUp, increasing spell damage dealt by the unit. | 2 | 1 |
| [`Temporary`](Abilities_and_Spells.md#object-temporary) | Object | An object that defines a temporary status effect with duration and expiration conditions. | 2 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`DivineShield`](./Enums.md) | Integer | The number of charges of Divine Shield applied, which blocks the next instances of damage entirely; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | 1 |
| [`HealthGain`](./Enums.md) | Integer / String | The amount of health restored to the source. | 1 | 2*X |
| [`KineticSpikes`](./Enums.md) | Integer | The number of Kinetic Spikes stacks applied, which deal damage back to attackers when the unit is hit. | 1 | 2 |

</details>

---

### Object: `AbilityReaction`


**Definition:** No definition provided.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 10 ||
| `ability_damage_only` | Boolean | If true, this reaction only triggers from damage caused by abilities. | 7 ||
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 1 ||

</details>

---

### Object: `AddSelfStatusToBasicAttack`


**Definition:** Applies or references the 'AddSelfStatusToBasicAttack' effect/state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 11 ||
| [`RandomMagicMissile`](./Enums.md) | Integer | The number of random magic missiles fired, each dealing independent damage; can also be an object with custom tooltip data. | 7 | 2 |

</details>

---

### Object: `AddTemporaryEffectsToBasicAttack`


**Definition:** Applies the 'AddTemporaryEffectsToBasicAttack' effect.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Fury` | Integer | Applies the 'Fury' effect. | 4 ||
| `CastAgain` | Integer / String | Applies the 'CastAgain' effect. | 2 ||

</details>

---

### Object: `Conditional_BadRoll`


**Definition:** Conditional trigger: Executes nested logic based on a randomized bad outcome probability.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnBegin`](./Passives_and_Statuses.md#context-statuseachturnbegin)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`odds`](./Enums.md#enum-odds) | Number | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. | 8 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 8 |
| [`Temporary`](Abilities_and_Spells.md#object-temporary) | Object | An object that defines a temporary status effect with duration and expiration conditions. | 5 ||

</details>

---

### Object: `Conditional_HasStatus`


**Definition:** Conditional trigger: Executes nested logic if the target currently has the specified status effect.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CritsApplyStatus`](./Passives_and_Statuses.md#context-critsapplystatus), [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | The specific status ID to check for. | 20 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 20 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution. | 4 | |

</details>

---

### Object: `DeathRattle`


**Definition:** No definition provided.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 13 ||
| `pop_corpse` | Boolean | If true, the unit's corpse is removed when this passive triggers. | 11 ||

</details>

---

### Object: `ElementalManaCostReduction`


**Definition:** Applies the 'ElementalManaCostReduction' effect.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `reduction` | Integer || 5 ||
| [`element`](./Arrays.md#array-element) | Array / Enum | The specific element type required or applied. | 5 ||

</details>

---

### Object: `FindItemFromPool`


**Definition:** No definition provided.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Passives_and_Statuses.md#context-statusonbattleend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Number | Probability of finding the item. | 3 ||
| [`pool`](./Enums.md#enum-pool) | Array / Enum | The item pool to draw from. | 2 ||

</details>

---

### Object: `MoveTowardsDamageSource`


**Definition:** No definition provided.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | Specifies the ability used to move when damaged. | 5 ||
| `move_far` | Boolean | If true, the unit moves as far as possible towards the damage source. | 4 ||

</details>

---

### Object: `ObjectOnHitCharacter`


**Definition:** No definition provided.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnEnd`](./Passives_and_Statuses.md#context-statuseachturnend), [`StatusEachTurnEndPerEnemyKill`](./Passives_and_Statuses.md#context-statuseachturnendperenemykill)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum | The entity ID of the character to spawn (e.g., CharmedFlea). | 7 ||
| `stacks` | Enum / Integer | The number of stacks, duration, or intensity to apply. | 5 ||

</details>

---

### Object: `SpawnCatCopyOnBattleStart`


**Definition:** Applies the 'SpawnCatCopyOnBattleStart' effect.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the template identifier of the entity to spawn, referencing a predefined character or object in the game data. | 4 ||
| [`prevent_chain_tag`](./Enums.md#enum-prevent_chain_tag) | Enum | Prevents spawning if a unit with the specified tag (e.g., 'ancestorset_shade') already exists. | 4 ||

</details>

---

### Object: `SpawnOnBattleStartRandomEmptyTile`


**Definition:** Applies or references the 'SpawnOnBattleStartRandomEmptyTile' effect/state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the template identifier of the entity to spawn, referencing a predefined character or object in the game data. | 11 ||
| [`number`](./Arrays.md#array-number) | Array / Integer || 10 ||

</details>

---

### Object: `statuses`


**Definition:** Status effects possessed by the character.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ChanceToRevive`](./Passives_and_Statuses.md#context-chancetorevive), [`StatusOnBattleEndIfKillThresholdMet`](./Passives_and_Statuses.md#context-statusonbattleendifkillthresholdmet)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 12 ||
| [`AllStatsUp`](./Enums.md) | Array / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 4 | [.5] |
| [`FindItemFromPool`](Abilities_and_Spells.md#object-finditemfrompool) | Enum / Object | Determines the item pool name from which a random item is granted to the source. | 2 | consumables |
| [`PermanentDexterity`](./Enums.md) | Integer | The amount of permanent dexterity added to the unit. | 2 | 1 |
| [`HealthGain`](./Enums.md) | Integer / String | The amount of health restored to the source. | 1 | 2*X |

</details>

---

### Object: `StatusEveryXSpellCasts`


**Definition:** Applies or references the 'StatusEveryXSpellCasts' effect/state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | The number of stacks, duration, or intensity to apply. | 8 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| [`AllStatsUp`](./Enums.md) | Array / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 2 | [.5] |
| [`SpellDamageUp`](./Enums.md) | Integer | The number of stacks of SpellDamageUp, increasing spell damage dealt by the unit. | 2 | 1 |
| [`ReduceManaCost`](./Enums.md) | Integer | The number by which mana cost of abilities is reduced, up to a minimum of zero. | 1 | 1 |
| [`RepairWeapon`](./Enums.md) | Integer | The number of stacks of RepairWeapon applied (or an array [stacks, probability] for random application). | 1 | 1 |
| [`RepairWeaponCondition`](./Enums.md) | Integer | The amount of weapon condition repaired per spell cast. | 1 | 1 |

</details>

---

### Object: `StatusGroup`


**Definition:** Groups multiple status effects together for batch application.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomStatusFromPool`](./Passives_and_Statuses.md#context-randomstatusfrompool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 ||
| [`LuckUp`](./Enums.md) | Integer | Specifies the number of Luck stacks applied, where positive values increase critical hit chance and loot quality and negative values decrease them. | 2 | 2 |
| [`SpeedUp`](./Enums.md) | Integer | Specifies the number of Speed stacks applied, where each stack modifies the unit's turn order and dodge chance. | 2 | 2 |
| [`DexterityUp`](./Enums.md) | Integer | The amount of Dexterity stat increased or decreased (negative values lower the stat); can be a formula or fixed integer. | 1 | 2 |
| [`SpawnCoinAnywhere`](./Enums.md) | Integer | If integer, the number of coins spawned; if array, [stacks, probability] of spawning a coin anywhere on the map. | 1 | 1 |

</details>

---

### Object: `StatusKilledCharacters`


**Definition:** Event Trigger: Applies nested statuses to killed characters.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusOnAllyCatDeath`


**Definition:** Event Trigger: Applies nested statuses when ally cat death.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 ||
| [`AllStatsUp`](./Enums.md) | Array / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 2 | [.5] |
| [`FillMana`](./Enums.md) | Array / Integer | The amount of mana restored to the unit; can be a fixed integer or an array `[stacks, probability]` for a chance-based application. | 1 | [.25] |
| [`HealthGain`](./Enums.md) | Integer / String | The amount of health restored to the source. | 1 | 2*X |
| [`PercentHeal`](./Enums.md) | Integer || 1 | 50 |
| [`TakeExtraTurn`](./Enums.md) | Integer | The number of extra turns granted to the unit. | 1 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Object: `StatusOnBattleStart`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 9 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 7 |
| [`FullHeal`](./Enums.md) | Integer | If 1, fully heals the target's health and status effects. | 2 | 1 |
| [`Sleep`](./Enums.md) | Integer | The number of stacks of Sleep, putting the unit to sleep for that many turns; can be an array `[stacks, probability]`. | 1 | 1 |

</details>

---

### Object: `StatusOnEatFood`


**Definition:** Event Trigger: Applies nested statuses when eat food.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 ||
| [`StrengthUp`](./Enums.md) | Integer | Specifies the number of Strength stacks applied, where positive values increase melee damage and negative values decrease it. | 2 | 2 |
| [`Cleanse`](./Enums.md) | Integer | If set to 1, removes all status effects from the target; if 0, no cleanse. | 1 | 0 |
| [`IntelligenceUp`](./Enums.md) | Integer | The amount of intelligence increase, which can be a fixed integer or a mathematical expression. | 1 | -1 |
| [`RandomStatUp`](./Enums.md) | Integer | The amount of random stat increase (or decrease if negative) applied to a random stat. | 1 | 2 |

</details>

---

### Object: `StatusOnGainCoins`


**Definition:** Event Trigger: Applies nested statuses when gain coins.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 ||
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object | An object listing possible status effects to randomly pick from and apply. | 2 ||
| [`DivineShield`](./Enums.md) | Integer | The number of charges of Divine Shield applied, which blocks the next instances of damage entirely; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `StatusOnHealed`


**Definition:** Event Trigger: Applies nested statuses when healed.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object | An object or entity name that spawns upon hitting a character, with optional stacks and chance. | 1 | Coin |
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object | An object listing possible status effects to randomly pick from and apply. | 1 ||
| [`Thorns`](./Enums.md) | Integer | The number of Thorns stacks applied, which deals damage back to melee attackers. | 1 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Object: `StatusOnKillEnemy`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 11 ||
| [`DivineShield`](./Enums.md) | Integer | The number of charges of Divine Shield applied, which blocks the next instances of damage entirely; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 2 | 1 |
| [`ManaGain`](./Enums.md) | Integer | The amount of mana gained; can be a fixed integer or a formula using variables like `X` (e.g., damage dealt or ability cost). | 2 | 2 |
| [`HealthGain`](./Enums.md) | Integer / String | The amount of health restored to the source. | 1 | 2*X |
| [`RefreshMovePoints`](./Enums.md) | Integer | The amount of move points restored to the unit. | 1 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Object: `StatusOnTookDamageFromAbility`


**Definition:** Event Trigger: Applies statuses when taking damage from an ability.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 ||
| [`DiminishingHealthRegen`](./Enums.md) | Integer | The number of stacks of DiminishingHealthRegen, providing health regeneration each turn that decreases with each stack. | 2 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`Shield`](./Enums.md) | Integer / String | Specifies the number of Shield stacks applied, where each stack reduces incoming damage by a flat amount. | 1 | 2 |

</details>

---

### Object: `AbilityWhenTaggedCharacterMovesNear`


**Definition:** AI Trigger: Executes an ability when a character with a specific tag moves adjacent.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 5 ||
| [`range`](./Engine_Uncategorized_Resources.md#valid-property-keys) | Variable | Distance or area of effect in tiles. | 5 ||
| [`tag`](./Enums.md#enum-tag) | Array / Enum | The specific entity tag required or applied. | 5 ||

</details>

---

### Object: `AddPassivesToSummonAbilityMinions`


**Definition:** Applies the 'AddPassivesToSummonAbilityMinions' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`DamageUp`](./Enums.md) | Integer | The amount of damage increase, or a string formula for dynamic calculation. | 2 | 2 |
| [`Doomed`](./Enums.md) | Integer | The number of turns until the target is instantly killed when this counter reaches zero. | 2 | 3 |
| [`MovementUp`](./Enums.md) | Integer | The number of points of additional movement gained for a number of turns. | 2 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Object: `AddPassiveToSpawnedRocks`


**Definition:** Applies the 'AddPassiveToSpawnedRocks' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AddFilledMaxHealth` | Number | Applies the 'AddFilledMaxHealth' effect. | 2 ||
| `JoinSpawnerFaction` | Number | Applies the 'JoinSpawnerFaction' effect. | 2 ||

</details>

---

### Object: `AddSelfStatusToWeapons`


**Definition:** Applies the 'AddSelfStatusToWeapons' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `AddStatusToAllDamageAbilities`


**Definition:** Applies the 'AddStatusToAllDamageAbilities' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`Bleed`](./Enums.md) | Array / Integer | The number of Bleed stacks applied, which deals bleeding damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | [.1] |
| [`Piercing`](./Enums.md) | Integer || 1 | 1 |
| [`Weakness`](./Enums.md) | Enum / Integer | The number of Weakness stacks applied, which increases damage taken by the target; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | 2 |

</details>

---

### Object: `AddStatusToBasicAttackWithCooldown`


**Definition:** Applies the 'AddStatusToBasicAttackWithCooldown' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CharmedForceAttack` | `Number` | Applies the 'CharmedForceAttack' effect. | 2 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

---

### Object: `AddStatusToFirstBasicAttack`


**Definition:** Applies the 'AddStatusToFirstBasicAttack' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `AddStatusToMeleeDamage`


**Definition:** Applies the 'AddStatusToMeleeDamage' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`DelayedWind`](Engine_StatusAndPassiveKeys.md#object-delayedwind) | Object | Applies the 'DelayedWind' effect. | 1 ||
| [`DelayedWindCone`](Abilities_and_Spells.md#object-delayedwindcone) | Object || 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Object: `AddStatusToTrampleDamage`


**Definition:** Applies the 'AddStatusToTrampleDamage' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `AllyHealthRegenAura`


**Definition:** Applies the 'AllyHealthRegenAura' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`range`](./Enums.md#enum-range) | Enum / Integer | Distance or area of effect in tiles. | 2 ||
| `stacks` | Enum / Integer | The number of stacks, duration, or intensity to apply. | 2 ||

</details>

---

### Object: `AlternateCraftingPools`


**Definition:** Applies the 'AlternateCraftingPools' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tinkerer_0`](./Enums.md#enum-tinkerer_0) | Enum || 2 ||
| [`tinkerer_1`](./Enums.md#enum-tinkerer_1) | Enum || 2 ||

</details>

---

### Object: `ApplyStatusesToRandomEnemiesEachTurn`


**Definition:** Applies or references the 'ApplyStatusesToRandomEnemiesEachTurn' effect/state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||
| [`Bounty`](./Enums.md) | Integer | The number of Bounty status stacks applied to random enemies each turn. | 3 | 3 |
| `count` | Array / Integer | The numerical quantity. | 2 ||

</details>

---

### Object: `ApplyStatusIfCrit`


**Definition:** Conditional trigger: Executes the nested logic only if the triggering action was a critical hit.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 8 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||
| [`Purge`](./Enums.md) | Integer | The number of stacks of Purge to apply, removing beneficial statuses. | 2 | 0 |

</details>

---

### Object: `ApplyToSource`


**Definition:** Redirects the nested effects to apply to the caster/source of the ability instead of the target.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`Conditional_Ally`](./Passives_and_Statuses.md#context-conditional_ally)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 43 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 20 |
| [`AllStatsUp`](./Enums.md) | Array / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 6 | [.5] |
| [`Shield`](./Enums.md) | Integer / String | Specifies the number of Shield stacks applied, where each stack reduces incoming damage by a flat amount. | 5 | 2 |

</details>

---

### Object: `AutocastEachTurnBegin`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 1 ||
| `advantage_polarity` | Number || 1 ||
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 1 ||

</details>

---

### Object: `BoobyTrapItems`


**Definition:** Applies the 'BoobyTrapItems' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`on_break`](Miscellaneous.md#object-on_break) | Object || 2 ||
| [`on_throw`](Miscellaneous.md#object-on_throw) | Object || 2 ||

</details>

---

### Object: `BoostWeaponDamage`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`crit_chance`](./Engine_DamagingKeys.md#valid-property-keys) | `String` | The chance for the damage instance to critically hit, expressed as a percentage (e.g., 50%) or a decimal fraction (e.g., .5). | 4 ||
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | The base damage properties of an attack. | 4 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||

</details>

---

### Object: `BouncyProjectiles`


**Definition:** Applies the 'BouncyProjectiles' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max_bounces` | Integer || 3 ||
| `max_range` | Enum / Integer || 3 ||

</details>

---

### Object: `CatAPultAnimation`


**Definition:** Applies the 'CatAPultAnimation' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 2 ||
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation clip to use for the ability’s meta representation. | 2 ||

</details>

---

### Object: `CatchProjectiles`


**Definition:** Applies or references the 'CatchProjectiles' effect/state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ally_chance` | Integer || 5 ||
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 5 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 ||
| [`Quivered`](./Enums.md) | Integer | The number of stacks of Quivered, which grants bonus attacks; can be an array [stacks, probability]. | 5 | 2 |
| [`AllStatsUp`](./Enums.md) | Array / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 1 | [.5] |

</details>

---

### Object: `ChanceToBackflip`


**Definition:** Applies or references the 'ChanceToBackflip' effect/state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 6 ||
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 6 ||

</details>

---

### Object: `ChangeTile`


**Definition:** Transforms the terrain tile under the target.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tile`](./Enums.md#enum-tile) | Array / Enum | The specific tile type to change into (e.g., GlassTile). | 12 ||
| `aoe` | Integer | The area of effect or distance in tiles. | 2 ||

</details>

---

### Object: `ClassManaCostReduction`


**Definition:** Applies or references the 'ClassManaCostReduction' effect/state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `reduction` | Integer || 7 ||
| [`class`](./Enums.md#enum-class) | Enum | Character class identifier. | 6 ||

</details>

---

### Object: `Conditional_Adjacent`


**Definition:** Conditional object: Executes nested logic only if the target is/has Adjacent.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`Bleed`](./Enums.md) | Array / Integer | The number of Bleed stacks applied, which deals bleeding damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 2 | [.1] |
| [`BonusCritChance`](./Enums.md) | Integer | The percentage increase in critical hit chance when the target is affected by the specified element. | 2 | 50 |
| [`BonusDamage`](./Enums.md) | Integer | The amount of bonus damage added to an attack; can be a static integer or a formula using variables like `X` or `bonus_melee_damage`. | 2 | 2 |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Object: `Conditional_Boss`


**Definition:** Conditional trigger: Executes nested logic if the target is a Boss.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusKillers`](./Passives_and_Statuses.md#context-statuskillers)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 19 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 6 |
| [`Stun`](./Enums.md) | Array / Integer | The number of Stun stacks applied, which prevents the target from taking actions; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 3 | [.05*X] |
| [`Charmed`](./Enums.md) | Array / Integer | The number of turns of Charmed applied, or an array with duration and chance. | 2 | [.40] |

</details>

---

### Object: `Conditional_Corpse`


**Definition:** Conditional trigger: Executes nested logic if the target is a dead body/corpse.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToElementDamage`](./Passives_and_Statuses.md#context-addstatustoelementdamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 10 ||
| `Revive` | `Number` | Applies the 'Revive' effect. | 7 ||
| `OverrideDamage` | `Number` | Applies the 'OverrideDamage' effect. | 2 ||
| `TakeExtraTurn` | `Number` | Applies the 'TakeExtraTurn' effect. | 2 ||
| [`Charmed`](./Enums.md) | Array / Integer | The number of turns of Charmed applied, or an array with duration and chance. | 2 | [.40] |
| [`SafeDoomed`](./Enums.md) | Integer | The number of turns until the target is instantly killed when this counter reaches zero, but unlike standard Doomed, it does not inflict injuries upon death. | 2 | 1 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`DamageUp`](./Enums.md) | Integer | The amount of damage increase, or a string formula for dynamic calculation. | 1 | 2 |
| [`SpeedUp`](./Enums.md) | Integer | Specifies the number of Speed stacks applied, where each stack modifies the unit's turn order and dodge chance. | 1 | 2 |

</details>

---

### Object: `Conditional_HasTag`


**Definition:** Conditional trigger: Executes nested logic if the target possesses the specified entity tag.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToAllDamage`](./Passives_and_Statuses.md#context-addstatustoalldamage), [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Array / Enum | The specific string tag to check for. | 46 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 46 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 11 ||
| `FlatLeechIfDamaged` | `Number` | Applies the 'FlatLeechIfDamaged' effect. | 1 ||
| [`Charmed`](./Enums.md) | Array / Integer | The number of turns of Charmed applied, or an array with duration and chance. | 1 | [.40] |

</details>

---

### Object: `Conditional_NotBoss`


**Definition:** Conditional trigger: Executes nested logic if the target is NOT a Boss.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusKillers`](./Passives_and_Statuses.md#context-statuskillers)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution. | 3 | |

</details>

---

### Object: `Conditional_PartyMember`


**Definition:** Conditional constraint. Nested properties only trigger if this is true.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Enemy`](./Passives_and_Statuses.md#context-conditional_enemy)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution. | 3 | |

</details>

---

### Object: `Conditional_Shielded`


**Definition:** Conditional trigger: Executes nested logic if the target currently has a Shield status.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 5 |
| `BonusCritChance` | `Number` | Applies the 'BonusCritChance' effect. | 2 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||

</details>

---

### Object: `Craft`


**Definition:** Synthesizes or spawns a new item from a specific pool.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Array / Enum | Specifies the loot pool, ability pool, or item category from which an item or effect is selected; can be a specific pool name, table index, or inline array. | 15 ||
| [`slot`](./Enums.md#enum-slot) | Enum / Integer | Specifies the equipment slot(s) to craft into (e.g., weapon, neck, face). Can be an integer index or an array of slot names. | 14 ||

</details>

---

### Object: `DamageNeighborsAfterMove`


**Definition:** Examples: `{ ... }`  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](./Math_Equations.md) | Equation | The base damage properties of an attack. | 4 ||
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 4 ||
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 4 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||
| [`elements`](./Arrays.md#array-elements) | Array | A list of elemental types applied to the damage instance, such as Heat or Fire, used for weaknesses, resistances, and visual effects. | 4 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |

</details>

---

### Object: `DamageNeighborTilesWhenCastSpell`


**Definition:** Combat Trigger: Deals damage to neighbor tiles when cast spell.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`fire`](Characters_and_Bosses.md#object-fire) | Object || 1 ||
| [`ice`](Engine_LogicKeys.md#object-ice) | Object || 1 ||
| [`lightning`](Events_and_Encounters.md#object-lightning) | Object || 1 ||
| [`triattack`](Miscellaneous.md#object-triattack) | Object || 1 ||

</details>

---

### Object: `DamageReductionAura`


**Definition:** Combat Trigger: Deals damage to reduction aura.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allies_only` | Boolean | If true, the Buddy effect only targets allies. | 2 ||
| [`range`](./Enums.md#enum-range) | Enum / Integer | Distance or area of effect in tiles. | 2 ||
| `stacks` | Enum / Integer | The number of stacks, duration, or intensity to apply. | 2 ||

</details>

---

### Object: `Earth`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](./Math_Equations.md) | Equation | The base damage properties of an attack. | 2 ||

</details>

---

### Object: `Electric`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `ElementalAttunement`


**Definition:** Applies the 'ElementalAttunement' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Earth`](Engine_LogicKeys.md#object-earth) | Object | Applies the 'Earth' effect. | 2 ||
| [`Electric`](Engine_LogicKeys.md#object-electric) | Object | Applies the 'Electric' effect. | 2 ||
| [`Fire`](Characters_and_Bosses.md#object-fire) | Integer / Object | Applies the 'Fire' effect. | 2 ||
| [`Grass`](Engine_LogicKeys.md#object-grass) | Object | Applies the 'Grass' effect. | 2 ||
| [`Gravity`](Engine_LogicKeys.md#object-gravity) | Object | Applies the 'Gravity' effect. | 2 ||
| [`Holy`](Characters_and_Bosses.md#object-holy) | Enum / Object | Applies the 'Holy' effect. | 2 ||
| [`Ice`](Engine_LogicKeys.md#object-ice) | Object | Applies the 'Ice' effect. | 2 ||
| [`Shadow`](Engine_LogicKeys.md#object-shadow) | Object | Applies the 'Shadow' effect. | 2 ||
| [`Water`](Characters_and_Bosses.md#object-water) | Object | Applies the 'Water' effect. | 2 ||
| [`Wind`](Engine_LogicKeys.md#object-wind) | Object | Applies the 'Wind' effect. | 2 ||

</details>

---

### Object: `EscapeSequence`


**Definition:** Applies the 'EscapeSequence' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RandomDistanceDisplace` | `Number` | Displaces the target by a randomized distance. | 2 ||
| `SafeExplosionIfHitSomething` | Number | Applies the 'SafeExplosionIfHitSomething' effect. | 2 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

---

### Object: `Eternal`


**Definition:** Applies the 'Eternal' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `health_percent` | Integer || 3 ||
| `stacks` | Enum / Integer | The number of stacks, duration, or intensity to apply. | 3 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`AllStatsUp`](./Enums.md) | Array / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 1 | [.5] |
| [`TakeExtraTurn`](./Enums.md) | Integer | The number of extra turns granted to the unit. | 1 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Object: `ExtraStatusWhenDealingDamage`


**Definition:** Applies or references the 'ExtraStatusWhenDealingDamage' effect/state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `Fire`


**Definition:** Character Form: Behavior and stats for the 'Fire' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`Burn`](./Enums.md) | Enum / Integer | The number of Burn stacks applied, which deals fire damage over time; can be an integer, a variable X, or an array `[stacks, probability]` to specify chance of application. | 2 | 2 |

</details>

---

### Object: `Grass`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`Poison`](./Enums.md) | Array / Enum / Integer | The number of Poison stacks applied, which deals poison damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 2 | [.5] |

</details>

---

### Object: `Gravity`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `GravityWell`


**Definition:** Applies the 'GravityWell' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | The base damage properties of an attack. | 2 ||
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 2 ||
| [`elements`](./Arrays.md#array-elements) | Array | A list of elemental types applied to the damage instance, such as Heat or Fire, used for weaknesses, resistances, and visual effects. | 2 ||
| [`cant_miss`](./Enums.md) | Boolean | If true, the damage instance always hits its target, bypassing accuracy and evasion checks. | 2 | true |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Defines the effects (e.g., statuses, damage) applied by the revenge damage. | 2 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [{Damaging Keys}](./Engine_DamagingKeys.md#valid-property-keys) | Object | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Object: `HealAlliesEachTurn`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveUntilCastSpell`](./Passives_and_Statuses.md#context-passiveuntilcastspell)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exclude_self` | Boolean || 2 ||
| `mana` | Enum / Integer || 2 ||
| `stacks` | Enum / Integer | The number of stacks, duration, or intensity to apply. | 2 ||

</details>

---

### Object: `Holy`


**Definition:** Character Form: Behavior and stats for the \'Holy\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||
| [`FlatLeech`](./Enums.md) | Enum | The amount of flat health restored per hit (leech). | 2 | X |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Object: `HolyDamageBlessing`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveUntilGetKill`](./Passives_and_Statuses.md#context-passiveuntilgetkill)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage_multiplier` | Number || 2 ||
| [`Burn`](./Enums.md) | Enum / Integer | The number of Burn stacks applied, which deals fire damage over time; can be an integer, a variable X, or an array `[stacks, probability]` to specify chance of application. | 2 | 2 |

</details>

---

### Object: `Ice`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `InfiniteRebirth`


**Definition:** Applies the 'InfiniteRebirth' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `health` | Integer | The unit's base health, specified as an absolute integer or a percentage modifier. | 3 ||
| `playercat_health` | Integer | The percentage of maximum health the player cat must have to trigger rebirth. | 3 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`TempSpeedUp`](./Enums.md) | Integer | Alias for TempSpeedUp; temporarily increases the unit's speed stat. | 2 | 10 |

</details>

---

### Object: `LateBloomer`


**Definition:** Applies the 'LateBloomer' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | The number of stacks, duration, or intensity to apply. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`AllStatsUp`](./Enums.md) | Array / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 2 | [.5] |

</details>

---

### Object: `LightningRod`


**Definition:** Applies the 'LightningRod' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Tech`](./Enums.md) | Integer | The number of Tech stacks applied, which increase the damage of the next ability used. | 2 | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

---

### Object: `LowHealthAllyDodgeChanceAura`


**Definition:** Applies the 'LowHealthAllyDodgeChanceAura' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 2 ||
| `theshold` | Number || 2 ||

</details>

---

### Object: `MovementReaction`


**Definition:** Reaction: Triggers an effect or ability when forced to move.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 11 ||
| `enemies_only` | Boolean | If true, this effect only targets enemies. | 7 ||

</details>

---

### Object: `NextBattleStatus`


**Definition:** Applies the 'NextBattleStatus' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Passives_and_Statuses.md#context-statusonbattleend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `on_break`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BoobyTrapItems`](./Passives_and_Statuses.md#context-boobytrapitems)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SafeExplosionIfHitSomething` | Number | Applies the 'SafeExplosionIfHitSomething' effect. | 2 ||

</details>

---

### Object: `on_throw`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BoobyTrapItems`](./Passives_and_Statuses.md#context-boobytrapitems)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HitExplosion` | `Number` | Applies the 'HitExplosion' effect. | 2 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

---

### Object: `PassiveAfterXKills`


**Definition:** Applies or references the 'PassiveAfterXKills' effect/state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | The number of stacks, duration, or intensity to apply. | 4 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 4 ||

</details>

---

### Object: `PassiveAtFullHealth`


**Definition:** Applies the 'PassiveAtFullHealth' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TakeExtraDamage` | Number | Applies the 'TakeExtraDamage' effect. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`ManaCostReduction`](./Enums.md) | Integer | The amount or percentage by which the mana cost of abilities is reduced. | 2 | 2 |

</details>

---

### Object: `PassiveAtInjuryThreshold`


**Definition:** Applies the 'PassiveAtInjuryThreshold' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | `String` || 2 ||
| [`mode`](./Enums.md#enum-mode) | Enum | Specifies the comparison operator for evaluating a condition against a threshold (e.g., equal, greater). | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 ||
| [`threshold`](Items_and_Equipment.md#object-threshold) | Integer / Object | The health threshold value (absolute or equation) at which this ability becomes available. | 2 | 7 |

</details>

---

### Object: `PassiveGroup`


**Definition:** Passive: A collection of passives grouped together for easier management.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomPassivePool`](./Passives_and_Statuses.md#context-randompassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 14 ||
| [`SetDefaultFace`](./Enums.md) | Enum | Specifies the default face expression for the unit (e.g., sad, happy, insane). | 2 | sad |
| [`AllStatsUp`](./Enums.md) | Array / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 1 | [.5] |
| [`CharismaUp`](./Enums.md) | Integer | The amount of Charisma stat increased or decreased (negative values lower the stat); can be a formula or fixed integer. | 1 | 5 |
| [`IntelligenceUp`](./Enums.md) | Integer | The amount of intelligence increase, which can be a fixed integer or a mathematical expression. | 1 | -1 |
| [`SpeedUp`](./Enums.md) | Integer | Specifies the number of Speed stacks applied, where each stack modifies the unit's turn order and dodge chance. | 1 | 2 |

</details>

---

### Object: `PassiveUntilCastSpell`


**Definition:** Applies the 'PassiveUntilCastSpell' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`HealAlliesEachTurn`](Engine_StatusAndPassiveKeys.md#object-healallieseachturn) | Object | Applies the 'HealAlliesEachTurn' effect. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`StatusAlliesEachTurn`](Items_and_Equipment.md#object-statusallieseachturn) | Object || 1 ||

</details>

---

### Object: `PassiveUntilGetKill`


**Definition:** Applies the 'PassiveUntilGetKill' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`HolyDamageBlessing`](Engine_StatusAndPassiveKeys.md#object-holydamageblessing) | Object | Applies the 'HolyDamageBlessing' effect. | 2 ||

</details>

---

### Object: `PassiveWhenTheAlpha`


**Definition:** State Trigger: Grants nested passives when the alpha.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TogglableRoundEndExtraTurn` | Number | Applies the 'TogglableRoundEndExtraTurn' effect. | 2 ||

</details>

---

### Object: `PassiveWhileInMonkMeleeStance`


**Definition:** Applies the 'PassiveWhileInMonkMeleeStance' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`Brace`](./Enums.md) | Integer | The amount of flat damage reduction applied to the source. | 3 | 2 |
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of health regeneration (HealthRegen) granted by this damage instance. | 1 | 2 |

</details>

---

### Object: `PassiveWhileInMonkRangedStance`


**Definition:** Applies the 'PassiveWhileInMonkRangedStance' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`AddBonusRange`](./Enums.md) | Integer | The number of extra tiles added to the unit's attack range. | 2 | 2 |
| [`AddSpellDamage`](./Enums.md) | Integer || 2 | 2 |
| [`KineticSpikes`](./Enums.md) | Integer | The number of Kinetic Spikes stacks applied, which deal damage back to attackers when the unit is hit. | 1 | 2 |

</details>

---

### Object: `PassiveWhilePreviewingMonkRangedStance`


**Definition:** Applies the 'PassiveWhilePreviewingMonkRangedStance' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`AddBonusRange`](./Enums.md) | Integer | The number of extra tiles added to the unit's attack range. | 2 | 2 |

</details>

---

### Object: `PassiveWhileWearingMetal`


**Definition:** Applies the 'PassiveWhileWearingMetal' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AddElementsToWeapon`](./Enums.md#enum-addelementstoweapon) | Enum | Applies the 'AddElementsToWeapon' effect. | 2 ||

</details>

---

### Object: `RepressedMemoriesMetronome`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ScaledStatusOnSpendMana`](./Passives_and_Statuses.md#context-scaledstatusonspendmana)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Array / Enum | Specifies the loot pool, ability pool, or item category from which an item or effect is selected; can be a specific pool name, table index, or inline array. | 2 ||
| `stacks` | Enum / Integer | The number of stacks, duration, or intensity to apply. | 2 ||

</details>

---

### Object: `ScaledStatusOnOverMana`


**Definition:** Applies the 'ScaledStatusOnOverMana' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`RandomMagicMissile`](./Enums.md) | Integer | The number of random magic missiles fired, each dealing independent damage; can also be an object with custom tooltip data. | 2 | 2 |
| [`Cleanse`](./Enums.md) | Integer | If set to 1, removes all status effects from the target; if 0, no cleanse. | 1 | 0 |

</details>

---

### Object: `ScaledStatusOnSpendMana`


**Definition:** Applies the 'ScaledStatusOnSpendMana' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`RepressedMemoriesMetronome`](Engine_StatusAndPassiveKeys.md#object-repressedmemoriesmetronome) | Object | Applies the 'RepressedMemoriesMetronome' effect. | 2 ||

</details>

---

### Object: `schadenfreude_scaled_stats`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `con` | Enum / Integer | The constitution stat value or modifier for the unit. | 1 ||
| `str` | Enum / Integer || 1 ||

</details>

---

### Object: `SecurityBotProtect`


**Definition:** AI Logic: Guarding behavior for Security Bot units.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 7 ||
| [`move`](./Enums.md#enum-move) | Enum | Determines which movement ability the unit uses. | 5 ||

</details>

---

### Object: `Shadow`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`crit_chance`](./Engine_DamagingKeys.md#valid-property-keys) | `String` | The chance for the damage instance to critically hit, expressed as a percentage (e.g., 50%) or a decimal fraction (e.g., .5). | 2 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||

</details>

---

### Object: `SmiteEnemiesWhoKill`


**Definition:** Applies the 'SmiteEnemiesWhoKill' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | The base damage properties of an attack. | 2 ||
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 2 ||
| [`elements`](./Arrays.md#array-elements) | Array | A list of elemental types applied to the damage instance, such as Heat or Fire, used for weaknesses, resistances, and visual effects. | 2 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `SpecialFriends`


**Definition:** Applies the 'SpecialFriends' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`AllStatsUp`](./Enums.md) | Array / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 2 | [.5] |
| [`HealthGain`](./Enums.md) | Integer / String | The amount of health restored to the source. | 2 | 2*X |

</details>

---

### Object: `StatsAtLowHealth`


**Definition:** Applies the 'StatsAtLowHealth' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`threshold`](Items_and_Equipment.md#object-threshold) | Integer / Object | The health threshold value (absolute or equation) at which this ability becomes available. | 2 | 7 |
| `speed` | Array / Number | The movement speed of the projectile or graphic, as a single number or a range [min max]. | 1 ||
| `strength` | Integer | The base strength stat governing physical damage dealt. | 1 ||

</details>

---

### Object: `StatusAfterCastSpell`


**Definition:** Applies or references the 'StatusAfterCastSpell' effect/state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |
| [`TempSpellDamageUp`](./Enums.md) | Integer | A temporary increase to spell damage output. | 2 | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`TempDamageUp`](./Enums.md) | Integer | The number of temporary damage increase stacks applied to the target for the current turn. | 1 | 2 |

</details>

---

### Object: `StatusAlliesOnBattleStart`


**Definition:** Applies or references the 'StatusAlliesOnBattleStart' effect/state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 9 ||
| [`EquipTemporaryItem`](./Enums.md) | Enum | Specifies the item that is temporarily equipped to the unit. | 2 | FoodMedium |

</details>

---

### Object: `StatusAlliesOnGainCoins`


**Definition:** Event Trigger: Applies nested statuses to allies on gain coins.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`HealthGain`](./Enums.md) | Integer / String | The amount of health restored to the source. | 2 | 2*X |
| [`LuckUp`](./Enums.md) | Integer | Specifies the number of Luck stacks applied, where positive values increase critical hit chance and loot quality and negative values decrease them. | 2 | 2 |
| `scaled` | Boolean || 1 ||

</details>

---

### Object: `StatusAllyWhenAllySpendsMana`


**Definition:** Event Trigger: Applies nested statuses to ally when ally spends mana.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`AllStatsUp`](./Enums.md) | Array / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 2 | [.5] |
| [`threshold`](Items_and_Equipment.md#object-threshold) | Integer / Object | The health threshold value (absolute or equation) at which this ability becomes available. | 2 | 7 |

</details>

---

### Object: `StatusAnyCatAllyWhoKills`


**Definition:** Event Trigger: Applies nested statuses to any cat ally who kills.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusDamagers`


**Definition:** Event Trigger: Applies nested statuses to damagers.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`LuckUp`](./Enums.md) | Integer | Specifies the number of Luck stacks applied, where positive values increase critical hit chance and loot quality and negative values decrease them. | 2 | 2 |
| [`Fear`](./Enums.md) | Array / Integer | The number of Fear stacks applied, which reduces the target's accuracy and may cause it to flee; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | [.15] |

</details>

---

### Object: `StatusEachTurnEndForEachTurn`


**Definition:** Event Trigger: Applies nested statuses to each turn end for each turn.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||
| [`RandomMagicMissile`](./Enums.md) | Integer | The number of random magic missiles fired, each dealing independent damage; can also be an object with custom tooltip data. | 3 | 2 |

</details>

---

### Object: `StatusEachTurnEndPerEnemyKill`


**Definition:** Event Trigger: Applies nested statuses to each turn end per enemy kill.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object | An object or entity name that spawns upon hitting a character, with optional stacks and chance. | 2 | Coin |

</details>

---

### Object: `StatusEnemiesOnDeath`


**Definition:** Event Trigger: Applies nested statuses to enemies on death.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusEveryXTurnBegins`


**Definition:** Event Trigger: Applies nested statuses to every x turn begins.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | The duration of the effect in turns. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`DivineShield`](./Enums.md) | Integer | The number of charges of Divine Shield applied, which blocks the next instances of damage entirely; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 2 | 1 |

</details>

---

### Object: `StatusKillers`


**Definition:** Instantly kills the target if they possess the specified status effects.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusOnAnyDeath`


**Definition:** Event Trigger: Applies nested statuses when any death.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`LuckUp`](./Enums.md) | Integer | Specifies the number of Luck stacks applied, where positive values increase critical hit chance and loot quality and negative values decrease them. | 2 | 2 |

</details>

---

### Object: `StatusOnBattleEndIfKillThresholdMet`


**Definition:** Event Trigger: Applies nested statuses when battle end if kill threshold met.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `kills` | Number || 2 ||
| [`statuses`](Characters_and_Bosses.md#object-statuses) | Object | Defines the status effects applied when the revival or aura triggers. | 2 ||

</details>

---

### Object: `StatusOnBreakItem`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`Shield`](./Enums.md) | Integer / String | Specifies the number of Shield stacks applied, where each stack reduces incoming damage by a flat amount. | 2 | 2 |
| [`Thorns`](./Enums.md) | Integer | The number of Thorns stacks applied, which deals damage back to melee attackers. | 2 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `StatusOnCollectPickup`


**Definition:** Event Trigger: Applies nested statuses when collect pickup.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Tech`](./Enums.md) | Integer | The number of Tech stacks applied, which increase the damage of the next ability used. | 2 | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

---

### Object: `StatusOnDealtDamage`


**Definition:** Event Trigger: Applies nested statuses when dealt damage.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`TempDexterityUp`](./Enums.md) | Integer | A temporary increase to the dexterity stat, specified as an alias or integer. | 2 | 2 |
| [`TempStrengthUp`](./Enums.md) | Integer | Alias for TempStrengthUp; temporarily increases the unit's strength stat. | 2 | 2 |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`TempLuckUp`](./Enums.md) | Integer || 1 | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

---

### Object: `StatusOnDealtDamageThreshold`


**Definition:** Event Trigger: Applies nested statuses when dealt damage threshold.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `count_overkill` | Boolean || 2 ||
| `ignore_during_movement` | Boolean || 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`RefreshMovePoints`](./Enums.md) | Integer | The amount of move points restored to the unit. | 2 | 1 |
| [`Shield`](./Enums.md) | Integer / String | Specifies the number of Shield stacks applied, where each stack reduces incoming damage by a flat amount. | 2 | 2 |
| [`threshold`](Items_and_Equipment.md#object-threshold) | Integer / Object | The health threshold value (absolute or equation) at which this ability becomes available. | 2 | 7 |
| [`AllStatsUp`](./Enums.md) | Array / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 1 | [.5] |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Object: `StatusOnEndMove`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusOnGainShield`


**Definition:** Event Trigger: Applies nested statuses when gain shield.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`Temporary`](Abilities_and_Spells.md#object-temporary) | Object | An object that defines a temporary status effect with duration and expiration conditions. | 2 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Object: `StatusOnHeal`


**Definition:** Event Trigger: Applies nested statuses when heal.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`SpeedUp`](./Enums.md) | Integer | Specifies the number of Speed stacks applied, where each stack modifies the unit's turn order and dodge chance. | 2 | 2 |
| [`RandomStatUp`](./Enums.md) | Integer | The amount of random stat increase (or decrease if negative) applied to a random stat. | 1 | 2 |

</details>

---

### Object: `StatusOnOverMana`


**Definition:** Event Trigger: Applies nested statuses when over mana.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`IntelligenceUp`](./Enums.md) | Integer | The amount of intelligence increase, which can be a fixed integer or a mathematical expression. | 2 | -1 |
| [`SpellDamageUp`](./Enums.md) | Integer | The number of stacks of SpellDamageUp, increasing spell damage dealt by the unit. | 2 | 1 |
| [`DivineShield`](./Enums.md) | Integer | The number of charges of Divine Shield applied, which blocks the next instances of damage entirely; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | 1 |

</details>

---

### Object: `StatusOnPickupCoins`


**Definition:** Event Trigger: Applies nested statuses when pickup coins.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`RefreshMovePoints`](./Enums.md) | Integer | The amount of move points restored to the unit. | 2 | 1 |
| [`DexterityUp`](./Enums.md) | Integer | The amount of Dexterity stat increased or decreased (negative values lower the stat); can be a formula or fixed integer. | 1 | 2 |
| [`SpeedUp`](./Enums.md) | Integer | Specifies the number of Speed stacks applied, where each stack modifies the unit's turn order and dodge chance. | 1 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `StatusOnPopCorpse`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 ||
| [`HealthGain`](./Enums.md) | Integer / String | The amount of health restored to the source. | 3 | 2*X |

</details>

---

### Object: `StatusOnTookDamageFromEnemyAbility`


**Definition:** Event Trigger: Applies nested statuses when took damage from enemy ability.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`Quivered`](./Enums.md) | Integer | The number of stacks of Quivered, which grants bonus attacks; can be an array [stacks, probability]. | 2 | 2 |
| [`MoveQuivered`](./Enums.md) | Integer | Specifies the number of bonus movement points granted; an array `[stacks, probability]` specifies the amount and its chance of application. | 1 | 2 |

</details>

---

### Object: `StatusOnTriggerTrap`


**Definition:** Event Trigger: Applies nested statuses when trigger trap.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`DexterityUp`](./Enums.md) | Integer | The amount of Dexterity stat increased or decreased (negative values lower the stat); can be a formula or fixed integer. | 2 | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`Quivered`](./Enums.md) | Integer | The number of stacks of Quivered, which grants bonus attacks; can be an array [stacks, probability]. | 1 | 2 |

</details>

---

### Object: `StatusOnUseBasicAttack`


**Definition:** Event Trigger: Applies nested statuses when use basic attack.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`FlippedFacingForceAttack`](./Enums.md) | Integer || 2 | 1 |

</details>

---

### Object: `StatusOnUseElementAbility`


**Definition:** Event Trigger: Applies nested statuses when use element ability.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Array / Enum | The specific element type required or applied. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`SpeedUp`](./Enums.md) | Integer | Specifies the number of Speed stacks applied, where each stack modifies the unit's turn order and dodge chance. | 2 | 2 |

</details>

---

### Object: `StatusPerInjury`


**Definition:** Event Trigger: Applies nested statuses to per injury.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cap` | Number || 2 ||
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | `String` || 2 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`Shield`](./Enums.md) | Integer / String | Specifies the number of Shield stacks applied, where each stack reduces incoming damage by a flat amount. | 2 | 2 |
| [`StrengthUp`](./Enums.md) | Integer | Specifies the number of Strength stacks applied, where positive values increase melee damage and negative values decrease it. | 1 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Object: `StatusThingsKnockedBack`


**Definition:** Event Trigger: Applies nested statuses to things knocked back.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Drag` | Number | Applies the 'Drag' effect. | 2 ||

</details>

---

### Object: `StatusWhenAllySpendsMana`


**Definition:** Event Trigger: Applies nested statuses to when ally spends mana.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`OneUseSpellDamageUp`](./Enums.md) | Integer | The magnitude of spell damage increase, consumed after a single spell cast. | 2 | 2 |
| [`ManaGain`](./Enums.md) | Integer | The amount of mana gained; can be a fixed integer or a formula using variables like `X` (e.g., damage dealt or ability cost). | 1 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Object: `TaggedPickupEffectReplacement`


**Definition:** Applies the 'TaggedPickupEffectReplacement' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Array / Enum | The specific entity tag required or applied. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`HealthGain`](./Enums.md) | Integer / String | The amount of health restored to the source. | 2 | 2*X |

</details>

---

### Object: `TowerDefense`


**Definition:** Applies the 'TowerDefense' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | The base damage properties of an attack. | 2 ||
| `range` | Enum / Integer | Distance or area of effect in tiles. | 2 ||

</details>

---

### Object: `Water`


**Definition:** Character Form: Behavior and stats for the \'Water\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AOEPuddle`](./Math_Equations.md) | Equation | Applies the 'AOEPuddle' effect. | 2 ||

</details>

---

### Object: `Wind`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`knockback`](./Math_Equations.md) | Equation | The number of tiles to push the target away from the attacker; can be negative to pull the target closer, or 'str' to scale with the attacker's strength stat. | 2 ||

</details>

---

### Object: `AbilityChargeRefundChance`


**Definition:** Applies the 'AbilityChargeRefundChance' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `advantage_softcap` | Number || 1 ||
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 1 ||

</details>

---

### Object: `AddStatusesIfPersistentWeatherElement`


**Definition:** Applies the 'AddStatusesIfPersistentWeatherElement' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`elements`](./Arrays.md#array-elements) | Array | A list of elemental types applied to the damage instance, such as Heat or Fire, used for weaknesses, resistances, and visual effects. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`Burn`](./Enums.md) | Enum / Integer | The number of Burn stacks applied, which deals fire damage over time; can be an integer, a variable X, or an array `[stacks, probability]` to specify chance of application. | 1 | 2 |

</details>

---

### Object: `AddStatusesToReceivedElementalDamage`


**Definition:** Applies the 'AddStatusesToReceivedElementalDamage' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`elements`](./Arrays.md#array-elements) | Array | A list of elemental types applied to the damage instance, such as Heat or Fire, used for weaknesses, resistances, and visual effects. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`Burn`](./Enums.md) | Enum / Integer | The number of Burn stacks applied, which deals fire damage over time; can be an integer, a variable X, or an array `[stacks, probability]` to specify chance of application. | 1 | 2 |

</details>

---

### Object: `AddStatusToKnockbackDamage`


**Definition:** Modifier: Injects a status effect into a specific action.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `AddStatusToReceivedDamage_ExcludeStatuses`


**Definition:** Applies the 'AddStatusToReceivedDamage_ExcludeStatuses' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `AddStatusToSpells`


**Definition:** Modifier: Injects a status effect into a specific action.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `AddTemporaryEffectsToEquipment`


**Definition:** Applies the 'AddTemporaryEffectsToEquipment' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CastAgain` | Integer / String | Applies the 'CastAgain' effect. | 1 ||

</details>

---

### Object: `Autism`


**Definition:** Applies the 'Autism' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `innate` | Number || 1 ||
| `learned` | Number || 1 ||

</details>

---

### Object: `ChanceToRevive`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | The number of stacks, duration, or intensity to apply. | 5 ||
| [`statuses`](Characters_and_Bosses.md#object-statuses) | Object | Defines the status effects applied when the revival or aura triggers. | 3 ||

</details>

---

### Object: `CollectPickupsOnBattleEnd`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `pop_corpses` | Boolean || 1 ||

</details>

---

### Object: `Conditional_DoesDamage`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToReceivedDamage_ExcludeStatuses`](./Passives_and_Statuses.md#context-addstatustoreceiveddamage_excludestatuses)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution. | 0 | |

</details>

---

### Object: `Conditional_GoodRoll`


**Definition:** Conditional trigger: Executes nested logic based on a randomized favorable outcome probability.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnBegin`](./Passives_and_Statuses.md#context-statuseachturnbegin)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `odds` | Number | The probability (0.0 to 1.0) of triggering the 'good roll' success state. | 37 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 37 ||
| `UseRandomSpell_Madness` | `Number` | Applies the 'UseRandomSpell_Madness' effect. | 1 ||

</details>

---

### Object: `Conditional_SourceHasTag`


**Definition:** Conditional object: Executes nested logic only if the target is/has SourceHasTag.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Array / Enum | The specific entity tag required or applied. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`Conditional_Ally`](Abilities_and_Spells.md#object-conditional_ally) | Object || 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `DamageIfDidntUseSpecificAbility`


**Definition:** Combat Trigger: Deals damage to if didnt use specific ability.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 1 ||
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | The base damage properties of an attack. | 1 ||

</details>

---

### Object: `DelayedWind`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToMeleeDamage`](./Passives_and_Statuses.md#context-addstatustomeleedamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `distance` | Integer | The area of effect or distance in tiles. | 1 ||

</details>

---

### Object: `DelayedWindCone`


**Definition:** Creates a delayed Area of Effect cone.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToMeleeDamage`](./Passives_and_Statuses.md#context-addstatustomeleedamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `distance` | Integer | The area of effect or distance in tiles. | 2 ||

</details>

---

### Object: `Diabetes`


**Definition:** Applies the 'Diabetes' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`AllStatsUp`](./Enums.md) | Array / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 1 | [.5] |
| [`Confusion`](./Enums.md) | Integer | The number of turns of Confusion applied, or an array with duration and chance. | 1 | 2 |

</details>

---

### Object: `EnergyStorm`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cycle_start` | Number || 1 ||
| `period` | Number || 1 ||

</details>

---

### Object: `fire`


**Definition:** Character Form: Behavior and stats for the 'Fire' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#context-damageneighbortileswhencastspell)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | The base damage properties of an attack. | 1 ||
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 1 ||
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 1 ||
| [`elements`](./Arrays.md#array-elements) | Array | A list of elemental types applied to the damage instance, such as Heat or Fire, used for weaknesses, resistances, and visual effects. | 1 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `ForceMoveAway`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusAdjacentOnTheirTurnBegin`](./Passives_and_Statuses.md#context-statusadjacentontheirturnbegin)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `free` | Boolean | If true, the option has no cost and can be chosen freely; or specifies an object for free options. | 1 ||

</details>

---

### Object: `FurnitureStats`


**Definition:** Applies the 'FurnitureStats' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Appeal` | Number | Applies the 'Appeal' effect. | 1 ||
| `Comfort` | Number | Applies the 'Comfort' effect. | 1 ||
| `Stimulation` | Number | Applies the 'Stimulation' effect. | 1 ||

</details>

---

### Object: `ice`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#context-damageneighbortileswhencastspell)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | The base damage properties of an attack. | 1 ||
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 1 ||
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 1 ||
| [`elements`](./Arrays.md#array-elements) | Array | A list of elemental types applied to the damage instance, such as Heat or Fire, used for weaknesses, resistances, and visual effects. | 1 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `lightning`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#context-damageneighbortileswhencastspell)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | The base damage properties of an attack. | 1 ||
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 1 ||
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 1 ||
| [`elements`](./Arrays.md#array-elements) | Array | A list of elemental types applied to the damage instance, such as Heat or Fire, used for weaknesses, resistances, and visual effects. | 1 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `MegaMinions`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cycle_start` | Number || 1 ||
| `stacks` | Enum / Integer | The number of stacks, duration, or intensity to apply. | 1 ||

</details>

---

### Object: `MoveWhenDamaged`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`weights`](./Enums.md#enum-weights) | Array / Enum | An array of three weighting values or a named preset for Crazy Eye background behavior weights. | 9 ||

</details>

---

### Object: `PassiveLevelScaledStatus`


**Definition:** Applies the 'PassiveLevelScaledStatus' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`SizeScalePercent`](./Math_Equations.md) | Equation | Applies the 'SizeScalePercent' effect. | 1 ||
| [`Shield`](./Enums.md) | Integer / String | Specifies the number of Shield stacks applied, where each stack reduces incoming damage by a flat amount. | 1 | 2 |
| [`Trample`](./Enums.md) | Array / Integer | The number of tiles this character can move through enemies, dealing damage or applying effects equal to the value. | 1 | [3] |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Object: `RandomPassivePool`


**Definition:** Logic: Grants a random passive from the specified pool upon spawning.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||
| [`PassiveGroup`](Characters_and_Bosses.md#object-passivegroup) | Object | Defines a grouping of passives that can be randomly selected from the passive pool. | 2 ||

</details>

---

### Object: `ReplaceBrain`


**Definition:** Applies the 'ReplaceBrain' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`brain`](./Enums.md#enum-brain) | Enum | Specifies the AI brain type (e.g., NoBrain, PlayerBrain, GenericBrain). | 4 ||
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | Specifies the preset decision weight set (e.g., careless, zombie) for the AI. | 4 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 4 ||

</details>

---

### Object: `Robot`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allow_energize_self` | Boolean || 2 ||

</details>

---

### Object: `ScaledStatusOnBleedDamage`


**Definition:** Applies the 'ScaledStatusOnBleedDamage' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`Charge`](./Enums.md) | Integer | The number of stacks of Charge, which makes the caster gain 1 Mana per stack at the start of its next turn. | 1 | 2 |

</details>

---

### Object: `ScaledStatusOnLoseShield`


**Definition:** Applies the 'ScaledStatusOnLoseShield' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`Thorns`](./Enums.md) | Integer | The number of Thorns stacks applied, which deals damage back to melee attackers. | 1 | 2 |

</details>

---

### Object: `ScaledStatusOnOverHealed`


**Definition:** Applies the 'ScaledStatusOnOverHealed' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SpawnScaledRotFly` | Number | Applies the 'SpawnScaledRotFly' effect. | 1 ||

</details>

---

### Object: `SelfDamageWhenDealDamage`


**Definition:** Applies the 'SelfDamageWhenDealDamage' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | The base damage properties of an attack. | 1 ||
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 1 ||

</details>

---

### Object: `StackingDodgeChanceOnTookDamage`


**Definition:** Applies the 'StackingDodgeChanceOnTookDamage' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `amount` | Array | The numerical quantity. | 1 ||
| `cap` | Number || 1 ||

</details>

---

### Object: `StatusAdjacentOnTheirTurnBegin`


**Definition:** Event Trigger: Applies nested statuses to adjacent on their turn begin.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusAlliesEachTurn`


**Definition:** Applies or references the 'StatusAlliesEachTurn' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveUntilCastSpell`](./Passives_and_Statuses.md#context-passiveuntilcastspell)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| `exclude_self` | Boolean || 1 ||
| [`RandomStatUp`](./Enums.md) | Integer | The amount of random stat increase (or decrease if negative) applied to a random stat. | 1 | 2 |

</details>

---

### Object: `StatusAlliesOnSpendMana`


**Definition:** Event Trigger: Applies nested statuses to allies on spend mana.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusAlliesScaledByCursedOnDeath`


**Definition:** Event Trigger: Applies nested statuses to allies scaled by cursed on death.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`LuckUp`](./Enums.md) | Integer | Specifies the number of Luck stacks applied, where positive values increase critical hit chance and loot quality and negative values decrease them. | 1 | 2 |

</details>

---

### Object: `StatusIfBattleAlreadyBegan`


**Definition:** Event Trigger: Applies nested statuses to if battle already began.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`PermanentMadness`](./Enums.md) | Integer | If set to 1, the Madness status is permanent and will never expire; can use an alias for the status. | 1 | 1 |

</details>

---

### Object: `StatusOnEatPill`


**Definition:** Examples: `{ ... }`  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusOnLoseShield`


**Definition:** Event Trigger: Applies nested statuses when lose shield.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`Thorns`](./Enums.md) | Integer | The number of Thorns stacks applied, which deals damage back to melee attackers. | 1 | 2 |

</details>

---

### Object: `StatusOnTakeHealthDamage`


**Definition:** Event Trigger: Applies nested statuses when take health damage.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`PermanentConstitution`](./Enums.md) | Integer | The amount of permanent Constitution (max HP) added. | 1 | -1 |

</details>

---

### Object: `StatusOnTurnEndIfDidntCastAbilityTypes`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 5 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 ||
| [`ManaGain`](./Enums.md) | Integer | The amount of mana gained; can be a fixed integer or a formula using variables like `X` (e.g., damage dealt or ability cost). | 1 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Object: `StrengthInNumbersAura`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `count_self` | Boolean || 1 ||
| `stacks` | Enum / Integer | The number of stacks, duration, or intensity to apply. | 1 ||

</details>

---

### Object: `Study`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `marked` | Number || 1 ||
| `stacks` | Enum / Integer | The number of stacks, duration, or intensity to apply. | 1 ||

</details>

---

### Object: `TakeBonusTurnWithStatus`


**Definition:** Grants the character an immediate extra turn while afflicted with specific statuses.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnKill`](./Passives_and_Statuses.md#context-statusonkill)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 ||
| [`Madness`](./Enums.md) | Integer | Specifies the number of Madness stacks applied, which cause the target to act randomly or attack allies; can be an integer, array `[stacks, probability]`, or a keyword alias. | 3 | 1 |

</details>

---

### Object: `TheHunger`


**Definition:** Applies the 'TheHunger' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`Madness`](./Enums.md) | Integer | Specifies the number of Madness stacks applied, which cause the target to act randomly or attack allies; can be an integer, array `[stacks, probability]`, or a keyword alias. | 1 | 1 |

</details>

---

### Object: `TileDamageMultiplier`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ally_multiplier` | Number || 1 ||
| `multiplier` | Number | Multiplicative modifier to a base value. | 1 ||

</details>

---

### Object: `TourettesMeows`


**Definition:** Applies the 'TourettesMeows' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cooldown`](./Arrays.md#array-cooldown) | Array || 1 ||
| [`pool`](./Arrays.md#array-pool) | Array / Enum | Specifies the loot pool, ability pool, or item category from which an item or effect is selected; can be a specific pool name, table index, or inline array. | 1 ||

</details>

---

### Object: `triattack`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#context-damageneighbortileswhencastspell)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | The base damage properties of an attack. | 1 ||
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 1 ||
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 1 ||
| [`elements`](./Arrays.md#array-elements) | Array | A list of elemental types applied to the damage instance, such as Heat or Fire, used for weaknesses, resistances, and visual effects. | 1 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

---


<details>
<summary><b>AddSelfStatusToWeapons</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

<details>
<summary><b>AddStatusToAllDamage</b></summary>

> **Total Count:** 16

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

<details>
<summary><b>AddStatusToBasicAttackWithCooldown</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

<details>
<summary><b>AddStatusToFirstBasicAttack</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

<details>
<summary><b>AddStatusToKnockbackDamage</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

<details>
<summary><b>AddStatusToMeleeDamage</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

<details>
<summary><b>AddStatusToReceivedDamage_ExcludeStatuses</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

<details>
<summary><b>AddStatusToSpells</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

<details>
<summary><b>AddStatusToTrampleDamage</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

<details>
<summary><b>Conditional_Adjacent</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

<details>
<summary><b>Conditional_DoesDamage</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

<details>
<summary><b>Conditional_GoodRoll</b></summary>

> **Total Count:** 30

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

<details>
<summary><b>Conditional_NotBoss</b></summary>

> **Total Count:** 13

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

<details>
<summary><b>Conditional_PartyMember</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

<details>
<summary><b>Conditional_Shielded</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

<details>
<summary><b>ExtraStatusWhenDealingDamage</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

<details>
<summary><b>NextBattleStatus</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

<details>
<summary><b>PassiveLevelScaledStatus</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

<details>
<summary><b>StatusAdjacentOnTheirTurnBegin</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

<details>
<summary><b>StatusAlliesOnSpendMana</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

<details>
<summary><b>StatusAnyCatAllyWhoKills</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

<details>
<summary><b>StatusEnemiesOnDeath</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

<details>
<summary><b>StatusKilledCharacters</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

<details>
<summary><b>StatusKillers</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

<details>
<summary><b>StatusOnDealtDamage</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

<details>
<summary><b>StatusOnEatPill</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

<details>
<summary><b>StatusOnEndMove</b></summary>

> **Total Count:** 9

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

<details>
<summary><b>StatusOnOverHealed</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>


## Discovered Objects

> These tables were auto-generated by the schema audit tool. They document objects found in the `.gon` files that were not previously documented.

### Object: `AIControlNextTurn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `include_spells` | Boolean || 1 | `true` (Boolean) |
| `stacks` | Enum / Integer | The number of stacks or formula for the status effect applied. | 1 | `1` (Number) |


### Object: `AbilityHealthThreshold`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 13 | `FormShrinkFour` (Enum), `DybbukPossess` (Enum) |
| [`threshold`](Items_and_Equipment.md#object-threshold) | Enum / Integer / Object | The health threshold value (absolute or equation) at which this ability becomes available. | 12 | `1*champion_multiplier` (Enum), `3*champion_multiplier` (Enum), `200` (Number), `1` (Number), `"max(X*.33, 5)"` (String), `"max(X*.5, 1)"` (String) |
| `even_if_stunned` | Boolean | If true, the reaction triggers even if the unit is stunned. | 7 | `true` (Boolean) |
| `immediate` | Boolean | If true, the forced attack executes immediately without waiting. | 6 | `true` (Boolean) |
| `use_ai` | Boolean | If true, the AI decides whether to use the ability when the threshold is met. | 2 | `true` (Boolean) |
| `also_use_if_buddy_is_dead` | Boolean | If true, the ability can still be used at threshold if the unit's buddy is dead. | 1 | `true` (Boolean) |
| `aux` | Integer | An integer modifier for the auxiliary stat, often used for scaling or effect values. | 1 | `25` (Number) |
| `threshold_min` | Enum | Specifies the minimum health threshold (as an equation) for the ability to be available. | 1 | `X` (Enum) |


### Object: `AbilityOnRoundEnd`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 2 | `DestroyerRaise` (Enum) |
| `force_display_name` | Boolean | If true, forces the display of the ability name even if it would otherwise be hidden. | 2 | `true` (Boolean) |


### Object: `AbilityOnRoundEndOnce`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 1 | `wp_SignalAmplifierSpawnTerminator` (Enum) |
| `even_of_stunned` | Boolean || 1 | `true` (Boolean) |


### Object: `AddAdvantageToEvent`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `add` | Array / Integer || 1 | `5` (Number) |
| `options` | Array || 1 | `[smash bash open]` (Array) |
| `type` | Enum | Specifies the damage type or trigger context (e.g., 'event', 'melee', 'battle'). | 1 | `treasure_box` (Enum) |


### Object: `AddStatusToBackstabs`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Bleed` | Array / Integer | The number of Bleed stacks applied, which deals bleeding damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | `[1 .1]` (Array), `[3 .1]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |


### Object: `AddStatusToFirstSpellEachTurn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_IsSelf`](Abilities_and_Spells.md#object-conditional_isself) | Object || 1 | `{ ... }` (Object) |
| [`Else`](Abilities_and_Spells.md#object-else) | Object | An object containing effects that apply when the parent conditional condition is not met. | 1 | `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |


### Object: `AddStatusToReceivedDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_IsPhysicalAttack`](Characters_and_Bosses.md#object-conditional_isphysicalattack) | Object || 1 | `{ ... }` (Object) |
| [`Else`](Abilities_and_Spells.md#object-else) | Object | An object containing effects that apply when the parent conditional condition is not met. | 1 | `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |


### Object: `AfterImage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `object` | Array / Enum | Specifies the template identifier of the entity to spawn, referencing a predefined character or object in the game data. | 2 | `PlayerCat_ThiefShade` (Enum) |
| `skilltemp` | Boolean || 2 | `true` (Boolean) |


### Object: `AggroTargetIsGovernedByHitEffect`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `enemies_only` | Boolean | If true, this effect only targets enemies. | 1 | `false` (Boolean) |


### Object: `AllStatsAura`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `aura_requires_tag` | Enum | Specifies the tag required for units to be affected by the all-stats aura. | 1 | `humanoid` (Enum) |
| `range` | Enum / Integer | The range (in tiles) of the aura, or 'global' for infinite range. | 1 | `global` (Enum) |
| `stacks` | Enum / Integer | The number of stacks or formula for the status effect applied. | 1 | `1` (Number) |


### Object: `AllStatsUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `AlluringDoodieEater`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number | A multiplier or percentage representing the probability of the effect occurring. | 1 | `10` (Number) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | A damage instance object that defines the damage, type, effects, and AI scoring for an ability. | 1 | `{ ... }` (Object) |


### Object: `AllyDodgeChanceAura`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number | A multiplier or percentage representing the probability of the effect occurring. | 1 | `25` (Number) |
| `range` | Enum / Integer | The range (in tiles) of the aura, or 'global' for infinite range. | 1 | `1` (Number) |


### Object: `AlphaAllStatsUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `AlphaCat`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `Ammo`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `ArmorBreakOnHit`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance_to_break` | Integer || 2 | `10` (Number), `5` (Number) |
| `durability_loss` | Integer || 2 | `0` (Number) |


### Object: `ArmorPickup`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `frame_range` | Array | Specifies the animation frame range (start and end) for the pickup's sprite. | 3 | `[6 6]` (Array), `[1 2]` (Array) |
| `stacks` | Enum / Integer | The number of stacks or formula for the status effect applied. | 3 | `4` (Number), `6` (Number) |


### Object: `BackflipWhenTargeted`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 7 | `Teleport` (Enum), `SZBBackflipDodge` (Enum) |
| `stacks` | Enum / Integer | The number of stacks or formula for the status effect applied. | 7 | `4` (Number), `1` (Number) |


### Object: `BaitAura`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `range` | Enum / Integer | The range (in tiles) of the aura, or 'global' for infinite range. | 4 | `3` (Number) |


### Object: `BattlefieldUniqueRandomPassive`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DemonicGlyph_Bite` | Integer || 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `DemonicGlyph_Bounce` | Integer || 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `DemonicGlyph_Fire` | Integer || 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `DemonicGlyph_Movement` | Integer || 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `DemonicGlyph_Summon` | Integer || 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |


### Object: `Bird`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `BirdRewards`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ally_rewards`](Characters_and_Bosses.md#object-ally_rewards) | Object || 18 | `{ ... }` (Object) |
| [`statuses`](Characters_and_Bosses.md#object-statuses) | Object | Defines the status effects applied when the revival or aura triggers. | 5 | `{ ... }` (Object) |


### Object: `BlastResistance`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `Bleed`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `BleedThorns`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `Blind`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `BoostDamageAura`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `BoostDamageGlobalAura`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `BossRewards`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `common` | Enum | Specifies the common reward table or specific reward given. | 20 | `RatBomb` (Enum), `ChubsCollar` (Enum) |
| `rare` | Enum | Specifies the rare reward table or specific reward given. | 16 | `BorisBrain` (Enum), `JohnnysStool` (Enum) |


### Object: `Brace`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `BraceForEachNeighboringEnemy`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `Brittle`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `BrittleDuringElement`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `Bruise`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `Buddy`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allies_only` | Boolean | If true, the Buddy effect only targets allies. | 3 | `false` (Boolean) |
| `obj` | Array / Enum | The object(s) spawned when this passive triggers. | 3 | `ZaratanaVS` (Enum), `PyrophinaVS` (Enum) |
| `reclaim_if_lost` | Boolean | If true, the Buddy will attempt to be reclaimed if it becomes lost. | 1 | `true` (Boolean) |


### Object: `BuffImmunity`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exclude` | Enum | Specifies an element type that is excluded from triggering the form change. | 1 | `SpellDamageUp` (Enum) |


### Object: `BungaCheers`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ally_damage` | Enum | Specifies the cheering animation to play when an ally takes damage. | 1 | `littleboo` (Enum) |
| `ally_dead` | Enum | Specifies the cheering animation to play when an ally dies. | 1 | `bigboo` (Enum) |
| `enemy_damage` | Enum | Specifies the cheering animation to play when an enemy takes damage. | 1 | `littlecheer` (Enum) |
| `enemy_dead` | Enum | Specifies the cheering animation to play when an enemy dies. | 1 | `bigcheer` (Enum) |
| `warrior_tag` | Enum | Specifies the tag used to identify summoned warriors for the Bunga entrance sequence. | 1 | `bungawarrior` (Enum) |


### Object: `BungaEntrance`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 2 | `BungaEntrance` (Enum), `BecomeTheDestroyer` (Enum) |
| `even_if_stunned` | Boolean | If true, the reaction triggers even if the unit is stunned. | 2 | `true` (Boolean) |
| `health_threshold` | Integer | The health threshold (absolute HP value) that triggers the reaction. Use -1 for no threshold. | 2 | `150` (Number), `-1` (Number) |
| `warrior_tag` | Enum | Specifies the tag used to identify summoned warriors for the Bunga entrance sequence. | 2 | `bungawarrior` (Enum), `finalboss_clonecat` (Enum) |


### Object: `Burn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `CatPartsSizeScale`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `head` | Enum / Number | The visual ID (integer) of the head part applied to the cat. | 1 | `1.3` (Number) |


### Object: `CatPartsTransform`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `palette` | Enum / Integer | Index or list of palette indices used for coloring the entity or its variations. | 17 | `Fighter` (Enum), `Medic` (Enum), `76` (Number), `78` (Number) |
| `ear1` | Integer || 13 | `1501` (Number), `343` (Number) |
| `tail` | Integer | The visual ID (integer) of the tail part applied to the cat. | 13 | `1504` (Number), `1503` (Number) |
| `arm2` | Number | The visual ID (integer/number) of the second arm part applied to the cat. | 11 | `1013` (Number), `1501` (Number) |
| `arm1` | Number | The visual ID (integer/number) of the first arm part applied to the cat. | 10 | `1043` (Number), `1013` (Number) |
| `ear2` | Integer | The visual ID (integer) of the second ear part applied to the cat. | 10 | `1005` (Number), `1501` (Number) |
| `leg1` | Integer | The visual ID (integer) of the first leg part applied to the cat. | 8 | `41` (Number), `1043` (Number) |
| `leg2` | Integer | The visual ID (integer) of the second leg part applied to the cat. | 8 | `41` (Number), `1043` (Number) |
| `mouth` | Number | The visual ID (number) of the mouth part applied to the cat. | 8 | `1005` (Number), `1069` (Number) |
| `head` | Enum / Number | The visual ID (integer) of the head part applied to the cat. | 6 | `1027` (Number), `1504` (Number) |
| `texture` | Integer | The visual ID (integer) of the texture applied to the cat. | 6 | `322` (Number), `19` (Number) |
| `body` | Number | The visual ID (number) of the body part applied to the cat. | 5 | `31` (Number), `1029` (Number) |
| `eye1` | Integer | The visual ID (integer) of the first eye part applied to the cat. | 3 | `1013` (Number), `1069` (Number) |
| `eye2` | Integer | The visual ID (integer) of the second eye part applied to the cat. | 3 | `1013` (Number), `1069` (Number) |
| `eyebrow1` | Integer | The visual ID (integer) of the first eyebrow part applied to the cat. | 1 | `1069` (Number) |
| `eyebrow2` | Integer | The visual ID (integer) of the second eyebrow part applied to the cat. | 1 | `1070` (Number) |


### Object: `CaveFamilyEnrage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 6 | `CaveCatEnrageTwo` (Enum), `CaveCatEnrageOne` (Enum) |
| `count` | Array / Integer | The number of times or items to generate, spawn, or apply. | 6 | `1` (Number), `0` (Number) |
| `tag` | Array / Enum | Specifies the name of the tag to check for on the target. | 6 | `cavefamily` (Enum) |


### Object: `CerberubsAggroTargetBehavior`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alert_form` | Enum | Specifies the form to switch to when the Cerberubs unit is alerted. | 1 | `Alert` (Enum) |
| `default_form` | Enum | Specifies the default form for the Cerberubs unit. | 1 | `Normal` (Enum) |


### Object: `ChainKnockback`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `ChanceToBlockAndCounter`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `backstab_only` | Boolean || 1 | `true` (Boolean) |
| `chance` | Number | A multiplier or percentage representing the probability of the effect occurring. | 1 | `100` (Number) |


### Object: `ChanceToForceEvent`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number | A multiplier or percentage representing the probability of the effect occurring. | 1 | `25` (Number) |
| `event` | Enum || 1 | `Blessing` (Enum) |


### Object: `ChanceToFormChangeOnAbilityDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number | A multiplier or percentage representing the probability of the effect occurring. | 1 | `15` (Number) |
| `form` | Enum / Integer | Specifies the form name (e.g., "Big", "Small", "Angry") the unit transforms into. | 1 | `Flop2` (Enum) |


### Object: `ChanceToSpitOnDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 7 | `MoonHandDrop` (Enum), `SpewerSpit` (Enum) |
| `flat_chance` | Integer | The flat percentage chance to spit when damaged. | 5 | `100` (Number), `50` (Number) |
| `chance_per_damage` | Integer | The percentage chance to spit per point of damage taken. | 3 | `0` (Number), `2` (Number) |
| `backstabs_only` | Boolean | If true, this reaction only triggers when the unit is backstabbed. | 1 | `true` (Boolean) |
| `even_on_0_damage_if_knockback` | Boolean | If true, this reaction triggers on zero-damage hits if knockback occurred. | 1 | `true` (Boolean) |


### Object: `ChaosBossFormChangeGuide`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `active_pieces` | Array | The list of active boss piece names that are used in the Chaos boss fight. | 1 | `[Johnny Throb Flush]` (Array) |
| `passive_pieces` | Array | The list of passive boss piece names that are used in the Chaos boss fight. | 1 | `[Host Nettle Bubs]` (Array) |
| `passives_health_threshold` | Integer | The health percentage threshold at which the Chaos boss's passive pieces activate. | 1 | `50` (Number) |


### Object: `ChaosBossPieces`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `active_pieces` | Array | The list of active boss piece names that are used in the Chaos boss fight. | 1 | `[Johnny Throb Flush]` (Array) |
| `passive_pieces` | Array | The list of passive boss piece names that are used in the Chaos boss fight. | 1 | `[Host Nettle Bubs]` (Array) |


### Object: `ChaosHeadDropIn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 1 | `ChaosSpawnIn` (Enum) |
| `new_music` | Enum | Specifies the music track to play when the Chaos head drops in. | 1 | `chaos_boss_part2` (Enum) |
| `tag` | Array / Enum | Specifies the name of the tag to check for on the target. | 1 | `riftheadguardian` (Enum) |


### Object: `CharacterLightSource`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `color` | Array | An RGB color array or named color used for this visual effect. | 16 | `[.7 .8 .9]` (Array), `[1 1 1]` (Array) |
| `size` | Enum / Number | A scale multiplier for the spawned entity's visual size, specified as a single value or a randomized range [min, max]; 'gemini' uses a special sizing mode. | 16 | `1.7` (Number), `8` (Number) |
| `glow` | Array | Specifies the RGBA color values for the character's glow effect. | 8 | `[1 .75 .5 .5]` (Array), `[1 1 1 1]` (Array) |


### Object: `Charge`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `CharmAllFlies`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `CherubimReaction`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Leave`](Engine_LogicKeys.md#object-leave) | Enum / Object || 2 | `LELeave` (Enum), `CherubimLeave` (Enum), `{ ... }` (Object) |
| [`Return`](Engine_LogicKeys.md#object-return) | Enum / Object || 2 | `CherubimReturn` (Enum), `LEReturn` (Enum), `{ ... }` (Object) |


### Object: `Conductor`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |


### Object: `Confusion`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `ConjureBonusAbility`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 2 | `Class` (Enum), `Colorless` (Enum) |
| `upgraded` | Boolean | If true, the ability evolution uses an upgraded version or state instead of the base one. | 2 | `true` (Boolean) |


### Object: `Consumed`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `mount_mode` | Boolean / Enum || 12 | `true` (Boolean), `auto` (Enum) |
| `drop_on_death` | Boolean / Enum | Specifies whether and how the consumed unit is dropped upon death. "deferred" delays the drop, "true" forces it, "false" prevents it. | 11 | `false` (Boolean), `true` (Boolean), `deferred` (Enum) |


### Object: `ConvertDamageToScaledStatus`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DelayedPain` | Integer | The number of stacks of DelayedPain, which deals damage to the unit after a delay (e.g., at the end of its next turn). | 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `stacks` | Enum / Integer | The number of stacks or formula for the status effect applied. | 1 | `3` (Number) |


### Object: `CounterAttack`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 5 | `StegoTailSwipe` (Enum), `neck_TentacleArmorCounter` (Enum) |
| `chance` | Number | A multiplier or percentage representing the probability of the effect occurring. | 1 | `15` (Number) |
| `melee_only` | Boolean || 1 | `true` (Boolean) |
| `ranged_only` | Boolean | If true, this reaction only triggers from ranged attacks. | 1 | `true` (Boolean) |
| `without_orienting` | Boolean | If true, the counterattack is performed without reorienting the unit. | 1 | `true` (Boolean) |


### Object: `CounterNextAttacks`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `CreateGlobalModifiers`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`BloodRain`](Engine_GlobalModifierKeys.md#object-bloodrain) | Integer / Object | If set to 1, enables a blood rain visual effect globally. | 3 | `1` (Number), `{ ... }` (Object) |
| [`LowerAmbientLight`](Abilities_and_Spells.md#object-lowerambientlight) | Object || 3 | `50` (Number), `33` (Number), `{ ... }` (Object) |


### Object: `CritChanceUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `CyborgTurns`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`TakeBonusTurnWithAIControl`](Abilities_and_Spells.md#object-takebonusturnwithaicontrol) | Object || 1 | `{ ... }` (Object) |
| `stacks` | Enum / Integer | The number of stacks or formula for the status effect applied. | 1 | `1` (Number) |


### Object: `DamageUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `DeathChill`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `DeathRattleRevive`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 8 | `HitlerPulp2` (Enum), `HitlerPulp4` (Enum) |
| `even_if_stunned` | Boolean | If true, the reaction triggers even if the unit is stunned. | 8 | `true` (Boolean) |


### Object: `DejaVu`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `DelayedAutoRevive`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `health` | Integer | The unit's base health, specified as an absolute integer or a percentage modifier. | 6 | `30` (Number), `15` (Number) |
| `rounds` | Integer | The number of rounds the unit must wait before reviving. | 6 | `1` (Number), `2` (Number) |


### Object: `DepressionAura`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `aura_effects_allies` | Boolean | If false, the aura does not affect allied units. | 4 | `false` (Boolean) |
| `range` | Enum / Integer | The range (in tiles) of the aura, or 'global' for infinite range. | 4 | `global` (Enum), `1` (Number) |
| `stacks` | Enum / Integer | The number of stacks or formula for the status effect applied. | 4 | `1` (Number) |


### Object: `DiceBehavior`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dice_size` | Integer | The number of sides on the die used by the dice behavior. | 1 | `6` (Number) |
| `knockback_damage` | Integer | The amount of damage dealt to the target upon knockback. | 1 | `5` (Number) |


### Object: `DiesToElement`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `element` | Array / Enum || 1 | `Fire` (Enum) |
| `instant` | Boolean | If true, the consumption (e.g., grabbing, eating) happens instantly without animation delay. | 1 | `true` (Boolean) |


### Object: `DiesToPiercingAndSpikes`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `deferred` | Boolean | If true, the death is deferred until the end of the current action. | 1 | `true` (Boolean) |


### Object: `DirtyClaws`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `DivineShield`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `DodgeChance_Status`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `DodgeWhenTargeted`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 1 | `ShadowstepDodge` (Enum) |


### Object: `Doomed`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `DukeOfFlies`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `DurabilityTransform`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `eq` | Array || 7 | `[2 EstusFlask_Half]` (Array), `[0 JarOfNothing]` (Array) |
| `ge` | Array || 4 | `[3 EstusFlask_Full]` (Array), `[2 WaterBottle_Full]` (Array) |


### Object: `DybbukPossessionFallback`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exit_ability` | Enum | Specifies the ability used to exit the possession state. | 1 | `DybbukReturn` (Enum) |
| `form` | Enum / Integer | Specifies the form name (e.g., "Big", "Small", "Angry") the unit transforms into. | 1 | `Possessing` (Enum) |


### Object: `Dyslexia`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |


### Object: `Empath`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |


### Object: `ExtraBasicAttacks_Status`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `ExtraBasicMoves_Status`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `FaceAwayLastDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability_damage_only` | Boolean | If true, this reaction only triggers from damage caused by abilities. | 1 | `true` (Boolean) |
| `override_hit_animation` | Boolean | If true, overrides the default hit animation with a custom one. | 1 | `true` (Boolean) |
| `use_turn_animations` | Boolean | If true, uses the unit's turn animations for the face-last-damage effect. | 1 | `true` (Boolean) |


### Object: `FaceLastDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `use_turn_animations` | Boolean | If true, uses the unit's turn animations for the face-last-damage effect. | 1 | `true` (Boolean) |


### Object: `FinalBossBeamQueue`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `queue` | Enum | Specifies the ability or animation to queue for the beam attack. | 1 | `TheChild_TargetBeam` (Enum) |
| `release` | Enum | Specifies the ability or animation to release the queued beams. | 1 | `TheChild_ReleaseBeams` (Enum) |
| `transform` | Enum | Specifies the ability or animation to transform the boss into another form. | 1 | `TheChild_TransformBoris` (Enum) |


### Object: `FinalBossBecomeTheChild`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `GlobalSpawnCharacter` | Enum || 1 | `MegaGuppy` (Enum) |
| `PlayBackground` | Integer || 1 | `1` (Number), `0` (Number) |
| [`SwitchMusic`](Abilities_and_Spells.md#object-switchmusic) | Object || 1 | `{ ... }` (Object) |


### Object: `FinalBossHitCountdownBoris`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object | Determines which ability the target is forced to cast immediately, ignoring normal costs and cooldowns. | 1 | `neck_ChefsApron` (Enum), `TheChild_TransformExplosive` (Enum), `{ ... }` (Object) |
| `icon` | Integer | The ID of the icon displayed on the countdown overlay. | 1 | `802` (Number) |
| `icon_ready` | Integer | The ID of the icon displayed when the countdown is ready. | 1 | `803` (Number) |
| `stacks` | Enum / Integer | The number of stacks or formula for the status effect applied. | 1 | `7` (Number) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |


### Object: `FinalBossHitCountdownExplosive`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object | Determines which ability the target is forced to cast immediately, ignoring normal costs and cooldowns. | 1 | `neck_ChefsApron` (Enum), `head_HitlersToupe` (Enum), `{ ... }` (Object) |
| `icon` | Integer | The ID of the icon displayed on the countdown overlay. | 1 | `800` (Number) |
| `icon_ready` | Integer | The ID of the icon displayed when the countdown is ready. | 1 | `801` (Number) |
| `stacks` | Enum / Integer | The number of stacks or formula for the status effect applied. | 1 | `7` (Number) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |


### Object: `FinalBossHitCountdownHoly`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon` | Integer | The ID of the icon displayed on the countdown overlay. | 1 | `804` (Number) |
| `icon_ready` | Integer | The ID of the icon displayed when the countdown is ready. | 1 | `805` (Number) |
| `stacks` | Enum / Integer | The number of stacks or formula for the status effect applied. | 1 | `7` (Number) |


### Object: `FinalBossPupils`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `look_at_offset` | Array | A 3D vector offset for the look-at target position. | 1 | `[0 2.5 0]` (Array) |
| `radius` | Array / Integer || 1 | `13` (Number) |
| `reset_center_because_no_target_halflife` | Number | The halflife in seconds for resetting pupil center when no target exists. | 1 | `.1` (String) |
| `reset_center_because_of_animation_halflife` | Number | The halflife in seconds for resetting pupil center due to animation interruption. | 1 | `.05` (String) |
| `teleport_tracking_halflife` | Number | The halflife in seconds for updating pupil tracking after a teleport. | 1 | `.01` (String) |
| `tracking_acquisition_halflife` | Number | The halflife in seconds for acquiring a new tracking target. | 1 | `.1` (String) |
| `virtual_head_position` | Array | A 3D vector defining the virtual head position used for pupil calculations. | 1 | `[11 2 11]` (Array) |


### Object: `FinalBossShieldHealth`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `break_ability` | Enum | Specifies the ability used to break the shield. | 1 | `DestroyerBreakShield` (Enum) |
| `state_health` | Array | An array of health thresholds corresponding to different shield states. | 1 | `[0 35 35 35 35 0]` (Array) |


### Object: `FinalBossSyncAnimations`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `other_character` | Enum | Specifies the other character to synchronize animations with. | 1 | `MegaGuppy` (Enum) |
| [`other_form_change_abilities`](Characters_and_Bosses.md#object-other_form_change_abilities) | Object || 1 | `{ ... }` (Object) |


### Object: `Flammable`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `FlyDamageIncrease`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allies_only` | Boolean | If true, the Buddy effect only targets allies. | 1 | `true` (Boolean) |
| `stacks` | Enum / Integer | The number of stacks or formula for the status effect applied. | 1 | `2` (Number) |


### Object: `Flying`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `FollowUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `FormChangeDuringWeatherElement`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `element` | Array / Enum || 2 | `Water` (Enum) |
| `form` | Enum / Integer | Specifies the form name (e.g., "Big", "Small", "Angry") the unit transforms into. | 2 | `Rain` (Enum) |


### Object: `FormChangeHealthThreshold`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `form_above` | Enum | Specifies the form to change into when health is above the threshold. | 3 | `Default` (Enum), `Full` (Enum) |
| `form_below` | Enum | Specifies the form to change into when health is below the threshold. | 3 | `DesireMech` (Enum), `Standing2` (Enum) |
| [`threshold`](Items_and_Equipment.md#object-threshold) | Enum / Integer / Object | The health threshold value (absolute or equation) at which this ability becomes available. | 3 | `X-4` (Enum), `25` (Number), `50` (Number) |
| `count_shield` | Boolean | If true, shields are counted as health when evaluating the health threshold for form changes. | 1 | `true` (Boolean) |


### Object: `FormChangeOffMap`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `form_offmap` | Enum | Specifies the form to use when the unit is off the map. | 8 | `Insane_Ceiling` (Enum), `SpawningPhase` (Enum) |
| `form_onmap` | Enum | Specifies the form to use when the unit is on the map. | 8 | `Default_Ground` (Enum), `Insane_Ground` (Enum) |


### Object: `FormChangeOnElementInfluence`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `element` | Array / Enum || 9 | `[fire]` (Array), `water` (Enum), `wind` (Enum) |
| `form` | Enum / Integer | Specifies the form name (e.g., "Big", "Small", "Angry") the unit transforms into. | 9 | `hot` (Enum), `default` (Enum) |
| `exclude` | Enum | Specifies an element type that is excluded from triggering the form change. | 5 | `water` (Enum), `fire` (Enum) |
| `particle` | Enum | Specifies the particle effect to play on form change. | 5 | `FireExtinguish` (Enum) |
| `sfx` | Enum | Specifies the sound effect to play on form change. | 5 | `FireExtinguish` (Enum) |


### Object: `FormChangeWhileHasStatus`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `status` | Enum || 35 | `T2CopyCatInternal` (Enum), `Grappling` (Enum) |
| `form_hasnot` | Enum | Specifies a form the unit must NOT currently be in for this passive to trigger. | 30 | `Default` (Enum), `Empty` (Enum) |
| `form_has` | Enum | Specifies the form the unit must currently be in for this passive to trigger. | 25 | `Primed` (Enum), `Full` (Enum) |


### Object: `FormChangeWhilePrimingAbility`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `not_priming` | Enum | Specifies the form to switch to when the unit is not priming an ability. | 6 | `DualSword` (Enum), `SwordAndShield` (Enum) |
| `priming` | Enum | Specifies the form to switch to when the unit is priming an ability. | 6 | `DualSword_Primed` (Enum), `Priming` (Enum) |


### Object: `FormChanger`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `initial_form` | Enum / Integer | Specifies which form the unit starts in. | 56 | `Default` (Enum), `Normal` (Enum), `1` (Number), `5` (Number) |
| [`Default`](Characters_and_Bosses.md#object-default) | Enum / Object || 37 | `release` (Enum), `{ ... }` (Object) |
| [`Normal`](Characters_and_Bosses.md#object-normal) | Integer / Object || 11 | `0` (Number), `{ ... }` (Object) |
| [`Rage`](Characters_and_Bosses.md#object-rage) | Object || 10 | `{ ... }` (Object) |
| [`HasCat`](Characters_and_Bosses.md#object-hascat) | Object || 5 | `{ ... }` (Object) |
| [`OffMap`](Characters_and_Bosses.md#object-offmap) | Object || 4 | `{ ... }` (Object) |
| [`default`](Characters_and_Bosses.md#object-default) | Enum / Object || 4 | `{ ... }` (Object) |
| [`hot`](Characters_and_Bosses.md#object-hot) | Object || 4 | `{ ... }` (Object) |
| [`AllAlive`](Characters_and_Bosses.md#object-allalive) | Object || 3 | `{ ... }` (Object) |
| [`Down`](Characters_and_Bosses.md#object-down) | Object || 3 | `{ ... }` (Object) |
| [`Full`](Characters_and_Bosses.md#object-full) | Object || 3 | `{ ... }` (Object) |
| [`OneAlive`](Characters_and_Bosses.md#object-onealive) | Object || 3 | `{ ... }` (Object) |
| [`TwoAlive`](Characters_and_Bosses.md#object-twoalive) | Object || 3 | `{ ... }` (Object) |
| [`Up`](Characters_and_Bosses.md#object-up) | Object || 3 | `{ ... }` (Object) |
| [`Big`](Characters_and_Bosses.md#object-big) | Object || 2 | `{ ... }` (Object) |
| [`Boris`](Characters_and_Bosses.md#object-boris) | Enum / Object || 2 | `MegaGuppy_TransformBoris` (Enum), `{ ... }` (Object) |
| [`CaveMan`](Characters_and_Bosses.md#object-caveman) | Object || 2 | `{ ... }` (Object) |
| [`CaveManSpear`](Characters_and_Bosses.md#object-cavemanspear) | Object || 2 | `{ ... }` (Object) |
| [`Empty`](Characters_and_Bosses.md#object-empty) | Object || 2 | `{ ... }` (Object) |
| [`Explosive`](Characters_and_Bosses.md#object-explosive) | Enum / Object || 2 | `MegaGuppy_TransformExplosive` (Enum), `{ ... }` (Object) |
| [`Holding`](Characters_and_Bosses.md#object-holding) | Object || 2 | `{ ... }` (Object) |
| [`Holy`](Characters_and_Bosses.md#object-holy) | Enum / Object || 2 | `MegaGuppy_TransformHoly` (Enum), `{ ... }` (Object) |
| [`NotPriming`](Characters_and_Bosses.md#object-notpriming) | Object || 2 | `{ ... }` (Object) |
| [`Priming`](Characters_and_Bosses.md#object-priming) | Object || 2 | `{ ... }` (Object) |
| [`Rain`](Characters_and_Bosses.md#object-rain) | Object | Configures a rain weather effect, including particle system and AI brain. | 2 | `4` (Number), `1` (Number), `{ ... }` (Object) |
| [`Small`](Characters_and_Bosses.md#object-small) | Object || 2 | `{ ... }` (Object) |
| [`SquirrelForm`](Characters_and_Bosses.md#object-squirrelform) | Object || 2 | `{ ... }` (Object) |
| [`Turtled`](Characters_and_Bosses.md#object-turtled) | Object || 2 | `{ ... }` (Object) |
| [`active`](Characters_and_Bosses.md#object-active) | Object || 2 | `{ ... }` (Object) |
| [`passive`](Characters_and_Bosses.md#object-passive) | Object || 2 | `{ ... }` (Object) |
| [`Alert`](Characters_and_Bosses.md#object-alert) | Object || 1 | `{ ... }` (Object) |
| [`Angry`](Characters_and_Bosses.md#object-angry) | Object || 1 | `{ ... }` (Object) |
| [`Attacker`](Characters_and_Bosses.md#object-attacker) | Object || 1 | `{ ... }` (Object) |
| [`BellyFull`](Characters_and_Bosses.md#object-bellyfull) | Object || 1 | `{ ... }` (Object) |
| [`BigHolding`](Characters_and_Bosses.md#object-bigholding) | Object || 1 | `{ ... }` (Object) |
| [`BigHoldingCat`](Characters_and_Bosses.md#object-bigholdingcat) | Object || 1 | `{ ... }` (Object) |
| [`Bishop`](Characters_and_Bosses.md#object-bishop) | Boolean (Flag) / Object || 1 | `(Flag)` (Boolean (Flag)), `{ ... }` (Object) |
| [`BlackHole`](Characters_and_Bosses.md#object-blackhole) | Object || 1 | `{ ... }` (Object) |
| [`Bomb`](Characters_and_Bosses.md#object-bomb) | Boolean (Flag) / Object || 1 | `(Flag)` (Boolean (Flag)), `{ ... }` (Object) |
| [`Bully`](Characters_and_Bosses.md#object-bully) | Object || 1 | `{ ... }` (Object) |
| [`Butcher`](Engine_LogicKeys.md#object-butcher) | Object || 1 | `[CAT_EMBARK_QUOTES_BUTCHER_1 CAT_EMBARK_QUOTES_BUTCHER_2 CAT_EMBARK_QUOTES_BUTCHER_3 CAT_EMBARK_QUOTES_BUTCHER_4 CAT_EMBARK_QUOTES_BUTCHER_5 CAT_EMBARK_QUOTES_BUTCHER_6 CAT_EMBARK_QUOTES_BUTCHER_7 CAT_EMBARK_QUOTES_BUTCHER_8 CAT_EMBARK_QUOTES_BUTCHER_9 CAT_EMBARK_QUOTES_BUTCHER_10]` (Array), `[CAT_RETURN_EARLY_QUOTES_BUTCHER_1 CAT_RETURN_EARLY_QUOTES_BUTCHER_2 CAT_RETURN_EARLY_QUOTES_BUTCHER_3 CAT_RETURN_EARLY_QUOTES_BUTCHER_4 CAT_RETURN_EARLY_QUOTES_BUTCHER_5]` (Array), `{ ... }` (Object) |
| [`CaveBaby`](Characters_and_Bosses.md#object-cavebaby) | Object || 1 | `{ ... }` (Object) |
| [`CaveWoman`](Characters_and_Bosses.md#object-cavewoman) | Object || 1 | `{ ... }` (Object) |
| [`CaveWomanHasCat`](Characters_and_Bosses.md#object-cavewomanhascat) | Object || 1 | `{ ... }` (Object) |
| [`Charging`](Characters_and_Bosses.md#object-charging) | Object || 1 | `{ ... }` (Object) |
| [`Close`](Characters_and_Bosses.md#object-close) | Object || 1 | `{ ... }` (Object) |
| [`Colorless`](Engine_LogicKeys.md#object-colorless) | Array / Object || 1 | `[CAT_RETURN_EARLY_QUOTES_COLORLESS_1 CAT_RETURN_EARLY_QUOTES_COLORLESS_2 CAT_RETURN_EARLY_QUOTES_COLORLESS_3 CAT_RETURN_EARLY_QUOTES_COLORLESS_4 CAT_RETURN_EARLY_QUOTES_COLORLESS_5]` (Array), `[CAT_EMBARK_QUOTES_COLORLESS_1 CAT_EMBARK_QUOTES_COLORLESS_2 CAT_EMBARK_QUOTES_COLORLESS_3 CAT_EMBARK_QUOTES_COLORLESS_4 CAT_EMBARK_QUOTES_COLORLESS_5 CAT_EMBARK_QUOTES_COLORLESS_6 CAT_EMBARK_QUOTES_COLORLESS_7 CAT_EMBARK_QUOTES_COLORLESS_8]` (Array), `{ ... }` (Object) |
| [`Cultist`](Characters_and_Bosses.md#object-cultist) | Object || 1 | `{ ... }` (Object) |
| [`Damaged`](Characters_and_Bosses.md#object-damaged) | Object || 1 | `{ ... }` (Object) |
| [`Default_Ceiling`](Characters_and_Bosses.md#object-default_ceiling) | Object || 1 | `{ ... }` (Object) |
| [`Default_Ground`](Characters_and_Bosses.md#object-default_ground) | Object || 1 | `{ ... }` (Object) |
| [`DesireMech`](Characters_and_Bosses.md#object-desiremech) | Object || 1 | `{ ... }` (Object) |
| [`Die`](Characters_and_Bosses.md#object-die) | Integer / Object | Specifies the number of sides on a die roll for a random outcome. | 1 | `6` (Number), `1` (Number), `{ ... }` (Object) |
| [`Druid`](Engine_LogicKeys.md#object-druid) | Array / Object || 1 | `[CAT_RETURN_EARLY_QUOTES_DRUID_1 CAT_RETURN_EARLY_QUOTES_DRUID_2 CAT_RETURN_EARLY_QUOTES_DRUID_3 CAT_RETURN_EARLY_QUOTES_DRUID_4 CAT_RETURN_EARLY_QUOTES_DRUID_5]` (Array), `[CAT_VS_BOSS_QUOTES_DRUID_1 CAT_VS_BOSS_QUOTES_DRUID_2 CAT_VS_BOSS_QUOTES_DRUID_3 CAT_VS_BOSS_QUOTES_DRUID_4 CAT_VS_BOSS_QUOTES_DRUID_5 CAT_VS_BOSS_QUOTES_DRUID_6 CAT_VS_BOSS_QUOTES_DRUID_7 CAT_VS_BOSS_QUOTES_DRUID_8 CAT_VS_BOSS_QUOTES_DRUID_9]` (Array), `{ ... }` (Object) |
| [`Drunker`](Characters_and_Bosses.md#object-drunker) | Object || 1 | `{ ... }` (Object) |
| [`DualSword`](Characters_and_Bosses.md#object-dualsword) | Object || 1 | `{ ... }` (Object) |
| [`DualSword_Primed`](Characters_and_Bosses.md#object-dualsword_primed) | Object || 1 | `{ ... }` (Object) |
| [`Dumb`](Characters_and_Bosses.md#object-dumb) | Integer / Object || 1 | `3` (Number), `{ ... }` (Object) |
| [`Explody`](Characters_and_Bosses.md#object-explody) | Object || 1 | `{ ... }` (Object) |
| [`FightPhase`](Characters_and_Bosses.md#object-fightphase) | Object || 1 | `{ ... }` (Object) |
| [`Fighter`](Engine_LogicKeys.md#object-fighter) | Array / Object || 1 | `[CAT_VS_BOSS_QUOTES_FIGHTER_1 CAT_VS_BOSS_QUOTES_FIGHTER_2 CAT_VS_BOSS_QUOTES_FIGHTER_3 CAT_VS_BOSS_QUOTES_FIGHTER_4 CAT_VS_BOSS_QUOTES_FIGHTER_5 CAT_VS_BOSS_QUOTES_FIGHTER_6 CAT_VS_BOSS_QUOTES_FIGHTER_7 CAT_VS_BOSS_QUOTES_FIGHTER_8 CAT_VS_BOSS_QUOTES_FIGHTER_9]` (Array), `[CAT_RETURN_EARLY_QUOTES_FIGHTER_1 CAT_RETURN_EARLY_QUOTES_FIGHTER_2 CAT_RETURN_EARLY_QUOTES_FIGHTER_3 CAT_RETURN_EARLY_QUOTES_FIGHTER_4 CAT_RETURN_EARLY_QUOTES_FIGHTER_5 CAT_RETURN_EARLY_QUOTES_FIGHTER_6]` (Array), `{ ... }` (Object) |
| [`Fire`](Characters_and_Bosses.md#object-fire) | Integer / Object || 1 | `1` (Number), `{ ... }` (Object) |
| [`FireFull`](Characters_and_Bosses.md#object-firefull) | Integer / Object || 1 | `1` (Number), `{ ... }` (Object) |
| [`Flop`](Characters_and_Bosses.md#object-flop) | Object || 1 | `{ ... }` (Object) |
| [`Flop2`](Characters_and_Bosses.md#object-flop2) | Object || 1 | `{ ... }` (Object) |
| [`Flush`](Characters_and_Bosses.md#object-flush) | Object || 1 | `{ ... }` (Object) |
| [`FlushBubs`](Characters_and_Bosses.md#object-flushbubs) | Object || 1 | `{ ... }` (Object) |
| [`FlushHost`](Characters_and_Bosses.md#object-flushhost) | Object || 1 | `{ ... }` (Object) |
| [`FlushNettle`](Characters_and_Bosses.md#object-flushnettle) | Object || 1 | `{ ... }` (Object) |
| [`Grappling`](Characters_and_Bosses.md#object-grappling) | Object || 1 | `{ ... }` (Object) |
| [`Grown`](Characters_and_Bosses.md#object-grown) | Object || 1 | `{ ... }` (Object) |
| [`GuaranteedJackpot`](Characters_and_Bosses.md#object-guaranteedjackpot) | Object || 1 | `{ ... }` (Object) |
| [`Guarding`](Characters_and_Bosses.md#object-guarding) | Object || 1 | `{ ... }` (Object) |
| [`HalfDead`](Characters_and_Bosses.md#object-halfdead) | Object || 1 | `{ ... }` (Object) |
| [`HasDeadCat`](Characters_and_Bosses.md#object-hasdeadcat) | Object || 1 | `{ ... }` (Object) |
| [`HasRock`](Characters_and_Bosses.md#object-hasrock) | Object || 1 | `{ ... }` (Object) |
| [`Headless`](Characters_and_Bosses.md#object-headless) | Object || 1 | `{ ... }` (Object) |
| [`Hint_CrackedVisuals`](Characters_and_Bosses.md#object-hint_crackedvisuals) | Object || 1 | `{ ... }` (Object) |
| [`Hint_CrackedVisuals2`](Characters_and_Bosses.md#object-hint_crackedvisuals2) | Object || 1 | `{ ... }` (Object) |
| [`Hint_CrackedVisuals3`](Characters_and_Bosses.md#object-hint_crackedvisuals3) | Object || 1 | `{ ... }` (Object) |
| [`HumanDead`](Characters_and_Bosses.md#object-humandead) | Object || 1 | `{ ... }` (Object) |
| [`Hunter`](Engine_LogicKeys.md#object-hunter) | Array / Object || 1 | `[CAT_RETURN_EARLY_QUOTES_HUNTER_1 CAT_RETURN_EARLY_QUOTES_HUNTER_2 CAT_RETURN_EARLY_QUOTES_HUNTER_3 CAT_RETURN_EARLY_QUOTES_HUNTER_4 CAT_RETURN_EARLY_QUOTES_HUNTER_5]` (Array), `[CAT_EMBARK_QUOTES_HUNTER_1 CAT_EMBARK_QUOTES_HUNTER_2 CAT_EMBARK_QUOTES_HUNTER_3 CAT_EMBARK_QUOTES_HUNTER_4 CAT_EMBARK_QUOTES_HUNTER_5 CAT_EMBARK_QUOTES_HUNTER_6 CAT_EMBARK_QUOTES_HUNTER_7 CAT_EMBARK_QUOTES_HUNTER_8 CAT_EMBARK_QUOTES_HUNTER_9 CAT_EMBARK_QUOTES_HUNTER_10]` (Array), `{ ... }` (Object) |
| [`InitialPhase`](Characters_and_Bosses.md#object-initialphase) | Object || 1 | `{ ... }` (Object) |
| [`Insane_Ceiling`](Characters_and_Bosses.md#object-insane_ceiling) | Object || 1 | `{ ... }` (Object) |
| [`Insane_Ground`](Characters_and_Bosses.md#object-insane_ground) | Object || 1 | `{ ... }` (Object) |
| [`Johnny`](Characters_and_Bosses.md#object-johnny) | Object || 1 | `{ ... }` (Object) |
| [`JohnnyBubs`](Characters_and_Bosses.md#object-johnnybubs) | Object || 1 | `{ ... }` (Object) |
| [`JohnnyHost`](Characters_and_Bosses.md#object-johnnyhost) | Object || 1 | `{ ... }` (Object) |
| [`JohnnyNettle`](Characters_and_Bosses.md#object-johnnynettle) | Object || 1 | `{ ... }` (Object) |
| [`Joystick`](Characters_and_Bosses.md#object-joystick) | Object || 1 | `{ ... }` (Object) |
| [`LastHit`](Characters_and_Bosses.md#object-lasthit) | Object || 1 | `{ ... }` (Object) |
| [`Lifted`](Characters_and_Bosses.md#object-lifted) | Object || 1 | `{ ... }` (Object) |
| [`Lit`](Characters_and_Bosses.md#object-lit) | Object || 1 | `{ ... }` (Object) |
| [`Mage`](Engine_LogicKeys.md#object-mage) | Array / Object || 1 | `[CAT_VS_BOSS_QUOTES_MAGE_1 CAT_VS_BOSS_QUOTES_MAGE_2 CAT_VS_BOSS_QUOTES_MAGE_3 CAT_VS_BOSS_QUOTES_MAGE_4 CAT_VS_BOSS_QUOTES_MAGE_5 CAT_VS_BOSS_QUOTES_MAGE_6 CAT_VS_BOSS_QUOTES_MAGE_7]` (Array), `[CAT_RETURN_EARLY_QUOTES_MAGE_1 CAT_RETURN_EARLY_QUOTES_MAGE_2 CAT_RETURN_EARLY_QUOTES_MAGE_3 CAT_RETURN_EARLY_QUOTES_MAGE_4 CAT_RETURN_EARLY_QUOTES_MAGE_5]` (Array), `{ ... }` (Object) |
| [`Medic`](Engine_LogicKeys.md#object-medic) | Array / Object || 1 | `[CAT_EMBARK_QUOTES_MEDIC_1 CAT_EMBARK_QUOTES_MEDIC_2 CAT_EMBARK_QUOTES_MEDIC_3 CAT_EMBARK_QUOTES_MEDIC_4 CAT_EMBARK_QUOTES_MEDIC_5 CAT_EMBARK_QUOTES_MEDIC_6 CAT_EMBARK_QUOTES_MEDIC_7 CAT_EMBARK_QUOTES_MEDIC_8 CAT_EMBARK_QUOTES_MEDIC_9 CAT_EMBARK_QUOTES_MEDIC_10...]` (Array), `[CAT_VS_BOSS_QUOTES_MEDIC_1 CAT_VS_BOSS_QUOTES_MEDIC_2 CAT_VS_BOSS_QUOTES_MEDIC_3 CAT_VS_BOSS_QUOTES_MEDIC_4 CAT_VS_BOSS_QUOTES_MEDIC_5 CAT_VS_BOSS_QUOTES_MEDIC_6]` (Array), `{ ... }` (Object) |
| [`Monk`](Engine_LogicKeys.md#object-monk) | Array / Object || 1 | `[CAT_EMBARK_QUOTES_MONK_1 CAT_EMBARK_QUOTES_MONK_2 CAT_EMBARK_QUOTES_MONK_3 CAT_EMBARK_QUOTES_MONK_4 CAT_EMBARK_QUOTES_MONK_5 CAT_EMBARK_QUOTES_MONK_6 CAT_EMBARK_QUOTES_MONK_7 CAT_EMBARK_QUOTES_MONK_8]` (Array), `[CAT_RETURN_QUOTES_MONK_1 CAT_RETURN_QUOTES_MONK_2 CAT_RETURN_QUOTES_MONK_3 CAT_RETURN_QUOTES_MONK_4 CAT_RETURN_QUOTES_MONK_5]` (Array), `{ ... }` (Object) |
| [`Mounted`](Characters_and_Bosses.md#object-mounted) | Object || 1 | `{ ... }` (Object) |
| [`MouthFull`](Characters_and_Bosses.md#object-mouthfull) | Object || 1 | `{ ... }` (Object) |
| [`Mutant`](Characters_and_Bosses.md#object-mutant) | Integer / Object || 1 | `1` (Number), `{ ... }` (Object) |
| [`Necromancer`](Engine_LogicKeys.md#object-necromancer) | Array / Object || 1 | `[CAT_RETURN_EARLY_QUOTES_NECROMANCER_1 CAT_RETURN_EARLY_QUOTES_NECROMANCER_2 CAT_RETURN_EARLY_QUOTES_NECROMANCER_3 CAT_RETURN_EARLY_QUOTES_NECROMANCER_4 CAT_RETURN_EARLY_QUOTES_NECROMANCER_5 CAT_RETURN_EARLY_QUOTES_NECROMANCER_6]` (Array), `[CAT_EMBARK_QUOTES_NECROMANCER_1 CAT_EMBARK_QUOTES_NECROMANCER_2 CAT_EMBARK_QUOTES_NECROMANCER_3 CAT_EMBARK_QUOTES_NECROMANCER_4 CAT_EMBARK_QUOTES_NECROMANCER_5 CAT_EMBARK_QUOTES_NECROMANCER_6 CAT_EMBARK_QUOTES_NECROMANCER_7 CAT_EMBARK_QUOTES_NECROMANCER_8 CAT_EMBARK_QUOTES_NECROMANCER_9 CAT_EMBARK_QUOTES_NECROMANCER_10...]` (Array), `{ ... }` (Object) |
| [`NeutronStar`](Characters_and_Bosses.md#object-neutronstar) | Object || 1 | `{ ... }` (Object) |
| `NoDeathRattle` | Object || 1 | `{ ... }` (Object) |
| [`NoEyes`](Characters_and_Bosses.md#object-noeyes) | Object || 1 | `{ ... }` (Object) |
| [`NoStick`](Characters_and_Bosses.md#object-nostick) | Object || 1 | `{ ... }` (Object) |
| [`NormalFull`](Characters_and_Bosses.md#object-normalfull) | Integer / Object || 1 | `0` (Number), `{ ... }` (Object) |
| [`Nuke`](Characters_and_Bosses.md#object-nuke) | Object || 1 | `{ ... }` (Object) |
| [`Obey`](Characters_and_Bosses.md#object-obey) | Integer / Object || 1 | `1` (Number), `{ ... }` (Object) |
| [`Off`](Characters_and_Bosses.md#object-off) | Object || 1 | `{ ... }` (Object) |
| [`OffScreen`](Characters_and_Bosses.md#object-offscreen) | Object || 1 | `{ ... }` (Object) |
| [`OneEye`](Characters_and_Bosses.md#object-oneeye) | Object || 1 | `{ ... }` (Object) |
| [`Open`](Characters_and_Bosses.md#object-open) | Object || 1 | `{ ... }` (Object) |
| [`OpenCat`](Characters_and_Bosses.md#object-opencat) | Object || 1 | `{ ... }` (Object) |
| [`Out`](Characters_and_Bosses.md#object-out) | Object || 1 | `{ ... }` (Object) |
| [`Possessing`](Characters_and_Bosses.md#object-possessing) | Object || 1 | `{ ... }` (Object) |
| [`Primed`](Characters_and_Bosses.md#object-primed) | Object || 1 | `{ ... }` (Object) |
| [`Psychic`](Engine_LogicKeys.md#object-psychic) | Array / Object || 1 | `[CAT_EMBARK_QUOTES_PSYCHIC_1 CAT_EMBARK_QUOTES_PSYCHIC_2 CAT_EMBARK_QUOTES_PSYCHIC_3 CAT_EMBARK_QUOTES_PSYCHIC_4 CAT_EMBARK_QUOTES_PSYCHIC_5 CAT_EMBARK_QUOTES_PSYCHIC_6 CAT_EMBARK_QUOTES_PSYCHIC_7 CAT_EMBARK_QUOTES_PSYCHIC_8 CAT_EMBARK_QUOTES_PSYCHIC_9 CAT_EMBARK_QUOTES_PSYCHIC_10]` (Array), `[CAT_RETURN_QUOTES_PSYCHIC_1 CAT_RETURN_QUOTES_PSYCHIC_2 CAT_RETURN_QUOTES_PSYCHIC_3 CAT_RETURN_QUOTES_PSYCHIC_4 CAT_RETURN_QUOTES_PSYCHIC_5]` (Array), `{ ... }` (Object) |
| [`Pulp2`](Characters_and_Bosses.md#object-pulp2) | Object || 1 | `{ ... }` (Object) |
| [`Pulp3`](Characters_and_Bosses.md#object-pulp3) | Object || 1 | `{ ... }` (Object) |
| [`Pulp4`](Characters_and_Bosses.md#object-pulp4) | Object || 1 | `{ ... }` (Object) |
| [`Pulp5`](Characters_and_Bosses.md#object-pulp5) | Object || 1 | `{ ... }` (Object) |
| [`Pulp6`](Characters_and_Bosses.md#object-pulp6) | Object || 1 | `{ ... }` (Object) |
| [`Pulp7`](Characters_and_Bosses.md#object-pulp7) | Object || 1 | `{ ... }` (Object) |
| [`Sitting`](Characters_and_Bosses.md#object-sitting) | Object || 1 | `{ ... }` (Object) |
| [`SmallHolding`](Characters_and_Bosses.md#object-smallholding) | Object || 1 | `{ ... }` (Object) |
| [`SmallHoldingCat`](Characters_and_Bosses.md#object-smallholdingcat) | Object || 1 | `{ ... }` (Object) |
| [`SpawningPhase`](Characters_and_Bosses.md#object-spawningphase) | Object || 1 | `{ ... }` (Object) |
| [`Standing`](Characters_and_Bosses.md#object-standing) | Object || 1 | `{ ... }` (Object) |
| [`Standing2`](Characters_and_Bosses.md#object-standing2) | Object || 1 | `{ ... }` (Object) |
| [`Start_Ceiling`](Characters_and_Bosses.md#object-start_ceiling) | Object || 1 | `{ ... }` (Object) |
| [`Stop`](Characters_and_Bosses.md#object-stop) | Integer / Object || 1 | `2` (Number), `{ ... }` (Object) |
| [`SwordAndShield`](Characters_and_Bosses.md#object-swordandshield) | Object || 1 | `{ ... }` (Object) |
| [`SwordAndShield_Primed`](Characters_and_Bosses.md#object-swordandshield_primed) | Object || 1 | `{ ... }` (Object) |
| [`Tank`](Engine_LogicKeys.md#object-tank) | Array / Object || 1 | `[CAT_EMBARK_QUOTES_TANK_1 CAT_EMBARK_QUOTES_TANK_2 CAT_EMBARK_QUOTES_TANK_3 CAT_EMBARK_QUOTES_TANK_4 CAT_EMBARK_QUOTES_TANK_5 CAT_EMBARK_QUOTES_TANK_6 CAT_EMBARK_QUOTES_TANK_7 CAT_EMBARK_QUOTES_TANK_8 CAT_EMBARK_QUOTES_TANK_9 CAT_EMBARK_QUOTES_TANK_10...]` (Array), `[CAT_RETURN_QUOTES_TANK_1 CAT_RETURN_QUOTES_TANK_2 CAT_RETURN_QUOTES_TANK_3 CAT_RETURN_QUOTES_TANK_4 CAT_RETURN_QUOTES_TANK_5]` (Array), `{ ... }` (Object) |
| [`Tar`](Characters_and_Bosses.md#object-tar) | Integer / Object || 1 | `2` (Number), `{ ... }` (Object) |
| [`TarFull`](Characters_and_Bosses.md#object-tarfull) | Integer / Object || 1 | `2` (Number), `{ ... }` (Object) |
| [`Thief`](Engine_LogicKeys.md#object-thief) | Array / Object || 1 | `[CAT_VS_BOSS_QUOTES_THIEF_1 CAT_VS_BOSS_QUOTES_THIEF_2 CAT_VS_BOSS_QUOTES_THIEF_3 CAT_VS_BOSS_QUOTES_THIEF_4 CAT_VS_BOSS_QUOTES_THIEF_5 CAT_VS_BOSS_QUOTES_THIEF_6]` (Array), `[CAT_RETURN_QUOTES_THIEF_1 CAT_RETURN_QUOTES_THIEF_2 CAT_RETURN_QUOTES_THIEF_3 CAT_RETURN_QUOTES_THIEF_4 CAT_RETURN_QUOTES_THIEF_5]` (Array), `{ ... }` (Object) |
| [`Throb`](Characters_and_Bosses.md#object-throb) | Object || 1 | `{ ... }` (Object) |
| [`ThrobBubs`](Characters_and_Bosses.md#object-throbbubs) | Object || 1 | `{ ... }` (Object) |
| [`ThrobHost`](Characters_and_Bosses.md#object-throbhost) | Object || 1 | `{ ... }` (Object) |
| [`ThrobNettle`](Characters_and_Bosses.md#object-throbnettle) | Object || 1 | `{ ... }` (Object) |
| [`Tinkerer`](Engine_LogicKeys.md#object-tinkerer) | Array / Object || 1 | `[CAT_EMBARK_QUOTES_TINKERER_1 CAT_EMBARK_QUOTES_TINKERER_2 CAT_EMBARK_QUOTES_TINKERER_3 CAT_EMBARK_QUOTES_TINKERER_4 CAT_EMBARK_QUOTES_TINKERER_5 CAT_EMBARK_QUOTES_TINKERER_6 CAT_EMBARK_QUOTES_TINKERER_7 CAT_EMBARK_QUOTES_TINKERER_8 CAT_EMBARK_QUOTES_TINKERER_9 CAT_EMBARK_QUOTES_TINKERER_10]` (Array), `[CAT_RETURN_EARLY_QUOTES_TINKERER_1 CAT_RETURN_EARLY_QUOTES_TINKERER_2 CAT_RETURN_EARLY_QUOTES_TINKERER_3]` (Array), `{ ... }` (Object) |
| [`Transformed`](Characters_and_Bosses.md#object-transformed) | Object || 1 | `{ ... }` (Object) |
| [`TwoEyes`](Characters_and_Bosses.md#object-twoeyes) | Object || 1 | `{ ... }` (Object) |
| [`Unlit`](Characters_and_Bosses.md#object-unlit) | Object || 1 | `{ ... }` (Object) |
| `Unmounted` | Object || 1 | `{ ... }` (Object) |
| [`Unwashed`](Characters_and_Bosses.md#object-unwashed) | Object || 1 | `{ ... }` (Object) |
| [`Washed`](Characters_and_Bosses.md#object-washed) | Object || 1 | `{ ... }` (Object) |
| [`Washer`](Characters_and_Bosses.md#object-washer) | Object || 1 | `{ ... }` (Object) |
| [`Water`](Characters_and_Bosses.md#object-water) | Object || 1 | `{ ... }` (Object) |
| [`WereMan`](Characters_and_Bosses.md#object-wereman) | Object || 1 | `{ ... }` (Object) |
| [`Zealot`](Characters_and_Bosses.md#object-zealot) | Object || 1 | `{ ... }` (Object) |
| [`ZealotBomb`](Characters_and_Bosses.md#object-zealotbomb) | Object || 1 | `{ ... }` (Object) |
| `sync_brain_patterns` | Boolean | If true, the unit's AI patterns are synchronized across all its forms. | 1 | `true` (Boolean) |


### Object: `Fragile`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `FragileDuringElement`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `FrankBolts`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |


### Object: `FullPower`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `GlobalFamiliarDamageBoost`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `GlobalFamiliarMoveBoost`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `GlobalFlowerTrapperAura`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Tangled`](Abilities_and_Spells.md#object-tangled) | Array / Integer / Object | The number of turns the target is unable to move, with optional [stacks, probability] format. | 1 | `[1 .1]` (Array), `[1 .33]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |


### Object: `GlobalMeleeRevengeDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `knockback` | Enum / Integer | The number of tiles to push the target away from the attacker; can be negative to pull the target closer, or 'str' to scale with the attacker's strength stat. | 1 | `5` (Number) |


### Object: `HPAltStates`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `clipname` | Enum | Specifies the animation clip name for the alternate state. | 1 | `poopmain` (Enum) |
| `thresholds` | Array | An array of health percentage thresholds that trigger state changes. | 1 | `[[ 1 0 ] [ 0 3 ]]` (Array) |


### Object: `HealNeighborsEachTurn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allies_only` | Boolean | If true, the Buddy effect only targets allies. | 1 | `true` (Boolean) |
| `stacks` | Enum / Integer | The number of stacks or formula for the status effect applied. | 1 | `3` (Number) |


### Object: `HealingAura`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `HealthPickup`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `frame_range` | Array | Specifies the animation frame range (start and end) for the pickup's sprite. | 15 | `[1 2]` (Array), `[5 5]` (Array) |
| `stacks` | Enum / Integer | The number of stacks or formula for the status effect applied. | 15 | `7` (Number), `10` (Number) |
| `stored_food_value` | Integer | The amount of food value this pickup provides when consumed. | 15 | `4` (Number), `2` (Number) |
| `anything_eats` | Boolean | If true, any unit can consume this pickup, not just those with specific dietary restrictions. | 4 | `true` (Boolean) |
| `force_frame` | Integer | Forces the pickup to display a specific animation frame. | 1 | `12` (Number) |


### Object: `HealthRegenUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `HitlerExecute`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 1 | `HitlerShoot` (Enum) |
| `tag` | Array / Enum | Specifies the name of the tag to check for on the target. | 1 | `grown_hitler_clone` (Enum) |
| [`threshold`](Items_and_Equipment.md#object-threshold) | Enum / Integer / Object | The health threshold value (absolute or equation) at which this ability becomes available. | 1 | `15` (Number) |


### Object: `Hypomania`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |


### Object: `ImmediateAbilityReaction`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 13 | `FormShrinkTwoSnakey` (Enum), `ButtWeb_AlreadyEnraged` (Enum) |
| `ability_damage_only` | Boolean | If true, this reaction only triggers from damage caused by abilities. | 6 | `true` (Boolean) |
| `backstabs_only` | Boolean | If true, this reaction only triggers when the unit is backstabbed. | 2 | `true` (Boolean) |
| `damage_threshold` | Integer | The amount of damage taken that triggers this immediate ability reaction. | 2 | `10` (Number) |
| `even_if_blocked` | Boolean | If true, the reaction triggers even if the damage was blocked. | 2 | `true` (Boolean) |
| `even_if_stunned` | Boolean | If true, the reaction triggers even if the unit is stunned. | 2 | `true` (Boolean) |
| `health_threshold` | Integer | The health threshold (absolute HP value) that triggers the reaction. Use -1 for no threshold. | 2 | `50` (Number), `70` (Number) |
| `buddy_damage_only` | Boolean | If true, the reaction only triggers from damage dealt by the unit's buddy. | 1 | `true` (Boolean) |
| `target_furthest_valid` | Boolean | If true, the reaction targets the furthest valid target instead of the closest. | 1 | `true` (Boolean) |


### Object: `Immobile`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `ImmortalLeeches`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `ItemAuxTransform`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `le` | Array || 3 | `[50 MoneyBag_Large]` (Array), `[10 MoneyBag_Small]` (Array) |
| `ge` | Array || 2 | `[20 BlackShard_Glowing]` (Array), `[10 NuclearKnife_Glowing]` (Array) |
| `lt` | Array || 1 | `[10 NuclearKnife]` (Array) |


### Object: `JohnnyNeedsWashing`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `form_unwashed` | Enum | Specifies the form when the character is unwashed. | 1 | `Unwashed` (Enum) |
| `form_washed` | Enum | Specifies the form when the character is washed. | 1 | `Washed` (Enum) |


### Object: `KillsHeal`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `KineticSpikes`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `Lifesteal`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `LuckUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `Madness`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | The number of stacks or formula for the status effect applied. | 1 | `1` (Number) |
| `tickdown_this_turn` | Boolean | If true, the madness stacks tick down at the end of the current turn instead of next turn. | 1 | `true` (Boolean) |


### Object: `ManaPickup`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `frame_range` | Array | Specifies the animation frame range (start and end) for the pickup's sprite. | 3 | `[6 6]` (Array), `[1 2]` (Array) |
| `stacks` | Enum / Integer | The number of stacks or formula for the status effect applied. | 3 | `4` (Number), `6` (Number) |


### Object: `MegaDinoDropController`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `head_drop` | Enum | Specifies the ability or animation for the head dropping. | 1 | `MD_HeadDrop` (Enum) |
| `leg_leave` | Enum | Specifies the ability or animation for legs leaving the body. | 1 | `MD_LegLeave` (Enum) |
| `leg_return` | Enum | Specifies the ability or animation for legs returning to the body. | 1 | `MD_LegReturn` (Enum) |
| `stable_legs` | Integer | The number of legs required to remain stable before the head drops. | 1 | `3` (Number) |


### Object: `Metal`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `MetalDetector`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `MissChance`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `ModularPickup`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Cleanse`](Engine_StatusAndPassiveKeys.md#object-cleanse) | Integer / Object | If set to 1, removes all status effects from the target; if 0, no cleanse. | 1 | `1` (Number), `0` (Number), `{ ... }` (Object) |
| `sound_event` | Enum | Specifies the sound event played on pickup. | 1 | `EatAntidote` (Enum) |


### Object: `MonkCatReactionAbilities`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 | `attack` (Enum) |
| `move` | Enum | Determines which movement ability the unit uses. | 1 | `move` (Enum) |
| `spell` | Enum | Specifies the spell ability granted by this reaction. | 1 | `MCHadouken` (Enum) |
| `trinket` | Enum | Specifies the trinket item associated with this ability. | 1 | `MCHadouken` (Enum) |
| `weapon` | Enum || 1 | `attack` (Enum) |


### Object: `MotherGrowController`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`eat_damage`](Characters_and_Bosses.md#object-eat_damage) | Object || 1 | `{ ... }` (Object) |
| `tumor_object` | Enum | Specifies the parent tumor object that controls growth. | 1 | `MotherTumor` (Enum) |


### Object: `MotherTumorPassive`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Cat`](Characters_and_Bosses.md#object-cat) | Object || 1 | `{ ... }` (Object) |
| [`NonCat`](Characters_and_Bosses.md#object-noncat) | Object || 1 | `{ ... }` (Object) |
| `considered_forms` | Array | An array of form names considered for growth decisions. | 1 | `[Big BigHolding BigHoldingCat]` (Array) |
| `grow_ability` | Enum | Specifies the ability used to grow the tumor. | 1 | `MotherTumorGrow` (Enum) |
| `pass_ani` | Enum | Specifies the animation played when passing the tumor. | 1 | `pass` (Enum) |
| `receive_ani` | Enum | Specifies the animation played when receiving the tumor. | 1 | `receive` (Enum) |


### Object: `MotherTumorSpawnInCapture`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Cat`](Characters_and_Bosses.md#object-cat) | Object || 2 | `{ ... }` (Object) |
| [`NonCat`](Characters_and_Bosses.md#object-noncat) | Object || 2 | `{ ... }` (Object) |
| [`Nothing`](Characters_and_Bosses.md#object-nothing) | Object || 1 | `{ ... }` (Object) |


### Object: `Mount`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `eject_ability` | Enum | Specifies the ability used to eject the rider from the mount. | 1 | `MechSuitEject` (Enum) |
| `enter_ability` | Enum | Specifies the ability used to enter the mount. | 1 | `EnterMech` (Enum) |


### Object: `MoveAfterAnyAttemptedAttack`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `weights` | Array / Enum | An array of three weighting values or a named preset for Crazy Eye background behavior weights. | 1 | `bat_chaos_runaway` (Enum) |


### Object: `MoveAwayFromDamageSource`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `move_ability` | Enum | Specifies the ability used to move when damaged. | 1 | `BirdFly` (Enum) |


### Object: `MoveAwayWhenEnemyAdjacent`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `move_ability` | Enum | Specifies the ability used to move when damaged. | 1 | `YA_Jetpack` (Enum) |
| `once_per_turn` | Boolean | If true, this movement reaction can only trigger once per turn. | 1 | `true` (Boolean) |
| `weights` | Array / Enum | An array of three weighting values or a named preset for Crazy Eye background behavior weights. | 1 | `stay_far_always_move` (Enum) |


### Object: `MoveQuivered`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `MoveTowardsKillers`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `character_filter` | Array | Specifies the list of character types that the unit will move towards. | 3 | `[SpiderCat TallSpiderCat]` (Array) |
| `move_ability` | Enum | Specifies the ability used to move when damaged. | 3 | `SpiderReturn` (Enum) |


### Object: `MultiSpawnOnDeath`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `count` | Array / Integer | The number of times or items to generate, spawn, or apply. | 1 | `[0 2]` (Array) |
| `obj` | Array / Enum | The object(s) spawned when this passive triggers. | 1 | `Maggot` (Enum) |


### Object: `MutateAfterXTurns`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `NoManaRegen`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `NonStackingDivineShield`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `NumbingLeeches`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `ObjectDetector`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number | A multiplier or percentage representing the probability of the effect occurring. | 1 | `10` (Number) |
| `object` | Array / Enum | Specifies the template identifier of the entity to spawn, referencing a predefined character or object in the game data. | 1 | `CharmedDip` (Enum) |


### Object: `Paranoia`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |


### Object: `PassiveIfStrAuxEquals`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 7 | `{ ... }` (Object) |
| `value` | Enum | The magnitude or stat reference for this elite buff (e.g., numeric, 'spd', 'con'). | 7 | `int` (Enum), `spd` (Enum) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 7 |


### Object: `PassiveIfWeaponIsUsable`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Brace`](Events_and_Encounters.md#object-brace) | Enum / Integer / Object | The amount of flat damage reduction applied to the source. | 2 | `[1 .5]` (Array), `10` (Number), `4` (Number), `{ ... }` (Object) |


### Object: `PassiveWhenDead`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |
| [`AutocastEachRound`](Abilities_and_Spells.md#object-autocasteachround) | Enum / Object | An object defining an ability that is automatically cast each round, with optional force display or ignore stun. | 1 | `SpiderReturn` (Enum), `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |


### Object: `PassiveWhenOnTile`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 7 | `{ ... }` (Object) |
| `tile` | Array / Enum | Specifies the tile type(s) to change to (e.g., RoadTile, WaterTile). Can be a single tile or an array of tiles. | 7 | `[WaterTile]` (Array), `[TallGrassTile TallFlowerTile]` (Array) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 7 |


### Object: `PassiveWhileHasDurability`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`MovementReaction`](Characters_and_Bosses.md#object-movementreaction) | Object | Triggers an ability when an entity moves near the unit. | 1 | `{ ... }` (Object) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |


### Object: `PassiveWhileNotHasStatus`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |
| `status` | Enum || 2 | `DemonicGlyph_Movement` (Enum), `ExistUntilIdleUpkeep` (Enum) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |


### Object: `PassiveWhileShielded`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Integer | The amount of health regeneration (HealthRegen) granted by this damage instance. | 1 | `[1 .5]` (Array), `4` (Number), `3` (Number), `{ ... }` (Object) |


### Object: `PermanentImmobile`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `PermanentMadness`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `Poison`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `PoisonThorns`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `PoopWhenHit`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number | A multiplier or percentage representing the probability of the effect occurring. | 1 | `25` (Number) |
| `object` | Array / Enum | Specifies the template identifier of the entity to spawn, referencing a predefined character or object in the game data. | 1 | `Poop` (Enum) |


### Object: `ProtectTargetedAllies`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 2 | `SwapPositions_TankCat` (Enum) |
| `target_filter` | Enum | Specifies the target filter for the protect ability (e.g., 'any' or a specific unit type). | 2 | `any` (Enum), `Kitten` (Enum) |


### Object: `Quiver`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `Quivered`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `ReduceManaCost`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `ReflectProjectiles`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`self_damage`](Abilities_and_Spells.md#object-self_damage) | Boolean / Integer / Object | A damage instance object that applies damage and effects to the source unit itself. | 8 | `2` (Number) |


### Object: `RefreshEquipmentAbilityOnElement`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `element` | Array / Enum || 2 | `Electric` (Enum) |
| `text` | String || 2 | `"COMBAT_POPUP_RECHARGED"` (String) |


### Object: `RunWhenLastPlayerCatIsCharmed`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allow_decision_mid_turn` | Boolean | If true, allows this passive to make decisions during the middle of a turn. | 1 | `true` (Boolean) |
| `legacy_savekey` | Enum | Specifies the legacy save key for recovering stolen cats. | 1 | `Legacy_Marshmallow_StolenCatID` (Enum) |


### Object: `SafeDoomed`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `ScaldingOrbMoonBossOneShot`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CompleteItemQuest` | Enum || 1 | `Nuke` (Enum), `ScaldingOrb` (Enum) |
| `RemoveItem` | Enum || 1 | `BlackShard_Glowing` (Enum), `ScaldingOrb` (Enum) |


### Object: `ScaledStatusAlliesOnSpendMana`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_Adjacent`](Engine_LogicKeys.md#conditional_adjacent) | Object || 1 | `{ ... }` (Object) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |


### Object: `ScaledStatusOnHolyShieldBlock`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`RandomMagicMissile`](Abilities_and_Spells.md#object-randommagicmissile) | Integer / Object | The number of random magic missiles fired, each dealing independent damage; can also be an object with custom tooltip data. | 1 | `[1 .5]` (Array), `6` (Number), `10` (Number), `{ ... }` (Object) |


### Object: `ScalingAttackAnimation`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`default`](Characters_and_Bosses.md#object-default) | Enum / Object || 1 | `bite1` (Enum) |
| `thresholds` | Array | An array of health percentage thresholds that trigger state changes. | 1 | `[[ 5 bite2 ] [ 10 bite3 ]]` (Array) |


### Object: `SchrodingerDisorder`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |


### Object: `Scleroderma`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |


### Object: `SharePickups`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `include_coins` | Boolean | If true, includes coins in shared pickups. | 1 | `true` (Boolean) |


### Object: `ShoulderCheck`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `ShovingMatch`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `SkipFirstRounds`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `pop_chance` | Integer | The percentage chance that the first round skip will trigger. | 1 | `50` (Number) |
| `stacks` | Enum / Integer | The number of stacks or formula for the status effect applied. | 1 | `2` (Number) |


### Object: `SlotMachineRollPool`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`SlotResult_Jackpot_Coins`](Engine_LogicKeys.md#object-slotresult_jackpot_coins) | Integer / Object || 2 | `1` (Number), `{ ... }` (Object) |
| [`SlotResult_Explode`](Engine_LogicKeys.md#object-slotresult_explode) | Integer / Object || 1 | `1` (Number), `{ ... }` (Object) |
| [`SlotResult_Nothing`](Engine_LogicKeys.md#object-slotresult_nothing) | Integer / Object || 1 | `7` (Number), `{ ... }` (Object) |
| [`SlotResult_RandomPickup`](Engine_LogicKeys.md#object-slotresult_randompickup) | Integer / Object || 1 | `11` (Number), `{ ... }` (Object) |


### Object: `Slow`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `SmallRockBehavior`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage` | Equation | The damage dealt, which can be a numeric value, a formula string, or a defined damage object. | 4 | `9` (Equation), `5` (Equation) |
| `knockback` | Enum / Integer | The number of tiles to push the target away from the attacker; can be negative to pull the target closer, or 'str' to scale with the attacker's strength stat. | 4 | `1` (Number), `5` (Number) |
| `chain` | Boolean | Specifies the chain effect type (e.g., 'splashM') or 'true' to enable chaining. | 2 | `true` (Boolean) |


### Object: `SpawnCatCopyWhenDowned`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `object` | Array / Enum | Specifies the template identifier of the entity to spawn, referencing a predefined character or object in the game data. | 2 | `PlayerCat_NecroShade` (Enum), `PlayerCat_AncestralShade` (Enum) |
| `prevent_chain_tag` | Enum | Prevents spawning if a unit with the specified tag (e.g., 'ancestorset_shade') already exists. | 2 | `necroset_shade` (Enum), `ancestorset_shade` (Enum) |


### Object: `SpawnExtraThingsOnBattleStart`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `number` | Array / Integer || 31 | `[3 8]` (Array), `[0 2]` (Array), `3` (Number), `1` (Number) |
| `object` | Array / Enum | Specifies the template identifier of the entity to spawn, referencing a predefined character or object in the game data. | 23 | `[Spookie Scary Tatters Wisp Wisp Wisp]` (Array), `[Bombchu Deathbot RoboVacuum TinkererTurret]` (Array), `NeutralToad` (Enum), `Poop` (Enum) |
| `tile` | Array / Enum | Specifies the tile type(s) to change to (e.g., RoadTile, WaterTile). Can be a single tile or an array of tiles. | 7 | `TallGrassTile` (Enum), `FireTile` (Enum) |
| `trap` | Enum || 2 | `BearTrap` (Enum), `LandMine` (Enum) |


### Object: `SpawnItemLinkedFamiliar`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `break_on_pop_only` | Boolean || 2 | `true` (Boolean) |
| `object` | Array / Enum | Specifies the template identifier of the entity to spawn, referencing a predefined character or object in the game data. | 2 | `PyrophinaFamiliar` (Enum), `ZaratanaFamiliar` (Enum) |


### Object: `SpawnObjectOnPopCorpse`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `count` | Array / Integer | The number of times or items to generate, spawn, or apply. | 1 | `2` (Number) |
| `except_tiny` | Boolean || 1 | `true` (Boolean) |
| `object` | Array / Enum | Specifies the template identifier of the entity to spawn, referencing a predefined character or object in the game data. | 1 | `CharmedTinySpider` (Enum) |


### Object: `SpawnOnDeath`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `faction` | Enum | Determines which faction the spawned entity belongs to, controlling its team allegiance and targeting behavior. | 4 | `enemies` (Enum), `allies` (Enum) |
| `obj` | Array / Enum | The object(s) spawned when this passive triggers. | 4 | `[Spookie Spookie Scary Coin2 Coin3 Coin4]` (Array), `[Kitten Kitten TomTom TomTom Mangy Mangy CatCaller CatCaller GlassSpitter SpiderCat...]` (Array), `BeefyCharmedLeech` (Enum), `RiftKitten` (Enum) |
| [`additional_statuses`](Characters_and_Bosses.md#object-additional_statuses) | Object || 1 | `{ ... }` (Object) |


### Object: `SpawnRandomPickupsOnTaggedUnitKilled`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `count` | Array / Integer | The number of times or items to generate, spawn, or apply. | 1 | `[2 3]` (Array) |
| `tag` | Array / Enum | Specifies the name of the tag to check for on the target. | 1 | `poop` (Enum) |


### Object: `SpeedUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `SpellDamageUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `SpewerAltGraphics`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Fire`](Characters_and_Bosses.md#object-fire) | Integer / Object || 1 | `1` (Number), `{ ... }` (Object) |
| [`FireFull`](Characters_and_Bosses.md#object-firefull) | Integer / Object || 1 | `1` (Number), `{ ... }` (Object) |
| [`Normal`](Characters_and_Bosses.md#object-normal) | Integer / Object || 1 | `0` (Number), `{ ... }` (Object) |
| [`NormalFull`](Characters_and_Bosses.md#object-normalfull) | Integer / Object || 1 | `0` (Number), `{ ... }` (Object) |
| [`Tar`](Characters_and_Bosses.md#object-tar) | Integer / Object || 1 | `2` (Number), `{ ... }` (Object) |
| [`TarFull`](Characters_and_Bosses.md#object-tarfull) | Integer / Object || 1 | `2` (Number), `{ ... }` (Object) |


### Object: `SproutsGrantMovement`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `StackingFlowerTrail`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stack_key` | Enum || 3 | `FLOWER_SET` (String) |
| `stacks` | Enum / Integer | The number of stacks or formula for the status effect applied. | 3 | `1` (Number) |


### Object: `StatDependentPassive`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AddDamageToBasicAttack` | String || 1 | `4` (Number), `1` (Number), `"min(min(min(min(min(min(str,dex),int),con),lck),spd),cha)-2"` (String) |


### Object: `StatusAdjacentOnTheirTurnEnd`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ForceMoveAway` | Integer | The number of tiles the unit is forced to move away from its attacker. | 1 | `1` (Number), `{ ... }` (Object) |


### Object: `StatusAfterXTurns`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object | Determines which ability the target is forced to cast immediately, ignoring normal costs and cooldowns. | 2 | `neck_ChefsApron` (Enum), `CancerExplode` (Enum), `{ ... }` (Object) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |


### Object: `StatusAllCharactersOnSpawn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| [`Else`](Abilities_and_Spells.md#object-else) | Object | An object containing effects that apply when the parent conditional condition is not met. | 1 | `{ ... }` (Object) |
| `Poison` | Array / Integer | The number of Poison stacks applied, which deals poison damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |


### Object: `StatusCollector`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `StrengthUp` | Enum / Integer | Specifies the number of Strength stacks applied, where positive values increase melee damage and negative values decrease it. | 7 | `[1 .5]` (Array), `4` (Number), `-2` (Number), `{ ... }` (Object) |
| `Poison` | Array / Integer | The number of Poison stacks applied, which deals poison damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 4 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |
| [`Slow`](#object-slow) | Array / Enum / Integer / Object | The number of turns of Slow applied, or an array with duration and chance. | 4 | `[1 .1]` (Array), `[1 .25]` (Array), `-1` (Number), `3` (Number), `{ ... }` (Object) |


### Object: `StatusEachRoundBegin`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `NonStackingShield` | Number || 8 | `3` (Number), `8` (Number) |


### Object: `StatusEachRoundEnd`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`DoDamage`](Abilities_and_Spells.md#object-dodamage) | Object | An object defining damage to deal, including damage amount and type. | 1 | `{ ... }` (Object) |
| [`UseAbility`](Abilities_and_Spells.md#object-useability) | Enum / Object | Specifies the ability name the unit will use at the end of each round. | 1 | `GirlDinoPoop` (Enum), `Spit` (Enum), `{ ... }` (Object) |


### Object: `StatusEachTurnBeginIfHasStatus`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AllStatsUp` | Enum / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 1 | `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `DamageUp` | Integer / String | The amount of damage increase, or a string formula for dynamic calculation. | 1 | `[1 .5]` (Array), `-2` (Number), `3` (Number), `{ ... }` (Object) |
| `HealthGain` | Integer | The amount of health restored to the source. | 1 | `2*X` (Enum), `3*X` (Enum), `10` (Number), `4` (Number) |
| `animation` | Enum | Specifies the animation clip to use for the ability’s meta representation. | 1 | `pulse3` (Enum) |
| `consume` | Boolean | If true, the status is consumed upon applying the effect. | 1 | `true` (Boolean) |
| `status` | Enum || 1 | `Counterspell` (Enum) |


### Object: `StatusEachTurnEndIfEnabledAtStartOfTurn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object | Determines which ability the target is forced to cast immediately, ignoring normal costs and cooldowns. | 1 | `neck_ChefsApron` (Enum), `T2UnClone` (Enum), `{ ... }` (Object) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |


### Object: `StatusEveryXSpellCastsEachTurn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthGain` | Integer | The amount of health restored to the source. | 1 | `2*X` (Enum), `3*X` (Enum), `10` (Number), `4` (Number) |
| `stacks` | Enum / Integer | The number of stacks or formula for the status effect applied. | 1 | `3` (Number) |


### Object: `StatusIfDidntMove`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Charge` | Integer | The number of stacks of Charge, which makes the caster gain 1 Mana per stack at the start of its next turn. | 1 | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |


### Object: `StatusIfUnusedActPoints`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`BackflipWhenTargeted`](Abilities_and_Spells.md#object-backflipwhentargeted) | Enum / Integer / Object | The number of stacks of BackflipWhenTargeted or an object defining the dodge ability; causes the unit to perform a backflip dodge when targeted. | 1 | `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| [`Craft`](Abilities_and_Spells.md#object-craft) | Object | An object defining a crafting action, including the item pool and target slot. | 1 | `{ ... }` (Object) |


### Object: `StatusOnBackstab`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthGain` | Integer | The amount of health restored to the source. | 1 | `2*X` (Enum), `3*X` (Enum), `10` (Number), `4` (Number) |
| `SerratedClaws` | Integer || 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |


### Object: `StatusOnBreak`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 20 |
| [`Bruise`](#object-bruise) | Array / Integer / Object | The number of Bruise stacks applied, or an array with duration and chance. | 3 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| [`FindItemFromPool`](Abilities_and_Spells.md#object-finditemfrompool) | Enum / Object | Determines the item pool name from which a random item is granted to the source. | 3 | `chapter_specific_item` (Enum), `chapter_common` (Enum), `{ ... }` (Object) |
| `HealthGain` | Integer | The amount of health restored to the source. | 3 | `2*X` (Enum), `3*X` (Enum), `10` (Number), `4` (Number) |
| `HealthRegenUp` | Integer | The amount of health regeneration (HealthRegen) granted by this damage instance. | 3 | `[1 .5]` (Array), `4` (Number), `3` (Number), `{ ... }` (Object) |
| [`ApplyToRandomPartyMemberIfPossible`](Abilities_and_Spells.md#object-applytorandompartymemberifpossible) | Object | An object containing effects to apply to a random party member if one is available. | 1 | `{ ... }` (Object) |
| `ConstitutionUp` | Array / Enum / Integer | The amount of Constitution (HP) increase, or an array with duration and chance. | 1 | `[1 .5]` (Array), `-1` (Number), `-2` (Number), `{ ... }` (Object) |
| `DexterityUp` | Enum / Integer | The amount of Dexterity stat increased or decreased (negative values lower the stat); can be a formula or fixed integer. | 1 | `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `IntelligenceUp` | Enum / Integer | The amount of intelligence increase, which can be a fixed integer or a mathematical expression. | 1 | `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object | An object or entity name that spawns upon hitting a character, with optional stacks and chance. | 1 | `BestBud` (Enum), `Maggot` (Enum), `{ ... }` (Object) |
| `StrengthUp` | Enum / Integer | Specifies the number of Strength stacks applied, where positive values increase melee damage and negative values decrease it. | 1 | `[1 .5]` (Array), `4` (Number), `-2` (Number), `{ ... }` (Object) |


### Object: `StatusOnDie`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 9 |
| [`FindItemFromPool`](Abilities_and_Spells.md#object-finditemfrompool) | Enum / Object | Determines the item pool name from which a random item is granted to the source. | 1 | `chapter_specific_item` (Enum), `chapter_common` (Enum), `{ ... }` (Object) |
| [`RandomMagicMissile`](Abilities_and_Spells.md#object-randommagicmissile) | Integer / Object | The number of random magic missiles fired, each dealing independent damage; can also be an object with custom tooltip data. | 1 | `[1 .5]` (Array), `10` (Number), `6` (Number), `{ ... }` (Object) |
| `RemoveAmbientLightEffects` | Number | The duration or amount of ambient light effect removal applied over time. | 1 | `4` (Number), `.5` (String) |
| [`ScatterCoins`](Abilities_and_Spells.md#object-scattercoins) | Object | The number of coins scattered, or an object with stacks and stacking behavior. | 1 | `[1 .5]` (Array), `5` (Number), `{ ... }` (Object) |


### Object: `StatusOnDodge`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DodgeChance_Status` | Integer | The percentage of dodge chance granted by this status effect. | 1 | `[1 .5]` (Array), `15` (Number), `66` (Number), `{ ... }` (Object) |


### Object: `StatusOnEnemyCastSpell`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AllStatsUp` | Enum / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 1 | `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `HealthGain` | Integer | The amount of health restored to the source. | 1 | `2*X` (Enum), `3*X` (Enum), `8` (Number), `10` (Number) |


### Object: `StatusOnEnemyConfused`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ImmediateUseAbility`](Engine_StatusAndPassiveKeys.md#object-immediateuseability) | Enum / Object | Forces the unit to immediately use the specified ability, even if stunned. | 1 | `cm_Lard_Impl` (Enum), `tk_ButterBean_Mega` (Enum), `{ ... }` (Object) |


### Object: `StatusOnEnemyDeath`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Charge` | Integer | The number of stacks of Charge, which makes the caster gain 1 Mana per stack at the start of its next turn. | 1 | `[1 .5]` (Array), `3` (Number), `4` (Number), `{ ... }` (Object) |


### Object: `StatusOnFallAsleep`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AllStatsUp` | Enum / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 1 | `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `FillMana` | Integer | The amount of mana restored to the unit; can be a fixed integer or an array `[stacks, probability]` for a chance-based application. | 1 | `[1 .25]` (Array), `[1 .10]` (Array), `1` (Number) |
| `HealRandomInjury` | Integer | The number of random injuries healed on the target. | 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |


### Object: `StatusOnFullMana`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_OncePerBattle`](Abilities_and_Spells.md#object-conditional_onceperbattle) | Object || 1 | `{ ... }` (Object) |


### Object: `StatusOnSetPieceBreak`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`FindItemFromPool`](Abilities_and_Spells.md#object-finditemfrompool) | Enum / Object | Determines the item pool name from which a random item is granted to the source. | 1 | `chapter_specific_item` (Enum), `consumables` (Enum), `{ ... }` (Object) |
| `PermanentCharisma` | Integer | The amount of permanent Charisma stat increase applied. | 1 | `1` (Number), `2` (Number) |
| `PermanentConstitution` | Integer | The amount of permanent Constitution (max HP) added. | 1 | `-1` (Number), `-2` (Number) |
| `PermanentDexterity` | Integer | The amount of permanent dexterity added to the unit. | 1 | `1` (Number), `2` (Number) |
| `PermanentIntelligence` | Integer | The number of permanent intelligence stat points added or subtracted. | 1 | `1` (Number), `2` (Number) |
| `PermanentLuck` | Integer | The amount of permanent Luck stat increase applied. | 1 | `1` (Number), `2` (Number) |
| `PermanentSpeed` | Integer | The number of permanent speed stat points added or subtracted. | 1 | `1` (Number), `2` (Number) |
| `PermanentStrength` | Integer | The amount of permanent Strength stat increase applied. | 1 | `1` (Number), `2` (Number) |
| `set` | Array / Enum | The visual set or furniture style tag (e.g., elegant, guts, Tentacle, wooden, Druid). | 1 | `Recycled` (Enum) |


### Object: `StatusOnSpawnIn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CaptureFamiliar` | Integer | The number of stacks of CaptureFamiliar, enabling the unit to capture a target as a familiar upon defeating it. | 1 | `1` (Number) |
| `SetHealth` | Integer || 1 | `100` (Number), `50` (Number) |


### Object: `StatusOnTakeHealthOrShieldDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |
| `DivineShield` | Array / Integer | The number of charges of Divine Shield applied, which blocks the next instances of damage entirely; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 2 | `[1 .33]` (Array), `[1 .5]` (Array), `4` (Number), `1` (Number), `{ ... }` (Object) |
| [`Conditional_GoodRoll`](Abilities_and_Spells.md#object-conditional_goodroll) | Object | Defines a random roll with odds; if successful, the specified effects are applied. | 1 | `{ ... }` (Object) |
| [`Metronome`](Abilities_and_Spells.md#object-metronome) | Boolean (Flag) / Number / Object | Specifies the Metronome ability, which applies a buff that repeats actions; may include stack count and a list of banned abilities. | 1 | `(Flag)` (Boolean (Flag)), `1` (Number), `2` (Number), `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |


### Object: `StatusOverlappingCharactersAndDie`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Poison` | Array / Integer | The number of Poison stacks applied, which deals poison damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |


### Object: `StatusRandomEnemiesOnBattleStart`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Fear` | Array / Integer | The number of Fear stacks applied, which reduces the target's accuracy and may cause it to flee; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 3 | `[1 .1]` (Array), `[1 .05]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| `Bleed` | Array / Integer | The number of Bleed stacks applied, which deals bleeding damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | `[1 .1]` (Array), `[3 .1]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |
| `Charmed` | Array / Enum / Integer | The number of turns of Charmed applied, or an array with duration and chance. | 1 | `[1 .1+.02*cha]` (Array), `[1 .25]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| [`Confusion`](#object-confusion) | Array / Integer / Object | The number of turns of Confusion applied, or an array with duration and chance. | 1 | `[2 .15]` (Array), `[1 .1]` (Array), `3` (Number), `4` (Number), `{ ... }` (Object) |
| `Freeze` | Array / Integer | The number of stacks of Freeze, immobilizing the unit for that many turns; can be an array `[stacks, probability]`. | 1 | `[1 .1]` (Array), `[1 0.15]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |


### Object: `StatusWhenStatusCompletelyRemoved`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`UseAbility`](Abilities_and_Spells.md#object-useability) | Enum / Object | Specifies the ability name the unit will use at the end of each round. | 1 | `GirlDinoPoop` (Enum), `TormentorRuneAbsorb` (Enum), `{ ... }` (Object) |
| `status` | Enum || 1 | `BackflipWhenTargeted` (Enum) |


### Object: `Stealth`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `StrengthForEachNeighboringEnemy`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `StrengthUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `StunImmunity`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cleanse_on_apply` | Boolean | If true, applying StunImmunity removes existing stun effects. | 1 | `false` (Boolean) |


### Object: `SupportDieInsteadOfRun`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alt_dead_ani` | Enum | Specifies an alternative animation clip used when dead instead of default run. | 1 | `off` (Enum) |
| `alt_dying_ani` | Enum | Specifies an alternative animation clip used when dying instead of default run. | 1 | `shutdown` (Enum) |


### Object: `SupportFormChangeInsteadOfRun`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 2 | `TVChangeDie` (Enum), `SBotAnger` (Enum) |
| `wait_till_turn` | Boolean | If true, the support form change waits until the unit's turn instead of happening immediately. | 1 | `true` (Boolean) |


### Object: `SwimmingFormChange`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `form_in` | Enum | Specifies the form used when entering water. | 1 | `Water` (Enum) |
| `form_out` | Enum | Specifies the form used when exiting water. | 1 | `Out` (Enum) |


### Object: `SyncFormsWithBuddy`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `no_buddy` | Enum | Specifies the named form (e.g., Rage) used when syncing forms without a buddy. | 1 | `Rage` (Enum) |


### Object: `T3HitlerSpawningPhase`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `spell_use_groups` | Array | An array defining the groups of spells available during the spawning phase. | 1 | `[[ T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk T3Spawn_Tank...]` (Array) |


### Object: `TVBotScreen`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Die`](Characters_and_Bosses.md#object-die) | Integer / Object | Specifies the number of sides on a die roll for a random outcome. | 1 | `6` (Number), `1` (Number), `{ ... }` (Object) |
| [`Dumb`](Characters_and_Bosses.md#object-dumb) | Integer / Object || 1 | `3` (Number), `{ ... }` (Object) |
| `Fuck` | Integer || 1 | `5` (Number) |
| [`Obey`](Characters_and_Bosses.md#object-obey) | Integer / Object || 1 | `1` (Number), `{ ... }` (Object) |
| `Shit` | Integer || 1 | `4` (Number) |
| [`Stop`](Characters_and_Bosses.md#object-stop) | Integer / Object || 1 | `2` (Number), `{ ... }` (Object) |


### Object: `Tech`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `TempInitiativeChange`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `Terminator2Run`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `move_ability` | Enum | Specifies the ability used to move when damaged. | 1 | `T2GoopRun` (Enum) |
| `move_weights` | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 1 | `stay_far_always_move` (Enum) |


### Object: `TerminatorChase`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 1 | `T1ChokeReaction` (Enum) |
| `move` | Enum | Determines which movement ability the unit uses. | 1 | `MoveOne` (Enum) |


### Object: `TerminatorSkin`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `groups` | Array | Determines which skin groups are applied to the unit. | 1 | `[{ stacks 48 ParticleBurst Gibs_terminatorskin CatPartsTransform { head 1057 }...]` (Array) |
| `status` | Enum || 1 | `Brace` (Enum) |


### Object: `Thorns`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `TinkererBasicAttackSwitching`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `craft_ability` | Enum | Specifies the ability used for crafting in the Tinkerer's basic attack switching. | 3 | `TinkererCraft` (Enum) |
| `throw_ability` | Enum | Specifies the ability used for throwing in the Tinkerer's basic attack switching. | 3 | `TinkererThrow` (Enum) |


### Object: `TintItem`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `add` | Array / Integer || 1 | `[0.05 0.05 0.05]` (Array) |
| `ignore_if_str_aux_equals` | Enum || 1 | `ModelingClay_Default` (Enum) |
| `mul` | Array || 1 | `[0.45 0.3 0.25]` (Array) |


### Object: `Trample`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `TransformInXTurns`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `object` | Array / Enum | Specifies the template identifier of the entity to spawn, referencing a predefined character or object in the game data. | 8 | `[YellowBlaster GreyAlien GreenProber Amoeba MoonWorm Waggle KirbyFetus BrainDrain Fetus FetusGusher]` (Array), `[Squirrel Crow Snake Turtle Toad Catepillar]` (Array), `HuskG` (Enum), `SkeletonCatRevivedFamiliar` (Enum) |
| `stacks` | Enum / Integer | The number of stacks or formula for the status effect applied. | 8 | `3` (Number), `1` (Number) |
| `initiative` | Enum / Integer | Determines the unit's turn order position; lower values act earlier. | 4 | `keep_turns_end_turn` (Enum) |
| `animation` | Enum | Specifies the animation clip to use for the ability’s meta representation. | 2 | `hatch` (Enum) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Configures turn-taking behavior for the status effect, including whether the unit takes turns and bonus turns. | 1 | `[1 4]` (Array) |


### Object: `TransformItemOnElementInfluence`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `element` | Array / Enum || 5 | `Fire` (Enum), `Greater_Water` (Enum) |
| `full_repair` | Boolean || 5 | `true` (Boolean) |
| `item` | Enum || 5 | `WaterBottle_Full` (Enum), `GallonOfWater` (Enum) |


### Object: `TransformOnDeathImmediately`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `first_turn` | Enum | Determines when the spawned entity takes its first action, such as 'initiative' (immediately), 'next_turn' (after current unit), 'end_of_round', or 'next_round'. | 4 | `keep_turns` (Enum) |
| `obj` | Array / Enum | The object(s) spawned when this passive triggers. | 4 | `TallSkeletonCatCorpse` (Enum), `SkeletonCatCorpseFamiliar` (Enum) |


### Object: `TransformOnElementInfluence`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `element` | Array / Enum || 9 | `Holy` (Enum), `Fire` (Enum) |
| `object` | Array / Enum | Specifies the template identifier of the entity to spawn, referencing a predefined character or object in the game data. | 9 | `CookedBiggestFood` (Enum), `CookedBait` (Enum) |


### Object: `TransformOnElementInfluencex`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `element` | Array / Enum || 2 | `Holy` (Enum) |
| `object` | Array / Enum | Specifies the template identifier of the entity to spawn, referencing a predefined character or object in the game data. | 2 | `Bait` (Enum), `PurifiedPoisonFood` (Enum) |


### Object: `TransformOnStatusThreshold`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `object` | Array / Enum | Specifies the template identifier of the entity to spawn, referencing a predefined character or object in the game data. | 1 | `Moth` (Enum) |
| `status` | Enum || 1 | `AllStatsUp` (Enum) |
| [`threshold`](Items_and_Equipment.md#object-threshold) | Enum / Integer / Object | The health threshold value (absolute or equation) at which this ability becomes available. | 1 | `5` (Number) |


### Object: `Trapper`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 4 | `RattleSnakeTrap` (Enum), `BloatSideLaser` (Enum) |
| `cancel_movement` | Boolean | If true, the Trapper cancels the unit's movement when triggered. | 2 | `false` (Boolean) |
| `pathfinding_avoidance` | Integer | The amount of pathfinding avoidance cost assigned to the trap tile. | 2 | `250` (Number) |
| `range` | Enum / Integer | The range (in tiles) of the aura, or 'global' for infinite range. | 2 | `10` (Number) |


### Object: `Triskaidekaphobia`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |


### Object: `TunnelVision`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `crit_chance` | Number | The chance for the damage instance to critically hit, expressed as a percentage (e.g., 50%) or a decimal fraction (e.g., .5). | 1 | `50` (Number) |


### Object: `TwisterFling`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage` | Equation | The damage dealt, which can be a numeric value, a formula string, or a defined damage object. | 1 | `5` (Equation) |
| `max_dist` | Integer | The maximum distance (in tiles) the target can be flung. | 1 | `5` (Number) |
| `min_dist` | Integer | The minimum distance (in tiles) the target must be flung. | 1 | `3` (Number) |


### Object: `UnlimitedDeathRattleRevive`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 1 | `MD_Lift` (Enum) |
| `even_if_stunned` | Boolean | If true, the reaction triggers even if the unit is stunned. | 1 | `true` (Boolean) |


### Object: `UseAbility`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 2 | `Destroyer2HolyAttack` (Enum), `T3Pebbles_BoulderDrop` (Enum) |
| `respect_prime` | Boolean || 2 | `true` (Boolean) |


### Object: `UseAbilityWhenOutOfStatus`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 1 | `QueenHippoHeartAttack` (Enum) |
| `status` | Enum || 1 | `Brace` (Enum) |


### Object: `Vegan`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |


### Object: `Vengeful`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `Weakness`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `WobblyCat`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |


### Object: `Zombie`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

