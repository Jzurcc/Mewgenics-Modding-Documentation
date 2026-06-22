# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Enums.md#enum-mathequation).

## Passives & Statuses

### Context: `ROOT`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `name` | String | `"PASSIVE_MAINCOURSE_NAME", "PASSIVE_NEVERFULL_NAME", "PASSIVE_PUTREFY_NAME"` | Localization key for the passive's display name. |
| `class` | [`Enum/String`](./Enums.md#enum-class) | `Disorder, Butcher, Colorless` | Character class identifier. |
| `desc` | String | `"PASSIVE_MAINCOURSE_DESC", "PASSIVE_NEVERFULL_DESC", "PASSIVE_PUTREFY_DESCRIPTION"` | Localization key for the passive's display description. |
| `desc_multiclass` | String | `"PASSIVE_BARBED_MULTICLASS_DESC", "PASSIVE_HOOKED_MULTICLASS_DESC", "PASSIVE_GRAPPLINGHOOK_MULTICLASS_DESC"` |  |
| `auto_plus_signs_on_name` | Boolean | `false` |  |
| `name_mod` | String | `"CAT_NAME_MOD_GIGANTISM", "CAT_NAME_MOD_VEGAN", "CAT_NAME_MOD_DWARF"` |  |
| `tags` | [`Array`](./Arrays.md#array-tags) | `[ noncopyable ]` |  |
| `override_basic_attack` | [`Enum/String`](./Enums.md#enum-override_basic_attack) | `GerdShot, BasicMelee` |  |
| `shield` | Number | `8, 4` |  |
| `bonus_items` | [`Array`](./Arrays.md#array-bonus_items) | `[ Eyeball ]` | Flat addition to a base value. |
| `grant_ability` | [`Enum/String`](./Enums.md#enum-grant_ability) | `Rest` |  |

</details>

---

### Context: `passives`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddStatusToBasicAttack` | [`Block`](./Passives_and_Statuses.md#context-addstatustobasicattack) | `{ ... }` | Injects a status effect payload that applies whenever the character performs a basic attack. |
| `MulticlassLevelUp` | [`Enum/String`](./Enums.md#enum-multiclasslevelup) | `Mage, Fighter, Hunter` | Applies the 'MulticlassLevelUp' effect. |
| `CritChanceUp` | Number | `25, 10, 5` | Applies the 'CritChanceUp' effect. |
| `SpawnOnBattleStart` | [`Block`](./Passives_and_Statuses.md#context-spawnonbattlestart) | `{ ... }, BeefyCharmedLeech, CharmedTinySpider` | Applies the 'SpawnOnBattleStart' effect. |
| `AddCritMultiplier` | Number | `25%, 50%, 100%` | Applies the 'AddCritMultiplier' effect. |
| `MissChance` | Number | `10, 5, 15` | Applies the 'MissChance' effect. |
| `StatusOnKill` | [`Block`](./Passives_and_Statuses.md#context-statusonkill) | `{ ... }` | Event Trigger: Applies nested statuses when kill. |
| `ReplaceSpawnedObjects` | [`Array`](./Arrays.md#array-replacespawnedobjects) | `[ Crow Crow3 ], [ Crow2 Crow3 ], [ Crow Crow2 ]` | Applies the 'ReplaceSpawnedObjects' effect. |
| `AddBonusRange` | Number | `2, 1, 10` | Applies the 'AddBonusRange' effect. |
| `BonusAbility` | [`Enum/String`](./Enums.md#enum-bonusability) | `Groom, FeralMelee, Bloodzerk` | Applies the 'BonusAbility' effect. |
| `Brace` | Number | `2, 1, 3` | Applies the 'Brace' effect. |
| `DodgeChance` | Number | `10%, 25%, 15%` | Applies the 'DodgeChance' effect. |
| `HealthRegenUp` | Number | `2, 1, 3` | Applies the 'HealthRegenUp' effect. |
| `CritsApplyStatus` | [`Block`](./Passives_and_Statuses.md#context-critsapplystatus) | `{ ... }` | Applies the 'CritsApplyStatus' effect. |
| `PassiveLevelUpAtCombatEnd` | Number | `1` | Applies the 'PassiveLevelUpAtCombatEnd' effect. |
| `ExtraBasicAttacks` | Number | `2, 1` | Applies the 'ExtraBasicAttacks' effect. |
| `Trample` | Number | `9, 3` | Applies the 'Trample' effect. |
| `AmplifyStatus` | [`Block`](./Passives_and_Statuses.md#context-amplifystatus) | `{ ... }, Rot, Burn` | Applies the 'AmplifyStatus' effect. |
| `EquipTemporaryItem` | [`Enum/String`](./Enums.md#enum-equiptemporaryitem) | `FoodMedium, ButcherHook_Temporary, FoodBig` | Applies the 'EquipTemporaryItem' effect. |
| `ForceSpecificInjury` | [`Enum/String`](./Enums.md#enum-forcespecificinjury) | `int, cha, lck` | Applies the 'ForceSpecificInjury' effect. |
| `InnateElement` | [`Enum/String`](./Enums.md#enum-innateelement) | `Electric, Fire, Ice` | Applies the 'InnateElement' effect. |
| `ReplaceBasicAttack` | [`Enum/String`](./Enums.md#enum-replacebasicattack) | `BasicDruidAbilityVersatile, BasicButcherMeleeWideDoubleSpin, BasicButcherMeleeWideSpin` | Applies the 'ReplaceBasicAttack' effect. |
| `SizeScale` | [`Enum/String`](./Enums.md#enum-sizescale) | `.4, 1.3, .7` | Applies the 'SizeScale' effect. |
| `StatusImmunity` | [`Array`](./Arrays.md#array-statusimmunity) | `[ Sleep SleepParalysis ], Burn, [ Fear Madness PermanentMadness ]` | Event Trigger: Applies nested statuses to immunity. |
| `AbilityOnBattleStart` | [`Enum/String`](./Enums.md#enum-abilityonbattlestart) | `Heathens, MegaFart, neck_ChefsApron` | Applies the 'AbilityOnBattleStart' effect. |
| `AddCorpseHealth` | Number | `-999999, 96, 3` | Applies the 'AddCorpseHealth' effect. |
| `BlastResistance` | Number | `2, 3, 4` | Applies the 'BlastResistance' effect. |
| `ElementImmune` | [`Enum/String`](./Enums.md#enum-elementimmune) | `Electric, Fire, Ice` | Applies the 'ElementImmune' effect. |
| `Thorns` | Number | `2, 4` | Applies the 'Thorns' effect. |
| `AddElementsToBasicAttack` | [`Enum/String`](./Enums.md#enum-addelementstobasicattack) | `Electric, Fire, Ice` | Applies the 'AddElementsToBasicAttack' effect. |
| `AlphaTurns` | Number | `1, -1` | Applies the 'AlphaTurns' effect. |
| `BasicAttackDamageMultiplier` | Number | `33.333334%, 50%, 0` | Applies the 'BasicAttackDamageMultiplier' effect. |
| `BoostWeaponDamage` | Number | `2, 1, 5` | Applies the 'BoostWeaponDamage' effect. |
| `ExtraMovePoints` | Number | `1` | Applies the 'ExtraMovePoints' effect. |
| `ExtraWeaponAttacks` | Number | `2, 1` | Applies the 'ExtraWeaponAttacks' effect. |
| `ReplaceBasicAttackWhenCastable` | [`Enum/String`](./Enums.md#enum-replacebasicattackwhencastable) | `Shank, BasicSuplex, Shank2` | Applies the 'ReplaceBasicAttackWhenCastable' effect. |
| `SetSpellCosts` | Number | `0, 1, 3` | Applies the 'SetSpellCosts' effect. |
| `StatusOnStanceSwitch` | [`Block`](./Passives_and_Statuses.md#context-statusonstanceswitch) | `{ ... }` | Event Trigger: Applies nested statuses when stance switch. |
| `AddBonusMeleeRange` | Number | `2, 1, 10` | Applies the 'AddBonusMeleeRange' effect. |
| `AddManaRegen` | Number | `7, 1, 5` | Applies the 'AddManaRegen' effect. |
| `AllStatsUp` | Number | `-2, 2, -1` | Applies the 'AllStatsUp' effect. |
| `BasicAttackAOEBonus` | Number | `2, 1` | Applies the 'BasicAttackAOEBonus' effect. |
| `ReplaceBasicMove` | [`Enum/String`](./Enums.md#enum-replacebasicmove) | `BasicDashAttackMove, ToadJump_BasicMove, BellyFlop_BasicMove` | Applies the 'ReplaceBasicMove' effect. |
| `AbilityReaction` | [`Enum/String`](./Enums.md#enum-abilityreaction) | `Gassy_AssBlast2, PissYourself, Gassy_AssBlast` | Applies the 'AbilityReaction' effect. |
| `AddDamageToBasicAttack` | Number | `2, 1, 4` | Applies the 'AddDamageToBasicAttack' effect. |
| `AddLevelUpRerolls` | Number | `2, 1, 3` | Applies the 'AddLevelUpRerolls' effect. |
| `AddMovement` | Number | `2, 1, 4` | Applies the 'AddMovement' effect. |
| `AllyBonusAbilityAura` | [`Block`](./Passives_and_Statuses.md#context-allybonusabilityaura) | `{ ... }, NubbyToss` | Applies the 'AllyBonusAbilityAura' effect. |
| `BackstabCritChance` | Number | `1` | Applies the 'BackstabCritChance' effect. |
| `BoostHeals` | Number | `2, -2, 1` | Applies the 'BoostHeals' effect. |
| `FreezePiercing` | Number | `1` | Applies the 'FreezePiercing' effect. |
| `IncreaseExplosionDamage` | Number | `2, 3, 4` | Applies the 'IncreaseExplosionDamage' effect. |
| `KnockbackImmunity` | Number | `1` | Applies the 'KnockbackImmunity' effect. |
| `LevelUpClassOverride` | [`Enum/String`](./Enums.md#enum-levelupclassoverride) | `Jester, Colorless` | Applies the 'LevelUpClassOverride' effect. |
| `MakeSpellsRequireCharge` | Number | `1` | Applies the 'MakeSpellsRequireCharge' effect. |
| `MoveQuivered` | Number | `2` | Applies the 'MoveQuivered' effect. |
| `SpawnThingOnDeath` | [`Enum/String`](./Enums.md#enum-spawnthingondeath) | `ZombieCatFamiliar, CharmedDemonKitten` | Applies the 'SpawnThingOnDeath' effect. |
| `AddKnockbackDamage` | Number | `2, 1, 3` | Applies the 'AddKnockbackDamage' effect. |
| `AddTag` | [`Enum/String`](./Enums.md#enum-addtag) | `rock` | Applies the 'AddTag' effect. |
| `AllyDamageReduction` | Number | `0` | Applies the 'AllyDamageReduction' effect. |
| `AmplifyKnockback` | Number | `2, 10` | Applies the 'AmplifyKnockback' effect. |
| `AutocastEachTurnBegin` | [`Block`](./Passives_and_Statuses.md#context-autocasteachturnbegin) | `{ ... }, MindCrack_EldritchVisage2, MindCrack_EldritchVisage` | Applies the 'AutocastEachTurnBegin' effect. |
| `Bruise` | Number | `2, 1` | Applies the 'Bruise' effect. |
| `CobraReflex` | [`Enum/String`](./Enums.md#enum-cobrareflex) | `BasicMonkMelee` | Applies the 'CobraReflex' effect. |
| `ConsumablesInfiniteRange` | Number | `1` | Applies the 'ConsumablesInfiniteRange' effect. |
| `DamageUp` | Number | `4, 1, 3` | Combat Trigger: Deals damage to up. |
| `FreePathfindElement` | [`Enum/String`](./Enums.md#enum-freepathfindelement) | `Grass, Water` | Applies the 'FreePathfindElement' effect. |
| `IgnoreTiles` | Number | `1` | Applies the 'IgnoreTiles' effect. |
| `Quivered` | Number | `2, 1, 5` | Applies the 'Quivered' effect. |
| `TauntAlways` | Number | `1` | Applies the 'TauntAlways' effect. |
| `TileTrail` | [`Enum/String`](./Enums.md#enum-tiletrail) | `GrassTile, FlowerTile` | Applies the 'TileTrail' effect. |
| `TrinketActiveEffectsMultiplierBonus` | Number | `2, 1` | Applies the 'TrinketActiveEffectsMultiplierBonus' effect. |
| `TrinketPassiveMultiplierBonus` | Number | `2, 1` | Applies the 'TrinketPassiveMultiplierBonus' effect. |
| `UncappedMana` | Number | `1` | Applies the 'UncappedMana' effect. |
| `AbsorbManaAura` | Number | `1` | Applies the 'AbsorbManaAura' effect. |
| `AddHiddenTag` | [`Enum/String`](./Enums.md#enum-addhiddentag) | `bowling_ball` | Applies the 'AddHiddenTag' effect. |
| `AddInitiative` | Number | `-100, 999` | Applies the 'AddInitiative' effect. |
| `AddSpellDamage` | Number | `1` | Applies the 'AddSpellDamage' effect. |
| `AddStartingMana` | Number | `20, 5` | Applies the 'AddStartingMana' effect. |
| `AddStatusToExplosions` | [`Block`](./Passives_and_Statuses.md#context-addstatustoexplosions) | `{ ... }` | Applies the 'AddStatusToExplosions' effect. |
| `AddUnfilledMaxHealth` | Number | `50, 20` | Applies the 'AddUnfilledMaxHealth' effect. |
| `AddWeaponScaling` | Number | `1` | Applies the 'AddWeaponScaling' effect. |
| `AfterImage` | [`Enum/String`](./Enums.md#enum-afterimage) | `PlayerCat_ThiefShade2, PlayerCat_ThiefShade` | Spawns a visual decoy or shade at the caster's previous location. |
| `AllowPassTurn` | Number | `1, 0` | Applies the 'AllowPassTurn' effect. |
| `AllyDamageReaction` | [`Enum/String`](./Enums.md#enum-allydamagereaction) | `attack` | Applies the 'AllyDamageReaction' effect. |
| `AllyMoveAbilityAura` | [`Enum/String`](./Enums.md#enum-allymoveabilityaura) | `CatapultJump2, CatapultJump` | Applies the 'AllyMoveAbilityAura' effect. |
| `AllyMultiplyKnockbackDamage` | Number | `2` | Applies the 'AllyMultiplyKnockbackDamage' effect. |
| `AmplifyPositiveStatus` | Number | `2, 1` | Applies the 'AmplifyPositiveStatus' effect. |
| `AutoCritLowDamage` | Number | `2, 3` | Applies the 'AutoCritLowDamage' effect. |
| `AutoEquipConsumables` | Number | `1` | Applies the 'AutoEquipConsumables' effect. |
| `AutocastEachTurn` | [`Enum/String`](./Enums.md#enum-autocasteachturn) | `ViolentOutburst, DarkOneStrike` | Applies the 'AutocastEachTurn' effect. |
| `BasicAttackCritChance` | Number | `100%` | Applies the 'BasicAttackCritChance' effect. |
| `BasicAttackStatusCarefulness` | Number | `1` | Applies the 'BasicAttackStatusCarefulness' effect. |
| `Bleed` | Number | `1, 3` | Applies the 'Bleed' effect. |
| `BonusFoodEachBattle` | Number | `2, 20` | Applies the 'BonusFoodEachBattle' effect. |
| `BoostAllyStatsOnDeath` | Number | `2, 1` | Applies the 'BoostAllyStatsOnDeath' effect. |
| `BraceForEachNeighboringEnemy` | Number | `2, 1` | Applies the 'BraceForEachNeighboringEnemy' effect. |
| `CCImmunity` | Number | `1` | Applies the 'CCImmunity' effect. |
| `CapDamageFromAllies` | Number | `1` | Applies the 'CapDamageFromAllies' effect. |
| `ChainKnockback` | Number | `1` | Applies the 'ChainKnockback' effect. |
| `ChanceToBlockAndCounter` | Number | `33%, 15%` | Applies the 'ChanceToBlockAndCounter' effect. |
| `ChanceToRevive` | [`Block`](./Passives_and_Statuses.md#context-chancetorevive) | `{ ... }, 25` | Applies the 'ChanceToRevive' effect. |
| `ChangeTauntPriority` | Number | `-1` | Applies the 'ChangeTauntPriority' effect. |
| `CharmAllFlies` | Number | `1` | Applies the 'CharmAllFlies' effect. |
| `CoinsAddDamage` | Number | `2, 1` | Applies the 'CoinsAddDamage' effect. |
| `CollectPickupsOnBattleEnd` | [`Block`](./Passives_and_Statuses.md#context-collectpickupsonbattleend) | `{ ... }, 1` | Applies the 'CollectPickupsOnBattleEnd' effect. |
| `Conductor` | Number | `2` | Applies the 'Conductor' effect. |
| `ConjureCastSpellsForAllies` | Number | `2, 1` | Applies the 'ConjureCastSpellsForAllies' effect. |
| `ConsumableEffectsMultiplierBonus` | Number | `1` | Applies the 'ConsumableEffectsMultiplierBonus' effect. |
| `CounterAttack` | [`Enum/String`](./Enums.md#enum-counterattack) | `ReflexPunchJab2, ReflexPunchJab` | Applies the 'CounterAttack' effect. |
| `DamageEnemiesOnHeal` | Number | `2, 1` | Combat Trigger: Deals damage to enemies on heal. |
| `DamageEnemiesOnKill` | Number | `2, 1` | Combat Trigger: Deals damage to enemies on kill. |
| `DeathChill` | Number | `1` | Applies the 'DeathChill' effect. |
| `DebuffImmunity` | Number | `1` | Applies the 'DebuffImmunity' effect. |
| `DejaVu` | Number | `10%` | Applies the 'DejaVu' effect. |
| `DirtyClaws` | Number | `1` | Applies the 'DirtyClaws' effect. |
| `DoubleCastWeapons` | Number | `2, 1` | Applies the 'DoubleCastWeapons' effect. |
| `DukeOfFlies` | Number | `1` | Applies the 'DukeOfFlies' effect. |
| `Dyslexia` | [`Array`](./Arrays.md#array-dyslexia) | `[ 6 9 ], [ 3 5 ]` | Applies the 'Dyslexia' effect. |
| `EMP` | [`Block`](./Passives_and_Statuses.md#context-emp) | `{ ... }` | Applies the 'EMP' effect. |
| `Empath` | Number | `50%, 100%` | Applies the 'Empath' effect. |
| `EnemiesGetPickupsKnockedOut` | Number | `2, 1` | Applies the 'EnemiesGetPickupsKnockedOut' effect. |
| `EnergyStorm` | [`Block`](./Passives_and_Statuses.md#context-energystorm) | `{ ... }, 3` | Applies the 'EnergyStorm' effect. |
| `EquipmentPassiveMultiplierBonus` | Number | `1` | Applies the 'EquipmentPassiveMultiplierBonus' effect. |
| `EquipmentSetBonusBonus` | Number | `2, 1` | Applies the 'EquipmentSetBonusBonus' effect. |
| `ExplodeOverkilledEnemies` | Number | `2, 1` | Applies the 'ExplodeOverkilledEnemies' effect. |
| `FaceShield` | Number | `0` | Applies the 'FaceShield' effect. |
| `FamiliarSecondaryDamageImmunity` | Number | `1` | Applies the 'FamiliarSecondaryDamageImmunity' effect. |
| `FlowerPowerAuraBrace` | Number | `1` | Applies the 'FlowerPowerAuraBrace' effect. |
| `FlowerPowerAuraStrength` | Number | `1` | Applies the 'FlowerPowerAuraStrength' effect. |
| `FlowersOnEndTurn` | Number | `4, 3` | Applies the 'FlowersOnEndTurn' effect. |
| `FlyDamageIncrease` | Number | `1, 4` | Applies the 'FlyDamageIncrease' effect. |
| `Flying` | Number | `1` | Applies the 'Flying' effect. |
| `FollowUp` | [`Enum/String`](./Enums.md#enum-followup) | `FollowUpDash, FollowUpDash2` | Applies the 'FollowUp' effect. |
| `FullHealthCritChance` | Number | `100` | Applies the 'FullHealthCritChance' effect. |
| `FullPower` | Number | `3` | Applies the 'FullPower' effect. |
| `GainExtraShield` | Number | `2` | Applies the 'GainExtraShield' effect. |
| `HeadArmorPassiveMultiplierBonus` | Number | `2, 1` | Applies the 'HeadArmorPassiveMultiplierBonus' effect. |
| `HealDamagesEnemies` | Number | `1` | Applies the 'HealDamagesEnemies' effect. |
| `HealsAlsoRegenMana` | Number | `50%, 2` | Applies the 'HealsAlsoRegenMana' effect. |
| `HealsCanRevive` | Number | `1, 3` | Applies the 'HealsCanRevive' effect. |
| `HolyShieldTransferToTaggedMinions` | [`Enum/String`](./Enums.md#enum-holyshieldtransfertotaggedminions) | `any, crow` | Applies the 'HolyShieldTransferToTaggedMinions' effect. |
| `ImmortalLeeches` | Number | `1` | Applies the 'ImmortalLeeches' effect. |
| `IncreaseExplosionSize` | Number | `2` | Applies the 'IncreaseExplosionSize' effect. |
| `IncreaseHealingSpellRange` | Number | `2` | Applies the 'IncreaseHealingSpellRange' effect. |
| `IncreaseSpellRange` | Number | `10, 5` | Applies the 'IncreaseSpellRange' effect. |
| `KillsHeal` | Number | `50%, 5` | Applies the 'KillsHeal' effect. |
| `KillsToMeat` | [`Enum/String`](./Enums.md#enum-killstomeat) | `Food` | Applies the 'KillsToMeat' effect. |
| `LightningAspectCharge` | Number | `1, 0` | Applies the 'LightningAspectCharge' effect. |
| `LineOfSightTrueSightAura` | [`Enum/String`](./Enums.md#enum-lineofsighttruesightaura) | `.5, 0` | Applies the 'LineOfSightTrueSightAura' effect. |
| `LobbedHook` | Number | `2, 1` | Applies the 'LobbedHook' effect. |
| `MakeBasicAttackPassThroughThings` | Number | `1` | Applies the 'MakeBasicAttackPassThroughThings' effect. |
| `ManaRegenMultiplierIfManaEmpty` | Number | `2` | Applies the 'ManaRegenMultiplierIfManaEmpty' effect. |
| `MegaMinions` | [`Block`](./Passives_and_Statuses.md#context-megaminions) | `{ ... }, 3` | Applies the 'MegaMinions' effect. |
| `Metal` | Number | `1` | Applies the 'Metal' effect. |
| `MetalDetector` | Number | `10, 5` | Applies the 'MetalDetector' effect. |
| `MinimumTech` | Number | `1` | Applies the 'MinimumTech' effect. |
| `MoveAndUseAbilityEachTurnBeginIfPossible` | [`Enum/String`](./Enums.md#enum-moveanduseabilityeachturnbeginifpossible) | `Cannibalize, EatShit` | Applies the 'MoveAndUseAbilityEachTurnBeginIfPossible' effect. |
| `NoReflection` | Number | `1` | Applies the 'NoReflection' effect. |
| `NubbyTossPriority` | Number | `1` | Applies the 'NubbyTossPriority' effect. |
| `NumbingLeeches` | Number | `3` | Applies the 'NumbingLeeches' effect. |
| `OverhealGainsBothShield` | Number | `2, 1` | Applies the 'OverhealGainsBothShield' effect. |
| `OverrideBasicAttack` | [`Enum/String`](./Enums.md#enum-overridebasicattack) | `GerdShot, BasicMelee` | Applies the 'OverrideBasicAttack' effect. |
| `ParasitesArentCursed` | Number | `1` | Applies the 'ParasitesArentCursed' effect. |
| `PassiveWhenAffectedByElement` | [`Block`](./Passives_and_Statuses.md#context-passivewhenaffectedbyelement) | `{ ... }` | State Trigger: Grants nested passives when affected by element. |
| `PermanentItems` | Number | `2, 1` | Applies the 'PermanentItems' effect. |
| `PoisonThorns` | Number | `2, 1` | Applies the 'PoisonThorns' effect. |
| `ProtectTargetedAllies` | [`Enum/String`](./Enums.md#enum-protecttargetedallies) | `SwapPositions_WideLoad2, SwapPositions_WideLoad` | Applies the 'ProtectTargetedAllies' effect. |
| `Quiver` | Number | `2, 1` | Applies the 'Quiver' effect. |
| `RangedTrueShot` | Number | `1` | Applies the 'RangedTrueShot' effect. |
| `RemoveLineOfSightRestrictions` | Number | `1` | Applies the 'RemoveLineOfSightRestrictions' effect. |
| `RemoveOncePerFightRestriction` | Number | `1` | Applies the 'RemoveOncePerFightRestriction' effect. |
| `ReplaceBasicAttackWhenDead` | [`Enum/String`](./Enums.md#enum-replacebasicattackwhendead) | `Haunt` | Applies the 'ReplaceBasicAttackWhenDead' effect. |
| `ReviveOnWin` | Number | `100%` | Applies the 'ReviveOnWin' effect. |
| `RobotsInheritArmor` | Number | `2, 1` | Applies the 'RobotsInheritArmor' effect. |
| `RockDetector` | Number | `10` | Applies the 'RockDetector' effect. |
| `ShareHealthRegen` | Number | `1` | Applies the 'ShareHealthRegen' effect. |
| `SharePickups` | Number | `1` | Applies the 'SharePickups' effect. |
| `ShoulderCheck` | Number | `100%, 33%` | Applies the 'ShoulderCheck' effect. |
| `ShovingMatch` | [`Enum/String`](./Enums.md#enum-shovingmatch) | `attack` | Applies the 'ShovingMatch' effect. |
| `ShowHiddenThings` | Number | `1` | Applies the 'ShowHiddenThings' effect. |
| `SmallEnemiesIgnoreYou` | Number | `1` | Applies the 'SmallEnemiesIgnoreYou' effect. |
| `SpawnObjectOnPopCorpse` | [`Enum/String`](./Enums.md#enum-spawnobjectonpopcorpse) | `Food` | Applies the 'SpawnObjectOnPopCorpse' effect. |
| `SpeedUp` | Number | `6` | Applies the 'SpeedUp' effect. |
| `SplittableMove` | Number | `1, 3` | Applies the 'SplittableMove' effect. |
| `SpreadExtraDebuffs` | Number | `2, 1` | Applies the 'SpreadExtraDebuffs' effect. |
| `SpreadPainBonus` | Number | `2` | Applies the 'SpreadPainBonus' effect. |
| `StatMinimum` | Number | `7, 5` | Applies the 'StatMinimum' effect. |
| `StatusAlliesOnKill` | [`Block`](./Passives_and_Statuses.md#context-statusalliesonkill) | `{ ... }` | Event Trigger: Applies nested statuses to allies on kill. |
| `StatusReplacement` | [`Array`](./Arrays.md#array-statusreplacement) | `[ Petrify PetrifyCharmed ]` | Event Trigger: Applies nested statuses to replacement. |
| `Stealth` | Number | `1` | Applies the 'Stealth' effect. |
| `StrengthForEachNeighboringEnemy` | Number | `2, 3` | Applies the 'StrengthForEachNeighboringEnemy' effect. |
| `StrengthInNumbersAura` | [`Block`](./Passives_and_Statuses.md#context-strengthinnumbersaura) | `{ ... }, 1` | Applies the 'StrengthInNumbersAura' effect. |
| `StrengthUp` | Number | `2` | Applies the 'StrengthUp' effect. |
| `Study` | [`Block`](./Passives_and_Statuses.md#context-study) | `{ ... }, 1` | Applies the 'Study' effect. |
| `Tech` | Number | `1` | Applies the 'Tech' effect. |
| `TileDamageMultiplier` | [`Block`](./Passives_and_Statuses.md#context-tiledamagemultiplier) | `{ ... }, 2` | Applies the 'TileDamageMultiplier' effect. |
| `TowerDefenseReflex` | [`Enum/String`](./Enums.md#enum-towerdefensereflex) | `BasicRanged_1DMG, attack` | Applies the 'TowerDefenseReflex' effect. |
| `TrapEffectsMultiplier` | Number | `2` | Applies the 'TrapEffectsMultiplier' effect. |
| `UncappedHP` | Number | `1` | Applies the 'UncappedHP' effect. |
| `UpgradeLevelUpClassActives` | [`Enum/String`](./Enums.md#enum-upgradelevelupclassactives) | `Colorless` | Applies the 'UpgradeLevelUpClassActives' effect. |
| `UpgradeLevelUpClassPassives` | [`Enum/String`](./Enums.md#enum-upgradelevelupclasspassives) | `Colorless` | Applies the 'UpgradeLevelUpClassPassives' effect. |
| `UpgradeSpawnedPickups` | Number | `2, 1` | Applies the 'UpgradeSpawnedPickups' effect. |
| `Vengeful` | Number | `1` | Applies the 'Vengeful' effect. |
| `WaterWalk` | Number | `1` | Applies the 'WaterWalk' effect. |
| `Weakness` | Number | `1, 5` | Applies the 'Weakness' effect. |
| `WeaponCountsAsBasicAttack` | Number | `1` | Applies the 'WeaponCountsAsBasicAttack' effect. |
| `WeaponDamageMultiplierBonus` | Number | `2` | Applies the 'WeaponDamageMultiplierBonus' effect. |
| `AddAllyNeighborsToAbilityRange` | Number | `1` | Applies the 'AddAllyNeighborsToAbilityRange' effect. |
| `AddAllyNeighborsToAttackRange` | Number | `1` | Applies the 'AddAllyNeighborsToAttackRange' effect. |
| `AddChaScalingSpellDamage` | Number | `3` | Applies the 'AddChaScalingSpellDamage' effect. |
| `AddKnockbackToEverything` | Number | `1` | Applies the 'AddKnockbackToEverything' effect. |
| `AddLevelUpStatMultiplier` | Number | `1` | Applies the 'AddLevelUpStatMultiplier' effect. |
| `AddRangedCritChance` | Number | `25%` | Applies the 'AddRangedCritChance' effect. |
| `AllDamageCrits` | Number | `1` | Applies the 'AllDamageCrits' effect. |
| `AlliesAvoidTraps` | Number | `1` | Applies the 'AlliesAvoidTraps' effect. |
| `AllyChainKnockback` | Number | `1` | Applies the 'AllyChainKnockback' effect. |
| `AllyMultiplyKnockbackDistance` | Number | `2` | Applies the 'AllyMultiplyKnockbackDistance' effect. |
| `AllyUncappedHPAura` | Number | `1` | Applies the 'AllyUncappedHPAura' effect. |
| `AlphaCat` | Number | `1` | Applies the 'AlphaCat' effect. |
| `AmplifyNegativeStatus` | Number | `1` | Applies the 'AmplifyNegativeStatus' effect. |
| `ArmorDodgeChance` | Number | `10%` | Applies the 'ArmorDodgeChance' effect. |
| `BackstabImmunity` | Number | `1` | Applies the 'BackstabImmunity' effect. |
| `BackstabWeakness` | Number | `0.75` | Applies the 'BackstabWeakness' effect. |
| `BasicAttackStatusSwap` | [`Array`](./Arrays.md#array-basicattackstatusswap) | `[ TempDamageUp DamageUp ]` | Applies the 'BasicAttackStatusSwap' effect. |
| `BlacklistPickupType` | [`Enum/String`](./Enums.md#enum-blacklistpickuptype) | `food` | Applies the 'BlacklistPickupType' effect. |
| `BleedThorns` | Number | `2` | Applies the 'BleedThorns' effect. |
| `BonusHealthRegenBasedOnDex` | Number | `5` | Applies the 'BonusHealthRegenBasedOnDex' effect. |
| `BonusRangeBasedOnDex` | Number | `5` | Applies the 'BonusRangeBasedOnDex' effect. |
| `BoostDamageAura` | Number | `1` | Applies the 'BoostDamageAura' effect. |
| `BoostDamageGlobalAura` | Number | `1` | Applies the 'BoostDamageGlobalAura' effect. |
| `BoostRangeAura` | Number | `1` | Applies the 'BoostRangeAura' effect. |
| `BoostRangeGlobalAura` | Number | `1` | Applies the 'BoostRangeGlobalAura' effect. |
| `BuffImmunity` | Number | `1` | Applies the 'BuffImmunity' effect. |
| `Burn` | Number | `1` | Applies the 'Burn' effect. |
| `CanRemoveCursedItems` | Number | `1` | Applies the 'CanRemoveCursedItems' effect. |
| `CantDodge` | Number | `1` | Applies the 'CantDodge' effect. |
| `CapMovementAbilityRange` | Number | `1` | Applies the 'CapMovementAbilityRange' effect. |
| `CapTechSpent` | Number | `0` | Applies the 'CapTechSpent' effect. |
| `ConductorManaRegen` | Number | `2` | Applies the 'ConductorManaRegen' effect. |
| `ConfusionEffectOnTaggedAbilities` | [`Enum/String`](./Enums.md#enum-confusioneffectontaggedabilities) | `consumable` | Applies the 'ConfusionEffectOnTaggedAbilities' effect. |
| `ConsumablesMeleeRange` | Number | `1` | Applies the 'ConsumablesMeleeRange' effect. |
| `DepressionAura` | Number | `2` | Applies the 'DepressionAura' effect. |
| `DisableAbilities` | [`Enum/String`](./Enums.md#enum-disableabilities) | `all_items` | Applies the 'DisableAbilities' effect. |
| `DisableAbilitiesWithTag` | [`Enum/String`](./Enums.md#enum-disableabilitieswithtag) | `meat` | Applies the 'DisableAbilitiesWithTag' effect. |
| `Doomed` | Number | `3` | Applies the 'Doomed' effect. |
| `EachSpellFreeAtFullMana` | Number | `1` | Applies the 'EachSpellFreeAtFullMana' effect. |
| `EquipRandomTemporaryItemFromPool` | [`Enum/String`](./Enums.md#enum-equiprandomtemporaryitemfrompool) | `weapons` | Applies the 'EquipRandomTemporaryItemFromPool' effect. |
| `ExhaustionRoundChange` | Number | `3` | Applies the 'ExhaustionRoundChange' effect. |
| `ExplosionImmunity` | Number | `1` | Applies the 'ExplosionImmunity' effect. |
| `ExtraBasicMoves_Status` | Number | `1` | Applies the 'ExtraBasicMoves_Status' effect. |
| `ExtraInjuryOnDeath` | Number | `1` | Applies the 'ExtraInjuryOnDeath' effect. |
| `ExtraTrinketUses` | Number | `1` | Applies the 'ExtraTrinketUses' effect. |
| `FaceArmorPassiveMultiplierBonus` | Number | `2` | Applies the 'FaceArmorPassiveMultiplierBonus' effect. |
| `ForceUseAbility` | [`Enum/String`](./Enums.md#enum-forceuseability) | `MockingbirdForm` | Applies the 'ForceUseAbility' effect. |
| `FreeSpellsAtFullMana` | Number | `1` | Applies the 'FreeSpellsAtFullMana' effect. |
| `FrontstabBasicAttackCritChance` | Number | `100%` | Applies the 'FrontstabBasicAttackCritChance' effect. |
| `FrontstabCritChance` | Number | `100%` | Applies the 'FrontstabCritChance' effect. |
| `FullHeal` | Number | `1` | Applies the 'FullHeal' effect. |
| `FullHealthAllStatsUp` | Number | `1` | Applies the 'FullHealthAllStatsUp' effect. |
| `FullHealthManaRegen` | Number | `5` | Applies the 'FullHealthManaRegen' effect. |
| `GrassTileHealing` | Number | `1` | Applies the 'GrassTileHealing' effect. |
| `HPGainBlock` | Number | `1` | Applies the 'HPGainBlock' effect. |
| `HealAtStart` | Number | `100%` | Applies the 'HealAtStart' effect. |
| `HealingAura` | Number | `1` | Applies the 'HealingAura' effect. |
| `HolyDamageMultiplierBonus` | Number | `1` | Applies the 'HolyDamageMultiplierBonus' effect. |
| `HouseFoodRequirementMultiplier` | Number | `0` | Applies the 'HouseFoodRequirementMultiplier' effect. |
| `Hypomania` | Number | `3` | Applies the 'Hypomania' effect. |
| `IncreaseItemUsesOnEquip` | Number | `1` | Applies the 'IncreaseItemUsesOnEquip' effect. |
| `InjuryImmunity` | Number | `1` | Applies the 'InjuryImmunity' effect. |
| `InvertBrainFaction` | Number | `1` | Applies the 'InvertBrainFaction' effect. |
| `LimitDamage` | Number | `1` | Applies the 'LimitDamage' effect. |
| `LimitHeal` | Number | `1` | Applies the 'LimitHeal' effect. |
| `LimitSelfKnockbackDamage` | Number | `1` | Applies the 'LimitSelfKnockbackDamage' effect. |
| `LimitedTileTrail` | [`Enum/String`](./Enums.md#enum-limitedtiletrail) | `FlowerTile` | Applies the 'LimitedTileTrail' effect. |
| `Madness` | Number | `1` | Applies the Madness debuff/status effect. |
| `ManaCostReduction` | Number | `25%` | Applies the 'ManaCostReduction' effect. |
| `MaxAccuracy` | Number | `1` | Applies the 'MaxAccuracy' effect. |
| `MaxStartingMana` | Number | `1` | Applies the 'MaxStartingMana' effect. |
| `MoveAwayFromDamageSource` | [`Enum/String`](./Enums.md#enum-moveawayfromdamagesource) | `MoveOne` | Applies the 'MoveAwayFromDamageSource' effect. |
| `MoveRandomly` | Number | `1` | Applies the 'MoveRandomly' effect. |
| `MoveSpeedMultiplier` | [`Enum/String`](./Enums.md#enum-movespeedmultiplier) | `.5` | Applies the 'MoveSpeedMultiplier' effect. |
| `NeckArmorPassiveMultiplierBonus` | Number | `2` | Applies the 'NeckArmorPassiveMultiplierBonus' effect. |
| `NoManaRegen` | Number | `1` | Applies the 'NoManaRegen' effect. |
| `OverrideMaxHealth` | Number | `1` | Applies the 'OverrideMaxHealth' effect. |
| `OverrideMaxMana` | Number | `1` | Applies the 'OverrideMaxMana' effect. |
| `OverridePalette` | Number | `87` | Applies the 'OverridePalette' effect. |
| `Paranoia` | [`Enum/String`](./Enums.md#enum-paranoia) | `ParanoiaBasicMelee` | Applies the 'Paranoia' effect. |
| `PermanentImmobile` | Number | `1` | Applies the 'PermanentImmobile' effect. |
| `PermanentKitten` | Number | `1` | Applies the 'PermanentKitten' effect. |
| `PermanentMadness` | Number | `1` | Applies the 'PermanentMadness' effect. |
| `Phasing` | Number | `1` | Applies the 'Phasing' effect. |
| `Poison` | Number | `1` | Applies the 'Poison' effect. |
| `PoisonMultiplier` | Number | `2` | Applies the 'PoisonMultiplier' effect. |
| `PoopWhenHit` | [`Enum/String`](./Enums.md#enum-poopwhenhit) | `Poop` | Applies the 'PoopWhenHit' effect. |
| `RealTimePressure_OneUnit` | Number | `5` | Applies the 'RealTimePressure_OneUnit' effect. |
| `ReceivedStatusReplacement` | [`Array`](./Arrays.md#array-receivedstatusreplacement) | `[ Sleep SleepParalysis ]` | Applies the 'ReceivedStatusReplacement' effect. |
| `RefreshMoveOnWeaponConnect` | Number | `1` | Applies the 'RefreshMoveOnWeaponConnect' effect. |
| `ReplaceSpellsWhenDead` | [`Enum/String`](./Enums.md#enum-replacespellswhendead) | `Spook` | Applies the 'ReplaceSpellsWhenDead' effect. |
| `SafeExplosions` | Number | `1` | Applies the 'SafeExplosions' effect. |
| `SchrodingerDisorder` | Number | `50%` | Applies the 'SchrodingerDisorder' effect. |
| `Scleroderma` | Number | `1` | Applies the 'Scleroderma' effect. |
| `SetDefaultFacePassive` | [`Enum/String`](./Enums.md#enum-setdefaultfacepassive) | `insane` | Applies the 'SetDefaultFacePassive' effect. |
| `Slow` | Number | `5` | Applies the 'Slow' effect. |
| `SmallRockBehavior` | Number | `5` | Applies the 'SmallRockBehavior' effect. |
| `SpawnCreepOnHit` | Number | `1` | Applies the 'SpawnCreepOnHit' effect. |
| `SpawnMeatOnMove` | [`Enum/String`](./Enums.md#enum-spawnmeatonmove) | `Food` | Applies the 'SpawnMeatOnMove' effect. |
| `SpreadPainBonusCrit` | Number | `1` | Applies the 'SpreadPainBonusCrit' effect. |
| `StatusCarefulness` | Number | `1` | Event Trigger: Applies nested statuses to carefulness. |
| `StrictLimitDamage` | Number | `1` | Applies the 'StrictLimitDamage' effect. |
| `TauntAtFullHealth` | Number | `1` | Applies the 'TauntAtFullHealth' effect. |
| `TempInitiativeChange` | Number | `-999` | Applies the 'TempInitiativeChange' effect. |
| `Triskaidekaphobia` | Number | `13` | Applies the 'Triskaidekaphobia' effect. |
| `UncappedHPBonusStr` | Number | `5` | Applies the 'UncappedHPBonusStr' effect. |
| `Vegan` | Number | `1` | Applies the 'Vegan' effect. |
| `WeaponActiveEffectsMultiplierBonus` | Number | `2` | Applies the 'WeaponActiveEffectsMultiplierBonus' effect. |
| `WeaponPassiveMultiplierBonus` | Number | `2` | Applies the 'WeaponPassiveMultiplierBonus' effect. |
| `WeaponsDontLoseDurability` | Number | `0` | Applies the 'WeaponsDontLoseDurability' effect. |
| `WobblyCat` | Number | `25%` | Applies the 'WobblyCat' effect. |

</details>

---

### Context: `2`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"PASSIVE_MAINCOURSE2_DESC", "PASSIVE_PUTREFY2_DESCRIPTION", "PASSIVE_NEVERFULL2_DESC"` | Localization key for the passive's display description. |
| `desc_multiclass` | String | `"PASSIVE_HOOKED2_MULTICLASS_DESC", "PASSIVE_GRAPPLINGHOOK2_MULTICLASS_DESC", "PASSIVE_BARBED2_MULTICLASS_DESC"` |  |
| `override_basic_attack` | [`Enum/String`](./Enums.md#enum-override_basic_attack) | `BasicButcherMeleeWideDoubleSpin, BasicDruidAbilityVersatile, BasicMagicMissile` |  |
| `shield` | Number | `8, 4` |  |
| `bonus_items` | [`Array`](./Arrays.md#array-bonus_items) | `[ SpiderWebber ], [ Stick Stick Stick ], [ FoodBig FoodBig FoodBig FoodBig ]` | Flat addition to a base value. |
| `divine_shield` | Number | `1, 3` |  |
| `icon` | [`Enum/String`](./Enums.md#enum-icon) | `DejaVu2` |  |

</details>

---

### Context: `stats`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `con` | Number | `2, -2, -1` |  |
| `spd` | Number | `2, 1, 3` |  |
| `cha` | Number | `2, 3, 4` |  |
| `int` | Number | `2, -2, -1` |  |
| `str` | Number | `2, 4, -1` |  |
| `dex` | Number | `6, 3, -1` |  |
| `lck` | Number | `2, 1, 4` |  |

</details>

---

### Context: `AddStatusToBasicAttack`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Poison` | Number | `1, [ 1 .5 ], 3` | Applies the 'Poison' effect. |
| `Bleed` | Number | `2, 1` | Applies the 'Bleed' effect. |
| `Knockback` | Number | `1, 3, 4` | Applies the 'Knockback' effect. |
| `Bruise` | Number | `2, 1` | Applies the 'Bruise' effect. |
| `Conditional_Ally` | [`Block`](./Passives_and_Statuses.md#context-conditional_ally) | `{ ... }` | Conditional trigger: Executes nested logic if the target is friendly to the caster. |
| `BounceObject` | [`Enum/String`](./Enums.md#enum-bounceobject) | `CharmedLeech, BeefyCharmedLeech, AllyRotFly` | Spawns a physics object that visually bounces off the target. |
| `Weakness` | Number | `1` | Applies the 'Weakness' effect. |
| `Burn` | Number | `2, 1, 5` | Applies the 'Burn' effect. |
| `Leech` | Number | `1` | Applies the 'Leech' effect. |
| `Piercing` | Number | `1` | Applies the 'Piercing' effect. |
| `Slow` | Number | `2, 1, 5` | Applies the 'Slow' effect. |
| `BurgleCoin` | Number | `1` | Applies the 'BurgleCoin' effect. |
| `ChangeTile` | [`Block`](./Passives_and_Statuses.md#context-changetile) | `{ ... }, BrambleTile` | Transforms the terrain tile under the target. |
| `Charmed` | [`Array`](./Arrays.md#array-charmed) | `[ 1 .25 ]` | Applies the 'Charmed' effect. |
| `Fear` | [`Array`](./Arrays.md#array-fear) | `[ 1 .25 ]` | Applies the 'Fear' effect. |
| `Freeze` | [`Array`](./Arrays.md#array-freeze) | `[ 1 .20 ], [ 1 .5 ]` | Applies the 'Freeze' effect. |
| `KnockOutCoin` | Number | `1, [ 1 .5 ]` | Forces the target to drop coins. |
| `LuckUp` | Number | `-1` | Applies the 'LuckUp' effect. |
| `Madness` | Number | `1` | Applies the Madness debuff/status effect. |
| `MagicWeakness` | Number | `2, 1` | Applies the 'MagicWeakness' effect. |
| `Rot` | Number | `-999999, 1` | Applies the 'Rot' effect. |
| `SoulLink` | Number | `1` | Applies the 'SoulLink' effect. |
| `SpawnBearTrapOnMiss` | Number | `1` | Applies the 'SpawnBearTrapOnMiss' effect. |
| `Stun` | [`Array`](./Arrays.md#array-stun) | `[ 1 .15 ], [ 1 .40 ]` | Applies the 'Stun' effect. |
| `ApplyToSource` | [`Block`](./Passives_and_Statuses.md#context-applytosource) | `{ ... }` | Redirects the nested effects to apply to the caster/source of the ability instead of the target. |
| `BigSplashDamage` | Number | `2` | Applies the 'BigSplashDamage' effect. |
| `Blind` | Number | `1` | Applies the 'Blind' effect. |
| `Confusion` | Number | `1` | Applies the 'Confusion' effect. |
| `DamageOrHealConditionally` | Number | `1` | Combat Trigger: Deals damage to or heal conditionally. |
| `Else` | [`Block`](./Passives_and_Statuses.md#context-else) | `{ ... }` | Fallback block that executes if the preceding `Conditional_` block evaluated to false. |
| `Leeches` | Number | `1` | Applies the 'Leeches' effect. |
| `ManaLeeches` | Number | `1` | Applies the 'ManaLeeches' effect. |
| `OverrideChainKnockback` | Number | `0` | Applies the 'OverrideChainKnockback' effect. |
| `OverrideChainKnockbackDamage` | Number | `0` | Applies the 'OverrideChainKnockbackDamage' effect. |
| `SplashDamage` | Number | `2` | Applies the 'SplashDamage' effect. |

</details>

---

### Context: `RandomStatusFromPool`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1, -1` | Applies the 'AllStatsUp' effect. |
| `Bleed` | Number | `1` | Applies the 'Bleed' effect. |
| `BleedThorns` | Number | `1` | Applies the 'BleedThorns' effect. |
| `Blind` | Number | `1` | Applies the 'Blind' effect. |
| `Brace` | Number | `1` | Applies the 'Brace' effect. |
| `Bruise` | Number | `1` | Applies the 'Bruise' effect. |
| `Burn` | Number | `1` | Applies the 'Burn' effect. |
| `Charge` | Number | `1` | Applies the 'Charge' effect. |
| `Charmed` | Number | `1` | Applies the 'Charmed' effect. |
| `Confusion` | Number | `1` | Applies the 'Confusion' effect. |
| `DiminishingHealthRegen` | Number | `1` | Applies the 'DiminishingHealthRegen' effect. |
| `DivineShield` | Number | `1` | Applies the 'DivineShield' effect. |
| `Fear` | Number | `1` | Applies the 'Fear' effect. |
| `Freeze` | Number | `1` | Applies the 'Freeze' effect. |
| `Immobile` | Number | `1` | Applies the 'Immobile' effect. |
| `KineticSpikes` | Number | `1` | Applies the 'KineticSpikes' effect. |
| `Madness` | Number | `1` | Applies the Madness debuff/status effect. |
| `MagicWeakness` | Number | `1` | Applies the 'MagicWeakness' effect. |
| `Marked` | Number | `1` | Applies the 'Marked' effect. |
| `MoveQuivered` | Number | `1` | Applies the 'MoveQuivered' effect. |
| `ObjectOnHitCharacter` | [`Enum/String`](./Enums.md#enum-objectonhitcharacter) | `CharmedLeech, BeefyCharmedLeech` | Spawns a specific character or entity upon impact. |
| `Petrify` | Number | `1` | Applies the 'Petrify' effect. |
| `Poison` | Number | `1` | Applies the 'Poison' effect. |
| `Quivered` | Number | `1` | Applies the 'Quivered' effect. |
| `Reflect` | Number | `1` | Applies the 'Reflect' effect. |
| `Shield` | Number | `1` | Applies the 'Shield' effect. |
| `Sleep` | Number | `1` | Applies the 'Sleep' effect. |
| `Slow` | Number | `1` | Applies the 'Slow' effect. |
| `Stun` | Number | `1` | Applies the 'Stun' effect. |
| `Tarred` | Number | `1` | Applies the 'Tarred' effect. |
| `Thorns` | Number | `1` | Applies the 'Thorns' effect. |
| `Weakness` | Number | `1` | Applies the 'Weakness' effect. |
| `ConstitutionUp` | Number | `1` | Applies the 'ConstitutionUp' effect. |
| `SpawnCoinAnywhere` | Number | `1` | Applies the 'SpawnCoinAnywhere' effect. |
| `SpeedUp` | Number | `1` | Applies the 'SpeedUp' effect. |
| `StrengthUp` | Number | `1` | Applies the 'StrengthUp' effect. |

</details>

---

### Context: `Temporary`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | `2, 1, 5` | The number of stacks, duration, or intensity to apply. |
| `status` | [`Enum/String`](./Enums.md#enum-status) | `Brace, Thorns, Uncontrollable` | The status effect to apply. |
| `turns` | Number | `1` | Duration in turns. |
| `expires_on_end_turn` | Boolean | `true` |  |
| `expires_on_begin_turn` | Boolean | `true` | If true, ticks down at the start of the turn rather than the end. |

</details>

---

### Context: `AddPassivesToMinions`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DamageUp` | Number | `2, 3` | Combat Trigger: Deals damage to up. |
| `IncreaseExplosionDamage` | Number | `2, 3, 4` | Applies the 'IncreaseExplosionDamage' effect. |
| `FreePathfindElement` | [`Enum/String`](./Enums.md#enum-freepathfindelement) | `Grass, Water` | Applies the 'FreePathfindElement' effect. |
| `AddMaxHealth` | Number | `10, 5` | Applies the 'AddMaxHealth' effect. |
| `AddSpeed` | Number | `4` | Applies the 'AddSpeed' effect. |
| `FamiliarBonusAbility` | [`Enum/String`](./Enums.md#enum-familiarbonusability) | `FamiliarSelfDestruct, FamiliarSelfDestruct2` | Applies the 'FamiliarBonusAbility' effect. |
| `ForceAttack` | Number | `1` | Forces the character to execute an immediate attack. |
| `HealthGain` | Number | `10, 5` | Applies the 'HealthGain' effect. |
| `HealthRegenUp` | Number | `3` | Applies the 'HealthRegenUp' effect. |
| `HolyShieldTransferToSpawner` | Number | `1` | Applies the 'HolyShieldTransferToSpawner' effect. |
| `IncreaseExplosionSize` | Number | `2` | Applies the 'IncreaseExplosionSize' effect. |
| `PoisonThorns` | Number | `2, 1` | Applies the 'PoisonThorns' effect. |
| `WaterWalk` | Number | `1` | Applies the 'WaterWalk' effect. |
| `tag_filter` | [`Enum/String`](./Enums.md#enum-tag_filter) | `crow` |  |
| `AddUnfilledMaxHealth` | Number | `10` | Applies the 'AddUnfilledMaxHealth' effect. |
| `DivineShield` | Number | `1` | Applies the 'DivineShield' effect. |
| `GrassTileHealing` | Number | `1` | Applies the 'GrassTileHealing' effect. |
| `Quivered` | Number | `1` | Applies the 'Quivered' effect. |
| `SafeExplosions` | Number | `1` | Applies the 'SafeExplosions' effect. |
| `TakeExtraTurn` | Number | `1` | Applies the 'TakeExtraTurn' effect. |
| `UncappedHP` | Number | `1` | Applies the 'UncappedHP' effect. |

</details>

---

### Context: `effects`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `VisualFXTile` | [`Enum/String`](./Enums.md#enum-visualfxtile) | `WaterConduct, IcePoof, BurnTrigger` | Applies the 'VisualFXTile' effect. |
| `Stun` | [`Array`](./Arrays.md#array-stun) | `[ 1, .05*X ], 1, [ 1, .05 ]` | Applies the 'Stun' effect. |
| `Freeze` | [`Array`](./Arrays.md#array-freeze) | `[ 1, .05 ], [ 1, .15 ]` | Applies the 'Freeze' effect. |
| `Burn` | Number | `1` | Applies the 'Burn' effect. |
| `Charmed` | [`Array`](./Arrays.md#array-charmed) | `[ 1, .40 ], [ 1, .25 ]` | Applies the 'Charmed' effect. |
| `Petrify` | [`Array`](./Arrays.md#array-petrify) | `[ 1, .1 ], [ 1, .2 ]` | Applies the 'Petrify' effect. |
| `Poison` | Number | `1` | Applies the 'Poison' effect. |
| `Slow` | Number | `2` | Applies the 'Slow' effect. |
| `Bleed` | Number | `1` | Applies the 'Bleed' effect. |
| `Bruise` | Number | `1` | Applies the 'Bruise' effect. |
| `Fear` | Number | `1` | Applies the 'Fear' effect. |
| `Immobile` | Number | `1` | Applies the 'Immobile' effect. |
| `Leeches` | Number | `1` | Applies the 'Leeches' effect. |
| `Madness` | Number | `1` | Applies the Madness debuff/status effect. |
| `Marked` | Number | `1` | Applies the 'Marked' effect. |
| `Weakness` | Number | `1` | Applies the 'Weakness' effect. |

</details>

---

### Context: `SpreadDisease`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`MeleeRevengeDamage`](./Passives_and_Statuses.md#context-meleerevengedamage)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `disease` | [`Enum/String`](./Enums.md#enum-disease) | `CommonCold, Pox, Rabies` | The specific status effect ID representing the disease. |
| `chance` | Number | `25%, 50%, 100%` | Probability (0.0 to 1.0 or percentage) of transmitting. |
| `can_apply_to_anything` | Boolean | `true` |  |

</details>

---

### Context: `SpawnOnBattleStart`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `SmallRock, [ BuffFamiliarMaggot BuffFamiliarPooter BuffFamiliarFlea ..., CharmedFlea` |  |
| `number` | Number | `1, [ 2 3 ], 3` |  |

</details>

---

### Context: `StatusEachTurnEnd`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ForceUseAbility` | [`Block`](./Passives_and_Statuses.md#context-forceuseability) | `{ ... }, MiniFart, Rest` | Applies the 'ForceUseAbility' effect. |
| `NonStackingDivineShield` | Number | `1` | Applies the 'NonStackingDivineShield' effect. |
| `SpeedUp` | Number | `-2, 1` | Applies the 'SpeedUp' effect. |
| `EmptyMana` | Number | `1` | Applies the 'EmptyMana' effect. |
| `RangeUp` | Number | `1` | Applies the 'RangeUp' effect. |
| `IntelligenceUp` | Number | `1` | Applies the 'IntelligenceUp' effect. |
| `KineticSpikes` | Number | `1` | Applies the 'KineticSpikes' effect. |
| `PermanentMadness` | Number | `1` | Applies the 'PermanentMadness' effect. |
| `StrengthUp` | Number | `1` | Applies the 'StrengthUp' effect. |
| `UseAbility_Madness` | [`Enum/String`](./Enums.md#enum-useability_madness) | `weapon` | Applies the 'UseAbility_Madness' effect. |

</details>

---

### Context: `StatusOnBattleEnd`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `even_if_dead` | Boolean | `true` | If true, triggers the effect even if the character died during the battle. |
| `FindItemFromPool` | [`Block`](./Passives_and_Statuses.md#context-finditemfrompool) | `{ ... }, chapter, consumables` | Generates an item drop from the specified loot pool. |
| `RandomPermanentStat` | Number | `1, 3, -3` | Applies the 'RandomPermanentStat' effect. |
| `PermanentSpeed` | Number | `-1` | Applies the 'PermanentSpeed' effect. |
| `RandomMutation` | Number | `1` | Applies the 'RandomMutation' effect. |
| `PermanentConstitution` | Number | `-1` | Applies the 'PermanentConstitution' effect. |
| `PermanentIntelligence` | Number | `-1` | Applies the 'PermanentIntelligence' effect. |
| `PermanentStrength` | Number | `2` | Applies the 'PermanentStrength' effect. |

</details>

---

### Context: `DamageNeighborsOnEndMove`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `0` | The base damage properties of an attack. |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `status` | The classification type (e.g., damage type or element). |
| `cant_miss` | Boolean | `true` |  |
| `knockback` | Number | `1` |  |

</details>

---

### Context: `StatusOnTookDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `SpeedUp` | Number | `2, 1` | Applies the 'SpeedUp' effect. |
| `ConstitutionUp` | Number | `1, -1` | Applies the 'ConstitutionUp' effect. |
| `DamageUp` | Number | `2, 1` | Combat Trigger: Deals damage to up. |
| `IntelligenceUp` | Number | `-2, -1` | Applies the 'IntelligenceUp' effect. |
| `Shield` | Number | `2, 1` | Applies the 'Shield' effect. |
| `StrengthUp` | Number | `1, -1` | Applies the 'StrengthUp' effect. |
| `TempDamageUp` | Number | `2, 1` | Applies the 'TempDamageUp' effect. |
| `DiminishingHealthRegen` | Number | `1` | Applies the 'DiminishingHealthRegen' effect. |
| `MovementUp` | Number | `1` | Applies the 'MovementUp' effect. |
| `RandomInjury` | Number | `1` | Applies the 'RandomInjury' effect. |
| `RandomStatUp` | Number | `1` | Applies the 'RandomStatUp' effect. |
| `TempMovement` | Number | `1` | Applies the 'TempMovement' effect. |
| `Thorns` | Number | `1` | Applies the 'Thorns' effect. |

</details>

---

### Context: `lock_item_slot`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `slot` | [`Enum/String`](./Enums.md#enum-slot) | `neck, face, trinket` |  |
| `frame` | Number | `11, 16, 17` |  |

</details>

---

### Context: `StatusOnKill`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DamageUp` | Number | `1` | Combat Trigger: Deals damage to up. |
| `EquipPermanentItem` | [`Enum/String`](./Enums.md#enum-equippermanentitem) | `BoneClub` | Applies the 'EquipPermanentItem' effect. |
| `RefreshActPoints` | Number | `1` | Applies the 'RefreshActPoints' effect. |
| `RefreshMovePoints` | Number | `1` | Applies the 'RefreshMovePoints' effect. |
| `StrengthUp` | Number | `2` | Applies the 'StrengthUp' effect. |
| `AllStatsUp` | Number | `1` | Applies the 'AllStatsUp' effect. |
| `HealthGain` | Number | `5` | Applies the 'HealthGain' effect. |
| `LuckUp` | Number | `2` | Applies the 'LuckUp' effect. |
| `RandomStatUp` | Number | `1` | Applies the 'RandomStatUp' effect. |
| `SpeedUp` | Number | `2` | Applies the 'SpeedUp' effect. |
| `Stealth` | Number | `1` | Applies the 'Stealth' effect. |

</details>

---

### Context: `StatusOnUseAbilityWithTag`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `shapeshift, musical` | The specific entity tag required or applied. |
| `RefreshActPoints` | Number | `1` | Applies the 'RefreshActPoints' effect. |
| `DamageUp` | Number | `1` | Combat Trigger: Deals damage to up. |
| `exclude_basicattack` | Boolean | `true` |  |
| `HealthGain` | Number | `1` | Applies the 'HealthGain' effect. |
| `RandomStatUp` | Number | `1` | Applies the 'RandomStatUp' effect. |

</details>

---

### Context: `spell_graphics_override`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `area_particle` | [`Enum/String`](./Enums.md#enum-area_particle) | `WaterConduct` |  |
| `center_particle` | [`Enum/String`](./Enums.md#enum-center_particle) | `WaterConduct` |  |
| `palette` | Number | `-1` |  |
| `particle` | [`Enum/String`](./Enums.md#enum-particle) | `WaterConduct` |  |

</details>

---

### Context: `1`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `bonus_items` | [`Array`](./Arrays.md#array-bonus_items) | `[ Pipe ], [ Stick Stick Stick ], [ SpiderEgg ]` | Flat addition to a base value. |
| `override_basic_attack` | [`Enum/String`](./Enums.md#enum-override_basic_attack) | `BasicDruidAbilityVersatile, BasicButcherMeleeWideSpin, BasicMagicMissile` |  |
| `divine_shield` | Number | `1` |  |
| `shield` | Number | `2, 4` |  |
| `desc` | String | `"DISORDER_DEJAVU_DESC"` | Localization key for the passive's display description. |

</details>

---

### Context: `CritsApplyStatus`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ObjectOnHitCharacter` | [`Enum/String`](./Enums.md#enum-objectonhitcharacter) | `RandomPickup, Coin` | Spawns a specific character or entity upon impact. |
| `Stun` | [`Array`](./Arrays.md#array-stun) | `[ 1 .25 ], [ 1 .33 ], 1` | Applies the 'Stun' effect. |
| `Weakness` | Number | `2, 1` | Applies the 'Weakness' effect. |
| `Bleed` | Number | `1` | Applies the 'Bleed' effect. |
| `Bruise` | Number | `1` | Applies the 'Bruise' effect. |
| `Confusion` | Number | `1` | Applies the 'Confusion' effect. |
| `Immobile` | Number | `1` | Applies the 'Immobile' effect. |

</details>

---

### Context: `StatusOnStanceSwitch`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RandomMagicMissile` | Number | `1` | Fires a randomized number of magic missiles. |
| `ForceUseAbility` | [`Enum/String`](./Enums.md#enum-forceuseability) | `RapidFlowSpin, RapidFlowSpin2` | Applies the 'ForceUseAbility' effect. |
| `NextBasicAttackCritsThisTurn` | Number | `1` | Guarantees the next basic attack executed this turn will be a critical hit. |
| `RandomStatUp` | Number | `1` | Applies the 'RandomStatUp' effect. |
| `Shield` | Number | `2, 3` | Applies the 'Shield' effect. |
| `PartialCleanse` | Number | `1` | Applies the 'PartialCleanse' effect. |

</details>

---

### Context: `SpawnEachTurn`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Array`](./Arrays.md#array-object) | `[ CharmedTumorousMaggot CharmedChargeyMaggot CharmedSwapp..., CharmedFlea, CharmedMaggot` |  |
| `chance` | Number | `50%, .5, 15%` | The probability (0.0 to 1.0 or percentage) of this effect triggering. |
| `number` | Number | `1` |  |
| `good` | Boolean | `false` |  |

</details>

---

### Context: `Conditional_Ally`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1, [ 1 .5 ]` | Applies the 'AllStatsUp' effect. |
| `Cleanse` | Number | `0` | Applies the 'Cleanse' effect. |
| `ClearNegativeEffects` | Number | `1` | Applies the 'ClearNegativeEffects' effect. |
| `DamageUp` | Number | `1` | Combat Trigger: Deals damage to up. |
| `Shield` | Number | `2, 3` | Applies the 'Shield' effect. |
| `TempSpeedUp` | Number | `4` | Applies the 'TempSpeedUp' effect. |
| `SpeedUp` | Number | `1` | Applies the 'SpeedUp' effect. |

</details>

---

### Context: `CureDisease`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Number | `5%, 30%, 15%` | The probability (0.0 to 1.0 or percentage) of this effect triggering. |
| `disease` | [`Enum/String`](./Enums.md#enum-disease) | `Ebola, Pox, CommonCold` |  |
| `can_apply_to_anything` | Boolean | `true` |  |

</details>

---

### Context: `StatusOnTurnEndIfManaOrHealthExact`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `mana` | Number | `5, 4` |  |
| `IntelligenceUp` | Number | `1` | Applies the 'IntelligenceUp' effect. |
| `Shield` | Number | `5` | Applies the 'Shield' effect. |
| `SpellDamageUp` | Number | `1` | Applies the 'SpellDamageUp' effect. |
| `DivineShield` | Number | `1` | Applies the 'DivineShield' effect. |
| `HealthGain` | Number | `5` | Applies the 'HealthGain' effect. |
| `KineticSpikes` | Number | `1` | Applies the 'KineticSpikes' effect. |

</details>

---

### Context: `AddStatusToExplosions`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddElement` | [`Enum/String`](./Enums.md#enum-addelement) | `Napalm, Fire` | Applies the 'AddElement' effect. |
| `Burn` | Number | `6, 3` | Applies the 'Burn' effect. |

</details>

---

### Context: `Conditional_Corpse`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Charmed` | Number | `1` | Applies the 'Charmed' effect. |
| `OverrideDamage` | Number | `0` | Applies the 'OverrideDamage' effect. |
| `Revive` | Number | `1` | Applies the 'Revive' effect. |
| `SafeDoomed` | Number | `1` | Applies the 'SafeDoomed' effect. |
| `TakeExtraTurn` | Number | `1` | Applies the 'TakeExtraTurn' effect. |
| `DamageUp` | Number | `2` | Combat Trigger: Deals damage to up. |
| `SpeedUp` | Number | `8` | Applies the 'SpeedUp' effect. |

</details>

---

### Context: `ManaCostReductionTagged`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `reduction` | Number | `50%, 1, 3` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `summon, musical` | The specific entity tag required or applied. |

</details>

---

### Context: `SpawnThingOnDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `CharmedLeech, Food, PoisonFood` |  |
| `good` | Boolean | `false, true` |  |
| `spawn_on_death_hit` | Boolean | `false` |  |
| `consider_all_layers` | Boolean | `true` |  |

</details>

---

### Context: `StatusAlliesOnDeath`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` | Applies the 'AllStatsUp' effect. |
| `HealAndOverhealToShield` | Number | `12, 20` | Applies the 'HealAndOverhealToShield' effect. |
| `Reanimate` | Number | `100%, 33%` | Applies the 'Reanimate' effect. |
| `TakeExtraTurn` | Number | `1` | Applies the 'TakeExtraTurn' effect. |
| `triggers_limit` | Number | `1` |  |
| `Freeze` | Number | `1` | Applies the 'Freeze' effect. |
| `FullHeal` | Number | `1` | Applies the 'FullHeal' effect. |

</details>

---

### Context: `MeleeRevengeDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `1, 0, 3` | The base damage properties of an attack. |
| `elements` | [`Array`](./Arrays.md#array-elements) | `[ Ice ], [ Fire ]` |  |
| `Poison` | Number | `3` | Applies the 'Poison' effect. |
| `SpreadDisease` | [`Block`](./Passives_and_Statuses.md#context-spreaddisease) | `{ ... }` | Provides a chance to transmit a disease status to adjacent targets. |
| `Weakness` | Number | `1` | Applies the 'Weakness' effect. |

</details>

---

### Context: `StatusOnDealtDamageThreshold`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RefreshMovePoints` | Number | `1` | Applies the 'RefreshMovePoints' effect. |
| `Shield` | Number | `2` | Applies the 'Shield' effect. |
| `count_overkill` | Boolean | `true` |  |
| `ignore_during_movement` | Boolean | `true` |  |
| `threshold` | Number | `10` |  |
| `AllStatsUp` | Number | `1` | Applies the 'AllStatsUp' effect. |

</details>

---

### Context: `Else`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `CaptureFamiliar` | Number | `1` | Applies the 'CaptureFamiliar' effect. |
| `FactionConversion` | Number | `1` | Applies the 'FactionConversion' effect. |
| `Marked` | Number | `1` | Applies the 'Marked' effect. |
| `PermanentCharm` | Number | `1` | Applies the 'PermanentCharm' effect. |
| `Fear` | Number | `1` | Applies the 'Fear' effect. |
| `TempSpeedUp` | Number | `4` | Applies the 'TempSpeedUp' effect. |

</details>

---

### Context: `PassiveAtStatThreshold`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `mode` | [`Enum/String`](./Enums.md#enum-mode) | `less_or_equal` |  |

</details>

---

### Context: `StatusEveryXSpellCasts`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | `6, 3` | The number of stacks, duration, or intensity to apply. |
| `AllStatsUp` | Number | `1` | Applies the 'AllStatsUp' effect. |
| `SpellDamageUp` | Number | `1` | Applies the 'SpellDamageUp' effect. |
| `ReduceManaCost` | Number | `1` | Applies the 'ReduceManaCost' effect. |
| `RepairWeapon` | Number | `1` | Applies the 'RepairWeapon' effect. |
| `RepairWeaponCondition` | Number | `1` | Applies the 'RepairWeaponCondition' effect. |

</details>

---

### Context: `StatusOnTurnEndIfManaExact`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `mana` | Number | `2, 0` |  |
| `FreeSpell` | Number | `1` | Applies the 'FreeSpell' effect. |
| `Quivered` | Number | `1` | Applies the 'Quivered' effect. |
| `MoveQuivered` | Number | `1` | Applies the 'MoveQuivered' effect. |
| `SpellDamageUp` | Number | `1` | Applies the 'SpellDamageUp' effect. |

</details>

---

### Context: `threshold`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `int` | Number | `-10, 0, 4` |  |
| `cha` | Number | `0` |  |
| `spd` | Number | `0` |  |

</details>

---

### Context: `AddStatusToBasicMeleeAttack`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Confusion` | Number | `1` | Applies the 'Confusion' effect. |
| `Bruise` | Number | `1` | Applies the 'Bruise' effect. |
| `FaceAway` | Number | `1` | Applies the 'FaceAway' effect. |
| `Stun` | [`Array`](./Arrays.md#array-stun) | `[ 1 .15 ], [ 1 .2 ]` | Applies the 'Stun' effect. |

</details>

---

### Context: `AddStatusToElementAbilities`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `element` | [`Enum/String`](./Enums.md#enum-element) | `Gravity` | The specific element type required or applied. |
| `ChangeTile` | [`Enum/String`](./Enums.md#enum-changetile) | `FloatingGlassTile` | Transforms the terrain tile under the target. |
| `Bleed` | Number | `1` | Applies the 'Bleed' effect. |

</details>

---

### Context: `PassiveIfAllArmorEmpty`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddSpellDamage` | Number | `2, 1` | Applies the 'AddSpellDamage' effect. |
| `CounterAttack` | [`Enum/String`](./Enums.md#enum-counterattack) | `attack` | Applies the 'CounterAttack' effect. |
| `ExtraMovePoints` | Number | `1` | Applies the 'ExtraMovePoints' effect. |
| `ManaCostReduction` | Number | `1` | Applies the 'ManaCostReduction' effect. |
| `Flying` | Number | `1` | Applies the 'Flying' effect. |

</details>

---

### Context: `StatusOnCrit`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `LuckUp` | Number | `1` | Applies the 'LuckUp' effect. |
| `DamageUp` | Number | `1` | Combat Trigger: Deals damage to up. |
| `Shield` | Number | `2, 3` | Applies the 'Shield' effect. |
| `CritChanceUp` | Number | `5` | Applies the 'CritChanceUp' effect. |
| `RandomStatUp` | Number | `1` | Applies the 'RandomStatUp' effect. |

</details>

---

### Context: `StatusOnTurnEndIfCastNSpells`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `spells` | Number | `2, 1` |  |
| `DoubleCastSpell` | Number | `2, 1` | Applies the 'DoubleCastSpell' effect. |
| `Quivered` | Number | `1` | Applies the 'Quivered' effect. |
| `MoveQuivered` | Number | `1` | Applies the 'MoveQuivered' effect. |

</details>

---

### Context: `schadenfreude_scaled_stats`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `con` | Number | `2` |  |
| `str` | Number | `2` |  |
| `cha` | Number | `2` |  |
| `dex` | Number | `2` |  |
| `int` | Number | `2` |  |
| `lck` | Number | `2` |  |
| `spd` | Number | `2` |  |

</details>

---

### Context: `AddDamageToElementDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `2, 1` | The base damage properties of an attack. |
| `element` | [`Enum/String`](./Enums.md#enum-element) | `Electric, Fire` | The specific element type required or applied. |

</details>

---

### Context: `AllyManaRegenAura`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `range` | [`Enum/String`](./Enums.md#enum-range) | `global` | Distance or area of effect in tiles. |
| `stacks` | Number | `2, 1` | The number of stacks, duration, or intensity to apply. |

</details>

---

### Context: `AutocastEachRound`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `MedicObey, RaiseTheDead, MedicObey2` | The ID of the ability to autocast. |
| `even_if_stunned` | Boolean | `true` | If true, bypasses stun and hard-CC restrictions to cast anyway. |
| `force_display_name` | Boolean | `true` |  |

</details>

---

### Context: `DistanceBonusDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `min_range` | Number | `1, 3` |  |
| `stacks` | Number | `1` | The number of stacks, duration, or intensity to apply. |

</details>

---

### Context: `GravityWell`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cant_miss` | Boolean | `true` |  |
| `damage` | Number | `0, 5` | The base damage properties of an attack. |
| `elements` | [`Array`](./Arrays.md#array-elements) | `[ Gravity ]` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `status` | The classification type (e.g., damage type or element). |

</details>

---

### Context: `PassiveAtHealthThreshold`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `mode` | [`Enum/String`](./Enums.md#enum-mode) | `less_or_equal, equal` |  |
| `threshold` | Number | `1, 5` |  |

</details>

---

### Context: `StatusIfUnusedMovePoints`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Number | `8` | Applies the 'HealthGain' effect. |
| `MoveQuivered` | Number | `2` | Applies the 'MoveQuivered' effect. |
| `Brace` | Number | `1` | Applies the 'Brace' effect. |
| `ConstitutionUp` | Number | `2` | Applies the 'ConstitutionUp' effect. |
| `ManaGain` | Number | `5` | Applies the 'ManaGain' effect. |
| `Shield` | Number | `2` | Applies the 'Shield' effect. |

</details>

---

### Context: `AddSelfStatusToBasicAttack`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RandomMagicMissile` | Number | `1` | Fires a randomized number of magic missiles. |

</details>

---

### Context: `CatchProjectiles`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Quivered` | Number | `1` | Applies the 'Quivered' effect. |
| `ally_chance` | Number | `100%` |  |
| `chance` | Number | `50%, 33%` | The probability (0.0 to 1.0 or percentage) of this effect triggering. |
| `AllStatsUp` | Number | `1` | Applies the 'AllStatsUp' effect. |

</details>

---

### Context: `PassiveIfEmptyFace`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddCritMultiplier` | Number | `25%, 40%` | Applies the 'AddCritMultiplier' effect. |
| `CritChanceUp` | Number | `10` | Applies the 'CritChanceUp' effect. |
| `DodgeChance` | Number | `15%, 10%` | Applies the 'DodgeChance' effect. |
| `KineticSpikes` | Number | `1` | Applies the 'KineticSpikes' effect. |

</details>

---

### Context: `PassiveIfEmptyHead`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddCritMultiplier` | Number | `25%, 40%` | Applies the 'AddCritMultiplier' effect. |
| `CritChanceUp` | Number | `10` | Applies the 'CritChanceUp' effect. |
| `DodgeChance` | Number | `15%, 10%` | Applies the 'DodgeChance' effect. |
| `KineticSpikes` | Number | `1` | Applies the 'KineticSpikes' effect. |

</details>

---

### Context: `PassiveIfEmptyNeck`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddCritMultiplier` | Number | `25%, 40%` | Applies the 'AddCritMultiplier' effect. |
| `CritChanceUp` | Number | `10` | Applies the 'CritChanceUp' effect. |
| `DodgeChance` | Number | `15%, 10%` | Applies the 'DodgeChance' effect. |
| `KineticSpikes` | Number | `1` | Applies the 'KineticSpikes' effect. |

</details>

---

### Context: `StatusEachTurnBegin`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `FillMana` | [`Array`](./Arrays.md#array-fillmana) | `[ 1 .10 ], [ 1 .25 ]` | Applies the 'FillMana' effect. |
| `IntelligenceUp` | Number | `1` | Applies the 'IntelligenceUp' effect. |
| `RandomStatUp` | Number | `2, 3` | Applies the 'RandomStatUp' effect. |
| `Fear` | [`Array`](./Arrays.md#array-fear) | `[ 1 .15 ]` | Applies the 'Fear' effect. |

</details>

---

### Context: `StatusGroup`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `LuckUp` | Number | `2` | Applies the 'LuckUp' effect. |
| `SpawnCoinAnywhere` | Number | `1` | Applies the 'SpawnCoinAnywhere' effect. |
| `SpeedUp` | Number | `2` | Applies the 'SpeedUp' effect. |
| `DexterityUp` | Number | `2` | Applies the 'DexterityUp' effect. |

</details>

---

### Context: `StatusPerInjury`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Shield` | Number | `3` | Applies the 'Shield' effect. |
| `cap` | Number | `10` |  |
| `injury` | [`Enum/String`](./Enums.md#enum-injury) | `int` |  |
| `StrengthUp` | Number | `1` | Applies the 'StrengthUp' effect. |

</details>

---

### Context: `AbilityWhenTaggedCharacterMovesNear`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `move` | The ID of the ability to trigger or reference. |
| `range` | Number | `2, global` | Distance or area of effect in tiles. |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `food` | The specific entity tag required or applied. |

</details>

---

### Context: `AddPassivesToCharmed`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddMaxHealth` | Number | `10, 5` | Applies the 'AddMaxHealth' effect. |
| `AddSpeed` | Number | `4` | Applies the 'AddSpeed' effect. |
| `DamageUp` | Number | `2, 3` | Combat Trigger: Deals damage to up. |

</details>

---

### Context: `AddPassivesToSummonAbilityMinions`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DamageUp` | Number | `2, 4` | Combat Trigger: Deals damage to up. |
| `Doomed` | Number | `1` | Applies the 'Doomed' effect. |
| `MovementUp` | Number | `2, 4` | Applies the 'MovementUp' effect. |

</details>

---

### Context: `AddStatusToElementDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `element` | [`Enum/String`](./Enums.md#enum-element) | `Electric, Fire` | The specific element type required or applied. |
| `Burn` | Number | `1, 3` | Applies the 'Burn' effect. |

</details>

---

### Context: `AddStatusToWeapons`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | `1` | Applies the 'Bleed' effect. |
| `PullSourceToKnockbackImmuneTarget` | Number | `1` | Applies the 'PullSourceToKnockbackImmuneTarget' effect. |
| `Cleave` | Number | `1` | Causes the attack to hit adjacent enemies alongside the primary target. |
| `LeechPercent` | Number | `50` | Applies the 'LeechPercent' effect. |

</details>

---

### Context: `AmplifyStatus`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `addstacks` | Number | `2` |  |
| `status` | [`Enum/String`](./Enums.md#enum-status) | `Poison, Burn, Bleed` | The ID of the status effect to check or apply. |

</details>

---

### Context: `Conditional_Adjacent`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | `2, 1` | Applies the 'Bleed' effect. |
| `BonusCritChance` | Number | `50, 25` | Applies the 'BonusCritChance' effect. |
| `BonusDamage` | Number | `2, 3` | Applies the 'BonusDamage' effect. |

</details>

---

### Context: `DamageNeighborsAfterMove`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | [`Enum/String`](./Enums.md#enum-damage) | `X` | The base damage properties of an attack. |
| `elements` | [`Array`](./Arrays.md#array-elements) | `[ Electric ]` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `spell` | The classification type (e.g., damage type or element). |

</details>

---

### Context: `DamageReductionAura`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `allies_only` | Boolean | `true` |  |
| `range` | [`Enum/String`](./Enums.md#enum-range) | `global` | Distance or area of effect in tiles. |
| `stacks` | Number | `2, 1` | The number of stacks, duration, or intensity to apply. |

</details>

---

### Context: `ElementalManaCostReduction`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `element` | [`Enum/String`](./Enums.md#enum-element) | `Gravity, [ Fire Ice Electric Earth Wind Water Grass Holy Gravity ]` | The specific element type required or applied. |
| `reduction` | Number | `2, 1` |  |

</details>

---

### Context: `Eternal`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `health_percent` | Number | `50%` |  |
| `stacks` | Number | `1` | The number of stacks, duration, or intensity to apply. |
| `AllStatsUp` | Number | `2` | Applies the 'AllStatsUp' effect. |
| `TakeExtraTurn` | Number | `1` | Applies the 'TakeExtraTurn' effect. |

</details>

---

### Context: `ForceUseAbility`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`StatusEachTurnEnd`](./Passives_and_Statuses.md#context-statuseachturnend)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `TigerForm, CrohnsPoop, DysenteryPoop` | The ID of the ability to trigger or reference. |
| `chance` | [`Enum/String`](./Enums.md#enum-chance) | `.5, .2, 33%` | The probability (0.0 to 1.0 or percentage) of this effect triggering. |

</details>

---

### Context: `HealAlliesEachTurn`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `exclude_self` | Boolean | `false` |  |
| `mana` | Number | `2, 3` |  |
| `stacks` | Number | `2, 3` | The number of stacks, duration, or intensity to apply. |

</details>

---

### Context: `InfiniteRebirth`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `TempSpeedUp` | Number | `10` | Applies the 'TempSpeedUp' effect. |
| `health` | Number | `25%, 1` |  |
| `playercat_health` | Number | `100%` |  |

</details>

---

### Context: `MoveTowardsDamageSource`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `move_ability` | [`Enum/String`](./Enums.md#enum-move_ability) | `move, TrampleMove, TrampleMoveOne` |  |
| `move_far` | Boolean | `false` |  |

</details>

---

### Context: `ObjectOnHitCharacter`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `CharmedFlea` | The entity ID of the character to spawn (e.g., CharmedFlea). |
| `stacks` | Number | `2, 1` | The number of stacks, duration, or intensity to apply. |

</details>

---

### Context: `PassiveAtInjuryThreshold`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `injury` | [`Enum/String`](./Enums.md#enum-injury) | `spd` |  |
| `mode` | [`Enum/String`](./Enums.md#enum-mode) | `greater_or_equal` |  |
| `threshold` | Number | `4` |  |

</details>

---

### Context: `PassiveGroup`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `SetDefaultFace` | [`Enum/String`](./Enums.md#enum-setdefaultface) | `sad, happy` | Applies the 'SetDefaultFace' effect. |
| `AllStatsUp` | Number | `-2` | Applies the 'AllStatsUp' effect. |
| `CharismaUp` | Number | `5` | Applies the 'CharismaUp' effect. |
| `IntelligenceUp` | Number | `5` | Applies the 'IntelligenceUp' effect. |
| `SpeedUp` | Number | `5` | Applies the 'SpeedUp' effect. |

</details>

---

### Context: `PassiveWhenAtFullMana`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Brace` | Number | `2, 3` | Applies the 'Brace' effect. |
| `Flying` | Number | `1` | Applies the 'Flying' effect. |
| `AddMovement` | Number | `20` | Applies the 'AddMovement' effect. |
| `ReplaceBasicMove` | [`Enum/String`](./Enums.md#enum-replacebasicmove) | `Teleport` | Applies the 'ReplaceBasicMove' effect. |

</details>

---

### Context: `SmiteEnemiesWhoKill`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `10` | The base damage properties of an attack. |
| `elements` | [`Array`](./Arrays.md#array-elements) | `[ Holy ]` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `spell` | The classification type (e.g., damage type or element). |

</details>

---

### Context: `SpawnCatCopyOnBattleStart`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `PlayerCat_MiniMiniMe, PlayerCat_MiniMe` |  |
| `prevent_chain_tag` | [`Enum/String`](./Enums.md#enum-prevent_chain_tag) | `minime_clone` |  |

</details>

---

### Context: `SpawnOnBattleStartRandomEmptyTile`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `number` | [`Array`](./Arrays.md#array-number) | `10, [ 2 3 ], [ 1 2 ]` |  |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `RandomPickup, Coin` |  |

</details>

---

### Context: `StatusOnAllyCatDeath`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `2` | Applies the 'AllStatsUp' effect. |
| `FillMana` | Number | `1` | Applies the 'FillMana' effect. |
| `HealthGain` | Number | `8` | Applies the 'HealthGain' effect. |
| `PercentHeal` | Number | `50` | Applies the 'PercentHeal' effect. |
| `TakeExtraTurn` | Number | `1` | Applies the 'TakeExtraTurn' effect. |

</details>

---

### Context: `StatusOnOverHealed`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ForceUseAbility_NonStack` | [`Enum/String`](./Enums.md#enum-forceuseability_nonstack) | `Indigestion_Fart2, Indigestion_Fart` | Applies the 'ForceUseAbility_NonStack' effect. |
| `StrengthUp` | Number | `1` | Applies the 'StrengthUp' effect. |
| `CurrentWeaponDamageUp` | Number | `1` | Applies the 'CurrentWeaponDamageUp' effect. |
| `SpawnScaledRotFly` | Number | `0` | Applies the 'SpawnScaledRotFly' effect. |

</details>

---

### Context: `empty_armor_scaled_stats`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cha` | Number | `1` |  |
| `int` | Number | `1` |  |
| `spd` | Number | `2, 1` |  |

</details>

---

### Context: `statuses`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `FindItemFromPool` | [`Enum/String`](./Enums.md#enum-finditemfrompool) | `consumables, chapter` | Generates an item drop from the specified loot pool. |
| `PermanentDexterity` | Number | `1` | Applies the 'PermanentDexterity' effect. |
| `AllStatsUp` | Number | `1` | Applies the 'AllStatsUp' effect. |
| `HealthGain` | Number | `10` | Applies the 'HealthGain' effect. |

</details>

---

### Context: `Conditional_FirstApplicationThisTurn`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `TakeExtraTurn` | Number | `1` | Applies the 'TakeExtraTurn' effect. |
| `AllStatsUp` | Number | `1` | Applies the 'AllStatsUp' effect. |
| `FillMana` | Number | `1` | Applies the 'FillMana' effect. |
| `ManaGain` | Number | `5` | Applies the 'ManaGain' effect. |

</details>

---

### Context: `PassiveWhileInMonkRangedStance`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddBonusRange` | Number | `2, 1` | Applies the 'AddBonusRange' effect. |
| `AddSpellDamage` | Number | `2` | Applies the 'AddSpellDamage' effect. |
| `KineticSpikes` | Number | `2` | Applies the 'KineticSpikes' effect. |

</details>

---

### Context: `StatusAlliesOnGainCoins`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Number | `1` | Applies the 'HealthGain' effect. |
| `LuckUp` | Number | `1` | Applies the 'LuckUp' effect. |
| `scaled` | Boolean | `true` |  |

</details>

---

### Context: `StatusAlliesOnKill`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` | Applies the 'AllStatsUp' effect. |
| `DamageUp` | Number | `1` | Combat Trigger: Deals damage to up. |
| `HealthGain` | Number | `5` | Applies the 'HealthGain' effect. |

</details>

---

### Context: `StatusOnCastSpell`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | `2, 1` | Applies the 'Charge' effect. |
| `CurrentWeaponDamageUp` | Number | `1` | Applies the 'CurrentWeaponDamageUp' effect. |
| `HealthGain` | Number | `1` | Applies the 'HealthGain' effect. |

</details>

---

### Context: `StatusOnDealtDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `TempDexterityUp` | Number | `2` | Applies the 'TempDexterityUp' effect. |
| `TempStrengthUp` | Number | `2, 1` | Applies the 'TempStrengthUp' effect. |
| `TempLuckUp` | Number | `2` | Applies the 'TempLuckUp' effect. |

</details>

---

### Context: `StatusOnEatFood`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `StrengthUp` | Number | `1` | Applies the 'StrengthUp' effect. |
| `Cleanse` | Number | `0` | Applies the 'Cleanse' effect. |
| `IntelligenceUp` | Number | `1` | Applies the 'IntelligenceUp' effect. |
| `RandomStatUp` | Number | `1` | Applies the 'RandomStatUp' effect. |

</details>

---

### Context: `StatusOnKillEnemy`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DivineShield` | Number | `1` | Applies the 'DivineShield' effect. |
| `HealthGain` | Number | `2` | Applies the 'HealthGain' effect. |
| `ManaGain` | Number | `3` | Applies the 'ManaGain' effect. |
| `RefreshMovePoints` | Number | `1` | Applies the 'RefreshMovePoints' effect. |

</details>

---

### Context: `StatusOnOverMana`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `IntelligenceUp` | Number | `1` | Applies the 'IntelligenceUp' effect. |
| `SpellDamageUp` | Number | `1` | Applies the 'SpellDamageUp' effect. |
| `DivineShield` | Number | `1` | Applies the 'DivineShield' effect. |

</details>

---

### Context: `AddPassiveToSpawnedRocks`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddFilledMaxHealth` | Number | `7, 3` | Applies the 'AddFilledMaxHealth' effect. |
| `JoinSpawnerFaction` | Number | `1` | Applies the 'JoinSpawnerFaction' effect. |

</details>

---

### Context: `AddStatusToAllDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `LeaveBehindRockOnKnockback` | Number | `1` | Applies the 'LeaveBehindRockOnKnockback' effect. |
| `Blind` | Number | `1` | Applies the 'Blind' effect. |
| `NonLethal` | Number | `1` | Applies the 'NonLethal' effect. |

</details>

---

### Context: `AllyBonusAbilityAura`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `Bowl, Bowl2` | The ID of the ability to trigger or reference. |
| `square` | Boolean | `true` |  |

</details>

---

### Context: `AllyHealthRegenAura`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `range` | [`Enum/String`](./Enums.md#enum-range) | `global` | Distance or area of effect in tiles. |
| `stacks` | Number | `2, 1` | The number of stacks, duration, or intensity to apply. |

</details>

---

### Context: `AlternateCraftingPools`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `tinkerer_0` | [`Enum/String`](./Enums.md#enum-tinkerer_0) | `tinkerer_0_bombs` |  |
| `tinkerer_1` | [`Enum/String`](./Enums.md#enum-tinkerer_1) | `tinkerer_1_bombs` |  |

</details>

---

### Context: `BoostWeaponDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `crit_chance` | [`Enum/String`](./Enums.md#enum-crit_chance) | `.5, .25` |  |
| `damage` | Number | `2, 3` | The base damage properties of an attack. |

</details>

---

### Context: `BouncyProjectiles`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `max_bounces` | Number | `2, 1` |  |
| `max_range` | Number | `4, 3` |  |

</details>

---

### Context: `CatAPultAnimation`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `CatapultJump2, CatapultJump` | The ID of the ability to trigger or reference. |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `knockupatk` |  |

</details>

---

### Context: `ChanceToBackflip`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `BlinkDodge` | The ID of the ability to trigger or reference. |
| `chance` | Number | `50%, 33%` | The probability (0.0 to 1.0 or percentage) of this effect triggering. |

</details>

---

### Context: `ClassManaCostReduction`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `class` | [`Enum/String`](./Enums.md#enum-class) | `Colorless` | Character class identifier. |
| `reduction` | Number | `2, 1` |  |

</details>

---

### Context: `Conditional_Enemy`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Confusion` | Number | `2, 3` | Applies the 'Confusion' effect. |
| `Stun` | [`Array`](./Arrays.md#array-stun) | `[ 1 .5 ]` | Applies the 'Stun' effect. |

</details>

---

### Context: `Conditional_HasTag`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `poop, rat` | The specific string tag to check for. |
| `Charmed` | Number | `1` | Applies the 'Charmed' effect. |
| `FlatLeechIfDamaged` | Number | `5` | Applies the 'FlatLeechIfDamaged' effect. |

</details>

---

### Context: `Craft`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `pool` | [`Enum/String`](./Enums.md#enum-pool) | `tinkerer_default` |  |
| `slot` | [`Enum/String`](./Enums.md#enum-slot) | `random_empty_armor_or_weapon` |  |

</details>

---

### Context: `DeathRattle`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `LastGasp, LastGasp2` | The ID of the ability to trigger or reference. |
| `pop_corpse` | Boolean | `false` |  |

</details>

---

### Context: `EMP`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `status_explosion_override` | [`Enum/String`](./Enums.md#enum-status_explosion_override) | `WaterConduct` |  |

</details>

---

### Context: `EscapeSequence`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RandomDistanceDisplace` | Number | `20` | Displaces the target by a randomized distance. |
| `SafeExplosionIfHitSomething` | Number | `10, 5` | Applies the 'SafeExplosionIfHitSomething' effect. |

</details>

---

### Context: `HolyDamageBlessing`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Burn` | Number | `2, 3` | Applies the 'Burn' effect. |
| `damage_multiplier` | Number | `2, 3` |  |

</details>

---

### Context: `LateBloomer`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `3` | Applies the 'AllStatsUp' effect. |
| `stacks` | Number | `5, 3` | The number of stacks, duration, or intensity to apply. |

</details>

---

### Context: `LowHealthAllyDodgeChanceAura`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Number | `50%` | The probability (0.0 to 1.0 or percentage) of this effect triggering. |
| `theshold` | Number | `5` |  |

</details>

---

### Context: `MovementReaction`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `weapon` | The ID of the ability to trigger or reference. |
| `enemies_only` | Boolean | `true` |  |

</details>

---

### Context: `NextBattleStatus`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `3` | Applies the 'AllStatsUp' effect. |
| `FullHeal` | Number | `1` | Applies the 'FullHeal' effect. |

</details>

---

### Context: `PassiveAtFullHealth`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ManaCostReduction` | Number | `2` | Applies the 'ManaCostReduction' effect. |
| `TakeExtraDamage` | Number | `200%` | Applies the 'TakeExtraDamage' effect. |

</details>

---

### Context: `PassiveWhenAffectedByElement`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `element` | [`Enum/String`](./Enums.md#enum-element) | `water` | The specific element type required or applied. |

</details>

---

### Context: `RepressedMemoriesMetronome`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `pool` | [`Enum/String`](./Enums.md#enum-pool) | `Psychic, Jester` |  |
| `stacks` | Number | `1` | The number of stacks, duration, or intensity to apply. |

</details>

---

### Context: `SecurityBotProtect`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `attack` | The ID of the ability to trigger or reference. |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `move, MoveThree` |  |

</details>

---

### Context: `SpecialFriends`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `2` | Applies the 'AllStatsUp' effect. |
| `HealthGain` | Number | `8` | Applies the 'HealthGain' effect. |

</details>

---

### Context: `StatsAtLowHealth`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `threshold` | Number | `5` |  |
| `speed` | Number | `6` |  |
| `strength` | Number | `6` |  |

</details>

---

### Context: `StatusAllyWhenAllySpendsMana`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` | Applies the 'AllStatsUp' effect. |
| `threshold` | Number | `7` |  |

</details>

---

### Context: `StatusEnemiesOnDeath`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `-2, -1` | Applies the 'AllStatsUp' effect. |
| `Freeze` | Number | `2` | Applies the 'Freeze' effect. |

</details>

---

### Context: `StatusEveryXTurnBegins`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DivineShield` | Number | `1` | Applies the 'DivineShield' effect. |
| `turns` | Number | `2, 3` | The duration of the effect in turns. |

</details>

---

### Context: `StatusOnPickupCoins`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RefreshMovePoints` | Number | `1` | Applies the 'RefreshMovePoints' effect. |
| `DexterityUp` | Number | `1` | Applies the 'DexterityUp' effect. |
| `SpeedUp` | Number | `1` | Applies the 'SpeedUp' effect. |

</details>

---

### Context: `StatusOnUseElementAbility`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `SpeedUp` | Number | `2, 1` | Applies the 'SpeedUp' effect. |
| `element` | [`Enum/String`](./Enums.md#enum-element) | `Gravity` | The specific element type required or applied. |

</details>

---

### Context: `TaggedPickupEffectReplacement`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `HealthGain` | [`Enum/String`](./Enums.md#enum-healthgain) | `3*X, 2*X` | Applies the 'HealthGain' effect. |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `scrap, money` | The specific entity tag required or applied. |

</details>

---

### Context: `TowerDefense`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `2, 1` | The base damage properties of an attack. |
| `range` | Number | `2, 1` | Distance or area of effect in tiles. |

</details>

---

### Context: `3`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"DISORDER_SEVEREDEJAVU_DESC"` | Localization key for the passive's display description. |
| `icon` | [`Enum/String`](./Enums.md#enum-icon) | `DejaVu3` |  |
| `name` | String | `"DISORDER_SEVEREDEJAVU_NAME"` | Localization key for the passive's display name. |

</details>

---

### Context: `AbilityReaction`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `SpontaneouslyCombust` | The ID of the ability to trigger or reference. |
| `ability_damage_only` | Boolean | `true` |  |
| `chance` | Number | `15%` | The probability (0.0 to 1.0 or percentage) of this effect triggering. |

</details>

---

### Context: `AddStatusToAllDamageAbilities`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | `1` | Applies the 'Bleed' effect. |
| `Piercing` | Number | `1` | Applies the 'Piercing' effect. |
| `Weakness` | Number | `2` | Applies the 'Weakness' effect. |

</details>

---

### Context: `AddTemporaryEffectsToBasicAttack`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `CastAgain` | Number | `2, 1` | Applies the 'CastAgain' effect. |
| `Fury` | Number | `75` | Applies the 'Fury' effect. |

</details>

---

### Context: `ApplyStatusesToRandomEnemiesEachTurn`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Bounty` | Number | `1, 3` | Applies the 'Bounty' effect. |
| `count` | Number | `2` | The numerical quantity. |

</details>

---

### Context: `AutocastEachTurnBegin`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `PoxScratch` | The ID of the ability to trigger or reference. |
| `advantage_polarity` | Number | `-1` |  |
| `chance` | Number | `10%` | The probability (0.0 to 1.0 or percentage) of this effect triggering. |

</details>

---

### Context: `Conditional_BadRoll`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `odds` | [`Enum/String`](./Enums.md#enum-odds) | `.1` | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. |

</details>

---

### Context: `Conditional_HasStatus`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `status` | [`Enum/String`](./Enums.md#enum-status) | `Fear, Marked` | The specific status ID to check for. |

</details>

---

### Context: `FurnitureStats`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Appeal` | Number | `1` | Applies the 'Appeal' effect. |
| `Comfort` | Number | `1` | Applies the 'Comfort' effect. |
| `Stimulation` | Number | `1` | Applies the 'Stimulation' effect. |

</details>

---

### Context: `PassiveLevelScaledStatus`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Shield` | String | `"2*(X-1)"` | Applies the 'Shield' effect. |
| `SizeScalePercent` | String | `"sqrt(1.0+(.05*(X-1)))*100"` | Applies the 'SizeScalePercent' effect. |
| `Trample` | [`Array`](./Arrays.md#array-trample) | `[ 3, X-8 ]` | Applies the 'Trample' effect. |

</details>

---

### Context: `PassiveWhileInMonkMeleeStance`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Brace` | Number | `2, 1` | Applies the 'Brace' effect. |
| `HealthRegenUp` | Number | `2` | Applies the 'HealthRegenUp' effect. |

</details>

---

### Context: `ReplaceBrain`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `brain` | [`Enum/String`](./Enums.md#enum-brain) | `GenericBrain` |  |
| `decision_weights` | [`Enum/String`](./Enums.md#enum-decision_weights) | `default` |  |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `keep_distance` |  |

</details>

---

### Context: `ScaledStatusOnOverMana`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RandomMagicMissile` | Number | `1` | Fires a randomized number of magic missiles. |
| `Cleanse` | Number | `0` | Applies the 'Cleanse' effect. |

</details>

---

### Context: `StatusAfterCastSpell`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `TempSpellDamageUp` | Number | `1` | Applies the 'TempSpellDamageUp' effect. |
| `TempDamageUp` | Number | `1` | Applies the 'TempDamageUp' effect. |

</details>

---

### Context: `StatusDamagers`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `LuckUp` | Number | `-1` | Applies the 'LuckUp' effect. |
| `Fear` | [`Array`](./Arrays.md#array-fear) | `[ 1 .25 ]` | Applies the 'Fear' effect. |

</details>

---

### Context: `StatusOnBattleStart`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `FullHeal` | Number | `1` | Applies the 'FullHeal' effect. |
| `Sleep` | Number | `1` | Applies the 'Sleep' effect. |

</details>

---

### Context: `StatusOnBreakItem`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Thorns` | Number | `2, 1` | Applies the 'Thorns' effect. |
| `Shield` | Number | `3` | Applies the 'Shield' effect. |

</details>

---

### Context: `StatusOnHeal`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `SpeedUp` | Number | `2, 4` | Applies the 'SpeedUp' effect. |
| `RandomStatUp` | Number | `1` | Applies the 'RandomStatUp' effect. |

</details>

---

### Context: `StatusOnTookDamageFromAbility`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DiminishingHealthRegen` | Number | `2, 1` | Applies the 'DiminishingHealthRegen' effect. |
| `Shield` | Number | `2` | Applies the 'Shield' effect. |

</details>

---

### Context: `StatusOnTookDamageFromEnemyAbility`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Quivered` | Number | `1` | Applies the 'Quivered' effect. |
| `MoveQuivered` | Number | `1` | Applies the 'MoveQuivered' effect. |

</details>

---

### Context: `StatusOnTriggerTrap`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DexterityUp` | Number | `2` | Applies the 'DexterityUp' effect. |
| `Quivered` | Number | `1` | Applies the 'Quivered' effect. |

</details>

---

### Context: `StatusWhenAllySpendsMana`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `OneUseSpellDamageUp` | Number | `2` | Applies the 'OneUseSpellDamageUp' effect. |
| `ManaGain` | Number | `2` | Applies the 'ManaGain' effect. |

</details>

---

### Context: `fire`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `3` | The base damage properties of an attack. |
| `elements` | [`Array`](./Arrays.md#array-elements) | `[ Fire ]` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `spell` | The classification type (e.g., damage type or element). |

</details>

---

### Context: `ice`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `3` | The base damage properties of an attack. |
| `elements` | [`Array`](./Arrays.md#array-elements) | `[ Ice ]` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `spell` | The classification type (e.g., damage type or element). |

</details>

---

### Context: `keyword_tooltips`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Weakness` | Number | `1` | Applies the 'Weakness' effect. |
| `MagicWeakness` | Number | `1` | Applies the 'MagicWeakness' effect. |

</details>

---

### Context: `lightning`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `3` | The base damage properties of an attack. |
| `elements` | [`Array`](./Arrays.md#array-elements) | `[ Electric ]` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `spell` | The classification type (e.g., damage type or element). |

</details>

---

### Context: `triattack`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `6` | The base damage properties of an attack. |
| `elements` | [`Array`](./Arrays.md#array-elements) | `[ Fire Ice Electric ]` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `spell` | The classification type (e.g., damage type or element). |

</details>

---

### Context: `AbilityChargeRefundChance`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `advantage_softcap` | Number | `3.5` |  |
| `chance` | Number | `50%` | The probability (0.0 to 1.0 or percentage) of this effect triggering. |

</details>

---

### Context: `AddSelfStatusToWeapons`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ChanceToBreak` | Number | `100, 50` | Applies the 'ChanceToBreak' effect. |

</details>

---

### Context: `AddStatusToBasicAttackWithCooldown`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `CharmedForceAttack` | Number | `1` | Applies the 'CharmedForceAttack' effect. |

</details>

---

### Context: `AddStatusToFirstBasicAttack`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Charmed` | Number | `5` | Applies the 'Charmed' effect. |

</details>

---

### Context: `AddStatusToTrampleDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Cleave` | Number | `1` | Causes the attack to hit adjacent enemies alongside the primary target. |

</details>

---

### Context: `AddStatusesIfPersistentWeatherElement`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Burn` | Number | `3` | Applies the 'Burn' effect. |
| `elements` | [`Array`](./Arrays.md#array-elements) | `[ Heat Fire ]` |  |

</details>

---

### Context: `AddStatusesToReceivedElementalDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Burn` | Number | `3` | Applies the 'Burn' effect. |
| `elements` | [`Array`](./Arrays.md#array-elements) | `[ Heat Fire ]` |  |

</details>

---

### Context: `ApplyStatusIfCrit`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Purge` | Number | `0` | Applies the 'Purge' effect. |

</details>

---

### Context: `ApplyToSource`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` | Applies the 'AllStatsUp' effect. |
| `Shield` | Number | `1` | Applies the 'Shield' effect. |

</details>

---

### Context: `Autism`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `innate` | Number | `-2` |  |
| `learned` | Number | `1` |  |

</details>

---

### Context: `ChangeTile`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `aoe` | Number | `1` | The area of effect or distance in tiles. |
| `tile` | [`Enum/String`](./Enums.md#enum-tile) | `BrambleTile` | The specific tile type to change into (e.g., GlassTile). |

</details>

---

### Context: `Conditional_Boss`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Charmed` | Number | `1` | Applies the 'Charmed' effect. |
| `Stun` | Number | `3` | Applies the 'Stun' effect. |

</details>

---

### Context: `Conditional_GoodRoll`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `UseRandomSpell_Madness` | Number | `1` | Applies the 'UseRandomSpell_Madness' effect. |
| `odds` | Number | `33%` | The probability (0.0 to 1.0) of triggering the 'good roll' success state. |

</details>

---

### Context: `Conditional_PartyMember`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Charmed` | Number | `5` | Applies the 'Charmed' effect. |

</details>

---

### Context: `Conditional_Shielded`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `BonusCritChance` | Number | `100` | Applies the 'BonusCritChance' effect. |

</details>

---

### Context: `DamageIfDidntUseSpecificAbility`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `Groom` | The ID of the ability to trigger or reference. |
| `damage` | Number | `2` | The base damage properties of an attack. |

</details>

---

### Context: `Diabetes`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `-1` | Applies the 'AllStatsUp' effect. |
| `Confusion` | Number | `1` | Applies the 'Confusion' effect. |

</details>

---

### Context: `Earth`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | [`Enum/String`](./Enums.md#enum-damage) | `X` | The base damage properties of an attack. |

</details>

---

### Context: `Electric`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Stun` | [`Array`](./Arrays.md#array-stun) | `[ 1 .1*X ]` | Applies the 'Stun' effect. |

</details>

---

### Context: `EnergyStorm`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cycle_start` | Number | `2` |  |
| `period` | Number | `3` |  |

</details>

---

### Context: `FindItemFromPool`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Passives_and_Statuses.md#context-statusonbattleend)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | [`Enum/String`](./Enums.md#enum-chance) | `.5` | Probability of finding the item. |
| `pool` | [`Enum/String`](./Enums.md#enum-pool) | `pills` | The item pool to draw from. |

</details>

---

### Context: `Fire`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Burn` | [`Enum/String`](./Enums.md#enum-burn) | `X` | Applies the 'Burn' effect. |

</details>

---

### Context: `Grass`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Poison` | [`Enum/String`](./Enums.md#enum-poison) | `X` | Applies the 'Poison' effect. |

</details>

---

### Context: `Gravity`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Weakness` | [`Enum/String`](./Enums.md#enum-weakness) | `X` | Applies the 'Weakness' effect. |

</details>

---

### Context: `Holy`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `FlatLeech` | [`Enum/String`](./Enums.md#enum-flatleech) | `X` | Applies the 'FlatLeech' effect. |

</details>

---

### Context: `Ice`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Slow` | [`Enum/String`](./Enums.md#enum-slow) | `X` | Applies the 'Slow' effect. |

</details>

---

### Context: `LightningRod`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Tech` | Number | `1` | Applies the 'Tech' effect. |

</details>

---

### Context: `MegaMinions`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cycle_start` | Number | `3` |  |
| `stacks` | Number | `3` | The number of stacks, duration, or intensity to apply. |

</details>

---

### Context: `PassiveAfterXKills`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | `3` | The number of stacks, duration, or intensity to apply. |

</details>

---

### Context: `PassiveWhenTheAlpha`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `TogglableRoundEndExtraTurn` | Number | `1` | Applies the 'TogglableRoundEndExtraTurn' effect. |

</details>

---

### Context: `PassiveWhilePreviewingMonkRangedStance`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddBonusRange` | Number | `2, 1` | Applies the 'AddBonusRange' effect. |

</details>

---

### Context: `PassiveWhileWearingMetal`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddElementsToWeapon` | [`Enum/String`](./Enums.md#enum-addelementstoweapon) | `Electric` | Applies the 'AddElementsToWeapon' effect. |

</details>

---

### Context: `RevengeDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `knockback` | Number | `10` |  |

</details>

---

### Context: `SelfDamageWhenDealDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `1` | The base damage properties of an attack. |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `status` | The classification type (e.g., damage type or element). |

</details>

---

### Context: `Shadow`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `crit_chance` | [`Enum/String`](./Enums.md#enum-crit_chance) | `.05*X` |  |

</details>

---

### Context: `StackingDodgeChanceOnTookDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `amount` | Number | `10%` | The numerical quantity. |
| `cap` | Number | `50%` |  |

</details>

---

### Context: `StatusAlliesEachTurn`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RandomStatUp` | Number | `3` | Applies the 'RandomStatUp' effect. |
| `exclude_self` | Boolean | `false` |  |

</details>

---

### Context: `StatusAlliesOnBattleStart`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `EquipTemporaryItem` | [`Enum/String`](./Enums.md#enum-equiptemporaryitem) | `SleepDart, SleepDart2` | Applies the 'EquipTemporaryItem' effect. |

</details>

---

### Context: `StatusAnyCatAllyWhoKills`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AlphaCat` | Number | `1` | Applies the 'AlphaCat' effect. |

</details>

---

### Context: `StatusEachTurnEndForEachTurn`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RandomMagicMissile` | Number | `2, 4` | Fires a randomized number of magic missiles. |

</details>

---

### Context: `StatusKilledCharacters`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AutoReanimate` | Number | `50%, 100%` | Applies the 'AutoReanimate' effect. |

</details>

---

### Context: `StatusOnAnyDeath`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `LuckUp` | Number | `1` | Applies the 'LuckUp' effect. |

</details>

---

### Context: `StatusOnBattleEndIfKillThresholdMet`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `kills` | Number | `3` |  |

</details>

---

### Context: `StatusOnCollectPickup`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Tech` | Number | `1` | Applies the 'Tech' effect. |

</details>

---

### Context: `StatusOnEndMove`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ForceAttack` | Number | `1` | Forces the character to execute an immediate attack. |

</details>

---

### Context: `StatusOnHealed`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ObjectOnHitCharacter` | [`Enum/String`](./Enums.md#enum-objectonhitcharacter) | `CharmedLeech` | Spawns a specific character or entity upon impact. |
| `Thorns` | Number | `1` | Applies the 'Thorns' effect. |

</details>

---

### Context: `StatusOnPopCorpse`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Number | `8, 2` | Applies the 'HealthGain' effect. |

</details>

---

### Context: `StatusOnTurnEndIfDidntCastAbilityTypes`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ManaGain` | Number | `7` | Applies the 'ManaGain' effect. |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `attack` | The classification type (e.g., damage type or element). |

</details>

---

### Context: `StatusOnUseBasicAttack`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `FlippedFacingForceAttack` | Number | `1` | Applies the 'FlippedFacingForceAttack' effect. |

</details>

---

### Context: `StatusThingsKnockedBack`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Drag` | Number | `2, 1` | Applies the 'Drag' effect. |

</details>

---

### Context: `StrengthInNumbersAura`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `count_self` | Boolean | `true` |  |
| `stacks` | Number | `1` | The number of stacks, duration, or intensity to apply. |

</details>

---

### Context: `Study`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `marked` | Number | `2` |  |
| `stacks` | Number | `1` | The number of stacks, duration, or intensity to apply. |

</details>

---

### Context: `TileDamageMultiplier`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ally_multiplier` | Number | `0` |  |
| `multiplier` | Number | `2` | Multiplicative modifier to a base value. |

</details>

---

### Context: `TourettesMeows`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cooldown` | [`Array`](./Arrays.md#array-cooldown) | `[ 8 15 ]` |  |
| `pool` | [`Array`](./Arrays.md#array-pool) | `[ Hit Hiss Normal ]` |  |

</details>

---

### Context: `Water`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AOEPuddle` | [`Enum/String`](./Enums.md#enum-aoepuddle) | `X-1` | Applies the 'AOEPuddle' effect. |

</details>

---

### Context: `Wind`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `knockback` | [`Enum/String`](./Enums.md#enum-knockback) | `X` |  |

</details>

---

### Context: `on_break`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `SafeExplosionIfHitSomething` | Number | `10, 5` | Applies the 'SafeExplosionIfHitSomething' effect. |

</details>

---

### Context: `on_throw`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `HitExplosion` | Number | `10, 5` | Applies the 'HitExplosion' effect. |

</details>

---

### Context: `10`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"DISORDER_DISTEMPERMAX_DESC"` | Localization key for the passive's display description. |

</details>

---

### Context: `AddStatusToKnockbackDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Bruise` | Number | `1` | Applies the 'Bruise' effect. |

</details>

---

### Context: `AddStatusToSpells`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `LeechPercent` | Number | `50` | Applies the 'LeechPercent' effect. |

</details>

---

### Context: `AddTemporaryEffectsToEquipment`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `CastAgain` | Number | `1` | Applies the 'CastAgain' effect. |

</details>

---

### Context: `ChanceToRevive`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | `33` | The number of stacks, duration, or intensity to apply. |

</details>

---

### Context: `CollectPickupsOnBattleEnd`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `pop_corpses` | Boolean | `true` |  |

</details>

---

### Context: `Conditional_DoesDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Bleed` | [`Array`](./Arrays.md#array-bleed) | `[ 1 .1 ]` | Applies the 'Bleed' effect. |

</details>

---

### Context: `Conditional_SourceHasTag`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `crow` | The specific entity tag required or applied. |

</details>

---

### Context: `DelayedWind`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `distance` | Number | `2` | The area of effect or distance in tiles. |

</details>

---

### Context: `DelayedWindCone`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `distance` | Number | `10` | The area of effect or distance in tiles. |

</details>

---

### Context: `ForceMoveAway`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `free` | Boolean | `false` |  |

</details>

---

### Context: `MoveWhenDamaged`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `weights` | [`Enum/String`](./Enums.md#enum-weights) | `stay_far_always_move` |  |

</details>

---

### Context: `Robot`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `allow_energize_self` | Boolean | `true` |  |

</details>

---

### Context: `ScaledStatusOnBleedDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | `2` | Applies the 'Charge' effect. |

</details>

---

### Context: `ScaledStatusOnLoseShield`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Thorns` | Number | `1` | Applies the 'Thorns' effect. |

</details>

---

### Context: `ScaledStatusOnOverHealed`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `SpawnScaledRotFly` | Number | `1` | Applies the 'SpawnScaledRotFly' effect. |

</details>

---

### Context: `StatusAlliesOnSpendMana`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ManaGain` | Number | `1` | Applies the 'ManaGain' effect. |

</details>

---

### Context: `StatusAlliesScaledByCursedOnDeath`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `LuckUp` | Number | `1` | Applies the 'LuckUp' effect. |

</details>

---

### Context: `StatusIfBattleAlreadyBegan`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `PermanentMadness` | Number | `1` | Applies the 'PermanentMadness' effect. |

</details>

---

### Context: `StatusOnEatPill`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `3` | Applies the 'AllStatsUp' effect. |

</details>

---

### Context: `StatusOnGainCoins`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DivineShield` | Number | `1` | Applies the 'DivineShield' effect. |

</details>

---

### Context: `StatusOnLoseShield`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Thorns` | Number | `1` | Applies the 'Thorns' effect. |

</details>

---

### Context: `StatusOnTakeHealthDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `PermanentConstitution` | Number | `-1` | Applies the 'PermanentConstitution' effect. |

</details>

---

### Context: `TakeBonusTurnWithStatus`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Madness` | Number | `1` | Applies the Madness debuff/status effect. |

</details>

---

### Context: `TheHunger`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Madness` | Number | `1` | Applies the Madness debuff/status effect. |

</details>

---

### Context: `4`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `5`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `6`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `7`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `8`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `9`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `AddStatusToMeleeDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `AddStatusToReceivedDamage_ExcludeStatuses`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `BoobyTrapItems`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Conditional_NotBoss`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `DamageNeighborTilesWhenCastSpell`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `ElementalAttunement`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `ExtraStatusWhenDealingDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `PassiveUntilCastSpell`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `PassiveUntilGetKill`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `RandomPassivePool`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `ScaledStatusOnSpendMana`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `StatusAdjacentOnTheirTurnBegin`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `StatusEachTurnEndPerEnemyKill`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `StatusKillers`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `StatusOnGainShield`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

