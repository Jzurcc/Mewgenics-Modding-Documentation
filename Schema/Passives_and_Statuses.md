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
| [`desc`](./Strings.md#string-desc) | Enum | Localization key for the passive's display description. | 2423 |  |
| [`name`](./Strings.md#string-name) | Enum | Localization key for the passive's display name. | 3307 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2985 |  |
| [`class`](./Enums.md#enum-class) | Enum | Character class identifier. | 600 |  |
| [`stats`](Characters_and_Bosses.md#object-stats) | Object || 461 ||
| [`AbilityReaction`](Characters_and_Bosses.md#object-abilityreaction) | Enum / Object || 2 | `SCSneakUp` (Enum), `attack` (Enum), `{ ... }` (Object) |
| [`AfterImage`](Abilities_and_Spells.md#object-afterimage) | Object || 1 | `PlayerCat_ThiefShade2` (Enum), `PlayerCat_ThiefShade` (Enum), `{ ... }` (Object) |
| [`AllyBonusAbilityAura`](Miscellaneous.md#object-allybonusabilityaura) | Enum / Object || 1 | `NubbyToss` (Enum), `{ ... }` (Object) |
| `AlphaCat` | Integer || 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `AmplifyStatus` | Enum || 4 | `Burn` (Enum), `Poison` (Enum), `{ ... }` (Object) |
| [`AutocastEachTurnBegin`](Miscellaneous.md#object-autocasteachturnbegin) | Enum / Object || 1 | `MindCrack_EldritchVisage2` (Enum), `MindCrack_EldritchVisage` (Enum), `{ ... }` (Object) |
| [`BackflipWhenTargeted`](Abilities_and_Spells.md#object-backflipwhentargeted) | Enum / Integer / Object || 1 | `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `BackstabCritChance` | Number || 1 | `1` (Number), `.25` (String) |
| [`BlastResistance`](#object-blastresistance) | Array / Number / Object || 3 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `BleedThorns` | Integer || 4 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Blind` | Array / Integer || 3 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`BoostDamageGlobalAura`](#object-boostdamageglobalaura) | Array / Number / Object || 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`BoostWeaponDamage`](Items_and_Equipment.md#object-boostweapondamage) | Object || 5 | `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`BraceForEachNeighboringEnemy`](#object-braceforeachneighboringenemy) | Array / Number / Object || 1 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `cha` | Enum / Integer || 89 ||
| [`ChainKnockback`](#object-chainknockback) | Number / Object || 1 | `1` (Number), `{ ... }` (Object) |
| [`ChanceToBlockAndCounter`](Items_and_Equipment.md#object-chancetoblockandcounter) | Integer / Object || 1 | `15` (Number), `33` (Number), `{ ... }` (Object) |
| [`ChanceToRevive`](Elite_Buffs.md#object-chancetorevive) | Integer / Object || 1 | `100` (Number), `25` (Number), `{ ... }` (Object) |
| [`CharmAllFlies`](#object-charmallflies) | Array / Number / Object || 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`CollectPickupsOnBattleEnd`](Miscellaneous.md#object-collectpickupsonbattleend) | Number / Object || 1 | `1` (Number), `{ ... }` (Object) |
| [`Conductor`](#object-conductor) | Boolean (Flag) / Number / Object || 1 | `(Flag)` (Boolean (Flag)), `2` (Number), `{ ... }` (Object) |
| [`ConjureBonusAbility`](Abilities_and_Spells.md#object-conjurebonusability) | Enum / Object || 1 | `Class` (Enum), `Mage` (Enum), `{ ... }` (Object) |
| [`CounterAttack`](Cat_Mutations.md#object-counterattack) | Array / Enum / Object || 2 | `[attack GSScream]` (Array), `Shove` (Enum), `YeticatSnowball_Counter` (Enum), `{ ... }` (Object) |
| `CritChanceUp` | Integer || 18 | `[1 .5]` (Array), `1` (Number), `50` (Number), `{ ... }` (Object) |
| [`DamageReductionAura`](Miscellaneous.md#object-damagereductionaura) | Array / Number / Object || 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`DeathChill`](#object-deathchill) | Number / Object || 1 | `1` (Number), `{ ... }` (Object) |
| [`DeathRattle`](Characters_and_Bosses.md#object-deathrattle) | Enum / Object || 1 | `BoomerCatExplode` (Enum), `BombFlyExplode` (Enum), `{ ... }` (Object) |
| [`DejaVu`](#object-dejavu) | Number / Object || 1 | `10` (Number), `{ ... }` (Object) |
| `DepressionAura` | Integer || 1 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`DirtyClaws`](#object-dirtyclaws) | Number / Object || 1 | `1` (Number), `{ ... }` (Object) |
| [`DukeOfFlies`](#object-dukeofflies) | Number / Object || 1 | `1` (Number), `{ ... }` (Object) |
| [`Empath`](#object-empath) | Number / Object || 1 | `50` (Number), `100` (Number), `{ ... }` (Object) |
| [`EnergyStorm`](Miscellaneous.md#object-energystorm) | Number / Object || 1 | `3` (Number), `{ ... }` (Object) |
| [`FlyDamageIncrease`](Items_and_Equipment.md#object-flydamageincrease) | Object || 1 | `[1 .5]` (Array), `1` (Number), `4` (Number), `{ ... }` (Object) |
| `Flying` | Integer || 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`FollowUp`](#object-followup) | Enum / Object || 1 | `FollowUpDash` (Enum), `FollowUpDash2` (Enum), `{ ... }` (Object) |
| [`FullPower`](#object-fullpower) | Number / Object || 1 | `3` (Number), `{ ... }` (Object) |
| [`HealingAura`](#object-healingaura) | Number / Object || 1 | `1` (Number), `{ ... }` (Object) |
| `Immobile` | Array / Integer || 2 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `10` (Number), `{ ... }` (Object) |
| [`ImmortalLeeches`](#object-immortalleeches) | Number / Object || 1 | `1` (Number), `{ ... }` (Object) |
| [`KillsHeal`](#object-killsheal) | Number / Object || 1 | `5` (Number), `50` (Number), `{ ... }` (Object) |
| `KineticSpikes` | Integer || 3 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`LateBloomer`](Miscellaneous.md#object-latebloomer) | Array / Number / Object || 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `LineOfSightTrueSightAura` | Number / String || 1 | `0` (Number), `.5` (String) |
| [`LowHealthAllyDodgeChanceAura`](Miscellaneous.md#object-lowhealthallydodgechanceaura) | Array / Number / Object || 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`MegaMinions`](Miscellaneous.md#object-megaminions) | Number / Object || 1 | `3` (Number), `{ ... }` (Object) |
| `Metal` | Integer || 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`MetalDetector`](#object-metaldetector) | Number / Object || 1 | `5` (Number), `10` (Number), `{ ... }` (Object) |
| `MissChance` | Integer || 12 | `[1 .5]` (Array), `1` (Number), `20` (Number), `{ ... }` (Object) |
| [`MoveAwayFromDamageSource`](Characters_and_Bosses.md#object-moveawayfromdamagesource) | Object || 1 | `MoveOne` (Enum), `BasicJump` (Enum), `{ ... }` (Object) |
| `MoveQuivered` | Integer || 3 | `[1 0.1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`MoveTowardsDamageSource`](Characters_and_Bosses.md#object-movetowardsdamagesource) | Enum / Object || 1 | `MoveOne` (Enum), `{ ... }` (Object) |
| [`MoveWhenDamaged`](Cat_Mutations.md#object-movewhendamaged) | Enum / Object || 1 | `TKNG_Hop` (Enum), `move` (Enum), `{ ... }` (Object) |
| [`NumbingLeeches`](#object-numbingleeches) | Number / Object || 1 | `3` (Number), `{ ... }` (Object) |
| `PoisonThorns` | Integer || 3 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`PoopWhenHit`](Items_and_Equipment.md#object-poopwhenhit) | Object || 2 | `Poop` (Enum), `{ ... }` (Object) |
| [`ProtectTargetedAllies`](Characters_and_Bosses.md#object-protecttargetedallies) | Object || 1 | `SwapPositions_WideLoad2` (Enum), `SwapPositions_WideLoad` (Enum), `{ ... }` (Object) |
| [`Quiver`](#object-quiver) | Number / Object || 1 | `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Quivered` | Array / Integer || 5 | `[1 0.1]` (Array), `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `RandomStatUp` | Integer / String || 1 | `"ceil(X/3)"` (Enum), `"ceil(X/2)"` (Enum), `2` (Number), `-5` (Number) |
| [`ReflectProjectiles`](Characters_and_Bosses.md#object-reflectprojectiles) | Integer / Object || 2 | `1` (Number), `100` (Number), `{ ... }` (Object) |
| [`Robot`](Characters_and_Bosses.md#object-robot) | Integer / Object || 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`SharePickups`](Characters_and_Bosses.md#object-sharepickups) | Object || 1 | `1` (Number), `{ ... }` (Object) |
| [`ShoulderCheck`](#object-shouldercheck) | Number / Object || 1 | `100` (Number), `33` (Number), `{ ... }` (Object) |
| [`ShovingMatch`](#object-shovingmatch) | Enum / Object || 1 | `attack` (Enum), `{ ... }` (Object) |
| `SizeScale` | Number || 2 | `1.1` (Number), `1.3` (Number), `.6` (String), `.75` (String) |
| [`SpawnExtraThingsOnBattleStart`](Cat_Mutations.md#object-spawnextrathingsonbattlestart) | Object || 1 | `{ ... }` (Object) |
| [`SpawnObjectOnPopCorpse`](Items_and_Equipment.md#object-spawnobjectonpopcorpse) | Enum / Object || 1 | `Coin` (Enum), `Catnip` (Enum), `{ ... }` (Object) |
| [`SpawnOnBattleStart`](Elite_Buffs.md#object-spawnonbattlestart) | Enum / Object || 9 | `ZombieCatFamiliar` (Enum), `BeefyCharmedLeech` (Enum), `{ ... }` (Object) |
| `spd` | Enum / Integer || 78 ||
| `shield` | Enum / Integer || 191 ||
| `con` | Enum / Integer || 79 ||
| `int` | Enum / Integer || 66 ||
| `lck` | Enum / Integer || 53 ||
| `StatusImmunity` | Array / Enum || 4 | `[Burn]` (Array), `[Freeze Slow]` (Array), `Burn` (Enum), `Webbed` (Enum) |
| `Stealth` | Array / Integer || 1 | `[1 .1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `str` | Enum / Integer || 45 ||
| `dex` | Enum / Integer || 30 ||
| [`keyword_tooltips`](Abilities_and_Spells.md#object-keyword_tooltips) | Object | Examples: `{ ... }` | 28 ||
| `divine_shield` | Integer | Examples: `3, 1` | 20 ||
| [`lock_item_slot`](Miscellaneous.md#object-lock_item_slot) | Object || 16 ||
| [`name_mod`](./Strings.md#string-name_mod) | String || 11 ||
| [`desc_multiclass`](./Strings.md#string-desc_multiclass) | String || 5 ||
| [`override_basic_attack`](./Enums.md#enum-override_basic_attack) | Enum || 6 ||
| `auto_plus_signs_on_name` | Boolean || 4 ||
| [`bonus_items`](./Arrays.md#array-bonus_items) | Array | Flat addition to a base value. | 5 ||
| [`empty_armor_scaled_stats`](Miscellaneous.md#object-empty_armor_scaled_stats) | Object | Examples: `{ ... }` | 2 ||
| [`tags`](./Arrays.md#array-tags) | Array / Enum || 241 ||
| [`schadenfreude_scaled_stats`](Miscellaneous.md#object-schadenfreude_scaled_stats) | Object | Examples: `{ ... }` | 1 ||
| [`grant_ability`](./Enums.md#enum-grant_ability) | Enum || 1 ||
| [`StrengthForEachNeighboringEnemy`](#object-strengthforeachneighboringenemy) | Array / Number / Object || 1 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`StrengthInNumbersAura`](Miscellaneous.md#object-strengthinnumbersaura) | Number / Object || 1 | `1` (Number), `{ ... }` (Object) |
| [`Study`](Miscellaneous.md#object-study) | Number / Object || 1 | `1` (Number), `{ ... }` (Object) |
| `SwapHighestAndLowestStat` | Integer || 1 | `1` (Number) |
| `Tech` | Integer || 1 | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `Thorns` | Integer || 18 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`TileDamageMultiplier`](Miscellaneous.md#object-tiledamagemultiplier) | Number / Object || 1 | `2` (Number), `{ ... }` (Object) |
| `Trample` | Integer || 7 | `[1 .5]` (Array), `[3 X-8]` (Array), `1` (Number), `6` (Number), `{ ... }` (Object) |
| [`Vegan`](#object-vegan) | Number / Object || 2 | `1` (Number), `{ ... }` (Object) |
| [`Vengeful`](#object-vengeful) | Number / Object || 1 | `1` (Number), `{ ... }` (Object) |
| [`Weakness`](#object-weakness) | Array / Integer / Object || 1 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `YOffset` | Number || 3 | `-.18` (String), `.25` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1910 ||

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
| [`AbilityOnBattleStart`](./Enums.md) | Enum || 11 | neck_ChefsApron |
| [`AbilityReaction`](Characters_and_Bosses.md#object-abilityreaction) | Enum / Object || 23 | PissYourself |
| [`AbilityWhenTaggedCharacterMovesNear`](Cat_Mutations.md#object-abilitywhentaggedcharactermovesnear) | Object || 3 ||
| [`AbsorbManaAura`](./Enums.md) | Integer || 1 | 1 |
| [`AddAllyNeighborsToAttackRange`](./Enums.md) | Integer || 1 | 1 |
| [`AddBonusMeleeRange`](./Enums.md) | Integer || 5 | 2 |
| [`AddBonusRange`](./Enums.md) | Integer || 15 | 2 |
| [`AddCorpseHealth`](./Enums.md) | Integer || 14 | 96 |
| [`AddCritMultiplier`](./Enums.md) | Integer || 4 | 200 |
| [`AddDamageToBasicAttack`](./Enums.md) | Integer || 2 | 2 |
| [`AddDamageToElementDamage`](Cat_Mutations.md#object-adddamagetoelementdamage) | Object || 6 ||
| [`AddElementsToBasicAttack`](./Enums.md) | Enum || 7 | Ice |
| [`AddHiddenTag`](./Enums.md) | Enum || 5 | bowling_ball |
| [`AddInitiative`](./Enums.md) | Integer || 7 | -100 |
| [`AddKnockbackDamage`](./Enums.md) | Integer || 4 | 2 |
| [`AddLevelUpRerolls`](./Enums.md) | Integer || 10 | 2 |
| [`AddLevelUpStatMultiplier`](./Enums.md) | Integer || 1 | 1 |
| [`AddManaRegen`](./Enums.md) | Integer || 13 | 7 |
| [`AddMovement`](./Enums.md) | Integer || 20 | 20 |
| [`AddPassiveToSpawnedRocks`](Miscellaneous.md#object-addpassivetospawnedrocks) | Object || 1 ||
| [`AddPassivesToCharmed`](Items_and_Equipment.md#object-addpassivestocharmed) | Object || 3 ||
| [`AddPassivesToMinions`](Items_and_Equipment.md#object-addpassivestominions) | Object || 21 ||
| [`AddPassivesToSummonAbilityMinions`](Miscellaneous.md#object-addpassivestosummonabilityminions) | Object || 1 ||
| [`AddSelfStatusToBasicAttack`](Items_and_Equipment.md#object-addselfstatustobasicattack) | Object || 9 ||
| [`AddSelfStatusToWeapons`](Items_and_Equipment.md#object-addselfstatustoweapons) | Object || 2 ||
| [`AddSpellDamage`](./Enums.md) | Integer || 1 | 2 |
| [`AddStartingMana`](./Enums.md) | Integer || 2 | 20 |
| [`AddStatusToAllDamage`](Items_and_Equipment.md#object-addstatustoalldamage) | Object || 11 ||
| [`AddStatusToBasicAttack`](Abilities_and_Spells.md#object-addstatustobasicattack) | Object || 133 ||
| [`AddStatusToBasicAttackWithCooldown`](Miscellaneous.md#object-addstatustobasicattackwithcooldown) | Object || 1 ||
| [`AddStatusToBasicMeleeAttack`](Cat_Mutations.md#object-addstatustobasicmeleeattack) | Object || 3 ||
| [`AddStatusToElementAbilities`](Miscellaneous.md#object-addstatustoelementabilities) | Object || 3 ||
| [`AddStatusToElementDamage`](Items_and_Equipment.md#object-addstatustoelementdamage) | Object || 4 ||
| [`AddStatusToExplosions`](Miscellaneous.md#object-addstatustoexplosions) | Object || 1 ||
| [`AddStatusToFirstBasicAttack`](Miscellaneous.md#object-addstatustofirstbasicattack) | Object || 1 ||
| [`AddStatusToKnockbackDamage`](Items_and_Equipment.md#object-addstatustoknockbackdamage) | Object || 2 ||
| [`AddStatusToMeleeDamage`](Miscellaneous.md#object-addstatustomeleedamage) | Object || 1 ||
| [`AddStatusToReceivedDamage_ExcludeStatuses`](Miscellaneous.md#object-addstatustoreceiveddamage_excludestatuses) | Object || 1 ||
| [`AddStatusToSpells`](Characters_and_Bosses.md#object-addstatustospells) | Object || 3 ||
| [`AddStatusToTrampleDamage`](Characters_and_Bosses.md#object-addstatustotrampledamage) | Object || 1 ||
| [`AddStatusToWeapons`](Characters_and_Bosses.md#object-addstatustoweapons) | Object || 4 ||
| [`AddStatusesIfPersistentWeatherElement`](Miscellaneous.md#object-addstatusesifpersistentweatherelement) | Object || 1 ||
| [`AddStatusesToReceivedElementalDamage`](Miscellaneous.md#object-addstatusestoreceivedelementaldamage) | Object || 1 ||
| [`AddTag`](./Enums.md) | Enum || 9 | rock |
| [`AddTemporaryEffectsToBasicAttack`](Cat_Mutations.md#object-addtemporaryeffectstobasicattack) | Object || 4 ||
| [`AddUnfilledMaxHealth`](./Enums.md) | Integer || 2 | 20 |
| [`AddWeaponScaling`](./Enums.md) | Integer || 1 | 1 |
| [`AfterImage`](./Enums.md) | Enum || 1 | PlayerCat_ThiefShade2 |
| [`AllStatsUp`](./Enums.md) | Array / Integer || 14 | [.5] |
| [`AllowPassTurn`](./Enums.md) | Integer || 1 | 0 |
| [`AllyBonusAbilityAura`](Miscellaneous.md#object-allybonusabilityaura) | Enum / Object || 3 | NubbyToss |
| [`AllyDamageReaction`](./Enums.md) | Enum || 1 | attack |
| [`AllyDamageReduction`](./Enums.md) | Integer || 2 | 0 |
| [`AllyHealthRegenAura`](Miscellaneous.md#object-allyhealthregenaura) | Object || 1 ||
| [`AllyManaRegenAura`](Miscellaneous.md#object-allymanaregenaura) | Object || 2 ||
| [`AllyMoveAbilityAura`](./Enums.md) | Enum || 1 | CatapultJump2 |
| [`AllyMultiplyKnockbackDamage`](./Enums.md) | Integer || 1 | 2 |
| [`AlphaCat`](./Enums.md) | Integer || 1 | 1 |
| [`AlphaTurns`](./Enums.md) | Integer || 7 | -1 |
| [`AlternateCraftingPools`](Miscellaneous.md#object-alternatecraftingpools) | Object || 1 ||
| [`AmplifyKnockback`](./Enums.md) | Integer || 3 | 2 |
| [`AmplifyPositiveStatus`](./Enums.md) | Integer || 1 | 2 |
| [`AmplifyStatus`](Miscellaneous.md#object-amplifystatus) | Enum / Object || 6 | Poison |
| [`ApplyStatusesToRandomEnemiesEachTurn`](Items_and_Equipment.md#object-applystatusestorandomenemieseachturn) | Object || 3 ||
| [`ArmorDodgeChance`](./Enums.md) | Integer || 19 | 10 |
| [`Autism`](Miscellaneous.md#object-autism) | Object || 1 ||
| [`AutoCritLowDamage`](./Enums.md) | Integer || 1 | 2 |
| [`AutoEquipConsumables`](./Enums.md) | Integer || 3 | 1 |
| [`AutocastEachRound`](Abilities_and_Spells.md#object-autocasteachround) | Object || 5 ||
| [`AutocastEachTurn`](./Enums.md) | Enum || 2 | ViolentOutburst |
| [`AutocastEachTurnBegin`](Miscellaneous.md#object-autocasteachturnbegin) | Enum / Object || 2 | MindCrack_EldritchVisage |
| [`BackstabCritChance`](./Enums.md) | Integer || 5 | 1 |
| [`BackstabImmunity`](./Enums.md) | Integer || 9 | 1 |
| [`BackstabWeakness`](./Enums.md) | Number || 1 | 0.75 |
| [`BasicAttackAOEBonus`](./Enums.md) | Integer || 2 | 2 |
| [`BasicAttackCritChance`](./Enums.md) | Integer || 3 | 100 |
| [`BasicAttackDamageMultiplier`](./Enums.md) | Number || 3 | 33.333334 |
| [`BasicAttackStatusCarefulness`](./Enums.md) | Integer || 1 | 1 |
| [`BlacklistPickupType`](./Enums.md) | Enum || 1 | food |
| [`BlastResistance`](./Enums.md) | Integer || 4 | 2 |
| [`Bleed`](./Enums.md) | Array / Integer || 7 | [.1] |
| [`BleedThorns`](./Enums.md) | Integer || 11 | 2 |
| [`BonusAbility`](./Enums.md) | Enum || 7 | FighterBonusThrow |
| [`BonusFoodEachBattle`](./Enums.md) | Integer || 1 | 2 |
| [`BoobyTrapItems`](Miscellaneous.md#object-boobytrapitems) | Object || 1 ||
| [`BoostAllyStatsOnDeath`](./Enums.md) | Integer || 1 | 2 |
| [`BoostDamageAura`](./Enums.md) | Integer || 1 | 1 |
| [`BoostHeals`](./Enums.md) | Integer || 8 | -2 |
| [`BoostRangeAura`](./Enums.md) | Integer || 1 | 1 |
| [`BoostWeaponDamage`](Items_and_Equipment.md#object-boostweapondamage) | Integer / Object || 4 | 2 |
| [`BouncyProjectiles`](Items_and_Equipment.md#object-bouncyprojectiles) | Object || 2 ||
| [`Brace`](./Enums.md) | Integer || 94 | 2 |
| [`BraceForEachNeighboringEnemy`](./Enums.md) | Integer || 1 | 2 |
| [`Bruise`](./Enums.md) | Integer || 9 | 2 |
| [`BuffImmunity`](./Enums.md) | Integer || 4 | 1 |
| [`Burn`](./Enums.md) | Enum / Integer || 5 | 2 |
| [`CCImmunity`](./Enums.md) | Integer || 2 | 1 |
| [`CanRemoveCursedItems`](./Enums.md) | Integer || 2 | 1 |
| [`CantDodge`](./Enums.md) | Integer || 1 | 1 |
| [`CapDamageFromAllies`](./Enums.md) | Integer || 1 | 1 |
| [`CapMovementAbilityRange`](./Enums.md) | Integer || 2 | 1 |
| [`CatAPultAnimation`](Miscellaneous.md#object-catapultanimation) | Object || 1 ||
| [`CatchProjectiles`](Items_and_Equipment.md#object-catchprojectiles) | Object || 4 ||
| [`ChainKnockback`](./Enums.md) | Integer || 1 | 1 |
| [`ChanceToBackflip`](Cat_Mutations.md#object-chancetobackflip) | Object || 4 ||
| [`ChanceToBlockAndCounter`](./Enums.md) | Integer || 3 | 33 |
| [`ChanceToRevive`](Elite_Buffs.md#object-chancetorevive) | Integer / Object || 8 | 25 |
| [`ChangeTauntPriority`](./Enums.md) | Integer || 2 | -1 |
| [`CharmAllFlies`](./Enums.md) | Integer || 1 | 1 |
| [`ClassManaCostReduction`](Cat_Mutations.md#object-classmanacostreduction) | Object || 5 ||
| [`CobraReflex`](./Enums.md) | Enum || 1 | BasicMonkMelee |
| [`CoinsAddDamage`](./Enums.md) | Integer || 1 | 2 |
| [`CollectPickupsOnBattleEnd`](Miscellaneous.md#object-collectpickupsonbattleend) | Integer / Object || 1 | 1 |
| [`Conductor`](./Enums.md) | Integer || 1 | 2 |
| [`ConfusionEffectOnTaggedAbilities`](./Enums.md) | Enum || 1 | consumable |
| [`ConjureCastSpellsForAllies`](./Enums.md) | Integer || 1 | 2 |
| [`ConsumableEffectsMultiplierBonus`](./Enums.md) | Integer || 2 | 1 |
| [`ConsumablesInfiniteRange`](./Enums.md) | Integer || 1 | 1 |
| [`ConsumablesMeleeRange`](./Enums.md) | Integer || 1 | 1 |
| [`CounterAttack`](./Enums.md) | Enum || 34 | ReflexPunchJab |
| [`CritChanceUp`](./Enums.md) | Integer || 16 | 80 |
| [`CritsApplyStatus`](Items_and_Equipment.md#object-critsapplystatus) | Object || 5 ||
| [`DamageEnemiesOnHeal`](./Enums.md) | Integer || 1 | 2 |
| [`DamageEnemiesOnKill`](./Enums.md) | Integer || 1 | 2 |
| [`DamageIfDidntUseSpecificAbility`](Miscellaneous.md#object-damageifdidntusespecificability) | Object || 1 ||
| [`DamageNeighborTilesWhenCastSpell`](Miscellaneous.md#object-damageneighbortileswhencastspell) | Object || 1 ||
| [`DamageNeighborsAfterMove`](Elite_Buffs.md#object-damageneighborsaftermove) | Object || 3 ||
| [`DamageNeighborsOnEndMove`](Miscellaneous.md#object-damageneighborsonendmove) | Object || 7 ||
| [`DamageReductionAura`](Miscellaneous.md#object-damagereductionaura) | Object || 1 ||
| [`DamageUp`](./Enums.md) | Integer || 21 | 2 |
| [`DeathChill`](./Enums.md) | Integer || 1 | 1 |
| [`DeathRattle`](Characters_and_Bosses.md#object-deathrattle) | Enum / Object || 35 | BoomerCatExplode |
| [`DebuffImmunity`](./Enums.md) | Integer || 7 | 1 |
| [`DejaVu`](./Enums.md) | Integer || 1 | 10 |
| [`DepressionAura`](./Enums.md) | Integer || 9 | 2 |
| [`Diabetes`](Miscellaneous.md#object-diabetes) | Object || 1 ||
| [`DirtyClaws`](./Enums.md) | Integer || 1 | 1 |
| [`DisableAbilities`](./Enums.md) | Enum || 2 | all_items |
| [`DisableAbilitiesWithTag`](./Enums.md) | Enum || 1 | meat |
| [`DodgeChance`](./Enums.md) | Integer || 14 | 50 |
| [`Doomed`](./Enums.md) | Integer || 1 | 3 |
| [`DoubleCastWeapons`](./Enums.md) | Integer || 2 | 2 |
| [`DukeOfFlies`](./Enums.md) | Integer || 1 | 1 |
| [`Dyslexia`](./Enums.md) | Array || 1 | [3] |
| [`EMP`](Miscellaneous.md#object-emp) | Object || 1 ||
| [`ElementImmune`](./Enums.md) | Enum || 39 | Ice |
| [`ElementalAttunement`](Miscellaneous.md#object-elementalattunement) | Object || 1 ||
| [`ElementalManaCostReduction`](Items_and_Equipment.md#object-elementalmanacostreduction) | Object || 3 ||
| [`Empath`](./Enums.md) | Integer || 1 | 50 |
| [`EnemiesGetPickupsKnockedOut`](./Enums.md) | Integer || 1 | 2 |
| [`EnergyStorm`](Miscellaneous.md#object-energystorm) | Integer / Object || 1 | 3 |
| [`EquipTemporaryItem`](./Enums.md) | Enum || 4 | FoodMedium |
| [`EquipmentPassiveMultiplierBonus`](./Enums.md) | Integer || 1 | 1 |
| [`EquipmentSetBonusBonus`](./Enums.md) | Integer || 1 | 2 |
| [`EscapeSequence`](Miscellaneous.md#object-escapesequence) | Object || 1 ||
| [`Eternal`](Items_and_Equipment.md#object-eternal) | Object || 2 ||
| [`ExhaustionRoundChange`](./Enums.md) | Integer || 1 | 3 |
| [`ExplodeOverkilledEnemies`](./Enums.md) | Integer || 1 | 2 |
| [`ExplosionImmunity`](./Enums.md) | Integer || 1 | 1 |
| [`ExtraBasicAttacks`](./Enums.md) | Integer || 11 | 2 |
| [`ExtraBasicMoves_Status`](./Enums.md) | Integer || 3 | 1 |
| [`ExtraInjuryOnDeath`](./Enums.md) | Integer || 1 | 1 |
| [`ExtraMovePoints`](./Enums.md) | Integer || 3 | 1 |
| [`ExtraStatusWhenDealingDamage`](Items_and_Equipment.md#object-extrastatuswhendealingdamage) | Object || 4 ||
| [`ExtraTrinketUses`](./Enums.md) | Integer || 1 | 1 |
| [`ExtraWeaponAttacks`](./Enums.md) | Integer || 6 | 2 |
| [`FaceArmorPassiveMultiplierBonus`](./Enums.md) | Integer || 4 | 2 |
| [`FaceShield`](./Enums.md) | Integer || 5 | 0 |
| [`FamiliarSecondaryDamageImmunity`](./Enums.md) | Integer || 1 | 1 |
| [`FlowerPowerAuraBrace`](./Enums.md) | Integer || 1 | 1 |
| [`FlowerPowerAuraStrength`](./Enums.md) | Integer || 1 | 1 |
| [`FlowersOnEndTurn`](./Enums.md) | Integer || 3 | 3 |
| [`FlyDamageIncrease`](./Enums.md) | Integer || 2 | 4 |
| [`Flying`](./Enums.md) | Integer || 9 | 1 |
| [`FollowUp`](./Enums.md) | Enum || 1 | FollowUpDash2 |
| [`ForceSpecificInjury`](./Enums.md) | Enum || 4 | int |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object || 1 | Hallucinate_Disorder |
| [`FreePathfindElement`](./Enums.md) | Enum || 2 | Grass |
| [`FreeSpellsAtFullMana`](./Enums.md) | Integer || 1 | 1 |
| [`FreezePiercing`](./Enums.md) | Integer || 4 | 1 |
| [`FrontstabBasicAttackCritChance`](./Enums.md) | Integer || 1 | 100 |
| [`FullHeal`](./Enums.md) | Integer || 1 | 1 |
| [`FullHealthCritChance`](./Enums.md) | Integer || 1 | 100 |
| [`FullPower`](./Enums.md) | Integer || 1 | 3 |
| [`FurnitureStats`](Miscellaneous.md#object-furniturestats) | Object || 1 ||
| [`GainExtraShield`](./Enums.md) | Integer || 2 | 2 |
| [`GravityWell`](Miscellaneous.md#object-gravitywell) | Object || 1 ||
| [`HPGainBlock`](./Enums.md) | Integer || 2 | 1 |
| [`HeadArmorPassiveMultiplierBonus`](./Enums.md) | Integer || 5 | 2 |
| [`HealDamagesEnemies`](./Enums.md) | Integer || 1 | 1 |
| [`HealsAlsoRegenMana`](./Enums.md) | Integer || 1 | 2 |
| [`HealsCanRevive`](./Enums.md) | Integer || 1 | 3 |
| [`HealthRegenUp`](./Enums.md) | Integer || 52 | 2 |
| [`HolyShieldTransferToTaggedMinions`](./Enums.md) | Enum || 1 | any |
| [`HouseFoodRequirementMultiplier`](./Enums.md) | Integer || 1 | 0 |
| [`Hypomania`](./Enums.md) | Integer || 1 | 3 |
| [`IgnoreTiles`](./Enums.md) | Integer || 6 | 1 |
| [`ImmortalLeeches`](./Enums.md) | Integer || 1 | 1 |
| [`IncreaseExplosionDamage`](./Enums.md) | Integer || 4 | 2 |
| [`IncreaseExplosionSize`](./Enums.md) | Integer || 4 | 2 |
| [`IncreaseHealingSpellRange`](./Enums.md) | Integer || 1 | 2 |
| [`IncreaseSpellRange`](./Enums.md) | Integer || 3 | 5 |
| [`InfiniteRebirth`](Characters_and_Bosses.md#object-infiniterebirth) | Object || 2 ||
| [`InjuryImmunity`](./Enums.md) | Integer || 5 | 1 |
| [`InnateElement`](./Enums.md) | Enum || 14 | Ice |
| [`InvertBrainFaction`](./Enums.md) | Integer || 1 | 1 |
| [`KillsHeal`](./Enums.md) | Integer || 1 | 50 |
| [`KillsToMeat`](./Enums.md) | Enum || 3 | Food |
| [`KnockbackImmunity`](./Enums.md) | Integer || 5 | 1 |
| [`LateBloomer`](Miscellaneous.md#object-latebloomer) | Object || 1 ||
| [`LevelUpClassOverride`](./Enums.md) | Enum || 4 | Jester |
| [`LightningAspectCharge`](./Enums.md) | Integer || 1 | 0 |
| [`LightningRod`](Miscellaneous.md#object-lightningrod) | Object || 1 ||
| [`LimitDamage`](./Enums.md) | Integer || 10 | 1 |
| [`LimitHeal`](./Enums.md) | Integer || 9 | 1 |
| [`LimitSelfKnockbackDamage`](./Enums.md) | Integer || 1 | 1 |
| [`LimitedTileTrail`](./Enums.md) | Enum || 1 | FlowerTile |
| [`LineOfSightTrueSightAura`](./Enums.md) | Number || 1 | 0 |
| [`LobbedHook`](./Enums.md) | Integer || 1 | 2 |
| [`LowHealthAllyDodgeChanceAura`](Miscellaneous.md#object-lowhealthallydodgechanceaura) | Object || 1 ||
| [`Madness`](./Enums.md) | Integer || 1 | 1 |
| [`MakeBasicAttackPassThroughThings`](./Enums.md) | Integer || 1 | 1 |
| [`MakeSpellsRequireCharge`](./Enums.md) | Integer || 4 | 1 |
| [`ManaCostReduction`](./Enums.md) | Integer || 7 | 2 |
| [`ManaCostReductionTagged`](Miscellaneous.md#object-manacostreductiontagged) | Object || 2 ||
| [`ManaRegenMultiplierIfManaEmpty`](./Enums.md) | Integer || 1 | 2 |
| [`MaxAccuracy`](./Enums.md) | Integer || 1 | 1 |
| [`MaxStartingMana`](./Enums.md) | Integer || 1 | 1 |
| [`MegaMinions`](Miscellaneous.md#object-megaminions) | Integer / Object || 1 | 3 |
| [`MeleeRevengeDamage`](Abilities_and_Spells.md#object-meleerevengedamage) | Object || 59 ||
| [`Metal`](./Enums.md) | Integer || 90 | 1 |
| [`MetalDetector`](./Enums.md) | Integer || 1 | 5 |
| [`MinimumTech`](./Enums.md) | Integer || 1 | 1 |
| [`MissChance`](./Enums.md) | Integer || 9 | 15 |
| [`MoveAndUseAbilityEachTurnBeginIfPossible`](./Enums.md) | Enum || 3 | EatShit |
| [`MoveAwayFromDamageSource`](./Enums.md) | Enum || 2 | MoveOne |
| [`MoveQuivered`](./Enums.md) | Integer || 3 | 2 |
| [`MoveSpeedMultiplier`](./Enums.md) | Number || 2 | .5 |
| [`MoveTowardsDamageSource`](Characters_and_Bosses.md#object-movetowardsdamagesource) | Object || 10 ||
| [`MoveWhenDamaged`](Cat_Mutations.md#object-movewhendamaged) | Object || 11 ||
| [`MovementReaction`](Characters_and_Bosses.md#object-movementreaction) | Object || 9 ||
| [`MulticlassLevelUp`](./Enums.md) | Enum || 12 | Druid |
| [`NeckArmorPassiveMultiplierBonus`](./Enums.md) | Integer || 3 | 2 |
| [`NoManaRegen`](./Enums.md) | Integer || 1 | 1 |
| [`NoReflection`](./Enums.md) | Integer || 1 | 1 |
| [`NubbyTossPriority`](./Enums.md) | Integer || 2 | 1 |
| [`NumbingLeeches`](./Enums.md) | Integer || 1 | 3 |
| [`OverhealGainsBothShield`](./Enums.md) | Integer || 1 | 2 |
| [`OverrideBasicAttack`](./Enums.md) | Enum || 7 | GerdShot |
| [`OverrideMaxHealth`](./Enums.md) | Integer || 7 | 1 |
| [`OverrideMaxMana`](./Enums.md) | Integer || 1 | 1 |
| [`OverridePalette`](./Enums.md) | Integer || 1 | 87 |
| [`Paranoia`](./Enums.md) | Enum || 1 | ParanoiaBasicMelee |
| [`ParasitesArentCursed`](./Enums.md) | Integer || 1 | 1 |
| [`PassiveAfterXKills`](Items_and_Equipment.md#object-passiveafterxkills) | Object || 3 ||
| [`PassiveAtFullHealth`](Miscellaneous.md#object-passiveatfullhealth) | Object || 1 ||
| [`PassiveAtHealthThreshold`](Items_and_Equipment.md#object-passiveathealththreshold) | Object || 7 ||
| [`PassiveAtInjuryThreshold`](Miscellaneous.md#object-passiveatinjurythreshold) | Object || 1 ||
| [`PassiveAtStatThreshold`](Items_and_Equipment.md#object-passiveatstatthreshold) | Object || 7 ||
| [`PassiveIfAllArmorEmpty`](Miscellaneous.md#object-passiveifallarmorempty) | Object || 4 ||
| [`PassiveIfEmptyFace`](Miscellaneous.md#object-passiveifemptyface) | Object || 3 ||
| [`PassiveIfEmptyHead`](Miscellaneous.md#object-passiveifemptyhead) | Object || 3 ||
| [`PassiveIfEmptyNeck`](Miscellaneous.md#object-passiveifemptyneck) | Object || 3 ||
| [`PassiveLevelScaledStatus`](Miscellaneous.md#object-passivelevelscaledstatus) | Object || 1 ||
| [`PassiveLevelUpAtCombatEnd`](./Enums.md) | Integer || 2 | 1 |
| [`PassiveUntilCastSpell`](Miscellaneous.md#object-passiveuntilcastspell) | Object || 1 ||
| [`PassiveUntilGetKill`](Miscellaneous.md#object-passiveuntilgetkill) | Object || 1 ||
| [`PassiveWhenAffectedByElement`](Cat_Mutations.md#object-passivewhenaffectedbyelement) | Object || 4 ||
| [`PassiveWhenAtFullMana`](Cat_Mutations.md#object-passivewhenatfullmana) | Object || 2 ||
| [`PassiveWhenTheAlpha`](Miscellaneous.md#object-passivewhenthealpha) | Object || 1 ||
| [`PassiveWhileInMonkMeleeStance`](Items_and_Equipment.md#object-passivewhileinmonkmeleestance) | Object || 2 ||
| [`PassiveWhileInMonkRangedStance`](Miscellaneous.md#object-passivewhileinmonkrangedstance) | Object || 1 ||
| [`PassiveWhilePreviewingMonkRangedStance`](Miscellaneous.md#object-passivewhilepreviewingmonkrangedstance) | Object || 1 ||
| [`PassiveWhileWearingMetal`](Miscellaneous.md#object-passivewhilewearingmetal) | Object || 1 ||
| [`PermanentImmobile`](./Enums.md) | Integer || 1 | 1 |
| [`PermanentItems`](./Enums.md) | Integer || 1 | 2 |
| [`PermanentKitten`](./Enums.md) | Integer || 1 | 1 |
| [`PermanentMadness`](./Enums.md) | Integer || 8 | 1 |
| [`Phasing`](./Enums.md) | Integer || 1 | 1 |
| [`Poison`](./Enums.md) | Array / Enum / Integer || 6 | [.5] |
| [`PoisonThorns`](./Enums.md) | Integer || 9 | 2 |
| [`PoopWhenHit`](./Enums.md) | Enum || 2 | Poop |
| [`ProtectTargetedAllies`](./Enums.md) | Enum || 3 | SwapPositions_WideLoad2 |
| [`Quiver`](./Enums.md) | Integer || 1 | 2 |
| [`Quivered`](./Enums.md) | Integer || 6 | 2 |
| [`RandomPassivePool`](Characters_and_Bosses.md#object-randompassivepool) | Object || 3 ||
| [`RangedTrueShot`](./Enums.md) | Integer || 3 | 1 |
| [`RealTimePressure_OneUnit`](./Enums.md) | Integer || 1 | 5 |
| [`ReceivedStatusReplacement`](./Enums.md) | Array || 1 | [Sleep] |
| [`RemoveLineOfSightRestrictions`](./Enums.md) | Integer || 2 | 1 |
| [`RemoveOncePerFightRestriction`](./Enums.md) | Integer || 1 | 1 |
| [`ReplaceBasicAttack`](./Enums.md) | Enum || 6 | BasicButcherMeleeWideDoubleSpin |
| [`ReplaceBasicAttackWhenCastable`](./Enums.md) | Enum || 3 | Shank2 |
| [`ReplaceBasicAttackWhenDead`](./Enums.md) | Enum || 1 | Haunt |
| [`ReplaceBasicMove`](./Enums.md) | Enum || 11 | ToadJump_BasicMove |
| [`ReplaceSpawnedObjects`](./Enums.md) | Array || 3 | [Boulder] |
| [`RevengeDamage`](Abilities_and_Spells.md#object-revengedamage) | Object || 15 ||
| [`ReviveOnWin`](./Enums.md) | Integer || 1 | 100 |
| [`Robot`](Characters_and_Bosses.md#object-robot) | Object || 47 ||
| [`RobotsInheritArmor`](./Enums.md) | Integer || 1 | 2 |
| [`RockDetector`](./Enums.md) | Integer || 1 | 10 |
| [`ScaledStatusOnBleedDamage`](Miscellaneous.md#object-scaledstatusonbleeddamage) | Object || 1 ||
| [`ScaledStatusOnOverMana`](Miscellaneous.md#object-scaledstatusonovermana) | Object || 1 ||
| [`ScaledStatusOnSpendMana`](Items_and_Equipment.md#object-scaledstatusonspendmana) | Object || 2 ||
| [`SchrodingerDisorder`](./Enums.md) | Integer || 1 | 50 |
| [`Scleroderma`](./Enums.md) | Integer || 1 | 1 |
| [`SecurityBotProtect`](Characters_and_Bosses.md#object-securitybotprotect) | Object || 7 ||
| [`SelfDamageWhenDealDamage`](Miscellaneous.md#object-selfdamagewhendealdamage) | Object || 1 ||
| [`SetDefaultFacePassive`](./Enums.md) | Enum || 3 | insane |
| [`SetSpellCosts`](./Enums.md) | Integer || 7 | 3 |
| [`ShareHealthRegen`](./Enums.md) | Integer || 1 | 1 |
| [`SharePickups`](./Enums.md) | Integer || 2 | 1 |
| [`ShoulderCheck`](./Enums.md) | Integer || 1 | 33 |
| [`ShovingMatch`](./Enums.md) | Enum || 1 | attack |
| [`ShowHiddenThings`](./Enums.md) | Integer || 1 | 1 |
| [`SizeScale`](./Enums.md) | Number || 14 | .4 |
| [`Slow`](./Enums.md) | Enum / Integer || 1 | 2 |
| [`SmallEnemiesIgnoreYou`](./Enums.md) | Integer || 1 | 1 |
| [`SmallRockBehavior`](./Enums.md) | Integer || 9 | 5 |
| [`SmiteEnemiesWhoKill`](Miscellaneous.md#object-smiteenemieswhokill) | Object || 1 ||
| [`SpawnCatCopyOnBattleStart`](Miscellaneous.md#object-spawncatcopyonbattlestart) | Object || 2 ||
| [`SpawnCreepOnHit`](./Enums.md) | Integer || 3 | 1 |
| [`SpawnEachTurn`](Cat_Mutations.md#object-spawneachturn) | Object || 15 ||
| [`SpawnObjectOnPopCorpse`](./Enums.md) | Enum || 3 | Food |
| [`SpawnOnBattleStart`](Elite_Buffs.md#object-spawnonbattlestart) | Enum / Object || 36 | CharmedTinySpider |
| [`SpawnOnBattleStartRandomEmptyTile`](Cat_Mutations.md#object-spawnonbattlestartrandomemptytile) | Object || 6 ||
| [`SpawnThingOnDamage`](Cat_Mutations.md#object-spawnthingondamage) | Object || 28 ||
| [`SpawnThingOnDeath`](./Enums.md) | Enum || 12 | CharmedDemonKitten |
| [`SpecialFriends`](Miscellaneous.md#object-specialfriends) | Object || 1 ||
| [`SpeedUp`](./Enums.md) | Integer || 7 | 2 |
| [`SplittableMove`](./Enums.md) | Integer || 1 | 3 |
| [`SpreadExtraDebuffs`](./Enums.md) | Integer || 1 | 2 |
| [`SpreadPainBonus`](./Enums.md) | Integer || 1 | 2 |
| [`StatMinimum`](./Enums.md) | Integer || 1 | 7 |
| [`StatsAtLowHealth`](Miscellaneous.md#object-statsatlowhealth) | Object || 2 ||
| [`StatusAdjacentOnTheirTurnBegin`](Miscellaneous.md#object-statusadjacentontheirturnbegin) | Object || 1 ||
| [`StatusAfterCastSpell`](Items_and_Equipment.md#object-statusaftercastspell) | Object || 3 ||
| [`StatusAlliesOnBattleStart`](Items_and_Equipment.md#object-statusalliesonbattlestart) | Object || 9 ||
| [`StatusAlliesOnDeath`](Items_and_Equipment.md#object-statusalliesondeath) | Object || 4 ||
| [`StatusAlliesOnGainCoins`](Miscellaneous.md#object-statusalliesongaincoins) | Object || 1 ||
| [`StatusAlliesOnKill`](Miscellaneous.md#object-statusalliesonkill) | Object || 1 ||
| [`StatusAllyWhenAllySpendsMana`](Miscellaneous.md#object-statusallywhenallyspendsmana) | Object || 1 ||
| [`StatusAnyCatAllyWhoKills`](Miscellaneous.md#object-statusanycatallywhokills) | Object || 1 ||
| [`StatusDamagers`](Miscellaneous.md#object-statusdamagers) | Object || 1 ||
| [`StatusEachTurnBegin`](Cat_Mutations.md#object-statuseachturnbegin) | Object || 18 ||
| [`StatusEachTurnEnd`](Cat_Mutations.md#object-statuseachturnend) | Object || 49 ||
| [`StatusEachTurnEndForEachTurn`](Characters_and_Bosses.md#object-statuseachturnendforeachturn) | Object || 2 ||
| [`StatusEachTurnEndPerEnemyKill`](Miscellaneous.md#object-statuseachturnendperenemykill) | Object || 1 ||
| [`StatusEnemiesOnDeath`](Miscellaneous.md#object-statusenemiesondeath) | Object || 1 ||
| [`StatusEveryXSpellCasts`](Cat_Mutations.md#object-statuseveryxspellcasts) | Object || 4 ||
| [`StatusEveryXTurnBegins`](Miscellaneous.md#object-statuseveryxturnbegins) | Object || 1 ||
| [`StatusIfBattleAlreadyBegan`](Miscellaneous.md#object-statusifbattlealreadybegan) | Object || 1 ||
| [`StatusIfUnusedMovePoints`](Cat_Mutations.md#object-statusifunusedmovepoints) | Object || 5 ||
| [`StatusImmunity`](./Enums.md) | Array / Enum || 34 | [Sleep] |
| [`StatusKilledCharacters`](Cat_Mutations.md#object-statuskilledcharacters) | Object || 2 ||
| [`StatusKillers`](Abilities_and_Spells.md#object-statuskillers) | Object || 1 ||
| [`StatusOnAllyCatDeath`](Cat_Mutations.md#object-statusonallycatdeath) | Object || 4 ||
| [`StatusOnAnyDeath`](Miscellaneous.md#object-statusonanydeath) | Object || 1 ||
| [`StatusOnBattleEnd`](Abilities_and_Spells.md#object-statusonbattleend) | Object || 45 ||
| [`StatusOnBattleEndIfKillThresholdMet`](Miscellaneous.md#object-statusonbattleendifkillthresholdmet) | Object || 1 ||
| [`StatusOnBattleStart`](Items_and_Equipment.md#object-statusonbattlestart) | Object || 15 ||
| [`StatusOnBreakItem`](Items_and_Equipment.md#object-statusonbreakitem) | Object || 3 ||
| [`StatusOnCastSpell`](Cat_Mutations.md#object-statusoncastspell) | Object || 4 ||
| [`StatusOnCollectPickup`](Items_and_Equipment.md#object-statusoncollectpickup) | Object || 2 ||
| [`StatusOnCrit`](Miscellaneous.md#object-statusoncrit) | Object || 3 ||
| [`StatusOnDealtDamage`](Miscellaneous.md#object-statusondealtdamage) | Object || 1 ||
| [`StatusOnDealtDamageThreshold`](Miscellaneous.md#object-statusondealtdamagethreshold) | Object || 1 ||
| [`StatusOnEatFood`](Cat_Mutations.md#object-statusoneatfood) | Object || 3 ||
| [`StatusOnEatPill`](Miscellaneous.md#object-statusoneatpill) | Object || 2 ||
| [`StatusOnEndMove`](Cat_Mutations.md#object-statusonendmove) | Object || 7 ||
| [`StatusOnGainCoins`](Characters_and_Bosses.md#object-statusongaincoins) | Object || 4 ||
| [`StatusOnGainShield`](Miscellaneous.md#object-statusongainshield) | Object || 1 ||
| [`StatusOnHeal`](Miscellaneous.md#object-statusonheal) | Object || 1 ||
| [`StatusOnHealed`](Items_and_Equipment.md#object-statusonhealed) | Object || 2 ||
| [`StatusOnKill`](Cat_Mutations.md#object-statusonkill) | Object || 29 ||
| [`StatusOnKillEnemy`](Items_and_Equipment.md#object-statusonkillenemy) | Object || 10 ||
| [`StatusOnLoseShield`](Miscellaneous.md#object-statusonloseshield) | Object || 1 ||
| [`StatusOnOverHealed`](Miscellaneous.md#object-statusonoverhealed) | Object || 3 ||
| [`StatusOnOverMana`](Miscellaneous.md#object-statusonovermana) | Object || 1 ||
| [`StatusOnPickupCoins`](Items_and_Equipment.md#object-statusonpickupcoins) | Object || 2 ||
| [`StatusOnPopCorpse`](Items_and_Equipment.md#object-statusonpopcorpse) | Object || 4 ||
| [`StatusOnStanceSwitch`](Miscellaneous.md#object-statusonstanceswitch) | Object || 3 ||
| [`StatusOnTakeHealthDamage`](Miscellaneous.md#object-statusontakehealthdamage) | Object || 1 ||
| [`StatusOnTookDamage`](Cat_Mutations.md#object-statusontookdamage) | Object || 29 ||
| [`StatusOnTookDamageFromAbility`](Cat_Mutations.md#object-statusontookdamagefromability) | Object || 6 ||
| [`StatusOnTookDamageFromEnemyAbility`](Miscellaneous.md#object-statusontookdamagefromenemyability) | Object || 1 ||
| [`StatusOnTriggerTrap`](Miscellaneous.md#object-statusontriggertrap) | Object || 1 ||
| [`StatusOnTurnEndIfCastNSpells`](Miscellaneous.md#object-statusonturnendifcastnspells) | Object || 3 ||
| [`StatusOnTurnEndIfDidntCastAbilityTypes`](Items_and_Equipment.md#object-statusonturnendifdidntcastabilitytypes) | Object || 5 ||
| [`StatusOnTurnEndIfManaExact`](Miscellaneous.md#object-statusonturnendifmanaexact) | Object || 2 ||
| [`StatusOnTurnEndIfManaOrHealthExact`](Miscellaneous.md#object-statusonturnendifmanaorhealthexact) | Object || 2 ||
| [`StatusOnUseAbilityWithTag`](Miscellaneous.md#object-statusonuseabilitywithtag) | Object || 3 ||
| [`StatusOnUseBasicAttack`](Items_and_Equipment.md#object-statusonusebasicattack) | Object || 2 ||
| [`StatusOnUseElementAbility`](Miscellaneous.md#object-statusonuseelementability) | Object || 1 ||
| [`StatusPerInjury`](Miscellaneous.md#object-statusperinjury) | Object || 1 ||
| [`StatusReplacement`](./Enums.md) | Array || 1 | [Petrify] |
| [`StatusThingsKnockedBack`](Miscellaneous.md#object-statusthingsknockedback) | Object || 1 ||
| [`StatusWhenAllySpendsMana`](Items_and_Equipment.md#object-statuswhenallyspendsmana) | Object || 2 ||
| [`Stealth`](./Enums.md) | Integer || 1 | 1 |
| [`StrengthForEachNeighboringEnemy`](./Enums.md) | Integer || 1 | 2 |
| [`StrengthInNumbersAura`](Miscellaneous.md#object-strengthinnumbersaura) | Integer / Object || 1 | 1 |
| [`StrengthUp`](./Enums.md) | Integer || 3 | 2 |
| [`StrictLimitDamage`](./Enums.md) | Integer || 1 | 1 |
| [`Study`](Miscellaneous.md#object-study) | Integer / Object || 1 | 1 |
| [`TaggedPickupEffectReplacement`](Miscellaneous.md#object-taggedpickupeffectreplacement) | Object || 1 ||
| [`TauntAlways`](./Enums.md) | Integer || 2 | 1 |
| [`TauntAtFullHealth`](./Enums.md) | Integer || 1 | 1 |
| [`Tech`](./Enums.md) | Integer || 1 | 1 |
| [`TempInitiativeChange`](./Enums.md) | Integer || 1 | -999 |
| [`TheHunger`](Miscellaneous.md#object-thehunger) | Object || 1 ||
| [`Thorns`](./Enums.md) | Integer || 65 | 2 |
| [`TileDamageMultiplier`](Miscellaneous.md#object-tiledamagemultiplier) | Integer / Object || 1 | 2 |
| [`TileTrail`](./Enums.md) | Enum || 6 | FlowerTile |
| [`TourettesMeows`](Miscellaneous.md#object-tourettesmeows) | Object || 1 ||
| [`TowerDefense`](Miscellaneous.md#object-towerdefense) | Object || 1 ||
| [`TowerDefenseReflex`](./Enums.md) | Enum || 2 | BasicRanged_1DMG |
| [`Trample`](./Enums.md) | Array / Integer || 88 | [3] |
| [`TrapEffectsMultiplier`](./Enums.md) | Integer || 1 | 2 |
| [`TrinketActiveEffectsMultiplierBonus`](./Enums.md) | Integer || 5 | 2 |
| [`TrinketPassiveMultiplierBonus`](./Enums.md) | Integer || 9 | 2 |
| [`Triskaidekaphobia`](./Enums.md) | Integer || 1 | 13 |
| [`UncappedHP`](./Enums.md) | Integer || 2 | 1 |
| [`UncappedMana`](./Enums.md) | Integer || 1 | 1 |
| [`UpgradeLevelUpClassActives`](./Enums.md) | Enum || 1 | Colorless |
| [`UpgradeLevelUpClassPassives`](./Enums.md) | Enum || 1 | Colorless |
| [`UpgradeSpawnedPickups`](./Enums.md) | Integer || 2 | 2 |
| [`Vegan`](./Enums.md) | Integer || 1 | 1 |
| [`Vengeful`](./Enums.md) | Integer || 1 | 1 |
| [`WaterWalk`](./Enums.md) | Integer || 14 | 1 |
| [`Weakness`](./Enums.md) | Enum / Integer || 2 | 2 |
| [`WeaponActiveEffectsMultiplierBonus`](./Enums.md) | Integer || 2 | 2 |
| [`WeaponCountsAsBasicAttack`](./Enums.md) | Integer || 1 | 1 |
| [`WeaponDamageMultiplierBonus`](./Enums.md) | Integer || 2 | 2 |
| [`WeaponPassiveMultiplierBonus`](./Enums.md) | Integer || 2 | 2 |
| [`WeaponsDontLoseDurability`](./Enums.md) | Integer || 3 | 0 |
| [`WobblyCat`](./Enums.md) | Integer || 1 | 25 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 8 |

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
| `con` | Enum / Integer || 34 ||
| `spd` | Enum / Integer || 27 ||
| `cha` | Enum / Integer || 24 ||
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
| [`ApplyStatusIfCrit`](Abilities_and_Spells.md#object-applystatusifcrit) | Object || 2 ||
| [`ApplyToSource`](Abilities_and_Spells.md#object-applytosource) | Object || 2 ||
| [`BigSplashDamage`](./Enums.md) | Integer || 1 | 2 |
| [`Bleed`](./Enums.md) | Array / Integer || 30 | [.1] |
| [`Blind`](./Enums.md) | Integer || 2 | 1 |
| [`BounceObject`](./Enums.md) | Enum || 4 | CharmedLeech |
| [`Bruise`](./Enums.md) | Integer || 12 | 2 |
| [`BurgleCoin`](./Enums.md) | Integer || 2 | 1 |
| [`Burn`](./Enums.md) | Enum / Integer || 16 | 2 |
| [`ChangeTile`](Abilities_and_Spells.md#object-changetile) | Enum / Object || 10 | FloatingGlassTile |
| [`Charmed`](./Enums.md) | Array / Integer || 3 | [.40] |
| [`Conditional_Adjacent`](Engine_LogicKeys.md#conditional_adjacent) | Object || 2 ||
| [`Conditional_Ally`](Abilities_and_Spells.md#object-conditional_ally) | Object || 5 ||
| [`Conditional_Enemy`](Abilities_and_Spells.md#object-conditional_enemy) | Object || 3 ||
| [`Conditional_HasTag`](Abilities_and_Spells.md#object-conditional_hastag) | Object || 1 ||
| [`Conditional_Shielded`](Abilities_and_Spells.md#object-conditional_shielded) | Object || 2 ||
| [`Conditional_SourceHasTag`](Engine_LogicKeys.md#conditional_sourcehastag) | Object || 1 ||
| [`Confusion`](./Enums.md) | Integer || 7 | 2 |
| [`DamageOrHealConditionally`](./Enums.md) | Integer || 4 | 1 |
| [`DistanceBonusDamage`](Engine_StatusAndPassiveKeys.md#object-distancebonusdamage) | Object || 4 ||
| [`Else`](Abilities_and_Spells.md#object-else) | Object || 1 ||
| [`Fear`](./Enums.md) | Array / Integer || 13 | [.15] |
| [`Freeze`](./Enums.md) | Array / Integer || 4 | [.15] |
| [`KnockOutCoin`](./Enums.md) | Array / Integer || 2 | [.5] |
| [`Knockback`](./Enums.md) | Integer || 24 | 3 |
| [`Leech`](./Enums.md) | Integer || 5 | 1 |
| [`Leeches`](./Enums.md) | Integer || 4 | 1 |
| [`LuckUp`](./Enums.md) | Integer || 2 | 2 |
| [`Madness`](./Enums.md) | Integer || 3 | 1 |
| [`MagicWeakness`](./Enums.md) | Integer || 3 | 2 |
| [`ManaLeeches`](./Enums.md) | Integer || 2 | 1 |
| [`OverrideChainKnockback`](./Enums.md) | Integer || 2 | 0 |
| [`OverrideChainKnockbackDamage`](./Enums.md) | Integer || 1 | 0 |
| [`Piercing`](./Enums.md) | Integer || 3 | 1 |
| [`Poison`](./Enums.md) | Array / Enum / Integer || 29 | [.5] |
| [`Rot`](./Enums.md) | Integer || 5 | -999999 |
| [`Slow`](./Enums.md) | Enum / Integer || 10 | 2 |
| [`SoulLink`](./Enums.md) | Integer || 4 | 1 |
| [`SpawnBearTrapOnMiss`](./Enums.md) | Integer || 2 | 1 |
| [`SplashDamage`](./Enums.md) | Integer || 1 | 2 |
| [`SpreadDisease`](Abilities_and_Spells.md#object-spreaddisease) | Object || 3 ||
| [`Stun`](./Enums.md) | Array / Integer || 8 | [.05*X] |
| [`Weakness`](./Enums.md) | Enum / Integer || 7 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 56 |

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
| [`Bleed`](./Enums.md) | Array / Integer || 54 | [.1] |
| [`Bruise`](./Enums.md) | Integer || 79 | 2 |
| [`Burn`](./Enums.md) | Enum / Integer || 85 | 2 |
| [`Charmed`](./Enums.md) | Array / Integer || 22 | [.40] |
| [`Fear`](./Enums.md) | Array / Integer || 31 | [.15] |
| [`Freeze`](./Enums.md) | Array / Integer || 19 | [.15] |
| [`Immobile`](./Enums.md) | Integer || 24 | 1 |
| [`Leeches`](./Enums.md) | Integer || 14 | 1 |
| [`Madness`](./Enums.md) | Integer || 19 | 1 |
| [`Marked`](./Enums.md) | Integer || 9 | 1 |
| [`Petrify`](./Enums.md) | Array / Integer || 15 | [.2] |
| [`Poison`](./Enums.md) | Array / Enum / Integer || 67 | [.5] |
| [`Slow`](./Enums.md) | Enum / Integer || 29 | 2 |
| [`SpreadDisease`](Abilities_and_Spells.md#object-spreaddisease) | Object || 8 ||
| [`Stun`](./Enums.md) | Array / Integer || 98 | [.05*X] |
| [`VisualFXTile`](./Enums.md) | Enum || 34 | IcePoof |
| [`Weakness`](./Enums.md) | Enum / Integer || 23 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 750 |

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
| [`AddMaxHealth`](./Enums.md) | Integer || 6 | 5 |
| [`AddSpeed`](./Enums.md) | Integer || 2 | 4 |
| [`AddStatusToBasicAttack`](Abilities_and_Spells.md#object-addstatustobasicattack) | Object || 4 ||
| [`AddStatusToExplosions`](Miscellaneous.md#object-addstatustoexplosions) | Object || 2 ||
| [`AddUnfilledMaxHealth`](./Enums.md) | Integer || 1 | 20 |
| [`DamageUp`](./Enums.md) | Integer || 7 | 2 |
| [`DivineShield`](./Enums.md) | Integer || 1 | 1 |
| [`EMP`](Miscellaneous.md#object-emp) | Object || 2 ||
| [`FamiliarBonusAbility`](./Enums.md) | Enum || 2 | FamiliarSelfDestruct |
| [`ForceAttack`](./Enums.md) | Integer || 2 | 1 |
| [`FreePathfindElement`](./Enums.md) | Enum || 3 | Grass |
| [`GrassTileHealing`](./Enums.md) | Integer || 1 | 1 |
| [`HealthGain`](./Enums.md) | Integer / String || 7 | 2*X |
| [`HealthRegenUp`](./Enums.md) | Integer || 2 | 2 |
| [`HolyShieldTransferToSpawner`](./Enums.md) | Integer || 2 | 1 |
| [`IncreaseExplosionDamage`](./Enums.md) | Integer || 4 | 2 |
| [`IncreaseExplosionSize`](./Enums.md) | Integer || 2 | 2 |
| [`PassiveWhenAffectedByElement`](Cat_Mutations.md#object-passivewhenaffectedbyelement) | Object || 2 ||
| [`PoisonThorns`](./Enums.md) | Integer || 2 | 2 |
| [`Quivered`](./Enums.md) | Integer || 1 | 2 |
| [`SafeExplosions`](./Enums.md) | Integer || 1 | 1 |
| [`StatusAlliesOnKill`](Miscellaneous.md#object-statusalliesonkill) | Object || 2 ||
| [`StatusOnKill`](Cat_Mutations.md#object-statusonkill) | Object || 2 ||
| [`TakeExtraTurn`](./Enums.md) | Integer || 1 | 1 |
| [`UncappedHP`](./Enums.md) | Integer || 1 | 1 |
| [`WaterWalk`](./Enums.md) | Integer || 2 | 1 |
| [`tag_filter`](./Enums.md) | Enum || 3 | crow |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

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
| [`object`](./Arrays.md#array-object) | Array / Enum || 38 ||
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
| [`Conditional_HasStatus`](Abilities_and_Spells.md#object-conditional_hasstatus) | Object || 2 ||
| [`ConstitutionUp`](./Enums.md) | Integer || 3 | 2 |
| [`Craft`](Abilities_and_Spells.md#object-craft) | Object || 2 ||
| [`DamageUp`](./Enums.md) | Integer || 3 | 2 |
| [`DiminishingHealthRegen`](./Enums.md) | Integer || 1 | 2 |
| [`Else`](Abilities_and_Spells.md#object-else) | Object || 1 ||
| [`IntelligenceUp`](./Enums.md) | Integer || 2 | -1 |
| [`MovementUp`](./Enums.md) | Integer || 1 | 2 |
| [`RandomInjury`](./Enums.md) | Integer || 1 | 1 |
| [`RandomStatUp`](./Enums.md) | Integer || 2 | 2 |
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object || 1 ||
| [`Shield`](./Enums.md) | Integer / String || 2 | 2 |
| [`SpeedUp`](./Enums.md) | Integer || 3 | 2 |
| [`StrengthUp`](./Enums.md) | Integer || 4 | 2 |
| [`TempDamageUp`](./Enums.md) | Integer || 2 | 2 |
| [`TempMovement`](./Enums.md) | Integer || 1 | 1 |
| [`Temporary`](Abilities_and_Spells.md#object-temporary) | Object || 3 ||
| [`Thorns`](./Enums.md) | Integer || 3 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 14 |

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
| [`EmptyMana`](./Enums.md) | Integer || 2 | 1 |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object || 12 | Hallucinate_Disorder |
| [`IntelligenceUp`](./Enums.md) | Integer || 2 | -1 |
| [`KineticSpikes`](./Enums.md) | Integer || 1 | 2 |
| [`NonStackingDivineShield`](./Enums.md) | Integer || 6 | 1 |
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object || 1 | Coin |
| [`PermanentMadness`](./Enums.md) | Integer || 1 | 1 |
| [`RangeUp`](./Enums.md) | Integer || 2 | 1 |
| [`SpeedUp`](./Enums.md) | Integer || 5 | 2 |
| [`StrengthUp`](./Enums.md) | Integer || 1 | 2 |
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
| [`slot`](./Enums.md#enum-slot) | Enum / Integer || 16 ||
| `frame` | Integer || 3 ||

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
| [`CureDisease`](Engine_StatusAndPassiveKeys.md#object-curedisease) | Object || 6 ||
| [`FindItemFromPool`](Abilities_and_Spells.md#object-finditemfrompool) | Enum / Object || 8 | consumables |
| [`NextBattleStatus`](Engine_StatusAndPassiveKeys.md#object-nextbattlestatus) | Object || 2 ||
| [`PermanentConstitution`](./Enums.md) | Integer || 2 | -1 |
| [`PermanentIntelligence`](./Enums.md) | Integer || 3 | -1 |
| [`PermanentSpeed`](./Enums.md) | Integer || 2 | -1 |
| [`PermanentStrength`](./Enums.md) | Integer || 1 | 2 |
| [`RandomMutation`](./Enums.md) | Integer || 9 | 1 |
| [`RandomPermanentStat`](./Enums.md) | Integer || 8 | 3 |

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
| [`AllStatsUp`](./Enums.md) | Array / Integer || 2 | [.5] |
| [`Conditional_FirstApplicationThisTurn`](Abilities_and_Spells.md#object-conditional_firstapplicationthisturn) | Object || 2 ||
| [`DamageUp`](./Enums.md) | Integer || 2 | 2 |
| [`EquipPermanentItem`](./Enums.md) | Enum || 3 | BoneClub |
| [`HealthGain`](./Enums.md) | Integer / String || 5 | 2*X |
| [`LuckUp`](./Enums.md) | Integer || 2 | 2 |
| [`RandomStatUp`](./Enums.md) | Integer || 1 | 2 |
| [`RefreshActPoints`](./Enums.md) | Integer || 2 | 1 |
| [`RefreshMovePoints`](./Enums.md) | Integer || 2 | 1 |
| [`SpeedUp`](./Enums.md) | Integer || 2 | 2 |
| [`Stealth`](./Enums.md) | Integer || 1 | 1 |
| [`StrengthUp`](./Enums.md) | Integer || 3 | 2 |
| [`TakeBonusTurnWithStatus`](Abilities_and_Spells.md#object-takebonusturnwithstatus) | Object || 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 6 |

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
| `NextBasicAttackCritsThisTurn` | `Number` | Guarantees the next basic attack executed this turn will be a critical hit. | 2 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object || 2 | Hallucinate_Disorder |
| [`PartialCleanse`](./Enums.md) | Integer || 1 | 1 |
| [`RandomMagicMissile`](./Enums.md) | Integer || 6 | 2 |
| [`RandomStatUp`](./Enums.md) | Integer || 2 | 2 |
| [`Shield`](./Enums.md) | Integer / String || 2 | 2 |

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
| `can_apply_to_anything` | Boolean || 6 ||

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
| [`Conditional_BadRoll`](Abilities_and_Spells.md#object-conditional_badroll) | Object || 5 ||
| [`Conditional_GoodRoll`](Abilities_and_Spells.md#object-conditional_goodroll) | Object || 1 ||
| [`Fear`](./Enums.md) | Array / Integer || 1 | [.15] |
| [`FillMana`](./Enums.md) | Array / Integer || 2 | [.25] |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object || 1 | Hallucinate_Disorder |
| [`IntelligenceUp`](./Enums.md) | Integer || 2 | -1 |
| [`RandomStatUp`](./Enums.md) | Integer || 2 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |

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
| `Cleanse` | `Number` | Applies the 'Cleanse' effect. | 3 ||
| [`ApplyToSource`](Abilities_and_Spells.md#object-applytosource) | Object | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 2 ||
| `ClearNegativeEffects` | `Number` | Applies the 'ClearNegativeEffects' effect. | 2 ||
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object | Selects and applies a random status effect from the provided nested block. | 2 ||
| [`AllStatsUp`](./Enums.md) | Array / Integer || 4 | [.5] |
| [`DamageUp`](./Enums.md) | Integer || 5 | 2 |
| [`Shield`](./Enums.md) | Integer / String || 2 | 2 |
| [`SpeedUp`](./Enums.md) | Integer || 1 | 2 |
| [`TempSpeedUp`](./Enums.md) | Integer || 2 | 10 |

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
| [`Bleed`](./Enums.md) | Array / Integer || 1 | [.1] |
| [`Bruise`](./Enums.md) | Integer || 1 | 2 |
| [`Conditional_HasStatus`](Abilities_and_Spells.md#object-conditional_hasstatus) | Object || 2 ||
| [`Confusion`](./Enums.md) | Integer || 1 | 2 |
| [`Else`](Abilities_and_Spells.md#object-else) | Object || 2 ||
| [`Immobile`](./Enums.md) | Integer || 1 | 1 |
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object || 2 | Coin |
| [`Stun`](./Enums.md) | Array / Integer || 3 | [.05*X] |
| [`Weakness`](./Enums.md) | Enum / Integer || 3 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

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
| `expires_on_end_turn` | Boolean || 21 ||

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
| [`mode`](./Enums.md#enum-mode) | Enum || 13 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 13 ||
| [`threshold`](Items_and_Equipment.md#object-threshold) | Integer / Object || 13 | 7 |

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
| `cha` | Enum / Integer || 2 ||
| `spd` | Enum / Integer || 2 ||

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
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 29 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 31 ||
| `knockback` | Enum / Integer || 3 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 29 |

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
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 47 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 43 ||
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | The base damage properties of an attack. | 22 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 70 ||
| [`elements`](./Arrays.md#array-elements) | Array || 10 ||
| [`Poison`](./Enums.md) | Array / Enum / Integer || 1 | [.5] |
| [`SpreadDisease`](Abilities_and_Spells.md#object-spreaddisease) | Object || 1 ||
| [`Weakness`](./Enums.md) | Enum / Integer || 1 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 49 |

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
| [`CounterAttack`](./Enums.md) | Enum || 2 | ReflexPunchJab |
| [`CritsApplyStatus`](Items_and_Equipment.md#object-critsapplystatus) | Object || 1 ||
| [`ExtraMovePoints`](./Enums.md) | Integer || 2 | 1 |
| [`Flying`](./Enums.md) | Integer || 1 | 1 |
| [`ManaCostReduction`](./Enums.md) | Integer || 2 | 2 |
| [`StatusOnStanceSwitch`](Miscellaneous.md#object-statusonstanceswitch) | Object || 2 ||

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
| [`AllStatsUp`](./Enums.md) | Array / Integer || 5 | [.5] |
| [`Bleed`](./Enums.md) | Array / Integer || 8 | [.1] |
| [`BleedThorns`](./Enums.md) | Integer || 4 | 2 |
| [`Blind`](./Enums.md) | Integer || 6 | 1 |
| [`Brace`](./Enums.md) | Integer || 6 | 2 |
| [`Bruise`](./Enums.md) | Integer || 6 | 2 |
| [`Burn`](./Enums.md) | Enum / Integer || 5 | 2 |
| [`Charge`](./Enums.md) | Integer || 8 | 2 |
| [`Charmed`](./Enums.md) | Array / Integer || 3 | [.40] |
| [`Confusion`](./Enums.md) | Integer || 3 | 2 |
| [`ConstitutionUp`](./Enums.md) | Integer || 4 | 2 |
| [`DiminishingHealthRegen`](./Enums.md) | Integer || 6 | 2 |
| [`DivineShield`](./Enums.md) | Integer || 9 | 1 |
| [`Fear`](./Enums.md) | Array / Integer || 3 | [.15] |
| [`Freeze`](./Enums.md) | Array / Integer || 3 | [.15] |
| [`Immobile`](./Enums.md) | Integer || 3 | 1 |
| [`KineticSpikes`](./Enums.md) | Integer || 9 | 2 |
| [`Madness`](./Enums.md) | Integer || 4 | 1 |
| [`MagicWeakness`](./Enums.md) | Integer || 4 | 2 |
| [`Marked`](./Enums.md) | Integer || 4 | 1 |
| [`MoveQuivered`](./Enums.md) | Integer || 5 | 2 |
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object || 1 | Coin |
| [`Petrify`](./Enums.md) | Array / Integer || 3 | [.2] |
| [`Poison`](./Enums.md) | Array / Enum / Integer || 9 | [.5] |
| [`Quivered`](./Enums.md) | Integer || 5 | 2 |
| [`Reflect`](./Enums.md) | Integer || 4 | 1 |
| [`Shield`](./Enums.md) | Integer / String || 12 | 2 |
| [`Sleep`](./Enums.md) | Integer || 3 | 1 |
| [`Slow`](./Enums.md) | Enum / Integer || 7 | 2 |
| [`SpawnCoinAnywhere`](./Enums.md) | Integer || 1 | 1 |
| [`SpeedUp`](./Enums.md) | Integer || 4 | 2 |
| [`StatusGroup`](Abilities_and_Spells.md#object-statusgroup) | Object || 3 ||
| [`StrengthUp`](./Enums.md) | Integer || 3 | 2 |
| [`Stun`](./Enums.md) | Array / Integer || 4 | [.05*X] |
| [`Tarred`](./Enums.md) | Integer || 4 | 1 |
| [`Thorns`](./Enums.md) | Integer || 10 | 2 |
| [`Weakness`](./Enums.md) | Enum / Integer || 8 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 12 |

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
| [`CritChanceUp`](./Enums.md) | Integer || 1 | 80 |
| [`DamageUp`](./Enums.md) | Integer || 2 | 2 |
| [`LuckUp`](./Enums.md) | Integer || 3 | 2 |
| [`RandomStatUp`](./Enums.md) | Integer || 1 | 2 |
| [`Shield`](./Enums.md) | Integer / String || 2 | 2 |
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
| [`Conditional_PartyMember`](Engine_LogicKeys.md#conditional_partymember) | Object || 2 ||
| [`Confusion`](./Enums.md) | Integer || 9 | 2 |
| [`Else`](Abilities_and_Spells.md#object-else) | Object || 2 ||
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object || 2 ||
| [`Stun`](./Enums.md) | Array / Integer || 2 | [.05*X] |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 12 |

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
| `cant_miss` | `Boolean` || 6 ||
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 6 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 ||
| `knockback` | Enum / Integer || 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 6 |

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
| [`chance`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Mixed | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 3 ||

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
| [`CritChanceUp`](./Enums.md) | Integer || 2 | 80 |
| [`DodgeChance`](./Enums.md) | Integer || 2 | 50 |
| [`KineticSpikes`](./Enums.md) | Integer || 1 | 2 |
| [`StatusOnStanceSwitch`](Miscellaneous.md#object-statusonstanceswitch) | Object || 2 ||

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
| [`CritChanceUp`](./Enums.md) | Integer || 2 | 80 |
| [`DodgeChance`](./Enums.md) | Integer || 2 | 50 |
| [`KineticSpikes`](./Enums.md) | Integer || 1 | 2 |
| [`StatusOnStanceSwitch`](Miscellaneous.md#object-statusonstanceswitch) | Object || 2 ||

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
| [`CritChanceUp`](./Enums.md) | Integer || 2 | 80 |
| [`DodgeChance`](./Enums.md) | Integer || 2 | 50 |
| [`KineticSpikes`](./Enums.md) | Integer || 1 | 2 |
| [`StatusOnStanceSwitch`](Miscellaneous.md#object-statusonstanceswitch) | Object || 2 ||

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
| `triggers_limit` | Number || 2 ||
| [`AllStatsUp`](./Enums.md) | Array / Integer || 2 | [.5] |
| [`Freeze`](./Enums.md) | Array / Integer || 1 | [.15] |
| [`FullHeal`](./Enums.md) | Integer || 1 | 1 |
| [`HealAndOverhealToShield`](./Enums.md) | Integer || 2 | 12 |
| [`Reanimate`](./Enums.md) | Integer || 2 | 33 |
| [`TakeExtraTurn`](./Enums.md) | Integer || 2 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |

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
| `exclude_basicattack` | Boolean || 2 ||
| [`Conditional_FirstApplicationThisTurn`](Abilities_and_Spells.md#object-conditional_firstapplicationthisturn) | Object || 2 ||
| [`DamageUp`](./Enums.md) | Integer || 2 | 2 |
| [`HealthGain`](./Enums.md) | Integer / String || 1 | 2*X |
| [`RandomStatUp`](./Enums.md) | Integer || 1 | 2 |
| [`RefreshActPoints`](./Enums.md) | Integer || 3 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

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
| [`Bleed`](./Enums.md) | Array / Integer || 1 | [.1] |
| [`ChangeTile`](Abilities_and_Spells.md#object-changetile) | Enum / Object || 2 | FloatingGlassTile |
| [`Conditional_Ally`](Abilities_and_Spells.md#object-conditional_ally) | Object || 2 ||
| [`Conditional_Enemy`](Abilities_and_Spells.md#object-conditional_enemy) | Object || 2 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 6 |

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
| [`Bleed`](./Enums.md) | Array / Integer || 3 | [.1] |
| [`Cleave`](./Enums.md) | Integer || 1 | 1 |
| [`LeechPercent`](./Enums.md) | Integer || 1 | 50 |
| [`PullSourceToKnockbackImmuneTarget`](./Enums.md) | Integer || 2 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |

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
| [`disease`](./Enums.md#enum-disease) | Enum || 6 ||
| `can_apply_to_anything` | Boolean || 1 ||

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
| [`Fear`](./Enums.md) | Array / Integer || 2 | [.15] |
| [`Marked`](./Enums.md) | Integer || 2 | 1 |
| [`PermanentCharm`](./Enums.md) | Integer || 2 | 1 |
| [`TempSpeedUp`](./Enums.md) | Integer || 1 | 10 |

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
| [`Weakness`](./Enums.md) | Enum / Integer || 1 | 2 |

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
| [`chance`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Mixed | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 20 ||
| [`object`](./Arrays.md#array-object) | Array / Enum || 22 ||
| `good` | Boolean || 2 ||
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
| [`object`](./Enums.md#enum-object) | Array / Enum || 38 ||
| `good` | Boolean || 20 ||
| `spawn_on_death_hit` | Boolean || 10 ||
| `consider_all_layers` | Boolean || 2 ||

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
| [`Bruise`](./Enums.md) | Integer || 2 | 2 |
| [`Confusion`](./Enums.md) | Integer || 3 | 2 |
| [`FaceAway`](./Enums.md) | Integer || 2 | 1 |
| [`SpreadDisease`](Abilities_and_Spells.md#object-spreaddisease) | Object || 1 ||
| [`Stun`](./Enums.md) | Array / Integer || 2 | [.05*X] |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

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
| [`Charge`](./Enums.md) | Integer || 4 | 2 |
| [`CurrentWeaponDamageUp`](./Enums.md) | Integer || 2 | 1 |
| [`HealthGain`](./Enums.md) | Integer / String || 1 | 2*X |
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
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||
| `SpawnScaledRotFly` | Number | Applies the 'SpawnScaledRotFly' effect. | 1 ||
| [`CurrentWeaponDamageUp`](./Enums.md) | Integer || 1 | 1 |
| [`ForceUseAbility_NonStack`](./Enums.md) | Enum || 2 | Indigestion_Fart2 |
| [`StrengthUp`](./Enums.md) | Integer || 2 | 2 |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |

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
| [`AddMaxHealth`](./Enums.md) | Integer || 2 | 5 |
| [`AddSpeed`](./Enums.md) | Integer || 2 | 4 |
| [`AddStatusToBasicAttack`](Abilities_and_Spells.md#object-addstatustobasicattack) | Object || 3 ||
| [`DamageUp`](./Enums.md) | Integer || 2 | 2 |

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
| [`Burn`](./Enums.md) | Enum / Integer || 3 | 2 |
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
| [`Burn`](./Enums.md) | Enum / Integer || 4 | 2 |

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
| `force_display_name` | Boolean || 2 ||

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
| [`AllStatsUp`](./Enums.md) | Array / Integer || 1 | [.5] |
| [`FillMana`](./Enums.md) | Array / Integer || 1 | [.25] |
| [`ManaGain`](./Enums.md) | Integer || 1 | 2 |
| [`TakeExtraTurn`](./Enums.md) | Integer || 2 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |

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
| `min_range` | Integer || 4 ||
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
| `cha` | Enum / Integer || 1 ||
| `int` | Enum / Integer || 1 ||
| `spd` | Enum / Integer || 1 ||

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
| [`mode`](./Enums.md#enum-mode) | Enum || 9 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 9 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 9 ||
| [`threshold`](Items_and_Equipment.md#object-threshold) | Integer / Object || 9 | 7 |

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
| [`passives`](Cat_Mutations.md#object-passives) | Object || 18 ||

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
| [`AddMovement`](./Enums.md) | Integer || 1 | 20 |
| [`AddStatusToBasicAttack`](Abilities_and_Spells.md#object-addstatustobasicattack) | Object || 2 ||
| [`Brace`](./Enums.md) | Integer || 2 | 2 |
| [`Flying`](./Enums.md) | Integer || 2 | 1 |
| [`ReplaceBasicMove`](./Enums.md) | Enum || 1 | ToadJump_BasicMove |

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
| `palette` | Enum / Integer || 4 ||
| [`particle`](./Enums.md#enum-particle) | Enum || 4 ||

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
| [`AllStatsUp`](./Enums.md) | Array / Integer || 2 | [.5] |
| [`DamageUp`](./Enums.md) | Integer || 2 | 2 |
| [`HealthGain`](./Enums.md) | Integer / String || 1 | 2*X |

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
| [`Brace`](./Enums.md) | Integer || 1 | 2 |
| [`ConstitutionUp`](./Enums.md) | Integer || 1 | 2 |
| [`HealthGain`](./Enums.md) | Integer / String || 4 | 2*X |
| [`ManaGain`](./Enums.md) | Integer || 2 | 2 |
| [`MoveQuivered`](./Enums.md) | Integer || 2 | 2 |
| [`Shield`](./Enums.md) | Integer / String || 1 | 2 |
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
| `spells` | Array || 5 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 ||
| [`DoubleCastSpell`](./Enums.md) | Integer || 3 | 2 |
| [`MoveQuivered`](./Enums.md) | Integer || 1 | 2 |
| [`Quivered`](./Enums.md) | Integer || 2 | 2 |

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
| [`FreeSpell`](./Enums.md) | Integer || 2 | 1 |
| [`MoveQuivered`](./Enums.md) | Integer || 1 | 2 |
| [`Quivered`](./Enums.md) | Integer || 2 | 2 |
| [`SpellDamageUp`](./Enums.md) | Integer || 1 | 1 |

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
| [`DivineShield`](./Enums.md) | Integer || 1 | 1 |
| [`HealthGain`](./Enums.md) | Integer / String || 1 | 2*X |
| [`IntelligenceUp`](./Enums.md) | Integer || 2 | -1 |
| [`KineticSpikes`](./Enums.md) | Integer || 1 | 2 |
| [`Shield`](./Enums.md) | Integer / String || 2 | 2 |
| [`SpellDamageUp`](./Enums.md) | Integer || 2 | 1 |
| [`Temporary`](Abilities_and_Spells.md#object-temporary) | Object || 2 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

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
| `ability_damage_only` | Boolean || 7 ||
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
| [`RandomMagicMissile`](./Enums.md) | Integer || 7 | 2 |

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
| [`Temporary`](Abilities_and_Spells.md#object-temporary) | Object || 5 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 8 |

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
| `pop_corpse` | Boolean || 11 ||

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
| [`move_ability`](./Enums.md#enum-move_ability) | Enum || 5 ||
| `move_far` | Boolean || 4 ||

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
| [`object`](./Enums.md#enum-object) | Array / Enum || 4 ||
| [`prevent_chain_tag`](./Enums.md#enum-prevent_chain_tag) | Enum || 4 ||

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
| [`object`](./Enums.md#enum-object) | Array / Enum || 11 ||
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
| [`AllStatsUp`](./Enums.md) | Array / Integer || 4 | [.5] |
| [`FindItemFromPool`](Abilities_and_Spells.md#object-finditemfrompool) | Enum / Object || 2 | consumables |
| [`HealthGain`](./Enums.md) | Integer / String || 1 | 2*X |
| [`PermanentDexterity`](./Enums.md) | Integer || 2 | 1 |

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
| [`AllStatsUp`](./Enums.md) | Array / Integer || 2 | [.5] |
| [`ReduceManaCost`](./Enums.md) | Integer || 1 | 1 |
| [`RepairWeapon`](./Enums.md) | Integer || 1 | 1 |
| [`RepairWeaponCondition`](./Enums.md) | Integer || 1 | 1 |
| [`SpellDamageUp`](./Enums.md) | Integer || 2 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |

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
| [`DexterityUp`](./Enums.md) | Integer || 1 | 2 |
| [`LuckUp`](./Enums.md) | Integer || 2 | 2 |
| [`SpawnCoinAnywhere`](./Enums.md) | Integer || 1 | 1 |
| [`SpeedUp`](./Enums.md) | Integer || 2 | 2 |

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
| [`AllStatsUp`](./Enums.md) | Array / Integer || 2 | [.5] |
| [`FillMana`](./Enums.md) | Array / Integer || 1 | [.25] |
| [`HealthGain`](./Enums.md) | Integer / String || 1 | 2*X |
| [`PercentHeal`](./Enums.md) | Integer || 1 | 50 |
| [`TakeExtraTurn`](./Enums.md) | Integer || 1 | 1 |
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
| [`FullHeal`](./Enums.md) | Integer || 2 | 1 |
| [`Sleep`](./Enums.md) | Integer || 1 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 7 |

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
| [`Cleanse`](./Enums.md) | Integer || 1 | 0 |
| [`IntelligenceUp`](./Enums.md) | Integer || 1 | -1 |
| [`RandomStatUp`](./Enums.md) | Integer || 1 | 2 |
| [`StrengthUp`](./Enums.md) | Integer || 2 | 2 |

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
| [`DivineShield`](./Enums.md) | Integer || 1 | 1 |
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object || 2 ||
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
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object || 1 | Coin |
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object || 1 ||
| [`Thorns`](./Enums.md) | Integer || 1 | 2 |
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
| [`DivineShield`](./Enums.md) | Integer || 2 | 1 |
| [`HealthGain`](./Enums.md) | Integer / String || 1 | 2*X |
| [`ManaGain`](./Enums.md) | Integer || 2 | 2 |
| [`RefreshMovePoints`](./Enums.md) | Integer || 1 | 1 |
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
| [`DiminishingHealthRegen`](./Enums.md) | Integer || 2 | 2 |
| [`Shield`](./Enums.md) | Integer / String || 1 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

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
| [`range`](./Engine_Uncategorized_Resources.md#valid-property-keys) | Mixed | Distance or area of effect in tiles. | 5 ||
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
| [`DamageUp`](./Enums.md) | Integer || 2 | 2 |
| [`Doomed`](./Enums.md) | Integer || 2 | 3 |
| [`MovementUp`](./Enums.md) | Integer || 2 | 2 |
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
| [`Bleed`](./Enums.md) | Array / Integer || 1 | [.1] |
| [`Piercing`](./Enums.md) | Integer || 1 | 1 |
| [`Weakness`](./Enums.md) | Enum / Integer || 1 | 2 |

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
| `count` | Array / Integer | The numerical quantity. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||
| [`Bounty`](./Enums.md) | Integer || 3 | 3 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||
| [`Purge`](./Enums.md) | Integer || 2 | 0 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 8 |

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
| [`AllStatsUp`](./Enums.md) | Array / Integer || 6 | [.5] |
| [`Shield`](./Enums.md) | Integer / String || 5 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 20 |

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
| [`crit_chance`](./Engine_DamagingKeys.md#valid-property-keys) | `String` || 4 ||
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
| [`animation`](./Enums.md#enum-animation) | Enum || 2 ||

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
| [`AllStatsUp`](./Enums.md) | Array / Integer || 1 | [.5] |
| [`Quivered`](./Enums.md) | Integer || 5 | 2 |

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
| [`Bleed`](./Enums.md) | Array / Integer || 2 | [.1] |
| [`BonusCritChance`](./Enums.md) | Integer || 2 | 50 |
| [`BonusDamage`](./Enums.md) | Integer || 2 | 2 |
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
| [`Charmed`](./Enums.md) | Array / Integer || 2 | [.40] |
| [`Stun`](./Enums.md) | Array / Integer || 3 | [.05*X] |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 6 |

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
| `Revive` | `Number` | Applies the 'Revive' effect. | 7 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 10 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| `OverrideDamage` | `Number` | Applies the 'OverrideDamage' effect. | 2 ||
| `TakeExtraTurn` | `Number` | Applies the 'TakeExtraTurn' effect. | 2 ||
| [`Charmed`](./Enums.md) | Array / Integer || 2 | [.40] |
| [`DamageUp`](./Enums.md) | Integer || 1 | 2 |
| [`SafeDoomed`](./Enums.md) | Integer || 2 | 1 |
| [`SpeedUp`](./Enums.md) | Integer || 1 | 2 |

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
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 11 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 46 ||
| `FlatLeechIfDamaged` | `Number` | Applies the 'FlatLeechIfDamaged' effect. | 1 ||
| [`Charmed`](./Enums.md) | Array / Integer || 1 | [.40] |

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
| `BonusCritChance` | `Number` | Applies the 'BonusCritChance' effect. | 2 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 5 |

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
| [`pool`](./Enums.md#enum-pool) | Array / Enum || 15 ||
| [`slot`](./Enums.md#enum-slot) | Enum / Integer || 14 ||

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
| [`elements`](./Arrays.md#array-elements) | Array || 4 ||
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
| `allies_only` | Boolean || 2 ||
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
| [`AllStatsUp`](./Enums.md) | Array / Integer || 1 | [.5] |
| [`TakeExtraTurn`](./Enums.md) | Integer || 1 | 1 |
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
| [`Burn`](./Enums.md) | Enum / Integer || 2 | 2 |

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
| [`Poison`](./Enums.md) | Array / Enum / Integer || 2 | [.5] |

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
| [`elements`](./Arrays.md#array-elements) | Array || 2 ||
| [`cant_miss`](./Enums.md) | Boolean || 2 | true |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object || 2 ||
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
| [`FlatLeech`](./Enums.md) | Enum || 2 | X |
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
| [`Burn`](./Enums.md) | Enum / Integer || 2 | 2 |

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
| `health` | Integer || 3 ||
| `playercat_health` | Integer || 3 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`TempSpeedUp`](./Enums.md) | Integer || 2 | 10 |

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
| [`AllStatsUp`](./Enums.md) | Array / Integer || 2 | [.5] |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||
| [`Tech`](./Enums.md) | Integer || 2 | 1 |

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
| `enemies_only` | Boolean || 7 ||

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
| [`passives`](Cat_Mutations.md#object-passives) | Object || 4 ||

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
| [`ManaCostReduction`](./Enums.md) | Integer || 2 | 2 |

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
| [`mode`](./Enums.md#enum-mode) | Enum || 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 2 ||
| [`threshold`](Items_and_Equipment.md#object-threshold) | Integer / Object || 2 | 7 |

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
| [`AllStatsUp`](./Enums.md) | Array / Integer || 1 | [.5] |
| [`CharismaUp`](./Enums.md) | Integer || 1 | 5 |
| [`IntelligenceUp`](./Enums.md) | Integer || 1 | -1 |
| [`SetDefaultFace`](./Enums.md) | Enum || 2 | sad |
| [`SpeedUp`](./Enums.md) | Integer || 1 | 2 |

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
| [`Brace`](./Enums.md) | Integer || 3 | 2 |
| [`HealthRegenUp`](./Enums.md) | Integer || 1 | 2 |

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
| [`AddBonusRange`](./Enums.md) | Integer || 2 | 2 |
| [`AddSpellDamage`](./Enums.md) | Integer || 2 | 2 |
| [`KineticSpikes`](./Enums.md) | Integer || 1 | 2 |

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
| [`AddBonusRange`](./Enums.md) | Integer || 2 | 2 |

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
| [`pool`](./Enums.md#enum-pool) | Array / Enum || 2 ||
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
| [`Cleanse`](./Enums.md) | Integer || 1 | 0 |
| [`RandomMagicMissile`](./Enums.md) | Integer || 2 | 2 |

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
| `con` | Enum / Integer || 1 ||
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
| [`move`](./Enums.md#enum-move) | Enum || 5 ||

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
| [`crit_chance`](./Engine_DamagingKeys.md#valid-property-keys) | `String` || 2 ||
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
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 1 ||
| [`elements`](./Arrays.md#array-elements) | Array || 2 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
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
| [`AllStatsUp`](./Enums.md) | Array / Integer || 2 | [.5] |
| [`HealthGain`](./Enums.md) | Integer / String || 2 | 2*X |

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
| `speed` | Array / Number || 1 ||
| `strength` | Integer || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`threshold`](Items_and_Equipment.md#object-threshold) | Integer / Object || 2 | 7 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`TempDamageUp`](./Enums.md) | Integer || 1 | 2 |
| [`TempSpellDamageUp`](./Enums.md) | Integer || 2 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |

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
| [`EquipTemporaryItem`](./Enums.md) | Enum || 2 | FoodMedium |

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
| `scaled` | Boolean || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`HealthGain`](./Enums.md) | Integer / String || 2 | 2*X |
| [`LuckUp`](./Enums.md) | Integer || 2 | 2 |

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
| [`AllStatsUp`](./Enums.md) | Array / Integer || 2 | [.5] |
| [`threshold`](Items_and_Equipment.md#object-threshold) | Integer / Object || 2 | 7 |

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
| [`Fear`](./Enums.md) | Array / Integer || 1 | [.15] |
| [`LuckUp`](./Enums.md) | Integer || 2 | 2 |

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
| [`RandomMagicMissile`](./Enums.md) | Integer || 3 | 2 |

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
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object || 2 | Coin |

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
| [`DivineShield`](./Enums.md) | Integer || 2 | 1 |

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
| [`LuckUp`](./Enums.md) | Integer || 2 | 2 |

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
| [`statuses`](Characters_and_Bosses.md#object-statuses) | Object || 2 ||

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
| [`Shield`](./Enums.md) | Integer / String || 2 | 2 |
| [`Thorns`](./Enums.md) | Integer || 2 | 2 |
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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`Tech`](./Enums.md) | Integer || 2 | 1 |

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
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||
| [`TempDexterityUp`](./Enums.md) | Integer || 2 | 2 |
| [`TempLuckUp`](./Enums.md) | Integer || 1 | 2 |
| [`TempStrengthUp`](./Enums.md) | Integer || 2 | 2 |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

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
| [`AllStatsUp`](./Enums.md) | Array / Integer || 1 | [.5] |
| [`RefreshMovePoints`](./Enums.md) | Integer || 2 | 1 |
| [`Shield`](./Enums.md) | Integer / String || 2 | 2 |
| [`threshold`](Items_and_Equipment.md#object-threshold) | Integer / Object || 2 | 7 |
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
| [`Temporary`](Abilities_and_Spells.md#object-temporary) | Object || 2 ||
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
| [`RandomStatUp`](./Enums.md) | Integer || 1 | 2 |
| [`SpeedUp`](./Enums.md) | Integer || 2 | 2 |

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
| [`DivineShield`](./Enums.md) | Integer || 1 | 1 |
| [`IntelligenceUp`](./Enums.md) | Integer || 2 | -1 |
| [`SpellDamageUp`](./Enums.md) | Integer || 2 | 1 |

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
| [`DexterityUp`](./Enums.md) | Integer || 1 | 2 |
| [`RefreshMovePoints`](./Enums.md) | Integer || 2 | 1 |
| [`SpeedUp`](./Enums.md) | Integer || 1 | 2 |
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
| [`HealthGain`](./Enums.md) | Integer / String || 3 | 2*X |

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
| [`MoveQuivered`](./Enums.md) | Integer || 1 | 2 |
| [`Quivered`](./Enums.md) | Integer || 2 | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`DexterityUp`](./Enums.md) | Integer || 2 | 2 |
| [`Quivered`](./Enums.md) | Integer || 1 | 2 |

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
| [`SpeedUp`](./Enums.md) | Integer || 2 | 2 |

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
| [`Shield`](./Enums.md) | Integer / String || 2 | 2 |
| [`StrengthUp`](./Enums.md) | Integer || 1 | 2 |
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
| [`ManaGain`](./Enums.md) | Integer || 1 | 2 |
| [`OneUseSpellDamageUp`](./Enums.md) | Integer || 2 | 2 |
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
| [`HealthGain`](./Enums.md) | Integer / String || 2 | 2*X |

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
| [`knockback`](./Math_Equations.md) | Equation || 2 ||

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
| [`elements`](./Arrays.md#array-elements) | Array || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`Burn`](./Enums.md) | Enum / Integer || 1 | 2 |

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
| [`elements`](./Arrays.md#array-elements) | Array || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`Burn`](./Enums.md) | Enum / Integer || 1 | 2 |

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
| [`statuses`](Characters_and_Bosses.md#object-statuses) | Object || 3 ||

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
| [`AllStatsUp`](./Enums.md) | Array / Integer || 1 | [.5] |
| [`Confusion`](./Enums.md) | Integer || 1 | 2 |

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
| [`elements`](./Arrays.md#array-elements) | Array || 1 ||
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
| `free` | Boolean || 1 ||

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
| [`elements`](./Arrays.md#array-elements) | Array || 1 ||
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
| [`elements`](./Arrays.md#array-elements) | Array || 1 ||
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
| [`weights`](./Enums.md#enum-weights) | Array / Enum || 9 ||

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
| [`Shield`](./Enums.md) | Integer / String || 1 | 2 |
| [`Trample`](./Enums.md) | Array / Integer || 1 | [3] |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

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
| [`PassiveGroup`](Characters_and_Bosses.md#object-passivegroup) | Object || 2 ||

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
| [`brain`](./Enums.md#enum-brain) | Enum || 4 ||
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum || 4 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum || 4 ||

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
| [`Charge`](./Enums.md) | Integer || 1 | 2 |

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
| [`Thorns`](./Enums.md) | Integer || 1 | 2 |

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
| `exclude_self` | Boolean || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`RandomStatUp`](./Enums.md) | Integer || 1 | 2 |

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
| [`LuckUp`](./Enums.md) | Integer || 1 | 2 |

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
| [`PermanentMadness`](./Enums.md) | Integer || 1 | 1 |

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
| [`Thorns`](./Enums.md) | Integer || 1 | 2 |

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
| [`PermanentConstitution`](./Enums.md) | Integer || 1 | -1 |

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
| [`ManaGain`](./Enums.md) | Integer || 1 | 2 |
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
| [`Madness`](./Enums.md) | Integer || 3 | 1 |

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
| [`Madness`](./Enums.md) | Integer || 1 | 1 |

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
| [`pool`](./Arrays.md#array-pool) | Array / Enum || 1 ||

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
| [`elements`](./Arrays.md#array-elements) | Array || 1 ||
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
| `stacks` | Enum / Integer || 1 | `1` (Number) |


### Object: `AbilityHealthThreshold`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum || 13 | `FormShrinkFour` (Enum), `DybbukPossess` (Enum) |
| `also_use_if_buddy_is_dead` | Boolean || 1 | `true` (Boolean) |
| `aux` | Integer || 1 | `25` (Number) |
| `even_if_stunned` | Boolean || 7 | `true` (Boolean) |
| `immediate` | Boolean || 6 | `true` (Boolean) |
| [`threshold`](Items_and_Equipment.md#object-threshold) | Enum / Integer / Object || 12 | `1*champion_multiplier` (Enum), `3*champion_multiplier` (Enum), `200` (Number), `1` (Number), `"max(X*.33, 5)"` (String), `"max(X*.5, 1)"` (String) |
| `threshold_min` | Enum || 1 | `X` (Enum) |
| `use_ai` | Boolean || 2 | `true` (Boolean) |


### Object: `AbilityOnRoundEnd`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum || 2 | `DestroyerRaise` (Enum) |
| `force_display_name` | Boolean || 2 | `true` (Boolean) |


### Object: `AbilityOnRoundEndOnce`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum || 1 | `wp_SignalAmplifierSpawnTerminator` (Enum) |
| `even_of_stunned` | Boolean || 1 | `true` (Boolean) |


### Object: `AddAdvantageToEvent`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `add` | Array / Integer || 1 | `5` (Number) |
| `options` | Array || 1 | `[smash bash open]` (Array) |
| `type` | Enum || 1 | `treasure_box` (Enum) |


### Object: `AddStatusToBackstabs`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Bleed` | Array / Integer || 1 | `[1 .1]` (Array), `[3 .1]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |


### Object: `AddStatusToFirstSpellEachTurn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_IsSelf`](Abilities_and_Spells.md#object-conditional_isself) | Object || 1 | `{ ... }` (Object) |
| [`Else`](Abilities_and_Spells.md#object-else) | Object || 1 | `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |


### Object: `AddStatusToReceivedDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_IsPhysicalAttack`](Characters_and_Bosses.md#object-conditional_isphysicalattack) | Object || 1 | `{ ... }` (Object) |
| [`Else`](Abilities_and_Spells.md#object-else) | Object || 1 | `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |


### Object: `AfterImage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `object` | Array / Enum || 2 | `PlayerCat_ThiefShade` (Enum) |
| `skilltemp` | Boolean || 2 | `true` (Boolean) |


### Object: `AggroTargetIsGovernedByHitEffect`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `enemies_only` | Boolean || 1 | `false` (Boolean) |


### Object: `AllStatsAura`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `aura_requires_tag` | Enum || 1 | `humanoid` (Enum) |
| `range` | Enum / Integer || 1 | `global` (Enum) |
| `stacks` | Enum / Integer || 1 | `1` (Number) |


### Object: `AllStatsUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `AlluringDoodieEater`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number || 1 | `10` (Number) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object || 1 | `{ ... }` (Object) |


### Object: `AllyDodgeChanceAura`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number || 1 | `25` (Number) |
| `range` | Enum / Integer || 1 | `1` (Number) |


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
| `frame_range` | Array || 3 | `[6 6]` (Array), `[1 2]` (Array) |
| `stacks` | Enum / Integer || 3 | `4` (Number), `6` (Number) |


### Object: `BackflipWhenTargeted`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum || 7 | `Teleport` (Enum), `SZBBackflipDodge` (Enum) |
| `stacks` | Enum / Integer || 7 | `4` (Number), `1` (Number) |


### Object: `BaitAura`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `range` | Enum / Integer || 4 | `3` (Number) |


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
| [`statuses`](Characters_and_Bosses.md#object-statuses) | Object || 5 | `{ ... }` (Object) |


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
| `common` | Enum || 20 | `RatBomb` (Enum), `ChubsCollar` (Enum) |
| `rare` | Enum || 16 | `BorisBrain` (Enum), `JohnnysStool` (Enum) |


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
| `allies_only` | Boolean || 3 | `false` (Boolean) |
| `obj` | Array / Enum || 3 | `ZaratanaVS` (Enum), `PyrophinaVS` (Enum) |
| `reclaim_if_lost` | Boolean || 1 | `true` (Boolean) |


### Object: `BuffImmunity`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exclude` | Enum || 1 | `SpellDamageUp` (Enum) |


### Object: `BungaCheers`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ally_damage` | Enum || 1 | `littleboo` (Enum) |
| `ally_dead` | Enum || 1 | `bigboo` (Enum) |
| `enemy_damage` | Enum || 1 | `littlecheer` (Enum) |
| `enemy_dead` | Enum || 1 | `bigcheer` (Enum) |
| `warrior_tag` | Enum || 1 | `bungawarrior` (Enum) |


### Object: `BungaEntrance`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum || 2 | `BungaEntrance` (Enum), `BecomeTheDestroyer` (Enum) |
| `even_if_stunned` | Boolean || 2 | `true` (Boolean) |
| `health_threshold` | Integer || 2 | `150` (Number), `-1` (Number) |
| `warrior_tag` | Enum || 2 | `bungawarrior` (Enum), `finalboss_clonecat` (Enum) |


### Object: `Burn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `CatPartsSizeScale`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `head` | Enum / Number || 1 | `1.3` (Number) |


### Object: `CatPartsTransform`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `arm1` | Number || 10 | `1043` (Number), `1013` (Number) |
| `arm2` | Number || 11 | `1013` (Number), `1501` (Number) |
| `body` | Number || 5 | `31` (Number), `1029` (Number) |
| `ear1` | Integer || 13 | `1501` (Number), `343` (Number) |
| `ear2` | Integer || 10 | `1005` (Number), `1501` (Number) |
| `eye1` | Integer || 3 | `1013` (Number), `1069` (Number) |
| `eye2` | Integer || 3 | `1013` (Number), `1069` (Number) |
| `eyebrow1` | Integer || 1 | `1069` (Number) |
| `eyebrow2` | Integer || 1 | `1070` (Number) |
| `head` | Enum / Number || 6 | `1027` (Number), `1504` (Number) |
| `leg1` | Integer || 8 | `41` (Number), `1043` (Number) |
| `leg2` | Integer || 8 | `41` (Number), `1043` (Number) |
| `mouth` | Number || 8 | `1005` (Number), `1069` (Number) |
| `palette` | Enum / Integer || 17 | `Fighter` (Enum), `Medic` (Enum), `76` (Number), `78` (Number) |
| `tail` | Integer || 13 | `1504` (Number), `1503` (Number) |
| `texture` | Integer || 6 | `322` (Number), `19` (Number) |


### Object: `CaveFamilyEnrage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum || 6 | `CaveCatEnrageTwo` (Enum), `CaveCatEnrageOne` (Enum) |
| `count` | Array / Integer || 6 | `1` (Number), `0` (Number) |
| `tag` | Array / Enum || 6 | `cavefamily` (Enum) |


### Object: `CerberubsAggroTargetBehavior`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alert_form` | Enum || 1 | `Alert` (Enum) |
| `default_form` | Enum || 1 | `Normal` (Enum) |


### Object: `ChainKnockback`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `ChanceToBlockAndCounter`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `backstab_only` | Boolean || 1 | `true` (Boolean) |
| `chance` | Number || 1 | `100` (Number) |


### Object: `ChanceToForceEvent`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number || 1 | `25` (Number) |
| `event` | Enum || 1 | `Blessing` (Enum) |


### Object: `ChanceToFormChangeOnAbilityDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number || 1 | `15` (Number) |
| `form` | Enum / Integer || 1 | `Flop2` (Enum) |


### Object: `ChanceToSpitOnDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum || 7 | `MoonHandDrop` (Enum), `SpewerSpit` (Enum) |
| `backstabs_only` | Boolean || 1 | `true` (Boolean) |
| `chance_per_damage` | Integer || 3 | `0` (Number), `2` (Number) |
| `even_on_0_damage_if_knockback` | Boolean || 1 | `true` (Boolean) |
| `flat_chance` | Integer || 5 | `100` (Number), `50` (Number) |


### Object: `ChaosBossFormChangeGuide`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `active_pieces` | Array || 1 | `[Johnny Throb Flush]` (Array) |
| `passive_pieces` | Array || 1 | `[Host Nettle Bubs]` (Array) |
| `passives_health_threshold` | Integer || 1 | `50` (Number) |


### Object: `ChaosBossPieces`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `active_pieces` | Array || 1 | `[Johnny Throb Flush]` (Array) |
| `passive_pieces` | Array || 1 | `[Host Nettle Bubs]` (Array) |


### Object: `ChaosHeadDropIn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum || 1 | `ChaosSpawnIn` (Enum) |
| `new_music` | Enum || 1 | `chaos_boss_part2` (Enum) |
| `tag` | Array / Enum || 1 | `riftheadguardian` (Enum) |


### Object: `CharacterLightSource`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `color` | Array || 16 | `[.7 .8 .9]` (Array), `[1 1 1]` (Array) |
| `glow` | Array || 8 | `[1 .75 .5 .5]` (Array), `[1 1 1 1]` (Array) |
| `size` | Enum / Number || 16 | `1.7` (Number), `8` (Number) |


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
| `ability` | Enum || 2 | `Class` (Enum), `Colorless` (Enum) |
| `upgraded` | Boolean || 2 | `true` (Boolean) |


### Object: `Consumed`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `drop_on_death` | Boolean / Enum || 11 | `false` (Boolean), `true` (Boolean), `deferred` (Enum) |
| `mount_mode` | Boolean / Enum || 12 | `true` (Boolean), `auto` (Enum) |


### Object: `ConvertDamageToScaledStatus`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DelayedPain` | Integer || 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `stacks` | Enum / Integer || 1 | `3` (Number) |


### Object: `CounterAttack`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum || 5 | `StegoTailSwipe` (Enum), `neck_TentacleArmorCounter` (Enum) |
| `chance` | Number || 1 | `15` (Number) |
| `melee_only` | Boolean || 1 | `true` (Boolean) |
| `ranged_only` | Boolean || 1 | `true` (Boolean) |
| `without_orienting` | Boolean || 1 | `true` (Boolean) |


### Object: `CounterNextAttacks`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `CreateGlobalModifiers`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`BloodRain`](Engine_GlobalModifierKeys.md#object-bloodrain) | Integer / Object || 3 | `1` (Number), `{ ... }` (Object) |
| [`LowerAmbientLight`](Abilities_and_Spells.md#object-lowerambientlight) | Object || 3 | `50` (Number), `33` (Number), `{ ... }` (Object) |


### Object: `CritChanceUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `CyborgTurns`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`TakeBonusTurnWithAIControl`](Abilities_and_Spells.md#object-takebonusturnwithaicontrol) | Object || 1 | `{ ... }` (Object) |
| `stacks` | Enum / Integer || 1 | `1` (Number) |


### Object: `DamageUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `DeathChill`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `DeathRattleRevive`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum || 8 | `HitlerPulp2` (Enum), `HitlerPulp4` (Enum) |
| `even_if_stunned` | Boolean || 8 | `true` (Boolean) |


### Object: `DejaVu`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `DelayedAutoRevive`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `health` | Integer || 6 | `30` (Number), `15` (Number) |
| `rounds` | Integer || 6 | `1` (Number), `2` (Number) |


### Object: `DepressionAura`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `aura_effects_allies` | Boolean || 4 | `false` (Boolean) |
| `range` | Enum / Integer || 4 | `global` (Enum), `1` (Number) |
| `stacks` | Enum / Integer || 4 | `1` (Number) |


### Object: `DiceBehavior`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dice_size` | Integer || 1 | `6` (Number) |
| `knockback_damage` | Integer || 1 | `5` (Number) |


### Object: `DiesToElement`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `element` | Array / Enum || 1 | `Fire` (Enum) |
| `instant` | Boolean || 1 | `true` (Boolean) |


### Object: `DiesToPiercingAndSpikes`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `deferred` | Boolean || 1 | `true` (Boolean) |


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
| `ability` | Enum || 1 | `ShadowstepDodge` (Enum) |


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
| `exit_ability` | Enum || 1 | `DybbukReturn` (Enum) |
| `form` | Enum / Integer || 1 | `Possessing` (Enum) |


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
| `ability_damage_only` | Boolean || 1 | `true` (Boolean) |
| `override_hit_animation` | Boolean || 1 | `true` (Boolean) |
| `use_turn_animations` | Boolean || 1 | `true` (Boolean) |


### Object: `FaceLastDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `use_turn_animations` | Boolean || 1 | `true` (Boolean) |


### Object: `FinalBossBeamQueue`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `queue` | Enum || 1 | `TheChild_TargetBeam` (Enum) |
| `release` | Enum || 1 | `TheChild_ReleaseBeams` (Enum) |
| `transform` | Enum || 1 | `TheChild_TransformBoris` (Enum) |


### Object: `FinalBossBecomeTheChild`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `GlobalSpawnCharacter` | Enum || 1 | `MegaGuppy` (Enum) |
| `PlayBackground` | Integer || 1 | `1` (Number), `0` (Number) |
| [`SwitchMusic`](Abilities_and_Spells.md#object-switchmusic) | Object || 1 | `{ ... }` (Object) |


### Object: `FinalBossHitCountdownBoris`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object || 1 | `neck_ChefsApron` (Enum), `TheChild_TransformExplosive` (Enum), `{ ... }` (Object) |
| `icon` | Integer || 1 | `802` (Number) |
| `icon_ready` | Integer || 1 | `803` (Number) |
| `stacks` | Enum / Integer || 1 | `7` (Number) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |


### Object: `FinalBossHitCountdownExplosive`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object || 1 | `neck_ChefsApron` (Enum), `head_HitlersToupe` (Enum), `{ ... }` (Object) |
| `icon` | Integer || 1 | `800` (Number) |
| `icon_ready` | Integer || 1 | `801` (Number) |
| `stacks` | Enum / Integer || 1 | `7` (Number) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |


### Object: `FinalBossHitCountdownHoly`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon` | Integer || 1 | `804` (Number) |
| `icon_ready` | Integer || 1 | `805` (Number) |
| `stacks` | Enum / Integer || 1 | `7` (Number) |


### Object: `FinalBossPupils`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `look_at_offset` | Array || 1 | `[0 2.5 0]` (Array) |
| `radius` | Array / Integer || 1 | `13` (Number) |
| `reset_center_because_no_target_halflife` | Number || 1 | `.1` (String) |
| `reset_center_because_of_animation_halflife` | Number || 1 | `.05` (String) |
| `teleport_tracking_halflife` | Number || 1 | `.01` (String) |
| `tracking_acquisition_halflife` | Number || 1 | `.1` (String) |
| `virtual_head_position` | Array || 1 | `[11 2 11]` (Array) |


### Object: `FinalBossShieldHealth`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `break_ability` | Enum || 1 | `DestroyerBreakShield` (Enum) |
| `state_health` | Array || 1 | `[0 35 35 35 35 0]` (Array) |


### Object: `FinalBossSyncAnimations`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `other_character` | Enum || 1 | `MegaGuppy` (Enum) |
| [`other_form_change_abilities`](Characters_and_Bosses.md#object-other_form_change_abilities) | Object || 1 | `{ ... }` (Object) |


### Object: `Flammable`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `FlyDamageIncrease`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allies_only` | Boolean || 1 | `true` (Boolean) |
| `stacks` | Enum / Integer || 1 | `2` (Number) |


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
| `form` | Enum / Integer || 2 | `Rain` (Enum) |


### Object: `FormChangeHealthThreshold`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `count_shield` | Boolean || 1 | `true` (Boolean) |
| `form_above` | Enum || 3 | `Default` (Enum), `Full` (Enum) |
| `form_below` | Enum || 3 | `DesireMech` (Enum), `Standing2` (Enum) |
| [`threshold`](Items_and_Equipment.md#object-threshold) | Enum / Integer / Object || 3 | `X-4` (Enum), `25` (Number), `50` (Number) |


### Object: `FormChangeOffMap`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `form_offmap` | Enum || 8 | `Insane_Ceiling` (Enum), `SpawningPhase` (Enum) |
| `form_onmap` | Enum || 8 | `Default_Ground` (Enum), `Insane_Ground` (Enum) |


### Object: `FormChangeOnElementInfluence`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `element` | Array / Enum || 9 | `[fire]` (Array), `water` (Enum), `wind` (Enum) |
| `exclude` | Enum || 5 | `water` (Enum), `fire` (Enum) |
| `form` | Enum / Integer || 9 | `hot` (Enum), `default` (Enum) |
| `particle` | Enum || 5 | `FireExtinguish` (Enum) |
| `sfx` | Enum || 5 | `FireExtinguish` (Enum) |


### Object: `FormChangeWhileHasStatus`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `form_has` | Enum || 25 | `Primed` (Enum), `Full` (Enum) |
| `form_hasnot` | Enum || 30 | `Default` (Enum), `Empty` (Enum) |
| `status` | Enum || 35 | `T2CopyCatInternal` (Enum), `Grappling` (Enum) |


### Object: `FormChangeWhilePrimingAbility`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `not_priming` | Enum || 6 | `DualSword` (Enum), `SwordAndShield` (Enum) |
| `priming` | Enum || 6 | `DualSword_Primed` (Enum), `Priming` (Enum) |


### Object: `FormChanger`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Alert`](Characters_and_Bosses.md#object-alert) | Object || 1 | `{ ... }` (Object) |
| [`AllAlive`](Characters_and_Bosses.md#object-allalive) | Object || 3 | `{ ... }` (Object) |
| [`Angry`](Characters_and_Bosses.md#object-angry) | Object || 1 | `{ ... }` (Object) |
| [`Attacker`](Characters_and_Bosses.md#object-attacker) | Object || 1 | `{ ... }` (Object) |
| [`BellyFull`](Characters_and_Bosses.md#object-bellyfull) | Object || 1 | `{ ... }` (Object) |
| [`Big`](Characters_and_Bosses.md#object-big) | Object || 2 | `{ ... }` (Object) |
| [`BigHolding`](Characters_and_Bosses.md#object-bigholding) | Object || 1 | `{ ... }` (Object) |
| [`BigHoldingCat`](Characters_and_Bosses.md#object-bigholdingcat) | Object || 1 | `{ ... }` (Object) |
| [`Bishop`](Characters_and_Bosses.md#object-bishop) | Boolean (Flag) / Object || 1 | `(Flag)` (Boolean (Flag)), `{ ... }` (Object) |
| [`BlackHole`](Characters_and_Bosses.md#object-blackhole) | Object || 1 | `{ ... }` (Object) |
| [`Bomb`](Characters_and_Bosses.md#object-bomb) | Boolean (Flag) / Object || 1 | `(Flag)` (Boolean (Flag)), `{ ... }` (Object) |
| [`Boris`](Characters_and_Bosses.md#object-boris) | Enum / Object || 2 | `MegaGuppy_TransformBoris` (Enum), `{ ... }` (Object) |
| [`Bully`](Characters_and_Bosses.md#object-bully) | Object || 1 | `{ ... }` (Object) |
| [`Butcher`](Engine_LogicKeys.md#object-butcher) | Object || 1 | `[CAT_EMBARK_QUOTES_BUTCHER_1 CAT_EMBARK_QUOTES_BUTCHER_2 CAT_EMBARK_QUOTES_BUTCHER_3 CAT_EMBARK_QUOTES_BUTCHER_4 CAT_EMBARK_QUOTES_BUTCHER_5 CAT_EMBARK_QUOTES_BUTCHER_6 CAT_EMBARK_QUOTES_BUTCHER_7 CAT_EMBARK_QUOTES_BUTCHER_8 CAT_EMBARK_QUOTES_BUTCHER_9 CAT_EMBARK_QUOTES_BUTCHER_10]` (Array), `[CAT_RETURN_EARLY_QUOTES_BUTCHER_1 CAT_RETURN_EARLY_QUOTES_BUTCHER_2 CAT_RETURN_EARLY_QUOTES_BUTCHER_3 CAT_RETURN_EARLY_QUOTES_BUTCHER_4 CAT_RETURN_EARLY_QUOTES_BUTCHER_5]` (Array), `{ ... }` (Object) |
| [`CaveBaby`](Characters_and_Bosses.md#object-cavebaby) | Object || 1 | `{ ... }` (Object) |
| [`CaveMan`](Characters_and_Bosses.md#object-caveman) | Object || 2 | `{ ... }` (Object) |
| [`CaveManSpear`](Characters_and_Bosses.md#object-cavemanspear) | Object || 2 | `{ ... }` (Object) |
| [`CaveWoman`](Characters_and_Bosses.md#object-cavewoman) | Object || 1 | `{ ... }` (Object) |
| [`CaveWomanHasCat`](Characters_and_Bosses.md#object-cavewomanhascat) | Object || 1 | `{ ... }` (Object) |
| [`Charging`](Characters_and_Bosses.md#object-charging) | Object || 1 | `{ ... }` (Object) |
| [`Close`](Characters_and_Bosses.md#object-close) | Object || 1 | `{ ... }` (Object) |
| [`Colorless`](Engine_LogicKeys.md#object-colorless) | Array / Object || 1 | `[CAT_RETURN_EARLY_QUOTES_COLORLESS_1 CAT_RETURN_EARLY_QUOTES_COLORLESS_2 CAT_RETURN_EARLY_QUOTES_COLORLESS_3 CAT_RETURN_EARLY_QUOTES_COLORLESS_4 CAT_RETURN_EARLY_QUOTES_COLORLESS_5]` (Array), `[CAT_EMBARK_QUOTES_COLORLESS_1 CAT_EMBARK_QUOTES_COLORLESS_2 CAT_EMBARK_QUOTES_COLORLESS_3 CAT_EMBARK_QUOTES_COLORLESS_4 CAT_EMBARK_QUOTES_COLORLESS_5 CAT_EMBARK_QUOTES_COLORLESS_6 CAT_EMBARK_QUOTES_COLORLESS_7 CAT_EMBARK_QUOTES_COLORLESS_8]` (Array), `{ ... }` (Object) |
| [`Cultist`](Characters_and_Bosses.md#object-cultist) | Object || 1 | `{ ... }` (Object) |
| [`Damaged`](Characters_and_Bosses.md#object-damaged) | Object || 1 | `{ ... }` (Object) |
| [`Default`](Characters_and_Bosses.md#object-default) | Enum / Object || 37 | `release` (Enum), `{ ... }` (Object) |
| [`Default_Ceiling`](Characters_and_Bosses.md#object-default_ceiling) | Object || 1 | `{ ... }` (Object) |
| [`Default_Ground`](Characters_and_Bosses.md#object-default_ground) | Object || 1 | `{ ... }` (Object) |
| [`DesireMech`](Characters_and_Bosses.md#object-desiremech) | Object || 1 | `{ ... }` (Object) |
| [`Die`](Characters_and_Bosses.md#object-die) | Integer / Object || 1 | `6` (Number), `1` (Number), `{ ... }` (Object) |
| [`Down`](Characters_and_Bosses.md#object-down) | Object || 3 | `{ ... }` (Object) |
| [`Druid`](Engine_LogicKeys.md#object-druid) | Array / Object || 1 | `[CAT_RETURN_EARLY_QUOTES_DRUID_1 CAT_RETURN_EARLY_QUOTES_DRUID_2 CAT_RETURN_EARLY_QUOTES_DRUID_3 CAT_RETURN_EARLY_QUOTES_DRUID_4 CAT_RETURN_EARLY_QUOTES_DRUID_5]` (Array), `[CAT_VS_BOSS_QUOTES_DRUID_1 CAT_VS_BOSS_QUOTES_DRUID_2 CAT_VS_BOSS_QUOTES_DRUID_3 CAT_VS_BOSS_QUOTES_DRUID_4 CAT_VS_BOSS_QUOTES_DRUID_5 CAT_VS_BOSS_QUOTES_DRUID_6 CAT_VS_BOSS_QUOTES_DRUID_7 CAT_VS_BOSS_QUOTES_DRUID_8 CAT_VS_BOSS_QUOTES_DRUID_9]` (Array), `{ ... }` (Object) |
| [`Drunker`](Characters_and_Bosses.md#object-drunker) | Object || 1 | `{ ... }` (Object) |
| [`DualSword`](Characters_and_Bosses.md#object-dualsword) | Object || 1 | `{ ... }` (Object) |
| [`DualSword_Primed`](Characters_and_Bosses.md#object-dualsword_primed) | Object || 1 | `{ ... }` (Object) |
| [`Dumb`](Characters_and_Bosses.md#object-dumb) | Integer / Object || 1 | `3` (Number), `{ ... }` (Object) |
| [`Empty`](Characters_and_Bosses.md#object-empty) | Object || 2 | `{ ... }` (Object) |
| [`Explody`](Characters_and_Bosses.md#object-explody) | Object || 1 | `{ ... }` (Object) |
| [`Explosive`](Characters_and_Bosses.md#object-explosive) | Enum / Object || 2 | `MegaGuppy_TransformExplosive` (Enum), `{ ... }` (Object) |
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
| [`Full`](Characters_and_Bosses.md#object-full) | Object || 3 | `{ ... }` (Object) |
| [`Grappling`](Characters_and_Bosses.md#object-grappling) | Object || 1 | `{ ... }` (Object) |
| [`Grown`](Characters_and_Bosses.md#object-grown) | Object || 1 | `{ ... }` (Object) |
| [`GuaranteedJackpot`](Characters_and_Bosses.md#object-guaranteedjackpot) | Object || 1 | `{ ... }` (Object) |
| [`Guarding`](Characters_and_Bosses.md#object-guarding) | Object || 1 | `{ ... }` (Object) |
| [`HalfDead`](Characters_and_Bosses.md#object-halfdead) | Object || 1 | `{ ... }` (Object) |
| [`HasCat`](Characters_and_Bosses.md#object-hascat) | Object || 5 | `{ ... }` (Object) |
| [`HasDeadCat`](Characters_and_Bosses.md#object-hasdeadcat) | Object || 1 | `{ ... }` (Object) |
| [`HasRock`](Characters_and_Bosses.md#object-hasrock) | Object || 1 | `{ ... }` (Object) |
| [`Headless`](Characters_and_Bosses.md#object-headless) | Object || 1 | `{ ... }` (Object) |
| [`Hint_CrackedVisuals`](Characters_and_Bosses.md#object-hint_crackedvisuals) | Object || 1 | `{ ... }` (Object) |
| [`Hint_CrackedVisuals2`](Characters_and_Bosses.md#object-hint_crackedvisuals2) | Object || 1 | `{ ... }` (Object) |
| [`Hint_CrackedVisuals3`](Characters_and_Bosses.md#object-hint_crackedvisuals3) | Object || 1 | `{ ... }` (Object) |
| [`Holding`](Characters_and_Bosses.md#object-holding) | Object || 2 | `{ ... }` (Object) |
| [`Holy`](Characters_and_Bosses.md#object-holy) | Enum / Object || 2 | `MegaGuppy_TransformHoly` (Enum), `{ ... }` (Object) |
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
| [`Normal`](Characters_and_Bosses.md#object-normal) | Integer / Object || 11 | `0` (Number), `{ ... }` (Object) |
| [`NormalFull`](Characters_and_Bosses.md#object-normalfull) | Integer / Object || 1 | `0` (Number), `{ ... }` (Object) |
| [`NotPriming`](Characters_and_Bosses.md#object-notpriming) | Object || 2 | `{ ... }` (Object) |
| [`Nuke`](Characters_and_Bosses.md#object-nuke) | Object || 1 | `{ ... }` (Object) |
| [`Obey`](Characters_and_Bosses.md#object-obey) | Integer / Object || 1 | `1` (Number), `{ ... }` (Object) |
| [`Off`](Characters_and_Bosses.md#object-off) | Object || 1 | `{ ... }` (Object) |
| [`OffMap`](Characters_and_Bosses.md#object-offmap) | Object || 4 | `{ ... }` (Object) |
| [`OffScreen`](Characters_and_Bosses.md#object-offscreen) | Object || 1 | `{ ... }` (Object) |
| [`OneAlive`](Characters_and_Bosses.md#object-onealive) | Object || 3 | `{ ... }` (Object) |
| [`OneEye`](Characters_and_Bosses.md#object-oneeye) | Object || 1 | `{ ... }` (Object) |
| [`Open`](Characters_and_Bosses.md#object-open) | Object || 1 | `{ ... }` (Object) |
| [`OpenCat`](Characters_and_Bosses.md#object-opencat) | Object || 1 | `{ ... }` (Object) |
| [`Out`](Characters_and_Bosses.md#object-out) | Object || 1 | `{ ... }` (Object) |
| [`Possessing`](Characters_and_Bosses.md#object-possessing) | Object || 1 | `{ ... }` (Object) |
| [`Primed`](Characters_and_Bosses.md#object-primed) | Object || 1 | `{ ... }` (Object) |
| [`Priming`](Characters_and_Bosses.md#object-priming) | Object || 2 | `{ ... }` (Object) |
| [`Psychic`](Engine_LogicKeys.md#object-psychic) | Array / Object || 1 | `[CAT_EMBARK_QUOTES_PSYCHIC_1 CAT_EMBARK_QUOTES_PSYCHIC_2 CAT_EMBARK_QUOTES_PSYCHIC_3 CAT_EMBARK_QUOTES_PSYCHIC_4 CAT_EMBARK_QUOTES_PSYCHIC_5 CAT_EMBARK_QUOTES_PSYCHIC_6 CAT_EMBARK_QUOTES_PSYCHIC_7 CAT_EMBARK_QUOTES_PSYCHIC_8 CAT_EMBARK_QUOTES_PSYCHIC_9 CAT_EMBARK_QUOTES_PSYCHIC_10]` (Array), `[CAT_RETURN_QUOTES_PSYCHIC_1 CAT_RETURN_QUOTES_PSYCHIC_2 CAT_RETURN_QUOTES_PSYCHIC_3 CAT_RETURN_QUOTES_PSYCHIC_4 CAT_RETURN_QUOTES_PSYCHIC_5]` (Array), `{ ... }` (Object) |
| [`Pulp2`](Characters_and_Bosses.md#object-pulp2) | Object || 1 | `{ ... }` (Object) |
| [`Pulp3`](Characters_and_Bosses.md#object-pulp3) | Object || 1 | `{ ... }` (Object) |
| [`Pulp4`](Characters_and_Bosses.md#object-pulp4) | Object || 1 | `{ ... }` (Object) |
| [`Pulp5`](Characters_and_Bosses.md#object-pulp5) | Object || 1 | `{ ... }` (Object) |
| [`Pulp6`](Characters_and_Bosses.md#object-pulp6) | Object || 1 | `{ ... }` (Object) |
| [`Pulp7`](Characters_and_Bosses.md#object-pulp7) | Object || 1 | `{ ... }` (Object) |
| [`Rage`](Characters_and_Bosses.md#object-rage) | Object || 10 | `{ ... }` (Object) |
| [`Rain`](Characters_and_Bosses.md#object-rain) | Object || 2 | `4` (Number), `1` (Number), `{ ... }` (Object) |
| [`Sitting`](Characters_and_Bosses.md#object-sitting) | Object || 1 | `{ ... }` (Object) |
| [`Small`](Characters_and_Bosses.md#object-small) | Object || 2 | `{ ... }` (Object) |
| [`SmallHolding`](Characters_and_Bosses.md#object-smallholding) | Object || 1 | `{ ... }` (Object) |
| [`SmallHoldingCat`](Characters_and_Bosses.md#object-smallholdingcat) | Object || 1 | `{ ... }` (Object) |
| [`SpawningPhase`](Characters_and_Bosses.md#object-spawningphase) | Object || 1 | `{ ... }` (Object) |
| [`SquirrelForm`](Characters_and_Bosses.md#object-squirrelform) | Object || 2 | `{ ... }` (Object) |
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
| [`Turtled`](Characters_and_Bosses.md#object-turtled) | Object || 2 | `{ ... }` (Object) |
| [`TwoAlive`](Characters_and_Bosses.md#object-twoalive) | Object || 3 | `{ ... }` (Object) |
| [`TwoEyes`](Characters_and_Bosses.md#object-twoeyes) | Object || 1 | `{ ... }` (Object) |
| [`Unlit`](Characters_and_Bosses.md#object-unlit) | Object || 1 | `{ ... }` (Object) |
| `Unmounted` | Object || 1 | `{ ... }` (Object) |
| [`Unwashed`](Characters_and_Bosses.md#object-unwashed) | Object || 1 | `{ ... }` (Object) |
| [`Up`](Characters_and_Bosses.md#object-up) | Object || 3 | `{ ... }` (Object) |
| [`Washed`](Characters_and_Bosses.md#object-washed) | Object || 1 | `{ ... }` (Object) |
| [`Washer`](Characters_and_Bosses.md#object-washer) | Object || 1 | `{ ... }` (Object) |
| [`Water`](Characters_and_Bosses.md#object-water) | Object || 1 | `{ ... }` (Object) |
| [`WereMan`](Characters_and_Bosses.md#object-wereman) | Object || 1 | `{ ... }` (Object) |
| [`Zealot`](Characters_and_Bosses.md#object-zealot) | Object || 1 | `{ ... }` (Object) |
| [`ZealotBomb`](Characters_and_Bosses.md#object-zealotbomb) | Object || 1 | `{ ... }` (Object) |
| [`active`](Characters_and_Bosses.md#object-active) | Object || 2 | `{ ... }` (Object) |
| [`default`](Characters_and_Bosses.md#object-default) | Enum / Object || 4 | `{ ... }` (Object) |
| [`hot`](Characters_and_Bosses.md#object-hot) | Object || 4 | `{ ... }` (Object) |
| `initial_form` | Enum / Integer || 56 | `Default` (Enum), `Normal` (Enum), `1` (Number), `5` (Number) |
| [`passive`](Characters_and_Bosses.md#object-passive) | Object || 2 | `{ ... }` (Object) |
| `sync_brain_patterns` | Boolean || 1 | `true` (Boolean) |


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
| [`Tangled`](Abilities_and_Spells.md#object-tangled) | Array / Integer / Object || 1 | `[1 .1]` (Array), `[1 .33]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |


### Object: `GlobalMeleeRevengeDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `knockback` | Enum / Integer || 1 | `5` (Number) |


### Object: `HPAltStates`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `clipname` | Enum || 1 | `poopmain` (Enum) |
| `thresholds` | Array || 1 | `[[ 1 0 ] [ 0 3 ]]` (Array) |


### Object: `HealNeighborsEachTurn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allies_only` | Boolean || 1 | `true` (Boolean) |
| `stacks` | Enum / Integer || 1 | `3` (Number) |


### Object: `HealingAura`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `HealthPickup`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `anything_eats` | Boolean || 4 | `true` (Boolean) |
| `force_frame` | Integer || 1 | `12` (Number) |
| `frame_range` | Array || 15 | `[1 2]` (Array), `[5 5]` (Array) |
| `stacks` | Enum / Integer || 15 | `7` (Number), `10` (Number) |
| `stored_food_value` | Integer || 15 | `4` (Number), `2` (Number) |


### Object: `HealthRegenUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `HitlerExecute`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum || 1 | `HitlerShoot` (Enum) |
| `tag` | Array / Enum || 1 | `grown_hitler_clone` (Enum) |
| [`threshold`](Items_and_Equipment.md#object-threshold) | Enum / Integer / Object || 1 | `15` (Number) |


### Object: `Hypomania`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |


### Object: `ImmediateAbilityReaction`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum || 13 | `FormShrinkTwoSnakey` (Enum), `ButtWeb_AlreadyEnraged` (Enum) |
| `ability_damage_only` | Boolean || 6 | `true` (Boolean) |
| `backstabs_only` | Boolean || 2 | `true` (Boolean) |
| `buddy_damage_only` | Boolean || 1 | `true` (Boolean) |
| `damage_threshold` | Integer || 2 | `10` (Number) |
| `even_if_blocked` | Boolean || 2 | `true` (Boolean) |
| `even_if_stunned` | Boolean || 2 | `true` (Boolean) |
| `health_threshold` | Integer || 2 | `50` (Number), `70` (Number) |
| `target_furthest_valid` | Boolean || 1 | `true` (Boolean) |


### Object: `Immobile`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `ImmortalLeeches`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `ItemAuxTransform`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ge` | Array || 2 | `[20 BlackShard_Glowing]` (Array), `[10 NuclearKnife_Glowing]` (Array) |
| `le` | Array || 3 | `[50 MoneyBag_Large]` (Array), `[10 MoneyBag_Small]` (Array) |
| `lt` | Array || 1 | `[10 NuclearKnife]` (Array) |


### Object: `JohnnyNeedsWashing`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `form_unwashed` | Enum || 1 | `Unwashed` (Enum) |
| `form_washed` | Enum || 1 | `Washed` (Enum) |


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
| `stacks` | Enum / Integer || 1 | `1` (Number) |
| `tickdown_this_turn` | Boolean || 1 | `true` (Boolean) |


### Object: `ManaPickup`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `frame_range` | Array || 3 | `[6 6]` (Array), `[1 2]` (Array) |
| `stacks` | Enum / Integer || 3 | `4` (Number), `6` (Number) |


### Object: `MegaDinoDropController`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `head_drop` | Enum || 1 | `MD_HeadDrop` (Enum) |
| `leg_leave` | Enum || 1 | `MD_LegLeave` (Enum) |
| `leg_return` | Enum || 1 | `MD_LegReturn` (Enum) |
| `stable_legs` | Integer || 1 | `3` (Number) |


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
| [`Cleanse`](Engine_StatusAndPassiveKeys.md#object-cleanse) | Integer / Object || 1 | `1` (Number), `0` (Number), `{ ... }` (Object) |
| `sound_event` | Enum || 1 | `EatAntidote` (Enum) |


### Object: `MonkCatReactionAbilities`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `attack` | Enum || 1 | `attack` (Enum) |
| `move` | Enum || 1 | `move` (Enum) |
| `spell` | Enum || 1 | `MCHadouken` (Enum) |
| `trinket` | Enum || 1 | `MCHadouken` (Enum) |
| `weapon` | Enum || 1 | `attack` (Enum) |


### Object: `MotherGrowController`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`eat_damage`](Characters_and_Bosses.md#object-eat_damage) | Object || 1 | `{ ... }` (Object) |
| `tumor_object` | Enum || 1 | `MotherTumor` (Enum) |


### Object: `MotherTumorPassive`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Cat`](Characters_and_Bosses.md#object-cat) | Object || 1 | `{ ... }` (Object) |
| [`NonCat`](Characters_and_Bosses.md#object-noncat) | Object || 1 | `{ ... }` (Object) |
| `considered_forms` | Array || 1 | `[Big BigHolding BigHoldingCat]` (Array) |
| `grow_ability` | Enum || 1 | `MotherTumorGrow` (Enum) |
| `pass_ani` | Enum || 1 | `pass` (Enum) |
| `receive_ani` | Enum || 1 | `receive` (Enum) |


### Object: `MotherTumorSpawnInCapture`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Cat`](Characters_and_Bosses.md#object-cat) | Object || 2 | `{ ... }` (Object) |
| [`NonCat`](Characters_and_Bosses.md#object-noncat) | Object || 2 | `{ ... }` (Object) |
| [`Nothing`](Characters_and_Bosses.md#object-nothing) | Object || 1 | `{ ... }` (Object) |


### Object: `Mount`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `eject_ability` | Enum || 1 | `MechSuitEject` (Enum) |
| `enter_ability` | Enum || 1 | `EnterMech` (Enum) |


### Object: `MoveAfterAnyAttemptedAttack`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `weights` | Array / Enum || 1 | `bat_chaos_runaway` (Enum) |


### Object: `MoveAwayFromDamageSource`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `move_ability` | Enum || 1 | `BirdFly` (Enum) |


### Object: `MoveAwayWhenEnemyAdjacent`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `move_ability` | Enum || 1 | `YA_Jetpack` (Enum) |
| `once_per_turn` | Boolean || 1 | `true` (Boolean) |
| `weights` | Array / Enum || 1 | `stay_far_always_move` (Enum) |


### Object: `MoveQuivered`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `MoveTowardsKillers`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `character_filter` | Array || 3 | `[SpiderCat TallSpiderCat]` (Array) |
| `move_ability` | Enum || 3 | `SpiderReturn` (Enum) |


### Object: `MultiSpawnOnDeath`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `count` | Array / Integer || 1 | `[0 2]` (Array) |
| `obj` | Array / Enum || 1 | `Maggot` (Enum) |


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
| `chance` | Number || 1 | `10` (Number) |
| `object` | Array / Enum || 1 | `CharmedDip` (Enum) |


### Object: `Paranoia`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |


### Object: `PassiveIfStrAuxEquals`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object || 7 | `{ ... }` (Object) |
| `value` | Enum || 7 | `int` (Enum), `spd` (Enum) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 7 |


### Object: `PassiveIfWeaponIsUsable`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Brace`](Events_and_Encounters.md#object-brace) | Enum / Integer / Object || 2 | `[1 .5]` (Array), `10` (Number), `4` (Number), `{ ... }` (Object) |


### Object: `PassiveWhenDead`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AutocastEachRound`](Abilities_and_Spells.md#object-autocasteachround) | Enum / Object || 1 | `SpiderReturn` (Enum), `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |


### Object: `PassiveWhenOnTile`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object || 7 | `{ ... }` (Object) |
| `tile` | Array / Enum || 7 | `[WaterTile]` (Array), `[TallGrassTile TallFlowerTile]` (Array) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 7 |


### Object: `PassiveWhileHasDurability`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`MovementReaction`](Characters_and_Bosses.md#object-movementreaction) | Object || 1 | `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |


### Object: `PassiveWhileNotHasStatus`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object || 2 | `{ ... }` (Object) |
| `status` | Enum || 2 | `DemonicGlyph_Movement` (Enum), `ExistUntilIdleUpkeep` (Enum) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |


### Object: `PassiveWhileShielded`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Integer || 1 | `[1 .5]` (Array), `4` (Number), `3` (Number), `{ ... }` (Object) |


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
| `chance` | Number || 1 | `25` (Number) |
| `object` | Array / Enum || 1 | `Poop` (Enum) |


### Object: `ProtectTargetedAllies`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum || 2 | `SwapPositions_TankCat` (Enum) |
| `target_filter` | Enum || 2 | `any` (Enum), `Kitten` (Enum) |


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
| [`self_damage`](Abilities_and_Spells.md#object-self_damage) | Boolean / Integer / Object || 8 | `2` (Number) |


### Object: `RefreshEquipmentAbilityOnElement`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `element` | Array / Enum || 2 | `Electric` (Enum) |
| `text` | String || 2 | `"COMBAT_POPUP_RECHARGED"` (String) |


### Object: `RunWhenLastPlayerCatIsCharmed`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allow_decision_mid_turn` | Boolean || 1 | `true` (Boolean) |
| `legacy_savekey` | Enum || 1 | `Legacy_Marshmallow_StolenCatID` (Enum) |


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
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |


### Object: `ScaledStatusOnHolyShieldBlock`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`RandomMagicMissile`](Abilities_and_Spells.md#object-randommagicmissile) | Integer / Object || 1 | `[1 .5]` (Array), `6` (Number), `10` (Number), `{ ... }` (Object) |


### Object: `ScalingAttackAnimation`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`default`](Characters_and_Bosses.md#object-default) | Enum / Object || 1 | `bite1` (Enum) |
| `thresholds` | Array || 1 | `[[ 5 bite2 ] [ 10 bite3 ]]` (Array) |


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
| `include_coins` | Boolean || 1 | `true` (Boolean) |


### Object: `ShoulderCheck`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `ShovingMatch`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `SkipFirstRounds`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `pop_chance` | Integer || 1 | `50` (Number) |
| `stacks` | Enum / Integer || 1 | `2` (Number) |


### Object: `SlotMachineRollPool`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`SlotResult_Explode`](Engine_LogicKeys.md#object-slotresult_explode) | Integer / Object || 1 | `1` (Number), `{ ... }` (Object) |
| [`SlotResult_Jackpot_Coins`](Engine_LogicKeys.md#object-slotresult_jackpot_coins) | Integer / Object || 2 | `1` (Number), `{ ... }` (Object) |
| [`SlotResult_Nothing`](Engine_LogicKeys.md#object-slotresult_nothing) | Integer / Object || 1 | `7` (Number), `{ ... }` (Object) |
| [`SlotResult_RandomPickup`](Engine_LogicKeys.md#object-slotresult_randompickup) | Integer / Object || 1 | `11` (Number), `{ ... }` (Object) |


### Object: `Slow`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `SmallRockBehavior`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chain` | Boolean || 2 | `true` (Boolean) |
| `damage` | Equation || 4 | `9` (Equation), `5` (Equation) |
| `knockback` | Enum / Integer || 4 | `1` (Number), `5` (Number) |


### Object: `SpawnCatCopyWhenDowned`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `object` | Array / Enum || 2 | `PlayerCat_NecroShade` (Enum), `PlayerCat_AncestralShade` (Enum) |
| `prevent_chain_tag` | Enum || 2 | `necroset_shade` (Enum), `ancestorset_shade` (Enum) |


### Object: `SpawnExtraThingsOnBattleStart`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `number` | Array / Integer || 31 | `[3 8]` (Array), `[0 2]` (Array), `3` (Number), `1` (Number) |
| `object` | Array / Enum || 23 | `[Spookie Scary Tatters Wisp Wisp Wisp]` (Array), `[Bombchu Deathbot RoboVacuum TinkererTurret]` (Array), `NeutralToad` (Enum), `Poop` (Enum) |
| `tile` | Array / Enum || 7 | `TallGrassTile` (Enum), `FireTile` (Enum) |
| `trap` | Enum || 2 | `BearTrap` (Enum), `LandMine` (Enum) |


### Object: `SpawnItemLinkedFamiliar`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `break_on_pop_only` | Boolean || 2 | `true` (Boolean) |
| `object` | Array / Enum || 2 | `PyrophinaFamiliar` (Enum), `ZaratanaFamiliar` (Enum) |


### Object: `SpawnObjectOnPopCorpse`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `count` | Array / Integer || 1 | `2` (Number) |
| `except_tiny` | Boolean || 1 | `true` (Boolean) |
| `object` | Array / Enum || 1 | `CharmedTinySpider` (Enum) |


### Object: `SpawnOnDeath`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`additional_statuses`](Characters_and_Bosses.md#object-additional_statuses) | Object || 1 | `{ ... }` (Object) |
| `faction` | Enum || 4 | `enemies` (Enum), `allies` (Enum) |
| `obj` | Array / Enum || 4 | `[Spookie Spookie Scary Coin2 Coin3 Coin4]` (Array), `[Kitten Kitten TomTom TomTom Mangy Mangy CatCaller CatCaller GlassSpitter SpiderCat...]` (Array), `BeefyCharmedLeech` (Enum), `RiftKitten` (Enum) |


### Object: `SpawnRandomPickupsOnTaggedUnitKilled`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `count` | Array / Integer || 1 | `[2 3]` (Array) |
| `tag` | Array / Enum || 1 | `poop` (Enum) |


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
| `stacks` | Enum / Integer || 3 | `1` (Number) |


### Object: `StatDependentPassive`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AddDamageToBasicAttack` | String || 1 | `4` (Number), `1` (Number), `"min(min(min(min(min(min(str,dex),int),con),lck),spd),cha)-2"` (String) |


### Object: `StatusAdjacentOnTheirTurnEnd`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ForceMoveAway` | Integer || 1 | `1` (Number), `{ ... }` (Object) |


### Object: `StatusAfterXTurns`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object || 2 | `neck_ChefsApron` (Enum), `CancerExplode` (Enum), `{ ... }` (Object) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |


### Object: `StatusAllCharactersOnSpawn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Else`](Abilities_and_Spells.md#object-else) | Object || 1 | `{ ... }` (Object) |
| `Poison` | Array / Integer || 1 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |


### Object: `StatusCollector`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Poison` | Array / Integer || 4 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |
| [`Slow`](#object-slow) | Array / Enum / Integer / Object || 4 | `[1 .1]` (Array), `[1 .25]` (Array), `-1` (Number), `3` (Number), `{ ... }` (Object) |
| `StrengthUp` | Enum / Integer || 7 | `[1 .5]` (Array), `4` (Number), `-2` (Number), `{ ... }` (Object) |


### Object: `StatusEachRoundBegin`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `NonStackingShield` | Number || 8 | `3` (Number), `8` (Number) |


### Object: `StatusEachRoundEnd`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`DoDamage`](Abilities_and_Spells.md#object-dodamage) | Object || 1 | `{ ... }` (Object) |
| [`UseAbility`](Abilities_and_Spells.md#object-useability) | Enum / Object || 1 | `GirlDinoPoop` (Enum), `Spit` (Enum), `{ ... }` (Object) |


### Object: `StatusEachTurnBeginIfHasStatus`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AllStatsUp` | Enum / Integer || 1 | `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `DamageUp` | Integer / String || 1 | `[1 .5]` (Array), `-2` (Number), `3` (Number), `{ ... }` (Object) |
| `HealthGain` | Integer || 1 | `2*X` (Enum), `3*X` (Enum), `10` (Number), `4` (Number) |
| `animation` | Enum || 1 | `pulse3` (Enum) |
| `consume` | Boolean || 1 | `true` (Boolean) |
| `status` | Enum || 1 | `Counterspell` (Enum) |


### Object: `StatusEachTurnEndIfEnabledAtStartOfTurn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object || 1 | `neck_ChefsApron` (Enum), `T2UnClone` (Enum), `{ ... }` (Object) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |


### Object: `StatusEveryXSpellCastsEachTurn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthGain` | Integer || 1 | `2*X` (Enum), `3*X` (Enum), `10` (Number), `4` (Number) |
| `stacks` | Enum / Integer || 1 | `3` (Number) |


### Object: `StatusIfDidntMove`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Charge` | Integer || 1 | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |


### Object: `StatusIfUnusedActPoints`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`BackflipWhenTargeted`](Abilities_and_Spells.md#object-backflipwhentargeted) | Enum / Integer / Object || 1 | `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| [`Craft`](Abilities_and_Spells.md#object-craft) | Object || 1 | `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |


### Object: `StatusOnBackstab`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthGain` | Integer || 1 | `2*X` (Enum), `3*X` (Enum), `10` (Number), `4` (Number) |
| `SerratedClaws` | Integer || 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |


### Object: `StatusOnBreak`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ApplyToRandomPartyMemberIfPossible`](Abilities_and_Spells.md#object-applytorandompartymemberifpossible) | Object || 1 | `{ ... }` (Object) |
| [`Bruise`](#object-bruise) | Array / Integer / Object || 3 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `ConstitutionUp` | Array / Enum / Integer || 1 | `[1 .5]` (Array), `-1` (Number), `-2` (Number), `{ ... }` (Object) |
| `DexterityUp` | Enum / Integer || 1 | `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| [`FindItemFromPool`](Abilities_and_Spells.md#object-finditemfrompool) | Enum / Object || 3 | `chapter_specific_item` (Enum), `chapter_common` (Enum), `{ ... }` (Object) |
| `HealthGain` | Integer || 3 | `2*X` (Enum), `3*X` (Enum), `10` (Number), `4` (Number) |
| `HealthRegenUp` | Integer || 3 | `[1 .5]` (Array), `4` (Number), `3` (Number), `{ ... }` (Object) |
| `IntelligenceUp` | Enum / Integer || 1 | `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object || 1 | `BestBud` (Enum), `Maggot` (Enum), `{ ... }` (Object) |
| `StrengthUp` | Enum / Integer || 1 | `[1 .5]` (Array), `4` (Number), `-2` (Number), `{ ... }` (Object) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 20 |


### Object: `StatusOnDie`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`FindItemFromPool`](Abilities_and_Spells.md#object-finditemfrompool) | Enum / Object || 1 | `chapter_specific_item` (Enum), `chapter_common` (Enum), `{ ... }` (Object) |
| [`RandomMagicMissile`](Abilities_and_Spells.md#object-randommagicmissile) | Integer / Object || 1 | `[1 .5]` (Array), `10` (Number), `6` (Number), `{ ... }` (Object) |
| `RemoveAmbientLightEffects` | Number || 1 | `4` (Number), `.5` (String) |
| [`ScatterCoins`](Abilities_and_Spells.md#object-scattercoins) | Object || 1 | `[1 .5]` (Array), `5` (Number), `{ ... }` (Object) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 9 |


### Object: `StatusOnDodge`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DodgeChance_Status` | Integer || 1 | `[1 .5]` (Array), `15` (Number), `66` (Number), `{ ... }` (Object) |


### Object: `StatusOnEnemyCastSpell`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AllStatsUp` | Enum / Integer || 1 | `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `HealthGain` | Integer || 1 | `2*X` (Enum), `3*X` (Enum), `8` (Number), `10` (Number) |


### Object: `StatusOnEnemyConfused`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ImmediateUseAbility`](Engine_StatusAndPassiveKeys.md#object-immediateuseability) | Enum / Object || 1 | `cm_Lard_Impl` (Enum), `tk_ButterBean_Mega` (Enum), `{ ... }` (Object) |


### Object: `StatusOnEnemyDeath`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Charge` | Integer || 1 | `[1 .5]` (Array), `3` (Number), `4` (Number), `{ ... }` (Object) |


### Object: `StatusOnFallAsleep`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AllStatsUp` | Enum / Integer || 1 | `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `FillMana` | Integer || 1 | `[1 .25]` (Array), `[1 .10]` (Array), `1` (Number) |
| `HealRandomInjury` | Integer || 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |


### Object: `StatusOnFullMana`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_OncePerBattle`](Abilities_and_Spells.md#object-conditional_onceperbattle) | Object || 1 | `{ ... }` (Object) |


### Object: `StatusOnSetPieceBreak`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`FindItemFromPool`](Abilities_and_Spells.md#object-finditemfrompool) | Enum / Object || 1 | `chapter_specific_item` (Enum), `consumables` (Enum), `{ ... }` (Object) |
| `PermanentCharisma` | Integer || 1 | `1` (Number), `2` (Number) |
| `PermanentConstitution` | Integer || 1 | `-1` (Number), `-2` (Number) |
| `PermanentDexterity` | Integer || 1 | `1` (Number), `2` (Number) |
| `PermanentIntelligence` | Integer || 1 | `1` (Number), `2` (Number) |
| `PermanentLuck` | Integer || 1 | `1` (Number), `2` (Number) |
| `PermanentSpeed` | Integer || 1 | `1` (Number), `2` (Number) |
| `PermanentStrength` | Integer || 1 | `1` (Number), `2` (Number) |
| `set` | Array / Enum || 1 | `Recycled` (Enum) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |


### Object: `StatusOnSpawnIn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CaptureFamiliar` | Integer || 1 | `1` (Number) |
| `SetHealth` | Integer || 1 | `100` (Number), `50` (Number) |


### Object: `StatusOnTakeHealthOrShieldDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_GoodRoll`](Abilities_and_Spells.md#object-conditional_goodroll) | Object || 1 | `{ ... }` (Object) |
| `DivineShield` | Array / Integer || 2 | `[1 .33]` (Array), `[1 .5]` (Array), `4` (Number), `1` (Number), `{ ... }` (Object) |
| [`Metronome`](Abilities_and_Spells.md#object-metronome) | Boolean (Flag) / Number / Object || 1 | `(Flag)` (Boolean (Flag)), `1` (Number), `2` (Number), `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |


### Object: `StatusOverlappingCharactersAndDie`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Poison` | Array / Integer || 1 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |


### Object: `StatusRandomEnemiesOnBattleStart`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Bleed` | Array / Integer || 1 | `[1 .1]` (Array), `[3 .1]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |
| `Charmed` | Array / Enum / Integer || 1 | `[1 .1+.02*cha]` (Array), `[1 .25]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| [`Confusion`](#object-confusion) | Array / Integer / Object || 1 | `[2 .15]` (Array), `[1 .1]` (Array), `3` (Number), `4` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer || 3 | `[1 .1]` (Array), `[1 .05]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| `Freeze` | Array / Integer || 1 | `[1 .1]` (Array), `[1 0.15]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |


### Object: `StatusWhenStatusCompletelyRemoved`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`UseAbility`](Abilities_and_Spells.md#object-useability) | Enum / Object || 1 | `GirlDinoPoop` (Enum), `TormentorRuneAbsorb` (Enum), `{ ... }` (Object) |
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
| `cleanse_on_apply` | Boolean || 1 | `false` (Boolean) |


### Object: `SupportDieInsteadOfRun`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alt_dead_ani` | Enum || 1 | `off` (Enum) |
| `alt_dying_ani` | Enum || 1 | `shutdown` (Enum) |


### Object: `SupportFormChangeInsteadOfRun`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum || 2 | `TVChangeDie` (Enum), `SBotAnger` (Enum) |
| `wait_till_turn` | Boolean || 1 | `true` (Boolean) |


### Object: `SwimmingFormChange`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `form_in` | Enum || 1 | `Water` (Enum) |
| `form_out` | Enum || 1 | `Out` (Enum) |


### Object: `SyncFormsWithBuddy`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `no_buddy` | Enum || 1 | `Rage` (Enum) |


### Object: `T3HitlerSpawningPhase`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `spell_use_groups` | Array || 1 | `[[ T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk T3Spawn_Tank...]` (Array) |


### Object: `TVBotScreen`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Die`](Characters_and_Bosses.md#object-die) | Integer / Object || 1 | `6` (Number), `1` (Number), `{ ... }` (Object) |
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
| `move_ability` | Enum || 1 | `T2GoopRun` (Enum) |
| `move_weights` | Enum || 1 | `stay_far_always_move` (Enum) |


### Object: `TerminatorChase`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum || 1 | `T1ChokeReaction` (Enum) |
| `move` | Enum || 1 | `MoveOne` (Enum) |


### Object: `TerminatorSkin`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `groups` | Array || 1 | `[{ stacks 48 ParticleBurst Gibs_terminatorskin CatPartsTransform { head 1057 }...]` (Array) |
| `status` | Enum || 1 | `Brace` (Enum) |


### Object: `Thorns`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `TinkererBasicAttackSwitching`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `craft_ability` | Enum || 3 | `TinkererCraft` (Enum) |
| `throw_ability` | Enum || 3 | `TinkererThrow` (Enum) |


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
| `animation` | Enum || 2 | `hatch` (Enum) |
| `initiative` | Enum / Integer || 4 | `keep_turns_end_turn` (Enum) |
| `object` | Array / Enum || 8 | `[YellowBlaster GreyAlien GreenProber Amoeba MoonWorm Waggle KirbyFetus BrainDrain Fetus FetusGusher]` (Array), `[Squirrel Crow Snake Turtle Toad Catepillar]` (Array), `HuskG` (Enum), `SkeletonCatRevivedFamiliar` (Enum) |
| `stacks` | Enum / Integer || 8 | `3` (Number), `1` (Number) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object || 1 | `[1 4]` (Array) |


### Object: `TransformItemOnElementInfluence`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `element` | Array / Enum || 5 | `Fire` (Enum), `Greater_Water` (Enum) |
| `full_repair` | Boolean || 5 | `true` (Boolean) |
| `item` | Enum || 5 | `WaterBottle_Full` (Enum), `GallonOfWater` (Enum) |


### Object: `TransformOnDeathImmediately`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `first_turn` | Enum || 4 | `keep_turns` (Enum) |
| `obj` | Array / Enum || 4 | `TallSkeletonCatCorpse` (Enum), `SkeletonCatCorpseFamiliar` (Enum) |


### Object: `TransformOnElementInfluence`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `element` | Array / Enum || 9 | `Holy` (Enum), `Fire` (Enum) |
| `object` | Array / Enum || 9 | `CookedBiggestFood` (Enum), `CookedBait` (Enum) |


### Object: `TransformOnElementInfluencex`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `element` | Array / Enum || 2 | `Holy` (Enum) |
| `object` | Array / Enum || 2 | `Bait` (Enum), `PurifiedPoisonFood` (Enum) |


### Object: `TransformOnStatusThreshold`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `object` | Array / Enum || 1 | `Moth` (Enum) |
| `status` | Enum || 1 | `AllStatsUp` (Enum) |
| [`threshold`](Items_and_Equipment.md#object-threshold) | Enum / Integer / Object || 1 | `5` (Number) |


### Object: `Trapper`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum || 4 | `RattleSnakeTrap` (Enum), `BloatSideLaser` (Enum) |
| `cancel_movement` | Boolean || 2 | `false` (Boolean) |
| `pathfinding_avoidance` | Integer || 2 | `250` (Number) |
| `range` | Enum / Integer || 2 | `10` (Number) |


### Object: `Triskaidekaphobia`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |


### Object: `TunnelVision`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `crit_chance` | Number || 1 | `50` (Number) |


### Object: `TwisterFling`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage` | Equation || 1 | `5` (Equation) |
| `max_dist` | Integer || 1 | `5` (Number) |
| `min_dist` | Integer || 1 | `3` (Number) |


### Object: `UnlimitedDeathRattleRevive`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum || 1 | `MD_Lift` (Enum) |
| `even_if_stunned` | Boolean || 1 | `true` (Boolean) |


### Object: `UseAbility`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum || 2 | `Destroyer2HolyAttack` (Enum), `T3Pebbles_BoulderDrop` (Enum) |
| `respect_prime` | Boolean || 2 | `true` (Boolean) |


### Object: `UseAbilityWhenOutOfStatus`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum || 1 | `QueenHippoHeartAttack` (Enum) |
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

