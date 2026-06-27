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
| [`name`](./Strings.md#string-name) | Enum | Specifies the localized name string for the entity, item, or ability. | 3307 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2985 |  |
| [`desc`](./Strings.md#string-desc) | Enum | Specifies the localized description string for the item or ability. | 2423 |  |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1910 ||
| [`class`](./Enums.md#enum-class) | Enum | Specifies the class that this ability belongs to, used for categorization and restrictions. | 600 |  |
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 461 ||
| [`tags`](./Arrays.md#array-tags) | Array / Enum | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). | 241 ||
| `shield` | Enum / Integer | The shield value granted by this mutation, or 'aux' to use the unit's auxiliary stat. | 191 ||
| `cha` | Enum / Integer | The Charisma stat value or modifier. | 89 ||
| `con` | Enum / Integer | The Constitution stat value or modifier. | 79 ||
| `spd` | Enum / Integer | The Speed stat value or modifier. | 78 ||
| `int` | Enum / Integer || 66 ||
| `lck` | Enum / Integer || 53 ||
| `str` | Enum / Integer || 45 ||
| `dex` | Enum / Integer || 30 ||
| [`keyword_tooltips`](Abilities_and_Spells.md#object-keyword_tooltips) | Object | Associates keyword tooltips with the ability, often used for status effects. | 28 ||
| `divine_shield` | Integer | The number of stacks of the Divine Shield status this mutation provides. | 20 ||
| `CritChanceUp` | Integer | The amount of critical hit chance added as a flat percentage. | 18 | `[1 .5]` (Array), `1` (Number), `50` (Number), `{ ... }` (Object) |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 18 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`lock_item_slot`](Miscellaneous.md#object-lock_item_slot) | Object || 16 ||
| `MissChance` | Integer | The flat percentage chance that the unit's attacks will miss. | 12 | `[1 .5]` (Array), `1` (Number), `20` (Number), `{ ... }` (Object) |
| [`name_mod`](./Strings.md#string-name_mod) | String || 11 ||
| [`SpawnOnBattleStart`](Elite_Buffs.md#object-spawnonbattlestart) | Enum / Object | Specifies the object that spawns adjacent to the unit at the start of battle. | 9 | `ZombieCatFamiliar` (Enum), `BeefyCharmedLeech` (Enum), `{ ... }` (Object) |
| `Trample` | Integer | The amount of bonus damage dealt when moving through an enemy. | 7 | `[1 .5]` (Array), `[3 X-8]` (Array), `1` (Number), `6` (Number), `{ ... }` (Object) |
| [`override_basic_attack`](./Enums.md#enum-override_basic_attack) | Enum || 6 ||
| [`BoostWeaponDamage`](Items_and_Equipment.md#object-boostweapondamage) | Object | The amount of bonus weapon damage applied, or an object with `damage` and `crit_chance` fields. | 5 | `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Quivered` | Array / Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 5 | `[1 0.1]` (Array), `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`desc_multiclass`](./Strings.md#string-desc_multiclass) | String || 5 ||
| [`bonus_items`](./Arrays.md#array-bonus_items) | Array | An array of item names granted as bonus rewards. | 5 ||
| `AmplifyStatus` | Enum || 4 | `Burn` (Enum), `Poison` (Enum), `{ ... }` (Object) |
| `BleedThorns` | Integer | The amount of bleed thorns damage dealt to attackers on hit. | 4 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `StatusImmunity` | Array / Enum | A list of status effect names the unit is immune to. | 4 | `[Burn]` (Array), `[Freeze Slow]` (Array), `Burn` (Enum), `Webbed` (Enum) |
| `auto_plus_signs_on_name` | Boolean || 4 ||
| [`BlastResistance`](#object-blastresistance) | Array / Number / Object || 3 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Blind` | Array / Integer | The amount of blind stacks applied, or an [stacks, probability] array. | 3 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `KineticSpikes` | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 3 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `MoveQuivered` | Integer | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 3 | `[1 0.1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `PoisonThorns` | Integer | The number of stacks of Poison applied to melee attackers when they hit this unit. | 3 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `YOffset` | Number | The vertical offset applied to the unit's visual position, used for floating or hovering effects. | 3 | `-.18` (String), `.25` (String) |
| [`AbilityReaction`](Characters_and_Bosses.md#object-abilityreaction) | Enum / Object | Specifies the ability used as a reaction when the unit is targeted by an ability. | 2 | `SCSneakUp` (Enum), `attack` (Enum), `{ ... }` (Object) |
| [`CounterAttack`](Cat_Mutations.md#object-counterattack) | Array / Enum / Object | Specifies the ability used when the unit counterattacks after being hit. | 2 | `[attack GSScream]` (Array), `Shove` (Enum), `YeticatSnowball_Counter` (Enum), `{ ... }` (Object) |
| `Immobile` | Array / Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 2 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `10` (Number), `{ ... }` (Object) |
| [`PoopWhenHit`](Items_and_Equipment.md#object-poopwhenhit) | Object | Specifies the object (e.g., Poop) spawned when the unit is hit, or an object with `chance` and `object`. | 2 | `Poop` (Enum), `{ ... }` (Object) |
| [`ReflectProjectiles`](Characters_and_Bosses.md#object-reflectprojectiles) | Integer / Object | The percentage chance to reflect projectiles back at the attacker; optionally includes self-damage. | 2 | `1` (Number), `100` (Number), `{ ... }` (Object) |
| `SizeScale` | Number | The multiplier applied to the unit's visual and hitbox size. | 2 | `1.1` (Number), `1.3` (Number), `.6` (String), `.75` (String) |
| [`empty_armor_scaled_stats`](Miscellaneous.md#object-empty_armor_scaled_stats) | Object | Defines the stat bonuses applied when no armor is equipped in a slot. | 2 ||
| [`Vegan`](#object-vegan) | Number / Object | If nonzero, sets the unit as Vegan; can also be an object with localization fields and the `Disorder` class. | 2 | `1` (Number), `{ ... }` (Object) |
| [`AfterImage`](Abilities_and_Spells.md#object-afterimage) | Object | Specifies the object or skill used to create an afterimage of the unit. | 1 | `PlayerCat_ThiefShade2` (Enum), `PlayerCat_ThiefShade` (Enum), `{ ... }` (Object) |
| [`AllyBonusAbilityAura`](Miscellaneous.md#object-allybonusabilityaura) | Enum / Object || 1 | `NubbyToss` (Enum), `{ ... }` (Object) |
| `AlphaCat` | Integer | The number of AlphaCat stacks applied to the source on kill. | 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`AutocastEachTurnBegin`](Miscellaneous.md#object-autocasteachturnbegin) | Enum / Object || 1 | `MindCrack_EldritchVisage2` (Enum), `MindCrack_EldritchVisage` (Enum), `{ ... }` (Object) |
| [`BackflipWhenTargeted`](Abilities_and_Spells.md#object-backflipwhentargeted) | Enum / Integer / Object | The number of backflip charges, or an object defining its ability. | 1 | `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `BackstabCritChance` | Number || 1 | `1` (Number), `.25` (String) |
| [`BoostDamageGlobalAura`](#object-boostdamageglobalaura) | Array / Number / Object || 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`BraceForEachNeighboringEnemy`](#object-braceforeachneighboringenemy) | Array / Number / Object || 1 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`ChainKnockback`](#object-chainknockback) | Number / Object || 1 | `1` (Number), `{ ... }` (Object) |
| [`ChanceToBlockAndCounter`](Items_and_Equipment.md#object-chancetoblockandcounter) | Integer / Object || 1 | `15` (Number), `33` (Number), `{ ... }` (Object) |
| [`ChanceToRevive`](Elite_Buffs.md#object-chancetorevive) | Integer / Object || 1 | `100` (Number), `25` (Number), `{ ... }` (Object) |
| [`CharmAllFlies`](#object-charmallflies) | Array / Number / Object || 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`CollectPickupsOnBattleEnd`](Miscellaneous.md#object-collectpickupsonbattleend) | Number / Object || 1 | `1` (Number), `{ ... }` (Object) |
| [`Conductor`](#object-conductor) | Boolean (Flag) / Number / Object || 1 | `(Flag)` (Boolean (Flag)), `2` (Number), `{ ... }` (Object) |
| [`ConjureBonusAbility`](Abilities_and_Spells.md#object-conjurebonusability) | Enum / Object | Specifies the name of the bonus ability to conjure. | 1 | `Class` (Enum), `Mage` (Enum), `{ ... }` (Object) |
| [`DamageReductionAura`](Miscellaneous.md#object-damagereductionaura) | Array / Number / Object || 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`DeathChill`](#object-deathchill) | Number / Object || 1 | `1` (Number), `{ ... }` (Object) |
| [`DeathRattle`](Characters_and_Bosses.md#object-deathrattle) | Enum / Object | Specifies an ability or effect triggered when the unit dies, optionally with a pop_corpse flag. | 1 | `BoomerCatExplode` (Enum), `BombFlyExplode` (Enum), `{ ... }` (Object) |
| [`DejaVu`](#object-dejavu) | Number / Object || 1 | `10` (Number), `{ ... }` (Object) |
| `DepressionAura` | Integer | The number of stacks of Depression status applied to nearby enemies each turn; can be an object with range and ally settings. | 1 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`DirtyClaws`](#object-dirtyclaws) | Number / Object || 1 | `1` (Number), `{ ... }` (Object) |
| [`DukeOfFlies`](#object-dukeofflies) | Number / Object || 1 | `1` (Number), `{ ... }` (Object) |
| [`Empath`](#object-empath) | Number / Object || 1 | `50` (Number), `100` (Number), `{ ... }` (Object) |
| [`EnergyStorm`](Miscellaneous.md#object-energystorm) | Number / Object || 1 | `3` (Number), `{ ... }` (Object) |
| [`FlyDamageIncrease`](Items_and_Equipment.md#object-flydamageincrease) | Object || 1 | `[1 .5]` (Array), `1` (Number), `4` (Number), `{ ... }` (Object) |
| `Flying` | Integer | If set to 1, grants the unit the Flying passive, allowing movement over obstacles and ignoring terrain penalties. | 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
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
| [`MoveAwayFromDamageSource`](Characters_and_Bosses.md#object-moveawayfromdamagesource) | Object | Specifies the move ability used to flee from the source of damage, or an object with `move_ability`. | 1 | `MoveOne` (Enum), `BasicJump` (Enum), `{ ... }` (Object) |
| [`MoveTowardsDamageSource`](Characters_and_Bosses.md#object-movetowardsdamagesource) | Enum / Object | Determines the movement behavior when moving towards the unit that dealt damage to it. | 1 | `MoveOne` (Enum), `{ ... }` (Object) |
| [`MoveWhenDamaged`](Cat_Mutations.md#object-movewhendamaged) | Enum / Object | Defines movement behavior when the unit takes damage, such as weights and move ability. | 1 | `TKNG_Hop` (Enum), `move` (Enum), `{ ... }` (Object) |
| [`NumbingLeeches`](#object-numbingleeches) | Number / Object || 1 | `3` (Number), `{ ... }` (Object) |
| [`ProtectTargetedAllies`](Characters_and_Bosses.md#object-protecttargetedallies) | Object | Specifies the ability used to protect targeted allies, including an optional target filter. | 1 | `SwapPositions_WideLoad2` (Enum), `SwapPositions_WideLoad` (Enum), `{ ... }` (Object) |
| [`Quiver`](#object-quiver) | Number / Object || 1 | `2` (Number), `1` (Number), `{ ... }` (Object) |
| `RandomStatUp` | Integer / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 1 | `"ceil(X/3)"` (Enum), `"ceil(X/2)"` (Enum), `2` (Number), `-5` (Number) |
| [`Robot`](Characters_and_Bosses.md#object-robot) | Integer / Object | If an integer 1, the unit is robotic and affected by electric/energized effects. If an object, contains further robot-specific properties. | 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`SharePickups`](Characters_and_Bosses.md#object-sharepickups) | Object | If 1 or an object with include_coins, makes the unit share pickups with nearby allies. | 1 | `1` (Number), `{ ... }` (Object) |
| [`ShoulderCheck`](#object-shouldercheck) | Number / Object || 1 | `100` (Number), `33` (Number), `{ ... }` (Object) |
| [`ShovingMatch`](#object-shovingmatch) | Enum / Object || 1 | `attack` (Enum), `{ ... }` (Object) |
| [`SpawnExtraThingsOnBattleStart`](Cat_Mutations.md#object-spawnextrathingsonbattlestart) | Object | An object with `object` and `number` (or range) defining what and how many objects to spawn at battle start. | 1 | `{ ... }` (Object) |
| [`SpawnObjectOnPopCorpse`](Items_and_Equipment.md#object-spawnobjectonpopcorpse) | Enum / Object || 1 | `Coin` (Enum), `Catnip` (Enum), `{ ... }` (Object) |
| `Stealth` | Array / Integer | The number of stealth stacks applied. | 1 | `[1 .1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| [`schadenfreude_scaled_stats`](Miscellaneous.md#object-schadenfreude_scaled_stats) | Object | Defines the stat bonuses (str, dex, con, int, cha) applied by the Schadenfreude trait at a given level. | 1 ||
| [`grant_ability`](./Enums.md#enum-grant_ability) | Enum || 1 ||
| [`StrengthForEachNeighboringEnemy`](#object-strengthforeachneighboringenemy) | Array / Number / Object || 1 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`StrengthInNumbersAura`](Miscellaneous.md#object-strengthinnumbersaura) | Number / Object || 1 | `1` (Number), `{ ... }` (Object) |
| [`Study`](Miscellaneous.md#object-study) | Number / Object || 1 | `1` (Number), `{ ... }` (Object) |
| `SwapHighestAndLowestStat` | Integer || 1 | `1` (Number) |
| `Tech` | Integer | The number of stacks of Tech applied, increasing the source's Tech stat. | 1 | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| [`TileDamageMultiplier`](Miscellaneous.md#object-tiledamagemultiplier) | Number / Object || 1 | `2` (Number), `{ ... }` (Object) |
| [`Vengeful`](#object-vengeful) | Number / Object || 1 | `1` (Number), `{ ... }` (Object) |
| [`Weakness`](#object-weakness) | Array / Integer / Object | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 1 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2039 ||
| [`AddStatusToBasicAttack`](Abilities_and_Spells.md#object-addstatustobasicattack) | Object | Contains status effects to add to the basic attack. | 133 ||
| [`Brace`](./Enums.md) | Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 94 | 2 |
| [`Metal`](./Enums.md) | Integer || 90 | 1 |
| [`Trample`](./Enums.md) | Array / Integer | The amount of bonus damage dealt when moving through an enemy. | 88 | [3] |
| [`Thorns`](./Enums.md) | Integer | The amount of thorns damage dealt to attackers on hit. | 65 | 2 |
| [`MeleeRevengeDamage`](Abilities_and_Spells.md#object-meleerevengedamage) | Object | Defines the damage and effects applied back to a melee attacker upon being hit. | 59 ||
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 52 | 2 |
| [`StatusEachTurnEnd`](Cat_Mutations.md#object-statuseachturnend) | Object | Specifies status effects applied to the unit at the end of each of its turns. | 49 ||
| [`Robot`](Characters_and_Bosses.md#object-robot) | Object | If an integer 1, the unit is robotic and affected by electric/energized effects. If an object, contains further robot-specific properties. | 47 ||
| [`StatusOnBattleEnd`](Abilities_and_Spells.md#object-statusonbattleend) | Object | An object containing status effects or passives applied to the unit when the battle ends. | 45 ||
| [`ElementImmune`](./Enums.md) | Enum | Specifies an element type (e.g., Fire, Ice) that the unit is immune to damage from. | 39 | Ice |
| [`SpawnOnBattleStart`](Elite_Buffs.md#object-spawnonbattlestart) | Enum / Object | Specifies the object that spawns adjacent to the unit at the start of battle. | 36 | CharmedTinySpider |
| [`DeathRattle`](Characters_and_Bosses.md#object-deathrattle) | Enum / Object | Specifies an ability or effect triggered when the unit dies, optionally with a pop_corpse flag. | 35 | BoomerCatExplode |
| [`CounterAttack`](./Enums.md) | Enum | Specifies the ability used when the unit counterattacks after being hit. | 34 | ReflexPunchJab |
| [`StatusImmunity`](./Enums.md) | Array / Enum | A list of status effect names the unit is immune to. | 34 | [Sleep] |
| [`StatusOnKill`](Cat_Mutations.md#object-statusonkill) | Object | Specifies status effects or actions triggered when the unit kills an enemy. | 29 ||
| [`StatusOnTookDamage`](Cat_Mutations.md#object-statusontookdamage) | Object | Specifies status effects or actions triggered when the unit takes damage. | 29 ||
| [`SpawnThingOnDamage`](Cat_Mutations.md#object-spawnthingondamage) | Object | Specifies an object that spawns on the tile when the unit takes damage. | 28 ||
| [`AbilityReaction`](Characters_and_Bosses.md#object-abilityreaction) | Enum / Object | Specifies the ability used as a reaction when the unit is targeted by an ability. | 23 | PissYourself |
| [`AddPassivesToMinions`](Items_and_Equipment.md#object-addpassivestominions) | Object || 21 ||
| [`DamageUp`](./Enums.md) | Integer | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 21 | 2 |
| [`AddMovement`](./Enums.md) | Integer | The amount of bonus movement points added to the unit's base movement. | 20 | 20 |
| [`ArmorDodgeChance`](./Enums.md) | Integer || 19 | 10 |
| [`StatusEachTurnBegin`](Cat_Mutations.md#object-statuseachturnbegin) | Object | Specifies status effects applied to the unit at the start of each of its turns. | 18 ||
| [`CritChanceUp`](./Enums.md) | Integer | The amount of critical hit chance added as a flat percentage. | 16 | 80 |
| [`AddBonusRange`](./Enums.md) | Integer | The number of additional tiles of range added to the unit's abilities. | 15 | 2 |
| [`RevengeDamage`](Abilities_and_Spells.md#object-revengedamage) | Object | An object defining the damage and effects that trigger when the unit is attacked. | 15 ||
| [`SpawnEachTurn`](Cat_Mutations.md#object-spawneachturn) | Object | Specifies an object that spawns on a random adjacent tile each turn, with optional chance. | 15 ||
| [`StatusOnBattleStart`](Items_and_Equipment.md#object-statusonbattlestart) | Object || 15 ||
| [`AddCorpseHealth`](./Enums.md) | Integer | The amount of bonus health the unit's corpse has before it can be resurrected. | 14 | 96 |
| [`AllStatsUp`](./Enums.md) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 14 | [.5] |
| [`DodgeChance`](./Enums.md) | Integer | The percentage chance the unit has to dodge incoming attacks. | 14 | 50 |
| [`InnateElement`](./Enums.md) | Enum | Specifies the innate elemental type of the unit (e.g., Fire, Ice, Electric). | 14 | Ice |
| [`SizeScale`](./Enums.md) | Number | The multiplier applied to the unit's visual and hitbox size. | 14 | .4 |
| [`WaterWalk`](./Enums.md) | Integer | If greater than 0, allows the unit to traverse water tiles as if they were ground. | 14 | 1 |
| [`AddManaRegen`](./Enums.md) | Integer | The flat amount of mana regenerated per turn. | 13 | 7 |
| [`MulticlassLevelUp`](./Enums.md) | Enum | Specifies the class that this unit gains a level in when multiclassing. | 12 | Druid |
| [`SpawnThingOnDeath`](./Enums.md) | Enum | Specifies the name of an object to spawn upon death. | 12 | CharmedDemonKitten |
| [`AbilityOnBattleStart`](./Enums.md) | Enum || 11 | neck_ChefsApron |
| [`AddStatusToAllDamage`](Items_and_Equipment.md#object-addstatustoalldamage) | Object || 11 ||
| [`BleedThorns`](./Enums.md) | Integer | The amount of bleed thorns damage dealt to attackers on hit. | 11 | 2 |
| [`ExtraBasicAttacks`](./Enums.md) | Integer | The number of additional basic attacks the unit can perform per turn. | 11 | 2 |
| [`MoveWhenDamaged`](Cat_Mutations.md#object-movewhendamaged) | Object | Defines movement behavior when the unit takes damage, such as weights and move ability. | 11 ||
| [`ReplaceBasicMove`](./Enums.md) | Enum | Specifies an alternative movement ability that replaces the unit's default move. | 11 | ToadJump_BasicMove |
| [`AddLevelUpRerolls`](./Enums.md) | Integer | The number of additional rerolls the unit gets when leveling up. | 10 | 2 |
| [`LimitDamage`](./Enums.md) | Integer | The maximum amount of damage the unit can take from a single hit. | 10 | 1 |
| [`MoveTowardsDamageSource`](Characters_and_Bosses.md#object-movetowardsdamagesource) | Object | Determines the movement behavior when moving towards the unit that dealt damage to it. | 10 ||
| [`StatusOnKillEnemy`](Items_and_Equipment.md#object-statusonkillenemy) | Object || 10 ||
| [`AddSelfStatusToBasicAttack`](Items_and_Equipment.md#object-addselfstatustobasicattack) | Object || 9 ||
| [`AddTag`](./Enums.md) | Enum | Specifies a gameplay tag (e.g., 'rock', 'plant') to add to the unit, used for interaction checks. | 9 | rock |
| [`BackstabImmunity`](./Enums.md) | Integer | If greater than 0, prevents the unit from taking extra damage from backstabs. | 9 | 1 |
| [`Bruise`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 9 | 2 |
| [`DepressionAura`](./Enums.md) | Integer | The number of stacks of Depression status applied to nearby enemies each turn; can be an object with range and ally settings. | 9 | 2 |
| [`Flying`](./Enums.md) | Integer | If set to 1, grants the unit the Flying passive, allowing movement over obstacles and ignoring terrain penalties. | 9 | 1 |
| [`LimitHeal`](./Enums.md) | Integer | If 1, prevents the unit from being healed. | 9 | 1 |
| [`MissChance`](./Enums.md) | Integer | The flat percentage chance that the unit's attacks will miss. | 9 | 15 |
| [`MovementReaction`](Characters_and_Bosses.md#object-movementreaction) | Object | Specifies an ability to cast when a unit moves within range, with options for targeting and conditions. | 9 ||
| [`PoisonThorns`](./Enums.md) | Integer | The number of stacks of Poison applied to melee attackers when they hit this unit. | 9 | 2 |
| [`SmallRockBehavior`](./Enums.md) | Integer | Defines the damage, knockback, and chain properties of small rocks spawned from this unit when destroyed. | 9 | 5 |
| [`StatusAlliesOnBattleStart`](Items_and_Equipment.md#object-statusalliesonbattlestart) | Object || 9 ||
| [`TrinketPassiveMultiplierBonus`](./Enums.md) | Integer || 9 | 2 |
| [`BoostHeals`](./Enums.md) | Integer || 8 | -2 |
| [`ChanceToRevive`](Elite_Buffs.md#object-chancetorevive) | Integer / Object || 8 | 25 |
| [`PermanentMadness`](./Enums.md) | Integer | The number of permanent madness stacks applied. | 8 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 8 |
| [`AddElementsToBasicAttack`](./Enums.md) | Enum | Specifies an elemental damage type that is added to the unit's basic attacks. | 7 | Ice |
| [`AddInitiative`](./Enums.md) | Integer | The amount of bonus or penalty to the unit's turn order initiative value. | 7 | -100 |
| [`AlphaTurns`](./Enums.md) | Integer | The number of turns the unit acts first in battle; negative values may indicate last. | 7 | -1 |
| [`Bleed`](./Enums.md) | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 7 | [.1] |
| [`BonusAbility`](./Enums.md) | Enum | Specifies the name of a bonus ability granted. | 7 | FighterBonusThrow |
| [`DamageNeighborsOnEndMove`](Miscellaneous.md#object-damageneighborsonendmove) | Object || 7 ||
| [`DebuffImmunity`](./Enums.md) | Integer | If 1, the unit is immune to debuffs. | 7 | 1 |
| [`ManaCostReduction`](./Enums.md) | Integer | The amount or percentage by which ability mana costs are reduced for this unit. | 7 | 2 |
| [`OverrideBasicAttack`](./Enums.md) | Enum || 7 | GerdShot |
| [`OverrideMaxHealth`](./Enums.md) | Integer | Replaces the unit's maximum health with this value. | 7 | 1 |
| [`PassiveAtHealthThreshold`](Items_and_Equipment.md#object-passiveathealththreshold) | Object || 7 ||
| [`PassiveAtStatThreshold`](Items_and_Equipment.md#object-passiveatstatthreshold) | Object || 7 ||
| [`SecurityBotProtect`](Characters_and_Bosses.md#object-securitybotprotect) | Object | Specifies the ability and movement used by a security bot to protect allies. | 7 ||
| [`SetSpellCosts`](./Enums.md) | Integer | Overrides the cost of all spells to this value. | 7 | 3 |
| [`SpeedUp`](./Enums.md) | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 7 | 2 |
| [`StatusOnEndMove`](Cat_Mutations.md#object-statusonendmove) | Object | Specifies status effects or actions triggered when the unit finishes moving. | 7 ||
| [`AddDamageToElementDamage`](Cat_Mutations.md#object-adddamagetoelementdamage) | Object | Defines additional damage of a specific element added to the unit's attacks. | 6 ||
| [`AmplifyStatus`](Miscellaneous.md#object-amplifystatus) | Enum / Object || 6 | Poison |
| [`ExtraWeaponAttacks`](./Enums.md) | Integer || 6 | 2 |
| [`IgnoreTiles`](./Enums.md) | Integer | If set to 1, movement ignores tile-based penalties or restrictions. | 6 | 1 |
| [`Poison`](./Enums.md) | Array / Enum / Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 6 | [.5] |
| [`Quivered`](./Enums.md) | Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 6 | 2 |
| [`ReplaceBasicAttack`](./Enums.md) | Enum | Specifies the ability ID that replaces the unit's basic attack. | 6 | BasicButcherMeleeWideDoubleSpin |
| [`SpawnOnBattleStartRandomEmptyTile`](Cat_Mutations.md#object-spawnonbattlestartrandomemptytile) | Object | Specifies an object that spawns on a random empty tile at the start of battle. | 6 ||
| [`StatusOnTookDamageFromAbility`](Cat_Mutations.md#object-statusontookdamagefromability) | Object | Specifies status effects triggered when the unit takes damage specifically from an ability (not environmental). | 6 ||
| [`TileTrail`](./Enums.md) | Enum | Specifies the type of tile left behind as the unit moves. | 6 | FlowerTile |
| [`AddBonusMeleeRange`](./Enums.md) | Integer | The number of additional tiles of range added to the unit's melee attacks. | 5 | 2 |
| [`AddHiddenTag`](./Enums.md) | Enum | A hidden tag applied to the unit for internal logic and triggers. | 5 | bowling_ball |
| [`AutocastEachRound`](Abilities_and_Spells.md#object-autocasteachround) | Object | Contains an ability name and optional 'even_if_stunned' flag to autocast each round. | 5 ||
| [`BackstabCritChance`](./Enums.md) | Integer || 5 | 1 |
| [`Burn`](./Enums.md) | Enum / Integer | The amount of Burn applied, either as a fixed number or a formula string. | 5 | 2 |
| [`ClassManaCostReduction`](Cat_Mutations.md#object-classmanacostreduction) | Object | Defines a reduction in mana cost for abilities of a specific class. | 5 ||
| [`CritsApplyStatus`](Items_and_Equipment.md#object-critsapplystatus) | Object || 5 ||
| [`FaceShield`](./Enums.md) | Integer | If 1, the unit has a face shield that protects it from certain attacks or effects. | 5 | 0 |
| [`HeadArmorPassiveMultiplierBonus`](./Enums.md) | Integer || 5 | 2 |
| [`InjuryImmunity`](./Enums.md) | Integer | The number of turns the unit is immune to injuries. | 5 | 1 |
| [`KnockbackImmunity`](./Enums.md) | Integer | If set to 1, the unit cannot be knocked back. | 5 | 1 |
| [`StatusIfUnusedMovePoints`](Cat_Mutations.md#object-statusifunusedmovepoints) | Object | Specifies status effects applied if the unit ends its turn with unused movement points. | 5 ||
| [`StatusOnTurnEndIfDidntCastAbilityTypes`](Items_and_Equipment.md#object-statusonturnendifdidntcastabilitytypes) | Object || 5 ||
| [`TrinketActiveEffectsMultiplierBonus`](./Enums.md) | Integer || 5 | 2 |
| [`AddCritMultiplier`](./Enums.md) | Integer || 4 | 200 |
| [`AddKnockbackDamage`](./Enums.md) | Integer | The amount of additional knockback damage applied. | 4 | 2 |
| [`AddStatusToElementDamage`](Items_and_Equipment.md#object-addstatustoelementdamage) | Object || 4 ||
| [`AddStatusToWeapons`](Characters_and_Bosses.md#object-addstatustoweapons) | Object | Specifies status effects to add to the unit's weapon attacks, with their stack counts. | 4 ||
| [`AddTemporaryEffectsToBasicAttack`](Cat_Mutations.md#object-addtemporaryeffectstobasicattack) | Object | A container object that lists temporary status effects applied to the unit's basic attack. | 4 ||
| [`BlastResistance`](./Enums.md) | Integer || 4 | 2 |
| [`BoostWeaponDamage`](Items_and_Equipment.md#object-boostweapondamage) | Integer / Object | The amount of bonus weapon damage applied, or an object with `damage` and `crit_chance` fields. | 4 | 2 |
| [`BuffImmunity`](./Enums.md) | Integer | If 1, the unit is immune to buffs. An optional object can list buffs to exclude from immunity. | 4 | 1 |
| [`CatchProjectiles`](Items_and_Equipment.md#object-catchprojectiles) | Object || 4 ||
| [`ChanceToBackflip`](Cat_Mutations.md#object-chancetobackflip) | Object | An object specifying the ability to use and the percentage chance to perform a backflip dodge when hit. | 4 ||
| [`EquipTemporaryItem`](./Enums.md) | Enum | Specifies which temporary item is equipped. | 4 | FoodMedium |
| [`ExtraStatusWhenDealingDamage`](Items_and_Equipment.md#object-extrastatuswhendealingdamage) | Object || 4 ||
| [`FaceArmorPassiveMultiplierBonus`](./Enums.md) | Integer || 4 | 2 |
| [`ForceSpecificInjury`](./Enums.md) | Enum || 4 | int |
| [`FreezePiercing`](./Enums.md) | Integer || 4 | 1 |
| [`IncreaseExplosionDamage`](./Enums.md) | Integer || 4 | 2 |
| [`IncreaseExplosionSize`](./Enums.md) | Integer || 4 | 2 |
| [`LevelUpClassOverride`](./Enums.md) | Enum || 4 | Jester |
| [`MakeSpellsRequireCharge`](./Enums.md) | Integer || 4 | 1 |
| [`PassiveIfAllArmorEmpty`](Miscellaneous.md#object-passiveifallarmorempty) | Object || 4 ||
| [`PassiveWhenAffectedByElement`](Cat_Mutations.md#object-passivewhenaffectedbyelement) | Object | An object containing `element` and `passives` that grants the listed passives while the unit is affected by the specified element. | 4 ||
| [`StatusAlliesOnDeath`](Items_and_Equipment.md#object-statusalliesondeath) | Object || 4 ||
| [`StatusEveryXSpellCasts`](Cat_Mutations.md#object-statuseveryxspellcasts) | Object | An object with `stacks` (number of spell casts) and status effects to apply after that many spell casts. | 4 ||
| [`StatusOnAllyCatDeath`](Cat_Mutations.md#object-statusonallycatdeath) | Object | An object listing status effects applied to the unit when an allied cat dies. | 4 ||
| [`StatusOnCastSpell`](Cat_Mutations.md#object-statusoncastspell) | Object | An object listing status effects applied to the unit whenever it casts a spell. | 4 ||
| [`StatusOnGainCoins`](Characters_and_Bosses.md#object-statusongaincoins) | Object | Specifies status effects applied when this unit gains coins. | 4 ||
| [`StatusOnPopCorpse`](Items_and_Equipment.md#object-statusonpopcorpse) | Object || 4 ||
| [`AbilityWhenTaggedCharacterMovesNear`](Cat_Mutations.md#object-abilitywhentaggedcharactermovesnear) | Object | An object containing `ability`, `tag`, and `range` that triggers the specified ability when a character with the given tag moves within range. | 3 ||
| [`AddPassivesToCharmed`](Items_and_Equipment.md#object-addpassivestocharmed) | Object || 3 ||
| [`AddStatusToBasicMeleeAttack`](Cat_Mutations.md#object-addstatustobasicmeleeattack) | Object | An object listing status effects applied by the unit's basic melee attack. | 3 ||
| [`AddStatusToElementAbilities`](Miscellaneous.md#object-addstatustoelementabilities) | Object || 3 ||
| [`AddStatusToSpells`](Characters_and_Bosses.md#object-addstatustospells) | Object | Specifies status effects added to all spell attacks used by this unit. | 3 ||
| [`AllyBonusAbilityAura`](Miscellaneous.md#object-allybonusabilityaura) | Enum / Object || 3 | NubbyToss |
| [`AmplifyKnockback`](./Enums.md) | Integer || 3 | 2 |
| [`ApplyStatusesToRandomEnemiesEachTurn`](Items_and_Equipment.md#object-applystatusestorandomenemieseachturn) | Object || 3 ||
| [`AutoEquipConsumables`](./Enums.md) | Integer || 3 | 1 |
| [`BasicAttackCritChance`](./Enums.md) | Integer || 3 | 100 |
| [`BasicAttackDamageMultiplier`](./Enums.md) | Number || 3 | 33.333334 |
| [`ChanceToBlockAndCounter`](./Enums.md) | Integer || 3 | 33 |
| [`DamageNeighborsAfterMove`](Elite_Buffs.md#object-damageneighborsaftermove) | Object || 3 ||
| [`ElementalManaCostReduction`](Items_and_Equipment.md#object-elementalmanacostreduction) | Object || 3 ||
| [`ExtraBasicMoves_Status`](./Enums.md) | Integer | The number of extra basic moves per turn granted. | 3 | 1 |
| [`ExtraMovePoints`](./Enums.md) | Integer | The number of additional movement points granted to this unit. | 3 | 1 |
| [`FlowersOnEndTurn`](./Enums.md) | Integer || 3 | 3 |
| [`IncreaseSpellRange`](./Enums.md) | Integer || 3 | 5 |
| [`KillsToMeat`](./Enums.md) | Enum || 3 | Food |
| [`MoveAndUseAbilityEachTurnBeginIfPossible`](./Enums.md) | Enum || 3 | EatShit |
| [`MoveQuivered`](./Enums.md) | Integer | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 3 | 2 |
| [`NeckArmorPassiveMultiplierBonus`](./Enums.md) | Integer || 3 | 2 |
| [`PassiveAfterXKills`](Items_and_Equipment.md#object-passiveafterxkills) | Object || 3 ||
| [`PassiveIfEmptyFace`](Miscellaneous.md#object-passiveifemptyface) | Object || 3 ||
| [`PassiveIfEmptyHead`](Miscellaneous.md#object-passiveifemptyhead) | Object || 3 ||
| [`PassiveIfEmptyNeck`](Miscellaneous.md#object-passiveifemptyneck) | Object || 3 ||
| [`ProtectTargetedAllies`](./Enums.md) | Enum | Specifies the ability used to protect targeted allies, including an optional target filter. | 3 | SwapPositions_WideLoad2 |
| [`RandomPassivePool`](Characters_and_Bosses.md#object-randompassivepool) | Object | A pool of random passives from which one is chosen for this unit. | 3 ||
| [`RangedTrueShot`](./Enums.md) | Integer || 3 | 1 |
| [`ReplaceBasicAttackWhenCastable`](./Enums.md) | Enum || 3 | Shank2 |
| [`ReplaceSpawnedObjects`](./Enums.md) | Array || 3 | [Boulder] |
| [`SetDefaultFacePassive`](./Enums.md) | Enum || 3 | insane |
| [`SpawnCreepOnHit`](./Enums.md) | Integer | If set to 1, spawns creep on the tile when this unit takes damage. | 3 | 1 |
| [`SpawnObjectOnPopCorpse`](./Enums.md) | Enum || 3 | Food |
| [`StatusAfterCastSpell`](Items_and_Equipment.md#object-statusaftercastspell) | Object || 3 ||
| [`StatusOnBreakItem`](Items_and_Equipment.md#object-statusonbreakitem) | Object || 3 ||
| [`StatusOnCrit`](Miscellaneous.md#object-statusoncrit) | Object || 3 ||
| [`StatusOnEatFood`](Cat_Mutations.md#object-statusoneatfood) | Object | An object listing status effects applied to the unit when it eats food. | 3 ||
| [`StatusOnOverHealed`](Miscellaneous.md#object-statusonoverhealed) | Object || 3 ||
| [`StatusOnStanceSwitch`](Miscellaneous.md#object-statusonstanceswitch) | Object || 3 ||
| [`StatusOnTurnEndIfCastNSpells`](Miscellaneous.md#object-statusonturnendifcastnspells) | Object || 3 ||
| [`StatusOnUseAbilityWithTag`](Miscellaneous.md#object-statusonuseabilitywithtag) | Object || 3 ||
| [`StrengthUp`](./Enums.md) | Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 3 | 2 |
| [`WeaponsDontLoseDurability`](./Enums.md) | Integer | If set to 1, weapons equipped by this unit do not lose durability. | 3 | 0 |
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
| [`CCImmunity`](./Enums.md) | Integer | If set to 1, this unit is immune to crowd control effects. | 2 | 1 |
| [`CanRemoveCursedItems`](./Enums.md) | Integer | If nonzero, allows the unit to remove cursed items from equipment slots. | 2 | 1 |
| [`CapMovementAbilityRange`](./Enums.md) | Integer || 2 | 1 |
| [`ChangeTauntPriority`](./Enums.md) | Integer || 2 | -1 |
| [`ConsumableEffectsMultiplierBonus`](./Enums.md) | Integer || 2 | 1 |
| [`DisableAbilities`](./Enums.md) | Enum || 2 | all_items |
| [`DoubleCastWeapons`](./Enums.md) | Integer || 2 | 2 |
| [`Eternal`](Items_and_Equipment.md#object-eternal) | Object || 2 ||
| [`FlyDamageIncrease`](./Enums.md) | Integer || 2 | 4 |
| [`FreePathfindElement`](./Enums.md) | Enum | Specifies a terrain element (e.g., Water, Grass) that the unit can pathfind through without penalty. | 2 | Grass |
| [`GainExtraShield`](./Enums.md) | Integer || 2 | 2 |
| [`HPGainBlock`](./Enums.md) | Integer || 2 | 1 |
| [`InfiniteRebirth`](Characters_and_Bosses.md#object-infiniterebirth) | Object | Specifies the health and effects for unlimited rebirth upon death. | 2 ||
| [`ManaCostReductionTagged`](Miscellaneous.md#object-manacostreductiontagged) | Object || 2 ||
| [`MoveAwayFromDamageSource`](./Enums.md) | Enum | Specifies the move ability used to flee from the source of damage, or an object with `move_ability`. | 2 | MoveOne |
| [`MoveSpeedMultiplier`](./Enums.md) | Number || 2 | .5 |
| [`NubbyTossPriority`](./Enums.md) | Integer || 2 | 1 |
| [`PassiveLevelUpAtCombatEnd`](./Enums.md) | Integer || 2 | 1 |
| [`PassiveWhenAtFullMana`](Cat_Mutations.md#object-passivewhenatfullmana) | Object | An object listing passive effects that are active only while the unit's mana is full. | 2 ||
| [`PassiveWhileInMonkMeleeStance`](Items_and_Equipment.md#object-passivewhileinmonkmeleestance) | Object || 2 ||
| [`PoopWhenHit`](./Enums.md) | Enum | Specifies the object (e.g., Poop) spawned when the unit is hit, or an object with `chance` and `object`. | 2 | Poop |
| [`RemoveLineOfSightRestrictions`](./Enums.md) | Integer || 2 | 1 |
| [`ScaledStatusOnSpendMana`](Items_and_Equipment.md#object-scaledstatusonspendmana) | Object || 2 ||
| [`SharePickups`](./Enums.md) | Integer | If 1 or an object with include_coins, makes the unit share pickups with nearby allies. | 2 | 1 |
| [`SpawnCatCopyOnBattleStart`](Miscellaneous.md#object-spawncatcopyonbattlestart) | Object || 2 ||
| [`StatsAtLowHealth`](Miscellaneous.md#object-statsatlowhealth) | Object || 2 ||
| [`StatusEachTurnEndForEachTurn`](Characters_and_Bosses.md#object-statuseachturnendforeachturn) | Object | Statuses applied at the end of each turn, with the number of turns as nested values. | 2 ||
| [`StatusKilledCharacters`](Cat_Mutations.md#object-statuskilledcharacters) | Object | An object listing status effects applied to the unit when it kills a character. | 2 ||
| [`StatusOnCollectPickup`](Items_and_Equipment.md#object-statusoncollectpickup) | Object || 2 ||
| [`StatusOnEatPill`](Miscellaneous.md#object-statusoneatpill) | Object || 2 ||
| [`StatusOnHealed`](Items_and_Equipment.md#object-statusonhealed) | Object || 2 ||
| [`StatusOnPickupCoins`](Items_and_Equipment.md#object-statusonpickupcoins) | Object || 2 ||
| [`StatusOnTurnEndIfManaExact`](Miscellaneous.md#object-statusonturnendifmanaexact) | Object || 2 ||
| [`StatusOnTurnEndIfManaOrHealthExact`](Miscellaneous.md#object-statusonturnendifmanaorhealthexact) | Object || 2 ||
| [`StatusOnUseBasicAttack`](Items_and_Equipment.md#object-statusonusebasicattack) | Object || 2 ||
| [`StatusWhenAllySpendsMana`](Items_and_Equipment.md#object-statuswhenallyspendsmana) | Object || 2 ||
| [`TauntAlways`](./Enums.md) | Integer || 2 | 1 |
| [`TowerDefenseReflex`](./Enums.md) | Enum | Specifies the ability or attack used when the unit counterattacks in tower defense reflex mode. | 2 | BasicRanged_1DMG |
| [`UncappedHP`](./Enums.md) | Integer | If 1, the unit's maximum HP is not capped by standard limits. | 2 | 1 |
| [`UpgradeSpawnedPickups`](./Enums.md) | Integer || 2 | 2 |
| [`Weakness`](./Enums.md) | Enum / Integer | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 2 | 2 |
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
| [`AfterImage`](./Enums.md) | Enum | Specifies the object or skill used to create an afterimage of the unit. | 1 | PlayerCat_ThiefShade2 |
| [`AllowPassTurn`](./Enums.md) | Integer || 1 | 0 |
| [`AllyDamageReaction`](./Enums.md) | Enum || 1 | attack |
| [`AllyHealthRegenAura`](Miscellaneous.md#object-allyhealthregenaura) | Object || 1 ||
| [`AllyMoveAbilityAura`](./Enums.md) | Enum || 1 | CatapultJump2 |
| [`AllyMultiplyKnockbackDamage`](./Enums.md) | Integer || 1 | 2 |
| [`AlphaCat`](./Enums.md) | Integer | The number of AlphaCat stacks applied to the source on kill. | 1 | 1 |
| [`AlternateCraftingPools`](Miscellaneous.md#object-alternatecraftingpools) | Object || 1 ||
| [`AmplifyPositiveStatus`](./Enums.md) | Integer || 1 | 2 |
| [`Autism`](Miscellaneous.md#object-autism) | Object || 1 ||
| [`AutoCritLowDamage`](./Enums.md) | Integer || 1 | 2 |
| [`BackstabWeakness`](./Enums.md) | Number || 1 | 0.75 |
| [`BasicAttackStatusCarefulness`](./Enums.md) | Integer || 1 | 1 |
| [`BlacklistPickupType`](./Enums.md) | Enum | Specifies a pickup type (e.g., food, catnip) that the unit will refuse to pick up. | 1 | food |
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
| [`DisableAbilitiesWithTag`](./Enums.md) | Enum | Specifies a tag that disables any ability with that tag on the unit. | 1 | meat |
| [`Doomed`](./Enums.md) | Integer | The number of stacks of Doomed applied, causing the target to die after a set number of turns. | 1 | 3 |
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
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object | The name of the ability the source is forced to use, optionally with a chance. | 1 | Hallucinate_Disorder |
| [`FreeSpellsAtFullMana`](./Enums.md) | Integer || 1 | 1 |
| [`FrontstabBasicAttackCritChance`](./Enums.md) | Integer || 1 | 100 |
| [`FullHeal`](./Enums.md) | Integer | If non-zero, fully restores the target's health. | 1 | 1 |
| [`FullHealthCritChance`](./Enums.md) | Integer || 1 | 100 |
| [`FullPower`](./Enums.md) | Integer || 1 | 3 |
| [`FurnitureStats`](Miscellaneous.md#object-furniturestats) | Object || 1 ||
| [`GravityWell`](Miscellaneous.md#object-gravitywell) | Object || 1 ||
| [`HealDamagesEnemies`](./Enums.md) | Integer || 1 | 1 |
| [`HealsAlsoRegenMana`](./Enums.md) | Integer || 1 | 2 |
| [`HealsCanRevive`](./Enums.md) | Integer || 1 | 3 |
| [`HolyShieldTransferToTaggedMinions`](./Enums.md) | Enum || 1 | any |
| [`HouseFoodRequirementMultiplier`](./Enums.md) | Integer | A multiplier for the amount of food the house requires; 0 removes the food requirement. | 1 | 0 |
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
| [`Madness`](./Enums.md) | Integer | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 1 | 1 |
| [`MakeBasicAttackPassThroughThings`](./Enums.md) | Integer || 1 | 1 |
| [`ManaRegenMultiplierIfManaEmpty`](./Enums.md) | Integer || 1 | 2 |
| [`MaxAccuracy`](./Enums.md) | Integer || 1 | 1 |
| [`MaxStartingMana`](./Enums.md) | Integer || 1 | 1 |
| [`MegaMinions`](Miscellaneous.md#object-megaminions) | Integer / Object || 1 | 3 |
| [`MetalDetector`](./Enums.md) | Integer || 1 | 5 |
| [`MinimumTech`](./Enums.md) | Integer || 1 | 1 |
| [`NoManaRegen`](./Enums.md) | Integer | The unit does not naturally regenerate mana per turn. Value indicates the stage or flag enabling this restriction. | 1 | 1 |
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
| [`PermanentImmobile`](./Enums.md) | Integer | The permanent amount of immobility stacks applied. | 1 | 1 |
| [`PermanentItems`](./Enums.md) | Integer || 1 | 2 |
| [`PermanentKitten`](./Enums.md) | Integer || 1 | 1 |
| [`Phasing`](./Enums.md) | Integer | If set to 1, allows the character to phase through solid objects or obstacles. | 1 | 1 |
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
| [`ShowHiddenThings`](./Enums.md) | Integer | If nonzero, reveals hidden objects or tiles on the map. | 1 | 1 |
| [`Slow`](./Enums.md) | Enum / Integer | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 1 | 2 |
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
| [`StatusKillers`](Abilities_and_Spells.md#object-statuskillers) | Object | An object containing nested conditionals that apply status effects when the unit kills an enemy. | 1 ||
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
| [`Stealth`](./Enums.md) | Integer | The number of stealth stacks applied. | 1 | 1 |
| [`StrengthForEachNeighboringEnemy`](./Enums.md) | Integer || 1 | 2 |
| [`StrengthInNumbersAura`](Miscellaneous.md#object-strengthinnumbersaura) | Integer / Object || 1 | 1 |
| [`StrictLimitDamage`](./Enums.md) | Integer || 1 | 1 |
| [`Study`](Miscellaneous.md#object-study) | Integer / Object || 1 | 1 |
| [`TaggedPickupEffectReplacement`](Miscellaneous.md#object-taggedpickupeffectreplacement) | Object || 1 ||
| [`TauntAtFullHealth`](./Enums.md) | Integer || 1 | 1 |
| [`Tech`](./Enums.md) | Integer | The number of stacks of Tech applied, increasing the source's Tech stat. | 1 | 1 |
| [`TempInitiativeChange`](./Enums.md) | Integer | The flat change to the unit's initiative value. | 1 | -999 |
| [`TheHunger`](Miscellaneous.md#object-thehunger) | Object || 1 ||
| [`TileDamageMultiplier`](Miscellaneous.md#object-tiledamagemultiplier) | Integer / Object || 1 | 2 |
| [`TourettesMeows`](Miscellaneous.md#object-tourettesmeows) | Object || 1 ||
| [`TowerDefense`](Miscellaneous.md#object-towerdefense) | Object || 1 ||
| [`TrapEffectsMultiplier`](./Enums.md) | Integer || 1 | 2 |
| [`Triskaidekaphobia`](./Enums.md) | Integer || 1 | 13 |
| [`UncappedMana`](./Enums.md) | Integer || 1 | 1 |
| [`UpgradeLevelUpClassActives`](./Enums.md) | Enum || 1 | Colorless |
| [`UpgradeLevelUpClassPassives`](./Enums.md) | Enum || 1 | Colorless |
| [`Vegan`](./Enums.md) | Integer | If nonzero, sets the unit as Vegan; can also be an object with localization fields and the `Disorder` class. | 1 | 1 |
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
| `con` | Enum / Integer | The Constitution stat value or modifier. | 34 ||
| `spd` | Enum / Integer | The Speed stat value or modifier. | 27 ||
| `cha` | Enum / Integer | The Charisma stat value or modifier. | 24 ||
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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 205 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 56 |
| [`Bleed`](./Enums.md) | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 30 | [.1] |
| [`Poison`](./Enums.md) | Array / Enum / Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 29 | [.5] |
| [`Knockback`](./Enums.md) | Integer | The number of tiles the target is pushed away from the source on hit. | 24 | 3 |
| [`Burn`](./Enums.md) | Enum / Integer | The amount of Burn applied, either as a fixed number or a formula string. | 16 | 2 |
| [`Fear`](./Enums.md) | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 13 | [.15] |
| [`Bruise`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 12 | 2 |
| [`ChangeTile`](Abilities_and_Spells.md#object-changetile) | Enum / Object | Specifies the tile type to change to, or an object defining tile change parameters (tile type and area of effect). | 10 | FloatingGlassTile |
| [`Slow`](./Enums.md) | Enum / Integer | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 10 | 2 |
| [`Stun`](./Enums.md) | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 8 | [.05*X] |
| [`Confusion`](./Enums.md) | Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 7 | 2 |
| [`Weakness`](./Enums.md) | Enum / Integer | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 7 | 2 |
| [`Conditional_Ally`](Abilities_and_Spells.md#object-conditional_ally) | Object || 5 ||
| [`Leech`](./Enums.md) | Integer | The amount of health leeched from the target (heals the attacker). | 5 | 1 |
| [`Rot`](./Enums.md) | Integer | Integer, or an array [stacks, probability] specifying the amount of Rot stacks applied with the given probability. | 5 | -999999 |
| [`BounceObject`](./Enums.md) | Enum | Specifies the object or projectile to spawn and bounce from the target. | 4 | CharmedLeech |
| [`DamageOrHealConditionally`](./Enums.md) | Integer | The amount of conditional damage or healing applied, based on certain conditions (e.g., ally or enemy). | 4 | 1 |
| [`DistanceBonusDamage`](Engine_StatusAndPassiveKeys.md#object-distancebonusdamage) | Object || 4 ||
| [`Freeze`](./Enums.md) | Array / Integer | The amount of freeze stacks applied, or an [stacks, probability] array. | 4 | [.15] |
| [`Leeches`](./Enums.md) | Integer | The number of stacks of the Leeches debuff applied, which deals damage over time and heals the applier. | 4 | 1 |
| [`SoulLink`](./Enums.md) | Integer | The number of soul link stacks applied. | 4 | 1 |
| [`Charmed`](./Enums.md) | Array / Integer | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 3 | [.40] |
| [`Conditional_Enemy`](Abilities_and_Spells.md#object-conditional_enemy) | Object || 3 ||
| [`Madness`](./Enums.md) | Integer | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 3 | 1 |
| [`MagicWeakness`](./Enums.md) | Integer | The amount of magic weakness stacks applied, or an [stacks, probability] array. | 3 | 2 |
| [`Piercing`](./Enums.md) | Integer || 3 | 1 |
| [`SpreadDisease`](Abilities_and_Spells.md#object-spreaddisease) | Object | Defines the parameters for spreading a disease, including chance, disease type, and whether it can apply to any target. | 3 ||
| [`ApplyStatusIfCrit`](Abilities_and_Spells.md#object-applystatusifcrit) | Object || 2 ||
| [`ApplyToSource`](Abilities_and_Spells.md#object-applytosource) | Object | An object of effects that are applied to the source of the ability (the caster). | 2 ||
| [`Blind`](./Enums.md) | Integer | The amount of blind stacks applied, or an [stacks, probability] array. | 2 | 1 |
| [`BurgleCoin`](./Enums.md) | Integer | The number of coins stolen from the target, or an array of `[number, probability]`. | 2 | 1 |
| [`Conditional_Adjacent`](Engine_LogicKeys.md#conditional_adjacent) | Object || 2 ||
| [`Conditional_Shielded`](Abilities_and_Spells.md#object-conditional_shielded) | Object || 2 ||
| [`KnockOutCoin`](./Enums.md) | Array / Integer | The number of coins knocked out, with an optional probability or an object with stacks and chance. | 2 | [.5] |
| [`LuckUp`](./Enums.md) | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 2 | 2 |
| [`ManaLeeches`](./Enums.md) | Integer | The number of mana leech stacks applied. | 2 | 1 |
| [`OverrideChainKnockback`](./Enums.md) | Integer | The custom number of tiles for chain knockback, overriding the default. | 2 | 0 |
| [`SpawnBearTrapOnMiss`](./Enums.md) | Integer || 2 | 1 |
| [`BigSplashDamage`](./Enums.md) | Integer || 1 | 2 |
| [`Conditional_HasTag`](Abilities_and_Spells.md#object-conditional_hastag) | Object | Evaluates whether the target has a specific tag; if true, applies the effects within; otherwise, runs the Else block. | 1 ||
| [`Conditional_SourceHasTag`](Engine_LogicKeys.md#conditional_sourcehastag) | Object || 1 ||
| [`Else`](Abilities_and_Spells.md#object-else) | Object | Contains the fallback effects to apply when a preceding conditional check fails. | 1 ||
| [`OverrideChainKnockbackDamage`](./Enums.md) | Integer | A formula string that overrides the damage dealt by chain knockback (e.g., "3+bonus_melee_ability_damage"). | 1 | 0 |
| [`SplashDamage`](./Enums.md) | Integer | The radius (in tiles) for splash damage applied to adjacent targets. | 1 | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1695 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 750 |
| [`Stun`](./Enums.md) | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 98 | [.05*X] |
| [`Burn`](./Enums.md) | Enum / Integer | The amount of Burn applied, either as a fixed number or a formula string. | 85 | 2 |
| [`Bruise`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 79 | 2 |
| [`Poison`](./Enums.md) | Array / Enum / Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 67 | [.5] |
| [`Bleed`](./Enums.md) | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 54 | [.1] |
| [`VisualFXTile`](./Enums.md) | Enum | Specifies the name of the visual effect to play on the target tile. | 34 | IcePoof |
| [`Fear`](./Enums.md) | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 31 | [.15] |
| [`Slow`](./Enums.md) | Enum / Integer | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 29 | 2 |
| [`Immobile`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 24 | 1 |
| [`Weakness`](./Enums.md) | Enum / Integer | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 23 | 2 |
| [`Charmed`](./Enums.md) | Array / Integer | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 22 | [.40] |
| [`Freeze`](./Enums.md) | Array / Integer | The amount of freeze stacks applied, or an [stacks, probability] array. | 19 | [.15] |
| [`Madness`](./Enums.md) | Integer | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 19 | 1 |
| [`Petrify`](./Enums.md) | Array / Integer | The amount of petrify stacks applied, or an [stacks, probability] array. | 15 | [.2] |
| [`Leeches`](./Enums.md) | Integer | The number of stacks of the Leeches debuff applied, which deals damage over time and heals the applier. | 14 | 1 |
| [`Marked`](./Enums.md) | Integer | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. | 9 | 1 |
| [`SpreadDisease`](Abilities_and_Spells.md#object-spreaddisease) | Object | Defines the parameters for spreading a disease, including chance, disease type, and whether it can apply to any target. | 8 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 35 ||
| [`DamageUp`](./Enums.md) | Integer | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 7 | 2 |
| [`HealthGain`](./Enums.md) | Integer / String | The amount of health restored to the source. | 7 | 2*X |
| [`AddMaxHealth`](./Enums.md) | Integer | The amount added to the unit's maximum health. Negative values reduce max health. | 6 | 5 |
| [`AddStatusToBasicAttack`](Abilities_and_Spells.md#object-addstatustobasicattack) | Object | Contains status effects to add to the basic attack. | 4 ||
| [`IncreaseExplosionDamage`](./Enums.md) | Integer || 4 | 2 |
| [`FreePathfindElement`](./Enums.md) | Enum | Specifies a terrain element (e.g., Water, Grass) that the unit can pathfind through without penalty. | 3 | Grass |
| [`tag_filter`](./Enums.md) | Enum || 3 | crow |
| [`AddSpeed`](./Enums.md) | Integer | The amount of speed added (or subtracted) to the unit. | 2 | 4 |
| [`AddStatusToExplosions`](Miscellaneous.md#object-addstatustoexplosions) | Object || 2 ||
| [`EMP`](Miscellaneous.md#object-emp) | Object || 2 ||
| [`FamiliarBonusAbility`](./Enums.md) | Enum || 2 | FamiliarSelfDestruct |
| [`ForceAttack`](./Enums.md) | Integer | If set to 1, forces the target to perform an attack against a random or specified target. | 2 | 1 |
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 2 | 2 |
| [`HolyShieldTransferToSpawner`](./Enums.md) | Integer || 2 | 1 |
| [`IncreaseExplosionSize`](./Enums.md) | Integer || 2 | 2 |
| [`PassiveWhenAffectedByElement`](Cat_Mutations.md#object-passivewhenaffectedbyelement) | Object | An object containing `element` and `passives` that grants the listed passives while the unit is affected by the specified element. | 2 ||
| [`PoisonThorns`](./Enums.md) | Integer | The number of stacks of Poison applied to melee attackers when they hit this unit. | 2 | 2 |
| [`StatusAlliesOnKill`](Miscellaneous.md#object-statusalliesonkill) | Object || 2 ||
| [`StatusOnKill`](Cat_Mutations.md#object-statusonkill) | Object | Specifies status effects or actions triggered when the unit kills an enemy. | 2 ||
| [`WaterWalk`](./Enums.md) | Integer | If greater than 0, allows the unit to traverse water tiles as if they were ground. | 2 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 |
| [`AddUnfilledMaxHealth`](./Enums.md) | Integer || 1 | 20 |
| [`DivineShield`](./Enums.md) | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | 1 |
| [`GrassTileHealing`](./Enums.md) | Integer || 1 | 1 |
| [`Quivered`](./Enums.md) | Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 1 | 2 |
| [`SafeExplosions`](./Enums.md) | Integer || 1 | 1 |
| [`TakeExtraTurn`](./Enums.md) | Integer | The number of extra turns granted to the source. | 1 | 1 |
| [`UncappedHP`](./Enums.md) | Integer | If 1, the unit's maximum HP is not capped by standard limits. | 1 | 1 |

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
| [`object`](./Arrays.md#array-object) | Array / Enum | Specifies the object or unit to be spawned. | 38 ||
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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 38 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 14 |
| [`StrengthUp`](./Enums.md) | Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 4 | 2 |
| [`ConstitutionUp`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 3 | 2 |
| [`DamageUp`](./Enums.md) | Integer | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 3 | 2 |
| [`SpeedUp`](./Enums.md) | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 3 | 2 |
| [`Temporary`](Abilities_and_Spells.md#object-temporary) | Object | Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions. | 3 ||
| [`Thorns`](./Enums.md) | Integer | The amount of thorns damage dealt to attackers on hit. | 3 | 2 |
| [`Conditional_HasStatus`](Abilities_and_Spells.md#object-conditional_hasstatus) | Object || 2 ||
| [`Craft`](Abilities_and_Spells.md#object-craft) | Object | Specifies the loot pool and slot to craft an item for the source. | 2 ||
| [`IntelligenceUp`](./Enums.md) | Integer | The amount of Intelligence added as a flat bonus. | 2 | -1 |
| [`RandomStatUp`](./Enums.md) | Integer | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | 2 |
| [`Shield`](./Enums.md) | Integer / String | The amount of shield granted to the source, absorbing incoming damage. | 2 | 2 |
| [`TempDamageUp`](./Enums.md) | Integer | The amount of temporary damage increase applied. | 2 | 2 |
| [`DiminishingHealthRegen`](./Enums.md) | Integer | The number of diminishing health regen stacks applied. | 1 | 2 |
| [`Else`](Abilities_and_Spells.md#object-else) | Object | Contains the fallback effects to apply when a preceding conditional check fails. | 1 ||
| [`MovementUp`](./Enums.md) | Integer | The amount of movement increase or decrease applied. | 1 | 2 |
| [`RandomInjury`](./Enums.md) | Integer | The number of random injuries applied. | 1 | 1 |
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object | A collection of status effects; one is randomly chosen and applied to the target. | 1 ||
| [`TempMovement`](./Enums.md) | Integer | The amount of temporary movement range added, or a string alias like 'mov'. | 1 | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 55 ||
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object | The name of the ability the source is forced to use, optionally with a chance. | 12 | Hallucinate_Disorder |
| [`NonStackingDivineShield`](./Enums.md) | Integer | The number of Divine Shield stacks that do not stack with duplicates. | 6 | 1 |
| [`SpeedUp`](./Enums.md) | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 5 | 2 |
| [`EmptyMana`](./Enums.md) | Integer || 2 | 1 |
| [`IntelligenceUp`](./Enums.md) | Integer | The amount of Intelligence added as a flat bonus. | 2 | -1 |
| [`RangeUp`](./Enums.md) | Integer | The number of stacks of bonus attack range applied. | 2 | 1 |
| [`KineticSpikes`](./Enums.md) | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 1 | 2 |
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 1 | Coin |
| [`PermanentMadness`](./Enums.md) | Integer | The number of permanent madness stacks applied. | 1 | 1 |
| [`StrengthUp`](./Enums.md) | Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 1 | 2 |
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
| [`slot`](./Enums.md#enum-slot) | Enum / Integer | Specifies the equipment slot (e.g., 'head', 'trinket', 'random_empty') where the crafted item is placed. | 16 ||
| `frame` | Integer | The sprite frame index to display. | 3 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 52 ||
| `even_if_dead` | Boolean | If true, the effect triggers even if the unit is dead. | 25 ||
| [`RandomMutation`](./Enums.md) | Integer | The number of random mutations to apply. | 9 | 1 |
| [`FindItemFromPool`](Abilities_and_Spells.md#object-finditemfrompool) | Enum / Object | Specifies the loot pool from which to find an item, with an optional chance. | 8 | consumables |
| [`RandomPermanentStat`](./Enums.md) | Integer | The amount of a random permanent stat change (positive or negative). | 8 | 3 |
| [`CureDisease`](Engine_StatusAndPassiveKeys.md#object-curedisease) | Object || 6 ||
| [`PermanentIntelligence`](./Enums.md) | Integer | The permanent amount of intelligence added or removed. | 3 | -1 |
| [`NextBattleStatus`](Engine_StatusAndPassiveKeys.md#object-nextbattlestatus) | Object || 2 ||
| [`PermanentConstitution`](./Enums.md) | Integer | The amount of permanent Constitution stat added or removed. | 2 | -1 |
| [`PermanentSpeed`](./Enums.md) | Integer | The permanent amount of speed added or removed. | 2 | -1 |
| [`PermanentStrength`](./Enums.md) | Integer | The amount of permanent bonus strength (physical damage modifier) granted. | 1 | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 34 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 6 |
| [`HealthGain`](./Enums.md) | Integer / String | The amount of health restored to the source. | 5 | 2*X |
| [`EquipPermanentItem`](./Enums.md) | Enum | The name of the item to permanently equip to the source. | 3 | BoneClub |
| [`StrengthUp`](./Enums.md) | Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 3 | 2 |
| [`AllStatsUp`](./Enums.md) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | [.5] |
| [`Conditional_FirstApplicationThisTurn`](Abilities_and_Spells.md#object-conditional_firstapplicationthisturn) | Object || 2 ||
| [`DamageUp`](./Enums.md) | Integer | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 2 | 2 |
| [`LuckUp`](./Enums.md) | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 2 | 2 |
| [`RefreshActPoints`](./Enums.md) | Integer | The amount of action points restored to the source. | 2 | 1 |
| [`RefreshMovePoints`](./Enums.md) | Integer | The amount of movement points restored to the source. | 2 | 1 |
| [`SpeedUp`](./Enums.md) | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 2 | 2 |
| [`RandomStatUp`](./Enums.md) | Integer | The amount of random stat increase applied, either as a fixed number or a formula string. | 1 | 2 |
| [`Stealth`](./Enums.md) | Integer | The number of stealth stacks applied. | 1 | 1 |
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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 14 ||
| [`RandomMagicMissile`](./Enums.md) | Integer | The number of random magic missiles fired, or an object defining its properties. | 6 | 2 |
| `NextBasicAttackCritsThisTurn` | `Number` | An object or number configuring the next basic attack to be a critical hit this turn. An object may contain stack, cant_miss, or piercing sub-keys. | 2 ||
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object | The name of the ability the source is forced to use, optionally with a chance. | 2 | Hallucinate_Disorder |
| [`RandomStatUp`](./Enums.md) | Integer | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | 2 |
| [`Shield`](./Enums.md) | Integer / String | The amount of shield granted to the source, absorbing incoming damage. | 2 | 2 |
| [`PartialCleanse`](./Enums.md) | Integer | The number of stacks of temporary status effects to remove from the target. | 1 | 1 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 ||

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
| [`disease`](./Enums.md#enum-disease) | Enum | Determines which disease is applied when spreading disease. | 13 ||
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 12 ||
| `can_apply_to_anything` | Boolean | If true, this disease can be spread to any unit, regardless of type. | 6 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 24 ||
| [`Conditional_BadRoll`](Abilities_and_Spells.md#object-conditional_badroll) | Object | An object containing an `odds` value and effects that are applied when a random roll succeeds. | 5 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 |
| [`FillMana`](./Enums.md) | Array / Integer | The amount of mana restored, or an [amount, probability] array. | 2 | [.25] |
| [`IntelligenceUp`](./Enums.md) | Integer | The amount of Intelligence added as a flat bonus. | 2 | -1 |
| [`RandomStatUp`](./Enums.md) | Integer | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | 2 |
| [`Conditional_GoodRoll`](Abilities_and_Spells.md#object-conditional_goodroll) | Object | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 1 ||
| [`Fear`](./Enums.md) | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 1 | [.15] |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object | The name of the ability the source is forced to use, optionally with a chance. | 1 | Hallucinate_Disorder |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 28 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 8 ||
| [`DamageUp`](./Enums.md) | Integer | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 5 | 2 |
| [`AllStatsUp`](./Enums.md) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 4 | [.5] |
| `Cleanse` | `Number` | The number of stacks of negative status effects removed from the target. | 3 ||
| [`ApplyToSource`](Abilities_and_Spells.md#object-applytosource) | Object | An object of effects that are applied to the source of the ability (the caster). | 2 ||
| `ClearNegativeEffects` | `Number` | The number of negative effects cleared from the target. | 2 ||
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object | A collection of status effects; one is randomly chosen and applied to the target. | 2 ||
| [`Shield`](./Enums.md) | Integer / String | The amount of shield granted to the source, absorbing incoming damage. | 2 | 2 |
| [`TempSpeedUp`](./Enums.md) | Integer | The number of stacks of temporary Speed Up applied to the unit. | 2 | 10 |
| [`SpeedUp`](./Enums.md) | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 1 | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 12 ||
| [`Stun`](./Enums.md) | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 3 | [.05*X] |
| [`Weakness`](./Enums.md) | Enum / Integer | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 3 | 2 |
| [`Conditional_HasStatus`](Abilities_and_Spells.md#object-conditional_hasstatus) | Object || 2 ||
| [`Else`](Abilities_and_Spells.md#object-else) | Object | Contains the fallback effects to apply when a preceding conditional check fails. | 2 ||
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 2 | Coin |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 |
| [`Bleed`](./Enums.md) | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 1 | [.1] |
| [`Bruise`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 1 | 2 |
| [`Confusion`](./Enums.md) | Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 1 | 2 |
| [`Immobile`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 1 | 1 |

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
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 57 ||
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 56 ||
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 52 ||
| `expires_on_begin_turn` | Boolean | If true, the temporary effect expires at the start of the target's turn. | 25 ||
| `expires_on_end_turn` | Boolean | If true, the temporary effect expires at the end of the target's turn. | 21 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 13 ||
| [`mode`](./Enums.md#enum-mode) | Enum | Specifies the comparison mode (equal, greater, less_or_equal, etc.) used for a conditional check. | 13 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 13 ||
| [`threshold`](Items_and_Equipment.md#object-threshold) | Integer / Object | The health threshold value, either as a formula using X (max health) or a fixed integer. | 13 | 7 |

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
| `cha` | Enum / Integer | The Charisma stat value or modifier. | 2 ||
| `spd` | Enum / Integer | The Speed stat value or modifier. | 2 ||

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
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 31 ||
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. | 29 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 29 |
| `knockback` | Enum / Integer | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 3 ||

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
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 70 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 49 |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. | 47 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 43 ||
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Specifies the amount of damage dealt, can be a number or expression. | 22 ||
| [`elements`](./Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 10 ||
| [`Poison`](./Enums.md) | Array / Enum / Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 1 | [.5] |
| [`SpreadDisease`](Abilities_and_Spells.md#object-spreaddisease) | Object | Defines the parameters for spreading a disease, including chance, disease type, and whether it can apply to any target. | 1 ||
| [`Weakness`](./Enums.md) | Enum / Integer | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 1 | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 8 ||
| [`AddSpellDamage`](./Enums.md) | Integer || 2 | 2 |
| [`CounterAttack`](./Enums.md) | Enum | Specifies the ability used when the unit counterattacks after being hit. | 2 | ReflexPunchJab |
| [`ExtraMovePoints`](./Enums.md) | Integer | The number of additional movement points granted to this unit. | 2 | 1 |
| [`ManaCostReduction`](./Enums.md) | Integer | The amount or percentage by which ability mana costs are reduced for this unit. | 2 | 2 |
| [`StatusOnStanceSwitch`](Miscellaneous.md#object-statusonstanceswitch) | Object || 2 ||
| [`CritsApplyStatus`](Items_and_Equipment.md#object-critsapplystatus) | Object || 1 ||
| [`Flying`](./Enums.md) | Integer | If set to 1, grants the unit the Flying passive, allowing movement over obstacles and ignoring terrain penalties. | 1 | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 33 ||
| [`Shield`](./Enums.md) | Integer / String | The amount of shield granted to the source, absorbing incoming damage. | 12 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 12 |
| [`Thorns`](./Enums.md) | Integer | The amount of thorns damage dealt to attackers on hit. | 10 | 2 |
| [`DivineShield`](./Enums.md) | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 9 | 1 |
| [`KineticSpikes`](./Enums.md) | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 9 | 2 |
| [`Poison`](./Enums.md) | Array / Enum / Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 9 | [.5] |
| [`Bleed`](./Enums.md) | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 8 | [.1] |
| [`Charge`](./Enums.md) | Integer | The number of charge stacks applied. | 8 | 2 |
| [`Weakness`](./Enums.md) | Enum / Integer | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 8 | 2 |
| [`Slow`](./Enums.md) | Enum / Integer | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 7 | 2 |
| [`Blind`](./Enums.md) | Integer | The amount of blind stacks applied, or an [stacks, probability] array. | 6 | 1 |
| [`Brace`](./Enums.md) | Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 6 | 2 |
| [`Bruise`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 6 | 2 |
| [`DiminishingHealthRegen`](./Enums.md) | Integer | The number of diminishing health regen stacks applied. | 6 | 2 |
| [`AllStatsUp`](./Enums.md) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 5 | [.5] |
| [`Burn`](./Enums.md) | Enum / Integer | The amount of Burn applied, either as a fixed number or a formula string. | 5 | 2 |
| [`MoveQuivered`](./Enums.md) | Integer | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 5 | 2 |
| [`Quivered`](./Enums.md) | Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 5 | 2 |
| [`BleedThorns`](./Enums.md) | Integer | The amount of bleed thorns damage dealt to attackers on hit. | 4 | 2 |
| [`ConstitutionUp`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 4 | 2 |
| [`Madness`](./Enums.md) | Integer | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 4 | 1 |
| [`MagicWeakness`](./Enums.md) | Integer | The amount of magic weakness stacks applied, or an [stacks, probability] array. | 4 | 2 |
| [`Marked`](./Enums.md) | Integer | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. | 4 | 1 |
| [`Reflect`](./Enums.md) | Integer | The amount of reflect stacks applied. | 4 | 1 |
| [`SpeedUp`](./Enums.md) | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 4 | 2 |
| [`Stun`](./Enums.md) | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 4 | [.05*X] |
| [`Tarred`](./Enums.md) | Integer | The amount of tarred stacks applied, or an [stacks, probability] array. | 4 | 1 |
| [`Charmed`](./Enums.md) | Array / Integer | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 3 | [.40] |
| [`Confusion`](./Enums.md) | Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 3 | 2 |
| [`Fear`](./Enums.md) | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 3 | [.15] |
| [`Freeze`](./Enums.md) | Array / Integer | The amount of freeze stacks applied, or an [stacks, probability] array. | 3 | [.15] |
| [`Immobile`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 3 | 1 |
| [`Petrify`](./Enums.md) | Array / Integer | The amount of petrify stacks applied, or an [stacks, probability] array. | 3 | [.2] |
| [`Sleep`](./Enums.md) | Integer | The amount of sleep stacks applied, or an [stacks, probability] array. | 3 | 1 |
| [`StatusGroup`](Abilities_and_Spells.md#object-statusgroup) | Object | A container grouping multiple status effects to be applied simultaneously. | 3 ||
| [`StrengthUp`](./Enums.md) | Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 3 | 2 |
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 1 | Coin |
| [`SpawnCoinAnywhere`](./Enums.md) | Integer | The number of coins to spawn. If an array, the second value is the probability of spawning them anywhere. | 1 | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 8 ||
| [`LuckUp`](./Enums.md) | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 3 | 2 |
| [`DamageUp`](./Enums.md) | Integer | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 2 | 2 |
| [`Shield`](./Enums.md) | Integer / String | The amount of shield granted to the source, absorbing incoming damage. | 2 | 2 |
| [`CritChanceUp`](./Enums.md) | Integer | The amount of critical hit chance added as a flat percentage. | 1 | 80 |
| [`RandomStatUp`](./Enums.md) | Integer | The amount of random stat increase applied, either as a fixed number or a formula string. | 1 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 34 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 12 |
| [`Confusion`](./Enums.md) | Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 9 | 2 |
| [`Conditional_PartyMember`](Engine_LogicKeys.md#conditional_partymember) | Object || 2 ||
| [`Else`](Abilities_and_Spells.md#object-else) | Object | Contains the fallback effects to apply when a preceding conditional check fails. | 2 ||
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object | A collection of status effects; one is randomly chosen and applied to the target. | 2 ||
| [`Stun`](./Enums.md) | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 2 | [.05*X] |

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
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Specifies the amount of damage dealt, can be a number or expression. | 7 ||
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 7 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 7 ||
| `cant_miss` | `Boolean` | If true, the damage instance always hits its target regardless of accuracy or evasion. | 6 ||
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. | 6 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 6 |
| `knockback` | Enum / Integer | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 5 ||
| [`chance`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A probability (decimal or percentage) for a form change or other effect to occur. | 3 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 7 ||
| [`AddCritMultiplier`](./Enums.md) | Integer || 2 | 200 |
| [`CritChanceUp`](./Enums.md) | Integer | The amount of critical hit chance added as a flat percentage. | 2 | 80 |
| [`DodgeChance`](./Enums.md) | Integer | The percentage chance the unit has to dodge incoming attacks. | 2 | 50 |
| [`StatusOnStanceSwitch`](Miscellaneous.md#object-statusonstanceswitch) | Object || 2 ||
| [`KineticSpikes`](./Enums.md) | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 1 | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 7 ||
| [`AddCritMultiplier`](./Enums.md) | Integer || 2 | 200 |
| [`CritChanceUp`](./Enums.md) | Integer | The amount of critical hit chance added as a flat percentage. | 2 | 80 |
| [`DodgeChance`](./Enums.md) | Integer | The percentage chance the unit has to dodge incoming attacks. | 2 | 50 |
| [`StatusOnStanceSwitch`](Miscellaneous.md#object-statusonstanceswitch) | Object || 2 ||
| [`KineticSpikes`](./Enums.md) | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 1 | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 7 ||
| [`AddCritMultiplier`](./Enums.md) | Integer || 2 | 200 |
| [`CritChanceUp`](./Enums.md) | Integer | The amount of critical hit chance added as a flat percentage. | 2 | 80 |
| [`DodgeChance`](./Enums.md) | Integer | The percentage chance the unit has to dodge incoming attacks. | 2 | 50 |
| [`StatusOnStanceSwitch`](Miscellaneous.md#object-statusonstanceswitch) | Object || 2 ||
| [`KineticSpikes`](./Enums.md) | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 1 | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 8 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 |
| `triggers_limit` | Number || 2 ||
| [`AllStatsUp`](./Enums.md) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | [.5] |
| [`HealAndOverhealToShield`](./Enums.md) | Integer || 2 | 12 |
| [`Reanimate`](./Enums.md) | Integer | The percentage chance to reanimate the target. | 2 | 33 |
| [`TakeExtraTurn`](./Enums.md) | Integer | The number of extra turns granted to the source. | 2 | 1 |
| [`Freeze`](./Enums.md) | Array / Integer | The amount of freeze stacks applied, or an [stacks, probability] array. | 1 | [.15] |
| [`FullHeal`](./Enums.md) | Integer | If non-zero, fully restores the target's health. | 1 | 1 |

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
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specifies the tag(s) to check on the target, used in conditional effects. | 7 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 7 ||
| [`RefreshActPoints`](./Enums.md) | Integer | The amount of action points restored to the source. | 3 | 1 |
| `exclude_basicattack` | Boolean || 2 ||
| [`Conditional_FirstApplicationThisTurn`](Abilities_and_Spells.md#object-conditional_firstapplicationthisturn) | Object || 2 ||
| [`DamageUp`](./Enums.md) | Integer | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 2 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 |
| [`HealthGain`](./Enums.md) | Integer / String | The amount of health restored to the source. | 1 | 2*X |
| [`RandomStatUp`](./Enums.md) | Integer | The amount of random stat increase applied, either as a fixed number or a formula string. | 1 | 2 |

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
| [`element`](./Enums.md#enum-element) | Array / Enum | Specifies which element(s) the conditional checks against. | 6 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 6 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 6 |
| [`ChangeTile`](Abilities_and_Spells.md#object-changetile) | Enum / Object | Specifies the tile type to change to, or an object defining tile change parameters (tile type and area of effect). | 2 | FloatingGlassTile |
| [`Conditional_Ally`](Abilities_and_Spells.md#object-conditional_ally) | Object || 2 ||
| [`Conditional_Enemy`](Abilities_and_Spells.md#object-conditional_enemy) | Object || 2 ||
| [`Bleed`](./Enums.md) | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 1 | [.1] |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 5 ||
| [`Bleed`](./Enums.md) | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 3 | [.1] |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 |
| [`PullSourceToKnockbackImmuneTarget`](./Enums.md) | Integer | The amount of pull force applied to the source toward a knockback-immune target. | 2 | 1 |
| [`Cleave`](./Enums.md) | Integer | The number of additional targets hit; if an object, contains a chance parameter for each cleave attempt. | 1 | 1 |
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
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 6 ||
| [`disease`](./Enums.md#enum-disease) | Enum | Determines which disease is applied when spreading disease. | 6 ||
| `can_apply_to_anything` | Boolean | If true, this disease can be spread to any unit, regardless of type. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 66 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 23 ||
| `CaptureFamiliar` | `Number` | The number of times to attempt to capture the target as a familiar. | 2 ||
| `FactionConversion` | `Number` | Converts the target to the caster's faction. | 2 ||
| [`Fear`](./Enums.md) | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 2 | [.15] |
| [`Marked`](./Enums.md) | Integer | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. | 2 | 1 |
| [`PermanentCharm`](./Enums.md) | Integer | If non-zero, permanently charms the target, converting it to the caster's faction permanently. | 2 | 1 |
| [`TempSpeedUp`](./Enums.md) | Integer | The number of stacks of temporary Speed Up applied to the unit. | 1 | 10 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 16 ||
| [`Weakness`](./Enums.md) | Enum / Integer | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 1 | 2 |

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
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specifies the tag(s) to check on the target, used in conditional effects. | 6 ||

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
| [`object`](./Arrays.md#array-object) | Array / Enum | Specifies the object or unit to be spawned. | 22 ||
| [`chance`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A probability (decimal or percentage) for a form change or other effect to occur. | 20 ||
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 ||
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
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the object or unit to be spawned. | 38 ||
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 20 ||
| `spawn_on_death_hit` | Boolean | If true, spawning only occurs when the damage is lethal. | 10 ||
| `consider_all_layers` | Boolean | If true, considers all map layers when determining the spawn location. | 2 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 9 ||
| [`Confusion`](./Enums.md) | Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 3 | 2 |
| [`Bruise`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 2 | 2 |
| [`FaceAway`](./Enums.md) | Integer | If set, forces the target to face away from the source. | 2 | 1 |
| [`Stun`](./Enums.md) | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 2 | [.05*X] |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 |
| [`SpreadDisease`](Abilities_and_Spells.md#object-spreaddisease) | Object | Defines the parameters for spreading a disease, including chance, disease type, and whether it can apply to any target. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 8 ||
| [`Charge`](./Enums.md) | Integer | The number of charge stacks applied. | 4 | 2 |
| [`CurrentWeaponDamageUp`](./Enums.md) | Integer || 2 | 1 |
| [`HealthGain`](./Enums.md) | Integer / String | The amount of health restored to the source. | 1 | 2*X |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 |

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
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 |
| [`ForceUseAbility_NonStack`](./Enums.md) | Enum || 2 | Indigestion_Fart2 |
| [`StrengthUp`](./Enums.md) | Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 2 | 2 |
| `SpawnScaledRotFly` | Number | The number of scaled Rot Flies to spawn when over-healed. | 1 ||
| [`CurrentWeaponDamageUp`](./Enums.md) | Integer || 1 | 1 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 ||

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
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Specifies the amount of damage dealt, can be a number or expression. | 9 ||
| [`element`](./Enums.md#enum-element) | Array / Enum | Specifies which element(s) the conditional checks against. | 9 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 5 ||
| [`AddStatusToBasicAttack`](Abilities_and_Spells.md#object-addstatustobasicattack) | Object | Contains status effects to add to the basic attack. | 3 ||
| [`AddMaxHealth`](./Enums.md) | Integer | The amount added to the unit's maximum health. Negative values reduce max health. | 2 | 5 |
| [`AddSpeed`](./Enums.md) | Integer | The amount of speed added (or subtracted) to the unit. | 2 | 4 |
| [`DamageUp`](./Enums.md) | Integer | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 2 | 2 |

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
| [`element`](./Enums.md#enum-element) | Array / Enum | Specifies which element(s) the conditional checks against. | 6 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 6 ||
| [`Burn`](./Enums.md) | Enum / Integer | The amount of Burn applied, either as a fixed number or a formula string. | 3 | 2 |
| [`Conditional_Corpse`](Abilities_and_Spells.md#object-conditional_corpse) | Object || 2 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 |

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
| [`AddElement`](./Enums.md#enum-addelement) | Enum | Specifies the element to add to explosions. | 4 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 ||
| [`Burn`](./Enums.md) | Enum / Integer | The amount of Burn applied, either as a fixed number or a formula string. | 4 | 2 |

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 ||
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
| [`range`](./Enums.md#enum-range) | Enum / Integer | The distance in tiles for the trigger effect; `global` means any distance. | 4 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 4 ||

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
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 3 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 9 ||
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 6 ||
| `force_display_name` | Boolean | If true, forces the display name to show for the ability. | 2 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 8 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 |
| [`TakeExtraTurn`](./Enums.md) | Integer | The number of extra turns granted to the source. | 2 | 1 |
| [`AllStatsUp`](./Enums.md) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | [.5] |
| [`FillMana`](./Enums.md) | Array / Integer | The amount of mana restored, or an [amount, probability] array. | 1 | [.25] |
| [`ManaGain`](./Enums.md) | Integer | The amount of mana restored to the source, which can be an expression. | 1 | 2 |

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
| `min_range` | Integer | The minimum range of the ability. | 4 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 4 ||

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
| `cha` | Enum / Integer | The Charisma stat value or modifier. | 1 ||
| `int` | Enum / Integer || 1 ||
| `spd` | Enum / Integer | The Speed stat value or modifier. | 1 ||

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
| [`mode`](./Enums.md#enum-mode) | Enum | Specifies the comparison mode (equal, greater, less_or_equal, etc.) used for a conditional check. | 9 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 9 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 9 ||
| [`threshold`](Items_and_Equipment.md#object-threshold) | Integer / Object | The health threshold value, either as a formula using X (max health) or a fixed integer. | 9 | 7 |

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
| [`element`](./Enums.md#enum-element) | Array / Enum | Specifies which element(s) the conditional checks against. | 18 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 18 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 18 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 5 ||
| [`AddStatusToBasicAttack`](Abilities_and_Spells.md#object-addstatustobasicattack) | Object | Contains status effects to add to the basic attack. | 2 ||
| [`Brace`](./Enums.md) | Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 2 | 2 |
| [`Flying`](./Enums.md) | Integer | If set to 1, grants the unit the Flying passive, allowing movement over obstacles and ignoring terrain penalties. | 2 | 1 |
| [`AddMovement`](./Enums.md) | Integer | The amount of bonus movement points added to the unit's base movement. | 1 | 20 |
| [`ReplaceBasicMove`](./Enums.md) | Enum | Specifies an alternative movement ability that replaces the unit's default move. | 1 | ToadJump_BasicMove |

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
| `palette` | Enum / Integer | Specifies the color palette index for the ability's visuals. | 4 ||
| [`particle`](./Enums.md#enum-particle) | Enum | Specifies the particle effect displayed. | 4 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 ||
| [`AllStatsUp`](./Enums.md) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | [.5] |
| [`DamageUp`](./Enums.md) | Integer | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 2 | 2 |
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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 8 ||
| [`HealthGain`](./Enums.md) | Integer / String | The amount of health restored to the source. | 4 | 2*X |
| [`ManaGain`](./Enums.md) | Integer | The amount of mana restored to the source, which can be an expression. | 2 | 2 |
| [`MoveQuivered`](./Enums.md) | Integer | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 2 | 2 |
| [`Brace`](./Enums.md) | Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 1 | 2 |
| [`ConstitutionUp`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 1 | 2 |
| [`Shield`](./Enums.md) | Integer / String | The amount of shield granted to the source, absorbing incoming damage. | 1 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 |

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
| `spells` | Array | The list of spell ability IDs the unit possesses. | 5 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 5 ||
| [`DoubleCastSpell`](./Enums.md) | Integer | The number of times the next spell cast is doubled, or a template with name and tooltip. | 3 | 2 |
| [`Quivered`](./Enums.md) | Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 2 | 2 |
| [`MoveQuivered`](./Enums.md) | Integer | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 1 | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 ||
| [`FreeSpell`](./Enums.md) | Integer | The number of stacks of Free Spell applied to the source, allowing the next spells to be cast without mana cost. | 2 | 1 |
| [`Quivered`](./Enums.md) | Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 2 | 2 |
| [`MoveQuivered`](./Enums.md) | Integer | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 1 | 2 |
| [`SpellDamageUp`](./Enums.md) | Integer | The number of stacks of SpellDamageUp applied, increasing spell damage. | 1 | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 ||
| [`IntelligenceUp`](./Enums.md) | Integer | The amount of Intelligence added as a flat bonus. | 2 | -1 |
| [`Shield`](./Enums.md) | Integer / String | The amount of shield granted to the source, absorbing incoming damage. | 2 | 2 |
| [`SpellDamageUp`](./Enums.md) | Integer | The number of stacks of SpellDamageUp applied, increasing spell damage. | 2 | 1 |
| [`Temporary`](Abilities_and_Spells.md#object-temporary) | Object | Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions. | 2 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 |
| [`DivineShield`](./Enums.md) | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | 1 |
| [`HealthGain`](./Enums.md) | Integer / String | The amount of health restored to the source. | 1 | 2*X |
| [`KineticSpikes`](./Enums.md) | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 1 | 2 |

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 10 ||
| `ability_damage_only` | Boolean | If true, the reaction only triggers on ability damage, not basic attacks. | 7 ||
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 11 ||
| [`RandomMagicMissile`](./Enums.md) | Integer | The number of random magic missiles fired, or an object defining its properties. | 7 | 2 |

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
| `Fury` | Integer | The amount of Fury (bonus damage or charges) gained. | 4 ||
| `CastAgain` | Integer / String | The number of additional times the ability can be cast this turn. | 2 ||

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
| [`odds`](./Enums.md#enum-odds) | Number | The probability of the effect occurring, expressed as a decimal or percentage. | 8 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 8 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 8 |
| [`Temporary`](Abilities_and_Spells.md#object-temporary) | Object | Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions. | 5 ||

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
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 20 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 20 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 4 | |

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 13 ||
| `pop_corpse` | Boolean | If true, the corpse is destroyed instead of left behind on death. | 11 ||

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
| [`element`](./Arrays.md#array-element) | Array / Enum | Specifies which element(s) the conditional checks against. | 5 ||

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
| [`chance`](./Enums.md#enum-chance) | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 3 ||
| [`pool`](./Enums.md#enum-pool) | Array / Enum | Specifies the name of the pool from which an ability is learned or an item is crafted. | 2 ||

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
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | Specifies the movement ability (e.g., BirdFly, TrampleMoveOne) used for the movement action. | 5 ||
| `move_far` | Boolean | If true, the unit moves the maximum distance towards the damage source. | 4 ||

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
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the object or unit to be spawned. | 7 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 5 ||

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
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the object or unit to be spawned. | 4 ||
| [`prevent_chain_tag`](./Enums.md#enum-prevent_chain_tag) | Enum | A tag that prevents chaining of spawns from the same source. | 4 ||

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
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the object or unit to be spawned. | 11 ||
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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 12 ||
| [`AllStatsUp`](./Enums.md) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 4 | [.5] |
| [`FindItemFromPool`](Abilities_and_Spells.md#object-finditemfrompool) | Enum / Object | Specifies the loot pool from which to find an item, with an optional chance. | 2 | consumables |
| [`PermanentDexterity`](./Enums.md) | Integer | The permanent amount of dexterity added or removed. | 2 | 1 |
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
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 8 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 8 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 |
| [`AllStatsUp`](./Enums.md) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | [.5] |
| [`SpellDamageUp`](./Enums.md) | Integer | The number of stacks of SpellDamageUp applied, increasing spell damage. | 2 | 1 |
| [`ReduceManaCost`](./Enums.md) | Integer | The number of stacks reducing mana cost of abilities. | 1 | 1 |
| [`RepairWeapon`](./Enums.md) | Integer | The number of weapon durability points restored; an array [stacks, probability] applies a chance-based repair. | 1 | 1 |
| [`RepairWeaponCondition`](./Enums.md) | Integer | The amount of weapon condition restored. | 1 | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 6 ||
| [`LuckUp`](./Enums.md) | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 2 | 2 |
| [`SpeedUp`](./Enums.md) | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 2 | 2 |
| [`DexterityUp`](./Enums.md) | Integer | The amount of dexterity change, or a keyword like 'item_aux'. | 1 | 2 |
| [`SpawnCoinAnywhere`](./Enums.md) | Integer | The number of coins to spawn. If an array, the second value is the probability of spawning them anywhere. | 1 | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 6 ||
| [`AllStatsUp`](./Enums.md) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | [.5] |
| [`FillMana`](./Enums.md) | Array / Integer | The amount of mana restored, or an [amount, probability] array. | 1 | [.25] |
| [`HealthGain`](./Enums.md) | Integer / String | The amount of health restored to the source. | 1 | 2*X |
| [`PercentHeal`](./Enums.md) | Integer || 1 | 50 |
| [`TakeExtraTurn`](./Enums.md) | Integer | The number of extra turns granted to the source. | 1 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 9 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 7 |
| [`FullHeal`](./Enums.md) | Integer | If non-zero, fully restores the target's health. | 2 | 1 |
| [`Sleep`](./Enums.md) | Integer | The amount of sleep stacks applied, or an [stacks, probability] array. | 1 | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 5 ||
| [`StrengthUp`](./Enums.md) | Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 2 | 2 |
| [`Cleanse`](./Enums.md) | Integer | The number of stacks of negative status effects removed from the target. | 1 | 0 |
| [`IntelligenceUp`](./Enums.md) | Integer | The amount of Intelligence added as a flat bonus. | 1 | -1 |
| [`RandomStatUp`](./Enums.md) | Integer | The amount of random stat increase applied, either as a fixed number or a formula string. | 1 | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 5 ||
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object | A collection of status effects; one is randomly chosen and applied to the target. | 2 ||
| [`DivineShield`](./Enums.md) | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 ||
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 1 | Coin |
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object | A collection of status effects; one is randomly chosen and applied to the target. | 1 ||
| [`Thorns`](./Enums.md) | Integer | The amount of thorns damage dealt to attackers on hit. | 1 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 11 ||
| [`DivineShield`](./Enums.md) | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 2 | 1 |
| [`ManaGain`](./Enums.md) | Integer | The amount of mana restored to the source, which can be an expression. | 2 | 2 |
| [`HealthGain`](./Enums.md) | Integer / String | The amount of health restored to the source. | 1 | 2*X |
| [`RefreshMovePoints`](./Enums.md) | Integer | The amount of movement points restored to the source. | 1 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 8 ||
| [`DiminishingHealthRegen`](./Enums.md) | Integer | The number of diminishing health regen stacks applied. | 2 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 |
| [`Shield`](./Enums.md) | Integer / String | The amount of shield granted to the source, absorbing incoming damage. | 1 | 2 |

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 5 ||
| [`range`](./Engine_Uncategorized_Resources.md#valid-property-keys) | Variable | The distance in tiles for the trigger effect; `global` means any distance. | 5 ||
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specifies the tag(s) to check on the target, used in conditional effects. | 5 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`DamageUp`](./Enums.md) | Integer | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 2 | 2 |
| [`Doomed`](./Enums.md) | Integer | The number of stacks of Doomed applied, causing the target to die after a set number of turns. | 2 | 3 |
| [`MovementUp`](./Enums.md) | Integer | The amount of movement increase or decrease applied. | 2 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 |

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
| `AddFilledMaxHealth` | Number | The amount of filled max health added to spawned rocks. | 2 ||
| `JoinSpawnerFaction` | Number | The faction ID that spawned rocks should join. | 2 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`Bleed`](./Enums.md) | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 1 | [.1] |
| [`Piercing`](./Enums.md) | Integer || 1 | 1 |
| [`Weakness`](./Enums.md) | Enum / Integer | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 1 | 2 |

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
| `CharmedForceAttack` | `Number` | If non-zero, forces the charmed target to use its basic attack on a random nearby unit. | 2 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 ||

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
| [`DelayedWind`](Engine_StatusAndPassiveKeys.md#object-delayedwind) | Object | Defines the properties for a delayed wind effect applied on melee damage. | 1 ||
| [`DelayedWindCone`](Abilities_and_Spells.md#object-delayedwindcone) | Object || 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 |

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
| [`range`](./Enums.md#enum-range) | Enum / Integer | The distance in tiles for the trigger effect; `global` means any distance. | 2 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 ||
| [`Bounty`](./Enums.md) | Integer | The number of bounty stacks applied to enemies, increasing rewards on defeat. | 3 | 3 |
| `count` | Array / Integer | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 2 ||

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
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 8 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 ||
| [`Purge`](./Enums.md) | Integer | The number of status effects to purge from the target. | 2 | 0 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 43 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 20 |
| [`AllStatsUp`](./Enums.md) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 6 | [.5] |
| [`Shield`](./Enums.md) | Integer / String | The amount of shield granted to the source, absorbing incoming damage. | 5 | 2 |

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 ||
| `advantage_polarity` | Number || 1 ||
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 1 ||

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
| [`crit_chance`](./Engine_DamagingKeys.md#valid-property-keys) | `String` | The chance for the damage instance to critically hit, expressed as a percentage or equation; values above 1 default to 100%. | 4 ||
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Specifies the amount of damage dealt, can be a number or expression. | 4 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 4 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 ||
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 2 ||

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
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 5 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 5 ||
| [`Quivered`](./Enums.md) | Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 5 | 2 |
| [`AllStatsUp`](./Enums.md) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | [.5] |

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 6 ||
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 6 ||

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
| [`tile`](./Enums.md#enum-tile) | Array / Enum | Specifies the tile type(s) to change to, either a single tile string or an array of tiles. | 12 ||
| `aoe` | Integer | The radius (in tiles) of the area affected by the tile change. | 2 ||

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
| [`class`](./Enums.md#enum-class) | Enum | Specifies the class that this ability belongs to, used for categorization and restrictions. | 6 ||

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
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 ||
| [`Bleed`](./Enums.md) | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 2 | [.1] |
| [`BonusCritChance`](./Enums.md) | Integer | The flat percentage increase to critical hit chance. | 2 | 50 |
| [`BonusDamage`](./Enums.md) | Integer | The amount of flat bonus damage added (negative values reduce damage). | 2 | 2 |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 19 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 6 |
| [`Stun`](./Enums.md) | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 3 | [.05*X] |
| [`Charmed`](./Enums.md) | Array / Integer | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 2 | [.40] |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 10 ||
| `Revive` | `Number` | Revives a dead target with the specified percentage of health (e.g., "50%", "100%") or a fixed number. | 7 ||
| `OverrideDamage` | `Number` | Overrides the damage of the current action to this flat value (can be negative to heal). | 2 ||
| `TakeExtraTurn` | `Number` | The number of extra turns granted to the source. | 2 ||
| [`Charmed`](./Enums.md) | Array / Integer | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 2 | [.40] |
| [`SafeDoomed`](./Enums.md) | Integer | The number of SafeDoomed stacks applied, or 'level' to scale with character level. | 2 | 1 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 ||
| [`DamageUp`](./Enums.md) | Integer | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 1 | 2 |
| [`SpeedUp`](./Enums.md) | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 1 | 2 |

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
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specifies the tag(s) to check on the target, used in conditional effects. | 46 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 46 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 11 ||
| `FlatLeechIfDamaged` | `Number` | The flat amount of health leeched when the unit takes damage. | 1 ||
| [`Charmed`](./Enums.md) | Array / Integer | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 1 | [.40] |

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
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 | |

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
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 | |

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
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 5 |
| `BonusCritChance` | `Number` | The flat percentage increase to critical hit chance. | 2 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 ||

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
| [`pool`](./Enums.md#enum-pool) | Array / Enum | Specifies the name of the pool from which an ability is learned or an item is crafted. | 15 ||
| [`slot`](./Enums.md#enum-slot) | Enum / Integer | Specifies the equipment slot (e.g., 'head', 'trinket', 'random_empty') where the crafted item is placed. | 14 ||

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
| [`damage`](./Math_Equations.md) | Equation | Specifies the amount of damage dealt, can be a number or expression. | 4 ||
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. | 4 ||
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 4 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 4 ||
| [`elements`](./Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 4 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 4 |

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
| `allies_only` | Boolean | If true, the effect only applies to allied units. | 2 ||
| [`range`](./Enums.md#enum-range) | Enum / Integer | The distance in tiles for the trigger effect; `global` means any distance. | 2 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 ||

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
| [`damage`](./Math_Equations.md) | Equation | Specifies the amount of damage dealt, can be a number or expression. | 2 ||

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
| [`Earth`](Engine_LogicKeys.md#object-earth) | Object | Defines the Earth element effects, including damage value. | 2 ||
| [`Electric`](Engine_LogicKeys.md#object-electric) | Object | Applies a Stun status effect with specified stacks and probability based on variable X. | 2 ||
| [`Fire`](Characters_and_Bosses.md#object-fire) | Integer / Object | Defines the 'Fire' form, which may be a stack count or an object that applies burn or uses lava attack. | 2 ||
| [`Grass`](Engine_LogicKeys.md#object-grass) | Object | Specifies the status effects applied to allies standing on grass tiles. | 2 ||
| [`Gravity`](Engine_LogicKeys.md#object-gravity) | Object | An object defining the effects granted by Gravity elemental attunement. | 2 ||
| [`Holy`](Characters_and_Bosses.md#object-holy) | Enum / Object | Specifies the 'Holy' form within FormChanger, with its own animation suffix and passives. | 2 ||
| [`Ice`](Engine_LogicKeys.md#object-ice) | Object | Applies the Slow status effect to targets hit by ice-element abilities. | 2 ||
| [`Shadow`](Engine_LogicKeys.md#object-shadow) | Object | An object defining the effects granted by Shadow elemental attunement. | 2 ||
| [`Water`](Characters_and_Bosses.md#object-water) | Object | Form state for water element, applying a puddle or movement bonus. | 2 ||
| [`Wind`](Engine_LogicKeys.md#object-wind) | Object | Defines the properties for the Wind element, such as knockback amount. | 2 ||

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
| `RandomDistanceDisplace` | `Number` | The number of stacks of a random distance displacement effect, or an object with stacks, min_dist, and chance. | 2 ||
| `SafeExplosionIfHitSomething` | Number | The radius of a safe explosion that only occurs if it hits an obstacle or entity. | 2 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 ||

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
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 3 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 ||
| [`AllStatsUp`](./Enums.md) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | [.5] |
| [`TakeExtraTurn`](./Enums.md) | Integer | The number of extra turns granted to the source. | 1 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 ||
| [`Burn`](./Enums.md) | Enum / Integer | The amount of Burn applied, either as a fixed number or a formula string. | 2 | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`Poison`](./Enums.md) | Array / Enum / Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 2 | [.5] |

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
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Specifies the amount of damage dealt, can be a number or expression. | 2 ||
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 2 ||
| [`elements`](./Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 2 ||
| [`cant_miss`](./Enums.md) | Boolean | If true, the damage instance always hits its target regardless of accuracy or evasion. | 2 | true |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. | 2 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 |
| [{Damaging Keys}](./Engine_DamagingKeys.md#valid-property-keys) | Object | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 2 |

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
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 ||
| [`FlatLeech`](./Enums.md) | Enum | The flat amount of health restored to the source when dealing damage, applied after the hit. | 2 | X |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 |

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
| [`Burn`](./Enums.md) | Enum / Integer | The amount of Burn applied, either as a fixed number or a formula string. | 2 | 2 |

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
| `health` | Integer | The maximum hit points of the unit. | 3 ||
| `playercat_health` | Integer | The percentage of maximum health the player cat must have to trigger the rebirth. | 3 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 ||
| [`TempSpeedUp`](./Enums.md) | Integer | The number of stacks of temporary Speed Up applied to the unit. | 2 | 10 |

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
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`AllStatsUp`](./Enums.md) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | [.5] |

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
| [`Tech`](./Enums.md) | Integer | The number of stacks of Tech applied, increasing the source's Tech stat. | 2 | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 ||

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
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 2 ||
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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 11 ||
| `enemies_only` | Boolean | If true, the arc lightning effect only chains to enemy units, ignoring allies. | 7 ||

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
| `SafeExplosionIfHitSomething` | Number | The radius of a safe explosion that only occurs if it hits an obstacle or entity. | 2 ||

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
| `HitExplosion` | `Number` | The radius of the explosion triggered on hit. | 2 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 ||

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
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 4 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 4 ||

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
| `TakeExtraDamage` | Number | The percentage of extra damage taken while at full health. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`ManaCostReduction`](./Enums.md) | Integer | The amount or percentage by which ability mana costs are reduced for this unit. | 2 | 2 |

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
| [`mode`](./Enums.md#enum-mode) | Enum | Specifies the comparison mode (equal, greater, less_or_equal, etc.) used for a conditional check. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 2 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 ||
| [`threshold`](Items_and_Equipment.md#object-threshold) | Integer / Object | The health threshold value, either as a formula using X (max health) or a fixed integer. | 2 | 7 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 14 ||
| [`SetDefaultFace`](./Enums.md) | Enum | Specifies the default facial expression, such as 'happy', 'sad', or 'insane'. | 2 | sad |
| [`AllStatsUp`](./Enums.md) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | [.5] |
| [`CharismaUp`](./Enums.md) | Integer | The amount of charisma change, or a keyword like 'item_aux'. | 1 | 5 |
| [`IntelligenceUp`](./Enums.md) | Integer | The amount of Intelligence added as a flat bonus. | 1 | -1 |
| [`SpeedUp`](./Enums.md) | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 1 | 2 |

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
| [`HealAlliesEachTurn`](Engine_StatusAndPassiveKeys.md#object-healallieseachturn) | Object | An object defining how much health and mana are healed to all allies each turn. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
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
| [`HolyDamageBlessing`](Engine_StatusAndPassiveKeys.md#object-holydamageblessing) | Object | An object defining the damage multiplier and status effects applied as a holy damage blessing. | 2 ||

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
| `TogglableRoundEndExtraTurn` | Number | The number of extra turns granted at the end of each round while the unit is the alpha. | 2 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 ||
| [`Brace`](./Enums.md) | Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 3 | 2 |
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 1 | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`AddBonusRange`](./Enums.md) | Integer | The number of additional tiles of range added to the unit's abilities. | 2 | 2 |
| [`AddSpellDamage`](./Enums.md) | Integer || 2 | 2 |
| [`KineticSpikes`](./Enums.md) | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 1 | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`AddBonusRange`](./Enums.md) | Integer | The number of additional tiles of range added to the unit's abilities. | 2 | 2 |

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
| [`AddElementsToWeapon`](./Enums.md#enum-addelementstoweapon) | Enum | Specifies the element to add to the unit's attacks while wearing metal equipment. | 2 ||

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
| [`pool`](./Enums.md#enum-pool) | Array / Enum | Specifies the name of the pool from which an ability is learned or an item is crafted. | 2 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`RandomMagicMissile`](./Enums.md) | Integer | The number of random magic missiles fired, or an object defining its properties. | 2 | 2 |
| [`Cleanse`](./Enums.md) | Integer | The number of stacks of negative status effects removed from the target. | 1 | 0 |

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
| [`RepressedMemoriesMetronome`](Engine_StatusAndPassiveKeys.md#object-repressedmemoriesmetronome) | Object | An object defining the metronome status effect and its pool triggered on mana spend. | 2 ||

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
| `con` | Enum / Integer | The Constitution stat value or modifier. | 1 ||
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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 7 ||
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 5 ||

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
| [`crit_chance`](./Engine_DamagingKeys.md#valid-property-keys) | `String` | The chance for the damage instance to critically hit, expressed as a percentage or equation; values above 1 default to 100%. | 2 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 2 ||

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
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Specifies the amount of damage dealt, can be a number or expression. | 2 ||
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 2 ||
| [`elements`](./Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 2 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 2 ||
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`AllStatsUp`](./Enums.md) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | [.5] |
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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`threshold`](Items_and_Equipment.md#object-threshold) | Integer / Object | The health threshold value, either as a formula using X (max health) or a fixed integer. | 2 | 7 |
| `speed` | Array / Number | The speed of the projectile or move, can be a value or a range. | 1 ||
| `strength` | Integer | The base strength stat, used for physical damage calculations. | 1 ||

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
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 4 |
| [`TempSpellDamageUp`](./Enums.md) | Integer | The amount of temporary spell damage increase applied. | 2 | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`TempDamageUp`](./Enums.md) | Integer | The amount of temporary damage increase applied. | 1 | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 9 ||
| [`EquipTemporaryItem`](./Enums.md) | Enum | Specifies which temporary item is equipped. | 2 | FoodMedium |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`HealthGain`](./Enums.md) | Integer / String | The amount of health restored to the source. | 2 | 2*X |
| [`LuckUp`](./Enums.md) | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 2 | 2 |
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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`AllStatsUp`](./Enums.md) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | [.5] |
| [`threshold`](Items_and_Equipment.md#object-threshold) | Integer / Object | The health threshold value, either as a formula using X (max health) or a fixed integer. | 2 | 7 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`LuckUp`](./Enums.md) | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 2 | 2 |
| [`Fear`](./Enums.md) | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 1 | [.15] |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 ||
| [`RandomMagicMissile`](./Enums.md) | Integer | The number of random magic missiles fired, or an object defining its properties. | 3 | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 2 | Coin |

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
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`DivineShield`](./Enums.md) | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 2 | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`LuckUp`](./Enums.md) | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 2 | 2 |

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
| [`statuses`](Characters_and_Bosses.md#object-statuses) | Object | Defines the status effects applied when the parent trigger event occurs. | 2 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 ||
| [`Shield`](./Enums.md) | Integer / String | The amount of shield granted to the source, absorbing incoming damage. | 2 | 2 |
| [`Thorns`](./Enums.md) | Integer | The amount of thorns damage dealt to attackers on hit. | 2 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 |

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
| [`Tech`](./Enums.md) | Integer | The number of stacks of Tech applied, increasing the source's Tech stat. | 2 | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||

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
| [`TempDexterityUp`](./Enums.md) | Integer | The number of temporary dexterity stacks applied, or a string alias like 'X'. | 2 | 2 |
| [`TempStrengthUp`](./Enums.md) | Integer | The number of stacks of temporary Strength Up applied to the unit. | 2 | 2 |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 |
| [`TempLuckUp`](./Enums.md) | Integer || 1 | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`RefreshMovePoints`](./Enums.md) | Integer | The amount of movement points restored to the source. | 2 | 1 |
| [`Shield`](./Enums.md) | Integer / String | The amount of shield granted to the source, absorbing incoming damage. | 2 | 2 |
| [`threshold`](Items_and_Equipment.md#object-threshold) | Integer / Object | The health threshold value, either as a formula using X (max health) or a fixed integer. | 2 | 7 |
| [`AllStatsUp`](./Enums.md) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | [.5] |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`Temporary`](Abilities_and_Spells.md#object-temporary) | Object | Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions. | 2 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`SpeedUp`](./Enums.md) | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 2 | 2 |
| [`RandomStatUp`](./Enums.md) | Integer | The amount of random stat increase applied, either as a fixed number or a formula string. | 1 | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`IntelligenceUp`](./Enums.md) | Integer | The amount of Intelligence added as a flat bonus. | 2 | -1 |
| [`SpellDamageUp`](./Enums.md) | Integer | The number of stacks of SpellDamageUp applied, increasing spell damage. | 2 | 1 |
| [`DivineShield`](./Enums.md) | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 ||
| [`RefreshMovePoints`](./Enums.md) | Integer | The amount of movement points restored to the source. | 2 | 1 |
| [`DexterityUp`](./Enums.md) | Integer | The amount of dexterity change, or a keyword like 'item_aux'. | 1 | 2 |
| [`SpeedUp`](./Enums.md) | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 1 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 5 ||
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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`Quivered`](./Enums.md) | Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 2 | 2 |
| [`MoveQuivered`](./Enums.md) | Integer | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 1 | 2 |

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
| [`DexterityUp`](./Enums.md) | Integer | The amount of dexterity change, or a keyword like 'item_aux'. | 2 | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`Quivered`](./Enums.md) | Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 1 | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 ||
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
| [`element`](./Enums.md#enum-element) | Array / Enum | Specifies which element(s) the conditional checks against. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`SpeedUp`](./Enums.md) | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 2 | 2 |

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`Shield`](./Enums.md) | Integer / String | The amount of shield granted to the source, absorbing incoming damage. | 2 | 2 |
| [`StrengthUp`](./Enums.md) | Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 1 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 |

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
| `Drag` | Number | The distance (in tiles) that the unit drags knocked-back targets toward itself. | 2 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 ||
| [`OneUseSpellDamageUp`](./Enums.md) | Integer | Increases spell damage by the specified amount, but the effect is consumed after a single use. Alias for SpellDamageUp. | 2 | 2 |
| [`ManaGain`](./Enums.md) | Integer | The amount of mana restored to the source, which can be an expression. | 1 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 |

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
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specifies the tag(s) to check on the target, used in conditional effects. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
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
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Specifies the amount of damage dealt, can be a number or expression. | 2 ||
| `range` | Enum / Integer | The distance in tiles for the trigger effect; `global` means any distance. | 2 ||

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
| [`AOEPuddle`](./Math_Equations.md) | Equation | Specifies the pattern or shape of an area-of-effect puddle left on the ground. | 2 ||

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
| [`knockback`](./Math_Equations.md) | Equation | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 2 ||

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
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 1 ||

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
| [`elements`](./Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`Burn`](./Enums.md) | Enum / Integer | The amount of Burn applied, either as a fixed number or a formula string. | 1 | 2 |

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
| [`elements`](./Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`Burn`](./Enums.md) | Enum / Integer | The amount of Burn applied, either as a fixed number or a formula string. | 1 | 2 |

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
| `CastAgain` | Integer / String | The number of additional times the ability can be cast this turn. | 1 ||

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
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 5 ||
| [`statuses`](Characters_and_Bosses.md#object-statuses) | Object | Defines the status effects applied when the parent trigger event occurs. | 3 ||

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
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | |

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
| `odds` | Number | The probability of the effect occurring, expressed as a decimal or percentage. | 37 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 37 ||
| `UseRandomSpell_Madness` | `Number` | The number of random spells cast when Madness triggers. | 1 ||

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
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specifies the tag(s) to check on the target, used in conditional effects. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`Conditional_Ally`](Abilities_and_Spells.md#object-conditional_ally) | Object || 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 |

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 ||
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Specifies the amount of damage dealt, can be a number or expression. | 1 ||

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
| `distance` | Integer | The number of tiles the target is knocked back or pulled. | 1 ||

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
| `distance` | Integer | The number of tiles the target is knocked back or pulled. | 2 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`AllStatsUp`](./Enums.md) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | [.5] |
| [`Confusion`](./Enums.md) | Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 1 | 2 |

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
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Specifies the amount of damage dealt, can be a number or expression. | 1 ||
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. | 1 ||
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 ||
| [`elements`](./Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 1 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 |

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
| `free` | Boolean | If true, this option requires no cost to activate. | 1 ||

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
| `Appeal` | Number | The amount of appeal provided by the furniture piece to the room. | 1 ||
| `Comfort` | Number | The amount of comfort provided by the furniture piece to the room. | 1 ||
| `Stimulation` | Number | The amount of stimulation provided by the furniture piece to the room. | 1 ||

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
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Specifies the amount of damage dealt, can be a number or expression. | 1 ||
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. | 1 ||
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 ||
| [`elements`](./Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 1 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 |

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
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Specifies the amount of damage dealt, can be a number or expression. | 1 ||
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. | 1 ||
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 ||
| [`elements`](./Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 1 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 |

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
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 ||

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
| [`weights`](./Enums.md#enum-weights) | Array / Enum | Specifies the weight array or named preset for the crazy eye background AI. | 9 ||

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
| [`SizeScalePercent`](./Math_Equations.md) | Equation | A formula string that calculates the percentage scale of the unit's size based on a variable X (e.g., level). | 1 ||
| [`Shield`](./Enums.md) | Integer / String | The amount of shield granted to the source, absorbing incoming damage. | 1 | 2 |
| [`Trample`](./Enums.md) | Array / Integer | The amount of bonus damage dealt when moving through an enemy. | 1 | [3] |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 ||
| [`PassiveGroup`](Characters_and_Bosses.md#object-passivegroup) | Object | A group of passive abilities that can be randomly assigned. | 2 ||

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
| [`brain`](./Enums.md#enum-brain) | Enum | Specifies the AI brain type used for decision-making logic. | 4 ||
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | Specifies the named set of decision weight presets used by the AI. | 4 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 4 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`Charge`](./Enums.md) | Integer | The number of charge stacks applied. | 1 | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`Thorns`](./Enums.md) | Integer | The amount of thorns damage dealt to attackers on hit. | 1 | 2 |

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
| `SpawnScaledRotFly` | Number | The number of scaled Rot Flies to spawn when over-healed. | 1 ||

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
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Specifies the amount of damage dealt, can be a number or expression. | 1 ||
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 ||

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
| `amount` | Array | For ambient light, the target brightness value (as a float or percentage array for RGB). | 1 ||
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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| `exclude_self` | Boolean || 1 ||
| [`RandomStatUp`](./Enums.md) | Integer | The amount of random stat increase applied, either as a fixed number or a formula string. | 1 | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`LuckUp`](./Enums.md) | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 1 | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`PermanentMadness`](./Enums.md) | Integer | The number of permanent madness stacks applied. | 1 | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`Thorns`](./Enums.md) | Integer | The amount of thorns damage dealt to attackers on hit. | 1 | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`PermanentConstitution`](./Enums.md) | Integer | The amount of permanent Constitution stat added or removed. | 1 | -1 |

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
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 5 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 5 ||
| [`ManaGain`](./Enums.md) | Integer | The amount of mana restored to the source, which can be an expression. | 1 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 |

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
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 ||

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
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 5 ||
| [`Madness`](./Enums.md) | Integer | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 3 | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`Madness`](./Enums.md) | Integer | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 1 | 1 |

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
| `multiplier` | Number | A multiplier applied to tile damage dealt to enemies. | 1 ||

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
| [`pool`](./Arrays.md#array-pool) | Array / Enum | Specifies the name of the pool from which an ability is learned or an item is crafted. | 1 ||

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
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Specifies the amount of damage dealt, can be a number or expression. | 1 ||
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. | 1 ||
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 ||
| [`elements`](./Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 1 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 1 ||

</details>

---


<details>
<summary><b>AddSelfStatusToWeapons</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||

</details>

<details>
<summary><b>AddStatusToAllDamage</b></summary>

> **Total Count:** 16

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||

</details>

<details>
<summary><b>AddStatusToBasicAttackWithCooldown</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||

</details>

<details>
<summary><b>AddStatusToFirstBasicAttack</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||

</details>

<details>
<summary><b>AddStatusToKnockbackDamage</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||

</details>

<details>
<summary><b>AddStatusToMeleeDamage</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||

</details>

<details>
<summary><b>AddStatusToReceivedDamage_ExcludeStatuses</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||

</details>

<details>
<summary><b>AddStatusToSpells</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||

</details>

<details>
<summary><b>AddStatusToTrampleDamage</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||

</details>

<details>
<summary><b>Conditional_Adjacent</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||

</details>

<details>
<summary><b>Conditional_DoesDamage</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||

</details>

<details>
<summary><b>Conditional_GoodRoll</b></summary>

> **Total Count:** 30

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||

</details>

<details>
<summary><b>Conditional_NotBoss</b></summary>

> **Total Count:** 13

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||

</details>

<details>
<summary><b>Conditional_PartyMember</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||

</details>

<details>
<summary><b>Conditional_Shielded</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||

</details>

<details>
<summary><b>ExtraStatusWhenDealingDamage</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||

</details>

<details>
<summary><b>NextBattleStatus</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||

</details>

<details>
<summary><b>PassiveLevelScaledStatus</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||

</details>

<details>
<summary><b>StatusAdjacentOnTheirTurnBegin</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||

</details>

<details>
<summary><b>StatusAlliesOnSpendMana</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||

</details>

<details>
<summary><b>StatusAnyCatAllyWhoKills</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||

</details>

<details>
<summary><b>StatusEnemiesOnDeath</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||

</details>

<details>
<summary><b>StatusKilledCharacters</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||

</details>

<details>
<summary><b>StatusKillers</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||

</details>

<details>
<summary><b>StatusOnDealtDamage</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||

</details>

<details>
<summary><b>StatusOnEatPill</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||

</details>

<details>
<summary><b>StatusOnEndMove</b></summary>

> **Total Count:** 9

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||

</details>

<details>
<summary><b>StatusOnOverHealed</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 |

</details>


## Discovered Objects

> These tables were auto-generated by the schema audit tool. They document objects found in the `.gon` files that were not previously documented.

### Object: `AIControlNextTurn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `include_spells` | Boolean || 1 | `true` (Boolean) |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `1` (Number) |


### Object: `AbilityHealthThreshold`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 13 | `FormShrinkFour` (Enum), `DybbukPossess` (Enum) |
| [`threshold`](Items_and_Equipment.md#object-threshold) | Enum / Integer / Object | The health threshold value, either as a formula using X (max health) or a fixed integer. | 12 | `1*champion_multiplier` (Enum), `3*champion_multiplier` (Enum), `200` (Number), `1` (Number), `"max(X*.33, 5)"` (String), `"max(X*.5, 1)"` (String) |
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 7 | `true` (Boolean) |
| `immediate` | Boolean | If true, the action (e.g., attack) occurs instantly without waiting for the unit's turn in the initiative order. | 6 | `true` (Boolean) |
| `use_ai` | Boolean | If true, the ability uses AI targeting logic when triggered at the threshold. | 2 | `true` (Boolean) |
| `also_use_if_buddy_is_dead` | Boolean | If true, the ability is also triggered when the unit's buddy is dead. | 1 | `true` (Boolean) |
| `aux` | Integer | An auxiliary integer value used for item properties, such as hunger value. | 1 | `25` (Number) |
| `threshold_min` | Enum | The minimum health threshold formula (e.g., X) for the ability to trigger. | 1 | `X` (Enum) |


### Object: `AbilityOnRoundEnd`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `DestroyerRaise` (Enum) |
| `force_display_name` | Boolean | If true, forces the display name to show for the ability. | 2 | `true` (Boolean) |


### Object: `AbilityOnRoundEndOnce`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `wp_SignalAmplifierSpawnTerminator` (Enum) |
| `even_of_stunned` | Boolean || 1 | `true` (Boolean) |


### Object: `AddAdvantageToEvent`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `add` | Array / Integer || 1 | `5` (Number) |
| `options` | Array || 1 | `[smash bash open]` (Array) |
| `type` | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `treasure_box` (Enum) |


### Object: `AddStatusToBackstabs`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Bleed` | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 1 | `[1 .1]` (Array), `[3 .1]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |


### Object: `AddStatusToFirstSpellEachTurn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_IsSelf`](Abilities_and_Spells.md#object-conditional_isself) | Object || 1 | `{ ... }` (Object) |
| [`Else`](Abilities_and_Spells.md#object-else) | Object | Contains the fallback effects to apply when a preceding conditional check fails. | 1 | `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 |


### Object: `AddStatusToReceivedDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_IsPhysicalAttack`](Characters_and_Bosses.md#object-conditional_isphysicalattack) | Object || 1 | `{ ... }` (Object) |
| [`Else`](Abilities_and_Spells.md#object-else) | Object | Contains the fallback effects to apply when a preceding conditional check fails. | 1 | `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 |


### Object: `AfterImage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `object` | Array / Enum | Specifies the object or unit to be spawned. | 2 | `PlayerCat_ThiefShade` (Enum) |
| `skilltemp` | Boolean || 2 | `true` (Boolean) |


### Object: `AggroTargetIsGovernedByHitEffect`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `enemies_only` | Boolean | If true, the arc lightning effect only chains to enemy units, ignoring allies. | 1 | `false` (Boolean) |


### Object: `AllStatsAura`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `aura_requires_tag` | Enum | Specifies the tag that units must have to be affected by this aura. | 1 | `humanoid` (Enum) |
| `range` | Enum / Integer | The distance in tiles for the trigger effect; `global` means any distance. | 1 | `global` (Enum) |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `1` (Number) |


### Object: `AllStatsUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `AlluringDoodieEater`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `10` (Number) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ ... }` (Object) |


### Object: `AllyDodgeChanceAura`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `25` (Number) |
| `range` | Enum / Integer | The distance in tiles for the trigger effect; `global` means any distance. | 1 | `1` (Number) |


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
| `frame_range` | Array | Specifies the minimum and maximum animation frame for the health pickup. | 3 | `[6 6]` (Array), `[1 2]` (Array) |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 3 | `4` (Number), `6` (Number) |


### Object: `BackflipWhenTargeted`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 7 | `Teleport` (Enum), `SZBBackflipDodge` (Enum) |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 7 | `4` (Number), `1` (Number) |


### Object: `BaitAura`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `range` | Enum / Integer | The distance in tiles for the trigger effect; `global` means any distance. | 4 | `3` (Number) |


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
| [`statuses`](Characters_and_Bosses.md#object-statuses) | Object | Defines the status effects applied when the parent trigger event occurs. | 5 | `{ ... }` (Object) |


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
| `common` | Enum | Defines the common reward block for a boss encounter. | 20 | `RatBomb` (Enum), `ChubsCollar` (Enum) |
| `rare` | Enum | Defines the rare reward block for a boss encounter. | 16 | `BorisBrain` (Enum), `JohnnysStool` (Enum) |


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
| `allies_only` | Boolean | If true, the effect only applies to allied units. | 3 | `false` (Boolean) |
| `obj` | Array / Enum | Specifies one or more object names to bounce towards the target. | 3 | `ZaratanaVS` (Enum), `PyrophinaVS` (Enum) |
| `reclaim_if_lost` | Boolean | If true, the buddy can be reclaimed after being lost. | 1 | `true` (Boolean) |


### Object: `BuffImmunity`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exclude` | Enum | Specifies an element or effect that does not trigger the form change. | 1 | `SpellDamageUp` (Enum) |


### Object: `BungaCheers`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ally_damage` | Enum | Specifies the cheer effect when an ally takes damage. | 1 | `littleboo` (Enum) |
| `ally_dead` | Enum | Specifies the cheer effect when an ally dies. | 1 | `bigboo` (Enum) |
| `enemy_damage` | Enum | Specifies the cheer effect when an enemy takes damage. | 1 | `littlecheer` (Enum) |
| `enemy_dead` | Enum | Specifies the cheer effect when an enemy dies. | 1 | `bigcheer` (Enum) |
| `warrior_tag` | Enum | Specifies the tag used to identify allied warriors for this ability. | 1 | `bungawarrior` (Enum) |


### Object: `BungaEntrance`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `BungaEntrance` (Enum), `BecomeTheDestroyer` (Enum) |
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 2 | `true` (Boolean) |
| `health_threshold` | Integer | The health value at or below which the reaction triggers. -1 disables this check. | 2 | `150` (Number), `-1` (Number) |
| `warrior_tag` | Enum | Specifies the tag used to identify allied warriors for this ability. | 2 | `bungawarrior` (Enum), `finalboss_clonecat` (Enum) |


### Object: `Burn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `CatPartsSizeScale`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `head` | Enum / Number | The catalog ID for the cat's head part. | 1 | `1.3` (Number) |


### Object: `CatPartsTransform`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `palette` | Enum / Integer | Specifies the color palette index for the ability's visuals. | 17 | `Fighter` (Enum), `Medic` (Enum), `76` (Number), `78` (Number) |
| `ear1` | Integer || 13 | `1501` (Number), `343` (Number) |
| `tail` | Integer | The catalog ID for the cat's tail part. | 13 | `1504` (Number), `1503` (Number) |
| `arm2` | Number | The catalog ID for the cat's second arm part. | 11 | `1013` (Number), `1501` (Number) |
| `arm1` | Number | The catalog ID for the cat's first arm part. | 10 | `1043` (Number), `1013` (Number) |
| `ear2` | Integer | The catalog ID for the cat's second ear part. | 10 | `1005` (Number), `1501` (Number) |
| `leg1` | Integer | The catalog ID for the cat's first leg part. | 8 | `41` (Number), `1043` (Number) |
| `leg2` | Integer | The catalog ID for the cat's second leg part. | 8 | `41` (Number), `1043` (Number) |
| `mouth` | Number | The catalog ID for the cat's mouth part. | 8 | `1005` (Number), `1069` (Number) |
| `head` | Enum / Number | The catalog ID for the cat's head part. | 6 | `1027` (Number), `1504` (Number) |
| `texture` | Integer | The catalog ID for the cat's texture. | 6 | `322` (Number), `19` (Number) |
| `body` | Number | The catalog ID for the cat's body part. | 5 | `31` (Number), `1029` (Number) |
| `eye1` | Integer | The catalog ID for the cat's first eye part. | 3 | `1013` (Number), `1069` (Number) |
| `eye2` | Integer | The catalog ID for the cat's second eye part. | 3 | `1013` (Number), `1069` (Number) |
| `eyebrow1` | Integer | The catalog ID for the cat's first eyebrow part. | 1 | `1069` (Number) |
| `eyebrow2` | Integer | The catalog ID for the cat's second eyebrow part. | 1 | `1070` (Number) |


### Object: `CaveFamilyEnrage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 6 | `CaveCatEnrageTwo` (Enum), `CaveCatEnrageOne` (Enum) |
| `count` | Array / Integer | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 6 | `1` (Number), `0` (Number) |
| `tag` | Array / Enum | Specifies the tag(s) to check on the target, used in conditional effects. | 6 | `cavefamily` (Enum) |


### Object: `CerberubsAggroTargetBehavior`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alert_form` | Enum | Specifies the form to use when the unit is alerted. | 1 | `Alert` (Enum) |
| `default_form` | Enum | Specifies the default form before aggro. | 1 | `Normal` (Enum) |


### Object: `ChainKnockback`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `ChanceToBlockAndCounter`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `backstab_only` | Boolean || 1 | `true` (Boolean) |
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `100` (Number) |


### Object: `ChanceToForceEvent`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `25` (Number) |
| `event` | Enum || 1 | `Blessing` (Enum) |


### Object: `ChanceToFormChangeOnAbilityDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `15` (Number) |
| `form` | Enum / Integer | Specifies the name of the form the unit changes into. | 1 | `Flop2` (Enum) |


### Object: `ChanceToSpitOnDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 7 | `MoonHandDrop` (Enum), `SpewerSpit` (Enum) |
| `flat_chance` | Integer | The base percentage chance to spit when taking damage. | 5 | `100` (Number), `50` (Number) |
| `chance_per_damage` | Integer | The additional percentage chance to spit per point of damage taken. | 3 | `0` (Number), `2` (Number) |
| `backstabs_only` | Boolean | If true, the reaction only triggers on backstab damage. | 1 | `true` (Boolean) |
| `even_on_0_damage_if_knockback` | Boolean | If true, the reaction triggers on zero damage if knockback occurs. | 1 | `true` (Boolean) |


### Object: `ChaosBossFormChangeGuide`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `active_pieces` | Array | An array of piece names that are considered actively part of the current form. | 1 | `[Johnny Throb Flush]` (Array) |
| `passive_pieces` | Array | An array of piece names that are considered passively part of the current form. | 1 | `[Host Nettle Bubs]` (Array) |
| `passives_health_threshold` | Integer | The health percentage threshold at which the boss's passive abilities change. | 1 | `50` (Number) |


### Object: `ChaosBossPieces`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `active_pieces` | Array | An array of piece names that are considered actively part of the current form. | 1 | `[Johnny Throb Flush]` (Array) |
| `passive_pieces` | Array | An array of piece names that are considered passively part of the current form. | 1 | `[Host Nettle Bubs]` (Array) |


### Object: `ChaosHeadDropIn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `ChaosSpawnIn` (Enum) |
| `new_music` | Enum | Specifies the music track to play during the boss's head drop-in animation. | 1 | `chaos_boss_part2` (Enum) |
| `tag` | Array / Enum | Specifies the tag(s) to check on the target, used in conditional effects. | 1 | `riftheadguardian` (Enum) |


### Object: `CharacterLightSource`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `color` | Array | The RGB color of the light source. | 16 | `[.7 .8 .9]` (Array), `[1 1 1]` (Array) |
| `size` | Enum / Number | The scale factor (size multiplier) of the spawned unit. | 16 | `1.7` (Number), `8` (Number) |
| `glow` | Array | The RGBA glow color of the light source. | 8 | `[1 .75 .5 .5]` (Array), `[1 1 1 1]` (Array) |


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
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 |


### Object: `Confusion`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `ConjureBonusAbility`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `Class` (Enum), `Colorless` (Enum) |
| `upgraded` | Boolean | If true, the evolved ability is the upgraded version. | 2 | `true` (Boolean) |


### Object: `Consumed`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `mount_mode` | Boolean / Enum || 12 | `true` (Boolean), `auto` (Enum) |
| `drop_on_death` | Boolean / Enum | Determines if and how the consumed unit is dropped on death; values include 'true', 'false', or 'deferred'. | 11 | `false` (Boolean), `true` (Boolean), `deferred` (Enum) |


### Object: `ConvertDamageToScaledStatus`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DelayedPain` | Integer | The number of stacks of DelayedPain applied, dealing damage after a delay. | 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `3` (Number) |


### Object: `CounterAttack`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 5 | `StegoTailSwipe` (Enum), `neck_TentacleArmorCounter` (Enum) |
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `15` (Number) |
| `melee_only` | Boolean || 1 | `true` (Boolean) |
| `ranged_only` | Boolean | If true, the reaction only triggers on ranged attacks. | 1 | `true` (Boolean) |
| `without_orienting` | Boolean | If true, the counter-attack does not rotate the character to face the attacker. | 1 | `true` (Boolean) |


### Object: `CounterNextAttacks`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `CreateGlobalModifiers`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`BloodRain`](Engine_GlobalModifierKeys.md#object-bloodrain) | Integer / Object | If non-zero, enables the blood rain visual effect. | 3 | `1` (Number), `{ ... }` (Object) |
| [`LowerAmbientLight`](Abilities_and_Spells.md#object-lowerambientlight) | Object || 3 | `50` (Number), `33` (Number), `{ ... }` (Object) |


### Object: `CritChanceUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `CyborgTurns`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`TakeBonusTurnWithAIControl`](Abilities_and_Spells.md#object-takebonusturnwithaicontrol) | Object || 1 | `{ ... }` (Object) |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `1` (Number) |


### Object: `DamageUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `DeathChill`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `DeathRattleRevive`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 8 | `HitlerPulp2` (Enum), `HitlerPulp4` (Enum) |
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 8 | `true` (Boolean) |


### Object: `DejaVu`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `DelayedAutoRevive`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `health` | Integer | The maximum hit points of the unit. | 6 | `30` (Number), `15` (Number) |
| `rounds` | Integer | The number of rounds after which the auto-revive triggers. | 6 | `1` (Number), `2` (Number) |


### Object: `DepressionAura`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `aura_effects_allies` | Boolean | If false, the aura does not affect allies. | 4 | `false` (Boolean) |
| `range` | Enum / Integer | The distance in tiles for the trigger effect; `global` means any distance. | 4 | `global` (Enum), `1` (Number) |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 4 | `1` (Number) |


### Object: `DiceBehavior`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dice_size` | Integer | The number of sides on the die. | 1 | `6` (Number) |
| `knockback_damage` | Integer | The amount of damage dealt by the knockback. | 1 | `5` (Number) |


### Object: `DiesToElement`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `element` | Array / Enum || 1 | `Fire` (Enum) |
| `instant` | Boolean | If true, the consumption happens immediately without a timer. | 1 | `true` (Boolean) |


### Object: `DiesToPiercingAndSpikes`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `deferred` | Boolean | If true, the destruction is deferred until the character is settled. | 1 | `true` (Boolean) |


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
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `ShadowstepDodge` (Enum) |


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
| `exit_ability` | Enum | Determines the ability used when the Dybbuk possession ends. | 1 | `DybbukReturn` (Enum) |
| `form` | Enum / Integer | Specifies the name of the form the unit changes into. | 1 | `Possessing` (Enum) |


### Object: `Dyslexia`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 |


### Object: `Empath`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 |


### Object: `ExtraBasicAttacks_Status`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `ExtraBasicMoves_Status`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `FaceAwayLastDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability_damage_only` | Boolean | If true, the reaction only triggers on ability damage, not basic attacks. | 1 | `true` (Boolean) |
| `override_hit_animation` | Boolean | If true, the character's hit animation is overridden by the face-away animation. | 1 | `true` (Boolean) |
| `use_turn_animations` | Boolean | If true, uses turn-based animations for the face change. | 1 | `true` (Boolean) |


### Object: `FaceLastDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `use_turn_animations` | Boolean | If true, uses turn-based animations for the face change. | 1 | `true` (Boolean) |


### Object: `FinalBossBeamQueue`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `queue` | Enum | Specifies the ability queued to fire the boss's beam. | 1 | `TheChild_TargetBeam` (Enum) |
| `release` | Enum | Specifies the ability queued to release the boss's stored beams. | 1 | `TheChild_ReleaseBeams` (Enum) |
| `transform` | Enum | Specifies the ability queued to transform the boss into its next form. | 1 | `TheChild_TransformBoris` (Enum) |


### Object: `FinalBossBecomeTheChild`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `GlobalSpawnCharacter` | Enum || 1 | `MegaGuppy` (Enum) |
| `PlayBackground` | Integer || 1 | `1` (Number), `0` (Number) |
| [`SwitchMusic`](Abilities_and_Spells.md#object-switchmusic) | Object || 1 | `{ ... }` (Object) |


### Object: `FinalBossHitCountdownBoris`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object | The name of the ability the source is forced to use, optionally with a chance. | 1 | `neck_ChefsApron` (Enum), `TheChild_TransformExplosive` (Enum), `{ ... }` (Object) |
| `icon` | Integer | The sprite ID or atlas key for the countdown icon when not ready. | 1 | `802` (Number) |
| `icon_ready` | Integer | The sprite ID or atlas key for the countdown icon when the ability is ready. | 1 | `803` (Number) |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `7` (Number) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 |


### Object: `FinalBossHitCountdownExplosive`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object | The name of the ability the source is forced to use, optionally with a chance. | 1 | `neck_ChefsApron` (Enum), `head_HitlersToupe` (Enum), `{ ... }` (Object) |
| `icon` | Integer | The sprite ID or atlas key for the countdown icon when not ready. | 1 | `800` (Number) |
| `icon_ready` | Integer | The sprite ID or atlas key for the countdown icon when the ability is ready. | 1 | `801` (Number) |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `7` (Number) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 |


### Object: `FinalBossHitCountdownHoly`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon` | Integer | The sprite ID or atlas key for the countdown icon when not ready. | 1 | `804` (Number) |
| `icon_ready` | Integer | The sprite ID or atlas key for the countdown icon when the ability is ready. | 1 | `805` (Number) |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `7` (Number) |


### Object: `FinalBossPupils`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `look_at_offset` | Array | A 3D vector offset from the head position that the pupils should look at. | 1 | `[0 2.5 0]` (Array) |
| `radius` | Array / Integer || 1 | `13` (Number) |
| `reset_center_because_no_target_halflife` | Number | The half-life for the pupil position to reset to center when no target is available. | 1 | `.1` (String) |
| `reset_center_because_of_animation_halflife` | Number | The half-life for the pupil position to reset to center during an animation. | 1 | `.05` (String) |
| `teleport_tracking_halflife` | Number | The half-life for the pupil tracking to reacquire a target after a teleport. | 1 | `.01` (String) |
| `tracking_acquisition_halflife` | Number | The half-life for the pupil tracking to smoothly acquire a new target. | 1 | `.1` (String) |
| `virtual_head_position` | Array | A 3D vector representing the virtual position of the head for pupil tracking. | 1 | `[11 2 11]` (Array) |


### Object: `FinalBossShieldHealth`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `break_ability` | Enum | Specifies the ability used to break the shield. | 1 | `DestroyerBreakShield` (Enum) |
| `state_health` | Array | An array of health thresholds defining state transitions. | 1 | `[0 35 35 35 35 0]` (Array) |


### Object: `FinalBossSyncAnimations`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `other_character` | Enum | Specifies the name of the other boss character whose animations are synced. | 1 | `MegaGuppy` (Enum) |
| [`other_form_change_abilities`](Characters_and_Bosses.md#object-other_form_change_abilities) | Object || 1 | `{ ... }` (Object) |


### Object: `Flammable`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `FlyDamageIncrease`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allies_only` | Boolean | If true, the effect only applies to allied units. | 1 | `true` (Boolean) |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `2` (Number) |


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
| `form` | Enum / Integer | Specifies the name of the form the unit changes into. | 2 | `Rain` (Enum) |


### Object: `FormChangeHealthThreshold`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `form_above` | Enum | The form to change to when health is above the threshold. | 3 | `Default` (Enum), `Full` (Enum) |
| `form_below` | Enum | The form to change to when health is below the threshold. | 3 | `DesireMech` (Enum), `Standing2` (Enum) |
| [`threshold`](Items_and_Equipment.md#object-threshold) | Enum / Integer / Object | The health threshold value, either as a formula using X (max health) or a fixed integer. | 3 | `X-4` (Enum), `25` (Number), `50` (Number) |
| `count_shield` | Boolean | If true, shields count towards the health threshold calculation. | 1 | `true` (Boolean) |


### Object: `FormChangeOffMap`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `form_offmap` | Enum | Specifies the form name to use when the unit is off the map. | 8 | `Insane_Ceiling` (Enum), `SpawningPhase` (Enum) |
| `form_onmap` | Enum | Specifies the form name to use when the unit returns to the map. | 8 | `Default_Ground` (Enum), `Insane_Ground` (Enum) |


### Object: `FormChangeOnElementInfluence`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `element` | Array / Enum || 9 | `[fire]` (Array), `water` (Enum), `wind` (Enum) |
| `form` | Enum / Integer | Specifies the name of the form the unit changes into. | 9 | `hot` (Enum), `default` (Enum) |
| `exclude` | Enum | Specifies an element or effect that does not trigger the form change. | 5 | `water` (Enum), `fire` (Enum) |
| `particle` | Enum | Specifies the particle effect displayed. | 5 | `FireExtinguish` (Enum) |
| `sfx` | Enum | Specifies the sound effect to play when the form change triggers. | 5 | `FireExtinguish` (Enum) |


### Object: `FormChangeWhileHasStatus`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `status` | Enum || 35 | `T2CopyCatInternal` (Enum), `Grappling` (Enum) |
| `form_hasnot` | Enum | Specifies a form that the unit must not be in for the status-triggered form change to occur. | 30 | `Default` (Enum), `Empty` (Enum) |
| `form_has` | Enum | Specifies a form that the unit must be in for the status-triggered form change to occur. | 25 | `Primed` (Enum), `Full` (Enum) |


### Object: `FormChangeWhilePrimingAbility`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `not_priming` | Enum | Specifies the form name to use when the unit is not priming an ability. | 6 | `DualSword` (Enum), `SwordAndShield` (Enum) |
| `priming` | Enum | Specifies the form name to use while the unit is priming an ability. | 6 | `DualSword_Primed` (Enum), `Priming` (Enum) |


### Object: `FormChanger`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `initial_form` | Enum / Integer | Specifies the starting form name for a unit with FormChanger. | 56 | `Default` (Enum), `Normal` (Enum), `1` (Number), `5` (Number) |
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
| [`Rain`](Characters_and_Bosses.md#object-rain) | Object | Defines the rain weather effect with associated particle, sound, and rendering settings. | 2 | `4` (Number), `1` (Number), `{ ... }` (Object) |
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
| [`Die`](Characters_and_Bosses.md#object-die) | Integer / Object | If set, kills the target immediately. | 1 | `6` (Number), `1` (Number), `{ ... }` (Object) |
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
| `sync_brain_patterns` | Boolean | If true, synchronizes brain patterns across form changes. | 1 | `true` (Boolean) |


### Object: `Fragile`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `FragileDuringElement`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `FrankBolts`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 |


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
| [`Tangled`](Abilities_and_Spells.md#object-tangled) | Array / Integer / Object | The number of stacks of the Tangled status effect applied, or an object defining its properties such as `stacks` and `alt_art`. | 1 | `[1 .1]` (Array), `[1 .33]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |


### Object: `GlobalMeleeRevengeDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `knockback` | Enum / Integer | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 1 | `5` (Number) |


### Object: `HPAltStates`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `clipname` | Enum | Specifies the animation clip name to use for the alt state. | 1 | `poopmain` (Enum) |
| `thresholds` | Array | An array of health percentage thresholds that trigger an alt state. | 1 | `[[ 1 0 ] [ 0 3 ]]` (Array) |


### Object: `HealNeighborsEachTurn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allies_only` | Boolean | If true, the effect only applies to allied units. | 1 | `true` (Boolean) |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `3` (Number) |


### Object: `HealingAura`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `HealthPickup`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `frame_range` | Array | Specifies the minimum and maximum animation frame for the health pickup. | 15 | `[1 2]` (Array), `[5 5]` (Array) |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 15 | `7` (Number), `10` (Number) |
| `stored_food_value` | Integer | The amount of food value stored in this pickup. | 15 | `4` (Number), `2` (Number) |
| `anything_eats` | Boolean | If true, any unit can consume this health pickup. | 4 | `true` (Boolean) |
| `force_frame` | Integer | Forces the health pickup to use a specific animation frame. | 1 | `12` (Number) |


### Object: `HealthRegenUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `HitlerExecute`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `HitlerShoot` (Enum) |
| `tag` | Array / Enum | Specifies the tag(s) to check on the target, used in conditional effects. | 1 | `grown_hitler_clone` (Enum) |
| [`threshold`](Items_and_Equipment.md#object-threshold) | Enum / Integer / Object | The health threshold value, either as a formula using X (max health) or a fixed integer. | 1 | `15` (Number) |


### Object: `Hypomania`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 |


### Object: `ImmediateAbilityReaction`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 13 | `FormShrinkTwoSnakey` (Enum), `ButtWeb_AlreadyEnraged` (Enum) |
| `ability_damage_only` | Boolean | If true, the reaction only triggers on ability damage, not basic attacks. | 6 | `true` (Boolean) |
| `backstabs_only` | Boolean | If true, the reaction only triggers on backstab damage. | 2 | `true` (Boolean) |
| `damage_threshold` | Integer | The amount of damage that must be dealt to trigger the ability reaction. | 2 | `10` (Number) |
| `even_if_blocked` | Boolean | If true, the reaction triggers even if the damage is blocked. | 2 | `true` (Boolean) |
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 2 | `true` (Boolean) |
| `health_threshold` | Integer | The health value at or below which the reaction triggers. -1 disables this check. | 2 | `50` (Number), `70` (Number) |
| `buddy_damage_only` | Boolean | If true, only damage dealt by the unit's buddy triggers the reaction. | 1 | `true` (Boolean) |
| `target_furthest_valid` | Boolean | If true, the reaction targets the furthest valid enemy. | 1 | `true` (Boolean) |


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
| `form_unwashed` | Enum | Specifies the form name for the unwashed state. | 1 | `Unwashed` (Enum) |
| `form_washed` | Enum | Specifies the form name for the washed state. | 1 | `Washed` (Enum) |


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
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `1` (Number) |
| `tickdown_this_turn` | Boolean | If true, madness stacks decrease at the start of this turn instead of the next. | 1 | `true` (Boolean) |


### Object: `ManaPickup`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `frame_range` | Array | Specifies the minimum and maximum animation frame for the health pickup. | 3 | `[6 6]` (Array), `[1 2]` (Array) |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 3 | `4` (Number), `6` (Number) |


### Object: `MegaDinoDropController`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `head_drop` | Enum | Specifies the ability triggered when the head drops down. | 1 | `MD_HeadDrop` (Enum) |
| `leg_leave` | Enum | Specifies the ability triggered when the legs leave the body. | 1 | `MD_LegLeave` (Enum) |
| `leg_return` | Enum | Specifies the ability triggered when the legs return to the body. | 1 | `MD_LegReturn` (Enum) |
| `stable_legs` | Integer | The number of legs that must be stable for the head to drop. | 1 | `3` (Number) |


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
| [`Cleanse`](Engine_StatusAndPassiveKeys.md#object-cleanse) | Integer / Object | The number of stacks of negative status effects removed from the target. | 1 | `1` (Number), `0` (Number), `{ ... }` (Object) |
| `sound_event` | Enum | Specifies the sound event to play when the pickup is used. | 1 | `EatAntidote` (Enum) |


### Object: `MonkCatReactionAbilities`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `attack` (Enum) |
| `move` | Enum | Specifies the name of the class's default movement ability. | 1 | `move` (Enum) |
| `spell` | Enum | Specifies the spell ability to use as a reaction. | 1 | `MCHadouken` (Enum) |
| `trinket` | Enum | The name of the trinket item the unit starts with. | 1 | `MCHadouken` (Enum) |
| `weapon` | Enum || 1 | `attack` (Enum) |


### Object: `MotherGrowController`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`eat_damage`](Characters_and_Bosses.md#object-eat_damage) | Object || 1 | `{ ... }` (Object) |
| `tumor_object` | Enum | Specifies the name of the tumor object to spawn. | 1 | `MotherTumor` (Enum) |


### Object: `MotherTumorPassive`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Cat`](Characters_and_Bosses.md#object-cat) | Object || 1 | `{ ... }` (Object) |
| [`NonCat`](Characters_and_Bosses.md#object-noncat) | Object || 1 | `{ ... }` (Object) |
| `considered_forms` | Array | An array of form names the tumor considers for interaction. | 1 | `[Big BigHolding BigHoldingCat]` (Array) |
| `grow_ability` | Enum | Specifies the ability used by the tumor to grow. | 1 | `MotherTumorGrow` (Enum) |
| `pass_ani` | Enum | Specifies the animation played when passing something to the tumor. | 1 | `pass` (Enum) |
| `receive_ani` | Enum | Specifies the animation played when receiving something from the tumor. | 1 | `receive` (Enum) |


### Object: `MotherTumorSpawnInCapture`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Cat`](Characters_and_Bosses.md#object-cat) | Object || 2 | `{ ... }` (Object) |
| [`NonCat`](Characters_and_Bosses.md#object-noncat) | Object || 2 | `{ ... }` (Object) |
| [`Nothing`](Characters_and_Bosses.md#object-nothing) | Object || 1 | `{ ... }` (Object) |


### Object: `Mount`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `eject_ability` | Enum | Specifies the ability used to eject the mounted character. | 1 | `MechSuitEject` (Enum) |
| `enter_ability` | Enum | Specifies the ability used to enter the mount. | 1 | `EnterMech` (Enum) |


### Object: `MoveAfterAnyAttemptedAttack`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `weights` | Array / Enum | Specifies the weight array or named preset for the crazy eye background AI. | 1 | `bat_chaos_runaway` (Enum) |


### Object: `MoveAwayFromDamageSource`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `move_ability` | Enum | Specifies the movement ability (e.g., BirdFly, TrampleMoveOne) used for the movement action. | 1 | `BirdFly` (Enum) |


### Object: `MoveAwayWhenEnemyAdjacent`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `move_ability` | Enum | Specifies the movement ability (e.g., BirdFly, TrampleMoveOne) used for the movement action. | 1 | `YA_Jetpack` (Enum) |
| `once_per_turn` | Boolean | If true, the movement away can only trigger once per turn. | 1 | `true` (Boolean) |
| `weights` | Array / Enum | Specifies the weight array or named preset for the crazy eye background AI. | 1 | `stay_far_always_move` (Enum) |


### Object: `MoveQuivered`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `MoveTowardsKillers`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `character_filter` | Array | Specifies which characters to consider as killers when moving towards them. | 3 | `[SpiderCat TallSpiderCat]` (Array) |
| `move_ability` | Enum | Specifies the movement ability (e.g., BirdFly, TrampleMoveOne) used for the movement action. | 3 | `SpiderReturn` (Enum) |


### Object: `MultiSpawnOnDeath`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `count` | Array / Integer | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 1 | `[0 2]` (Array) |
| `obj` | Array / Enum | Specifies one or more object names to bounce towards the target. | 1 | `Maggot` (Enum) |


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
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `10` (Number) |
| `object` | Array / Enum | Specifies the object or unit to be spawned. | 1 | `CharmedDip` (Enum) |


### Object: `Paranoia`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 |


### Object: `PassiveIfStrAuxEquals`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 7 | `{ ... }` (Object) |
| `value` | Enum | The numeric value or formula associated with the buff. | 7 | `int` (Enum), `spd` (Enum) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 7 |


### Object: `PassiveIfWeaponIsUsable`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Brace`](Events_and_Encounters.md#object-brace) | Enum / Integer / Object | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 2 | `[1 .5]` (Array), `10` (Number), `4` (Number), `{ ... }` (Object) |


### Object: `PassiveWhenDead`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 |
| [`AutocastEachRound`](Abilities_and_Spells.md#object-autocasteachround) | Enum / Object | Contains an ability name and optional 'even_if_stunned' flag to autocast each round. | 1 | `SpiderReturn` (Enum), `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 |


### Object: `PassiveWhenOnTile`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 7 | `{ ... }` (Object) |
| `tile` | Array / Enum | Specifies the tile type(s) to change to, either a single tile string or an array of tiles. | 7 | `[WaterTile]` (Array), `[TallGrassTile TallFlowerTile]` (Array) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 7 |


### Object: `PassiveWhileHasDurability`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`MovementReaction`](Characters_and_Bosses.md#object-movementreaction) | Object | Specifies an ability to cast when a unit moves within range, with options for targeting and conditions. | 1 | `{ ... }` (Object) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 |


### Object: `PassiveWhileNotHasStatus`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |
| `status` | Enum || 2 | `DemonicGlyph_Movement` (Enum), `ExistUntilIdleUpkeep` (Enum) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 |


### Object: `PassiveWhileShielded`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 1 | `[1 .5]` (Array), `4` (Number), `3` (Number), `{ ... }` (Object) |


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
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `25` (Number) |
| `object` | Array / Enum | Specifies the object or unit to be spawned. | 1 | `Poop` (Enum) |


### Object: `ProtectTargetedAllies`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `SwapPositions_TankCat` (Enum) |
| `target_filter` | Enum | Specifies which targets the protection applies to, based on their unit type or tag. | 2 | `any` (Enum), `Kitten` (Enum) |


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
| [`self_damage`](Abilities_and_Spells.md#object-self_damage) | Boolean / Integer / Object | Defines damage or effects applied to the caster when using the ability. | 8 | `2` (Number) |


### Object: `RefreshEquipmentAbilityOnElement`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `element` | Array / Enum || 2 | `Electric` (Enum) |
| `text` | String || 2 | `"COMBAT_POPUP_RECHARGED"` (String) |


### Object: `RunWhenLastPlayerCatIsCharmed`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allow_decision_mid_turn` | Boolean | If true, allows the decision to run to occur mid-turn instead of at the end. | 1 | `true` (Boolean) |
| `legacy_savekey` | Enum | Specifies the save key used to persist a legacy stolen cat ID. | 1 | `Legacy_Marshmallow_StolenCatID` (Enum) |


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
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 |


### Object: `ScaledStatusOnHolyShieldBlock`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`RandomMagicMissile`](Abilities_and_Spells.md#object-randommagicmissile) | Integer / Object | The number of random magic missiles fired, or an object defining its properties. | 1 | `[1 .5]` (Array), `6` (Number), `10` (Number), `{ ... }` (Object) |


### Object: `ScalingAttackAnimation`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`default`](Characters_and_Bosses.md#object-default) | Enum / Object || 1 | `bite1` (Enum) |
| `thresholds` | Array | An array of health percentage thresholds that trigger an alt state. | 1 | `[[ 5 bite2 ] [ 10 bite3 ]]` (Array) |


### Object: `SchrodingerDisorder`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 |


### Object: `Scleroderma`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 |


### Object: `SharePickups`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `include_coins` | Boolean | If true, coins are included in the shared pickup pool. | 1 | `true` (Boolean) |


### Object: `ShoulderCheck`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `ShovingMatch`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `SkipFirstRounds`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `pop_chance` | Integer | The percentage chance that the first round is skipped. | 1 | `50` (Number) |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `2` (Number) |


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
| `damage` | Equation | Specifies the amount of damage dealt, can be a number or expression. | 4 | `9` (Equation), `5` (Equation) |
| `knockback` | Enum / Integer | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 4 | `1` (Number), `5` (Number) |
| `chain` | Boolean | Specifies the ability to chain into and execute. | 2 | `true` (Boolean) |


### Object: `SpawnCatCopyWhenDowned`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `object` | Array / Enum | Specifies the object or unit to be spawned. | 2 | `PlayerCat_NecroShade` (Enum), `PlayerCat_AncestralShade` (Enum) |
| `prevent_chain_tag` | Enum | A tag that prevents chaining of spawns from the same source. | 2 | `necroset_shade` (Enum), `ancestorset_shade` (Enum) |


### Object: `SpawnExtraThingsOnBattleStart`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `number` | Array / Integer || 31 | `[3 8]` (Array), `[0 2]` (Array), `3` (Number), `1` (Number) |
| `object` | Array / Enum | Specifies the object or unit to be spawned. | 23 | `[Spookie Scary Tatters Wisp Wisp Wisp]` (Array), `[Bombchu Deathbot RoboVacuum TinkererTurret]` (Array), `NeutralToad` (Enum), `Poop` (Enum) |
| `tile` | Array / Enum | Specifies the tile type(s) to change to, either a single tile string or an array of tiles. | 7 | `TallGrassTile` (Enum), `FireTile` (Enum) |
| `trap` | Enum || 2 | `BearTrap` (Enum), `LandMine` (Enum) |


### Object: `SpawnItemLinkedFamiliar`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `break_on_pop_only` | Boolean || 2 | `true` (Boolean) |
| `object` | Array / Enum | Specifies the object or unit to be spawned. | 2 | `PyrophinaFamiliar` (Enum), `ZaratanaFamiliar` (Enum) |


### Object: `SpawnObjectOnPopCorpse`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `count` | Array / Integer | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 1 | `2` (Number) |
| `except_tiny` | Boolean || 1 | `true` (Boolean) |
| `object` | Array / Enum | Specifies the object or unit to be spawned. | 1 | `CharmedTinySpider` (Enum) |


### Object: `SpawnOnDeath`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `faction` | Enum | Specifies the faction of a spawned unit or projectile, determining its team allegiance and AI behavior. | 4 | `enemies` (Enum), `allies` (Enum) |
| `obj` | Array / Enum | Specifies one or more object names to bounce towards the target. | 4 | `[Spookie Spookie Scary Coin2 Coin3 Coin4]` (Array), `[Kitten Kitten TomTom TomTom Mangy Mangy CatCaller CatCaller GlassSpitter SpiderCat...]` (Array), `BeefyCharmedLeech` (Enum), `RiftKitten` (Enum) |
| [`additional_statuses`](Characters_and_Bosses.md#object-additional_statuses) | Object || 1 | `{ ... }` (Object) |


### Object: `SpawnRandomPickupsOnTaggedUnitKilled`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `count` | Array / Integer | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 1 | `[2 3]` (Array) |
| `tag` | Array / Enum | Specifies the tag(s) to check on the target, used in conditional effects. | 1 | `poop` (Enum) |


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
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 3 | `1` (Number) |


### Object: `StatDependentPassive`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AddDamageToBasicAttack` | String || 1 | `4` (Number), `1` (Number), `"min(min(min(min(min(min(str,dex),int),con),lck),spd),cha)-2"` (String) |


### Object: `StatusAdjacentOnTheirTurnEnd`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ForceMoveAway` | Integer | The distance to force the target away from the source. | 1 | `1` (Number), `{ ... }` (Object) |


### Object: `StatusAfterXTurns`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object | The name of the ability the source is forced to use, optionally with a chance. | 2 | `neck_ChefsApron` (Enum), `CancerExplode` (Enum), `{ ... }` (Object) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 |


### Object: `StatusAllCharactersOnSpawn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 |
| [`Else`](Abilities_and_Spells.md#object-else) | Object | Contains the fallback effects to apply when a preceding conditional check fails. | 1 | `{ ... }` (Object) |
| `Poison` | Array / Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 1 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |


### Object: `StatusCollector`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `StrengthUp` | Enum / Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 7 | `[1 .5]` (Array), `4` (Number), `-2` (Number), `{ ... }` (Object) |
| `Poison` | Array / Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 4 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |
| [`Slow`](#object-slow) | Array / Enum / Integer / Object | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 4 | `[1 .1]` (Array), `[1 .25]` (Array), `-1` (Number), `3` (Number), `{ ... }` (Object) |


### Object: `StatusEachRoundBegin`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `NonStackingShield` | Number || 8 | `3` (Number), `8` (Number) |


### Object: `StatusEachRoundEnd`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`DoDamage`](Abilities_and_Spells.md#object-dodamage) | Object | Contains damage parameters (amount, type, tile targets) to deal damage to the target. | 1 | `{ ... }` (Object) |
| [`UseAbility`](Abilities_and_Spells.md#object-useability) | Enum / Object | The name of the ability the target is forced to use. | 1 | `GirlDinoPoop` (Enum), `Spit` (Enum), `{ ... }` (Object) |


### Object: `StatusEachTurnBeginIfHasStatus`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 1 | `[1 .5]` (Array), `-2` (Number), `3` (Number), `{ ... }` (Object) |
| `HealthGain` | Integer | The amount of health restored to the source. | 1 | `2*X` (Enum), `3*X` (Enum), `10` (Number), `4` (Number) |
| `animation` | Enum | Specifies the animation played when the ability is used. | 1 | `pulse3` (Enum) |
| `consume` | Boolean | If true, the status is consumed after triggering. | 1 | `true` (Boolean) |
| `status` | Enum || 1 | `Counterspell` (Enum) |


### Object: `StatusEachTurnEndIfEnabledAtStartOfTurn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object | The name of the ability the source is forced to use, optionally with a chance. | 1 | `neck_ChefsApron` (Enum), `T2UnClone` (Enum), `{ ... }` (Object) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 |


### Object: `StatusEveryXSpellCastsEachTurn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthGain` | Integer | The amount of health restored to the source. | 1 | `2*X` (Enum), `3*X` (Enum), `10` (Number), `4` (Number) |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `3` (Number) |


### Object: `StatusIfDidntMove`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Charge` | Integer | The number of charge stacks applied. | 1 | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |


### Object: `StatusIfUnusedActPoints`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 |
| [`BackflipWhenTargeted`](Abilities_and_Spells.md#object-backflipwhentargeted) | Enum / Integer / Object | The number of backflip charges, or an object defining its ability. | 1 | `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| [`Craft`](Abilities_and_Spells.md#object-craft) | Object | Specifies the loot pool and slot to craft an item for the source. | 1 | `{ ... }` (Object) |


### Object: `StatusOnBackstab`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthGain` | Integer | The amount of health restored to the source. | 1 | `2*X` (Enum), `3*X` (Enum), `10` (Number), `4` (Number) |
| `SerratedClaws` | Integer || 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |


### Object: `StatusOnBreak`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 20 |
| [`Bruise`](#object-bruise) | Array / Integer / Object | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 3 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| [`FindItemFromPool`](Abilities_and_Spells.md#object-finditemfrompool) | Enum / Object | Specifies the loot pool from which to find an item, with an optional chance. | 3 | `chapter_specific_item` (Enum), `chapter_common` (Enum), `{ ... }` (Object) |
| `HealthGain` | Integer | The amount of health restored to the source. | 3 | `2*X` (Enum), `3*X` (Enum), `10` (Number), `4` (Number) |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 3 | `[1 .5]` (Array), `4` (Number), `3` (Number), `{ ... }` (Object) |
| [`ApplyToRandomPartyMemberIfPossible`](Abilities_and_Spells.md#object-applytorandompartymemberifpossible) | Object | Contains an inner effect block that is applied to a random living party member if one exists. | 1 | `{ ... }` (Object) |
| `ConstitutionUp` | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 1 | `[1 .5]` (Array), `-1` (Number), `-2` (Number), `{ ... }` (Object) |
| `DexterityUp` | Enum / Integer | The amount of dexterity change, or a keyword like 'item_aux'. | 1 | `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `IntelligenceUp` | Enum / Integer | The amount of Intelligence added as a flat bonus. | 1 | `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 1 | `BestBud` (Enum), `Maggot` (Enum), `{ ... }` (Object) |
| `StrengthUp` | Enum / Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 1 | `[1 .5]` (Array), `4` (Number), `-2` (Number), `{ ... }` (Object) |


### Object: `StatusOnDie`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 9 |
| [`FindItemFromPool`](Abilities_and_Spells.md#object-finditemfrompool) | Enum / Object | Specifies the loot pool from which to find an item, with an optional chance. | 1 | `chapter_specific_item` (Enum), `chapter_common` (Enum), `{ ... }` (Object) |
| [`RandomMagicMissile`](Abilities_and_Spells.md#object-randommagicmissile) | Integer / Object | The number of random magic missiles fired, or an object defining its properties. | 1 | `[1 .5]` (Array), `10` (Number), `6` (Number), `{ ... }` (Object) |
| `RemoveAmbientLightEffects` | Number | The fade-out duration in seconds for ambient light effects. | 1 | `4` (Number), `.5` (String) |
| [`ScatterCoins`](Abilities_and_Spells.md#object-scattercoins) | Object | The number of coins (or [stacks, probability] array) to scatter on the ground; can also include stacking behavior and formula. | 1 | `[1 .5]` (Array), `5` (Number), `{ ... }` (Object) |


### Object: `StatusOnDodge`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DodgeChance_Status` | Integer | The flat percentage increase to dodge chance applied as a status effect. | 1 | `[1 .5]` (Array), `15` (Number), `66` (Number), `{ ... }` (Object) |


### Object: `StatusOnEnemyCastSpell`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `HealthGain` | Integer | The amount of health restored to the source. | 1 | `2*X` (Enum), `3*X` (Enum), `8` (Number), `10` (Number) |


### Object: `StatusOnEnemyConfused`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ImmediateUseAbility`](Engine_StatusAndPassiveKeys.md#object-immediateuseability) | Enum / Object | Specifies the name of an ability to be triggered instantly from this effect. | 1 | `cm_Lard_Impl` (Enum), `tk_ButterBean_Mega` (Enum), `{ ... }` (Object) |


### Object: `StatusOnEnemyDeath`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Charge` | Integer | The number of charge stacks applied. | 1 | `[1 .5]` (Array), `3` (Number), `4` (Number), `{ ... }` (Object) |


### Object: `StatusOnFallAsleep`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `FillMana` | Integer | The amount of mana restored, or an [amount, probability] array. | 1 | `[1 .25]` (Array), `[1 .10]` (Array), `1` (Number) |
| `HealRandomInjury` | Integer | The number of random injuries healed on the target. | 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |


### Object: `StatusOnFullMana`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_OncePerBattle`](Abilities_and_Spells.md#object-conditional_onceperbattle) | Object || 1 | `{ ... }` (Object) |


### Object: `StatusOnSetPieceBreak`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 |
| [`FindItemFromPool`](Abilities_and_Spells.md#object-finditemfrompool) | Enum / Object | Specifies the loot pool from which to find an item, with an optional chance. | 1 | `chapter_specific_item` (Enum), `consumables` (Enum), `{ ... }` (Object) |
| `PermanentCharisma` | Integer | The amount of permanent Charisma added to the unit's base stats. | 1 | `1` (Number), `2` (Number) |
| `PermanentConstitution` | Integer | The amount of permanent Constitution stat added or removed. | 1 | `-1` (Number), `-2` (Number) |
| `PermanentDexterity` | Integer | The permanent amount of dexterity added or removed. | 1 | `1` (Number), `2` (Number) |
| `PermanentIntelligence` | Integer | The permanent amount of intelligence added or removed. | 1 | `1` (Number), `2` (Number) |
| `PermanentLuck` | Integer | The amount of permanent Luck added to the unit's base stats. | 1 | `1` (Number), `2` (Number) |
| `PermanentSpeed` | Integer | The permanent amount of speed added or removed. | 1 | `1` (Number), `2` (Number) |
| `PermanentStrength` | Integer | The amount of permanent bonus strength (physical damage modifier) granted. | 1 | `1` (Number), `2` (Number) |
| `set` | Array / Enum | Specifies the set name(s) the item belongs to for set bonuses. | 1 | `Recycled` (Enum) |


### Object: `StatusOnSpawnIn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CaptureFamiliar` | Integer | The number of times to attempt to capture the target as a familiar. | 1 | `1` (Number) |
| `SetHealth` | Integer || 1 | `100` (Number), `50` (Number) |


### Object: `StatusOnTakeHealthOrShieldDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 |
| `DivineShield` | Array / Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 2 | `[1 .33]` (Array), `[1 .5]` (Array), `4` (Number), `1` (Number), `{ ... }` (Object) |
| [`Conditional_GoodRoll`](Abilities_and_Spells.md#object-conditional_goodroll) | Object | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 1 | `{ ... }` (Object) |
| [`Metronome`](Abilities_and_Spells.md#object-metronome) | Boolean (Flag) / Number / Object | The number of times Metronome triggers, or an object with stacks and banned abilities. | 1 | `(Flag)` (Boolean (Flag)), `1` (Number), `2` (Number), `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 |


### Object: `StatusOverlappingCharactersAndDie`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Poison` | Array / Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 1 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |


### Object: `StatusRandomEnemiesOnBattleStart`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Fear` | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 3 | `[1 .1]` (Array), `[1 .05]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| `Bleed` | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 1 | `[1 .1]` (Array), `[3 .1]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |
| `Charmed` | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 1 | `[1 .1+.02*cha]` (Array), `[1 .25]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| [`Confusion`](#object-confusion) | Array / Integer / Object | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 1 | `[2 .15]` (Array), `[1 .1]` (Array), `3` (Number), `4` (Number), `{ ... }` (Object) |
| `Freeze` | Array / Integer | The amount of freeze stacks applied, or an [stacks, probability] array. | 1 | `[1 .1]` (Array), `[1 0.15]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |


### Object: `StatusWhenStatusCompletelyRemoved`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`UseAbility`](Abilities_and_Spells.md#object-useability) | Enum / Object | The name of the ability the target is forced to use. | 1 | `GirlDinoPoop` (Enum), `TormentorRuneAbsorb` (Enum), `{ ... }` (Object) |
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
| `cleanse_on_apply` | Boolean | If true, removes any existing stun effect when this immunity is applied. | 1 | `false` (Boolean) |


### Object: `SupportDieInsteadOfRun`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alt_dead_ani` | Enum | Specifies the alternative death animation to use when the support unit dies instead of running. | 1 | `off` (Enum) |
| `alt_dying_ani` | Enum | Specifies the alternative dying animation to use. | 1 | `shutdown` (Enum) |


### Object: `SupportFormChangeInsteadOfRun`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `TVChangeDie` (Enum), `SBotAnger` (Enum) |
| `wait_till_turn` | Boolean | If true, the form change will not occur until the unit's next turn. | 1 | `true` (Boolean) |


### Object: `SwimmingFormChange`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `form_in` | Enum | Determines the form to change into when entering water. | 1 | `Water` (Enum) |
| `form_out` | Enum | Determines the form to change into when leaving water. | 1 | `Out` (Enum) |


### Object: `SyncFormsWithBuddy`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `no_buddy` | Enum | Specifies an alternative form to use when there is no buddy. | 1 | `Rage` (Enum) |


### Object: `T3HitlerSpawningPhase`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `spell_use_groups` | Array | List of spell use groups that the spawning phase can use. | 1 | `[[ T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk T3Spawn_Tank...]` (Array) |


### Object: `TVBotScreen`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Die`](Characters_and_Bosses.md#object-die) | Integer / Object | If set, kills the target immediately. | 1 | `6` (Number), `1` (Number), `{ ... }` (Object) |
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
| `move_ability` | Enum | Specifies the movement ability (e.g., BirdFly, TrampleMoveOne) used for the movement action. | 1 | `T2GoopRun` (Enum) |
| `move_weights` | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 | `stay_far_always_move` (Enum) |


### Object: `TerminatorChase`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `T1ChokeReaction` (Enum) |
| `move` | Enum | Specifies the name of the class's default movement ability. | 1 | `MoveOne` (Enum) |


### Object: `TerminatorSkin`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `groups` | Array | Groups of actors that this skin applies to. | 1 | `[{ stacks 48 ParticleBurst Gibs_terminatorskin CatPartsTransform { head 1057 }...]` (Array) |
| `status` | Enum || 1 | `Brace` (Enum) |


### Object: `Thorns`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `TinkererBasicAttackSwitching`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `craft_ability` | Enum | The ability used for the craft action in the Tinkerer's basic attack switching. | 3 | `TinkererCraft` (Enum) |
| `throw_ability` | Enum | The ability used for the throw action in the Tinkerer's basic attack switching. | 3 | `TinkererThrow` (Enum) |


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
| `object` | Array / Enum | Specifies the object or unit to be spawned. | 8 | `[YellowBlaster GreyAlien GreenProber Amoeba MoonWorm Waggle KirbyFetus BrainDrain Fetus FetusGusher]` (Array), `[Squirrel Crow Snake Turtle Toad Catepillar]` (Array), `HuskG` (Enum), `SkeletonCatRevivedFamiliar` (Enum) |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 8 | `3` (Number), `1` (Number) |
| `initiative` | Enum / Integer | The unit's turn order priority; can be an integer modifier or 'keep_turns_end_turn' to force end of turn after acting. | 4 | `keep_turns_end_turn` (Enum) |
| `animation` | Enum | Specifies the animation played when the ability is used. | 2 | `hatch` (Enum) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `[1 4]` (Array) |


### Object: `TransformItemOnElementInfluence`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `element` | Array / Enum || 5 | `Fire` (Enum), `Greater_Water` (Enum) |
| `full_repair` | Boolean || 5 | `true` (Boolean) |
| `item` | Enum || 5 | `WaterBottle_Full` (Enum), `GallonOfWater` (Enum) |


### Object: `TransformOnDeathImmediately`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `first_turn` | Enum | Determines when the spawned unit takes its first turn relative to the spawn event. | 4 | `keep_turns` (Enum) |
| `obj` | Array / Enum | Specifies one or more object names to bounce towards the target. | 4 | `TallSkeletonCatCorpse` (Enum), `SkeletonCatCorpseFamiliar` (Enum) |


### Object: `TransformOnElementInfluence`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `element` | Array / Enum || 9 | `Holy` (Enum), `Fire` (Enum) |
| `object` | Array / Enum | Specifies the object or unit to be spawned. | 9 | `CookedBiggestFood` (Enum), `CookedBait` (Enum) |


### Object: `TransformOnElementInfluencex`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `element` | Array / Enum || 2 | `Holy` (Enum) |
| `object` | Array / Enum | Specifies the object or unit to be spawned. | 2 | `Bait` (Enum), `PurifiedPoisonFood` (Enum) |


### Object: `TransformOnStatusThreshold`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `object` | Array / Enum | Specifies the object or unit to be spawned. | 1 | `Moth` (Enum) |
| `status` | Enum || 1 | `AllStatsUp` (Enum) |
| [`threshold`](Items_and_Equipment.md#object-threshold) | Enum / Integer / Object | The health threshold value, either as a formula using X (max health) or a fixed integer. | 1 | `5` (Number) |


### Object: `Trapper`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 4 | `RattleSnakeTrap` (Enum), `BloatSideLaser` (Enum) |
| `cancel_movement` | Boolean | If true, the trapper cancels the trapped unit's movement. | 2 | `false` (Boolean) |
| `pathfinding_avoidance` | Integer | The weight that makes other units avoid traversing this tile during pathfinding. | 2 | `250` (Number) |
| `range` | Enum / Integer | The distance in tiles for the trigger effect; `global` means any distance. | 2 | `10` (Number) |


### Object: `Triskaidekaphobia`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 |


### Object: `TunnelVision`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `crit_chance` | Number | The chance for the damage instance to critically hit, expressed as a percentage or equation; values above 1 default to 100%. | 1 | `50` (Number) |


### Object: `TwisterFling`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage` | Equation | Specifies the amount of damage dealt, can be a number or expression. | 1 | `5` (Equation) |
| `max_dist` | Integer | The maximum distance in tiles the target can be displaced by the knockback effect. | 1 | `5` (Number) |
| `min_dist` | Integer | The minimum distance in tiles the target must be displaced by the knockback effect. | 1 | `3` (Number) |


### Object: `UnlimitedDeathRattleRevive`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `MD_Lift` (Enum) |
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 1 | `true` (Boolean) |


### Object: `UseAbility`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `Destroyer2HolyAttack` (Enum), `T3Pebbles_BoulderDrop` (Enum) |
| `respect_prime` | Boolean || 2 | `true` (Boolean) |


### Object: `UseAbilityWhenOutOfStatus`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `QueenHippoHeartAttack` (Enum) |
| `status` | Enum || 1 | `Brace` (Enum) |


### Object: `Vegan`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 |


### Object: `Vengeful`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `Weakness`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `WobblyCat`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 |


### Object: `Zombie`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

